---
title: Einkaufs- und Ausgabenanalyse Power BI-Inhalt
description: In diesem Thema wird beschrieben, was in den Inhalten der Einkaufs- und Ausgabenanalyse Power BI enthalten ist. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet werden.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "313841"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="2dcf3-104">Einkaufs- und Ausgabenanalyse Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="2dcf3-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dcf3-105">In diesem Thema wird beschrieben, was in den Inhalten der **Einkaufs- und Ausgabenanalyse** Microsoft Power BI enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="2dcf3-106">Es erläutert, wie Sie auf die Power BI-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="2dcf3-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2dcf3-107">Overview</span></span>

<span data-ttu-id="2dcf3-108">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt wurde entworfen, um Einkaufsleiter und Manager zu unterstützen, die für Budgets verantwortlich sind und ein Auge auf die Einkaufausgaben haben.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="2dcf3-109">Manager können Einkaufsausgaben wie folgt analysieren:</span><span class="sxs-lookup"><span data-stu-id="2dcf3-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="2dcf3-110">Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="2dcf3-111">Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="2dcf3-112">Es verwendet Transaktionsdaten und stellt eine Gesamtübersicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Einkaufsergebnisses für Debitoren und Produkte zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="2dcf3-113">Berichte zeigen Änderungen im Einkauf, der im Zeitverlauf aufwendet.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="2dcf3-114">Daher kann der Bericht dazu verwendet werden, um Manager über die positiven und negativen Ausgabentrends für einzelne Kreditoren und Produkten zu warnen.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="2dcf3-115">Diagramme zeigen zusätzlich Einkaufsausgaben für unterschiedliche Beschaffungskategorien und Kreditorengruppen an.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="2dcf3-116">Deshalb können Kategorie- und Regional-Manager die Diagramme nutzen, um Änderungen im Ausgabenverhalten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="2dcf3-117">Zugreifen auf den Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="2dcf3-117">Accessing the Power BI content</span></span>
<span data-ttu-id="2dcf3-118">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt wird auf der **Einkaufsausgabenanalyse**-Seit angezeigt (**Beschaffung** \> **Abfragen und Berichte** \> **Einkaufleistungsanalyse** \> **Einkaufs- und Ausgabenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="2dcf3-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="2dcf3-119">Metriken, die im Power BI-Inhalt enthalten sind</span><span class="sxs-lookup"><span data-stu-id="2dcf3-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="2dcf3-120">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt enthält einen Bericht, der aus einem Satz Metriken besteht.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="2dcf3-121">Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="2dcf3-122">Die folgende Liste bietet eine Übersicht über die Visualisierungen.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2dcf3-123">Berichtsseiten</span><span class="sxs-lookup"><span data-stu-id="2dcf3-123">Report page</span></span></th>
<th><span data-ttu-id="2dcf3-124">Diagramme</span><span class="sxs-lookup"><span data-stu-id="2dcf3-124">Charts</span></span></th>
<th><span data-ttu-id="2dcf3-125">Kacheln</span><span class="sxs-lookup"><span data-stu-id="2dcf3-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2dcf3-126">Einkauf pro Kreditor</span><span class="sxs-lookup"><span data-stu-id="2dcf3-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="2dcf3-127">Top 10 Kreditoren nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="2dcf3-128">Gesamte Bestellung nach Kreditorengruppe/Land/Name (Kreisdiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="2dcf3-129">Gesamte Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="2dcf3-130">Durchschnittlicher Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2dcf3-131">Gesamter Einkauf</span><span class="sxs-lookup"><span data-stu-id="2dcf3-131">Total purchase</span></span></li>
<li><span data-ttu-id="2dcf3-132">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="2dcf3-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="2dcf3-133">Kreditoren insgesamt</span><span class="sxs-lookup"><span data-stu-id="2dcf3-133">Total # vendors</span></span></li>
<li><span data-ttu-id="2dcf3-134">Summe aktive Kreditoren</span><span class="sxs-lookup"><span data-stu-id="2dcf3-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2dcf3-135">Einkaufs nach Produkt</span><span class="sxs-lookup"><span data-stu-id="2dcf3-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="2dcf3-136">Bestellung nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="2dcf3-137">Gesamteinkauf nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="2dcf3-138">Top 10 Produkte nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2dcf3-139">Produkte gesamt</span><span class="sxs-lookup"><span data-stu-id="2dcf3-139">Total # of products</span></span></li>
<li><span data-ttu-id="2dcf3-140">Gesamtanzahl der aktiven Produkte und Gesamtprozentsatz der Produkte</span><span class="sxs-lookup"><span data-stu-id="2dcf3-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="2dcf3-141">Zahl der Produkte, die zu 80% Einkauf betragen</span><span class="sxs-lookup"><span data-stu-id="2dcf3-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2dcf3-142">Einkaufsbericht nach Zeitraum\*</span><span class="sxs-lookup"><span data-stu-id="2dcf3-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="2dcf3-143">Einkauf nach Monat/Tag (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="2dcf3-144">Kumulative Abweichung des Einkaufs YOY (Wasserfalldiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="2dcf3-145">Gesamte Zunahme des Einkaufs YOY (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="2dcf3-146">Beschaffungsauszug (Matrix)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2dcf3-147">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="2dcf3-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="2dcf3-148">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="2dcf3-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2dcf3-149">Einkauf pro Kreditorstandort</span><span class="sxs-lookup"><span data-stu-id="2dcf3-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="2dcf3-150">Einkauf nach Ort</span><span class="sxs-lookup"><span data-stu-id="2dcf3-150">Purchase by city</span></span></li>
<li><span data-ttu-id="2dcf3-151">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="2dcf3-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="2dcf3-152">Einkauf nach Land</span><span class="sxs-lookup"><span data-stu-id="2dcf3-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="2dcf3-153">Einkaufausgabenanalyse nach Zeit</span><span class="sxs-lookup"><span data-stu-id="2dcf3-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="2dcf3-154">Einkauf aktuelles Jahr nach Monat/Tag (Liniendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="2dcf3-155">Einkauf aktuelles und letztes Jahr (Linien und Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="2dcf3-156">Einkaufausgabenanalyse nach Kreditor</span><span class="sxs-lookup"><span data-stu-id="2dcf3-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="2dcf3-157">Top 10 % der Bestellung (Trichter)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="2dcf3-158">Top 10-Kreditoren mit erhöhtem Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="2dcf3-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="2dcf3-159">Top 10-Kreditoren mit verringerten Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="2dcf3-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2dcf3-160">\*Einkauf dieser und letzten Jahr und Wachstum nach Beschaffungskategorie.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="2dcf3-161">Datenmodell und Entitäten</span><span class="sxs-lookup"><span data-stu-id="2dcf3-161">Data model and entities</span></span>
<span data-ttu-id="2dcf3-162">Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt im **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="2dcf3-163">Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="2dcf3-164">Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die für die Analyse optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="2dcf3-165">Weitere Informationen finden Sie in der [Übersicht Power BI-Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="2dcf3-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="2dcf3-166">Die aggregierenden Messungen in diesem Inhalt sind die Teilmenge der aggregierenden Messungen, die im Purchase Cube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="2dcf3-167">Um die Cube-Messungen im Entitätsspeicher bereitzustellen, müssen Sie diese bereitstellbar machen.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="2dcf3-168">Weitere Informationen finden Sie im Verfahren für die Bereitstellung aggregierender Messungen im Entitäts-Shop unter [Übersicht über die Power BI-Integration mit Entität-Shop](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="2dcf3-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="2dcf3-169">Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="2dcf3-170">Entität</span><span class="sxs-lookup"><span data-stu-id="2dcf3-170">Entity</span></span>        | <span data-ttu-id="2dcf3-171">Zentrale aggregierte Messungen</span><span class="sxs-lookup"><span data-stu-id="2dcf3-171">Key aggregate measurements</span></span> | <span data-ttu-id="2dcf3-172">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="2dcf3-172">Data source</span></span>                                 | <span data-ttu-id="2dcf3-173">Feld</span><span class="sxs-lookup"><span data-stu-id="2dcf3-173">Field</span></span>              | <span data-ttu-id="2dcf3-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dcf3-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="2dcf3-175">Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="2dcf3-175">Invoice lines</span></span> | <span data-ttu-id="2dcf3-176">Einkauf</span><span class="sxs-lookup"><span data-stu-id="2dcf3-176">Purchase</span></span>                   | <span data-ttu-id="2dcf3-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="2dcf3-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="2dcf3-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="2dcf3-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="2dcf3-179">Der Betrag in der Buchhaltungswährung.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="2dcf3-180">Die folgende Tabelle zeigt die wichtigen Messungen im Inhalt, die aus der Rechnungspositionsentität berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="2dcf3-181">Kennzahl</span><span class="sxs-lookup"><span data-stu-id="2dcf3-181">Measure</span></span>               | <span data-ttu-id="2dcf3-182">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="2dcf3-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dcf3-183">Einkauf aktuelles Jahr</span><span class="sxs-lookup"><span data-stu-id="2dcf3-183">Purchase current year</span></span> | <span data-ttu-id="2dcf3-184">Einkauf aktuelles Jahr = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="2dcf3-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="2dcf3-185">Einkauf letztes Jahr</span><span class="sxs-lookup"><span data-stu-id="2dcf3-185">Purchase last year</span></span>    | <span data-ttu-id="2dcf3-186">Einkauf letztes Jahr = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="2dcf3-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="2dcf3-187">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="2dcf3-187">YOY purchase growth</span></span>   | <span data-ttu-id="2dcf3-188">YOY-Einkaufzunahme = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="2dcf3-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="2dcf3-189">Die folgenden wichtigen Dimensionen im Inhaltspaket werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="2dcf3-190">Entität</span><span class="sxs-lookup"><span data-stu-id="2dcf3-190">Entity</span></span>                 | <span data-ttu-id="2dcf3-191">Beispiele für Attribute</span><span class="sxs-lookup"><span data-stu-id="2dcf3-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="2dcf3-192">Lieferanten</span><span class="sxs-lookup"><span data-stu-id="2dcf3-192">Vendors</span></span>                | <span data-ttu-id="2dcf3-193">Kreditorengruppen-, Kreditorregionen oder Land, Kreditorname</span><span class="sxs-lookup"><span data-stu-id="2dcf3-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="2dcf3-194">Produkte</span><span class="sxs-lookup"><span data-stu-id="2dcf3-194">Products</span></span>               | <span data-ttu-id="2dcf3-195">Produktnummer, Produktname, Artikelgruppenname</span><span class="sxs-lookup"><span data-stu-id="2dcf3-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="2dcf3-196">Beschaffungskategorien</span><span class="sxs-lookup"><span data-stu-id="2dcf3-196">Procurement categories</span></span> | <span data-ttu-id="2dcf3-197">Beschaffungskategorie, Beschaffungskategorienamen</span><span class="sxs-lookup"><span data-stu-id="2dcf3-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="2dcf3-198">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="2dcf3-198">Legal entities</span></span>         | <span data-ttu-id="2dcf3-199">Name der juristischen Person</span><span class="sxs-lookup"><span data-stu-id="2dcf3-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="2dcf3-200">Daten</span><span class="sxs-lookup"><span data-stu-id="2dcf3-200">Dates</span></span>                  | <span data-ttu-id="2dcf3-201">Daten, Jahresausgleich</span><span class="sxs-lookup"><span data-stu-id="2dcf3-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="2dcf3-202">Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahrs an.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="2dcf3-203">Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="2dcf3-204">Sie können das den Unternehmensfilter auch ändern.</span><span class="sxs-lookup"><span data-stu-id="2dcf3-204">You can also change the company filter.</span></span>
