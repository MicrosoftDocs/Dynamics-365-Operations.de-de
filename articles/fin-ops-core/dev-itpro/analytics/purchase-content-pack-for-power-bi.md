---
title: Einkaufs- und Ausgabenanalyse Power BI-Inhalt
description: In diesem Thema wird beschrieben, was in den Inhalten der Einkaufs- und Ausgabenanalyse Power BI enthalten ist.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4149b13754b544558dbb5666fbec7df97e5c5d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559548"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="39713-103">Einkaufs- und Ausgabenanalyse Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="39713-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39713-104">In diesem Thema wird beschrieben, was im Microsoft Power BI-Inhalt zur **Einkaufs- und Ausgabenanalyse** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="39713-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="39713-105">Es erläutert, wie Sie auf die Power BI-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39713-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="39713-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="39713-106">Overview</span></span>

<span data-ttu-id="39713-107">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt wurde entworfen, um Einkaufsleiter und Manager zu unterstützen, die für Budgets verantwortlich sind und die Einkaufausgaben nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="39713-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="39713-108">Manager können Einkaufsausgaben wie folgt analysieren:</span><span class="sxs-lookup"><span data-stu-id="39713-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="39713-109">Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)</span><span class="sxs-lookup"><span data-stu-id="39713-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="39713-110">Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie)</span><span class="sxs-lookup"><span data-stu-id="39713-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="39713-111">Es verwendet Transaktionsdaten und stellt eine Gesamtübersicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Einkaufsergebnisses für Debitoren und Produkte zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="39713-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="39713-112">Berichte zeigen Änderungen im Einkauf, der im Zeitverlauf aufwendet.</span><span class="sxs-lookup"><span data-stu-id="39713-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="39713-113">Daher kann der Bericht dazu verwendet werden, um Manager über die positiven und negativen Ausgabentrends für einzelne Kreditoren und Produkten zu warnen.</span><span class="sxs-lookup"><span data-stu-id="39713-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="39713-114">Diagramme zeigen zusätzlich Einkaufsausgaben für unterschiedliche Beschaffungskategorien und Kreditorengruppen an.</span><span class="sxs-lookup"><span data-stu-id="39713-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="39713-115">Deshalb können Kategorie- und Regional-Manager die Diagramme nutzen, um Änderungen im Ausgabenverhalten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="39713-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="39713-116">Zugreifen auf den Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="39713-116">Accessing the Power BI content</span></span>
<span data-ttu-id="39713-117">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt wird auf der **Einkaufsausgabenanalyse**-Seit angezeigt (**Beschaffung** \> **Abfragen und Berichte** \> **Einkaufleistungsanalyse** \> **Einkaufs- und Ausgabenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="39713-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="39713-118">Metriken, die im Power BI-Inhalt enthalten sind</span><span class="sxs-lookup"><span data-stu-id="39713-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="39713-119">Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt enthält einen Bericht, der aus einem Satz Metriken besteht.</span><span class="sxs-lookup"><span data-stu-id="39713-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="39713-120">Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt.</span><span class="sxs-lookup"><span data-stu-id="39713-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="39713-121">Die folgenden Abschnitte bieten eine Übersicht über die Visualisierungen.</span><span class="sxs-lookup"><span data-stu-id="39713-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="39713-122">Berichtsseite „Einkauf nach Kreditor“</span><span class="sxs-lookup"><span data-stu-id="39713-122">Purchase by vendor report page</span></span>
<span data-ttu-id="39713-123">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="39713-123">**Charts**</span></span>
- <span data-ttu-id="39713-124">Top 10 Kreditoren nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="39713-125">Gesamte Bestellung nach Kreditorengruppe/Land/Name (Kreisdiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="39713-126">Gesamte Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="39713-127">Durchschnittlicher Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="39713-128">**Kacheln**</span><span class="sxs-lookup"><span data-stu-id="39713-128">**Tiles**</span></span>
- <span data-ttu-id="39713-129">Gesamter Einkauf</span><span class="sxs-lookup"><span data-stu-id="39713-129">Total purchase</span></span>
- <span data-ttu-id="39713-130">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="39713-130">YOY purchase growth</span></span>
- <span data-ttu-id="39713-131">Kreditoren insgesamt</span><span class="sxs-lookup"><span data-stu-id="39713-131">Total # vendors</span></span>
- <span data-ttu-id="39713-132">Summe aktive Kreditoren</span><span class="sxs-lookup"><span data-stu-id="39713-132">Total # of active vendors</span></span>

<span data-ttu-id="39713-133">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="39713-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="39713-134">Berichtsseite „Einkauf nach Produkt“</span><span class="sxs-lookup"><span data-stu-id="39713-134">Purchase by product report page</span></span>

<span data-ttu-id="39713-135">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="39713-135">**Charts**</span></span>
- <span data-ttu-id="39713-136">Bestellung nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="39713-137">Gesamteinkauf nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="39713-138">Top 10 Produkte nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="39713-139">**Kacheln**</span><span class="sxs-lookup"><span data-stu-id="39713-139">**Tiles**</span></span>
- <span data-ttu-id="39713-140">Produkte gesamt</span><span class="sxs-lookup"><span data-stu-id="39713-140">Total # of products</span></span></li>
- <span data-ttu-id="39713-141">Gesamtanzahl der aktiven Produkte und Gesamtprozentsatz der Produkte</span><span class="sxs-lookup"><span data-stu-id="39713-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="39713-142">Zahl der Produkte, die zu 80% Einkauf betragen</span><span class="sxs-lookup"><span data-stu-id="39713-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="39713-143">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="39713-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="39713-144">Berichtsseite „Einkauf nach Zeitraum“</span><span class="sxs-lookup"><span data-stu-id="39713-144">Purchase by period report page</span></span>
<span data-ttu-id="39713-145">Diese Seite zeigt Einkäufe dieser und des letzten Jahres und den Wachstum nach Beschaffungskategorie.</span><span class="sxs-lookup"><span data-stu-id="39713-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="39713-146">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="39713-146">**Charts**</span></span> 
- <span data-ttu-id="39713-147">Einkauf nach Monat/Tag (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="39713-148">Kumulative Abweichung des Einkaufs YOY (Wasserfalldiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="39713-149">Gesamte Zunahme des Einkaufs YOY (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="39713-150">Beschaffungsauszug (Matrix)</span><span class="sxs-lookup"><span data-stu-id="39713-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="39713-151">**Kacheln**</span><span class="sxs-lookup"><span data-stu-id="39713-151">**Tiles**</span></span>
- <span data-ttu-id="39713-152">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="39713-152">YOY purchase growth</span></span>
- <span data-ttu-id="39713-153">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="39713-153">YOY purchase growth %</span></span>

<span data-ttu-id="39713-154">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="39713-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="39713-155">Berichtsseite „Einkauf nach Kreditorstandort“</span><span class="sxs-lookup"><span data-stu-id="39713-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="39713-156">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="39713-156">**Charts**</span></span>
- <span data-ttu-id="39713-157">Einkauf nach Ort</span><span class="sxs-lookup"><span data-stu-id="39713-157">Purchase by city</span></span>
- <span data-ttu-id="39713-158">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="39713-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="39713-159">Einkauf nach Land</span><span class="sxs-lookup"><span data-stu-id="39713-159">Purchase by country</span></span>

<span data-ttu-id="39713-160">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="39713-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="39713-161">Berichtsseite „Einkaufausgabenanalyse nach Zeit“</span><span class="sxs-lookup"><span data-stu-id="39713-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="39713-162">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="39713-162">**Charts**</span></span> 
- <span data-ttu-id="39713-163">Einkauf aktuelles Jahr nach Monat/Tag (Liniendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="39713-164">Einkauf aktuelles und letztes Jahr (Linien und Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="39713-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="39713-165">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="39713-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="39713-166">Berichtsseite „Einkaufausgabenanalyse nach Kreditor“</span><span class="sxs-lookup"><span data-stu-id="39713-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="39713-167">**Diagramme**</span><span class="sxs-lookup"><span data-stu-id="39713-167">**Charts**</span></span> 
- <span data-ttu-id="39713-168">Top 10 % der Bestellung (Trichter)</span><span class="sxs-lookup"><span data-stu-id="39713-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="39713-169">Top 10-Kreditoren mit erhöhtem Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="39713-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="39713-170">Top 10-Kreditoren mit verringerten Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="39713-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="39713-171">**Beispiel** 
</span><span class="sxs-lookup"><span data-stu-id="39713-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="39713-172">Datenmodell und Entitäten</span><span class="sxs-lookup"><span data-stu-id="39713-172">Data model and entities</span></span>
<span data-ttu-id="39713-173">Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt im **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="39713-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="39713-174">Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="39713-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="39713-175">Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die für die Analyse optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="39713-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="39713-176">Weitere Informationen finden Sie unter [Power BI Integration mit Entity Store](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="39713-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="39713-177">Die aggregierenden Messungen in diesem Inhalt sind die Teilmenge der aggregierenden Messungen, die im Purchase Cube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren.</span><span class="sxs-lookup"><span data-stu-id="39713-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="39713-178">Um die Cube-Messungen im Entitätsspeicher bereitzustellen, müssen Sie diese bereitstellbar machen.</span><span class="sxs-lookup"><span data-stu-id="39713-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="39713-179">Weitere Informationen finden Sie in der Vorgehensweise zum Bereitstellen von Aggregatmessungen im Entity Store unter [Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="39713-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="39713-180">Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.</span><span class="sxs-lookup"><span data-stu-id="39713-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="39713-181">Entität</span><span class="sxs-lookup"><span data-stu-id="39713-181">Entity</span></span>        | <span data-ttu-id="39713-182">Zentrale aggregierte Messungen</span><span class="sxs-lookup"><span data-stu-id="39713-182">Key aggregate measurements</span></span> | <span data-ttu-id="39713-183">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="39713-183">Data source</span></span>                                 | <span data-ttu-id="39713-184">Feld</span><span class="sxs-lookup"><span data-stu-id="39713-184">Field</span></span>              | <span data-ttu-id="39713-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39713-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="39713-186">Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="39713-186">Invoice lines</span></span> | <span data-ttu-id="39713-187">Einkauf</span><span class="sxs-lookup"><span data-stu-id="39713-187">Purchase</span></span>                   | <span data-ttu-id="39713-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="39713-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="39713-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="39713-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="39713-190">Der Betrag in der Buchhaltungswährung.</span><span class="sxs-lookup"><span data-stu-id="39713-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="39713-191">Die folgende Tabelle zeigt die wichtigen Messungen im Inhalt, die aus der Rechnungspositionsentität berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="39713-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="39713-192">Kennzahl</span><span class="sxs-lookup"><span data-stu-id="39713-192">Measure</span></span>               | <span data-ttu-id="39713-193">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="39713-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39713-194">Einkauf aktuelles Jahr</span><span class="sxs-lookup"><span data-stu-id="39713-194">Purchase current year</span></span> | <span data-ttu-id="39713-195">Einkauf aktuelles Jahr = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="39713-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="39713-196">Einkauf letztes Jahr</span><span class="sxs-lookup"><span data-stu-id="39713-196">Purchase last year</span></span>    | <span data-ttu-id="39713-197">Einkauf letztes Jahr = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="39713-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="39713-198">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="39713-198">YOY purchase growth</span></span>   | <span data-ttu-id="39713-199">YOY-Einkaufzunahme = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="39713-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="39713-200">Die folgenden wichtigen Dimensionen im Inhaltspaket werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="39713-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="39713-201">Entität</span><span class="sxs-lookup"><span data-stu-id="39713-201">Entity</span></span>                 | <span data-ttu-id="39713-202">Beispiele für Attribute</span><span class="sxs-lookup"><span data-stu-id="39713-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="39713-203">Lieferanten</span><span class="sxs-lookup"><span data-stu-id="39713-203">Vendors</span></span>                | <span data-ttu-id="39713-204">Kreditorengruppen-, Kreditorregionen oder Land, Kreditorname</span><span class="sxs-lookup"><span data-stu-id="39713-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="39713-205">Produkte</span><span class="sxs-lookup"><span data-stu-id="39713-205">Products</span></span>               | <span data-ttu-id="39713-206">Produktnummer, Produktname, Artikelgruppenname</span><span class="sxs-lookup"><span data-stu-id="39713-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="39713-207">Beschaffungskategorien</span><span class="sxs-lookup"><span data-stu-id="39713-207">Procurement categories</span></span> | <span data-ttu-id="39713-208">Beschaffungskategorie, Beschaffungskategorienamen</span><span class="sxs-lookup"><span data-stu-id="39713-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="39713-209">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="39713-209">Legal entities</span></span>         | <span data-ttu-id="39713-210">Name der juristischen Person</span><span class="sxs-lookup"><span data-stu-id="39713-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="39713-211">Daten</span><span class="sxs-lookup"><span data-stu-id="39713-211">Dates</span></span>                  | <span data-ttu-id="39713-212">Daten, Jahresausgleich</span><span class="sxs-lookup"><span data-stu-id="39713-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="39713-213">Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahrs an.</span><span class="sxs-lookup"><span data-stu-id="39713-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="39713-214">Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern.</span><span class="sxs-lookup"><span data-stu-id="39713-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="39713-215">Sie können das den Unternehmensfilter auch ändern.</span><span class="sxs-lookup"><span data-stu-id="39713-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]