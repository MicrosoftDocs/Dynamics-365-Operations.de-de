---
title: Beispiele und Logik für Inventarfäligkeitsberichte
description: In diesem Thema werden einige Beispiele vorgestellt, die zeigen, wie die Ergebnisse eines Inventaralterungsberichts interpretiert werden.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d9c70a7931c009cd53fbd28a3f4c768d04964a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214417"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="69980-103">Beispiele und Logik für Inventarfäligkeitsberichte</span><span class="sxs-lookup"><span data-stu-id="69980-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69980-104">In diesem Thema werden einige Beispiele vorgestellt, die zeigen, wie die Ergebnisse eines **Inventarfälligkeitsberichts** interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="69980-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="69980-105">In diesem Bericht werden die verfügbaren Mengen- und Bestandswerte für einen ausgewählten Artikel oder eine Artikelgruppe in mehrere Periodenbereiche unterteilt.</span><span class="sxs-lookup"><span data-stu-id="69980-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="69980-106">Dieses Thema zeigt auch die interne Logik des Berichts.</span><span class="sxs-lookup"><span data-stu-id="69980-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="69980-107">Die Beispiele in diesem Thema zeigen Ergebnisse, die auf einem Standard **Fälligkeit des Inventar** Berichts dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="69980-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="69980-108">Im Allgemeinen empfehlen wir jedoch die Verwendung der Version [Speicherung von Inventarfälligkeitsberichten](inventory-aging-report-storage.md) dieses Berichts, insbesondere wenn Sie viele Artikel und Lager haben, die verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="69980-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="69980-109">Durch die Speicherung von Inventarfälligkeitsberichten wird jeder von Ihnen erstellte Bericht gespeichert, die Ergebnisse als interaktive Seite und als Diagramm angezeigt und Sie können jeden gespeicherten Bericht exportieren.</span><span class="sxs-lookup"><span data-stu-id="69980-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="69980-110">Beispieldaten, die in diesen Beispielen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="69980-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="69980-111">Die Beispiele in diesem Thema basieren auf den in diesem Abschnitt beschriebenen Beispieltransaktionsdaten für das Inventar.</span><span class="sxs-lookup"><span data-stu-id="69980-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="69980-112">Lagerdimensionsgruppe einrichten</span><span class="sxs-lookup"><span data-stu-id="69980-112">Storage dimension setup</span></span>

<span data-ttu-id="69980-113">Das Beispielsystem enthält die folgenden Einstellungen für die Speicherabmessungen.</span><span class="sxs-lookup"><span data-stu-id="69980-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="69980-114">Name</span><span class="sxs-lookup"><span data-stu-id="69980-114">Name</span></span>      | <span data-ttu-id="69980-115">Aktiv</span><span class="sxs-lookup"><span data-stu-id="69980-115">Active</span></span> | <span data-ttu-id="69980-116">Physischer Bestand</span><span class="sxs-lookup"><span data-stu-id="69980-116">Physical inventory</span></span> | <span data-ttu-id="69980-117">Wertmäßiger Bestand</span><span class="sxs-lookup"><span data-stu-id="69980-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="69980-118">Site</span><span class="sxs-lookup"><span data-stu-id="69980-118">Site</span></span>      | <span data-ttu-id="69980-119">Ja</span><span class="sxs-lookup"><span data-stu-id="69980-119">Yes</span></span>    | <span data-ttu-id="69980-120">Ja</span><span class="sxs-lookup"><span data-stu-id="69980-120">Yes</span></span>                | <span data-ttu-id="69980-121">Ja</span><span class="sxs-lookup"><span data-stu-id="69980-121">Yes</span></span>                 |
| <span data-ttu-id="69980-122">Lagerort</span><span class="sxs-lookup"><span data-stu-id="69980-122">Warehouse</span></span> | <span data-ttu-id="69980-123">Ja</span><span class="sxs-lookup"><span data-stu-id="69980-123">Yes</span></span>    | <span data-ttu-id="69980-124">Ja</span><span class="sxs-lookup"><span data-stu-id="69980-124">Yes</span></span>                | <span data-ttu-id="69980-125">Nr.</span><span class="sxs-lookup"><span data-stu-id="69980-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="69980-126">Lagermodell</span><span class="sxs-lookup"><span data-stu-id="69980-126">Inventory model</span></span>

