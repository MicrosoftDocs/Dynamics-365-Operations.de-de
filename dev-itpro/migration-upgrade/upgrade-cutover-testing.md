---
title: "Übernahmetest aktualisieren"
description: "In diesem Thema wird erläutert, wie Sie die Aufgaben testen, die auftreten, nachdem Sie AX 2012 beenden, jedoch bevor Sie Dynamics 365 for Finance and Operations, Enterprise Edition aktivieren."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
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
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: de-de
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>Übernahmetest aktualisieren

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Übernahme* ist die Bedingung, die Sie für den endgültigen Prozess des Abrufens eines neuen Live Systems verwenden. Dieser Übernahme-Prozess besteht aus den Aufgaben, die auftreten, wenn Sie Microsoft Dynamics AX 2012 verlassen, aber bevor Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, eingeschaltet wird. Der Zweck des Übernahmetests ist es, den Übernahmeprozess zu üben, mit dessen Hilfe eine nahtlose  Erfahrung für alle Beteiligten während der tatsächlichen Übernahme vor dem Go-Live sichergestellt wird.

Es gibt zwei Hauptarbeitsstreams währen der Übernahme:

- **Technischer Workstream** – Dieser Workstream umfasst den Datenaktualisierungsausführungsprozess. Ihr Unternehmen setzt eine Grenze für den Betrag der zugelassenen Ausfallzeiten. Während dieser Ausfallzeiten sind weder AX 2012 noch Finance and Operations verfügbar. Dieser Workstream muss den Datenaktualisierungsprozedur optimieren, um dej Ausfallzeitanforderungen der Unternehmung zu entsprechen.
- **Funktionaler Workstream** – Dieser Workstream umfasst die Konfigurationsaufgaben, die ausgeführt werden, nachdem der Upgrad abgeschlossen ist. Alle diese Aufgaben müssen dokumentiert und mengenmäßig bestimmt werden, und eine Ressource muss zugewiesen werden, da die funktionale Aufgabe und die technische Aufgabe in die genehmigte Ausfallzeit des Unternehmens passen muss.

Die folgende Abbildung zeigt den gesamten Übernahmeprozess bis zum Go Live an, da diese in der Produktionsumgebung auftritt.

![Übernahmeprozess](./media/cutover_1.png)

Dieser Übernahmeprozess unterscheidet sich von einer grundlegenden Datenaktualisierung in einer Sandboxumgebung wie folgt:

- Die AX 2012-Datenbank wird nicht kopiert, sondern nur unterstützt, und anschließend wird die ursprüngliche Datenbank geändert. Dieser Ansatz ist schneller und die Sicherung bietet einen Rückhalt, sollte dies erforderlich sein.
- Da die Produktionsumgebung für Finance and Operations eingeschränkten Zugriff hat, werden die Aufgaben, die zuvor auf der Sandboxinstanz AOS Application Object Server (AOS) ausgeführt wurden, jetzt vom  Microsoft DSE Team ausgeführt. Dazu zählen das Herunterladen und Importieren der bacpac Datei und Ausführung des MajorversionDataUpgrade.zip-Pakets.
- Hier können Sie folgende Aufgaben ausführen:

    - Ausführen einer Feuerprobe.
    - Schließen Sie Anwendungseinstellungsaufgaben ab. Dieser Schritt kann umfangreich sein, abhängig von der Funktionen, die verwendet werden. Im Rahmen dieses Schritts konfiguriert das funktionale Team Neuanmeldungsfunktionen, damit es bereit ist, im aktualisierten System verwendet werden zu können.
    - Zugriff von Benutzern zulassen. Melden Sie die Benutzerbasis, dass die Aktualisierung abgeschlossen ist und dass sie System erneut verwenden können.

## <a name="technical-workstream"></a>Technische Aufgabe

Die technische Aufgabe umfasst verschiedene technische Teammitglieder: der Datenbankadministrator (DBA), der AX-2012-Systemadministrator, die Serveradministratoren und die Entwickler, die mit AX 2012 und Finance and Operations vertraut sind. In diesem Thema wird erläutert, welche Aufgaben diese Rollen umfassen.

Während der Übernahme wird sich das Team auf technische Leistung und Zuverlässigkeitstests der Datenaktualisierung konzentrieren, um sicherzustellen dass die genehmigt Ausfallzeit des Unternehmens eingehalten wird. Viele der Elemente der Hardware und Software werden in diesen Prozess invoviert sein. Einige dieser Elemente sind lokal, während andere in der Microsoft-Cloud sind. Darüber hinaus werden viele Elemente des benutzerdefinierten Anwendungscodes und des standardmäßigen Codes beteiligt sein. Das Ergebnis dieser Tests sollte im Übernahmeprozess für Ihre Umgebung als Vertrauensbasis dienen.

### <a name="turn-off-the-ax-2012-aos-instances"></a>AX 2012 ASO-Instanzen ausschalten

Diese Aufgabe umfasst AX 2012-Systemadministratoren und die Serveradministratoren.

Die folgenden Bereiche sollten überprüft werden:

