---
title: Fehlercodes für die Systemdiagnose der Tabellenzuordnung
description: In diesem Thema werden Fehlercodes für die Systemdiagnose der Tabellenzuordnung beschrieben.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061277"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Fehlercodes für die Systemdiagnose der Tabellenzuordnung

[!include [banner](../../includes/banner.md)]



In diesem Thema werden Fehlercodes für die Systemdiagnose der Tabellenzuordnung beschrieben.

## <a name="error-100"></a>Fehler 100

Die Fehlermeldung lautet: „Für das Ausführen von Finance und Operations Empfehlungen ist mindestens die Plattformversion PU 43 erforderlich.“

Die Funktion erfordert Plattform-Updates für die Version 10.0.19 oder höher der Apps für Finanzen und Betrieb.

## <a name="error-400"></a>Fehler 400

Die Fehlermeldung lautet: „Für die Entität \{Finance und Operations UniqueEntityName\} wurden keine Daten zur Registrierung von Ereignissen gefunden. Das bedeutet, dass entweder die Zuordnung nicht ausgeführt wird oder alle Feldzuordnungen unidirektional sind.“

## <a name="error-500"></a>Fehler 500

Die Fehlermeldung lautet: „Keine Projektkonfigurationen für Projekt \{Projektname\} gefunden. Dies kann entweder daran liegen, dass das Projekt nicht aktiviert ist oder dass alle Zuordnungen von Feldern unidirektional vom Customer Engagement zu Finance und Operations sind.“

Überprüfen Sie die Zuordnungen für die Tabellenzuordnung. Wenn sie unidirektional von Customer Engagement-Apps zu Finance und Operations-Apps sind, wird kein Datenverkehr für die Live-Synchronisierung von Finance und Operations-Apps auf Dataverse erzeugt.

## <a name="error-900"></a>Fehler 900

Die Fehlermeldung lautet: „Ungültiges Format des Quellfilters \{sourceFilter\} für die Entität \{Finance und Operations UniqueEntityName\}.“

Der Quellfilter, der in der Tabellenzuordnung für Apps für Finanzen und Betrieb angegeben ist, ist syntaktisch nicht korrekt. Um die Filterkriterien zu validieren, siehe [Beheben von Problemen mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Fehler 1000

Die Fehlermeldung lautet: „Entität \{Finance und Operations UniqueEntityName\}, die für den duales Schreiben Live-Sync verwendet wird, ist \{Finance und Operations EntityFilterQueryString\}. Datensätze, die die Abfragekriterien erfüllen, werden für die Live-Synchronisierung abgeholt.“

Die zurückgegebene Entitätsabfrage ist die unterstützende SQL-Abfrage für die Entität. Suchen Sie in der Abfrage nach Inner Joins oder Filtern, die die Geschäftsdaten bestimmen, die für die Livesynchronisierung abgerufen werden. Inner Joins und Filter sind obligatorische Bedingungen, die für jeden Datensatz erfüllt sein müssen, der für die Dual-Write-Livesynchronisierung aufgenommen wird.

## <a name="error-1300"></a>Fehler 1300

Die Fehlermeldung lautet: „Virtuelle Felder \{s.EntityFieldName\} für die Entität \{Finance und Operations EntityMetadata.EntityProperties.LogicalEntityName\} können nicht für duales Schreiben verfolgt werden.“

Virtuelle Felder aus Finance und Operations Tabellen sind nicht für die Nachverfolgung aktiviert. Die Live-Synchronisierung kann die Daten synchronisieren, aber die Änderungen, die an den Spalten vorgenommen wurden, können nicht übernommen werden.

## <a name="error-1500"></a>Fehler 1500

Die Fehlermeldung lautet: „Es sollte mindestens ein Feld einem Nicht-Nachschlagefeld für die Kundenbindung zugeordnet sein, um die Verfolgung der Datenquelle \{datasource.DataSourceName\} zu ermöglichen.“

Die Datenquelle aus der Entität hat kein Feld, das für Dual-Write zugeordnet ist. Änderungen an der zugrunde liegenden Tabelle werden für Dual-Write nicht nachverfolgt.

## <a name="error-1600"></a>Fehler 1600

Die Fehlermeldung lautet: „Datasource: \{datasource.DataSourceName\} für Entität \{Finance und Operations EntityMetadata.EntityProperties.LogicalEntityName\} hat einen Bereich. Nur Datensätze, die die Bereichsbedingung erfüllen, werden für den Outbound abgeholt.“

Entitäten in Apps für Finanzen und Betrieb können Datenquellen haben, in denen Filterbereiche aktiviert sind. Diese Bereiche definieren die Datensätze, die als Teil der Live-Synchronisierung erfasst werden. Wenn einige Datensätze in den Apps von Finance und Operations auf Dataverse übersprungen werden, prüfen Sie, ob die Datensätze den Bereichskriterien der Entität entsprechen. Eine einfache Möglichkeit, diese Überprüfung durchzuführen, besteht darin, eine SQL-Abfrage auszuführen, die dem folgenden Beispiel ähnelt.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Fehler 1700

Die Fehlermeldung lautet: „Tabelle: \{datasourceTable.Key.subscribedTableName\} für Entität \{datasourceTable.Key.entityName\} wird für Entität \{origTableToEntityMaps.EntityName\} verfolgt. Dieselben Tabellen, die für mehrere Entitäten verfolgt werden, können sich auf die Systemleistung für Live-Synchronisierungstransaktionen auswirken.“

Wenn dieselbe Tabelle von mehreren Entitäten verfolgt wird, löst jede Änderung an der Tabelle eine Dual-Write-Auswertung für die verknüpften Entitäten aus. Obwohl die Filterklauseln nur die gültigen Datensätze senden, kann die Auswertung bei Abfragen mit langer Ausführungszeit oder nicht optimierten Abfrageplänen zu Leistungsproblemen führen. Dieses Problem ist aus geschäftlicher Sicht möglicherweise nicht vermeidbar. Wenn jedoch viele sich überschneidende Tabellen über mehrere Entitäten hinweg vorhanden sind, sollten Sie erwägen, die Entität zu vereinfachen oder Optimierungen für Entitätsabfragen zu überprüfen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
