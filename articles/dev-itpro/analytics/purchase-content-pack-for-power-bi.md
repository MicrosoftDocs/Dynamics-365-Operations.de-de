---
title: Einkaufausgabenanalyse Power BI-Inhalt
description: "In diesem Thema wird beschrieben, was im Einkaufs- und Ausgabenanalyse Power Bl Inhalt enthalten ist. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet werden."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 07b6f433a8355d7f9ed6dce8e26f78d38a86a713
ms.contentlocale: de-de
ms.lasthandoff: 12/18/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Einkaufausgabenanalyse Power BI-Inhalt

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im **Einkaufs- und Ausgabenanalyse** Microsoft Power Bl Inhalt enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Überblick

Der **Einkaufs- und Ausgabenanalyse** Power BI Inhalt wurde entworfen, um Einkaufsleiter und Manager zu unterstützen, die für Budgets verantwortlich sind und ein Auge auf die Einkaufausgaben haben. Manager können Einkaufsausgaben wie folgt analysieren:

-   Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)
-   Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie)

Es verwendet Transaktionsdaten und stellt eine Gesamtübersicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Einkaufsergebnisses für Debitoren und Produkte zur Verfügung. Berichte zeigen Änderungen im Einkauf, der im Zeitverlauf aufwendet. Daher kann der Bericht dazu verwendet werden, um Manager über die positiven und negativen Ausgabentrends für einzelne Kreditoren und Produkten zu warnen. Diagramme zeigen zusätzlich Einkaufsausgaben für unterschiedliche Beschaffungskategorien und Kreditorengruppen an. Deshalb können Kategorie- und Regional-Manager die Diagramme nutzen, um Änderungen im Ausgabenverhalten zu identifizieren.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Der **Einkaufausgabenanalyse** Poper BI-Inhalt wird auf der **Einkauf und Ausgabenanalyse** angezeigt (**Beschaffung** > **Abfragen und Berichte** > **Einkaufleistungsanalyse** > **Einkauf und Ausgabenanalyse**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrik, die im Power BI Inhalt enthalten ist
Der Power BI Inhalt **Einkaufsausgabenanalyse** enthält einen Bericht, der aus einem Satz Metriken besteht. Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt. Die folgende Liste bietet eine Übersicht über die Visualisierungen.

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
Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt **Einkaufs- und Ausgabenanalyse** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).

Die gesamten Messungen in diesem Inhaltspaket sind die Teilmenge der gesamten Messungen, die im Einkaufscube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren. Um die Cube-Messungen im Entitätspeicher bereitzustellen, müssen Sie diese bereitstellbar machen. Weitere Informationen finden Sie unter dem Verfahren für die Bereitstellung aggregierter Messungen im Entitäts-Shop unter  [Power BI Integration mit Entität-Shop](power-bi-integration-entity-store.md). Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.

| Entität        | Zentrale aggregierte Messungen | Datenquelle                                 | Feld              | Beschreibung                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Rechnungspositionen | Einkauf                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Der Betrag in der Buchhaltungswährung. |

Die folgende Tabelle zeigt die wichtigen Messungen im Inhalt, die aus der Rechnungspositionsentität berechnet werden.

| Kennzahl               | Herstellkostenkalkulation                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Einkauf aktuelles Jahr | Einkauf aktuelles Jahr = SUM('Invoice lines'\[Purchase\])                                            |
| Einkauf letztes Jahr    | Einkauf letztes Jahr = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| YOY-Einkaufzunahme   | YOY-Einkaufzunahme = \[Purchase current year\] – \[Purchase last year\]                            |

Die folgenden wichtigen Dimensionen im Inhaltspaket werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

| Entität                 | Beispiele für Attribute                                |
|------------------------|-------------------------------------------------------|
| Lieferanten                | Kreditorengruppen-, Kreditorregionen oder Land, Kreditorname |
| Produkte               | Produktnummer, Produktname, Artikelgruppenname        |
| Beschaffungskategorien | Beschaffungskategorie, Beschaffungskategorienamen      |
| Juristische Personen         | Name der juristischen Person                                     |
| Daten                  | Daten, Jahresausgleich                                    |

Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahrs an. Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern. Sie können das den Unternehmensfilter auch ändern.

