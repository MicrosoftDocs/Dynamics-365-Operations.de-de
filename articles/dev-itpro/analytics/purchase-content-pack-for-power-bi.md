---
title: Einkaufausgabenanalyse Power BI-Inhalt
description: "In diesem Thema wird beschrieben, was im Einkaufs- und Ausgabenanalyse Power Bl Inhalt enthalten ist. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet werden."
author: FrankDahl
manager: AnnBe
ms.date: 12/01/2017
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
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: f38f82b4275599a6b958c495f32b72778b400024
ms.contentlocale: de-de
ms.lasthandoff: 12/01/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="7676c-104">Einkaufausgabenanalyse Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="7676c-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7676c-105">In diesem Thema wird beschrieben, was im **Einkaufs- und Ausgabenanalyse** Microsoft Power Bl Inhalt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7676c-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="7676c-106">Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7676c-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="7676c-107">Überblick</span><span class="sxs-lookup"><span data-stu-id="7676c-107">Overview</span></span>

<span data-ttu-id="7676c-108">Der **Einkaufs- und Ausgabenanalyse** Power BI Inhalt wurde entworfen, um Einkaufsleiter und Manager zu unterstützen, die für Budgets verantwortlich sind und ein Auge auf die Einkaufausgaben haben.</span><span class="sxs-lookup"><span data-stu-id="7676c-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="7676c-109">Manager können Einkaufsausgaben wie folgt analysieren:</span><span class="sxs-lookup"><span data-stu-id="7676c-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="7676c-110">Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)</span><span class="sxs-lookup"><span data-stu-id="7676c-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="7676c-111">Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie)</span><span class="sxs-lookup"><span data-stu-id="7676c-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="7676c-112">Es verwendet Transaktionsdaten und stellt eine Gesamtübersicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Einkaufsergebnisses für Debitoren und Produkte zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7676c-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="7676c-113">Berichte zeigen Änderungen im Einkauf, der im Zeitverlauf aufwendet.</span><span class="sxs-lookup"><span data-stu-id="7676c-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="7676c-114">Daher kann der Bericht dazu verwendet werden, um Manager über die positiven und negativen Ausgabentrends für einzelne Kreditoren und Produkten zu warnen.</span><span class="sxs-lookup"><span data-stu-id="7676c-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="7676c-115">Diagramme zeigen zusätzlich Einkaufsausgaben für unterschiedliche Beschaffungskategorien und Kreditorengruppen an.</span><span class="sxs-lookup"><span data-stu-id="7676c-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="7676c-116">Deshalb können Kategorie- und Regional-Manager die Diagramme nutzen, um Änderungen im Ausgabenverhalten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7676c-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="7676c-117">Zugreifen au Power BI Inhalt</span><span class="sxs-lookup"><span data-stu-id="7676c-117">Accessing the Power BI content</span></span>
<span data-ttu-id="7676c-118">Der **Einkaufausgabenanalyse** Poper BI-Inhalt wird auf der **Einkauf und Ausgabenanalyse** angezeigt (**Beschaffung** > **Abfragen und Berichte** > **Einkaufleistungsanalyse** > **Einkauf und Ausgabenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="7676c-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="7676c-119">Metrik, die im Power BI Inhalt enthalten ist</span><span class="sxs-lookup"><span data-stu-id="7676c-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="7676c-120">Der Power BI Inhalt **Einkaufsausgabenanalyse** enthält einen Bericht, der aus einem Satz Metriken besteht.</span><span class="sxs-lookup"><span data-stu-id="7676c-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="7676c-121">Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7676c-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="7676c-122">Die folgende Liste bietet eine Übersicht über die Visualisierungen.</span><span class="sxs-lookup"><span data-stu-id="7676c-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7676c-123">Berichtsseiten</span><span class="sxs-lookup"><span data-stu-id="7676c-123">Report page</span></span></th>
<th><span data-ttu-id="7676c-124">Diagramme</span><span class="sxs-lookup"><span data-stu-id="7676c-124">Charts</span></span></th>
<th><span data-ttu-id="7676c-125">Kacheln</span><span class="sxs-lookup"><span data-stu-id="7676c-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7676c-126">Einkauf pro Kreditor</span><span class="sxs-lookup"><span data-stu-id="7676c-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="7676c-127">Top 10 Kreditoren nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="7676c-128">Gesamte Bestellung nach Kreditorengruppe/Land/Name (Kreisdiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="7676c-129">Gesamte Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="7676c-130">Durchschnittlicher Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7676c-131">Gesamter Einkauf</span><span class="sxs-lookup"><span data-stu-id="7676c-131">Total purchase</span></span></li>
<li><span data-ttu-id="7676c-132">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="7676c-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="7676c-133">Kreditoren insgesamt</span><span class="sxs-lookup"><span data-stu-id="7676c-133">Total # vendors</span></span></li>
<li><span data-ttu-id="7676c-134">Summe aktive Kreditoren</span><span class="sxs-lookup"><span data-stu-id="7676c-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7676c-135">Einkaufs nach Produkt</span><span class="sxs-lookup"><span data-stu-id="7676c-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="7676c-136">Bestellung nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="7676c-137">Gesamteinkauf nach Beschaffungskategorie Produktnamen (Tortendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="7676c-138">Top 10 Produkte nach Einkauf (gestapeltes Balkendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7676c-139">Produkte gesamt</span><span class="sxs-lookup"><span data-stu-id="7676c-139">Total # of products</span></span></li>
<li><span data-ttu-id="7676c-140">Gesamtanzahl der aktiven Produkte und Gesamtprozentsatz der Produkte</span><span class="sxs-lookup"><span data-stu-id="7676c-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="7676c-141">Zahl der Produkte, die zu 80% Einkauf betragen</span><span class="sxs-lookup"><span data-stu-id="7676c-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7676c-142">Einkaufsbericht nach Zeitraum*</span><span class="sxs-lookup"><span data-stu-id="7676c-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="7676c-143">Einkauf nach Monat/Tag (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="7676c-144">Kumulative Abweichung des Einkaufs YOY (Wasserfalldiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="7676c-145">Gesamte Zunahme des Einkaufs YOY (Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="7676c-146">Beschaffungsauszug (Matrix)</span><span class="sxs-lookup"><span data-stu-id="7676c-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7676c-147">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="7676c-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="7676c-148">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="7676c-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7676c-149">Einkauf pro Kreditorstandort</span><span class="sxs-lookup"><span data-stu-id="7676c-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="7676c-150">Einkauf nach Ort</span><span class="sxs-lookup"><span data-stu-id="7676c-150">Purchase by city</span></span></li>
<li><span data-ttu-id="7676c-151">YOY-Einkaufzunahme %</span><span class="sxs-lookup"><span data-stu-id="7676c-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="7676c-152">Einkauf nach Land</span><span class="sxs-lookup"><span data-stu-id="7676c-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7676c-153">Einkaufausgabenanalyse nach Zeit</span><span class="sxs-lookup"><span data-stu-id="7676c-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="7676c-154">Einkauf aktuelles Jahr nach Monat/Tag (Liniendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="7676c-155">Einkauf aktuelles und letztes Jahr (Linien und Spaltendiagramm)</span><span class="sxs-lookup"><span data-stu-id="7676c-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7676c-156">Einkaufausgabenanalyse nach Kreditor</span><span class="sxs-lookup"><span data-stu-id="7676c-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="7676c-157">Top 10 % der Bestellung (Trichter)</span><span class="sxs-lookup"><span data-stu-id="7676c-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="7676c-158">Top 10-Kreditoren mit erhöhtem Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="7676c-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="7676c-159">Top 10-Kreditoren mit verringerten Ausgaben YOY</span><span class="sxs-lookup"><span data-stu-id="7676c-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7676c-160">\*Einkauf dieser und letzten Jahr und Wachstum nach Beschaffungskategorie.</span><span class="sxs-lookup"><span data-stu-id="7676c-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="7676c-161">Erweitern des Power BI-Inhalts</span><span class="sxs-lookup"><span data-stu-id="7676c-161">Extending the Power BI content</span></span>
<span data-ttu-id="7676c-162">Wenn Sie die Inhaltspakete verwenden, die in Microsoft Dynamics Lifecycle Services (LCS) verfügbar sind, können Sie großartige Analysen für Person bereitstellen, die sich nicht in Microsoft Dynamics 365 anmelden.</span><span class="sxs-lookup"><span data-stu-id="7676c-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="7676c-163">Sie können diese Inhaltspakete so ändern, dass sie andere Berichte oder grafische Elemente umfassen, und die Inhaltspakete dann für die Analyse auf Ihrem Power BI.com-Mandanten veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="7676c-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="7676c-164">Sie finden den **Einkaufs- und Ausgabenanalyse**-Power BI-Inhalt in der freigegebenen Anlagenbibliothek in LCS.</span><span class="sxs-lookup"><span data-stu-id="7676c-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="7676c-165">Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="7676c-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="7676c-166">Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.</span><span class="sxs-lookup"><span data-stu-id="7676c-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="7676c-167">Stellen Sie sicher, dass Sie den **Einkaufs- und Ausgabenanalyse**-Inhalt herunterladen, der der von Ihnen verwendeten Dynamics 365-Version entspricht.</span><span class="sxs-lookup"><span data-stu-id="7676c-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="7676c-168">Wenn Sie Microsoft Dynamics 365 for Operations, Version 1611, verwenden, ist KB 4011327 eine Voraussetzung für diesen Power BI-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="7676c-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="7676c-169">Nachdem Sie sich bei LCS angemeldet haben, können Sie unter https://fix.lcs.dynamics.com/issue/results/?q=kb4011327 auf KB zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7676c-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="7676c-170">Datenmodell und Entitäten</span><span class="sxs-lookup"><span data-stu-id="7676c-170">Data model and entities</span></span>
<span data-ttu-id="7676c-171">Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt **Einkaufs- und Ausgabenanalyse** auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="7676c-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="7676c-172">Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7676c-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="7676c-173">Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die zwecks Analyse optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="7676c-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="7676c-174">Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="7676c-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="7676c-175">Die gesamten Messungen in diesem Inhaltspaket sind die Teilmenge der gesamten Messungen, die im Einkaufscube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren.</span><span class="sxs-lookup"><span data-stu-id="7676c-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="7676c-176">Um die Cube-Messungen im Entitätspeicher bereitzustellen, müssen Sie diese bereitstellbar machen.</span><span class="sxs-lookup"><span data-stu-id="7676c-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="7676c-177">Weitere Informationen finden Sie unter dem Verfahren für die Bereitstellung aggregierter Messungen im Entitäts-Shop unter  [Power BI Integration mit Entität-Shop](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="7676c-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="7676c-178">Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.</span><span class="sxs-lookup"><span data-stu-id="7676c-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="7676c-179">Entität</span><span class="sxs-lookup"><span data-stu-id="7676c-179">Entity</span></span>        | <span data-ttu-id="7676c-180">Zentrale aggregierte Messungen</span><span class="sxs-lookup"><span data-stu-id="7676c-180">Key aggregate measurements</span></span> | <span data-ttu-id="7676c-181">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="7676c-181">Data source</span></span>                                 | <span data-ttu-id="7676c-182">Feld</span><span class="sxs-lookup"><span data-stu-id="7676c-182">Field</span></span>              | <span data-ttu-id="7676c-183">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7676c-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="7676c-184">Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="7676c-184">Invoice lines</span></span> | <span data-ttu-id="7676c-185">Einkauf</span><span class="sxs-lookup"><span data-stu-id="7676c-185">Purchase</span></span>                   | <span data-ttu-id="7676c-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="7676c-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="7676c-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="7676c-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="7676c-188">Der Betrag in der Buchhaltungswährung.</span><span class="sxs-lookup"><span data-stu-id="7676c-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="7676c-189">Die folgende Tabelle zeigt die wichtigen Messungen im Inhalt, die aus der Rechnungspositionsentität berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="7676c-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="7676c-190">Kennzahl</span><span class="sxs-lookup"><span data-stu-id="7676c-190">Measure</span></span>               | <span data-ttu-id="7676c-191">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="7676c-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7676c-192">Einkauf aktuelles Jahr</span><span class="sxs-lookup"><span data-stu-id="7676c-192">Purchase current year</span></span> | <span data-ttu-id="7676c-193">Einkauf aktuelles Jahr = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="7676c-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="7676c-194">Einkauf letztes Jahr</span><span class="sxs-lookup"><span data-stu-id="7676c-194">Purchase last year</span></span>    | <span data-ttu-id="7676c-195">Einkauf letztes Jahr = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="7676c-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="7676c-196">YOY-Einkaufzunahme</span><span class="sxs-lookup"><span data-stu-id="7676c-196">YOY purchase growth</span></span>   | <span data-ttu-id="7676c-197">YOY-Einkaufzunahme = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="7676c-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="7676c-198">Die folgenden wichtigen Dimensionen im Inhaltspaket werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7676c-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="7676c-199">Entität</span><span class="sxs-lookup"><span data-stu-id="7676c-199">Entity</span></span>                 | <span data-ttu-id="7676c-200">Beispiele für Attribute</span><span class="sxs-lookup"><span data-stu-id="7676c-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="7676c-201">Lieferanten</span><span class="sxs-lookup"><span data-stu-id="7676c-201">Vendors</span></span>                | <span data-ttu-id="7676c-202">Kreditorengruppen-, Kreditorregionen oder Land, Kreditorname</span><span class="sxs-lookup"><span data-stu-id="7676c-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="7676c-203">Produkte</span><span class="sxs-lookup"><span data-stu-id="7676c-203">Products</span></span>               | <span data-ttu-id="7676c-204">Produktnummer, Produktname, Artikelgruppenname</span><span class="sxs-lookup"><span data-stu-id="7676c-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="7676c-205">Beschaffungskategorien</span><span class="sxs-lookup"><span data-stu-id="7676c-205">Procurement categories</span></span> | <span data-ttu-id="7676c-206">Beschaffungskategorie, Beschaffungskategorienamen</span><span class="sxs-lookup"><span data-stu-id="7676c-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="7676c-207">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="7676c-207">Legal entities</span></span>         | <span data-ttu-id="7676c-208">Name der juristischen Person</span><span class="sxs-lookup"><span data-stu-id="7676c-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="7676c-209">Daten</span><span class="sxs-lookup"><span data-stu-id="7676c-209">Dates</span></span>                  | <span data-ttu-id="7676c-210">Daten, Jahresausgleich</span><span class="sxs-lookup"><span data-stu-id="7676c-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="7676c-211">Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahrs an.</span><span class="sxs-lookup"><span data-stu-id="7676c-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="7676c-212">Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern.</span><span class="sxs-lookup"><span data-stu-id="7676c-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="7676c-213">Sie können das den Unternehmensfilter auch ändern.</span><span class="sxs-lookup"><span data-stu-id="7676c-213">You can also change the company filter.</span></span>

