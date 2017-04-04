---
title: Kostenmanagement-Energie BIinhalt
description: "In diesem Thema wird beschrieben, was im Kostenmanagement-Energie BIinhalt enthalten ist. Es wird erläutert, wie Sie die Leistungsfähigkeit BIberichte zugreift und enthält Informationen zum Datenmodell und die Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Kostenmanagement-Energie BIinhalt

In diesem Thema wird beschrieben, was im Kostenmanagement-Energie BIinhalt enthalten ist. Es wird erläutert, wie Sie die Leistungsfähigkeit BIberichte zugreift und enthält Informationen zum Datenmodell und die Entitäten, die verwendet werden, um den Inhalt zu erstellen.

# <a name="overview"></a>Überblick

** Der Microsoft-Energie Kostenmanagement ** BIinhalt wird für Bestandsbuchhalter oder in der Organisation -Personen vorgesehen, die für Lagerbestände zuständig sind. ** Der Kostenmanagement ** Leistungsfähigkeit BIinhalt stellt Verwaltungseinblick in Lager und in im Fertigung (WIP)- Lagerbestand verfügbar und Kosten nach Kategorie im Zeitverlauf. durchfließen Die Informationen können auch verwendet werden als detaillierte Ergänzung der Finanzaufstellung.

## <a name="key-measures"></a>Schlüsselmaßnahmen

+ Anfangssaldo
+ Endsaldo
+ Nettoveränderung
+ Nettoveränderung in %
+ Fälligkeit

## <a name="key-performance-indicators"></a>Leistungskennzahlen (KPI)
+ Lagerumschlag
+ Lagergenauigkeit

