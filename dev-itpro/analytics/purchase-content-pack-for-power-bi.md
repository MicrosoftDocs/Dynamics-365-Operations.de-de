---
title: Einkaufausgabenanalyse Power BI-Inhalt
description: "In diesem Thema wird beschrieben, was im Einkaufausgabenanalyse-Inhaltspaket für Microsoft Power Bl enthalten ist. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ad0ee95113d05710cccc1a5e9d215b38244c2047
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Einkaufausgabenanalyse Power BI-Inhalt

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, was im Einkaufausgabenanalyse-Inhaltspaket für Microsoft Power Bl enthalten ist. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen.

<a name="overview"></a>Überblick
--------

Das Einkaufausgabenanalyse-Inhaltspaket für Microsoft Power BI wurde für Einkaufsleiter und Manager erstellt, die für Budgets zuständig sind. Es wurde entworfen, um diese zu bei den Einkaufausgaben zu unterstützen. Es verwendet Transaktionsdaten aus von Microsoft Dynamics 365 for Operations und stellt eine Gesamtübesicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Einkaufsergebnisses für Debitoren und Produkte zur Verfügung. Berichte zeigen Änderungen im Einkauf, der im Zeitverlauf aufwendet. Daher können sie verwendet werden, um Manager über die positive und negative Ausgabentrends für einzelne Kreditoren und Produkten zu warnen. Diagramme anzeigen Einkaufausgabe für unterschiedliche Beschaffungskategorien und Kreditorengruppen. Kategorie- und regional Manager finden es möglicherweise hilfreich, Diagramme zu verwenden, mit deren Hilfe, Änderungen im Ausgabenverhalten zu identifizieren. Der Inhaltspaket ermöglicht Einkaufsleiter und Manager, die für Budgets, analysieren Einkauf zuständig sind wie folgt aufwendend:

-   Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)
-   Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie)

## <a name="accessing-the-content-pack"></a>Zugreifen auf das Inhaltspaket
Der Einkaufausgabenanalyse-Inhaltspaket für Power BI wird als Implementierungsressource in Microsoft Dynamics Lifecycle Services (LCS) veröffentlicht und kann von Dynamics 365 for Operations zugegriffen werden. Weitere Informationen dazu, wie Power BI-Bericht erstellt werden, finden Sie unter [Power Bi Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).
Hinweis: KB4011327 ist eine Voraussetzung für diesen Power BI Inhalt Nachdem Sie sich bei Lifecycle Services angemeldet haben, können Sie hier auf KB zugreifen: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="metrics-that-are-included-in-the-content-pack"></a>Metriken, die im Paket enthalten sind
Der Einkaufausgabenanalyse-Inhaltspaket enthält einen Bericht, der einem Satz Metriken besteht. Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt. Die folgende Tabelle enthält eine Übersicht der im Visualisierungen im Inhaltspaket.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Berichtsseiten</th>
<th>Diagramme</th>
<th>Kacheln</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Einkauf pro Kreditor</td>
<td><ul>
<li>Top 10 Kreditoren nach Einkauf (gestapeltes Balkendiagramm)</li>
<li>Gesamte Bestellung nach Kreditorengruppe/Land/Name (Kreisdiagramm)</li>
<li>Gesamte Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</li>
<li>Durchschnittlicher Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</li>
</ul></td>
<td><ul>
<li>Gesamter Einkauf</li>
<li>YOY-Einkaufzunahme</li>
<li>Kreditoren insgesamt</li>
<li>Summe aktive Kreditoren</li>
</ul></td>
</tr>
<tr class="even">
<td>Einkaufs nach Produkt</td>
<td><ul>
<li>Bestellung nach Beschaffungskategorie Produktnamen (Tortendiagramm)</li>
<li>Gesamteinkauf nach Beschaffungskategorie Produktnamen (Tortendiagramm)</li>
<li>Top 10 Produkte nach Einkauf (gestapeltes Balkendiagramm)</li>
</ul></td>
<td><ul>
<li>Produkte gesamt</li>
<li>Gesamtanzahl der aktiven Produkte und Gesamtprozentsatz der Produkte</li>
<li>Zahl der Produkte, die zu 80% Einkauf betragen</li>
</ul></td>
</tr>
<tr class="odd">
<td>Einkaufsbericht nach Zeitraum*</td>
<td><ul>
<li>Einkauf nach Monat/Tag (Spaltendiagramm)</li>
<li>Kumulative Abweichung des Einkaufs YOY (Wasserfalldiagramm)</li>
<li>Gesamte Zunahme des Einkaufs YOY (Spaltendiagramm)</li>
<li>Beschaffungsauszug (Matrix)</li>
</ul></td>
<td><ul>
<li>YOY-Einkaufzunahme</li>
<li>YOY-Einkaufzunahme %</li>
</ul></td>
</tr>
<tr class="even">
<td>Einkauf pro Kreditorstandort</td>
<td><ul>
<li>Einkauf nach Ort</li>
<li>YOY-Einkaufzunahme %</li>
<li>Einkauf nach Land</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Einkaufausgabenanalyse nach Zeit</td>
<td><ul>
<li>Einkauf aktuelles Jahr nach Monat/Tag (Liniendiagramm)</li>
<li>Einkauf aktuelles und letztes Jahr (Linien und Spaltendiagramm)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Einkaufausgabenanalyse nach Kreditor</td>
<td><ul>
<li>Top 10 % der Bestellung (Trichter)</li>
<li>Top 10-Kreditoren mit erhöhtem Ausgaben YOY</li>
<li>Top 10-Kreditoren mit verringerten Ausgaben YOY</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Einkauf dieser und letzten Jahr und Wachstum nach Beschaffungskategorie.

