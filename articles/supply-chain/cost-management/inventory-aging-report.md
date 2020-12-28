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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6e708e4dc818f20fc8d835053da75c2fe9c98f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428684"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="d2386-103">Beispiele und Logik für Inventarfäligkeitsberichte</span><span class="sxs-lookup"><span data-stu-id="d2386-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2386-104">In diesem Thema werden einige Beispiele vorgestellt, die zeigen, wie die Ergebnisse eines **Inventarfälligkeitsberichts** interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="d2386-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="d2386-105">In diesem Bericht werden die verfügbaren Mengen- und Bestandswerte für einen ausgewählten Artikel oder eine Artikelgruppe in mehrere Periodenbereiche unterteilt.</span><span class="sxs-lookup"><span data-stu-id="d2386-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="d2386-106">Dieses Thema zeigt auch die interne Logik des Berichts.</span><span class="sxs-lookup"><span data-stu-id="d2386-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="d2386-107">Die Beispiele in diesem Thema zeigen Ergebnisse, die auf einem Standard **Fälligkeit des Inventar** Berichts dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d2386-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="d2386-108">Im Allgemeinen empfehlen wir jedoch die Verwendung der Version [Speicherung von Inventarfälligkeitsberichten](inventory-aging-report-storage.md) dieses Berichts, insbesondere wenn Sie viele Artikel und Lager haben, die verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d2386-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="d2386-109">Durch die Speicherung von Inventarfälligkeitsberichten wird jeder von Ihnen erstellte Bericht gespeichert, die Ergebnisse als interaktive Seite und als Diagramm angezeigt und Sie können jeden gespeicherten Bericht exportieren.</span><span class="sxs-lookup"><span data-stu-id="d2386-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="d2386-110">Beispieldaten, die in diesen Beispielen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d2386-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="d2386-111">Die Beispiele in diesem Thema basieren auf den in diesem Abschnitt beschriebenen Beispieltransaktionsdaten für das Inventar.</span><span class="sxs-lookup"><span data-stu-id="d2386-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="d2386-112">Lagerdimensionsgruppe einrichten</span><span class="sxs-lookup"><span data-stu-id="d2386-112">Storage dimension setup</span></span>

<span data-ttu-id="d2386-113">Das Beispielsystem enthält die folgenden Einstellungen für die Speicherabmessungen.</span><span class="sxs-lookup"><span data-stu-id="d2386-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="d2386-114">Name</span><span class="sxs-lookup"><span data-stu-id="d2386-114">Name</span></span>      | <span data-ttu-id="d2386-115">Aktiv</span><span class="sxs-lookup"><span data-stu-id="d2386-115">Active</span></span> | <span data-ttu-id="d2386-116">Physischer Bestand</span><span class="sxs-lookup"><span data-stu-id="d2386-116">Physical inventory</span></span> | <span data-ttu-id="d2386-117">Wertmäßiger Bestand</span><span class="sxs-lookup"><span data-stu-id="d2386-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="d2386-118">Site</span><span class="sxs-lookup"><span data-stu-id="d2386-118">Site</span></span>      | <span data-ttu-id="d2386-119">Ja</span><span class="sxs-lookup"><span data-stu-id="d2386-119">Yes</span></span>    | <span data-ttu-id="d2386-120">Ja</span><span class="sxs-lookup"><span data-stu-id="d2386-120">Yes</span></span>                | <span data-ttu-id="d2386-121">Ja</span><span class="sxs-lookup"><span data-stu-id="d2386-121">Yes</span></span>                 |
| <span data-ttu-id="d2386-122">Lagerort</span><span class="sxs-lookup"><span data-stu-id="d2386-122">Warehouse</span></span> | <span data-ttu-id="d2386-123">Ja</span><span class="sxs-lookup"><span data-stu-id="d2386-123">Yes</span></span>    | <span data-ttu-id="d2386-124">Ja</span><span class="sxs-lookup"><span data-stu-id="d2386-124">Yes</span></span>                | <span data-ttu-id="d2386-125">Nr.</span><span class="sxs-lookup"><span data-stu-id="d2386-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="d2386-126">Lagermodell</span><span class="sxs-lookup"><span data-stu-id="d2386-126">Inventory model</span></span>