Die primäre Datenquelle für CostAggregatedCostStatementEntryEntity ist die CostStatementCache-Tabelle. Diese Tabelle wird durch das Datensatzcacheframework verwaltet. Standardmäßig wird die Tabelle aller Stunden 24 aktualisiert, wobei Sie können manuelle Aktualisierungen in der Datencachekonfiguration aktivieren. Sie können eine manuelle Aktualisierung in ** Kostenmanagement ** oder ** Kostenanalyse ** im - Arbeitsbereich dann möglich. Nach Abschluss der Aktualisierung von CostStatementCache ausgeführt ist, müssen Sie die OData-Verbindung auf Energie BI.com, aktualisieren aktualisierte Daten auf der Katalogwebsite anzuzeigen. Die Kennzahl der Abweichung (Einkauf, Produktion) in diesem BIinhalt Energie betreffen nur Artikel, die von der Standardkostenbestandsmethode valuated. Produktionsabweichung wird als Differenz zwischen aktiven Kosten und realisierten Kosten berechnet. Die Produktionsabweichung wird berechnet, wenn der Produktionsauftrag den Status aufweist ** ** beendet. Weitere Informationen zu jeder Typ z Produktionsabweichungstypen und berechnet wird, finden [Sie zum Analysieren von Abweichungen bei einem abgeschlossenen Produktionsauftrag]( https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Zugreifen Leistung des BIinhalts
** Der Kostenmanagement ** Leistungsfähigkeit BIinhalt ist von PowerBI.com verfügbar. Weitere Informationen dazu, wie Microsoft Dynamics 365 für Arbeitsgänge Daten, finden Sie Zugriffs-Energie Verbindung hergestellt und lädt [BIinhalt von PowerBI.com ]( power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrik, das im BIinhalt Energie enthalten sind
Der Inhalt enthält einen Satz Berichtsseiten. Jede Seite enthält einen Satz Metriken, das als Diagramme, Kacheln und Tabellen visuell dargestellt werden. Die folgende Tabelle enthält eine Übersicht der im Visualisierungen ** Kostenmanagement ** Leistungsfähigkeit BIinhalt.

| Berichtsseite | Diagramme | Titel |
|---|---|---|
|Gesamte Lager (Standard nach aktueller Periode) |Genauigkeit |Bestandskennzahlen:<br>Bestandsendsaldo<br>Bestandsnettoveränderung<br>Bestandsnettoveränderung %<br>|
| |Lagerumschlag | |
| |Bestandsendsaldo von Ressourcengruppe | |
| |Bestandsnettoveränderung nach Ebene 2 namen-Ebene 1 und der Kategorie " Kategorie namens| |
| |Kaufen Sie Abweichungen nach Kategorienamen Ebene 3 und Ressourcengruppen- | |
|Lagerbestand nach Standort (Standard nach aktueller Periode) |Bestandsendsaldo nach und Standorts-Namen Ressourcengruppe | |
| |Bestandsdrehung nach und Standorts-Namen Ressourcengruppe | |
| |Bestandsendsaldo nach Ort und Ressourcengruppe | |
|Bestand nach Ressourcengruppe (Standard nach aktueller Periode) |Bestandskennzahlen | |
| |Bestandsrichtigkeit nach Betrag von Ressourcengruppe | |
| |Bestandsdrehung nach Betrag von Ressourcengruppe | |
|Lager (Standardaktuelles anhand des YOY vorheriges Jahr) |Bestandskennzahlen | |
| |KPIs Lager:<br>Lagerumschlag<br>Lagergenauigkeit | |
| |Bestandsendsaldo nach Jahr und Ressourcengruppe | |
| |Kaufen Sie Abweichungen nach Kategorienamen Ebene 3 und Jahr- | |
|Bestandsfälligkeit (Standard nach aktuellem Jahr) |Bestandsfälligkeit nach Quartal und Ressourcengruppe | |
| |Bestandsfälligkeit nach und Standortsnamen Quartals- | |
|RIF Gesamt (Standard nach aktueller Periode) |RIF-Nettoveränderung nach Ebene 2 namen-Ebene 1 und der Kategorie " Kategorie namens |Kennzahlen der in Durchführung befindlichen Arbeiten RIF:<br>RIF-Endsaldo<br>RIF-Nettoveränderung<br>RIF-Nettoveränderung %<br> |
| |Produktionsabweichungen nach Kategorienamen Ebene 3 und Ressourcengruppen- | |
| |RIF-Nettoveränderung von Ressourcengruppe | |
|RIF nach Standort (Standard nach aktueller Periode) |Kennzahlen der in Durchführung befindlichen Arbeiten RIF | |
| |RIF-Nettoveränderung nach Standortsnamen- und Kategorienamenebene 2 | |
| |Produktionsabweichungen nach Standortsnamen- und Kategorienamenebene 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 für Arbeitsgangsdaten wird verwendet, um in der Berichtsseiten ** Kostenmanagement ** Leistungsfähigkeit BIinhalt aufzufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der Übersicht [Power BI-Integration mit Entitätsshop] (power-bi-integration-entity-store.md ). Die folgenden Schlüsselaggregatsmessungen werden als Grundlage des Inhalts verwendet.

| Entität            | Gesamte Messung des Schlüssels | Datenquelle für Dynamics 365 für Arbeitsgänge | Feld             | Beschreibung                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Auszugseinträge | Nettoveränderung                | CostAggregatedCostStatementEntryEntity      | Summe (Betrag \[\])   | Betrag in der Buchhaltungswährung |
| Auszugseinträge | Nettoveränderungsmenge       | CostAggregatedCostStatementEntryEntity      | Summe (\[\]Menge) |                                   |

Die folgende Tabelle zeigt, wie die Tastenfunktionen gesamten Messungen verwendet werden, um mehrere berechnete Kennzahlen im Dataset des Inhalts zu erstellen.

| Kennzahl                                 | Wie die festgelegte Kennzahl berechnet wird                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anfangssaldo                       | Nettoveränderung \]\[Endsaldo__ent_dict_PLACEHOLDER\]-                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Anfangssaldoenmenge              | Nettoveränderungsmenge \]\[\]-                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Endsaldo                          | BERECHNEN Sie "SUMME (Betrag \[\]), FILTER (ALLEXCEPT "Steuerkalender ", "\ calendars'entity_PLACEHOLDER steuerlich [LedgerRecId\], "\ entities'entity_PLACEHOLDER [Kennung\], entities'entity_PLACEHOLDER "[Name \\]\ Ledgers'entity_PLACEHOLDER, "Währung "\][\]\\]Ledgers'entity_PLACEHOLDER [- beschreibung,\]\Ledgers'entity_PLACEHOLDER [-Name\]",\]LIFO steuerlich calendars'entity_PLACEHOLDER \\]&lt;= [Datums MAX\] steuerlich " calendars'entity_PLACEHOLDER \\]) [Datum)\]                                                                                                                                                                                           |
| Endsaldomenge                 | BERECHNEN Sie "SUMME \[Menge (\]), FILTER (ALLEXCEPT "Steuerkalender ", "\ calendars'entity_PLACEHOLDER steuerlich [LedgerRecId\], "\ entities'entity_PLACEHOLDER [Kennung\], entities'entity_PLACEHOLDER "[Name \\]\ Ledgers'entity_PLACEHOLDER, "Währung "\][\]\\]Ledgers'entity_PLACEHOLDER [- beschreibung,\]\Ledgers'entity_PLACEHOLDER [-Name\]",\]LIFO steuerlich calendars'entity_PLACEHOLDER \\]&lt;= [Datums MAX\] steuerlich " calendars'entity_PLACEHOLDER \\]) [Datum)\]                                                                                                                                                                                         |
| Bestandsanfangssaldo             | BERECHNEN Sie "Anfangssaldo \[,\]'Auszug entries'entity_PLACEHOLDER \\] = [Auszugs-Typ "Lager")                                                                                                                                                                                                                                                                                                                                                                                      |
| Bestandsendsaldo                | BERECHNEN Sie "\[Endsaldo\], 'Auszug entries'entity_PLACEHOLDER \\] = [Auszugs-Typ "Lager")                                                                                                                                                                                                                                                                                                                                                                                         |
| Bestandsnettoveränderung                    | BERECHNEN Sie "\[Nettoveränderung\], 'Auszug entries'entity_PLACEHOLDER \\] [Anwendung " Lager")                                                                                                                                                                                                                                                                                                                                                                                             |
| Bestandsnettoveränderungsmenge           | Sie BERECHNEN Sie \[\]Nettoveränderungsmenge (' Auszug entries'entity_PLACEHOLDER \\] = [Anwendung\] Lager ")                                                                                                                                                                                                                                                                                                                                                                                    |
| Bestandsnettoveränderung %                  | IF (\[Bestandsendsaldo\] 0,0, Bestandsendsaldo\]\[\]\] / )                                                                                                                                                                                                                                                                                                                                                                           |
| Bestandsdrehung nach Betrag                | ((ODER wenn \[Bestandsdurchschnittliches aktueller Salden\]&lt;\] 0, verkauften oder verbrauchte Abgänge\] \[= &gt;0 ), 0, ABS (\[verkauften oder verbrauchte Probleme\]/\[aktueller Salden\])                                                                                                                                                                                                                                                                                                  |
| Bestandsdurchschnittliches aktueller Salden               | Bestandsanfangssaldoen-\](\[\] + \]\[                                                                                                                                                                                                                                                                                                                                                                                                       |
| Verkauften oder verbrauchte Abgänge des Lagers       | \[Lager z verbrauchte Materialkosten\]\] + \[Lager                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Lager verbrauchte Materialkosten        | Sie BERECHNEN Sie \[\]Bestandsnettoveränderung (' Auszug entries'entity_PLACEHOLDER \ [Kategoriename - Ebene 2\_\]\_\] ConsumedMaterialsCost ")                                                                                                                                                                                                                                                                                                                                                            |
| Lager verkauft                          | Sie BERECHNEN Sie \[\]Bestandsnettoveränderung (' Auszug entries'entity_PLACEHOLDER \ [Kategoriename - Ebene 2\_\]\_\] verkauft ")                                                                                                                                                                                                                                                                                                                                                                             |
| Bestandsrichtigkeit nach Betrag            | IF (\[Bestandsendsaldo\]&lt;\] 0 ODER, IF ((\[Mehrbetrag\]&lt;&gt; 0\]\[Bestandsendsaldo\]&lt; 0)\] 0, 1 ", " 0, MAX (\[Bestandsendsaldo\]\[ABS\]\[Bestandsgezählter Mehrbetrag\]\[)/\[Bestandsendsaldo\]))                                                                                                                                                                                                                              |
| Bestandsgezählter betrag                | Sie BERECHNEN Sie \[\]Bestandsnettoveränderung (' Auszug entries'entity_PLACEHOLDER \ [Kategoriename - Ebene 3\_\]\_\] Inventur ")                                                                                                                                                                                                                                                                                                                                                                         |
| Bestandsfälligkeit                         | wenn "ISBLANK (maximal ('steuerlich calendars'entity_PLACEHOLDER \\]) [Datum), blank() MAX (0, Bestandsfälligkeits-Zugangsmenge MIN (\[,\]zukünftig\]\[Bestandsfälligkeitsendsaldomengen__ent_dict_PLACEHOLDER\] - \]\[) Lager \* \[Einheitenkosten\]Kosten                                                                                                                                                                                                                                |
| Bestandsfälligkeits-Zugangsmenge       | IF (\[minDate\] = \[minDateAllSelected\], BERECHNEN (\[,\]Bestandsnettoveränderungsmenge\]Auszug entries'entity_PLACEHOLDER \\]&gt; [Menge 0\] FILTER (ALLEXCEPT "Steuerkalender "," \ calendars'entity_PLACEHOLDER steuerlich [LedgerRecId\],\]\entities'entity_PLACEHOLDER [Kennung\], entities'entity_PLACEHOLDER\][Name \\]\Ledgers'entity_PLACEHOLDER,\]Währung ", [\]\\]\][- beschreibung, "\]Ledgers'entity_PLACEHOLDER [-Name\]", " LIFO steuerlich\]\\]&lt;= [Datums MAX ('\] calendars'entity_PLACEHOLDER \\]) [Datum)), BERECHNEN Sie "\[,\]Bestandsnettoveränderungsmenge\]Auszug entries'entity_PLACEHOLDER \\]&gt; [Menge 0\] ) |
| Bestandsfälligkeits-Endsaldomenge | \[Bestandsendsaldomenge\] + (\[Bestandsnettoveränderungsmenge\], FILTER (\]" Steuerkalender ", "\ calendars'entity_PLACEHOLDER steuerlich [LedgerRecId\], "\]entities'entity_PLACEHOLDER [Kennung\], entities'entity_PLACEHOLDER " [Name\]\]Ledgers'entity_PLACEHOLDER, "Währung", [\]\\]Ledgers'entity_PLACEHOLDER\]- beschreibung, " \ Ledgers'entity_PLACEHOLDER [\]\]", " LIFO steuerlich calendars'entity_PLACEHOLDER \\]Datums-\]&gt; Maximums (steuerlich " calendars'entity_PLACEHOLDER \\])\] Datum))                                                                                                                                 |
| Bestandsfälligkeitszugänge zukünftig  | BERECHNEN Sie "\[" Auszug\]Bestandsnettoveränderung\]\\]&gt; entries'entity_PLACEHOLDER [Betrag 0, FILTER (ALLEXCEPT "Steuerkalender", " \ calendars'entity_PLACEHOLDER steuerlich [LedgerRecId\]" \ entities'entity_PLACEHOLDER [Kennung\]entities'entity_PLACEHOLDER " [Name \\]\ Ledgers'entity_PLACEHOLDER\]" Währung\], [\]\\]Ledgers'entity_PLACEHOLDER [- beschreibung, " \\][-Name\]", "\]calendars'entity_PLACEHOLDER \ [Datums-\]&gt; MAXIMUMS ('\] calendars'entity_PLACEHOLDER \\]) [Datum))                                                                                                                                             |
| Lager Einheitenkosten Kosten                 | BERECHNEN Sie "Bestands-Endsaldomenge \]ALLEXCEPT "Steuerkalender", " \ calendars'entity_PLACEHOLDER steuerlich [LedgerRecId\]" \ entities'entity_PLACEHOLDER [Kennung\]entities'entity_PLACEHOLDER " [Name \\]\ Ledgers'entity_PLACEHOLDER\]" Währung\], [\]\\]Ledgers'entity_PLACEHOLDER [- beschreibung, " \\]) [-Name\]\[Bestandsendsaldo__ent_dict_PLACEHOLDER\] / \[                                                                                                                                                                                                                 |
| Kaufen Sie Abweichungen                      | BERECHNEN Sie "SUMME (Betrag \[\]), "Auszug entries'entity_PLACEHOLDER \ [Kategoriename - Ebene 2\_\] =\] verschafft ", " Auszug entries'entity_PLACEHOLDER \\] = [Anwendung\] Abweichung) "                                                                                                                                                                                                                                                                                                                              |
| RIF-Anfangssaldo                   | BERECHNEN Sie "Anfangssaldo \[,\]'Auszug entries'entity_PLACEHOLDER \\] = [Auszugs-Typ "RIF")                                                                                                                                                                                                                                                                                                                                                                                            |
| RIF-Endsaldo                      | BERECHNEN Sie "\[Endsaldo\], 'Auszug entries'entity_PLACEHOLDER \\] = [Auszugs-Typ "RIF")                                                                                                                                                                                                                                                                                                                                                                                               |
| RIF-Nettoveränderung                          | BERECHNEN Sie "\[Nettoveränderung\], 'Auszug entries'entity_PLACEHOLDER \\] [Anwendung " RIF")                                                                                                                                                                                                                                                                                                                                                                                                   |
| RIF-Nettoveränderung %                        | IF (RIF Endsaldo \]\[= 0, 0, Nettoveränderungs-__ent_dict_PLACEHOLDER\] / \[\[Endsaldo \[\]                                                                                                                                                                                                                                                                                                                                                                                             |
| Produktionsabweichungen                    | BERECHNEN Sie "SUMME (Betrag \[\]), "Auszug entries'entity_PLACEHOLDER \ [Kategoriename - Ebene 2\_\] =\] ManufacturedCost ", " Auszug entries'entity_PLACEHOLDER \\] = [Anwendung\] Abweichung) "                                                                                                                                                                                                                                                                                                                      |
| Kategoriename - Ebene 1                 | Wechselt Kategoriename (\[- Ebene 1 kein\_\]" ", "kein", "NetSourcing", "Nettobevorratung"," NetUsage "," Netzwerkgebrauch "," NetConversionCost "," Nettoverarbeitungskosten ", " "," NetCostOfGoodsManufactured Stunden-Einstandspreis von Waren Produktion ", "BeginningBalance"," Anfangssaldo ")                                                                                                                                                                                                         |
| Kategoriename - Ebene 2                 | Wechselt Kategoriename (\[- Ebene 2\_\]keine\]" ", "keine ", "verschafft", " ", "verschafft abgeschafft abgeschafft", " ", "übertragen", "übertragen", "verkauft", "Verkauf", "ConsumedMaterialsCost", "Verbraucht Materialkosten", "ConsumedManufacturingCost", "Verbraucht Herstellkosten"," ConsumedOutsourcingCost "," Auslagerungskosten Verbraucht ", "ConsumedIndirectCost"," Verbraucht indirekte Kosten ", "ManufacturedCost"," Zähler "Kosten", " Abweichungen," Abweichungen ")                            |
| Kategoriename - Ebene 3                 | Wechselt Kategoriename (\[- Ebene 3 kein\_\]" ", "kein", " ", Inventur- "kein", "ProductionPriceVariance- Produktionspreis", " ", "QuantityVariance-", "Menge", "SubstitutionVariance-" Ersetzung, " ", "ScrapVariance-", "Ausschuss", "LotSizeVariance-", "Abrechnungslosgröße" Abweichung, " "," RevaluationVariance der Neubewertung "," PurchasePriceVariance "," des Einkaufspreises "," "," CostChangeVariance der Kostenänderung "," "," RoundingVariance der Rundung ")                                                   |

Die folgenden wichtigen Dimensionen werden als Filter verwendet, um die gesamten Messungen ein Crossdocking, um größere Granularität zu erreichen tiefere und analytische Einblicke bereitzustellen.

| Entität           | Beispiele für Attribute                       |
|------------------|----------------------------------------------|
| Entitäten         | Kennung, Name                                     |
| Steuerkalender | Kalender, Monat, Periode, Quartal, Jahr       |
| KPI-Ziele        | Bestandsrichtigkeitsziel, Bestandsdrehungsziel |
| Sachkonten          | Währung, Name, Beschreibung                  |
| Standorte            | Kennung, Name, Land, Ort                      |

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)



