---
title: Beispiele und Logik für Inventarfäligkeitsberichte
description: In diesem Thema werden einige Beispiele vorgestellt, die zeigen, wie die Ergebnisse eines Inventaralterungsberichts interpretiert werden.
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484529"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="12efc-103">Beispiele und Logik für Inventarfäligkeitsberichte</span><span class="sxs-lookup"><span data-stu-id="12efc-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12efc-104">In diesem Thema werden einige Beispiele vorgestellt, die zeigen, wie die Ergebnisse eines **Inventarfälligkeitsberichts** interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="12efc-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="12efc-105">In diesem Bericht werden die verfügbaren Mengen- und Bestandswerte für einen ausgewählten Artikel oder eine Artikelgruppe in mehrere Periodenbereiche unterteilt.</span><span class="sxs-lookup"><span data-stu-id="12efc-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="12efc-106">Dieses Thema zeigt auch die interne Logik des Berichts.</span><span class="sxs-lookup"><span data-stu-id="12efc-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="12efc-107">Die Beispiele in diesem Thema zeigen Ergebnisse, die auf einem Standard **Fälligkeit des Inventar** Berichts dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="12efc-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="12efc-108">Im Allgemeinen empfehlen wir jedoch die Verwendung der Version [Speicherung von Inventarfälligkeitsberichten](inventory-aging-report-storage.md) dieses Berichts, insbesondere wenn Sie viele Artikel und Lager haben, die verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="12efc-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="12efc-109">Durch die Speicherung von Inventarfälligkeitsberichten wird jeder von Ihnen erstellte Bericht gespeichert, die Ergebnisse als interaktive Seite und als Diagramm angezeigt und Sie können jeden gespeicherten Bericht exportieren.</span><span class="sxs-lookup"><span data-stu-id="12efc-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="12efc-110">Beispieldaten, die in diesen Beispielen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="12efc-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="12efc-111">Die Beispiele in diesem Thema basieren auf den in diesem Abschnitt beschriebenen Beispieltransaktionsdaten für das Inventar.</span><span class="sxs-lookup"><span data-stu-id="12efc-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="12efc-112">Lagerdimensionsgruppe einrichten</span><span class="sxs-lookup"><span data-stu-id="12efc-112">Storage dimension setup</span></span>

<span data-ttu-id="12efc-113">Das Beispielsystem enthält die folgenden Einstellungen für die Speicherabmessungen.</span><span class="sxs-lookup"><span data-stu-id="12efc-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="12efc-114">Name</span><span class="sxs-lookup"><span data-stu-id="12efc-114">Name</span></span>      | <span data-ttu-id="12efc-115">Aktiv</span><span class="sxs-lookup"><span data-stu-id="12efc-115">Active</span></span> | <span data-ttu-id="12efc-116">Physischer Bestand</span><span class="sxs-lookup"><span data-stu-id="12efc-116">Physical inventory</span></span> | <span data-ttu-id="12efc-117">Wertmäßiger Bestand</span><span class="sxs-lookup"><span data-stu-id="12efc-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="12efc-118">Site</span><span class="sxs-lookup"><span data-stu-id="12efc-118">Site</span></span>      | <span data-ttu-id="12efc-119">Ja</span><span class="sxs-lookup"><span data-stu-id="12efc-119">Yes</span></span>    | <span data-ttu-id="12efc-120">Ja</span><span class="sxs-lookup"><span data-stu-id="12efc-120">Yes</span></span>                | <span data-ttu-id="12efc-121">Ja</span><span class="sxs-lookup"><span data-stu-id="12efc-121">Yes</span></span>                 |
| <span data-ttu-id="12efc-122">Lagerort</span><span class="sxs-lookup"><span data-stu-id="12efc-122">Warehouse</span></span> | <span data-ttu-id="12efc-123">Ja</span><span class="sxs-lookup"><span data-stu-id="12efc-123">Yes</span></span>    | <span data-ttu-id="12efc-124">Ja</span><span class="sxs-lookup"><span data-stu-id="12efc-124">Yes</span></span>                | <span data-ttu-id="12efc-125">Nr.</span><span class="sxs-lookup"><span data-stu-id="12efc-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="12efc-126">Lagermodell</span><span class="sxs-lookup"><span data-stu-id="12efc-126">Inventory model</span></span>

