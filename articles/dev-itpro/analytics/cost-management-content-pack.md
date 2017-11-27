---
title: "Kostenverwaltung für Power BI Inhalt"
description: "In diesem Thema wird beschrieben, was im Kostenmanagement Power Bl enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f509852f15b9518d0a01be1f89d4f07c76caf341
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="cost-management-power-bi-content"></a>Kostenverwaltung für Power BI Inhalt

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, was im Kostenmanagement Power Bl enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

# <a name="overview"></a>Überblick

Der  **Kostenmanagement** Microsoft Power BI Inhalt dient für Bestandsbuchhalter oder Einzelpersonen in der Organisation, die für den Bestand zuständig sind. Der **Kostenmanagement** Power BI Inhalt bietet Einblicke in Bestand und Arbeitsfortschritte (WIP)Bestand und wie die Kosten nach Kategorie im Laufe der Zeit hindurch fließen. Die Informationen können auch als detaillierte Ergänzung der Finanzaufstellung verwendet werden.

## <a name="key-measures"></a>Zentrale Maßnahmen

+ Anfangssaldo
+ Endsaldo
+ Nettoveränderung
+ Nettoveränderung in %
+ Fälligkeit

## <a name="key-performance-indicators"></a>Leistungskennzahlen (KPI)
+ Lagerumschlag
+ Lagergenauigkeit