<span data-ttu-id="d2386-127">Für das Beispielsystem lautet das Bestandsmodell für die freigegebenen Produkte *FIFO*, und die **Selbstkostenpreis** Einstellung für das Bestandsmodell ist auf *Physischen Wert einschließen* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2386-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="d2386-128">Lagerbuchungen</span><span class="sxs-lookup"><span data-stu-id="d2386-128">Inventory transactions</span></span>

<span data-ttu-id="d2386-129">Das Beispielsystem enthält die folgenden Inventurtransaktionen für ein freigegebenes Produkt mit der Artikelnummer *1000*.</span><span class="sxs-lookup"><span data-stu-id="d2386-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="d2386-130">Referenz</span><span class="sxs-lookup"><span data-stu-id="d2386-130">Reference</span></span>      | <span data-ttu-id="d2386-131">Site</span><span class="sxs-lookup"><span data-stu-id="d2386-131">Site</span></span> | <span data-ttu-id="d2386-132">Lagerort</span><span class="sxs-lookup"><span data-stu-id="d2386-132">Warehouse</span></span> | <span data-ttu-id="d2386-133">Zugang</span><span class="sxs-lookup"><span data-stu-id="d2386-133">Receipt</span></span>   | <span data-ttu-id="d2386-134">Abgang</span><span class="sxs-lookup"><span data-stu-id="d2386-134">Issue</span></span> | <span data-ttu-id="d2386-135">Physisches Datum</span><span class="sxs-lookup"><span data-stu-id="d2386-135">Physical date</span></span> | <span data-ttu-id="d2386-136">Finanzdatum</span><span class="sxs-lookup"><span data-stu-id="d2386-136">Financial date</span></span> | <span data-ttu-id="d2386-137">Leistung</span><span class="sxs-lookup"><span data-stu-id="d2386-137">Quantity</span></span> | <span data-ttu-id="d2386-138">Betrag KORE</span><span class="sxs-lookup"><span data-stu-id="d2386-138">Cost amount</span></span> | <span data-ttu-id="d2386-139">Phys. Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="d2386-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="d2386-140">Bestellung</span><span class="sxs-lookup"><span data-stu-id="d2386-140">Purchase order</span></span> | <span data-ttu-id="d2386-141">1</span><span class="sxs-lookup"><span data-stu-id="d2386-141">1</span></span>    | <span data-ttu-id="d2386-142">11</span><span class="sxs-lookup"><span data-stu-id="d2386-142">11</span></span>        | <span data-ttu-id="d2386-143">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="d2386-143">Purchased</span></span> |       | <span data-ttu-id="d2386-144">15. März</span><span class="sxs-lookup"><span data-stu-id="d2386-144">March 15</span></span>      | <span data-ttu-id="d2386-145">15. März</span><span class="sxs-lookup"><span data-stu-id="d2386-145">March 15</span></span>       | <span data-ttu-id="d2386-146">10</span><span class="sxs-lookup"><span data-stu-id="d2386-146">10</span></span>       | <span data-ttu-id="d2386-147">1.000</span><span class="sxs-lookup"><span data-stu-id="d2386-147">1,000</span></span>       | <span data-ttu-id="d2386-148">1.000</span><span class="sxs-lookup"><span data-stu-id="d2386-148">1,000</span></span>                |
| <span data-ttu-id="d2386-149">Bestellung</span><span class="sxs-lookup"><span data-stu-id="d2386-149">Purchase order</span></span> | <span data-ttu-id="d2386-150">2</span><span class="sxs-lookup"><span data-stu-id="d2386-150">2</span></span>    | <span data-ttu-id="d2386-151">21</span><span class="sxs-lookup"><span data-stu-id="d2386-151">21</span></span>        | <span data-ttu-id="d2386-152">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="d2386-152">Purchased</span></span> |       | <span data-ttu-id="d2386-153">15. März</span><span class="sxs-lookup"><span data-stu-id="d2386-153">March 15</span></span>      | <span data-ttu-id="d2386-154">15. März</span><span class="sxs-lookup"><span data-stu-id="d2386-154">March 15</span></span>       | <span data-ttu-id="d2386-155">10</span><span class="sxs-lookup"><span data-stu-id="d2386-155">10</span></span>       | <span data-ttu-id="d2386-156">2,000</span><span class="sxs-lookup"><span data-stu-id="d2386-156">2,000</span></span>       | <span data-ttu-id="d2386-157">2,000</span><span class="sxs-lookup"><span data-stu-id="d2386-157">2,000</span></span>                |
| <span data-ttu-id="d2386-158">Bestellung</span><span class="sxs-lookup"><span data-stu-id="d2386-158">Purchase order</span></span> | <span data-ttu-id="d2386-159">1</span><span class="sxs-lookup"><span data-stu-id="d2386-159">1</span></span>    | <span data-ttu-id="d2386-160">11</span><span class="sxs-lookup"><span data-stu-id="d2386-160">11</span></span>        | <span data-ttu-id="d2386-161">Eingegangen</span><span class="sxs-lookup"><span data-stu-id="d2386-161">Received</span></span>  |       | <span data-ttu-id="d2386-162">April 15</span><span class="sxs-lookup"><span data-stu-id="d2386-162">April 15</span></span>      |                | <span data-ttu-id="d2386-163">5</span><span class="sxs-lookup"><span data-stu-id="d2386-163">5</span></span>        |             | <span data-ttu-id="d2386-164">375</span><span class="sxs-lookup"><span data-stu-id="d2386-164">375</span></span>                  |
| <span data-ttu-id="d2386-165">Umlagerungsauftrag</span><span class="sxs-lookup"><span data-stu-id="d2386-165">Transfer order</span></span> | <span data-ttu-id="d2386-166">1</span><span class="sxs-lookup"><span data-stu-id="d2386-166">1</span></span>    | <span data-ttu-id="d2386-167">11</span><span class="sxs-lookup"><span data-stu-id="d2386-167">11</span></span>        |           | <span data-ttu-id="d2386-168">Verkauft</span><span class="sxs-lookup"><span data-stu-id="d2386-168">Sold</span></span>  | <span data-ttu-id="d2386-169">Mai 2</span><span class="sxs-lookup"><span data-stu-id="d2386-169">May 2</span></span>         | <span data-ttu-id="d2386-170">Mai 2</span><span class="sxs-lookup"><span data-stu-id="d2386-170">May 2</span></span>          | <span data-ttu-id="d2386-171">-5</span><span class="sxs-lookup"><span data-stu-id="d2386-171">-5</span></span>       | <span data-ttu-id="d2386-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="d2386-172">-458.33</span></span>     | <span data-ttu-id="d2386-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="d2386-173">-458.33</span></span>              |
| <span data-ttu-id="d2386-174">Umlagerungsauftrag</span><span class="sxs-lookup"><span data-stu-id="d2386-174">Transfer order</span></span> | <span data-ttu-id="d2386-175">1</span><span class="sxs-lookup"><span data-stu-id="d2386-175">1</span></span>    | <span data-ttu-id="d2386-176">12</span><span class="sxs-lookup"><span data-stu-id="d2386-176">12</span></span>        | <span data-ttu-id="d2386-177">Eingekauft</span><span class="sxs-lookup"><span data-stu-id="d2386-177">Purchased</span></span> |       | <span data-ttu-id="d2386-178">Mai 2</span><span class="sxs-lookup"><span data-stu-id="d2386-178">May 2</span></span>         | <span data-ttu-id="d2386-179">Mai 2</span><span class="sxs-lookup"><span data-stu-id="d2386-179">May 2</span></span>          | <span data-ttu-id="d2386-180">5</span><span class="sxs-lookup"><span data-stu-id="d2386-180">5</span></span>        | <span data-ttu-id="d2386-181">458.33</span><span class="sxs-lookup"><span data-stu-id="d2386-181">458.33</span></span>      | <span data-ttu-id="d2386-182">458.33</span><span class="sxs-lookup"><span data-stu-id="d2386-182">458.33</span></span>               |
| <span data-ttu-id="d2386-183">Auftrag</span><span class="sxs-lookup"><span data-stu-id="d2386-183">Sales order</span></span>    | <span data-ttu-id="d2386-184">1</span><span class="sxs-lookup"><span data-stu-id="d2386-184">1</span></span>    | <span data-ttu-id="d2386-185">12</span><span class="sxs-lookup"><span data-stu-id="d2386-185">12</span></span>        |           | <span data-ttu-id="d2386-186">Verkauft</span><span class="sxs-lookup"><span data-stu-id="d2386-186">Sold</span></span>  | <span data-ttu-id="d2386-187">Mai 3</span><span class="sxs-lookup"><span data-stu-id="d2386-187">May 3</span></span>         | <span data-ttu-id="d2386-188">Mai 3</span><span class="sxs-lookup"><span data-stu-id="d2386-188">May 3</span></span>          | <span data-ttu-id="d2386-189">-1</span><span class="sxs-lookup"><span data-stu-id="d2386-189">-1</span></span>       | <span data-ttu-id="d2386-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="d2386-190">-91.67</span></span>      | <span data-ttu-id="d2386-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="d2386-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="d2386-192">Wie Mengen und Beträge in jedem Periodenbereich berechnet werden</span><span class="sxs-lookup"><span data-stu-id="d2386-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="d2386-193">Mithilfe der in den vorherigen Abschnitten beschriebenen Beispieldaten können Sie einen Bericht **Alterung des Inventars** mit folgenden Einstellungen ausführen:</span><span class="sxs-lookup"><span data-stu-id="d2386-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="d2386-194">**Stand:** *9. Mai 2020*</span><span class="sxs-lookup"><span data-stu-id="d2386-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="d2386-195">**Seite:** *Aussicht*</span><span class="sxs-lookup"><span data-stu-id="d2386-195">**Site:** *View*</span></span>
- <span data-ttu-id="d2386-196">**Lagerort:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="d2386-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="d2386-197">**Artikelnummer:** *Gesamt*</span><span class="sxs-lookup"><span data-stu-id="d2386-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="d2386-198">**Alterungsdauer:** Legen Sie dieses Feld fest, um monatliche Bereiche zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d2386-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="d2386-199">In diesem Fall ähnelt der Inhalt des generierten Berichts dem folgenden Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d2386-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="d2386-200">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="d2386-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-201">Site</span><span class="sxs-lookup"><span data-stu-id="d2386-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-202">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-203">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="d2386-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-204">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="d2386-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-205">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="d2386-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-206">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="d2386-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="d2386-210">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-211">P1:Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="d2386-212">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-213">P2:Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="d2386-214">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-215">P3:Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="d2386-216">1000</span><span class="sxs-lookup"><span data-stu-id="d2386-216">1000</span></span></td>
    <td><span data-ttu-id="d2386-217">1</span><span class="sxs-lookup"><span data-stu-id="d2386-217">1</span></span></td>
    <td><span data-ttu-id="d2386-218">14</span><span class="sxs-lookup"><span data-stu-id="d2386-218">14</span></span></td>
    <td><span data-ttu-id="d2386-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="d2386-219">1,283.33</span></span></td>
    <td><span data-ttu-id="d2386-220">14</span><span class="sxs-lookup"><span data-stu-id="d2386-220">14</span></span></td>
    <td><span data-ttu-id="d2386-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="d2386-221">1,283.33</span></span></td>
    <td><span data-ttu-id="d2386-222">91.67</span><span class="sxs-lookup"><span data-stu-id="d2386-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-223">5.00</span><span class="sxs-lookup"><span data-stu-id="d2386-223">5.00</span></span></td>
    <td><span data-ttu-id="d2386-224">458.33</span><span class="sxs-lookup"><span data-stu-id="d2386-224">458.33</span></span></td>
    <td><span data-ttu-id="d2386-225">9.00</span><span class="sxs-lookup"><span data-stu-id="d2386-225">9.00</span></span></td>
    <td><span data-ttu-id="d2386-226">825.00</span><span class="sxs-lookup"><span data-stu-id="d2386-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="d2386-227">1000</span><span class="sxs-lookup"><span data-stu-id="d2386-227">1000</span></span></td>
    <td><span data-ttu-id="d2386-228">2</span><span class="sxs-lookup"><span data-stu-id="d2386-228">2</span></span></td>
    <td><span data-ttu-id="d2386-229">10</span><span class="sxs-lookup"><span data-stu-id="d2386-229">10</span></span></td>
    <td><span data-ttu-id="d2386-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-230">2,000.00</span></span></td>
    <td><span data-ttu-id="d2386-231">10</span><span class="sxs-lookup"><span data-stu-id="d2386-231">10</span></span></td>
    <td><span data-ttu-id="d2386-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-232">2,000.00</span></span></td>
    <td><span data-ttu-id="d2386-233">200.00</span><span class="sxs-lookup"><span data-stu-id="d2386-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-234">10.00</span><span class="sxs-lookup"><span data-stu-id="d2386-234">10.00</span></span></td>
    <td><span data-ttu-id="d2386-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="d2386-236"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="d2386-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="d2386-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="d2386-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="d2386-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="d2386-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="d2386-243">Beachten Sie die folgenden Details in diesem Beispielbericht:</span><span class="sxs-lookup"><span data-stu-id="d2386-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="d2386-244">Die Werte **Inventarwertmenge**, **Inventarwert** und **Durchschnittliche Stückkosten**, die im Bericht angezeigt werden, sind Werte für die Dimension des Finanzinventars (in diesem Fall **Seite**).</span><span class="sxs-lookup"><span data-stu-id="d2386-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="d2386-245">Für Standort 1 enthält der Bericht beispielsweise die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="d2386-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="d2386-246">Den Wert **Inventarwertmenge** ist *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="d2386-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="d2386-247">Der Wert **Inventarwertmenge** ist *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span><span class="sxs-lookup"><span data-stu-id="d2386-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="d2386-248">Der Wert **Durchschnittliche Stückkosten** ist *91,67*.</span><span class="sxs-lookup"><span data-stu-id="d2386-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="d2386-249">Der Wert **Lagerwert** und der Wert **Menge** in jedem Periodenbereich werden mithilfe vom Wert **Durchschnittliche Stückkosten** berechnet.</span><span class="sxs-lookup"><span data-stu-id="d2386-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="d2386-250">Der Bericht ermittelt die verfügbare Menge für jeden Periodenbereich, indem die insgesamt erhaltene Bestandsmenge für jeden Periodenbereich zusammengefasst wird.</span><span class="sxs-lookup"><span data-stu-id="d2386-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="d2386-251">Anschließend wird das Prinzip First In, First Out (FIFO)  angewendet, um die gesamte ausgegebene Menge abzuziehen, unabhängig vom verwendeten Bestandsmodell.</span><span class="sxs-lookup"><span data-stu-id="d2386-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="d2386-252">Wenn Sie denselben Bericht erneut ausführen, diesmal jedoch die Felder **Seite** und **Lagerort** auf *Anzeigen* festlegen, wird der neue Bericht dem folgenden Beispiel ähneln.</span><span class="sxs-lookup"><span data-stu-id="d2386-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="d2386-253">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="d2386-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-254">Site</span><span class="sxs-lookup"><span data-stu-id="d2386-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-255">Lagerort</span><span class="sxs-lookup"><span data-stu-id="d2386-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-256">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-257">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="d2386-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-258">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="d2386-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-259">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="d2386-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-260">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="d2386-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="d2386-264">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-265">P1: Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="d2386-266">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-267">P2: Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="d2386-268">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-269">P3: Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="d2386-270">1000</span><span class="sxs-lookup"><span data-stu-id="d2386-270">1000</span></span></td>
    <td><span data-ttu-id="d2386-271">1</span><span class="sxs-lookup"><span data-stu-id="d2386-271">1</span></span></td>
    <td><span data-ttu-id="d2386-272">11</span><span class="sxs-lookup"><span data-stu-id="d2386-272">11</span></span></td>
    <td><span data-ttu-id="d2386-273">10</span><span class="sxs-lookup"><span data-stu-id="d2386-273">10</span></span></td>
    <td><span data-ttu-id="d2386-274">916.67</span><span class="sxs-lookup"><span data-stu-id="d2386-274">916.67</span></span></td>
    <td><span data-ttu-id="d2386-275">14</span><span class="sxs-lookup"><span data-stu-id="d2386-275">14</span></span></td>
    <td><span data-ttu-id="d2386-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="d2386-276">1,283.33</span></span></td>
    <td><span data-ttu-id="d2386-277">91.67</span><span class="sxs-lookup"><span data-stu-id="d2386-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-278">5.00</span><span class="sxs-lookup"><span data-stu-id="d2386-278">5.00</span></span></td>
    <td><span data-ttu-id="d2386-279">458.33</span><span class="sxs-lookup"><span data-stu-id="d2386-279">458.33</span></span></td>
    <td><span data-ttu-id="d2386-280">5.00</span><span class="sxs-lookup"><span data-stu-id="d2386-280">5.00</span></span></td>
    <td><span data-ttu-id="d2386-281">458.33</span><span class="sxs-lookup"><span data-stu-id="d2386-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="d2386-282">1000</span><span class="sxs-lookup"><span data-stu-id="d2386-282">1000</span></span></td>
    <td><span data-ttu-id="d2386-283">1</span><span class="sxs-lookup"><span data-stu-id="d2386-283">1</span></span></td>
    <td><span data-ttu-id="d2386-284">12</span><span class="sxs-lookup"><span data-stu-id="d2386-284">12</span></span></td>
    <td><span data-ttu-id="d2386-285">4</span><span class="sxs-lookup"><span data-stu-id="d2386-285">4</span></span></td>
    <td><span data-ttu-id="d2386-286">366.67</span><span class="sxs-lookup"><span data-stu-id="d2386-286">366.67</span></span></td>
    <td><span data-ttu-id="d2386-287">14</span><span class="sxs-lookup"><span data-stu-id="d2386-287">14</span></span></td>
    <td><span data-ttu-id="d2386-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="d2386-288">1,283.33</span></span></td>
    <td><span data-ttu-id="d2386-289">91.67</span><span class="sxs-lookup"><span data-stu-id="d2386-289">91.67</span></span></td>
    <td><span data-ttu-id="d2386-290">4.00</span><span class="sxs-lookup"><span data-stu-id="d2386-290">4.00</span></span></td>
    <td><span data-ttu-id="d2386-291">366.67</span><span class="sxs-lookup"><span data-stu-id="d2386-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="d2386-292">1000</span><span class="sxs-lookup"><span data-stu-id="d2386-292">1000</span></span></td>
    <td><span data-ttu-id="d2386-293">2</span><span class="sxs-lookup"><span data-stu-id="d2386-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="d2386-294">10</span><span class="sxs-lookup"><span data-stu-id="d2386-294">10</span></span></td>
    <td><span data-ttu-id="d2386-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-295">2,000.00</span></span></td>
    <td><span data-ttu-id="d2386-296">10</span><span class="sxs-lookup"><span data-stu-id="d2386-296">10</span></span></td>
    <td><span data-ttu-id="d2386-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-297">2,000.00</span></span></td>
    <td><span data-ttu-id="d2386-298">200.00</span><span class="sxs-lookup"><span data-stu-id="d2386-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-299">10.00</span><span class="sxs-lookup"><span data-stu-id="d2386-299">10.00</span></span></td>
    <td><span data-ttu-id="d2386-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="d2386-301"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="d2386-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="d2386-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="d2386-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="d2386-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="d2386-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="d2386-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="d2386-310">Diesmal ist Site 1 in zwei Zeilen unterteilt, eine für Lager 11 und eine für Lager 12.</span><span class="sxs-lookup"><span data-stu-id="d2386-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="d2386-311">Aber die Werte **Inventarwertmenge**, **Inventarwert** und **Durchschnittliche Stückkosten**, die im Bericht angezeigt werden, sind gleich weil der **Lagerort** keine Finanzdimension ist.</span><span class="sxs-lookup"><span data-stu-id="d2386-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="d2386-312">Beachten Sie außerdem, dass die Mengenverteilung von Standort 1 unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="d2386-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="d2386-313">In dem ersten Bericht, den Sie ausgeführt haben, hat das System den Transportauftrag ignoriert, der an derselben Site aufgetreten ist, und die Menge der Verkaufsrechnung vom Zeitraumbereich **31.03.2020 – 01.03.2020** in Site 1 abgezogen.</span><span class="sxs-lookup"><span data-stu-id="d2386-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="d2386-314">Im neuen Bericht zieht das System jedoch die Menge der Verkaufsrechnung vom Zeitraumbereich **08.05.2020 – 01.05.2020** im Lager 12 ab.</span><span class="sxs-lookup"><span data-stu-id="d2386-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="d2386-315">Effekte der Bestandschließung</span><span class="sxs-lookup"><span data-stu-id="d2386-315">Effects of inventory closing</span></span>