<span data-ttu-id="12efc-127">Für das Beispielsystem lautet das Bestandsmodell für die freigegebenen Produkte *FIFO*, und die **Selbstkostenpreis** Einstellung für das Bestandsmodell ist auf *Physischen Wert einschließen* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12efc-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="12efc-128">Lagerbuchungen</span><span class="sxs-lookup"><span data-stu-id="12efc-128">Inventory transactions</span></span>

<span data-ttu-id="12efc-129">Das Beispielsystem enthält die folgenden Inventurtransaktionen für ein freigegebenes Produkt mit der Artikelnummer *1000*.</span><span class="sxs-lookup"><span data-stu-id="12efc-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="12efc-130">Referenz</span><span class="sxs-lookup"><span data-stu-id="12efc-130">Reference</span></span>      | <span data-ttu-id="12efc-131">Site</span><span class="sxs-lookup"><span data-stu-id="12efc-131">Site</span></span> | <span data-ttu-id="12efc-132">Lagerort</span><span class="sxs-lookup"><span data-stu-id="12efc-132">Warehouse</span></span> | <span data-ttu-id="12efc-133">Zugang</span><span class="sxs-lookup"><span data-stu-id="12efc-133">Receipt</span></span>   | <span data-ttu-id="12efc-134">Abgang</span><span class="sxs-lookup"><span data-stu-id="12efc-134">Issue</span></span> | <span data-ttu-id="12efc-135">Physisches Datum</span><span class="sxs-lookup"><span data-stu-id="12efc-135">Physical date</span></span> | <span data-ttu-id="12efc-136">Finanzdatum</span><span class="sxs-lookup"><span data-stu-id="12efc-136">Financial date</span></span> | <span data-ttu-id="12efc-137">Leistung</span><span class="sxs-lookup"><span data-stu-id="12efc-137">Quantity</span></span> | <span data-ttu-id="12efc-138">Betrag KORE</span><span class="sxs-lookup"><span data-stu-id="12efc-138">Cost amount</span></span> | <span data-ttu-id="12efc-139">Phys. Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="12efc-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="12efc-140">Bestellung</span><span class="sxs-lookup"><span data-stu-id="12efc-140">Purchase order</span></span> | <span data-ttu-id="12efc-141">1</span><span class="sxs-lookup"><span data-stu-id="12efc-141">1</span></span>    | <span data-ttu-id="12efc-142">11</span><span class="sxs-lookup"><span data-stu-id="12efc-142">11</span></span>        | <span data-ttu-id="12efc-143">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="12efc-143">Purchased</span></span> |       | <span data-ttu-id="12efc-144">15. März</span><span class="sxs-lookup"><span data-stu-id="12efc-144">March 15</span></span>      | <span data-ttu-id="12efc-145">15. März</span><span class="sxs-lookup"><span data-stu-id="12efc-145">March 15</span></span>       | <span data-ttu-id="12efc-146">10</span><span class="sxs-lookup"><span data-stu-id="12efc-146">10</span></span>       | <span data-ttu-id="12efc-147">1.000</span><span class="sxs-lookup"><span data-stu-id="12efc-147">1,000</span></span>       | <span data-ttu-id="12efc-148">1.000</span><span class="sxs-lookup"><span data-stu-id="12efc-148">1,000</span></span>                |
| <span data-ttu-id="12efc-149">Bestellung</span><span class="sxs-lookup"><span data-stu-id="12efc-149">Purchase order</span></span> | <span data-ttu-id="12efc-150">2</span><span class="sxs-lookup"><span data-stu-id="12efc-150">2</span></span>    | <span data-ttu-id="12efc-151">21</span><span class="sxs-lookup"><span data-stu-id="12efc-151">21</span></span>        | <span data-ttu-id="12efc-152">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="12efc-152">Purchased</span></span> |       | <span data-ttu-id="12efc-153">15. März</span><span class="sxs-lookup"><span data-stu-id="12efc-153">March 15</span></span>      | <span data-ttu-id="12efc-154">15. März</span><span class="sxs-lookup"><span data-stu-id="12efc-154">March 15</span></span>       | <span data-ttu-id="12efc-155">10</span><span class="sxs-lookup"><span data-stu-id="12efc-155">10</span></span>       | <span data-ttu-id="12efc-156">2,000</span><span class="sxs-lookup"><span data-stu-id="12efc-156">2,000</span></span>       | <span data-ttu-id="12efc-157">2,000</span><span class="sxs-lookup"><span data-stu-id="12efc-157">2,000</span></span>                |
| <span data-ttu-id="12efc-158">Bestellung</span><span class="sxs-lookup"><span data-stu-id="12efc-158">Purchase order</span></span> | <span data-ttu-id="12efc-159">1</span><span class="sxs-lookup"><span data-stu-id="12efc-159">1</span></span>    | <span data-ttu-id="12efc-160">11</span><span class="sxs-lookup"><span data-stu-id="12efc-160">11</span></span>        | <span data-ttu-id="12efc-161">Eingegangen</span><span class="sxs-lookup"><span data-stu-id="12efc-161">Received</span></span>  |       | <span data-ttu-id="12efc-162">April 15</span><span class="sxs-lookup"><span data-stu-id="12efc-162">April 15</span></span>      |                | <span data-ttu-id="12efc-163">5</span><span class="sxs-lookup"><span data-stu-id="12efc-163">5</span></span>        |             | <span data-ttu-id="12efc-164">375</span><span class="sxs-lookup"><span data-stu-id="12efc-164">375</span></span>                  |
| <span data-ttu-id="12efc-165">Umlagerungsauftrag</span><span class="sxs-lookup"><span data-stu-id="12efc-165">Transfer order</span></span> | <span data-ttu-id="12efc-166">1</span><span class="sxs-lookup"><span data-stu-id="12efc-166">1</span></span>    | <span data-ttu-id="12efc-167">11</span><span class="sxs-lookup"><span data-stu-id="12efc-167">11</span></span>        |           | <span data-ttu-id="12efc-168">Verkauft</span><span class="sxs-lookup"><span data-stu-id="12efc-168">Sold</span></span>  | <span data-ttu-id="12efc-169">Mai 2</span><span class="sxs-lookup"><span data-stu-id="12efc-169">May 2</span></span>         | <span data-ttu-id="12efc-170">Mai 2</span><span class="sxs-lookup"><span data-stu-id="12efc-170">May 2</span></span>          | <span data-ttu-id="12efc-171">-5</span><span class="sxs-lookup"><span data-stu-id="12efc-171">-5</span></span>       | <span data-ttu-id="12efc-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="12efc-172">-458.33</span></span>     | <span data-ttu-id="12efc-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="12efc-173">-458.33</span></span>              |
| <span data-ttu-id="12efc-174">Umlagerungsauftrag</span><span class="sxs-lookup"><span data-stu-id="12efc-174">Transfer order</span></span> | <span data-ttu-id="12efc-175">1</span><span class="sxs-lookup"><span data-stu-id="12efc-175">1</span></span>    | <span data-ttu-id="12efc-176">12</span><span class="sxs-lookup"><span data-stu-id="12efc-176">12</span></span>        | <span data-ttu-id="12efc-177">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="12efc-177">Purchased</span></span> |       | <span data-ttu-id="12efc-178">Mai 2</span><span class="sxs-lookup"><span data-stu-id="12efc-178">May 2</span></span>         | <span data-ttu-id="12efc-179">Mai 2</span><span class="sxs-lookup"><span data-stu-id="12efc-179">May 2</span></span>          | <span data-ttu-id="12efc-180">5</span><span class="sxs-lookup"><span data-stu-id="12efc-180">5</span></span>        | <span data-ttu-id="12efc-181">458.33</span><span class="sxs-lookup"><span data-stu-id="12efc-181">458.33</span></span>      | <span data-ttu-id="12efc-182">458.33</span><span class="sxs-lookup"><span data-stu-id="12efc-182">458.33</span></span>               |
| <span data-ttu-id="12efc-183">Auftrag</span><span class="sxs-lookup"><span data-stu-id="12efc-183">Sales order</span></span>    | <span data-ttu-id="12efc-184">1</span><span class="sxs-lookup"><span data-stu-id="12efc-184">1</span></span>    | <span data-ttu-id="12efc-185">12</span><span class="sxs-lookup"><span data-stu-id="12efc-185">12</span></span>        |           | <span data-ttu-id="12efc-186">Verkauft</span><span class="sxs-lookup"><span data-stu-id="12efc-186">Sold</span></span>  | <span data-ttu-id="12efc-187">Mai 3</span><span class="sxs-lookup"><span data-stu-id="12efc-187">May 3</span></span>         | <span data-ttu-id="12efc-188">Mai 3</span><span class="sxs-lookup"><span data-stu-id="12efc-188">May 3</span></span>          | <span data-ttu-id="12efc-189">-1</span><span class="sxs-lookup"><span data-stu-id="12efc-189">-1</span></span>       | <span data-ttu-id="12efc-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="12efc-190">-91.67</span></span>      | <span data-ttu-id="12efc-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="12efc-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="12efc-192">Wie Mengen und Beträge in jedem Periodenbereich berechnet werden</span><span class="sxs-lookup"><span data-stu-id="12efc-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="12efc-193">Mithilfe der in den vorherigen Abschnitten beschriebenen Beispieldaten können Sie einen Bericht **Alterung des Inventars** mit folgenden Einstellungen ausführen:</span><span class="sxs-lookup"><span data-stu-id="12efc-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="12efc-194">**Stand:** *9. Mai 2020*</span><span class="sxs-lookup"><span data-stu-id="12efc-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="12efc-195">**Seite:** *Aussicht*</span><span class="sxs-lookup"><span data-stu-id="12efc-195">**Site:** *View*</span></span>
- <span data-ttu-id="12efc-196">**Lagerort:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="12efc-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="12efc-197">**Artikelnummer:** *Gesamt*</span><span class="sxs-lookup"><span data-stu-id="12efc-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="12efc-198">**Alterungsdauer:** Legen Sie dieses Feld fest, um monatliche Bereiche zu generieren.</span><span class="sxs-lookup"><span data-stu-id="12efc-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="12efc-199">In diesem Fall ähnelt der Inhalt des generierten Berichts dem folgenden Beispiel.</span><span class="sxs-lookup"><span data-stu-id="12efc-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="12efc-200">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="12efc-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-201">Site</span><span class="sxs-lookup"><span data-stu-id="12efc-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-202">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-203">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="12efc-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-204">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="12efc-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-205">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="12efc-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-206">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="12efc-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="12efc-210">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-211">P1:Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="12efc-212">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-213">P2:Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="12efc-214">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-215">P3:Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="12efc-216">1000</span><span class="sxs-lookup"><span data-stu-id="12efc-216">1000</span></span></td>
    <td><span data-ttu-id="12efc-217">1</span><span class="sxs-lookup"><span data-stu-id="12efc-217">1</span></span></td>
    <td><span data-ttu-id="12efc-218">14</span><span class="sxs-lookup"><span data-stu-id="12efc-218">14</span></span></td>
    <td><span data-ttu-id="12efc-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="12efc-219">1,283.33</span></span></td>
    <td><span data-ttu-id="12efc-220">14</span><span class="sxs-lookup"><span data-stu-id="12efc-220">14</span></span></td>
    <td><span data-ttu-id="12efc-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="12efc-221">1,283.33</span></span></td>
    <td><span data-ttu-id="12efc-222">91.67</span><span class="sxs-lookup"><span data-stu-id="12efc-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-223">5.00</span><span class="sxs-lookup"><span data-stu-id="12efc-223">5.00</span></span></td>
    <td><span data-ttu-id="12efc-224">458.33</span><span class="sxs-lookup"><span data-stu-id="12efc-224">458.33</span></span></td>
    <td><span data-ttu-id="12efc-225">9.00</span><span class="sxs-lookup"><span data-stu-id="12efc-225">9.00</span></span></td>
    <td><span data-ttu-id="12efc-226">825.00</span><span class="sxs-lookup"><span data-stu-id="12efc-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="12efc-227">1000</span><span class="sxs-lookup"><span data-stu-id="12efc-227">1000</span></span></td>
    <td><span data-ttu-id="12efc-228">2</span><span class="sxs-lookup"><span data-stu-id="12efc-228">2</span></span></td>
    <td><span data-ttu-id="12efc-229">10</span><span class="sxs-lookup"><span data-stu-id="12efc-229">10</span></span></td>
    <td><span data-ttu-id="12efc-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-230">2,000.00</span></span></td>
    <td><span data-ttu-id="12efc-231">10</span><span class="sxs-lookup"><span data-stu-id="12efc-231">10</span></span></td>
    <td><span data-ttu-id="12efc-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-232">2,000.00</span></span></td>
    <td><span data-ttu-id="12efc-233">200.00</span><span class="sxs-lookup"><span data-stu-id="12efc-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-234">10.00</span><span class="sxs-lookup"><span data-stu-id="12efc-234">10.00</span></span></td>
    <td><span data-ttu-id="12efc-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="12efc-236"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="12efc-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="12efc-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="12efc-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="12efc-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="12efc-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="12efc-243">Beachten Sie die folgenden Details in diesem Beispielbericht:</span><span class="sxs-lookup"><span data-stu-id="12efc-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="12efc-244">Die Werte **Inventarwertmenge**, **Inventarwert** und **Durchschnittliche Stückkosten**, die im Bericht angezeigt werden, sind Werte für die Dimension des Finanzinventars (in diesem Fall **Seite**).</span><span class="sxs-lookup"><span data-stu-id="12efc-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="12efc-245">Für Standort 1 enthält der Bericht beispielsweise die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="12efc-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="12efc-246">Den Wert **Inventarwertmenge** ist *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="12efc-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="12efc-247">Der Wert **Inventarwertmenge** ist *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span><span class="sxs-lookup"><span data-stu-id="12efc-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="12efc-248">Der Wert **Durchschnittliche Stückkosten** ist *91,67*.</span><span class="sxs-lookup"><span data-stu-id="12efc-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="12efc-249">Der Wert **Lagerwert** und der Wert **Menge** in jedem Periodenbereich werden mithilfe vom Wert **Durchschnittliche Stückkosten** berechnet.</span><span class="sxs-lookup"><span data-stu-id="12efc-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="12efc-250">Der Bericht ermittelt die verfügbare Menge für jeden Periodenbereich, indem die insgesamt erhaltene Bestandsmenge für jeden Periodenbereich zusammengefasst wird.</span><span class="sxs-lookup"><span data-stu-id="12efc-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="12efc-251">Anschließend wird das Prinzip First In, First Out (FIFO)  angewendet, um die gesamte ausgegebene Menge abzuziehen, unabhängig vom verwendeten Bestandsmodell.</span><span class="sxs-lookup"><span data-stu-id="12efc-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="12efc-252">Wenn Sie denselben Bericht erneut ausführen, diesmal jedoch die Felder **Seite** und **Lagerort** auf *Anzeigen* festlegen, wird der neue Bericht dem folgenden Beispiel ähneln.</span><span class="sxs-lookup"><span data-stu-id="12efc-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="12efc-253">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="12efc-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-254">Site</span><span class="sxs-lookup"><span data-stu-id="12efc-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-255">Lagerort</span><span class="sxs-lookup"><span data-stu-id="12efc-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-256">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-257">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="12efc-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-258">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="12efc-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-259">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="12efc-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-260">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="12efc-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="12efc-264">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-265">P1: Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="12efc-266">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-267">P2: Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="12efc-268">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-269">P3: Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="12efc-270">1000</span><span class="sxs-lookup"><span data-stu-id="12efc-270">1000</span></span></td>
    <td><span data-ttu-id="12efc-271">1</span><span class="sxs-lookup"><span data-stu-id="12efc-271">1</span></span></td>
    <td><span data-ttu-id="12efc-272">11</span><span class="sxs-lookup"><span data-stu-id="12efc-272">11</span></span></td>
    <td><span data-ttu-id="12efc-273">10</span><span class="sxs-lookup"><span data-stu-id="12efc-273">10</span></span></td>
    <td><span data-ttu-id="12efc-274">916.67</span><span class="sxs-lookup"><span data-stu-id="12efc-274">916.67</span></span></td>
    <td><span data-ttu-id="12efc-275">14</span><span class="sxs-lookup"><span data-stu-id="12efc-275">14</span></span></td>
    <td><span data-ttu-id="12efc-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="12efc-276">1,283.33</span></span></td>
    <td><span data-ttu-id="12efc-277">91.67</span><span class="sxs-lookup"><span data-stu-id="12efc-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-278">5.00</span><span class="sxs-lookup"><span data-stu-id="12efc-278">5.00</span></span></td>
    <td><span data-ttu-id="12efc-279">458.33</span><span class="sxs-lookup"><span data-stu-id="12efc-279">458.33</span></span></td>
    <td><span data-ttu-id="12efc-280">5.00</span><span class="sxs-lookup"><span data-stu-id="12efc-280">5.00</span></span></td>
    <td><span data-ttu-id="12efc-281">458.33</span><span class="sxs-lookup"><span data-stu-id="12efc-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="12efc-282">1000</span><span class="sxs-lookup"><span data-stu-id="12efc-282">1000</span></span></td>
    <td><span data-ttu-id="12efc-283">1</span><span class="sxs-lookup"><span data-stu-id="12efc-283">1</span></span></td>
    <td><span data-ttu-id="12efc-284">12</span><span class="sxs-lookup"><span data-stu-id="12efc-284">12</span></span></td>
    <td><span data-ttu-id="12efc-285">4</span><span class="sxs-lookup"><span data-stu-id="12efc-285">4</span></span></td>
    <td><span data-ttu-id="12efc-286">366.67</span><span class="sxs-lookup"><span data-stu-id="12efc-286">366.67</span></span></td>
    <td><span data-ttu-id="12efc-287">14</span><span class="sxs-lookup"><span data-stu-id="12efc-287">14</span></span></td>
    <td><span data-ttu-id="12efc-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="12efc-288">1,283.33</span></span></td>
    <td><span data-ttu-id="12efc-289">91.67</span><span class="sxs-lookup"><span data-stu-id="12efc-289">91.67</span></span></td>
    <td><span data-ttu-id="12efc-290">4.00</span><span class="sxs-lookup"><span data-stu-id="12efc-290">4.00</span></span></td>
    <td><span data-ttu-id="12efc-291">366.67</span><span class="sxs-lookup"><span data-stu-id="12efc-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="12efc-292">1000</span><span class="sxs-lookup"><span data-stu-id="12efc-292">1000</span></span></td>
    <td><span data-ttu-id="12efc-293">2</span><span class="sxs-lookup"><span data-stu-id="12efc-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="12efc-294">10</span><span class="sxs-lookup"><span data-stu-id="12efc-294">10</span></span></td>
    <td><span data-ttu-id="12efc-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-295">2,000.00</span></span></td>
    <td><span data-ttu-id="12efc-296">10</span><span class="sxs-lookup"><span data-stu-id="12efc-296">10</span></span></td>
    <td><span data-ttu-id="12efc-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-297">2,000.00</span></span></td>
    <td><span data-ttu-id="12efc-298">200.00</span><span class="sxs-lookup"><span data-stu-id="12efc-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-299">10.00</span><span class="sxs-lookup"><span data-stu-id="12efc-299">10.00</span></span></td>
    <td><span data-ttu-id="12efc-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="12efc-301"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="12efc-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="12efc-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="12efc-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="12efc-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="12efc-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="12efc-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="12efc-310">Diesmal ist Site 1 in zwei Zeilen unterteilt, eine für Lager 11 und eine für Lager 12.</span><span class="sxs-lookup"><span data-stu-id="12efc-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="12efc-311">Aber die Werte **Inventarwertmenge**, **Inventarwert** und **Durchschnittliche Stückkosten**, die im Bericht angezeigt werden, sind gleich weil der **Lagerort** keine Finanzdimension ist.</span><span class="sxs-lookup"><span data-stu-id="12efc-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="12efc-312">Beachten Sie außerdem, dass die Mengenverteilung von Standort 1 unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="12efc-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="12efc-313">In dem ersten Bericht, den Sie ausgeführt haben, hat das System den Transportauftrag ignoriert, der an derselben Site aufgetreten ist, und die Menge der Verkaufsrechnung vom Zeitraumbereich **31.03.2020 – 01.03.2020** in Site 1 abgezogen.</span><span class="sxs-lookup"><span data-stu-id="12efc-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="12efc-314">Im neuen Bericht zieht das System jedoch die Menge der Verkaufsrechnung vom Zeitraumbereich **08.05.2020 – 01.05.2020** im Lager 12 ab.</span><span class="sxs-lookup"><span data-stu-id="12efc-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="12efc-315">Effekte der Bestandschließung</span><span class="sxs-lookup"><span data-stu-id="12efc-315">Effects of inventory closing</span></span>