Die primäre Datenquelle für CostAggregatedCostStatementEntryEntity ist die CostStatementCache-Tabelle. Diese Tabelle wird durch das Datensatzcacheframework verwaltet. Standardmäßig wird die Tabelle alle Stunden 24 aktualisiert, wobei Sie manuelle Aktualisierungen in der Datencachekonfiguration aktivieren können. Sie können eine manuelle Aktualisierung in **Kostenmanagement** oder **Kostenanalyse** - Arbeitsbereich vornehmen. Nach Abschluss der Aktualisierung von CostStatementCache, müssen Sie die OData-Verbindung auf Power  Bl.com aktualisieren, um die aktualisierte Daten auf der Katalogwebsite anzuzeigen. Die Kennzahl der Abweichung (Einkauf, Produktion) in diesem Power Bi Inhalt enthält nur die nur die Elemente, die von der Standardkostenbestandsmethode valuiert werden. Die Produktionsabweichung wird als Differenz zwischen aktiven Kosten und realisierten Kosten berechnet. Die Produktionsabweichung wird berechnet, wenn der Produktionsauftrag den Status aufweist **beendet** aufweist. Weitere Informationen zu jedem Produktionsabweichungstyp und wie jeder Typ berechnet wird, finden Sie unter [Analysieren von Abweichungen für eine abgeschlossenen Produktionsauftrag](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Der Power BI Inhalt **Kostenmanagement** ist von PowerBI.com verfügbar. Weitere Informationen dazu, wie Microsoft Dynamics 365 for Finance and Operations Daten verbunden und geladen werden, finden Sie unter [Zugriff auf Power BI Inhalt von PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrik, die im Power BI Inhalt enthalten ist
Der Inhalt enthält einen Satz Berichtsseiten. Jede Seite enthält einen Satz Metriken, die als Diagramme, Kacheln und Tabellen visuell dargestellt werden. Die folgende Tabelle enthält eine Übersicht der Visualisierungen im **Kostenmanagement** Power Bl Inhalt.

| Berichtsseiten | Diagramme | Titel |
|---|---|---|
|Gesamtes Lager (Standard nach aktueller Periode) |Genauigkeit |Bestandskennzahlen:<br>Bestand Endbetrag<br>Bestand Nettoänderung<br>Bestand Nettoänderung in %<br>|
| |Lagerumschlag | |
| |Endsaldo von Ressourcengruppe | |
| |Bestandsnettoveränderung nach Kategoriename Ebene 1 und Kategoriename Ebene 2| |
| |Kaufen Sie Abweichungen nach Ressourcengruppen und Kategoriename Ebene 3 | |
|Bestand nach Lager (Standard nach aktueller Periode) |Endsaldo Bestand nach Standortname und Ressourcengruppe | |
| |Bestandumschlag nach Sndortname und Ressourcengruppe | |
| |Endsaldo Bestand nach Stadt und Ressourcengruppe | |
|Bestand nach Ressourcengruppe (Standard nach aktueller Periode) |Bestandsmassnahmen | |
| |Bestandsrichtigkeit nach Betrag nach Ressourcengruppe | |
| |Bestandsrichtigkeit nach Betrag nach Ressourcengruppe | |
|Bestand COY (Standard aktuelles Jahr vs. vorheriges Jahr) |Bestandsmassnahmen | |
| |Bestands-KPIs:<br>Lagerumschlag<br>Lagergenauigkeit | |
| |Endsaldo Bestand nach Jahr und Ressourcengruppe | |
| |Kaufen Sie Abweichungen nach Jahr und Kategoriename Ebene 3 | |
|Bestandsfälligkeit (Standard nach aktuellem Jahr) |Bestandsfälligkeit nach Quartal und Ressourcengruppe | |
| |Bestandsfälligkeit nach Quartal und Standortname | |
|RIF gesamt (Standard nach aktueller Periode) |RIF Nettänderung nach Kategoriename Ebene 1 und Kategoriename Ebene 2 |In Bearbeitung befindliche RIF-Vorgänge:<br>RIF-Endsaldo<br>RIF-Nettoveränderung<br>RIF-Nettoveränderung in %<br> |
| |Produktionsabweichungen nach Ressourcengruppen und Kategoriename Ebene 3 | |
| |RIF-Nettoveränderung von Ressourcengruppe | |
|RIF nach Standort (Standard nach aktueller Periode) |In Bearbeitung befindliche RIF-Maßnahmen | |
| |RIF Nettänderung nach Standortname und Kategoriename Ebene 2 | |
| |Produktionsabweichungen nach Standortname und Kategoriename Ebene 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Finance and Operations-Daten werden für die Berichte im **Kostenverwaltung**-Power BI-Inhalt ergänzt. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md). Die folgenden aggregierten Messungen werden als Grundlage des Inhaltspakets verwendet.

| Entität            | Zentrale aggregierte Messungen | Datenquelle für Finance and Operations | Feld             | Beschreibung                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Berichtseinträge | Nettoveränderung                | CostAggregatedCostStatementEntryEntity      | Summe (Betrag \[\])   | Betrag in Buchhaltungswährung |
| Berichtseinträge | Änderung der Nettomenge       | CostAggregatedCostStatementEntryEntity      | Sum(\[Menge\]) |                                   |

Die folgende Tabelle zeigt, wie die zentralen aggregierten Messungen verwendet werden, um mehrere berechnete Kennzahlen im Dataset des Inhalts zu erstellen.

| Kennzahl                                 | Wie die festgelegte Kennzahl berechnet wird                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anfangssaldo                       | \[Endsaldo\]-\[Nettoveränderung\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Anfangssaldo Menge              | \[Endsaldo Menge\]-\[Nettoveränderung Menge\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Endsaldo                          | BERECHNEN SIE(SUM(\[Amount\]), FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\])))                                                                                                                                                                                           |
| Endsaldo, Menge                 | BERECHNEN SIE(SUM(\[Menge\]), FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\])))                                                                                                                                                                                         |
| Anfangssaldo Bestand             | BERECHNEN Sie "Anfangssaldo \[,\]'Auszugseingabe'\[Berichtstyp\] = "Bestand")n                                                                                                                                                                                                                                                                                                                                                                                      |
| Bestand Endbetrag                | BERECHNEN Sie "Endsaldo \[,\]'Auszugseingabe'\[Berichtstyp\] = "Bestand")n                                                                                                                                                                                                                                                                                                                                                                                         |
| Bestand Nettoänderung                    | BERECHNEN Sie "Nettoänderung \[,\]'Auszugseingabe'\[Berichtstyp\] = "Bestand")n                                                                                                                                                                                                                                                                                                                                                                                             |
| Bestand Nettoänderungmenge           | BERECHNEN Sie "Nettoänderungsmenge \[,\]'Auszugseingabe'\[Berichtstyp\] = "Bestand")n                                                                                                                                                                                                                                                                                                                                                                                    |
| Bestand Nettoänderung in %                  | WENN(\[Bestand-Endsaldo\] = 0, 0, \[Bestand-Nettoveränderung\] / \[Bestand-Endsaldo\])                                                                                                                                                                                                                                                                                                                                                                           |
| Bestandumschlag nach Betrag                | wenn (oder(\[durchschnittlicher Bestand\] &lt;= 0, \[verkaufter Bestand oder konsumierte Artikel\] &gt;= 0), 0, ABS(\[verkaufter Bestand oder konsumierte Artikel\])/\[durchschnittlicher Bestandsaldo\])                                                                                                                                                                                                                                                                                                  |
| Durchschnittlicher Lagerbestandsaldo               | (\[Bestandendsaldo\] + \[Bestandanfangssaldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Verkaufter Bestand oder verbrauchte Artikel       | \[Bestand verkauft\] + \[Bestand verbrauchte Materialkosten\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Bestand verbrauchte Materialkosten        | BERECHNEN SIE(\[Bestand Nettoveränderung\],  Berichtseinträge'\[Kategoriename - Ebene 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Bestand verkauft                          | BERECHNEN SIE(\[Bestand Nettoveränderung\],  Berichtseinträge'\[Kategoriename - Ebene 2\_\] = "verkauft")                                                                                                                                                                                                                                                                                                                                                                             |
| Bestandgenauigkeit nach Betrag            | WENN(\[Bestandendsaldo\] &lt;= 0, WENN(ODER(\[Bestandbetrag\] &lt;&gt; 0, \[Bestandendsaldo\] &lt; 0), 0, 1), MAX(0, (\[Bestandendsaldo\] - ABS(\[Bestand gezählter Betrag\]))/\[Bestand Endsaldo\]))                                                                                                                                                                                                                              |
| Bestand gezählter Betrag                | BERECHNEN SIE(\[Bestand Nettoveränderung\],  Berichtseinträge'\[Kategoriename - Ebene 3\_\] = "Zählung")                                                                                                                                                                                                                                                                                                                                                                         |
| Bestandsfälligkeit                         | wenn(ISBLANK(max('Steuerkalender'\[Datum\])), blank(), MAX(0, MIN(\[Bestand Empfangsmenge\], \[Bestand Endsaldomenge\] - \[Bestand Empfangsmenge in der Zukunft\]))) \* \[Bestand durchschnittliche Einheitskosten\]                                                                                                                                                                                                                                |
| Bestandsfälligkeits-Zugangsmenge       | WENN(\[minDate\] = \[minDateAllSelected\], BERECHNEN(\[Bestand Nettoänderungsmenge\], 'Beitragseinträge'\[Menge\] &gt; 0, FILTER(ALLEXCEPT('Steuerkalender', 'Steuerjahr'\[LedgerRecId\], 'Entitäten'\[ID\], 'Entitäten'\[Name\], 'Ledgers'\[Währung\], 'Hauptbuch'\[Beschreibung\], 'Hauptbuch'\[Name\]), 'Steuerkalender'\[Datum\] &lt;= MAX('Steuerkalender'\[Datum\]))), BERECHNEN(\[Bestand Nettoveränderungsmenge\], 'Berichtseinträge'\[Menge\] &gt; 0)) |
| Bestandsfälligkeits-Endsaldomenge | \[Bestandendsummenmenge\] + CALCULATE(\[Bestandnettoveränderung\], FILTER(ALLEXCEPT('Steuerjahr', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &gt; max('Fiscal calendars'\[Date\]) ))                                                                                                                                 |
| Bestandsfälligkeitszugänge zukünftig  | CALCULATE(\[Bestandnettoveränderung\], 'Berichtseingaben'\[Betrag\] &gt; 0, FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &gt; MAX('Fiscal calendars'\[Date\])))                                                                                                                                             |
| Durchschnittliche Bestand-Einheitenkoste                 | CALCULATE(\[Bestandenbilanz\] / \[Bestandendbilanzmenge\],ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'Entitäten'\[ID\], 'Entitäten'\[Name\], 'Sachkonto'\[Währung\], 'Sachkonto'\[Beschreibung\], 'Sachkonto'\[Name\]))                                                                                                                                                                                                                 |
| Einkaufspreisabweichung                      | CALCULATE(SUM(\[Betrag\]), Berichtseingabe'\[Kategoriename - Ebene 2\_\] = "Erfasst", 'Berichtseingaben'\[Berichtstyp\] = "Abweichung")                                                                                                                                                                                                                                                                                                                              |
| RIF-Anfangssaldo                   | CALCULATE(\[Anfangssaldo\], 'Berichtseingaben'\[Berichtstyp\] = "RIF")                                                                                                                                                                                                                                                                                                                                                                                            |
| RIF-Endsaldo                      | CALCULATE(\[Endsaldo\], 'Berichtseingaben'\[Berichtstyp\] = "RIF")                                                                                                                                                                                                                                                                                                                                                                                               |
| RIF-Nettoveränderung                          | BERECHNE(\[Nettoänderung\], 'Berichtseingaben'\[Berichtstiyp\] = "RIF")                                                                                                                                                                                                                                                                                                                                                                                                   |
| RIF-Nettoveränderung in %                        | IF(\[RIF Endsaldo\] = 0, 0, \[RIF Nettoveränderung\] / \[RIF Endsaldo\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Produktionsabweichung                    | BERECHNE(SUM(\[Betrag\]), Berichtseingabe'\[Kategoriename - Ebene 2\_\] = "ManufacturedCost", 'Berichtseingaben'\[Berichtstyp\] = "Abweichung")                                                                                                                                                                                                                                                                                                                      |
| Kategoriename - Ebene 1                 | Wechselt Kategoriename (\[- Ebene 1 kein\_\]" ", "kein", "NetSourcing", "Nettobevorratung"," NetUsage "," Netzwerkgebrauch "," NetConversionCost "," Nettoverarbeitungskosten ", " "," NetCostOfGoodsManufactured Stunden-Einstandspreis von Waren Produktion ", "BeginningBalance"," Anfangssaldo ")                                                                                                                                                                                                         |
| Kategoriename - Ebene 2                 | switch(\[Kategoriename - Ebene 2\_\], "Keine", "Keine", "Procured", "Procured", "Disposed", "Disposed", "Transferred", "Transferred", "Sold", "Sold", "ConsumedMaterialsCost", "Consumed material cost", "ConsumedManufacturingCost", "Consumed manufacturing cost", "ConsumedOutsourcingCost", "Consumed outsourcing cost", "ConsumedIndirectCost", "Consumed indirect cost", "ManufacturedCost", "Manufactured cost", "Variances", "Variances")                            |
| Kategoriename - Ebene 3                 | switch(\[Kategoriename - Ebene 3\_\], "None", "None", "Counting", "None", "ProductionPriceVariance", "Production price", "QuantityVariance", "Quantity", "SubstitutionVariance", "Substitution", "ScrapVariance", "Scrap", "LotSizeVariance", "Lot size", "RevaluationVariance", "Revaluation", "PurchasePriceVariance", "Purchase price", "CostChangeVariance", "Cost change", "RoundingVariance", "Rounding variance")                                                   |

Die folgenden wichtigen Dimensionen werden als Filter verwendet, um die aggregierte Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

| Entität           | Beispiele für Attribute                       |
|------------------|----------------------------------------------|
| Entitäten         | Kennung, Name                                     |
| Steuerkalender | Kalender, Monat, Periode, Quartal Jahr       |
| KPI-Ziele        | Bestandsrichtigkeitsziel, Bestandsdrehungsziel |
| Sachkonten          | Währung, Name, Beschreibung                  |
| Standorte            | Kennung, Name, Land, Ort                      |

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)





