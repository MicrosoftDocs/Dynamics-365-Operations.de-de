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

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="9531f-104">Einkaufausgabenanalyse Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="9531f-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9531f-105">In diesem Thema wird beschrieben, was im **Einkaufs- und Ausgabenanalyse** Microsoft Power Bl Inhalt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9531f-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="9531f-106">Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9531f-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="9531f-107">Überblick</span><span class="sxs-lookup"><span data-stu-id="9531f-107">Overview</span></span>

<span data-ttu-id="9531f-108">Der **Einkaufs- und Ausgabenanalyse** Power BI Inhalt wurde entworfen, um Einkaufsleiter und Manager zu unterstützen, die für Budgets verantwortlich sind und ein Auge auf die Einkaufausgaben haben.</span><span class="sxs-lookup"><span data-stu-id="9531f-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="9531f-109">Manager können Einkaufsausgaben wie folgt analysieren:</span><span class="sxs-lookup"><span data-stu-id="9531f-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="9531f-110">Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)</span><span class="sxs-lookup"><span data-stu-id="9531f-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="9531f-111">Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie)</span><span class="sxs-lookup"><span data-stu-id="9531f-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="9531f-112">Es verwendet Transaktionsdaten und stellt eine Gesamtübersicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Einkaufsergebnisses für Debitoren und Produkte zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9531f-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="9531f-113">Berichte zeigen Änderungen im Einkauf, der im Zeitverlauf aufwendet.</span><span class="sxs-lookup"><span data-stu-id="9531f-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="9531f-114">Daher kann der Bericht dazu verwendet werden, um Manager über die positiven und negativen Ausgabentrends für einzelne Kreditoren und Produkten zu warnen.</span><span class="sxs-lookup"><span data-stu-id="9531f-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="9531f-115">Diagramme zeigen zusätzlich Einkaufsausgaben für unterschiedliche Beschaffungskategorien und Kreditorengruppen an.</span><span class="sxs-lookup"><span data-stu-id="9531f-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="9531f-116">Deshalb können Kategorie- und Regional-Manager die Diagramme nutzen, um Änderungen im Ausgabenverhalten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9531f-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="9531f-117">Zugreifen au Power BI Inhalt</span><span class="sxs-lookup"><span data-stu-id="9531f-117">Accessing the Power BI content</span></span>
<span data-ttu-id="9531f-118">Der **Einkaufausgabenanalyse** Poper BI-Inhalt wird auf der **Einkauf und Ausgabenanalyse** angezeigt (**Beschaffung** > **Abfragen und Berichte** > **Einkaufleistungsanalyse** > **Einkauf und Ausgabenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="9531f-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="9531f-119">Metrik, die im Power BI Inhalt enthalten ist</span><span class="sxs-lookup"><span data-stu-id="9531f-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="9531f-120">Der Power BI Inhalt **Einkaufsausgabenanalyse** enthält einen Bericht, der aus einem Satz Metriken besteht.</span><span class="sxs-lookup"><span data-stu-id="9531f-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="9531f-121">Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9531f-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="9531f-122">Die folgende Liste bietet eine Übersicht über die Visualisierungen.</span><span class="sxs-lookup"><span data-stu-id="9531f-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9531f-123">Berichtsseiten</span><span class="sxs-lookup"><span data-stu-id="9531f-123">Report page</span></span></th>
<th><span data-ttu-id="9531f-124">Diagramme</span><span class="sxs-lookup"><span data-stu-id="9531f-124">Charts</span></span></th>
<th><span data-ttu-id="9531f-125">Kacheln</span><span class="sxs-lookup"><span data-stu-id="9531f-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9531f-126">Einkauf pro Kreditor</span><span class="sxs-lookup"><span data-stu-id="9531f-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="9531f-127">Top 10 Kreditoren nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="9531f-128">Gesamte Bestellung nach Kreditorengruppe/Land/Name (Kreisdiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="9531f-129">Gesamte Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="9531f-130">Durchschnittlicher Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9531f-131">Gesamter Einkauf</span><span class="sxs-lookup"><span data-stu-id="9531f-131">Total purchase</span></span></li>
<li><span data-ttu-id="9531f-132">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="9531f-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="9531f-133">Kreditoren insgesamt</span><span class="sxs-lookup"><span data-stu-id="9531f-133">Total # vendors</span></span></li>
<li><span data-ttu-id="9531f-134">Summe aktive Kreditoren</span><span class="sxs-lookup"><span data-stu-id="9531f-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9531f-135">Einkaufs nach Produkt</span><span class="sxs-lookup"><span data-stu-id="9531f-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="9531f-136">Bestellung nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="9531f-137">Gesamteinkauf nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="9531f-138">Top 10 Produkte nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9531f-139">Produkte gesamt</span><span class="sxs-lookup"><span data-stu-id="9531f-139">Total # of products</span></span></li>
<li><span data-ttu-id="9531f-140">Gesamtanzahl der aktiven Produkte und Gesamtprozentsatz der Produkte</span><span class="sxs-lookup"><span data-stu-id="9531f-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="9531f-141">Zahl der Produkte, die zu 80% Einkauf betragen</span><span class="sxs-lookup"><span data-stu-id="9531f-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9531f-142">Einkaufsbericht nach Zeitraum\*</span><span class="sxs-lookup"><span data-stu-id="9531f-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="9531f-143">Einkauf nach Monat/Tag (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="9531f-144">Kumulative Abweichung des Einkaufs YOY (Wasserfalldiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="9531f-145">Gesamte Zunahme des Einkaufs YOY (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="9531f-146">Beschaffungsauszug (Matrix)</span><span class="sxs-lookup"><span data-stu-id="9531f-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9531f-147">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="9531f-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="9531f-148">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="9531f-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9531f-149">Einkauf pro Kreditorstandort</span><span class="sxs-lookup"><span data-stu-id="9531f-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="9531f-150">Einkauf nach Ort</span><span class="sxs-lookup"><span data-stu-id="9531f-150">Purchase by city</span></span></li>
<li><span data-ttu-id="9531f-151">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="9531f-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="9531f-152">Einkauf nach Land</span><span class="sxs-lookup"><span data-stu-id="9531f-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9531f-153">Einkaufausgabenanalyse nach Zeit</span><span class="sxs-lookup"><span data-stu-id="9531f-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="9531f-154">Einkauf aktuelles Jahr nach Monat/Tag (Liniendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="9531f-155">Einkauf aktuelles und letztes Jahr (Linien und Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="9531f-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9531f-156">Einkaufausgabenanalyse nach Kreditor</span><span class="sxs-lookup"><span data-stu-id="9531f-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="9531f-157">Top 10 % der Bestellung (Trichter)</span><span class="sxs-lookup"><span data-stu-id="9531f-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="9531f-158">Top 10-Kreditoren mit erhöhtem Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="9531f-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="9531f-159">Top 10-Kreditoren mit verringerten Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="9531f-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9531f-160">\\*Einkauf dieser und letzten Jahr und Wachstum nach Beschaffungskategorie.</span><span class="sxs-lookup"><span data-stu-id="9531f-160">\\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="9531f-161">Datenmodell und Entitäten</span><span class="sxs-lookup"><span data-stu-id="9531f-161">Data model and entities</span></span>
<span data-ttu-id="9531f-162">Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt **Einkaufs- und Ausgabenanalyse** auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="9531f-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="9531f-163">Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9531f-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="9531f-164">Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die zwecks Analyse optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="9531f-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="9531f-165">Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="9531f-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="9531f-166">Die gesamten Messungen in diesem Inhaltspaket sind die Teilmenge der gesamten Messungen, die im Einkaufscube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren.</span><span class="sxs-lookup"><span data-stu-id="9531f-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="9531f-167">Um die Cube-Messungen im Entitätspeicher bereitzustellen, müssen Sie diese bereitstellbar machen.</span><span class="sxs-lookup"><span data-stu-id="9531f-167">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="9531f-168">Weitere Informationen finden Sie unter dem Verfahren für die Bereitstellung aggregierter Messungen im Entitäts-Shop unter  [Power BI Integration mit Entität-Shop](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="9531f-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="9531f-169">Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.</span><span class="sxs-lookup"><span data-stu-id="9531f-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="9531f-170">Entität</span><span class="sxs-lookup"><span data-stu-id="9531f-170">Entity</span></span>        | <span data-ttu-id="9531f-171">Zentrale aggregierte Messungen</span><span class="sxs-lookup"><span data-stu-id="9531f-171">Key aggregate measurements</span></span> | <span data-ttu-id="9531f-172">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="9531f-172">Data source</span></span>                                 | <span data-ttu-id="9531f-173">Feld</span><span class="sxs-lookup"><span data-stu-id="9531f-173">Field</span></span>              | <span data-ttu-id="9531f-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9531f-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="9531f-175">Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="9531f-175">Invoice lines</span></span> | <span data-ttu-id="9531f-176">Einkauf</span><span class="sxs-lookup"><span data-stu-id="9531f-176">Purchase</span></span>                   | <span data-ttu-id="9531f-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="9531f-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="9531f-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="9531f-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="9531f-179">Der Betrag in der Buchhaltungswährung.</span><span class="sxs-lookup"><span data-stu-id="9531f-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="9531f-180">Die folgende Tabelle zeigt die wichtigen Messungen im Inhalt, die aus der Rechnungspositionsentität berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="9531f-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="9531f-181">Kennzahl</span><span class="sxs-lookup"><span data-stu-id="9531f-181">Measure</span></span>               | <span data-ttu-id="9531f-182">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="9531f-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9531f-183">Einkauf aktuelles Jahr</span><span class="sxs-lookup"><span data-stu-id="9531f-183">Purchase current year</span></span> | <span data-ttu-id="9531f-184">Einkauf aktuelles Jahr = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="9531f-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="9531f-185">Einkauf letztes Jahr</span><span class="sxs-lookup"><span data-stu-id="9531f-185">Purchase last year</span></span>    | <span data-ttu-id="9531f-186">Einkauf letztes Jahr = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="9531f-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="9531f-187">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="9531f-187">YOY purchase growth</span></span>   | <span data-ttu-id="9531f-188">YOY-Einkaufzunahme = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="9531f-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="9531f-189">Die folgenden wichtigen Dimensionen im Inhaltspaket werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9531f-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="9531f-190">Entität</span><span class="sxs-lookup"><span data-stu-id="9531f-190">Entity</span></span>                 | <span data-ttu-id="9531f-191">Beispiele für Attribute</span><span class="sxs-lookup"><span data-stu-id="9531f-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="9531f-192">Lieferanten</span><span class="sxs-lookup"><span data-stu-id="9531f-192">Vendors</span></span>                | <span data-ttu-id="9531f-193">Kreditorengruppen-, Kreditorregionen oder Land, Kreditorname</span><span class="sxs-lookup"><span data-stu-id="9531f-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="9531f-194">Produkte</span><span class="sxs-lookup"><span data-stu-id="9531f-194">Products</span></span>               | <span data-ttu-id="9531f-195">Produktnummer, Produktname, Artikelgruppenname</span><span class="sxs-lookup"><span data-stu-id="9531f-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="9531f-196">Beschaffungskategorien</span><span class="sxs-lookup"><span data-stu-id="9531f-196">Procurement categories</span></span> | <span data-ttu-id="9531f-197">Beschaffungskategorie, Beschaffungskategorienamen</span><span class="sxs-lookup"><span data-stu-id="9531f-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="9531f-198">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="9531f-198">Legal entities</span></span>         | <span data-ttu-id="9531f-199">Name der juristischen Person</span><span class="sxs-lookup"><span data-stu-id="9531f-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="9531f-200">Daten</span><span class="sxs-lookup"><span data-stu-id="9531f-200">Dates</span></span>                  | <span data-ttu-id="9531f-201">Daten, Jahresausgleich</span><span class="sxs-lookup"><span data-stu-id="9531f-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="9531f-202">Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahrs an.</span><span class="sxs-lookup"><span data-stu-id="9531f-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="9531f-203">Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern.</span><span class="sxs-lookup"><span data-stu-id="9531f-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="9531f-204">Sie können das den Unternehmensfilter auch ändern.</span><span class="sxs-lookup"><span data-stu-id="9531f-204">You can also change the company filter.</span></span>

