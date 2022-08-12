---
title: Fehlercodes für die Systemdiagnose der Tabellenzuordnung
description: In diesem Artikel werden Fehlercodes für die Systemdiagnose der Tabellenzuordnung beschrieben.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 16c79a788b66830b77b2cdfb33fd2416c530f7d2
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111565"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Fehlercodes für die Systemdiagnose der Tabellenzuordnung

[!include [banner](../../includes/banner.md)]



In diesem Artikel werden Fehlercodes für die Systemdiagnose der Tabellenzuordnung beschrieben.

## <a name="error-100"></a>Fehler 100

Die Fehlermeldung lautet: „Für das Ausführen von Finanzen und Betrieb-Empfehlungen ist mindestens die Plattformversion PU 43 erforderlich.“

Die Funktion erfordert Plattform-Updates für die Version 10.0.19 oder höher der Finanz- und Betriebs-Apps.

## <a name="error-400"></a>Fehler 400

Die Fehlermeldung lautet: „Für die Entität \{finance and operations UniqueEntityName\} wurden keine Daten zur Registrierung von Ereignissen gefunden. Das bedeutet, dass entweder die Zuordnung nicht ausgeführt wird oder alle Feldzuordnungen unidirektional sind.“

## <a name="error-500"></a>Fehler 500

Die Fehlermeldung lautet: „Keine Projektkonfigurationen für Projekt \{Projektname\} gefunden. Dies könnte entweder daran liegen, dass das Projekt nicht aktiviert ist oder dass alle Zuordnungen der Felder unidirektional sind, d.h. von Customer Engagement zu Finanzen und Betrieb.“

Überprüfen Sie die Zuordnungen für die Tabellenzuordnung. Wenn sie unidirektional von Customer Engagement-Apps zu Finanz- und Betriebs-Apps sind, wird kein Datenverkehr für die Live-Synchronisierung von Finanz- und Betriebs-Apps auf Dataverse erzeugt.

## <a name="error-900"></a>Fehler 900

Die Fehlermeldung lautet: „Ungültiges Format des Quellfilters \{sourceFilter\} für die Entität \{Finanzen und Betrieb UniqueEntityName\}.“

