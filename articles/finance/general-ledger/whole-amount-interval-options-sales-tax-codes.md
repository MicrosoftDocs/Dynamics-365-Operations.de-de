---
title: Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes
description: Dieser Artikel beschreibt die Optionen des Felds "Berechnungsmethoden" für Mehrwertsteuercodes und wie die Mehrwertsteuer für Intervalle und gesamte Beträge berechnet wird.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec724030e12e504625b2b102cba25b7eddbf7e96
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978435"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="08491-103">Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes</span><span class="sxs-lookup"><span data-stu-id="08491-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08491-104">Dieser Artikel beschreibt die Optionen des Felds "Berechnungsmethoden" für Mehrwertsteuercodes und wie die Mehrwertsteuer für Intervalle und gesamte Beträge berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="08491-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="08491-105">Sie können einen Mehrwertsteuercode so einrichten, dass er basierend auf einen ganzen Betrag oder einen Intervallbetrag berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="08491-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="08491-106">Verwenden Sie auf der Seite "Mehrwertsteuercodes" das Feld "Berechnungsmethode" im Inforegister "Berechnung", um auszuwählen, wie der Mehrwertsteuercode berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08491-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="08491-107">Gesamtbetrag – Der Steuersatz wird auf den gesamten steuerbaren Betrag angewendet.</span><span class="sxs-lookup"><span data-stu-id="08491-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="08491-108">Intervall – Der steuerbare Betrag wird aufgeteilt, und jeder Anteil wird in einen Bereich mit einem bestimmten Mehrwertsteuersatz eingeordnet.</span><span class="sxs-lookup"><span data-stu-id="08491-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="08491-109">Der Anteil, der einem bestimmten Intervall angehört, wird gemäß dem Steuersatz für dieses Intervall versteuert.</span><span class="sxs-lookup"><span data-stu-id="08491-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="08491-110">Die Mehrwertsteuer wird aus der Summe der Steuerbeträge gebildet, die für die einzelnen Betragsintervalle berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="08491-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="08491-111">Die Intervalloption ist nur verfügbar, wenn Sie im Feld "Berechnungsmethode" "Position" im Bereich "Mehrwertsteuer" der Parameterseite "Hauptbuch" auswählen.</span><span class="sxs-lookup"><span data-stu-id="08491-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="08491-112">Intervalle werden auf der Seite "Mehrwertsteuer-Codewerte" eingerichtet, indem Sie minimale und maximale Grenzbeträge pro Steuersatz eingeben.</span><span class="sxs-lookup"><span data-stu-id="08491-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="08491-113">Damit Steuern unabhängig von der ausgewählten Berechnungsmethode für alle steuerbaren Beträge berechnet werden, müssen die Intervalle die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="08491-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="08491-114">Die Untergrenze des ersten Intervalls muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="08491-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="08491-115">Die Obergrenze des letzten Intervalls muss Null sein (unbegrenzt).</span><span class="sxs-lookup"><span data-stu-id="08491-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="08491-116">Die Obergrenze eines beliebigen Intervalls muss kleiner als die Untergrenze des Folgeintervalls sein.</span><span class="sxs-lookup"><span data-stu-id="08491-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="08491-117">Bildet ein Betrag gleichzeitig die Obergrenze des vorherigen und die Untergrenze des nächsten Intervalls, gilt für den Betrag der Steuersatz des ersten Intervalls.</span><span class="sxs-lookup"><span data-stu-id="08491-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="08491-118">Liegt ein Betrag außerhalb der Intervalle, die mittels Unter- und Obergrenzen definiert wurden, wird der Steuersatz "0" verwendet.</span><span class="sxs-lookup"><span data-stu-id="08491-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="08491-119">Beispiel: Berechnungsmethode mit Gesamtbetrag</span><span class="sxs-lookup"><span data-stu-id="08491-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="08491-120">Auf der Seite "Mehrwertsteuer-Codewerte" werden Mehrwertsteuersätze für die folgenden Intervalle eingerichtet:</span><span class="sxs-lookup"><span data-stu-id="08491-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="08491-121">**Untergrenze**</span><span class="sxs-lookup"><span data-stu-id="08491-121">**Minimum limit**</span></span> | <span data-ttu-id="08491-122">**Höchstgrenze**</span><span class="sxs-lookup"><span data-stu-id="08491-122">**Maximum limit**</span></span> | <span data-ttu-id="08491-123">**Steuersatz**</span><span class="sxs-lookup"><span data-stu-id="08491-123">**Tax rate**</span></span> |
| <span data-ttu-id="08491-124">0,00</span><span class="sxs-lookup"><span data-stu-id="08491-124">0.00</span></span>              | <span data-ttu-id="08491-125">50,00</span><span class="sxs-lookup"><span data-stu-id="08491-125">50.00</span></span>             | <span data-ttu-id="08491-126">30 %</span><span class="sxs-lookup"><span data-stu-id="08491-126">30%</span></span>          |
| <span data-ttu-id="08491-127">50,00</span><span class="sxs-lookup"><span data-stu-id="08491-127">50.00</span></span>             | <span data-ttu-id="08491-128">100,00</span><span class="sxs-lookup"><span data-stu-id="08491-128">100.00</span></span>            | <span data-ttu-id="08491-129">20 %</span><span class="sxs-lookup"><span data-stu-id="08491-129">20%</span></span>          |
| <span data-ttu-id="08491-130">100,00</span><span class="sxs-lookup"><span data-stu-id="08491-130">100.00</span></span>            | <span data-ttu-id="08491-131">0,00</span><span class="sxs-lookup"><span data-stu-id="08491-131">0.00</span></span>              | <span data-ttu-id="08491-132">10 %</span><span class="sxs-lookup"><span data-stu-id="08491-132">10%</span></span>          |

