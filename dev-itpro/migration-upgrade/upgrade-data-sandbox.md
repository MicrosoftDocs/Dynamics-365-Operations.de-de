---
title: Datenaktualisierung in einer Sandkastenumgebung
description: "In diesem Thema wird erläutert, wie eine Datenaktualisierung vom AX 2012 zu Dynamics 365 for Finance and Operations in einer Sandboxumgebung ausgeführt wird."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: de-de
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>Datenaktualisierung in einer Sandkastenumgebung

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Die Ausgabe dieser Aufgabe ist eine aktualisierte Datenbank, die Sie in einer Sandboxumgebung verwenden können. Eine Sandboxumgebung ist eine Umgebung, in der Geschäftsbenutzer und funktionale Teammitglieder Anwendungsfunktionen prüfen können. Diese Funktionen umfassen Anpassungen und die Daten, die aus Microsoft Dynamics AX 2012 eingefügt wurden.

Es wird dringend empfohlen, dass Sie die Datenaktualisierung in einer Entwicklungsumgebung ausführen, bevor Sie sie in einer freigegebenen Sandboxumgebung ausführen, da dieser Ansatz die Gesamtzeit reduzieren kann, die für eine erfolgreiche Datenaktualisierung erforderlich ist. Weitere Informationen finden Sie unter [Datenaktualisierung in einer Entwicklungsumgebung](prepare-data-upgrade.md)

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>Überblick über den Aktualisierungsprozess von Sandkastendaten

Bevor Sie beginnen, Daten in einer Sandboxumgebung zu aktualisieren, haben Sie bereits Daten in einer Entwicklungsumgebung aktualisiert, wie erläutert in [Datenaktualisierung in einer Entwicklungsumgebung](prepare-data-upgrade.md) Die zwei Prozesse sind sehr ähnlich. Der Hauptunterschied ist, dass eine Sandboxumgebung Datenbank Microsoft Azures SQL für die Entwicklungsumgebung verwendet, während eine Entwicklungsumgebung Microsoft SQL Server verwendet. Diese technische Differenz in der Datenbankebene setzt voraus, dass Sie die Datenaktualisierungsprozedur in einer Sandboxumgebung ändern, da eine Sicherungskopie der Datenbankinstanz AX 2012 nicht in die SQL-Datenbank zurück geändert werden kann.

![Sandkastendaten-Aktualisierungsprozess](./media/data-upgrade-sandbox.png)

Hierbei gelten die allgemeinen Schritte im Aktualisierungsprozess.

1. Eine Kopie der AX 2012 Datenbank erstellen. Es wird dringend empfohlen, dass Sie eine Kopie verwenden, da Sie einige Objekte löschen müssen, die exportiert werden.
2. Exportiert die kopierte Datenbank in eine bacpac Datei, indem ein kostenloses SQL Server-Tool verwendet wird, das SQLPackage.exe. Dieses Tool stellt eine spezielle Art Datenbanksicherung dar, das in die SQL-Datenbank in importiert werden kann.
3. Laden Sie die bacpac Datei in den Azure Storage hoch.
4. Laden Sie die Datei bacpac auf die Application Object Server (AOS)- Maschine in der Sandkastenumgebung und importieren Sie diese anschließend, indem Sie SQLPackage.exe verwenden. Sie müssen ein Skript für die importierte Datenbank ausführen, um die SQL-Datenbankbenutzer zurückzusetzen.
5. Führen Sie das MajorVersionDataUpgrade.zip-Paket aus, um die Datenbank für die Datenaktualisierung gegen die importierte Datenbank auszuführen.

## <a name="create-a-copy-of-the-ax-2012-database"></a>Eine Kopie der AX 2012 Datenbank erstellen.

Sie müssen eine Kopie der AX 2012-Datenbank erstellen, die Sie aktualisieren möchten, da Sie einige Objekte aus der Datenbank löschen müssen. Diese Objekte enthalten alle Microsoft Windows-Authentifizierungsbenutzer. Diese Änderungen machen die geänderte Datenbank unbrauchbar für AX 2012. Im Rahmen dieses Schritts erstellen Sie eine Kopie der Datenbank und löschen diese Objekte.

Dieser Schritt muss der Datenbankadministrator (DBA) oder eine Person ausführen, die ähnliches Wissen und Erfahrung hat.

Um eine Datenbankkopie zu erstellen, können Sie eine Sicherungskopie der ursprünglichen Datenbank erstellen und sie unter einem neuen Namen wiederherstellen. Überprüfen Sie, ob ausreichend Platz für beide Datenbanken verfügbar ist. Sie können die Kopie auf einem anderen Server erstellen. Die Version der SQL Server-Instanz, die die Datenbank ausführt, ist nicht relevant.

Das folgende Beispiel des Codes, der eine Datenbankkopie erstellt. Sie müssen dieses Beispiel ändern, um den spezifischen Datenbanknamen widerzuspiegeln.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Nachdem die Kopie erstellt wurde, führen Sie das folgende Transact-SQL Skript (T -SQL) aus.
VORGEHEN 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>Exportiert die kopierte Datenbank in eine Datei bacpac

Exportiert die kopierte Datenbank in eine bacpac Datei, indem ein kostenloses SQL-Server-Tool verwendet wird, das SQLPackage.exe. Dieser Schritt sollte vom Datenbankadministrator oder einem Teammitglied mit entsprechendem Wissen gemacht werden.

Es ist außerordentlich wichtig, dass Sie die neueste Version von SQL Server Management Studio einrichten, bevor Sie diesen Schritt starten. Obwohl SQLPackage in früheren Versionen von Management Studio vorhanden ist, ist es nicht ordnungsgemäß für diesen Schritt konfiguriert, es sei denn, wenn die aktuelle Version eingerichtet wird.