<span data-ttu-id="69980-127">Für das Beispielsystem lautet das Bestandsmodell für die freigegebenen Produkte *FIFO*, und die **Selbstkostenpreis** Einstellung für das Bestandsmodell ist auf *Physischen Wert einschließen* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="69980-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="69980-128">Lagerbuchungen</span><span class="sxs-lookup"><span data-stu-id="69980-128">Inventory transactions</span></span>

<span data-ttu-id="69980-129">Das Beispielsystem enthält die folgenden Inventurtransaktionen für ein freigegebenes Produkt mit der Artikelnummer *1000*.</span><span class="sxs-lookup"><span data-stu-id="69980-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="69980-130">Referenz</span><span class="sxs-lookup"><span data-stu-id="69980-130">Reference</span></span>      | <span data-ttu-id="69980-131">Site</span><span class="sxs-lookup"><span data-stu-id="69980-131">Site</span></span> | <span data-ttu-id="69980-132">Lagerort</span><span class="sxs-lookup"><span data-stu-id="69980-132">Warehouse</span></span> | <span data-ttu-id="69980-133">Zugang</span><span class="sxs-lookup"><span data-stu-id="69980-133">Receipt</span></span>   | <span data-ttu-id="69980-134">Abgang</span><span class="sxs-lookup"><span data-stu-id="69980-134">Issue</span></span> | <span data-ttu-id="69980-135">Physisches Datum</span><span class="sxs-lookup"><span data-stu-id="69980-135">Physical date</span></span> | <span data-ttu-id="69980-136">Finanzdatum</span><span class="sxs-lookup"><span data-stu-id="69980-136">Financial date</span></span> | <span data-ttu-id="69980-137">Leistung</span><span class="sxs-lookup"><span data-stu-id="69980-137">Quantity</span></span> | <span data-ttu-id="69980-138">Betrag KORE</span><span class="sxs-lookup"><span data-stu-id="69980-138">Cost amount</span></span> | <span data-ttu-id="69980-139">Phys. Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="69980-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="69980-140">Bestellung</span><span class="sxs-lookup"><span data-stu-id="69980-140">Purchase order</span></span> | <span data-ttu-id="69980-141">1</span><span class="sxs-lookup"><span data-stu-id="69980-141">1</span></span>    | <span data-ttu-id="69980-142">11</span><span class="sxs-lookup"><span data-stu-id="69980-142">11</span></span>        | <span data-ttu-id="69980-143">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="69980-143">Purchased</span></span> |       | <span data-ttu-id="69980-144">15. März</span><span class="sxs-lookup"><span data-stu-id="69980-144">March 15</span></span>      | <span data-ttu-id="69980-145">15. März</span><span class="sxs-lookup"><span data-stu-id="69980-145">March 15</span></span>       | <span data-ttu-id="69980-146">10</span><span class="sxs-lookup"><span data-stu-id="69980-146">10</span></span>       | <span data-ttu-id="69980-147">1.000</span><span class="sxs-lookup"><span data-stu-id="69980-147">1,000</span></span>       | <span data-ttu-id="69980-148">1.000</span><span class="sxs-lookup"><span data-stu-id="69980-148">1,000</span></span>                |
| <span data-ttu-id="69980-149">Bestellung</span><span class="sxs-lookup"><span data-stu-id="69980-149">Purchase order</span></span> | <span data-ttu-id="69980-150">2</span><span class="sxs-lookup"><span data-stu-id="69980-150">2</span></span>    | <span data-ttu-id="69980-151">21</span><span class="sxs-lookup"><span data-stu-id="69980-151">21</span></span>        | <span data-ttu-id="69980-152">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="69980-152">Purchased</span></span> |       | <span data-ttu-id="69980-153">15. März</span><span class="sxs-lookup"><span data-stu-id="69980-153">March 15</span></span>      | <span data-ttu-id="69980-154">15. März</span><span class="sxs-lookup"><span data-stu-id="69980-154">March 15</span></span>       | <span data-ttu-id="69980-155">10</span><span class="sxs-lookup"><span data-stu-id="69980-155">10</span></span>       | <span data-ttu-id="69980-156">2,000</span><span class="sxs-lookup"><span data-stu-id="69980-156">2,000</span></span>       | <span data-ttu-id="69980-157">2,000</span><span class="sxs-lookup"><span data-stu-id="69980-157">2,000</span></span>                |
| <span data-ttu-id="69980-158">Bestellung</span><span class="sxs-lookup"><span data-stu-id="69980-158">Purchase order</span></span> | <span data-ttu-id="69980-159">1</span><span class="sxs-lookup"><span data-stu-id="69980-159">1</span></span>    | <span data-ttu-id="69980-160">11</span><span class="sxs-lookup"><span data-stu-id="69980-160">11</span></span>        | <span data-ttu-id="69980-161">Eingegangen</span><span class="sxs-lookup"><span data-stu-id="69980-161">Received</span></span>  |       | <span data-ttu-id="69980-162">April 15</span><span class="sxs-lookup"><span data-stu-id="69980-162">April 15</span></span>      |                | <span data-ttu-id="69980-163">5</span><span class="sxs-lookup"><span data-stu-id="69980-163">5</span></span>        |             | <span data-ttu-id="69980-164">375</span><span class="sxs-lookup"><span data-stu-id="69980-164">375</span></span>                  |
| <span data-ttu-id="69980-165">Umlagerungsauftrag</span><span class="sxs-lookup"><span data-stu-id="69980-165">Transfer order</span></span> | <span data-ttu-id="69980-166">1</span><span class="sxs-lookup"><span data-stu-id="69980-166">1</span></span>    | <span data-ttu-id="69980-167">11</span><span class="sxs-lookup"><span data-stu-id="69980-167">11</span></span>        |           | <span data-ttu-id="69980-168">Verkauft</span><span class="sxs-lookup"><span data-stu-id="69980-168">Sold</span></span>  | <span data-ttu-id="69980-169">Mai 2</span><span class="sxs-lookup"><span data-stu-id="69980-169">May 2</span></span>         | <span data-ttu-id="69980-170">Mai 2</span><span class="sxs-lookup"><span data-stu-id="69980-170">May 2</span></span>          | <span data-ttu-id="69980-171">-5</span><span class="sxs-lookup"><span data-stu-id="69980-171">-5</span></span>       | <span data-ttu-id="69980-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="69980-172">-458.33</span></span>     | <span data-ttu-id="69980-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="69980-173">-458.33</span></span>              |
| <span data-ttu-id="69980-174">Umlagerungsauftrag</span><span class="sxs-lookup"><span data-stu-id="69980-174">Transfer order</span></span> | <span data-ttu-id="69980-175">1</span><span class="sxs-lookup"><span data-stu-id="69980-175">1</span></span>    | <span data-ttu-id="69980-176">12</span><span class="sxs-lookup"><span data-stu-id="69980-176">12</span></span>        | <span data-ttu-id="69980-177">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="69980-177">Purchased</span></span> |       | <span data-ttu-id="69980-178">Mai 2</span><span class="sxs-lookup"><span data-stu-id="69980-178">May 2</span></span>         | <span data-ttu-id="69980-179">Mai 2</span><span class="sxs-lookup"><span data-stu-id="69980-179">May 2</span></span>          | <span data-ttu-id="69980-180">5</span><span class="sxs-lookup"><span data-stu-id="69980-180">5</span></span>        | <span data-ttu-id="69980-181">458.33</span><span class="sxs-lookup"><span data-stu-id="69980-181">458.33</span></span>      | <span data-ttu-id="69980-182">458.33</span><span class="sxs-lookup"><span data-stu-id="69980-182">458.33</span></span>               |
| <span data-ttu-id="69980-183">Auftrag</span><span class="sxs-lookup"><span data-stu-id="69980-183">Sales order</span></span>    | <span data-ttu-id="69980-184">1</span><span class="sxs-lookup"><span data-stu-id="69980-184">1</span></span>    | <span data-ttu-id="69980-185">12</span><span class="sxs-lookup"><span data-stu-id="69980-185">12</span></span>        |           | <span data-ttu-id="69980-186">Verkauft</span><span class="sxs-lookup"><span data-stu-id="69980-186">Sold</span></span>  | <span data-ttu-id="69980-187">Mai 3</span><span class="sxs-lookup"><span data-stu-id="69980-187">May 3</span></span>         | <span data-ttu-id="69980-188">Mai 3</span><span class="sxs-lookup"><span data-stu-id="69980-188">May 3</span></span>          | <span data-ttu-id="69980-189">-1</span><span class="sxs-lookup"><span data-stu-id="69980-189">-1</span></span>       | <span data-ttu-id="69980-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="69980-190">-91.67</span></span>      | <span data-ttu-id="69980-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="69980-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="69980-192">Wie Mengen und Beträge in jedem Periodenbereich berechnet werden</span><span class="sxs-lookup"><span data-stu-id="69980-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="69980-193">Mithilfe der in den vorherigen Abschnitten beschriebenen Beispieldaten können Sie einen Bericht **Alterung des Inventars** mit folgenden Einstellungen ausführen:</span><span class="sxs-lookup"><span data-stu-id="69980-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="69980-194">**Stand:** *9. Mai 2020*</span><span class="sxs-lookup"><span data-stu-id="69980-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="69980-195">**Seite:** *Aussicht*</span><span class="sxs-lookup"><span data-stu-id="69980-195">**Site:** *View*</span></span>
- <span data-ttu-id="69980-196">**Lagerort:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="69980-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="69980-197">**Artikelnummer:** *Gesamt*</span><span class="sxs-lookup"><span data-stu-id="69980-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="69980-198">**Alterungsdauer:** Legen Sie dieses Feld fest, um monatliche Bereiche zu generieren.</span><span class="sxs-lookup"><span data-stu-id="69980-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="69980-199">In diesem Fall ähnelt der Inhalt des generierten Berichts dem folgenden Beispiel.</span><span class="sxs-lookup"><span data-stu-id="69980-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="69980-200">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="69980-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-201">Site</span><span class="sxs-lookup"><span data-stu-id="69980-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-202">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="69980-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-203">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="69980-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-204">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="69980-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-205">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="69980-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-206">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="69980-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="69980-210">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="69980-211">P1:Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="69980-212">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="69980-213">P2:Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="69980-214">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="69980-215">P3:Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="69980-216">1000</span><span class="sxs-lookup"><span data-stu-id="69980-216">1000</span></span></td>
    <td><span data-ttu-id="69980-217">1</span><span class="sxs-lookup"><span data-stu-id="69980-217">1</span></span></td>
    <td><span data-ttu-id="69980-218">14</span><span class="sxs-lookup"><span data-stu-id="69980-218">14</span></span></td>
    <td><span data-ttu-id="69980-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="69980-219">1,283.33</span></span></td>
    <td><span data-ttu-id="69980-220">14</span><span class="sxs-lookup"><span data-stu-id="69980-220">14</span></span></td>
    <td><span data-ttu-id="69980-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="69980-221">1,283.33</span></span></td>
    <td><span data-ttu-id="69980-222">91.67</span><span class="sxs-lookup"><span data-stu-id="69980-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-223">5.00</span><span class="sxs-lookup"><span data-stu-id="69980-223">5.00</span></span></td>
    <td><span data-ttu-id="69980-224">458.33</span><span class="sxs-lookup"><span data-stu-id="69980-224">458.33</span></span></td>
    <td><span data-ttu-id="69980-225">9.00</span><span class="sxs-lookup"><span data-stu-id="69980-225">9.00</span></span></td>
    <td><span data-ttu-id="69980-226">825.00</span><span class="sxs-lookup"><span data-stu-id="69980-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="69980-227">1000</span><span class="sxs-lookup"><span data-stu-id="69980-227">1000</span></span></td>
    <td><span data-ttu-id="69980-228">2</span><span class="sxs-lookup"><span data-stu-id="69980-228">2</span></span></td>
    <td><span data-ttu-id="69980-229">10</span><span class="sxs-lookup"><span data-stu-id="69980-229">10</span></span></td>
    <td><span data-ttu-id="69980-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-230">2,000.00</span></span></td>
    <td><span data-ttu-id="69980-231">10</span><span class="sxs-lookup"><span data-stu-id="69980-231">10</span></span></td>
    <td><span data-ttu-id="69980-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-232">2,000.00</span></span></td>
    <td><span data-ttu-id="69980-233">200.00</span><span class="sxs-lookup"><span data-stu-id="69980-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-234">10.00</span><span class="sxs-lookup"><span data-stu-id="69980-234">10.00</span></span></td>
    <td><span data-ttu-id="69980-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="69980-236"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="69980-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="69980-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="69980-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="69980-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="69980-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="69980-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="69980-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="69980-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="69980-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="69980-243">Beachten Sie die folgenden Details in diesem Beispielbericht:</span><span class="sxs-lookup"><span data-stu-id="69980-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="69980-244">Die Werte **Inventarwertmenge**, **Inventarwert** und **Durchschnittliche Stückkosten**, die im Bericht angezeigt werden, sind Werte für die Dimension des Finanzinventars (in diesem Fall **Seite**).</span><span class="sxs-lookup"><span data-stu-id="69980-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="69980-245">Für Standort 1 enthält der Bericht beispielsweise die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="69980-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="69980-246">Den Wert **Inventarwertmenge** ist *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="69980-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="69980-247">Der Wert **Inventarwertmenge** ist *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span><span class="sxs-lookup"><span data-stu-id="69980-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="69980-248">Der Wert **Durchschnittliche Stückkosten** ist *91,67*.</span><span class="sxs-lookup"><span data-stu-id="69980-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="69980-249">Der Wert **Lagerwert** und der Wert **Menge** in jedem Periodenbereich werden mithilfe vom Wert **Durchschnittliche Stückkosten** berechnet.</span><span class="sxs-lookup"><span data-stu-id="69980-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="69980-250">Der Bericht ermittelt die verfügbare Menge für jeden Periodenbereich, indem die insgesamt erhaltene Bestandsmenge für jeden Periodenbereich zusammengefasst wird.</span><span class="sxs-lookup"><span data-stu-id="69980-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="69980-251">Anschließend wird das Prinzip First In, First Out (FIFO)  angewendet, um die gesamte ausgegebene Menge abzuziehen, unabhängig vom verwendeten Bestandsmodell.</span><span class="sxs-lookup"><span data-stu-id="69980-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="69980-252">Wenn Sie denselben Bericht erneut ausführen, diesmal jedoch die Felder **Seite** und **Lagerort** auf *Anzeigen* festlegen, wird der neue Bericht dem folgenden Beispiel ähneln.</span><span class="sxs-lookup"><span data-stu-id="69980-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="69980-253">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="69980-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-254">Site</span><span class="sxs-lookup"><span data-stu-id="69980-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-255">Lagerort</span><span class="sxs-lookup"><span data-stu-id="69980-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-256">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="69980-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-257">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="69980-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-258">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="69980-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-259">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="69980-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-260">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="69980-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="69980-264">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="69980-265">P1: Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="69980-266">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="69980-267">P2: Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="69980-268">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="69980-269">P3: Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="69980-270">1000</span><span class="sxs-lookup"><span data-stu-id="69980-270">1000</span></span></td>
    <td><span data-ttu-id="69980-271">1</span><span class="sxs-lookup"><span data-stu-id="69980-271">1</span></span></td>
    <td><span data-ttu-id="69980-272">11</span><span class="sxs-lookup"><span data-stu-id="69980-272">11</span></span></td>
    <td><span data-ttu-id="69980-273">10</span><span class="sxs-lookup"><span data-stu-id="69980-273">10</span></span></td>
    <td><span data-ttu-id="69980-274">916.67</span><span class="sxs-lookup"><span data-stu-id="69980-274">916.67</span></span></td>
    <td><span data-ttu-id="69980-275">14</span><span class="sxs-lookup"><span data-stu-id="69980-275">14</span></span></td>
    <td><span data-ttu-id="69980-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="69980-276">1,283.33</span></span></td>
    <td><span data-ttu-id="69980-277">91.67</span><span class="sxs-lookup"><span data-stu-id="69980-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-278">5.00</span><span class="sxs-lookup"><span data-stu-id="69980-278">5.00</span></span></td>
    <td><span data-ttu-id="69980-279">458.33</span><span class="sxs-lookup"><span data-stu-id="69980-279">458.33</span></span></td>
    <td><span data-ttu-id="69980-280">5.00</span><span class="sxs-lookup"><span data-stu-id="69980-280">5.00</span></span></td>
    <td><span data-ttu-id="69980-281">458.33</span><span class="sxs-lookup"><span data-stu-id="69980-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="69980-282">1000</span><span class="sxs-lookup"><span data-stu-id="69980-282">1000</span></span></td>
    <td><span data-ttu-id="69980-283">1</span><span class="sxs-lookup"><span data-stu-id="69980-283">1</span></span></td>
    <td><span data-ttu-id="69980-284">12</span><span class="sxs-lookup"><span data-stu-id="69980-284">12</span></span></td>
    <td><span data-ttu-id="69980-285">4</span><span class="sxs-lookup"><span data-stu-id="69980-285">4</span></span></td>
    <td><span data-ttu-id="69980-286">366.67</span><span class="sxs-lookup"><span data-stu-id="69980-286">366.67</span></span></td>
    <td><span data-ttu-id="69980-287">14</span><span class="sxs-lookup"><span data-stu-id="69980-287">14</span></span></td>
    <td><span data-ttu-id="69980-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="69980-288">1,283.33</span></span></td>
    <td><span data-ttu-id="69980-289">91.67</span><span class="sxs-lookup"><span data-stu-id="69980-289">91.67</span></span></td>
    <td><span data-ttu-id="69980-290">4.00</span><span class="sxs-lookup"><span data-stu-id="69980-290">4.00</span></span></td>
    <td><span data-ttu-id="69980-291">366.67</span><span class="sxs-lookup"><span data-stu-id="69980-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="69980-292">1000</span><span class="sxs-lookup"><span data-stu-id="69980-292">1000</span></span></td>
    <td><span data-ttu-id="69980-293">2</span><span class="sxs-lookup"><span data-stu-id="69980-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="69980-294">10</span><span class="sxs-lookup"><span data-stu-id="69980-294">10</span></span></td>
    <td><span data-ttu-id="69980-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-295">2,000.00</span></span></td>
    <td><span data-ttu-id="69980-296">10</span><span class="sxs-lookup"><span data-stu-id="69980-296">10</span></span></td>
    <td><span data-ttu-id="69980-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-297">2,000.00</span></span></td>
    <td><span data-ttu-id="69980-298">200.00</span><span class="sxs-lookup"><span data-stu-id="69980-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-299">10.00</span><span class="sxs-lookup"><span data-stu-id="69980-299">10.00</span></span></td>
    <td><span data-ttu-id="69980-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="69980-301"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="69980-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="69980-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="69980-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="69980-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="69980-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="69980-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="69980-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="69980-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="69980-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="69980-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="69980-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="69980-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="69980-310">Diesmal ist Site 1 in zwei Zeilen unterteilt, eine für Lager 11 und eine für Lager 12.</span><span class="sxs-lookup"><span data-stu-id="69980-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="69980-311">Aber die Werte **Inventarwertmenge**, **Inventarwert** und **Durchschnittliche Stückkosten**, die im Bericht angezeigt werden, sind gleich weil der **Lagerort** keine Finanzdimension ist.</span><span class="sxs-lookup"><span data-stu-id="69980-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="69980-312">Beachten Sie außerdem, dass die Mengenverteilung von Standort 1 unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="69980-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="69980-313">In dem ersten Bericht, den Sie ausgeführt haben, hat das System den Transportauftrag ignoriert, der an derselben Site aufgetreten ist, und die Menge der Verkaufsrechnung vom Zeitraumbereich **31.03.2020 – 01.03.2020** in Site 1 abgezogen.</span><span class="sxs-lookup"><span data-stu-id="69980-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="69980-314">Im neuen Bericht zieht das System jedoch die Menge der Verkaufsrechnung vom Zeitraumbereich **08.05.2020 – 01.05.2020** im Lager 12 ab.</span><span class="sxs-lookup"><span data-stu-id="69980-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="69980-315">Effekte der Bestandschließung</span><span class="sxs-lookup"><span data-stu-id="69980-315">Effects of inventory closing</span></span>

