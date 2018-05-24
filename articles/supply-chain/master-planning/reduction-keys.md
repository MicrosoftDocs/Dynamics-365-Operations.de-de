---
title: "Planzahlenverrechnungsschlüssel"
description: "Dieser Artikel enthält Beispiele, die zeigen, wie Sie einen Planzahlenverrechnungsschlüssel einrichten. Er umfasst Informationen zu den verschiedenen Einstellungen der Planzahlenverrechnungsschlüssel und deren Ergebnissen. Mithilfe von Planzahlenverrechnungsschlüsseln wird definiert, wie der Planungsbedarf verringert werden soll."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4b7f4ebd635e02f3cfc6d0f620dad30e6b1a98a2
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="reduction-keys"></a><span data-ttu-id="ae31c-105">Planzahlenverrechnungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="ae31c-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae31c-106">Dieser Artikel enthält Beispiele, die zeigen, wie Sie einen Planzahlenverrechnungsschlüssel einrichten.</span><span class="sxs-lookup"><span data-stu-id="ae31c-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="ae31c-107">Er umfasst Informationen zu den verschiedenen Einstellungen der Planzahlenverrechnungsschlüssel und deren Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="ae31c-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="ae31c-108">Mithilfe von Planzahlenverrechnungsschlüsseln wird definiert, wie der Planungsbedarf verringert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae31c-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="ae31c-109">Beispiel 1: Prozent - Planzahlenverrechnungsschlüssel-Planungsverringerungsprinzip</span><span class="sxs-lookup"><span data-stu-id="ae31c-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="ae31c-110">Dieses Beispiel verdeutlicht, wie ein Planzahlenverrechnungsschlüssel den Bedarf der Bedarfsplanung verringert, und zwar gemäß den vom Planzahlenverrechnungsschlüssel definierten Prozentsätzen und Perioden.</span><span class="sxs-lookup"><span data-stu-id="ae31c-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="ae31c-111">Wählen Sie auf der Seite **Planzahlenverrechnungsschlüssel** die folgenden Positionen.</span><span class="sxs-lookup"><span data-stu-id="ae31c-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="ae31c-112">Rückgeld</span><span class="sxs-lookup"><span data-stu-id="ae31c-112">Change</span></span> | <span data-ttu-id="ae31c-113">Einheit</span><span class="sxs-lookup"><span data-stu-id="ae31c-113">Unit</span></span>  | <span data-ttu-id="ae31c-114">Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="ae31c-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="ae31c-115">1</span><span class="sxs-lookup"><span data-stu-id="ae31c-115">1</span></span>    | <span data-ttu-id="ae31c-116">Monat</span><span class="sxs-lookup"><span data-stu-id="ae31c-116">Month</span></span> |   <span data-ttu-id="ae31c-117">100</span><span class="sxs-lookup"><span data-stu-id="ae31c-117">100</span></span>   |
   |   <span data-ttu-id="ae31c-118">2</span><span class="sxs-lookup"><span data-stu-id="ae31c-118">2</span></span>    | <span data-ttu-id="ae31c-119">Monat</span><span class="sxs-lookup"><span data-stu-id="ae31c-119">Month</span></span> |   <span data-ttu-id="ae31c-120">75</span><span class="sxs-lookup"><span data-stu-id="ae31c-120">75</span></span>    |
   |   <span data-ttu-id="ae31c-121">3</span><span class="sxs-lookup"><span data-stu-id="ae31c-121">3</span></span>    | <span data-ttu-id="ae31c-122">Monat</span><span class="sxs-lookup"><span data-stu-id="ae31c-122">Month</span></span> |   <span data-ttu-id="ae31c-123">50</span><span class="sxs-lookup"><span data-stu-id="ae31c-123">50</span></span>    |
   |   <span data-ttu-id="ae31c-124">4</span><span class="sxs-lookup"><span data-stu-id="ae31c-124">4</span></span>    | <span data-ttu-id="ae31c-125">Monat</span><span class="sxs-lookup"><span data-stu-id="ae31c-125">Month</span></span> |   <span data-ttu-id="ae31c-126">25</span><span class="sxs-lookup"><span data-stu-id="ae31c-126">25</span></span>    |


