---
title: Datenbankprotokollierung konfigurieren und verwalten
description: Sie können Änderungen an Tabellen und Feldern in Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5b8641655cf31453f6fc11e2056fb6bf96a43cbc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696262"
---
# <a name="configure-and-manage-database-logging"></a>Datenbankprotokollierung konfigurieren und verwalten


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können Änderungen an Tabellen und Feldern in Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen. In diesem Thema wird beschrieben, wie:

- Verwalten Sie Sicherheit und Leistung für die Datenbankprotokollierung
- Datenbankprotokollierung einrichten
- Bereinigen Sie Datenbankprotokolle

## <a name="overview-of-database-logging"></a>Übersicht über die Datenbankprotokollierung

Sie können Änderungen an Tabellen und Feldern in Microsoft Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen. Diese Änderungen umfassen das Einfügen, Aktualisieren oder Löschen. Die Datenbankprotokollierung speichert eine Aufzeichnung der Änderungen an Tabellen oder Feldern in der Datenbankprotokolltabelle.

Die geschäftlichen Verwendungen der Datenbankprotokollierung umfassen:

- Erstellen eines Überwachungsdatensatzes mit Änderungen an bestimmten Tabellen, die vertrauliche Informationen enthalten.
- Verfolgung einzelner Transaktionen. Die Datenbankprotokollierung dient nicht zur Verfolgung automatisierter Transaktionen, die in Stapeljobs ausgeführt werden.

## <a name="security-for-database-logging"></a>Sicherheit für die Datenbankprotokollierung

Datenbankprotokolle können sensible Daten enthalten. Beschränken Sie den Zugriff auf Sicherheitsrollen, die Zugriff auf die Protokolldaten benötigen.

## <a name="database-logging-and-performance"></a>Datenbankprotokollierung und Leistung

Die Datenbankprotokollierung kann zwar aus geschäftlicher Sicht hilfreich sein, sie kann allerdings auch eine hohe Ressourcenauslastung sowie einen hohen Verwaltungsaufwand bedeuten. Die Leistungsbeeinträchtigungen der Datenbankprotokollierung umfassen:

- Die Datenbankprotokolltabelle kann schnell wachsen und die Größe der Datenbank erhöhen. Das Wachstum hängt von der Menge der protokollierten Daten ab, die Sie behalten möchten. Standardmäßig verwaltet die Datenbankprotokolltabelle nur 30 Tage Protokolldaten. 

- Die Datenbankprotokollierung kann sich nachteilig auf lang laufende automatisierte Prozesse auswirken, z. B. auf lang laufende Datenimporte.

### <a name="best-practices"></a>Optimale Verfahren

Wählen Sie zum Eingrenzen der Anzahl von Protokolleinträgen und zur Steigerung der Leistung nur die jeweils gewünschten Felder für die Protokollierung und keine vollständigen Tabellen aus. Um die Gesamtleistung aufrechtzuerhalten, ist die Datenbankprotokollierung auf 20 Tabellen beschränkt.

> [!NOTE]
> Für einzelne Feldern können nur Aktualisierungen protokolliert werden.

## <a name="set-up-database-logging"></a>Datenbankprotokollierung einrichten

Sie können den Assistent **Protokollieren von Datenbankänderungen** zum Einrichten der Datenbankprotokollierung verwenden. Der Assistent bietet eine flexible Möglichkeit, die Protokollierung für Tabellen oder Felder einzurichten.

1. Gehen Sie zu **Systemadministration> Links> Datenbank> Datenbankprotokoll einrichten**. Wählen Sie **Neu** aus, um den Assistent **Protokollieren von Datenbankänderungen** zu starten.
2. Wählen Sie **Weiter**. 
3. Wählen Sie auf der Seite **Tabellen und Felder** des Assistenten die Tabellen und Felder aus, für die Sie die Datenbankprotokollierung aktivieren möchten, und wählen Sie **Weiter** aus.

   > [!Note]
   > Die Datenbankprotokollierung ist nicht für alle Tabellen in der Personaldatenbank verfügbar. Wenn Sie **Alle Tabellen anzeigen** unterhalb der Liste auswählen, wird die Liste der Tabellen und Felder erweitert, um alle Datenbanktabellen anzuzeigen, für die die Datenbankprotokollierung verfügbar ist. Dies ist jedoch eine Teilmenge der vollständigen Liste der Datenbanktabellen.

4. Wählen Sie auf der Seite **Änderungstypen** des Assistenten die Datenvorgänge aus, für die Sie Änderungen für jede der Tabellen und Felder verfolgen möchten, und wählen Sie **Weiter**. In der folgenden Tabelle finden Sie eine Beschreibung der Datenvorgänge, die für die Protokollierung verfügbar sind.
5. Überprüfen Sie auf der Seite **Fertig stellen** die vorgenommenen Änderungen und wählen Sie **Fertig stellen**.

| Vorgang | Beschreibung |
| -- | -- |
| Neue Buchungen nachverfolgen | Erstellen Sie ein Protokoll für neue Datensätze, die in der Tabelle erstellt werden. |
| Buchen | Erstellen Sie ein Protokoll für Aktualisierungen von Tabellendatensätzen oder Aktualisierungen für einzeln ausgewählte Felder in der Tabelle. Wenn Sie auswählen, Aktualisierungen für die Tabelle zu protokollieren, wird jedes Mal ein Protokolldatensatz erstellt, wenn eine Aktualisierung an einem Feld eines Datensatzes in der Tabelle vorgenommen wird. Wenn Sie auswählen, Aktualisierungen für bestimmte Felder zu protokollieren, wird ein Protokolldatensatz nur erstellt, wenn Aktualisierungen an diesen Feldern von Tabellendatensätzen vorgenommen werden. |
| Löschen | Erstellen Sie ein Protokoll für Datensätze, die aus der Tabelle gelöscht wurden. |
| Schlüssel umbenennen | Erstellen Sie einen Protokolldatensatz, wenn ein Tabellenschlüssel umbenannt wird. |


## <a name="clean-up-database-logs"></a>Bereinigen Sie Datenbankprotokolle

Sie können alle oder einen Teil der Datenbankprotokolle mit den folgenden Optionen löschen:

- Wählen Sie alle Protokolle für eine bestimmte Tabelle aus.
- Wählen Sie bestimmte Arten von Datenbankprotokollen aus.
- Wählen Sie ein Datum und eine Uhrzeit aus, zu der ein Protokoll erstellt wurde.

Gehen Sie zum Einrichten der Datenbankprotokoll-Bereinigung folgendermaßen vor: 

1. Gehen Sie zu **Systemadministration> Links > Datenbank > Datenbankprotokoll einrichten**. Wählen Sie **Protokoll bereinigen**.
2. Wählen Sie unter der Überschrift **Einzuschließende Datensätze** die Option **Filter**.
3. Wählen Sie die Methode, mit der die zu löschenden Protokolle ausgewählt werden sollen. Geben Sie eine der folgenden Optionen ein:

   - Tabellenkennung (ID)
   - Art des Protokolls
   - Datum und Uhrzeit der Erstellung

4. Verwenden Sie die **Bereinigung des Datenbankprotokolls** Registerkarte, um festzulegen, wann die Protokollbereinigungsaufgabe ausgeführt werden soll. Standardmäßig sind Datenbankprotokolle 30 Tage lang verfügbar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
