---
title: "Einkaufausgabenanalyse Leistungsfähigkeit BIinhalt"
description: "In diesem Thema wird beschrieben, was im das Content Pack der Einkauf ausgaben-Analyse für Microsoft-Energie BI enthalten ist. Es erläutert, wie auf die Berichte, die im Paket enthalten inhaltliche sind, und enthält Informationen zum Datenmodell und die Entitäten, die verwendet werden, um das Inhaltstext Pack zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Einkaufausgabenanalyse Leistungsfähigkeit BIinhalt

In diesem Thema wird beschrieben, was im das Content Pack der Einkauf ausgaben-Analyse für Microsoft-Energie BI enthalten ist. Es erläutert, wie auf die Berichte, die im Paket enthalten inhaltliche sind, und enthält Informationen zum Datenmodell und die Entitäten, die verwendet werden, um das Inhaltstext Pack zu erstellen.

<a name="overview"></a>Überblick
--------

Der Inhaltstext Pack der Einkauf ausgaben-Analyse für Microsoft-Energie wurde für BI Einkaufsleiter und Manager erstellt, die für Budgets zuständig sind. Die Beschriftung besitzt entworfen, um diese zu unterstützen, bis ein auf Einkaufausgabe beizubehalten. Es verwendet - Transaktionsdaten vornehmen der Bestellung von Microsoft Dynamics 365 für Arbeitsgänge und bietet eine gesamte wertberichtigt unternehmensweiten und Einkaufzahlen Aufschlüsselung der Ausgabe als Einkauf nach Kreditor und Produkt. Berichte entsperren Änderungen im Einkauf hervor, der im Zeitverlauf aufwendet. Daher können sie verwendet werden, um Manager über die positive und negative Ausgabentrends für einzelne Kreditoren und Produkten zu warnen. Diagramme anzeigen Einkaufausgabe für unterschiedliche Beschaffungskategorien und Kreditorengruppen. Kategorie und Manager regionale fest es möglicherweise hilfreich, Diagramme diese zu verwenden, mit deren Hilfe, Änderungen im Ausgabenverhalten zu identifizieren. Der Inhaltstext Pack und ermöglicht Einkaufsleiter die Manager, die für Budgets, analysieren Einkauf zuständig sind wie folgt aufwendend:

-   Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)
-   Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie "

## <a name="accessing-the-content-pack"></a>Zugreifen des das Content Packs
Der Inhaltstext Pack der Einkauf ausgaben-Analyse wird als Implementierungsanlage in den Microsoft Dynamics Lifecycle Services (LCS) veröffentlicht und kann von Microsoft Dynamics 365 für Arbeitsgänge zugegriffen werden. Weitere Informationen dazu, wie BIberichte Energie, finden Sie auf zugreift und öffnet [Leistung in BIinhalt Kreditbriefen von Microsoft und von den Partnern] (power-bi-content-microsoft-partners.md ).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Metrik, das das Content im Paket enthalten sind
Der Inhaltstext Pack der Einkauf ausgaben-Analyse enthält einen Bericht, der einem Satz Metriken besteht. Dadurch werden Metrik als Diagramme, Kacheln und Tabellen visuell dargestellt. Die folgende Tabelle enthält eine Übersicht der im Visualisierungen das Content Pack.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Berichtsseite</th>
<th>Diagramme</th>
<th>Tiles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bestellung nach Kreditor</td>
<td><ul>
<li>Top 10 Kreditoren durch Kauf "gestapeltes Balkendiagramm)</li>
<li>Gesamte Bestellung nach Kreditorengruppe/Land/Name (Kreisdiagramm)</li>
<li>Bestellung nach Kreditorengruppe/Land/Name (Spaltendiagramm)</li>
<li>Durchschnittlicher Bestellung nach Kreditorengruppe/Land/Name (Spaltendiagramm)</li>
</ul></td>
<td><ul>
<li>Gesamter Einkauf</li>
<li>YOY-Einkaufzunahme</li>
<li>Summe # Kreditoren</li>
<li>Summe # aktive Kreditoren</li>
</ul></td>
</tr>
<tr class="even">
<td>Einkaufnebenprodukt</td>
<td><ul>
<li>Bestellung nach Beschaffungskategorie Produktnamen Spaltendiagramm (/)</li>
<li>Gesamte Bestellung nach Beschaffungskategorie Produktnamen Kreisdiagramm (/)</li>
<li>Top 10 Produkte durch Kauf "gestapeltes Balkendiagramm)</li>
</ul></td>
<td><ul>
<li># Summe Produkte</li>
<li>Gesamter aktiver Produktprozentsatz der # Summe Produkte</li>
<li>Produkte, die Nummer 80% betragen Einkauf</li>
</ul></td>
</tr>
<tr class="odd">
<td>Einkauf von period*</td>
<td><ul>
<li>Einkauf nach Monat (Tag/Spaltendiagramm)</li>
<li>Kumulative Abweichung des Einkaufs YOY (Wasserfalldiagramm)</li>
<li>Gesamte Zunahme des Einkaufs YOY Spaltendiagramm ()</li>
<li>Beschaffungsauszug (Matrix-)</li>
</ul></td>
<td><ul>
<li>YOY-Einkaufzunahme</li>
<li>YOY-Einkaufzunahme %</li>
</ul></td>
</tr>
<tr class="even">
<td>Bestellung nach Standort des Kreditors</td>
<td><ul>
<li>Bestellung nach Ort</li>
<li>% Der Bestellung YOY Wachstum</li>
<li>Bestellung nach Land</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Einkaufausgabenanalyse nach Zeit</td>
<td><ul>
<li>Einkaufaktuelles nach Monat des (Tag/Liniendiagramm)</li>
<li>Einkaufstrom und Jahr (Position und -letztes Spaltendiagramm)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Einkaufausgabenanalyse nach Kreditor</td>
<td><ul>
<li>Bestellungen Top 10 % der Bestellung (Trichter)</li>
<li>Top 10 Kreditoren mit erhöhtem Ausgabenyoy</li>
<li>Top 10 Kreditoren mit verringertem Ausgabenyoy</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Einkauf dieses Jahr und letzte Jahr nach Beschaffungskategorie und Wachstum