- **Stapelverarbeitungsaufträge, die zum Zeitpunkt der Übernahme ausgeführt werden** – Ein Stapelverarbeitungsauftrag mit langer Laufzeit, der bereits begonnen wurde, verhindert, dass das System beendet werden kann. Planen Sie voraus, damit Sie die AOS-Instanzen im gewünschten Moment abschließen können. Möglicherweise müssen Sie Chargen so planen, dass Sie ausgeführt werden, bevor Sie AX 2012 abschalten.
- **Integrierte Systeme** – Sie haben möglicherweise anderen Systeme, die in die AX 2012 Umgebung integriert werden. Sie müssen diesen Faktor berücksichtigen, wenn Sie AX 2012 ausschalten möchten. So müssen Sie möglicherweise die integrierten Systeme einige Zeit ausschalten, bevor Sie AX 2012 auch beenden, damit alle restlichen Betriebsbuchungen abgeschlossen werden können. Die Anforderungen für integrierte Systeme variieren von Unternehmen zu Unternehmen. Daher müssen die Expertengruppen für dieses Szenarios unabhängig planen.

### <a name="create-a-backup-of-the-ax-2012-database"></a>Erstellen Sie eine Datensicherung der AY 2012 Datenbank.

Diese Aufgabe umfasst den Datenbankadministrator. Die Datensicherung wird verwendet, wenn ein Rollback erforderlich ist. Sie wird zudem als Referenzpunkt verwendet, der während einer Periode aufbewahrt wird und zeigt den Systemstatus zum Zeitpunkt der Übernahme an.

Die folgenden Bereiche sollten überprüft werden:

- Erhalten Sie konkrete zeitliche Steuerungen für den Backup-Prozess.
- Passen Sie die Backup-Optionen an, die verwendet werden (beispielsweise Komprimierung, Nicht-Komprimierung), um die schnellstmögliche Sicherung sicherzustellen.

### <a name="export-the-database-to-bacpac"></a>Die Datenbank in bacpac exportieren

Diese Aufgabe umfasst den Datenbankadministrator. Die Ausgabe dieser Aufgabe ist die Exportdatei, die auf Microsoft Azure für das System neu hochgeladen wurde.

Die folgenden Bereiche sollten überprüft werden:

- Erhalten Sie konkrete zeitliche Steuerungen für den Backup-Prozess.
- Optimieren Sie, um den Exportvorgang zu unterstützen, um die schnellstmögliche Erfahrung sicherzustellen. Die Optimierung kann die folgenden Aufgaben vorschreiben:

    - Messen Sie Systemressourcen während des Exports, wie CPU, und E/A Disketten-Arbeitsspeicher.
    - Wenn Ressourcenengpässe gefunden werden, erstellen Sie einen Plan, sie zu minimieren. Normalerweise minimieren Sie Engpässe, indem Sie mehr der erforderlichen Ressource zuordnen.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Laden Sie die bacpac Datei in den Azure Storage hoch

Diese Aufgabe umfasst den Datenbankadministrator oder die Serveradministratoren. Während dieser Aufgabe wird bacpac die Datei in Azure verschieben.

Die folgenden Bereiche sollten überprüft werden:

- Wählen Sie den Computer, der für den Upload verwendet wurde und überprüfen Sie, ob Azure konfiguriert und das Speicherexplorertool einsatzbereit sind.
- Erhalten Sie konkrete zeitliche Steuerungen für den Uploadvorgang, indem Sie ihn mehrmals messen. Uploadzeiten variieren, auf Grundlage Ihrer Internetverbindung und der Geschwindigkeit der geografischen Position von Azure in Bezug auf ein Datencenter Ihres Standorts.

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>Laden Sie die bacpac Datei herunter und importieren Sie diese in die Datenbank Azures SQL.

Wenn diese Aufgabe am Go Live passiert, wird sie vom Team Microsoft DSE ausgeführt. Allerdings wird während den Übernahmetests Ihr DBA involviert. Die Ausgabe dieser Aufgabe ist die Exportdatei, die auf Microsoft Azure für das System neu hochgeladen wurde.

Die folgenden Bereiche sollten überprüft werden:

- Erhalten Sie konkrete zeitliche Steuerungen für den Import-Prozess.
- Optimieren Sie, um den Exportvorgang zu unterstützen, um die schnellstmögliche Erfahrung sicherzustellen. Die Optimierung kann die folgenden Aufgaben vorschreiben:

    - Messen Sie Systemressourcen beim Export. Nachfolgend finden Sie einige Beispiele:

        - **Auf der AOS-Maschine:**, CPU Diskette E/A und Speicher
        - **Auf der Azure SQL Datenbankinstanz** SQL Datenbankdurchsatz (DTU). Sie können Azure SQL DTU von Microsoft SQL Server Management Studio auf der AOS-Maschine überwachen, indem Sie die sys.dm_resource_stats-Systemansicht berücksichtigen.

    - Wenn Ressourcenengpässe gefunden werden, erstellen Sie einen Plan, sie zu minimieren. Normalerweise minimieren Sie Engpässe, indem Sie mehr der erforderlichen Ressource zuordnen. Da diese Maschine von Microsoft gehostet ist, müssen Sie eine Anforderung an Microsoft für die  Erhöhung  der Betriebsmittel senden, wenn Sie bestimmen, dass dies die Engpassressource sind.

