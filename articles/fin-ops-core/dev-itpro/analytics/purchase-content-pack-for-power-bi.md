---
title: Einkaufs- und Ausgabenanalyse Power BI-Inhalt
description: In diesem Thema wird beschrieben, was in den Inhalten der Einkaufs- und Ausgabenanalyse Power BI enthalten ist. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet werden.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d25bacc2ec1f8e13376b96e188b099a184f7f8c6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569131"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="3c564-104">Einkaufs- und Ausgabenanalyse Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="3c564-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c564-105">In diesem Thema wird beschrieben, was in den Inhalten der **Einkaufs- und Ausgabenanalyse** Microsoft Power BI enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3c564-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="3c564-106">Es erläutert, wie Sie auf die Power BI-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c564-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="3c564-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="3c564-107">Overview</span></span>

<span data-ttu-id="3c564-108">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt wurde entworfen, um Einkaufsleiter und Manager zu unterstützen, die für Budgets verantwortlich sind und die Einkaufausgaben nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="3c564-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="3c564-109">Manager können Einkaufsausgaben wie folgt analysieren:</span><span class="sxs-lookup"><span data-stu-id="3c564-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="3c564-110">Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)</span><span class="sxs-lookup"><span data-stu-id="3c564-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="3c564-111">Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie)</span><span class="sxs-lookup"><span data-stu-id="3c564-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="3c564-112">Es verwendet Transaktionsdaten und stellt eine Gesamtübersicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Einkaufsergebnisses für Debitoren und Produkte zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3c564-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="3c564-113">Berichte zeigen Änderungen im Einkauf, der im Zeitverlauf aufwendet.</span><span class="sxs-lookup"><span data-stu-id="3c564-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="3c564-114">Daher kann der Bericht dazu verwendet werden, um Manager über die positiven und negativen Ausgabentrends für einzelne Kreditoren und Produkten zu warnen.</span><span class="sxs-lookup"><span data-stu-id="3c564-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="3c564-115">Diagramme zeigen zusätzlich Einkaufsausgaben für unterschiedliche Beschaffungskategorien und Kreditorengruppen an.</span><span class="sxs-lookup"><span data-stu-id="3c564-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="3c564-116">Deshalb können Kategorie- und Regional-Manager die Diagramme nutzen, um Änderungen im Ausgabenverhalten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3c564-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="3c564-117">Zugreifen auf den Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="3c564-117">Accessing the Power BI content</span></span>
<span data-ttu-id="3c564-118">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt wird auf der **Einkaufsausgabenanalyse**-Seit angezeigt (**Beschaffung** \> **Abfragen und Berichte** \> **Einkaufleistungsanalyse** \> **Einkaufs- und Ausgabenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="3c564-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="3c564-119">Metriken, die im Power BI-Inhalt enthalten sind</span><span class="sxs-lookup"><span data-stu-id="3c564-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="3c564-120">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt enthält einen Bericht, der aus einem Satz Metriken besteht.</span><span class="sxs-lookup"><span data-stu-id="3c564-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="3c564-121">Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3c564-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="3c564-122">Die folgenden Abschnitte bieten eine Übersicht über die Visualisierungen.</span><span class="sxs-lookup"><span data-stu-id="3c564-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="3c564-123">Berichtsseite „Einkauf nach Kreditor“</span><span class="sxs-lookup"><span data-stu-id="3c564-123">Purchase by vendor report page</span></span>
<span data-ttu-id="3c564-124">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="3c564-124">**Charts**</span></span>
- <span data-ttu-id="3c564-125">Top 10 Kreditoren nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="3c564-126">Gesamte Bestellung nach Kreditorengruppe/Land/Name (Kreisdiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="3c564-127">Gesamte Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="3c564-128">Durchschnittlicher Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="3c564-129">**Kacheln**</span><span class="sxs-lookup"><span data-stu-id="3c564-129">**Tiles**</span></span>
- <span data-ttu-id="3c564-130">Gesamter Einkauf</span><span class="sxs-lookup"><span data-stu-id="3c564-130">Total purchase</span></span>
- <span data-ttu-id="3c564-131">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="3c564-131">YOY purchase growth</span></span>
- <span data-ttu-id="3c564-132">Kreditoren insgesamt</span><span class="sxs-lookup"><span data-stu-id="3c564-132">Total # vendors</span></span>
- <span data-ttu-id="3c564-133">Summe aktive Kreditoren</span><span class="sxs-lookup"><span data-stu-id="3c564-133">Total # of active vendors</span></span>

<span data-ttu-id="3c564-134">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3c564-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="3c564-135">Berichtsseite „Einkauf nach Produkt“</span><span class="sxs-lookup"><span data-stu-id="3c564-135">Purchase by product report page</span></span>

<span data-ttu-id="3c564-136">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="3c564-136">**Charts**</span></span>
- <span data-ttu-id="3c564-137">Bestellung nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="3c564-138">Gesamteinkauf nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="3c564-139">Top 10 Produkte nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="3c564-140">**Kacheln**</span><span class="sxs-lookup"><span data-stu-id="3c564-140">**Tiles**</span></span>
- <span data-ttu-id="3c564-141">Produkte gesamt</span><span class="sxs-lookup"><span data-stu-id="3c564-141">Total # of products</span></span></li>
- <span data-ttu-id="3c564-142">Gesamtanzahl der aktiven Produkte und Gesamtprozentsatz der Produkte</span><span class="sxs-lookup"><span data-stu-id="3c564-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="3c564-143">Zahl der Produkte, die zu 80% Einkauf betragen</span><span class="sxs-lookup"><span data-stu-id="3c564-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="3c564-144">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3c564-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="3c564-145">Berichtsseite „Einkauf nach Zeitraum“</span><span class="sxs-lookup"><span data-stu-id="3c564-145">Purchase by period report page</span></span>
<span data-ttu-id="3c564-146">Diese Seite zeigt Einkäufe dieser und des letzten Jahres und den Wachstum nach Beschaffungskategorie.</span><span class="sxs-lookup"><span data-stu-id="3c564-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="3c564-147">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="3c564-147">**Charts**</span></span> 
- <span data-ttu-id="3c564-148">Einkauf nach Monat/Tag (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="3c564-149">Kumulative Abweichung des Einkaufs YOY (Wasserfalldiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="3c564-150">Gesamte Zunahme des Einkaufs YOY (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="3c564-151">Beschaffungsauszug (Matrix)</span><span class="sxs-lookup"><span data-stu-id="3c564-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="3c564-152">**Kacheln**</span><span class="sxs-lookup"><span data-stu-id="3c564-152">**Tiles**</span></span>
- <span data-ttu-id="3c564-153">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="3c564-153">YOY purchase growth</span></span>
- <span data-ttu-id="3c564-154">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="3c564-154">YOY purchase growth %</span></span>

<span data-ttu-id="3c564-155">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3c564-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="3c564-156">Berichtsseite „Einkauf nach Kreditorstandort“</span><span class="sxs-lookup"><span data-stu-id="3c564-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="3c564-157">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="3c564-157">**Charts**</span></span>
- <span data-ttu-id="3c564-158">Einkauf nach Ort</span><span class="sxs-lookup"><span data-stu-id="3c564-158">Purchase by city</span></span>
- <span data-ttu-id="3c564-159">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="3c564-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="3c564-160">Einkauf nach Land</span><span class="sxs-lookup"><span data-stu-id="3c564-160">Purchase by country</span></span>

<span data-ttu-id="3c564-161">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3c564-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="3c564-162">Berichtsseite „Einkaufausgabenanalyse nach Zeit“</span><span class="sxs-lookup"><span data-stu-id="3c564-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="3c564-163">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="3c564-163">**Charts**</span></span> 
- <span data-ttu-id="3c564-164">Einkauf aktuelles Jahr nach Monat/Tag (Liniendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="3c564-165">Einkauf aktuelles und letztes Jahr (Linien und Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="3c564-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="3c564-166">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3c564-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="3c564-167">Berichtsseite „Einkaufausgabenanalyse nach Kreditor“</span><span class="sxs-lookup"><span data-stu-id="3c564-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="3c564-168">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="3c564-168">**Charts**</span></span> 
- <span data-ttu-id="3c564-169">Top 10 % der Bestellung (Trichter)</span><span class="sxs-lookup"><span data-stu-id="3c564-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="3c564-170">Top 10-Kreditoren mit erhöhtem Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="3c564-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="3c564-171">Top 10-Kreditoren mit verringerten Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="3c564-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="3c564-172">**Beispiel** 
</span><span class="sxs-lookup"><span data-stu-id="3c564-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="3c564-173">Datenmodell und Entitäten</span><span class="sxs-lookup"><span data-stu-id="3c564-173">Data model and entities</span></span>
<span data-ttu-id="3c564-174">Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt im **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="3c564-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="3c564-175">Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3c564-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="3c564-176">Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die für die Analyse optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="3c564-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="3c564-177">Weitere Informationen finden Sie in der [Übersicht Power BI-Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="3c564-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="3c564-178">Die aggregierenden Messungen in diesem Inhalt sind die Teilmenge der aggregierenden Messungen, die im Purchase Cube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren.</span><span class="sxs-lookup"><span data-stu-id="3c564-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="3c564-179">Um die Cube-Messungen im Entitätsspeicher bereitzustellen, müssen Sie diese bereitstellbar machen.</span><span class="sxs-lookup"><span data-stu-id="3c564-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="3c564-180">Weitere Informationen finden Sie im Verfahren für die Bereitstellung aggregierender Messungen im Entitäts-Shop unter [Übersicht über die Power BI-Integration mit Entität-Shop](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="3c564-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="3c564-181">Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c564-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="3c564-182">Entität</span><span class="sxs-lookup"><span data-stu-id="3c564-182">Entity</span></span>        | <span data-ttu-id="3c564-183">Zentrale aggregierte Messungen</span><span class="sxs-lookup"><span data-stu-id="3c564-183">Key aggregate measurements</span></span> | <span data-ttu-id="3c564-184">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="3c564-184">Data source</span></span>                                 | <span data-ttu-id="3c564-185">Feld</span><span class="sxs-lookup"><span data-stu-id="3c564-185">Field</span></span>              | <span data-ttu-id="3c564-186">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c564-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="3c564-187">Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="3c564-187">Invoice lines</span></span> | <span data-ttu-id="3c564-188">Einkauf</span><span class="sxs-lookup"><span data-stu-id="3c564-188">Purchase</span></span>                   | <span data-ttu-id="3c564-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="3c564-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="3c564-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="3c564-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="3c564-191">Der Betrag in der Buchhaltungswährung.</span><span class="sxs-lookup"><span data-stu-id="3c564-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="3c564-192">Die folgende Tabelle zeigt die wichtigen Messungen im Inhalt, die aus der Rechnungspositionsentität berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="3c564-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="3c564-193">Kennzahl</span><span class="sxs-lookup"><span data-stu-id="3c564-193">Measure</span></span>               | <span data-ttu-id="3c564-194">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="3c564-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c564-195">Einkauf aktuelles Jahr</span><span class="sxs-lookup"><span data-stu-id="3c564-195">Purchase current year</span></span> | <span data-ttu-id="3c564-196">Einkauf aktuelles Jahr = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="3c564-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="3c564-197">Einkauf letztes Jahr</span><span class="sxs-lookup"><span data-stu-id="3c564-197">Purchase last year</span></span>    | <span data-ttu-id="3c564-198">Einkauf letztes Jahr = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="3c564-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="3c564-199">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="3c564-199">YOY purchase growth</span></span>   | <span data-ttu-id="3c564-200">YOY-Einkaufzunahme = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="3c564-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="3c564-201">Die folgenden wichtigen Dimensionen im Inhaltspaket werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3c564-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="3c564-202">Entität</span><span class="sxs-lookup"><span data-stu-id="3c564-202">Entity</span></span>                 | <span data-ttu-id="3c564-203">Beispiele für Attribute</span><span class="sxs-lookup"><span data-stu-id="3c564-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3c564-204">Lieferanten</span><span class="sxs-lookup"><span data-stu-id="3c564-204">Vendors</span></span>                | <span data-ttu-id="3c564-205">Kreditorengruppen-, Kreditorregionen oder Land, Kreditorname</span><span class="sxs-lookup"><span data-stu-id="3c564-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="3c564-206">Produkte</span><span class="sxs-lookup"><span data-stu-id="3c564-206">Products</span></span>               | <span data-ttu-id="3c564-207">Produktnummer, Produktname, Artikelgruppenname</span><span class="sxs-lookup"><span data-stu-id="3c564-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="3c564-208">Beschaffungskategorien</span><span class="sxs-lookup"><span data-stu-id="3c564-208">Procurement categories</span></span> | <span data-ttu-id="3c564-209">Beschaffungskategorie, Beschaffungskategorienamen</span><span class="sxs-lookup"><span data-stu-id="3c564-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="3c564-210">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="3c564-210">Legal entities</span></span>         | <span data-ttu-id="3c564-211">Name der juristischen Person</span><span class="sxs-lookup"><span data-stu-id="3c564-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="3c564-212">Daten</span><span class="sxs-lookup"><span data-stu-id="3c564-212">Dates</span></span>                  | <span data-ttu-id="3c564-213">Daten, Jahresausgleich</span><span class="sxs-lookup"><span data-stu-id="3c564-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="3c564-214">Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahrs an.</span><span class="sxs-lookup"><span data-stu-id="3c564-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="3c564-215">Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern.</span><span class="sxs-lookup"><span data-stu-id="3c564-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="3c564-216">Sie können das den Unternehmensfilter auch ändern.</span><span class="sxs-lookup"><span data-stu-id="3c564-216">You can also change the company filter.</span></span>