<span data-ttu-id="d2386-316">Wenn Sie das Inventar für Mai schließen und dann den vorherigen Bericht erneut ausführen, aber das Feld **Stand Datum** auf *31. Mai 2020* festlegen, werden Sie folgende Ergebnisse feststellen:</span><span class="sxs-lookup"><span data-stu-id="d2386-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="d2386-317">Der **Bestandwert** und der Wert **Durchschnittliche Stückkosten** werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d2386-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="d2386-318">Der **verfügbare Wert** und der Wert **Betrag** in jedem Periodenbereich werden entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d2386-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="d2386-319">Der neue Bericht sieht ähnlich aus wie das folgende Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d2386-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="d2386-320">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="d2386-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-321">Site</span><span class="sxs-lookup"><span data-stu-id="d2386-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-322">Lagerort</span><span class="sxs-lookup"><span data-stu-id="d2386-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-323">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-324">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="d2386-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-325">Lagerwertmenge</span><span class="sxs-lookup"><span data-stu-id="d2386-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-326">Lagerwert</span><span class="sxs-lookup"><span data-stu-id="d2386-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="d2386-327">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="d2386-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="d2386-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="d2386-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="d2386-331">P1: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-332">P1: Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="d2386-333">P2: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-334">P2: Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="d2386-335">P3: Menge</span><span class="sxs-lookup"><span data-stu-id="d2386-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="d2386-336">P3: Betrag</span><span class="sxs-lookup"><span data-stu-id="d2386-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="d2386-337">1000</span><span class="sxs-lookup"><span data-stu-id="d2386-337">1000</span></span></td>
    <td><span data-ttu-id="d2386-338">1</span><span class="sxs-lookup"><span data-stu-id="d2386-338">1</span></span></td>
    <td><span data-ttu-id="d2386-339">11</span><span class="sxs-lookup"><span data-stu-id="d2386-339">11</span></span></td>
    <td><span data-ttu-id="d2386-340">10</span><span class="sxs-lookup"><span data-stu-id="d2386-340">10</span></span></td>
    <td><span data-ttu-id="d2386-341">910.70</span><span class="sxs-lookup"><span data-stu-id="d2386-341">910.70</span></span></td>
    <td><span data-ttu-id="d2386-342">14</span><span class="sxs-lookup"><span data-stu-id="d2386-342">14</span></span></td>
    <td><span data-ttu-id="d2386-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="d2386-343">1,275.00</span></span></td>
    <td><span data-ttu-id="d2386-344">91.07</span><span class="sxs-lookup"><span data-stu-id="d2386-344">91.07</span></span></td>
    <td><span data-ttu-id="d2386-345">0,00</span><span class="sxs-lookup"><span data-stu-id="d2386-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="d2386-346">5.00</span><span class="sxs-lookup"><span data-stu-id="d2386-346">5.00</span></span></td>
    <td><span data-ttu-id="d2386-347">455.36</span><span class="sxs-lookup"><span data-stu-id="d2386-347">455.36</span></span></td>
    <td><span data-ttu-id="d2386-348">5.00</span><span class="sxs-lookup"><span data-stu-id="d2386-348">5.00</span></span></td>
    <td><span data-ttu-id="d2386-349">455.36</span><span class="sxs-lookup"><span data-stu-id="d2386-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="d2386-350">1000</span><span class="sxs-lookup"><span data-stu-id="d2386-350">1000</span></span></td>
    <td><span data-ttu-id="d2386-351">1</span><span class="sxs-lookup"><span data-stu-id="d2386-351">1</span></span></td>
    <td><span data-ttu-id="d2386-352">12</span><span class="sxs-lookup"><span data-stu-id="d2386-352">12</span></span></td>
    <td><span data-ttu-id="d2386-353">4</span><span class="sxs-lookup"><span data-stu-id="d2386-353">4</span></span></td>
    <td><span data-ttu-id="d2386-354">364.29</span><span class="sxs-lookup"><span data-stu-id="d2386-354">364.29</span></span></td>
    <td><span data-ttu-id="d2386-355">14</span><span class="sxs-lookup"><span data-stu-id="d2386-355">14</span></span></td>
    <td><span data-ttu-id="d2386-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="d2386-356">1,275.00</span></span></td>
    <td><span data-ttu-id="d2386-357">91.07</span><span class="sxs-lookup"><span data-stu-id="d2386-357">91.07</span></span></td>
    <td><span data-ttu-id="d2386-358">4.00</span><span class="sxs-lookup"><span data-stu-id="d2386-358">4.00</span></span></td>
    <td><span data-ttu-id="d2386-359">364.29</span><span class="sxs-lookup"><span data-stu-id="d2386-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="d2386-360">1000</span><span class="sxs-lookup"><span data-stu-id="d2386-360">1000</span></span></td>
    <td><span data-ttu-id="d2386-361">2</span><span class="sxs-lookup"><span data-stu-id="d2386-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="d2386-362">10</span><span class="sxs-lookup"><span data-stu-id="d2386-362">10</span></span></td>
    <td><span data-ttu-id="d2386-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-363">2,000.00</span></span></td>
    <td><span data-ttu-id="d2386-364">10</span><span class="sxs-lookup"><span data-stu-id="d2386-364">10</span></span></td>
    <td><span data-ttu-id="d2386-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-365">2,000.00</span></span></td>
    <td><span data-ttu-id="d2386-366">200.00</span><span class="sxs-lookup"><span data-stu-id="d2386-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-367">10.00</span><span class="sxs-lookup"><span data-stu-id="d2386-367">10.00</span></span></td>
    <td><span data-ttu-id="d2386-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="d2386-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="d2386-369"><strong>1000 Summen</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="d2386-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="d2386-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="d2386-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="d2386-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="d2386-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="d2386-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="d2386-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="d2386-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