2. <span data-ttu-id="ae31c-127">Verknüpfen Sie den Planzahlenverrechnungsschlüssel mit der Deckungsgruppe des Artikels.</span><span class="sxs-lookup"><span data-stu-id="ae31c-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="ae31c-128">Auf der **Produktprogrammpläne**-Seite im Feld **Reduktionsprinzip** wählen Sie **Prozent - Planzahlenverrechnungsschlüssel** aus.</span><span class="sxs-lookup"><span data-stu-id="ae31c-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="ae31c-129">Erstellen Sie eine Bedarfsplanung von 1000 Stück pro Monat.</span><span class="sxs-lookup"><span data-stu-id="ae31c-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="ae31c-130">Wird der Umsatzplanungslauf am 1. Januar ausgeführt, wird der Bedarf der Bedarfsplanung entsprechend den Prozentwerten verbraucht, die Sie auf der Seite **Planzahlenverrechnungsschlüssel** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="ae31c-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="ae31c-131">Die folgenden Bedarfsmengen werden in den Produktprogrammplan übertragen.</span><span class="sxs-lookup"><span data-stu-id="ae31c-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="ae31c-132">Monat</span><span class="sxs-lookup"><span data-stu-id="ae31c-132">Month</span></span>                | <span data-ttu-id="ae31c-133">Erforderliche Stückzahl</span><span class="sxs-lookup"><span data-stu-id="ae31c-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="ae31c-134">Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-134">January</span></span>              | <span data-ttu-id="ae31c-135">0</span><span class="sxs-lookup"><span data-stu-id="ae31c-135">0</span></span>                         |
| <span data-ttu-id="ae31c-136">Februar</span><span class="sxs-lookup"><span data-stu-id="ae31c-136">February</span></span>             | <span data-ttu-id="ae31c-137">250</span><span class="sxs-lookup"><span data-stu-id="ae31c-137">250</span></span>                       |
| <span data-ttu-id="ae31c-138">März</span><span class="sxs-lookup"><span data-stu-id="ae31c-138">March</span></span>                | <span data-ttu-id="ae31c-139">500</span><span class="sxs-lookup"><span data-stu-id="ae31c-139">500</span></span>                       |
| <span data-ttu-id="ae31c-140">April</span><span class="sxs-lookup"><span data-stu-id="ae31c-140">April</span></span>                | <span data-ttu-id="ae31c-141">750</span><span class="sxs-lookup"><span data-stu-id="ae31c-141">750</span></span>                       |
| <span data-ttu-id="ae31c-142">Mai - Dezember</span><span class="sxs-lookup"><span data-stu-id="ae31c-142">May through December</span></span> | <span data-ttu-id="ae31c-143">1.000</span><span class="sxs-lookup"><span data-stu-id="ae31c-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="ae31c-144">Beispiel 2: Buchungen - Planzahlenverrechnungsschlüssel-Planungsverringerungsprinzip</span><span class="sxs-lookup"><span data-stu-id="ae31c-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="ae31c-145">Dieses Beispiel verdeutlicht, wie tatsächliche Aufträge, die in den vom Planzahlenverrechnungsschlüssel definierten Perioden anfallen, den Bedarf der Bedarfsplanung verringern.</span><span class="sxs-lookup"><span data-stu-id="ae31c-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="ae31c-146">Auf der **Produktprogrammpläne**-Seite im Feld **Reduktionsprinzip** wählen Sie **Buchungen - Planzahlenverrechnungsschlüssel** aus.</span><span class="sxs-lookup"><span data-stu-id="ae31c-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="ae31c-147">Am 1. Januar lagen die folgenden Aufträge vor.</span><span class="sxs-lookup"><span data-stu-id="ae31c-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="ae31c-148">Monat</span><span class="sxs-lookup"><span data-stu-id="ae31c-148">Month</span></span>    | <span data-ttu-id="ae31c-149">Bestellte Stückzahl</span><span class="sxs-lookup"><span data-stu-id="ae31c-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="ae31c-150">Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-150">January</span></span>  | <span data-ttu-id="ae31c-151">956</span><span class="sxs-lookup"><span data-stu-id="ae31c-151">956</span></span>                      |
| <span data-ttu-id="ae31c-152">Februar</span><span class="sxs-lookup"><span data-stu-id="ae31c-152">February</span></span> | <span data-ttu-id="ae31c-153">1.176</span><span class="sxs-lookup"><span data-stu-id="ae31c-153">1,176</span></span>                    |
| <span data-ttu-id="ae31c-154">März</span><span class="sxs-lookup"><span data-stu-id="ae31c-154">March</span></span>    | <span data-ttu-id="ae31c-155">451</span><span class="sxs-lookup"><span data-stu-id="ae31c-155">451</span></span>                      |
| <span data-ttu-id="ae31c-156">April</span><span class="sxs-lookup"><span data-stu-id="ae31c-156">April</span></span>    | <span data-ttu-id="ae31c-157">119</span><span class="sxs-lookup"><span data-stu-id="ae31c-157">119</span></span>                      |