<span data-ttu-id="12efc-316">Wenn Sie das Inventar für Mai schließen und dann den vorherigen Bericht erneut ausführen, aber das Feld **Stand Datum** auf *31. Mai 2020* festlegen, werden Sie folgende Ergebnisse feststellen:</span><span class="sxs-lookup"><span data-stu-id="12efc-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="12efc-317">Der **Bestandwert** und der Wert **Durchschnittliche Stückkosten** werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="12efc-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="12efc-318">Der **verfügbare Wert** und der Wert **Betrag** in jedem Periodenbereich werden entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="12efc-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="12efc-319">Der neue Bericht sieht ähnlich aus wie das folgende Beispiel.</span><span class="sxs-lookup"><span data-stu-id="12efc-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="12efc-320">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="12efc-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-321">Site</span><span class="sxs-lookup"><span data-stu-id="12efc-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-322">Lagerort</span><span class="sxs-lookup"><span data-stu-id="12efc-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-323">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-324">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="12efc-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-325">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="12efc-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-326">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="12efc-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="12efc-327">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="12efc-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="12efc-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="12efc-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="12efc-331">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-332">P1: Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="12efc-333">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-334">P2: Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="12efc-335">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="12efc-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="12efc-336">P3: Betrag</span><span class="sxs-lookup"><span data-stu-id="12efc-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="12efc-337">1000</span><span class="sxs-lookup"><span data-stu-id="12efc-337">1000</span></span></td>
    <td><span data-ttu-id="12efc-338">1</span><span class="sxs-lookup"><span data-stu-id="12efc-338">1</span></span></td>
    <td><span data-ttu-id="12efc-339">11</span><span class="sxs-lookup"><span data-stu-id="12efc-339">11</span></span></td>
    <td><span data-ttu-id="12efc-340">10</span><span class="sxs-lookup"><span data-stu-id="12efc-340">10</span></span></td>
    <td><span data-ttu-id="12efc-341">910.70</span><span class="sxs-lookup"><span data-stu-id="12efc-341">910.70</span></span></td>
    <td><span data-ttu-id="12efc-342">14</span><span class="sxs-lookup"><span data-stu-id="12efc-342">14</span></span></td>
    <td><span data-ttu-id="12efc-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="12efc-343">1,275.00</span></span></td>
    <td><span data-ttu-id="12efc-344">91.07</span><span class="sxs-lookup"><span data-stu-id="12efc-344">91.07</span></span></td>
    <td><span data-ttu-id="12efc-345">0,00</span><span class="sxs-lookup"><span data-stu-id="12efc-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="12efc-346">5.00</span><span class="sxs-lookup"><span data-stu-id="12efc-346">5.00</span></span></td>
    <td><span data-ttu-id="12efc-347">455.36</span><span class="sxs-lookup"><span data-stu-id="12efc-347">455.36</span></span></td>
    <td><span data-ttu-id="12efc-348">5.00</span><span class="sxs-lookup"><span data-stu-id="12efc-348">5.00</span></span></td>
    <td><span data-ttu-id="12efc-349">455.36</span><span class="sxs-lookup"><span data-stu-id="12efc-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="12efc-350">1000</span><span class="sxs-lookup"><span data-stu-id="12efc-350">1000</span></span></td>
    <td><span data-ttu-id="12efc-351">1</span><span class="sxs-lookup"><span data-stu-id="12efc-351">1</span></span></td>
    <td><span data-ttu-id="12efc-352">12</span><span class="sxs-lookup"><span data-stu-id="12efc-352">12</span></span></td>
    <td><span data-ttu-id="12efc-353">4</span><span class="sxs-lookup"><span data-stu-id="12efc-353">4</span></span></td>
    <td><span data-ttu-id="12efc-354">364.29</span><span class="sxs-lookup"><span data-stu-id="12efc-354">364.29</span></span></td>
    <td><span data-ttu-id="12efc-355">14</span><span class="sxs-lookup"><span data-stu-id="12efc-355">14</span></span></td>
    <td><span data-ttu-id="12efc-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="12efc-356">1,275.00</span></span></td>
    <td><span data-ttu-id="12efc-357">91.07</span><span class="sxs-lookup"><span data-stu-id="12efc-357">91.07</span></span></td>
    <td><span data-ttu-id="12efc-358">4.00</span><span class="sxs-lookup"><span data-stu-id="12efc-358">4.00</span></span></td>
    <td><span data-ttu-id="12efc-359">364.29</span><span class="sxs-lookup"><span data-stu-id="12efc-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="12efc-360">1000</span><span class="sxs-lookup"><span data-stu-id="12efc-360">1000</span></span></td>
    <td><span data-ttu-id="12efc-361">2</span><span class="sxs-lookup"><span data-stu-id="12efc-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="12efc-362">10</span><span class="sxs-lookup"><span data-stu-id="12efc-362">10</span></span></td>
    <td><span data-ttu-id="12efc-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-363">2,000.00</span></span></td>
    <td><span data-ttu-id="12efc-364">10</span><span class="sxs-lookup"><span data-stu-id="12efc-364">10</span></span></td>
    <td><span data-ttu-id="12efc-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-365">2,000.00</span></span></td>
    <td><span data-ttu-id="12efc-366">200.00</span><span class="sxs-lookup"><span data-stu-id="12efc-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-367">10.00</span><span class="sxs-lookup"><span data-stu-id="12efc-367">10.00</span></span></td>
    <td><span data-ttu-id="12efc-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="12efc-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="12efc-369"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="12efc-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="12efc-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="12efc-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="12efc-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="12efc-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="12efc-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="12efc-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="12efc-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