### <a name="run-the-majorversiondataupgradezip-package"></a>Führen Sie das MajorVersiondataUpgrade.zip-Paket aus

Wenn diese Aufgabe am Go Live passiert, wird sie vom Team Microsoft DSE ausgeführt. Allerdings wird während den Übernahmetests Ihr Entwickler involviert. Während dieser Aufgabe wird die alte Datenbankstruktur der Struktur des neuen Systems angepasst.

Die Datenbanksynchronisierungsprozessausführungen ist Teil dieser Aufgabe. Die Datenbanksynchronisierung kann ziemlich lang dauern, beispielsweise wenn ein gruppierter Index auf einer Tabelle geändert hat, weil der Arbeitsgang ein Arbeitsgang mit SQL ist.

Es wird dringend empfohlen, dass Sie zuerst den Analyse- und Debuggingsprozess in einer Entwicklungsumgebung ausführen. In einer Sandboxumgebung sind Debuggings- und Analyseoptionen beschränkt. Die Zielsetzung besteht darin, geringste oder keine Probleme zu haben, die behoben werden müssen, wenn Sie Übernahmetests ausführen.

Die folgenden Bereiche sollten überprüft werden:

- Erhalten Sie konkrete zeitliche Steuerungen für den Import-Prozess.
- Optimieren Sie den Prozess, um die schnellstmögliche Erfahrung sicherzustellen. Die Optimierung kann die folgenden Aufgaben vorschreiben:

    - Überwachen von einzelnen Aktualisierungsscrips über die ReleaseUpdateScriptsExecutions-Tabelle.
    - Passen Sie Skripts an, um die Leistung zu optimieren. Diese Aufgabe kann vorschreiben, dass Sie ein Scrip X++-Code anpassen, um Sie für Ihr Datenset zu optimieren.
    - Azure SQL DTU überwachen, indem Sie Microsoft Dynamics Lifecycle Services (LCS)- Überwachung oder die sys.dm_resources_stats-Systemansicht in Management Studio verwenden. Wenn Ressourcen maximiert werden, müssen Sie möglicherweise eine höhere Datenbankebene vom Team Microsoft DSE anfordern.

### <a name="roll-back-to-ax-2012"></a>Zurücdk auf AX 2012

Das Ziel dieser Aufgabe ist es, Datenbankfeinabstimmungen zurücksetzen, indem die Sicherung, die erstellt wurde, als AX 2012 deaktiviert wurde, wieder verwendet und AX 2012 wieder aktiviert wird. Der Zustand des integrierten Systems muss möglicherweise auch wiederhergestellt werden. Da sich jedoch integrierte Systeme von Unternehmen zu Unternehmen unterscheiden, müssen Sie für dieses Szenarios, basierend auf Ihren speziellen Umständen unabhängig planen. Obwohl es unwahrscheinlich ist, dass Sie eine Übernahme machen müssen, ist es sehr wichtig, dass Sie einen Prozess getesteten haben, wenn Sie diesen erfordern würden.

## <a name="functional-workstream"></a>Funktionale Aufgabe

Nach einer Datenaktualisierung werden mehrere Konfigurationsaufgaben in der neuen Umgebung erforderlich. Ziel dieses Arbeitsstreams ist es, alle Konfigurationsaufgaben zu dokumentieren und zu quantifizieren und  Aufgaben zuweisen, um sicherzustellen, dass diese Aufgaben zusammen mit dem technischen Workstream während des Ausfallzeitfensters ausgeführt werden können.

Normalerweise erfordern funktionale Aufgaben einen Wechsel der Werte für bestimmte Systemparameter oder anderer Konfigurationsdaten. Diese Aufgaben werden mit Funktionsprüfungen erfolgreich identifiziert, was einer separaten Aktivitäten aus den Übernahmetests ist. Wenn eine Aufgabe dieses Typs identifiziert wird, sollte diese zusammenmit der funktionalen Ressource und Ihrem Entwickler geprüft werden.

Größere Änderungen erfordern möglicherweise, dass ein neues benutzerdefiniertes Datenaktualisierungsskript geschrieben wird, um die Daten zu aktualisieren während der Datenaktualisierung. Allerdings kann die funktionale Ressource kleineren Änderungen durch das neue System vornehmen, nachdem die Daten aktualisiert worden sind.

Größere Änderungen, die neue Aktualisierungsskripts haben, müssen getestet werden. Daher muss mindestens eine weitere Iterationen des MajorVersionDataUpgrade.zip-Pakets ausgeführt werden. Es ist wichtig, dass Sie die Kosten für das Paket für die Kosten der manuellen Dateneingabe erneut ausführen.

Für jede manuelle Änderung muss eine Aufgabe für das Uergangsplandokument hinzugefügt werden. Diese Aufgabe muss die folgenden Details anzeigen:

-   Welches ist die Aufgabe und was muss getan werden?
-   Wer muss es tun?
-   Wie lang wird es dauern?