<span data-ttu-id="ae31c-158">Unter Verwendung derselben Bedarfsplanung von 1000 Stück pro Monat werden die folgenden Bedarfsmengen in den Produktprogrammplan übertragen:</span><span class="sxs-lookup"><span data-stu-id="ae31c-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="ae31c-159">Monat</span><span class="sxs-lookup"><span data-stu-id="ae31c-159">Month</span></span>                | <span data-ttu-id="ae31c-160">Erforderliche Stückzahl</span><span class="sxs-lookup"><span data-stu-id="ae31c-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="ae31c-161">Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-161">January</span></span>              | <span data-ttu-id="ae31c-162">44</span><span class="sxs-lookup"><span data-stu-id="ae31c-162">44</span></span>                        |
| <span data-ttu-id="ae31c-163">Februar</span><span class="sxs-lookup"><span data-stu-id="ae31c-163">February</span></span>             | <span data-ttu-id="ae31c-164">0</span><span class="sxs-lookup"><span data-stu-id="ae31c-164">0</span></span>                         |
| <span data-ttu-id="ae31c-165">März</span><span class="sxs-lookup"><span data-stu-id="ae31c-165">March</span></span>                | <span data-ttu-id="ae31c-166">549</span><span class="sxs-lookup"><span data-stu-id="ae31c-166">549</span></span>                       |
| <span data-ttu-id="ae31c-167">April</span><span class="sxs-lookup"><span data-stu-id="ae31c-167">April</span></span>                | <span data-ttu-id="ae31c-168">881</span><span class="sxs-lookup"><span data-stu-id="ae31c-168">881</span></span>                       |
| <span data-ttu-id="ae31c-169">Mai - Dezember</span><span class="sxs-lookup"><span data-stu-id="ae31c-169">May through December</span></span> | <span data-ttu-id="ae31c-170">1.000</span><span class="sxs-lookup"><span data-stu-id="ae31c-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="ae31c-171">Beispiel 3: Buchungen - dynamische Periode Planungsverringerungsprinzip</span><span class="sxs-lookup"><span data-stu-id="ae31c-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="ae31c-172">In den meisten Fällen werden Systeme so eingerichtet, das Buchungen Bedarfsplanung innerhalb bestimmter Prognoseperioden reduzieren (Wochen, Monate usw.).</span><span class="sxs-lookup"><span data-stu-id="ae31c-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="ae31c-173">Die Perioden werden im Planzahlenverrechnungsschlüssel definiert.</span><span class="sxs-lookup"><span data-stu-id="ae31c-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="ae31c-174">Jedoch können die Zeit zwischen zwei Bedarfsplanungspositionen auch eine Periode *implizieren*.</span><span class="sxs-lookup"><span data-stu-id="ae31c-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="ae31c-175">Erstellen Sie eine Bedarfsplanung für die folgenden Datumsangaben und Mengen.</span><span class="sxs-lookup"><span data-stu-id="ae31c-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="ae31c-176">Datum</span><span class="sxs-lookup"><span data-stu-id="ae31c-176">Date</span></span>       | <span data-ttu-id="ae31c-177">Bedarfsplanung</span><span class="sxs-lookup"><span data-stu-id="ae31c-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="ae31c-178">1. Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-178">January 1</span></span>  | <span data-ttu-id="ae31c-179">1.000</span><span class="sxs-lookup"><span data-stu-id="ae31c-179">1,000</span></span>           |
   | <span data-ttu-id="ae31c-180">5. Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-180">January 5</span></span>  | <span data-ttu-id="ae31c-181">500</span><span class="sxs-lookup"><span data-stu-id="ae31c-181">500</span></span>             |
   | <span data-ttu-id="ae31c-182">12. Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-182">January 12</span></span> | <span data-ttu-id="ae31c-183">1.000</span><span class="sxs-lookup"><span data-stu-id="ae31c-183">1,000</span></span>           |

   <span data-ttu-id="ae31c-184">In dieser Planung gibt es keinen klaren Zeitraum zwischen den Planungsdaten. Zwischen der ersten und zweiten Datumsangabe besteht eine viertägige Spanne und zwischen der zweiten und dritten Datumsangabe besteht eine siebentägige Spanne.</span><span class="sxs-lookup"><span data-stu-id="ae31c-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="ae31c-185">Diese verschiedenen Spannen sind die dynamischen Perioden.</span><span class="sxs-lookup"><span data-stu-id="ae31c-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="ae31c-186">Erstellen Sie Auftragspositionen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ae31c-186">Create sales order lines as follows.</span></span>
   | <span data-ttu-id="ae31c-187">Datum</span><span class="sxs-lookup"><span data-stu-id="ae31c-187">Date</span></span>                             | <span data-ttu-id="ae31c-188">Auftragsmenge</span><span class="sxs-lookup"><span data-stu-id="ae31c-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="ae31c-189">15. Dezember Im Jahr zuvor</span><span class="sxs-lookup"><span data-stu-id="ae31c-189">December 15 in the previous year</span></span> | <span data-ttu-id="ae31c-190">500</span><span class="sxs-lookup"><span data-stu-id="ae31c-190">500</span></span>                  |
   | <span data-ttu-id="ae31c-191">3. Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-191">January 3</span></span>                        | <span data-ttu-id="ae31c-192">100</span><span class="sxs-lookup"><span data-stu-id="ae31c-192">100</span></span>                  |
   | <span data-ttu-id="ae31c-193">10. Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-193">January 10</span></span>                       | <span data-ttu-id="ae31c-194">200</span><span class="sxs-lookup"><span data-stu-id="ae31c-194">200</span></span>                  |

