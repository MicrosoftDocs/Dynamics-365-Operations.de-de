---
title: "Power BI-Inhalt – Produktionsleistung"
description: "In diesem Thema wird beschrieben, was im Warehouse Performance Power Bl Inhalt enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: AndersGirke
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ProductionPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d59a7aef90ecef0cd947b833f1cce1e2372f3033
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---

# <a name="production-performance-power-bi-content"></a>Power BI-Inhalt – Produktionsleistung

[!INCLUDE [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im **Produktionsleistung** Microsoft Power Bl Inhalt enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Überblick

Der **Produktionsfluss** ist für Power BI Inhalt für Produktions-Managers oder Personen in der Organisation, die für Produktionssteuerung zuständig sind.

Die Berichte, die in Power BI Inhalt eingeschlossen sind, um die Leistung von Produktionsvorgängen hinsichtlich der fristgerechten Ausführung, der Qualität und der Kosten zu überwachen. Die Berichte verwenden Transaktionsdaten von Produktionsaufträgen sowie von Chargenaufträgen und bieten eine gesamte wertberichtigte, unternehmensweite Produktionsmetrik und eine Aufschlüsselung der Metrik nach Produkt und Ressource an.

Der Power BI Inhalt hebt die Möglichkeit der Organisation hervor, die Produktion pünktlich und vollständig abzuschließen. Zukünftige Leistung wird auf Basis der projektiert Produktionspläne geplant. Verständliche Berichte enthalten detaillierte Einblicke in Produktfehler, die während der Produktion anfallen, und zeigt auch die Defektsätze für Ressourcen und Arbeitsgänge.

Mit diesem Power BI Inhalt können Sie Produktionsabweichungen analysieren. Die Produktionsabweichung wird als Differenz zwischen aktiven Kosten und realisierten Kosten berechnet. Die Berechnung von Produktionsabweichungen erfolgt, wenn Produktionsaufträge oder Chargenaufträge den Status **Beendet** erreichen.

Der **Produktionsfluss** Power BI Inhalt umfasst Daten, die aus Produktionsaufträgen und Chargenaufträgen stammen. Die Berichte enthalten keine Daten, die den Kanbanproduktionen zugeordnet sind.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Diw **Produktionsleistung** Power BI-Inhalt wird auf der **Produktionsleistung** angezeigt (**Produktionssteuerung** > **Abfragen und Berichte** > **Produktionsleistungsanalyse** > **Produktionsfluss**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrik, die im Power BI Inhalt enthalten ist

Der **Produktionsfluss** Power BI Inhalt enthält einen Satz Berichtsseiten. Jede Seite enthält einen Satz Metriken, die als Diagramme, Kacheln und Tabellen visuell dargestellt werden.

Die folgende Tabelle enthält eine Übersicht der Visualisierungen im Inhaltspaket.

| Berichtsseiten                                | Diagramme                                               | Kacheln |
|--------------------------------------------|------------------------------------------------------|-------|
| Produktionsleistung                     | <ul><li>Anzahl der Produktionsauftragspositionen nach Datum</li><li>Anzahl der Produktionen nach Produkt und Artikelgruppe</li><li>Anzahl der geplanten Produktionsaufträge nach Datum</li><li>10 tiefsten Produkte nach Pünktlichkeit und Vollständigkeit</li></ul> | <ul><li>Gesamtbestellung</li><li>Rechtzeitig und vollständig in Prozent</li><li>Unvollständig in %</li><li>Vorzeitig in %</li><li>verspätet in %</li></ul> |
| Defekte nach Produkt                         | <ul><li>Fehlerhafter Satz (PPM) nach Datum</li><li>Fehlerhafte Rate nach Produkt (PPM) und Artikelgruppe</li><li>Jährlich produzierte Menge nach Datum</li><li>Top 10 Produkte nach gültigem Preis</li></ul> | <ul><li>Fehlerhafter Satz (PPM)</li><li>Fehlerhafte Menge</li><li>Gesamtmenge</li></ul> |
| Defekter Trend nach Produkt                   | Defekter Satz (PPM) nach produzierter Menge | Fehlerrate (ppm) |
| Defekte nach Ressource                        | <ul><li>Fehlerhafter Satz (PPM) nach Datum</li><li>Fehlerhafter Satz (PPM) nach Ressource und Standort</li><li>Fehlerhafter Satz (PPM) nach Betrieb</li><li>Top 10 Ressourcen nach Defektsatz</li></ul> | Fehlerhafte Menge |
| Defekter Trend nach Ressource                  | Defekter Satz (PPM) nach produzierter Menge | |
| Produktionsabweichungen für eine Auftragskalkulation | <ul><li>Produktionsabweichung von Datums- und Kostengruppentyp</li><li>Produktionsabweichung nach Standort und Kostengruppentyp</li><li>Top 10 Produkte mit ungünstiger Produktionsabweichung</li><li>Top 10 Produkte mit ungünstiger Produktionsabweichung nach Ressource</li></ul> | <ul><li>Realisierte Kosten</li><li>Produktionsabweichung</li><li>Produktionsabweichung in %</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt **Produktionsleistung** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die zwecks Analyse optimiert ist. Weitere Informationen zu den Entitätsshop finden Sie unter [Power BI-Integration mit Entitäts-Shop](power-bi-integration-entity-store.md).

Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Power BI Inhalts verwendet.

| Entität                   | Zentrale aggregierte Messungen  | Datenquelle für Finance and Operations | Feld              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Die folgende Tabelle zeigt, wie die zentralen aggregierten Messungen verwendet werden, um mehrere berechnete Kennzahlen im Dataset des Inhalts zu erstellen.

| Kennzahl                  | Wie die festgelegte Kennzahl berechnet wird |
|--------------------------|-------------------------------|
| Produktionsabweichung in %   | SUMME ("Produktionsabweichungs"[Produktionsabweichung]) / SUMME("Produktionsabweichung "[vorkalkulierte Kosten)] |
| Alle Bestellvorschläge       | COUNTROWS (Geplanter Produktionsauftrag) |
| Vorzeitig                    | COUNTROWS(FILTER('Geplanter Produktionsauftrag', 'Geplanter Produktionsauftrag'[Geplantes Enddatum] \< 'Geplanter Produktionsauftrag'[Anforderungsdatum])) |
| Verspätet                     | COUNTROWS(FILTER('Geplanter Produktionsauftrag', 'Geplanter Produktionsauftrag'[Geplantes Enddatum] \> 'Geplanter Produktionsauftrag'[Anforderungsdatum])) |
| Termingerecht                  | COUNTROWS(FILTER('Geplanter Produktionsauftrag', 'Geplanter Produktionsauftrag'[Geplantes Enddatum] = 'Geplanter Produktionsauftrag'[Anforderungsdatum])) |
| Termingerecht %                | IF ("geplanter Produktionsauftrag"[Einschaltzeit] \<\> 0, "Einschaltzeit geplanter Produktionsauftrag"[Einschaltzeit], IF ("geplanter Produktionsauftrag"[alle Bestellvorschläge] \<\> 0, 0, LEER())) / "geplanter Produktionsauftrag"[alle Bestellvorschläge] |
| Abgeschl.                | COUNTROWS(FILTER("Produktionsauftrag", "Produktionsauftrag"[ist RAF'ed] = TRUE)) |
| Fehlerhafter Satz (PPM)     | IF ("Produktionsauftrag" [Gesamtmenge] = 0, BLANK(), (SUMME(Produktionsauftrag[Ausschussmenge]) / Produktionsauftrag[Gesamtmenge] \* 1000000) |
| Verzögerte Produktionsrate  | "Produktionsauftrag [Spät \#]/Produktionsauftrag abgeschlossen [Abgeschlossen] |
| Vorzeitig und vollständig          | COUNTROWS(FILTER('Produktionsauftrag', 'Produktionsauftrag'[Vollständig] = TRUE && 'Produktionsauftrag'[Vorzeitig] = TRUE)) |
| Vorzeitig \#                 | COUNTROWS (FILTER ("Produktionsauftrag", "Produktionsauftrag" [ist vorzeitig] = TRUE)) |
| Vorzeitig in %                  | IFERROR( IF('Produktionsauftrag'[Vorzeitig \#] \<\> 0, 'Produktiosnauftrag'[Vorzeitig \#], IF('Produktionsauftrag'[Gesamtauftrag] = 0, BLANK(), 0)) / 'Produktionsauftrag'[Gesamtauftrag], BLANK()) |
| Unvollständig               | COUNTROWS(FILTER('Produktionsauftrag', 'Produktionsauftrag'[Vollständig] = FALSE && 'Produktionsauftrag'[Is RAF'ed] = TRUE)) |
| Unvollständig in %             | IFERROR( IF('Produktionsauftrag'[Unvollständig] \<\> 0, 'Produktionsauftrag'[Unvollständig], IF('Produktionsauftrag'[Gesamtauftrag] = 0, BLANK(), 0)) / 'Produktionsauftrag'[Gesamtauftrag], BLANK()) |
| verzögert               | 'Produktionsauftrag'[Is RAF'ed] = TRUE && 'Produktionsauftrag'[Verzögerter Wert] = 1 |
| Ist früh                 | 'Produktionsauftrag'[Is RAF'ed] = TRUE && 'Produktionsauftrag'[Tage verzögert] \< 0 |
| Vollständig               | "Produktionsauftrag" [Gute Menge] \>= "Produktionsauftrag" [Planmenge] |
| Ist RAF'ed                | 'Produktionsauftrag'[Produktionsstatuswert] = 5 \|\| 'Produktionsauftrag'[Produktionsstatuswert] = 7 |
| Spät und vollständig           | COUNTROWS(FILTER('Produktionsauftrag', 'Produktionsauftrag'[Vollständig] = TRUE && 'Produktionsauftrag'[Verspätet] = TRUE)) |
| verspätet \#                  | COUNTROWS (FILTER ("Produktionsauftrag", "Produktionsauftrag" [ist voerspätet] = TRUE)) |
| verspätet in %                   | IFERROR( IF('Produktionsauftrag'[Spät \#] \<\> 0, 'Produktiosnauftrag'[Spät \#], IF('Produktionsauftrag'[Gesamtauftrag] = 0, BLANK(), 0)) / 'Produktionsauftrag'[Gesamtauftrag], BLANK()) |
| Rechtzeitig und vollständig        | COUNTROWS(FILTER('Produktionsauftrag', 'Produktionsauftrag'[vollständig] = TRUE && 'Produktionsauftrag'[verspätete] = FALSE && 'Produktionsauftrag'[Vorzeitig] = FALSE)) |
| Rechtzeitig und vollständig in Prozent      | IFERROR( IF('Produktionsauftrag'[Unvollständig] \<\> 0, 'Produktionsauftrag'[Rechtzeitig und vollständig], IF('Produktionsauftrag'[abgeschlossen] = 0, BLANK(), 0)) / 'Produktionsauftrag'[abgeschlossen], BLANK()) |
| Gesamtbestellung             | COUNTROWS (Produktionsauftrag) |
| Gesamtmenge           | SUMME('Produktionsauftrag'[Gute Menge]) + SUMME('Produktionsauftrag'[Fehlerhafte Menge]) |
| Fehlerrate (ppm)        | IF( 'Routentransaktion'[Verarbeitete Menge] = 0, BLANK(), (SUMME('Routentransaktion '[Fehlerhafte Menge]) / 'Routentransaktion'[Verarbeitete Menge]) \* 1000000) |
| Fehlerverhältnis (ppm) | IF( 'Routentransaktion'[Gesamte gemischte Menge] = 0, BLANK(), (SUMME('Routentransaktion '[Fehlerhafte Menge]) / 'Routentransaktion'[Gesamte gemischte Menge]) \* 1000000) |
| Verarbeitungsmenge       | SUMME (Arbeitsplanbuchungen [Gute Menge]) + SUMME (Arbeitsplanbuchung[Ausschussmenge]) |
| Gesamte gemischte Menge     | SUM('Produktionsauftrag'[Gute Menge]) + SUM('Routentransaktion'[Fehlerhafte Menge]) |

Die folgenden wichtigen Dimensionen im Verkaufscube werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

| Entität                    | Beispiele für Attribute                                        |
|---------------------------|---------------------------------------------------------------|
| Datum der Fertigmeldung | Abschlussdatum (Fertigmeldung), Monat und Jahr                 |
| Enddatum                | Beendetes Monatsgegenkonto und Monat                                  |
| Bedarfsdatum          | Bedarfsdatummonat Bedarfsdatum und Gegenkonto            |
| Arbeitsplan-Buchungsdatum    | Arbeitsplanbuchungsmonat Gegenkonto und Datum                       |
| Standorte                     | Standorte-Kennung, Standortsname, Bundesland und Ort                          |
| Entitäten                  | Benutzerkennung und Name                                                   |
| Ressourcen                 | Ressourcen-ID, Ressourcenname, Ressourcentyp und Ressourcengruppe |
| Produkte                  | Produktnummer, Produktname, Artikelgruppenname und Artikel-ID         |



