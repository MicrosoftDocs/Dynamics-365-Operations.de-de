---
title: Fehlercodes für die Systemdiagnose der Tabellenzuordnung
description: In diesem Thema werden Fehlercodes für die Systemdiagnose der Tabellenzuordnung beschrieben.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 4f0b92a6bc6c051a6bb24b49d3280ca5ecea3625
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725074"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Fehlercodes für die Systemdiagnose der Tabellenzuordnung

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden Fehlercodes für die Systemdiagnose der Tabellenzuordnung beschrieben.

## <a name="error-100"></a>Fehler 100

Die Fehlermeldung lautet: „Mindestens erforderliche Finance and Operations Plattformversion ist PU 43 zum Ausführen von Finance and Operations-Empfehlungen.“

Die Funktion erfordert Plattform-Updates für Version 10.0.19 oder höher von Finance and Operations-Apps.

## <a name="error-400"></a>Fehler 400

Die Fehlermeldung lautet: „Keine Registrierungsdaten für Geschäftsveranstaltungen für die Entität \{Finance and Operations UniqueEntityName\} gefunden. Das bedeutet, dass entweder die Karte nicht ausgeführt wird oder alle Feldzuordnungen unidirektional sind.“

## <a name="error-500"></a>Fehler 500

Die Fehlermeldung lautet: „Keine Projektkonfigurationen für Projekt \{Projektname\} gefunden. Dies kann entweder sein, dass das Projekt nicht aktiviert ist oder alle Feldzuordnungen unidirektional vom Kundenengagement zu Finance and Operations sind.“

Überprüfen Sie die Zuordnungen für die Tabellenzuordnung. Wenn sie unidirektional von Kundenbindungs-Apps zu Finance and Operations-Apps sind, wird kein Datenverkehr für die Live-Synchronisierung von Finance and Operations-Apps zu Dataverse generiert.

## <a name="error-900"></a>Fehler 900

Die Fehlermeldung lautet: „Ungültiger Quellfilter \{sourceFilter\} Format für Entität \{Finance and Operations UniqueEntityName\}.“

Der Quellfilter, der in der Tabellenzuordnung für Finance and Operations-Apps angegeben ist, ist syntaktisch nicht korrekt. Um die Filterkriterien zu validieren, siehe [Beheben von Problemen mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Fehler 1000

Die Fehlermeldung lautet: „Entity \{Finance and Operations UniqueEntityName\} Abfrage, die für die Dual-Write-Live-Synchronisierung verwendet wird, ist \{Finance and Operations EntityFilterQueryString\}. Datensätze, die die Abfragekriterien erfüllen, werden für die Live-Synchronisierung abgeholt.“

Die zurückgegebene Entitätsabfrage ist die unterstützende SQL-Abfrage für die Entität. Suchen Sie in der Abfrage nach Inner Joins oder Filtern, die die Geschäftsdaten bestimmen, die für die Livesynchronisierung abgerufen werden. Inner Joins und Filter sind obligatorische Bedingungen, die für jeden Datensatz erfüllt sein müssen, der für die Dual-Write-Livesynchronisierung aufgenommen wird.

## <a name="error-1300"></a>Fehler 1300

Die Fehlermeldung lautet: „Virtuelle Felder \{s.EntityFieldName\} für Entität \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} wird möglicherweise nicht für Dual-Write verfolgt.“

Virtuelle Felder von Finance and Operations-Tabellen sind nicht für das Tracking aktiviert. Die Live-Synchronisierung kann die Daten synchronisieren, aber die Änderungen, die an den Spalten vorgenommen wurden, können nicht übernommen werden.

## <a name="error-1500"></a>Fehler 1500

Die Fehlermeldung lautet: „Es sollte mindestens ein Feld einem Nicht-Nachschlagefeld für die Kundenbindung zugeordnet sein, um die Verfolgung der Datenquelle \{datasource.DataSourceName\} zu ermöglichen.“

Die Datenquelle aus der Entität hat kein Feld, das für Dual-Write zugeordnet ist. Änderungen an der zugrunde liegenden Tabelle werden für Dual-Write nicht nachverfolgt.

## <a name="error-1600"></a>Fehler 1600

Die Fehlermeldung lautet „Datenquelle: \{datasource.DataSourceName\} für Entität \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} hat eine Reichweite. Nur Datensätze, die die Bereichsbedingung erfüllen, werden für den Outbound abgeholt.“

Entitäten in Finance and Operations-Apps können Datenquellen haben, in denen Filterbereiche aktiviert sind. Diese Bereiche definieren die Datensätze, die als Teil der Live-Synchronisierung erfasst werden. Wenn einige Datensätze von Finance and Operations Apps zu Dataverse übersprungen werden, überprüfen Sie, ob die Datensätze die Bereichskriterien für die Entität erfüllen. Eine einfache Möglichkeit, diese Überprüfung durchzuführen, besteht darin, eine SQL-Abfrage auszuführen, die dem folgenden Beispiel ähnelt.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Fehler 1700

Die Fehlermeldung lautet: „Tabelle: \{datasourceTable.Key.subscribedTableName\} für Entität \{datasourceTable.Key.entityName\} wird für Entität \{origTableToEntityMaps.EntityName\} verfolgt. Dieselben Tabellen, die für mehrere Entitäten verfolgt werden, können sich auf die Systemleistung für Live-Synchronisierungstransaktionen auswirken.“

Wenn dieselbe Tabelle von mehreren Entitäten verfolgt wird, löst jede Änderung an der Tabelle eine Dual-Write-Auswertung für die verknüpften Entitäten aus. Obwohl die Filterklauseln nur die gültigen Datensätze senden, kann die Auswertung bei Abfragen mit langer Ausführungszeit oder nicht optimierten Abfrageplänen zu Leistungsproblemen führen. Dieses Problem ist aus geschäftlicher Sicht möglicherweise nicht vermeidbar. Wenn jedoch viele sich überschneidende Tabellen über mehrere Entitäten hinweg vorhanden sind, sollten Sie erwägen, die Entität zu vereinfachen oder Optimierungen für Entitätsabfragen zu überprüfen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