<span data-ttu-id="ae31c-195">Die Planung wird wie folgt reduziert:</span><span class="sxs-lookup"><span data-stu-id="ae31c-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="ae31c-196">Der erste Auftrag liegt nicht innerhalb einer Periode. Damit sich keine Planung.</span><span class="sxs-lookup"><span data-stu-id="ae31c-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="ae31c-197">Der zweite Auftrag liegt zwischen dem 1. Januar und dem 5. Januar. Damit reduziert er die Planung für den 1. Januar um 100.</span><span class="sxs-lookup"><span data-stu-id="ae31c-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="ae31c-198">Der dritte Auftrag liegt zwischen dem 5. Januar und dem 12. Januar. Damit reduziert er die Planung für den 5. Januar um 200.</span><span class="sxs-lookup"><span data-stu-id="ae31c-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="ae31c-199">Der nächste Bestellvorschlag wird zur Erfüllung der Planung erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae31c-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="ae31c-200">Bedarfsplanungsdatum</span><span class="sxs-lookup"><span data-stu-id="ae31c-200">Demand forecast date</span></span> | <span data-ttu-id="ae31c-201">Verringerte Menge</span><span class="sxs-lookup"><span data-stu-id="ae31c-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="ae31c-202">1. Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-202">January 1</span></span>            | <span data-ttu-id="ae31c-203">900</span><span class="sxs-lookup"><span data-stu-id="ae31c-203">900</span></span>              |
| <span data-ttu-id="ae31c-204">5. Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-204">January 5</span></span>            | <span data-ttu-id="ae31c-205">300</span><span class="sxs-lookup"><span data-stu-id="ae31c-205">300</span></span>              |
| <span data-ttu-id="ae31c-206">12. Januar</span><span class="sxs-lookup"><span data-stu-id="ae31c-206">January 12</span></span>           | <span data-ttu-id="ae31c-207">1.000</span><span class="sxs-lookup"><span data-stu-id="ae31c-207">1,000</span></span>            |

<span data-ttu-id="ae31c-208">Hier eine Zusammenfassung der **Buchungen - dynamische Periode**-Verringerung:</span><span class="sxs-lookup"><span data-stu-id="ae31c-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="ae31c-209">Der Planungsbedarf wird durch die tatsächlichen Auftragsbuchungen verringert, die während der dynamischen Periode stattfinden.</span><span class="sxs-lookup"><span data-stu-id="ae31c-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="ae31c-210">Die dynamische Periode erstreckt sich über die aktuellen Planungsdaten und endet beim Beginn der nächsten Planung.</span><span class="sxs-lookup"><span data-stu-id="ae31c-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="ae31c-211">Für diese Methode wird kein Planzahlenverrechnungsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae31c-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="ae31c-212">Wenn diese Option verwendet wird, tritt das folgende Verhalten auf:</span><span class="sxs-lookup"><span data-stu-id="ae31c-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="ae31c-213">Wenn die Planung vollständig verringert wird, wird der Planungsbedarf für die aktuelle Planung 0.</span><span class="sxs-lookup"><span data-stu-id="ae31c-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="ae31c-214">Wenn keine zukünftige Planung vorhanden ist, wird der Planungsbedarf der letzten eingegebenen Planung verringert.</span><span class="sxs-lookup"><span data-stu-id="ae31c-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="ae31c-215">Planungszeiträume sind in der Berechnung der Planungsverringerung enthalten.</span><span class="sxs-lookup"><span data-stu-id="ae31c-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="ae31c-216">Positive Tage sind in der Berechnung der Planungsverringerung enthalten.</span><span class="sxs-lookup"><span data-stu-id="ae31c-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="ae31c-217">Wenn die tatsächlichen Auftragsbuchungen größer sind als der geplante Bedarf, werden die verbleibenden Buchungen nicht in die nächste Planungsperiode vorgetragen.</span><span class="sxs-lookup"><span data-stu-id="ae31c-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="ae31c-218">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ae31c-218">Additional resources</span></span>
--------

[<span data-ttu-id="ae31c-219">Produktprogrammpläne</span><span class="sxs-lookup"><span data-stu-id="ae31c-219">Master plans</span></span>](master-plans.md)