## <a name="data-model-and-entities"></a>Datenmodell und Entitäten
Dynamics 365 für Arbeitsgangsdaten wird für den Bericht unter das Content Pack der Einkauf ausgaben-Analyse verwendet. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Weitere Informationen zum Entitätsshop, finden Sie Entitäts-Shop mit [Power BI-Integration in Dynamics Blogbeitrag] (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)-. Die gesamten Messungen in diesem das Content Pack sind die Teilmenge von vollständigen Messungen, die im Einkauf-Cuben in Microsoft Dynamics AX 2012 und Microsoft Dynamics 365 für Arbeitsgänge R3 2012 verfügbar waren. Zur Phase die gesamten Messungen des Cubes im Entitätsshop, müssen sie zur Bereitstellung geeignet ist. Weitere Informationen finden Sie in der Prozedur für die Bereitstellung von Messungen im gesamten Entitätsshop im Feld [Power BI-Integration mit Entitäts-Shop in Dynamics Blogbeitrag] (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)-. Die folgenden Schlüsselaggregatsmessungen sind direkt aus den Rechnungspositionen Entität verfügbar und werden als Grundlage des das Content Packs verwendet.

| Entität        | Key aggregate measurements | Datenquelle für Dynamics 365 für Arbeitsgänge | Feld              | Beschreibung                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Rechnungspositionen | Einkauf                   | VendInvoiceTrans                            | SUMME (LineAmountMST) | Der Betrag in der Buchhaltungswährung |

Die folgende Tabelle zeigt die Tastenfunktionen Messungen, das die im Paket mit der Rechnungspositionsentität berechnet werden.

| Kennzahl               | Herstellkostenkalkulation                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Einkaufaktuelles des | Einkaufaktuelles = des SUMME ('Rechnung lines'entity_PLACEHOLDER \\][Einkauf                                            |
| Einkaufletztes des    | Einkaufletztes des BERECHNEN = (SUMME ('Rechnung lines'entity_PLACEHOLDER \ [Einkauf \], SAMEPERIODLASTYEAR " Datumsangaben\[\]) |
| YOY-Einkaufzunahme   | YOY-Einkauf-Zunahme- = \[Einkaufaktuelles\] des \[\] \[\]des                            |

Die folgenden wichtigen Dimensionen im das Content Pack werden als Filter verwendet, um die gesamten Messungen ein Crossdocking, dass Sie mehr tiefere Granularität und analytische Einblicke erreichen können.

| Entität                 | Beispiele für Attribute                                |
|------------------------|-------------------------------------------------------|
| Lieferanten                | Kreditorengruppen-, Regionen, Kreditorenland oder Kreditors |
| Produkte               | Produktnummer, Produktname, Artikelgruppenname        |
| Beschaffungskategorien | Beschaffungskategorie, Beschaffungskategorienamen      |
| Juristische Personen         | Name der juristischen Person                                     |
| Daten                  | Datumsangaben, Jahrgegenkonto                                    |

Standardmäßig zeigt das Inhaltstext Pack Daten während des laufenden Kalenderjahr an. Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern. Sie können den Unternehmensfilter auch ändern.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)