Der Quellfilter, der in der Tabellenzuordnung für Finanz- und Betriebs-Apps angegeben ist, ist syntaktisch nicht korrekt. Um die Filterkriterien zu validieren, siehe [Beheben von Problemen mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Fehler 1000

Die Fehlermeldung lautet: „Entität \{Finanzen und Betrieb UniqueEntityName\}, die für den Dual-write Live-Sync verwendet wird, ist \{Finanzen und Betrieb EntityFilterQueryString\}. Datensätze, die die Abfragekriterien erfüllen, werden für die Live-Synchronisierung abgeholt.“

Die zurückgegebene Entitätsabfrage ist die unterstützende SQL-Abfrage für die Entität. Suchen Sie in der Abfrage nach Inner Joins oder Filtern, die die Geschäftsdaten bestimmen, die für die Livesynchronisierung abgerufen werden. Inner Joins und Filter sind obligatorische Bedingungen, die für jeden Datensatz erfüllt sein müssen, der für die Dual-Write-Livesynchronisierung aufgenommen wird.

## <a name="error-1300"></a>Fehler 1300

Die Fehlermeldung lautet: „Virtuelle Felder \{s.EntityFieldName\} für die Entität \{Finanzen und Betrieb EntityMetadata.EntityProperties.LogicalEntityName\} können für Dual-write nicht nachverfolgt werden.“

Virtuelle Felder aus Finanzen und Betrieb Tabellen sind nicht für die Nachverfolgung aktiviert. Die Live-Synchronisierung kann die Daten synchronisieren, aber die Änderungen, die an den Spalten vorgenommen wurden, können nicht übernommen werden.

## <a name="error-1500"></a>Fehler 1500

Die Fehlermeldung lautet: „Es sollte mindestens ein Feld einem Nicht-Nachschlagefeld für die Kundenbindung zugeordnet sein, um die Verfolgung der Datenquelle \{datasource.DataSourceName\} zu ermöglichen.“

Die Datenquelle aus der Entität hat kein Feld, das für Dual-Write zugeordnet ist. Änderungen an der zugrunde liegenden Tabelle werden für Dual-Write nicht nachverfolgt.

## <a name="error-1600"></a>Fehler 1600

Die Fehlermeldung lautet: „Datasource: \{datasource.DataSourceName\} für Entität \{Finanzen und Betrieb EntityMetadata.EntityProperties.LogicalEntityName\} hat einen Bereich. Nur Datensätze, die die Bereichsbedingung erfüllen, werden für den Outbound abgeholt.“

Entitäten in Finanz- und Betriebs-Apps können Datenquellen haben, in denen Filterbereiche aktiviert sind. Diese Bereiche definieren die Datensätze, die als Teil der Live-Synchronisierung erfasst werden. Wenn einige Datensätze in den Apps von Finanzen und Betrieb auf Dataverse zurückgesetzt werden, prüfen Sie, ob die Datensätze den Bereichskriterien der Entität entsprechen. Eine einfache Möglichkeit, diese Überprüfung durchzuführen, besteht darin, eine SQL-Abfrage auszuführen, die dem folgenden Beispiel ähnelt.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Fehler 1700

Die Fehlermeldung lautet: „Tabelle: \{datasourceTable.Key.subscribedTableName\} für Entität \{datasourceTable.Key.entityName\} wird für Entität \{origTableToEntityMaps.EntityName\} verfolgt. Dieselben Tabellen, die für mehrere Entitäten verfolgt werden, können sich auf die Systemleistung für Live-Synchronisierungstransaktionen auswirken.“

Wenn dieselbe Tabelle von mehreren Entitäten verfolgt wird, löst jede Änderung an der Tabelle eine Dual-Write-Auswertung für die verknüpften Entitäten aus. Obwohl die Filterklauseln nur die gültigen Datensätze senden, kann die Auswertung bei Abfragen mit langer Ausführungszeit oder nicht optimierten Abfrageplänen zu Leistungsproblemen führen. Dieses Problem ist aus geschäftlicher Sicht möglicherweise nicht vermeidbar. Wenn jedoch viele sich überschneidende Tabellen über mehrere Entitäten hinweg vorhanden sind, sollten Sie erwägen, die Entität zu vereinfachen oder Optimierungen für Entitätsabfragen zu überprüfen.

## <a name="error-1800"></a>Fehler 1800
Die Fehlermeldung lautet: „Datenquelle: {} für die Entität CustCustomerV3Entity enthält einen Bereichswert. Eingehende Datensätze von Dataverse zu Finanzen und Vorgängen können durch Bereichswerte auf Entitäten beeinflusst werden. Bitte testen Sie Datensatzaktualisierungen von Dataverse in Finanzen und Betrieb mit Datensätzen, die nicht den Filterkriterien entsprechen, um Ihre Einstellungen zu validieren.“

Wenn für die Entität in Finanz- und Betriebs-Apps ein Bereich angegeben ist, wird die eingehende Synchronisierung von Dataverse nach Finanz- und Betriebs-Apps auf das Aktualisierungsverhalten von Datensätzen getestet, die diesen Bereichskriterien nicht entsprechen. Jeder Datensatz, der nicht mit dem Bereich übereinstimmt, wird von der Entität als Einfügevorgang behandelt. Wenn in der zugrunde liegenden Tabelle ein Datensatz vorhanden ist, schlägt die Einfügung fehl. Wir empfehlen, dass Sie diesen Anwendungsfall für alle Szenarien testen, bevor Sie ihn in der Produktion bereitstellen.

## <a name="error-1900"></a>Fehler 1900
Die Fehlermeldung lautet: „Entität: hat {} Datenquellen, die nicht für ausgehenden dualen Schreibvorgang verfolgt werden. Dies kann die Abfrageleistung der Live-Synchronisierung beeinträchtigen. Bitte gestalten Sie die Entität in Finanzen und Betrieb um, um ungenutzte Datenquellen und Tabellen zu entfernen oder implementieren Sie getEntityRecordIdsImpactedByTableChange, um die Laufzeitabfragen zu optimieren.“

Wenn es viele Datenquellen gibt, die nicht für die Nachverfolgung in der tatsächlichen Live-Synchronisierung von Finanz- und Betriebs-Apps verwendet werden, besteht die Möglichkeit, dass die Leistung der Entität die Live-Synchronisierung beeinträchtigen kann. Um die nachverfolgten Tabellen zu optimieren, verwenden Sie die Methode getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Fehler 5000
Die Fehlermeldung lautet: „Synchrone Plugins sind für Datenverwaltungsereignisse für Entitätskonten registriert. Diese können sich auf die Leistung der anfänglichen Synchronisierung und des Live-Synchronisierungsimports in Dataverse auswirken. Um die beste Leistung zu erzielen, stellen Sie die Plugins auf asynchrone Verarbeitung um. Liste der registrierten Plugins {}.“

Synchrone Plugins auf einer Dataverse-Entität können die Leistung der Live-Synchronisierung und der anfänglichen Synchronisierung beeinträchtigen, da sie die Transaktionslast erhöht. Der empfohlene Ansatz besteht darin, die Plugins entweder zu deaktivieren oder diese Plugins asynchron einzustellen, wenn Sie mit langsamen Ladezeiten bei der anfänglichen Synchronisierung oder Live-Synchronisierung für eine bestimmte Entität konfrontiert sind.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