Dieser Schritt ist wichtig, da der Export erneut ausgeführt werden muss, vor der Ausfallzeiten und vor dem Go Live. Nachfolgend finden Sie einige Beispiele:

- Der bacpac Prozess ist sehr E/A und CPU intensiv. Daher führen Sie den Export auf einer leistungsstarken Maschine aus.
- SQLPackage soll auf der Maschine lokal ausgeführt werden, auf der sich die Datenbank befindet. Führen Sie nicht das SQLPackage auf einem lokalen Laptop aus, den Sie mit der Datenbankmaschine verbinden, da dieser Prozess auch Netzwerk intensiv ist.

Öffnen Sie eine Eingabeaufforderung **Command Prompt** im Administratormodus, und führen Sie den folgenden Befehl aus: 

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Hier ein Überblick über die Parameter:

- **ssn** (Quellservername) – Der Name der SQL Server-Instanz, von der exportiert wird. Für unseren Prozess sollte dieser Parameter **"localhost "** auf "Immer" festgelegt werden.
- **sdn** (Quelldatenbankname) – Der Name der Datenbank, die zu exportieren ist.
- **tf** (Zieldatei) – Der Pfad und Name der Datei, die exportiert werden sollen. Der Ordner muss vorhanden sein, doch die Datei wird vom Prozess erstellt.
- **/p:CommandTimeout** – Der Pro-Abfragentimeoutwert. Dieser Parameter aktiviert die größeren Tabellen, damit sie ohne Timeout exportiert werden können.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Laden Sie die bacpac Datei in den Azure Storage hoch

Laden Sie die bacpac Datei in den Azure Storage hoch. Weitere Informationen finden Sie unter UsingStorageExplorer.docx AUFGABE

### <a name="import-the-bacpac-file-into-sql-database"></a>SQL-Datenbank in die Modelldatenbank importieren

Im Rahmen dieses Schritts importieren Sie die exportierte bacpacortierte Datei an die SQL-Datenbankinstanz, die Ihre Sandboxumgebung verwendet. Sie müssen die neueste Version von Management Studio auf der Maschine der Sandbox AOS installiert haben. Importieren Sie die Datei dann, indem Sie das SQLPackage.exe-Tool verwenden.

Diese Aufgaben können Sie direkt in der AOS-Maschine in der Sandboxumgebung ausführen, da es die Firewallregeln gibt, die den Zugriff auf die SQL-Datenbankinstanz einschränken. Wenn Sie die AOS-Maschine verwenden, können Sie Zugriff erhalten.

Wir für den Exportschritt müssen Sie die neueste Version von Management Studio haben, bevor Sie den Import starten können. Dieser Schritt funktioniert nicht, wenn Sie eine ältere Version haben.

Aus Leistungsgründe empfehlen wir, dass Sie die Datei bacpac auf das Laufwerk D auf der AOS-Maschine sperren. Auf Azure virtuellen Computern (VMs) ist Laufwerk D eine physische Diskette, die üblicherweise höhere Leistung als andere verfügbare Disketten hat.

Öffnen Sie ein Fenster **Command Prompt** im Administratormodus, und führen Sie den folgenden Befehl aus: 

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Hier ein Überblick über die Parameter:

- **tsn** (Zielservername) – Der Name des SQL Azure Servers für den Import. Der Name findet man unter LCS. Suffix mit **.database.windows.net**.
- **sdn** (Quelldatenbankname) – Der Name der Datenbank, die zu importieren ist. Die Datenbank muss noch nicht vorhanden sind. Beim Importprozess erstellt sie.
- **tf** (Zieldatei) – Der Pfad und Name der Datei, von denen, die importiert werden sollen.
- **TP** (Zielkennwort) – Das für die SQL-Kennwort Ziel SQL Datenbankinstanz.
- **tu** (Zielnutzer) – Das ie SQL-Kennwort für die Ziel SQL Datenbankinstanz. Es wird empfohlen, eine Stapelverarbeitung **squladmin** zu verwenden. Sie können das Kennwort für diesen Benutzer aus dem LCS-Projekt abrufen.
- **/p:CommandTimeout** – Der Pro-Abfragentimeoutwert. Dieser Parameter aktiviert die größeren Tabellen, damit sie ohne Timeout exportiert werden können.
- **/p: DatabaseServiceObjective** – Das Service-Ebenenniveau der Datenbank, die erstellt wird. Sie können den Wert für die vorhandene Datenbank überprüfen, indem Sie Management Studio verwenden. Klicken Sie mit der rechten Maustaste auf das Feld ,**Eigenschaften**,

Nachdem Sie die Befehle ausgeführ haben, erhalten Sie die folgende Warnung. Sie können ignoriert werden.

![Sandboxfehler](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>Führen Sie das MajorVersionDataUpgrade.zip-Paket aus

Führen Sie das zur Bereitstellung geeignete Paket der Datenaktualisierung aus, wie unter beschrieben [Aktualisieren von Daten in der Entwicklungs-, in der Vorführung oder in der Sandboxumgebung](upgrade-data-to-latest-update.md).

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>Datenaktualisierung in einer Entwicklungsumgebung

Es ist ratsam, die gleiche Datenbank in einer Entwicklungsumgebung zu aktualisieren. Wenn Sie eine Kopie der Datenbank haben, für die die Entwicklungsumgebung verfügbar ist, ist es einfacher, Fehler zu prüfen, die in der aktualisierten Sandboxumgebung gefunden werden.