<span data-ttu-id="08491-133">Die Mehrwertsteuer wird mit dem gesamten steuerpflichtigen Betrag veranschlagt.</span><span class="sxs-lookup"><span data-stu-id="08491-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="08491-134">Steuerpflichtiger Betrag (Preis)</span><span class="sxs-lookup"><span data-stu-id="08491-134">Taxable amount (price)</span></span> | <span data-ttu-id="08491-135">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="08491-135">Calculation</span></span>    | <span data-ttu-id="08491-136">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="08491-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="08491-137">35,00</span><span class="sxs-lookup"><span data-stu-id="08491-137">35.00</span></span>                  | <span data-ttu-id="08491-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="08491-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="08491-139">10,50</span><span class="sxs-lookup"><span data-stu-id="08491-139">10.50</span></span>     |
| <span data-ttu-id="08491-140">50,00</span><span class="sxs-lookup"><span data-stu-id="08491-140">50.00</span></span>                  | <span data-ttu-id="08491-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="08491-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="08491-142">15:00</span><span class="sxs-lookup"><span data-stu-id="08491-142">15.00</span></span>     |
| <span data-ttu-id="08491-143">85,00</span><span class="sxs-lookup"><span data-stu-id="08491-143">85.00</span></span>                  | <span data-ttu-id="08491-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="08491-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="08491-145">17,00</span><span class="sxs-lookup"><span data-stu-id="08491-145">17.00</span></span>     |
| <span data-ttu-id="08491-146">305,00</span><span class="sxs-lookup"><span data-stu-id="08491-146">305.00</span></span>                 | <span data-ttu-id="08491-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="08491-147">305.00 \* 0.10</span></span> | <span data-ttu-id="08491-148">30,50</span><span class="sxs-lookup"><span data-stu-id="08491-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="08491-149">Beispiel: Berechnungsmethode mit Intervall</span><span class="sxs-lookup"><span data-stu-id="08491-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="08491-150">Auf der Seite "Werte" werden Mehrwertsteuersätze für die folgenden Intervalle eingerichtet:</span><span class="sxs-lookup"><span data-stu-id="08491-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="08491-151">**Untergrenze**</span><span class="sxs-lookup"><span data-stu-id="08491-151">**Minimum limit**</span></span> | <span data-ttu-id="08491-152">**Höchstgrenze**</span><span class="sxs-lookup"><span data-stu-id="08491-152">**Maximum limit**</span></span> | <span data-ttu-id="08491-153">**Steuersatz**</span><span class="sxs-lookup"><span data-stu-id="08491-153">**Tax rate**</span></span> |
| <span data-ttu-id="08491-154">0,00</span><span class="sxs-lookup"><span data-stu-id="08491-154">0.00</span></span>              | <span data-ttu-id="08491-155">50,00</span><span class="sxs-lookup"><span data-stu-id="08491-155">50.00</span></span>             | <span data-ttu-id="08491-156">30 %</span><span class="sxs-lookup"><span data-stu-id="08491-156">30%</span></span>          |
| <span data-ttu-id="08491-157">50,00</span><span class="sxs-lookup"><span data-stu-id="08491-157">50.00</span></span>             | <span data-ttu-id="08491-158">100,00</span><span class="sxs-lookup"><span data-stu-id="08491-158">100.00</span></span>            | <span data-ttu-id="08491-159">20 %</span><span class="sxs-lookup"><span data-stu-id="08491-159">20%</span></span>          |
| <span data-ttu-id="08491-160">100,00</span><span class="sxs-lookup"><span data-stu-id="08491-160">100.00</span></span>            | <span data-ttu-id="08491-161">0,00</span><span class="sxs-lookup"><span data-stu-id="08491-161">0.00</span></span>              | <span data-ttu-id="08491-162">10 %</span><span class="sxs-lookup"><span data-stu-id="08491-162">10%</span></span>          |

<span data-ttu-id="08491-163">Die Mehrwertsteuer wird aus der Summe der Steuerbeträge gebildet, die für die einzelnen Betragsintervalle berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="08491-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="08491-164">Steuerpflichtiger Betrag (Preis)</span><span class="sxs-lookup"><span data-stu-id="08491-164">Taxable amount (price)</span></span> | <span data-ttu-id="08491-165">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="08491-165">Calculation</span></span>                                                               | <span data-ttu-id="08491-166">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="08491-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="08491-167">35,00</span><span class="sxs-lookup"><span data-stu-id="08491-167">35.00</span></span>                  | <span data-ttu-id="08491-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="08491-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="08491-169">10,50</span><span class="sxs-lookup"><span data-stu-id="08491-169">10.50</span></span>     |
| <span data-ttu-id="08491-170">50,00</span><span class="sxs-lookup"><span data-stu-id="08491-170">50.00</span></span>                  | <span data-ttu-id="08491-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="08491-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="08491-172">15:00</span><span class="sxs-lookup"><span data-stu-id="08491-172">15.00</span></span>     |
| <span data-ttu-id="08491-173">85,00</span><span class="sxs-lookup"><span data-stu-id="08491-173">85.00</span></span>                  | <span data-ttu-id="08491-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="08491-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="08491-175">22,00</span><span class="sxs-lookup"><span data-stu-id="08491-175">22.00</span></span>     |
| <span data-ttu-id="08491-176">305,00</span><span class="sxs-lookup"><span data-stu-id="08491-176">305.00</span></span>                 | <span data-ttu-id="08491-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="08491-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="08491-178">45.50</span><span class="sxs-lookup"><span data-stu-id="08491-178">45.50</span></span>     |



<span data-ttu-id="08491-179">Weitere Informationen finden Sie unter [Umsatzsätze auf Basis der Marginalbasis und Berechnungsmethoden](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="08491-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>