<span data-ttu-id="69980-316">Wenn Sie das Inventar für Mai schließen und dann den vorherigen Bericht erneut ausführen, aber das Feld **Stand Datum** auf *31. Mai 2020* festlegen, werden Sie folgende Ergebnisse feststellen:</span><span class="sxs-lookup"><span data-stu-id="69980-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="69980-317">Der **Bestandwert** und der Wert **Durchschnittliche Stückkosten** werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="69980-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="69980-318">Der **verfügbare Wert** und der Wert **Betrag** in jedem Periodenbereich werden entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="69980-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="69980-319">Der neue Bericht sieht ähnlich aus wie das folgende Beispiel.</span><span class="sxs-lookup"><span data-stu-id="69980-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="69980-320">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="69980-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-321">Site</span><span class="sxs-lookup"><span data-stu-id="69980-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-322">Lagerort</span><span class="sxs-lookup"><span data-stu-id="69980-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-323">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="69980-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-324">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="69980-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-325">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="69980-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-326">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="69980-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="69980-327">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="69980-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="69980-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="69980-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="69980-331">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="69980-332">P1: Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="69980-333">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="69980-334">P2: Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="69980-335">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="69980-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="69980-336">P3: Betrag</span><span class="sxs-lookup"><span data-stu-id="69980-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="69980-337">1000</span><span class="sxs-lookup"><span data-stu-id="69980-337">1000</span></span></td>
    <td><span data-ttu-id="69980-338">1</span><span class="sxs-lookup"><span data-stu-id="69980-338">1</span></span></td>
    <td><span data-ttu-id="69980-339">11</span><span class="sxs-lookup"><span data-stu-id="69980-339">11</span></span></td>
    <td><span data-ttu-id="69980-340">10</span><span class="sxs-lookup"><span data-stu-id="69980-340">10</span></span></td>
    <td><span data-ttu-id="69980-341">910.70</span><span class="sxs-lookup"><span data-stu-id="69980-341">910.70</span></span></td>
    <td><span data-ttu-id="69980-342">14</span><span class="sxs-lookup"><span data-stu-id="69980-342">14</span></span></td>
    <td><span data-ttu-id="69980-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="69980-343">1,275.00</span></span></td>
    <td><span data-ttu-id="69980-344">91.07</span><span class="sxs-lookup"><span data-stu-id="69980-344">91.07</span></span></td>
    <td><span data-ttu-id="69980-345">0,00</span><span class="sxs-lookup"><span data-stu-id="69980-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="69980-346">5.00</span><span class="sxs-lookup"><span data-stu-id="69980-346">5.00</span></span></td>
    <td><span data-ttu-id="69980-347">455.36</span><span class="sxs-lookup"><span data-stu-id="69980-347">455.36</span></span></td>
    <td><span data-ttu-id="69980-348">5.00</span><span class="sxs-lookup"><span data-stu-id="69980-348">5.00</span></span></td>
    <td><span data-ttu-id="69980-349">455.36</span><span class="sxs-lookup"><span data-stu-id="69980-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="69980-350">1000</span><span class="sxs-lookup"><span data-stu-id="69980-350">1000</span></span></td>
    <td><span data-ttu-id="69980-351">1</span><span class="sxs-lookup"><span data-stu-id="69980-351">1</span></span></td>
    <td><span data-ttu-id="69980-352">12</span><span class="sxs-lookup"><span data-stu-id="69980-352">12</span></span></td>
    <td><span data-ttu-id="69980-353">4</span><span class="sxs-lookup"><span data-stu-id="69980-353">4</span></span></td>
    <td><span data-ttu-id="69980-354">364.29</span><span class="sxs-lookup"><span data-stu-id="69980-354">364.29</span></span></td>
    <td><span data-ttu-id="69980-355">14</span><span class="sxs-lookup"><span data-stu-id="69980-355">14</span></span></td>
    <td><span data-ttu-id="69980-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="69980-356">1,275.00</span></span></td>
    <td><span data-ttu-id="69980-357">91.07</span><span class="sxs-lookup"><span data-stu-id="69980-357">91.07</span></span></td>
    <td><span data-ttu-id="69980-358">4.00</span><span class="sxs-lookup"><span data-stu-id="69980-358">4.00</span></span></td>
    <td><span data-ttu-id="69980-359">364.29</span><span class="sxs-lookup"><span data-stu-id="69980-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="69980-360">1000</span><span class="sxs-lookup"><span data-stu-id="69980-360">1000</span></span></td>
    <td><span data-ttu-id="69980-361">2</span><span class="sxs-lookup"><span data-stu-id="69980-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="69980-362">10</span><span class="sxs-lookup"><span data-stu-id="69980-362">10</span></span></td>
    <td><span data-ttu-id="69980-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-363">2,000.00</span></span></td>
    <td><span data-ttu-id="69980-364">10</span><span class="sxs-lookup"><span data-stu-id="69980-364">10</span></span></td>
    <td><span data-ttu-id="69980-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-365">2,000.00</span></span></td>
    <td><span data-ttu-id="69980-366">200.00</span><span class="sxs-lookup"><span data-stu-id="69980-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-367">10.00</span><span class="sxs-lookup"><span data-stu-id="69980-367">10.00</span></span></td>
    <td><span data-ttu-id="69980-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="69980-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="69980-369"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="69980-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="69980-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="69980-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="69980-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="69980-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="69980-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="69980-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="69980-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="69980-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="69980-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="69980-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="69980-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="69980-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]