## <a name="data-model-and-entities"></a>Datenmodell und Entitäten
Dynamics 365 for Operations-Daten werden für den Bericht des Einkaufausgabenanalyse-Inhaltspakets verwendet. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Weitere Informationen zum Entitätsspeicher finden Sie unter [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Die gesamten Messungen in diesem Inhaltspaket sind die Teilmenge der gesamten Messungen, die im Purchase Cube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren. Um die Cube-Messungen im Entitätspeicher bereitzustellen, müssen Sie diese bereitstellbar machen. Weitere Informationen finden Sie unter [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.

| Entität        | Zentrale aggregierte Messungen | Datenquelle für Dynamics 365 for Operations | Feld              | Beschreibung                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Rechnungspositionen | Einkauf                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Der Betrag in der Buchhaltungswährung |

Die folgende Tabelle zeigt die wichtigen Messungen, das die im Paket aus Rechnungspositionsentitäten berechnet werden.

| Kennzahl               | Herstellkostenkalkulation                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Einkauf aktuelles Jahr | Einkauf aktuelles Jahr = SUM('Invoice lines'\[Purchase\])                                            |
| Einkauf letztes Jahr    | Einkauf letztes Jahr = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| YOY-Einkaufzunahme   | YOY-Einkaufzunahme = \[Purchase current year\] – \[Purchase last year\]                            |

Die folgenden wichtigen Dimensionen im Inhaltspaket werden als Filter verwendet, um die aggregierte Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

| Entität                 | Beispiele für Attribute                                |
|------------------------|-------------------------------------------------------|
| Lieferanten                | Kreditorengruppen-, Kreditorregionen oder Land, Kreditorname |
| Produkte               | Produktnummer, Produktname, Artikelgruppenname        |
| Beschaffungskategorien | Beschaffungskategorie, Beschaffungskategorienamen      |
| Juristische Personen         | Name der juristischen Person                                     |
| Daten                  | Daten, Jahresausgleich                                    |

Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahr an. Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern. Sie können das den Unternehmensfilter auch ändern.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)





