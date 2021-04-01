---
title: Mehrwertsteuersteuersätze auf Grundlage der Felder Berechnungsgrundlage und Berechnungsmethode
description: In diesem Artikel wird beschrieben, wie die Werte in den Feldern "Berechnungsgrundlage und Berechnungsmethode" den Steuersatz in Verkaufs- und Einkaufsbuchungstransaktionen bestimmen.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a379a466317757f94b152fb256236fae2fc63e9c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248950"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="6e1eb-103">Mehrwertsteuersteuersätze auf Grundlage der Felder Berechnungsgrundlage und Berechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="6e1eb-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e1eb-104">In diesem Artikel wird beschrieben, wie die Werte in den Feldern "Berechnungsgrundlage und Berechnungsmethode" den Steuersatz in Verkaufs- und Einkaufsbuchungstransaktionen bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="6e1eb-105">Die Berechnungsgrundlage im Berechnungs-Inforegister auf der Mehrwertsteuercodeseite bestimmt, welcher Betrag verwendet wird, um den/die entsprechenden Steuersatz/‑sätze auf der Seite Mehrwertsteuercodewerte auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="6e1eb-106">Der Betragstyp im Feld "Berechnungsgrundlage" in Kombination mit der Methode im Feld Berechnungsmethode bestimmt die Logik, um den richtigen Steuersatz für eine Buchung zu finden.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="6e1eb-107">Aus unterschiedlichen Kombinationen von Werten in diesen Feldern ergeben sich verschiedene Mehrwertsteuerberechnungen, wie aus den folgenden Beispielen ersichtlich.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="6e1eb-108">In den Beispielen werden die gleichen Steuerintervallwerte verwendet, die für jeden Steuercode auf der Seite Mehrwertsteuercodewerte eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="6e1eb-109">Um diese Seite zu öffnen, klicken Sie auf Mehrwertsteuercode &gt; Werte in der Seite Mehrwertsteuercodes.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="6e1eb-110">Wenn die Berechnungsgrundlage für mindestens einen der Mehrwertsteuercodes auf Positionen oder Einheiten basiert, muss der Wert des Feldes Berechnungsmethode auf der Seite Hauptbuchparameter auf Position festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="6e1eb-111"> Nettobetrag pro Position</span><span class="sxs-lookup"><span data-stu-id="6e1eb-111">Net amount per line</span></span>
<span data-ttu-id="6e1eb-112">Wählen Sie diese Option, um die Mehrwertsteuer auf der Grundlage des Nettobetrags für die Rechnungspositionen ausschließlich sonstiger Steuern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="6e1eb-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e1eb-113">Example</span></span>

<span data-ttu-id="6e1eb-114">Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="6e1eb-115">Betragsintervall</span><span class="sxs-lookup"><span data-stu-id="6e1eb-115">Amount interval</span></span>    | <span data-ttu-id="6e1eb-116">Steuersatz</span><span class="sxs-lookup"><span data-stu-id="6e1eb-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="6e1eb-117">0 bis 50</span><span class="sxs-lookup"><span data-stu-id="6e1eb-117">0 - 50</span></span>             | <span data-ttu-id="6e1eb-118">30 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-118">30%</span></span>      |
| <span data-ttu-id="6e1eb-119">50 bis 100</span><span class="sxs-lookup"><span data-stu-id="6e1eb-119">50 - 100</span></span>           | <span data-ttu-id="6e1eb-120">20 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-120">20%</span></span>      |
| <span data-ttu-id="6e1eb-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="6e1eb-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="6e1eb-122">10 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="6e1eb-123">Die Null (0) für das obere Limit im letzten Intervall bedeutet, dass alle Beträge über 100 in das Intervall eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="6e1eb-124">Berechnungsgrundlage: **Menge pro Position**</span><span class="sxs-lookup"><span data-stu-id="6e1eb-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="6e1eb-125">Berechnungsmethode **Intervall**</span><span class="sxs-lookup"><span data-stu-id="6e1eb-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="6e1eb-126">Sie kaufen 8 Lampen für jeweils 25,00 Euro.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="6e1eb-127">Der Nettobetrag der Rechnungsposition ist 200,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="6e1eb-128">Die Steuer wird folgendermaßen berechnet:</span><span class="sxs-lookup"><span data-stu-id="6e1eb-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="6e1eb-129">Mehrwertsteuer gesamt = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="6e1eb-130">Rechnungsgesamtbetrag = 200,00 + 35,00 = 235,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="6e1eb-131">**Variante**</span><span class="sxs-lookup"><span data-stu-id="6e1eb-131">**Variation**</span></span> 

<span data-ttu-id="6e1eb-132">Wenn die Rechnung unter Verwendung von zwei Positionen mit 4 Artikeln in jeder Position erstellt wird, beträgt der Nettobetrag pro Position 100,00 und die Mehrwertsteuer wird folgendermaßen berechnet:</span><span class="sxs-lookup"><span data-stu-id="6e1eb-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="6e1eb-133">Mehrwertsteuerposition 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="6e1eb-134">Mehrwertsteuerposition 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="6e1eb-135">Mehrwertsteuer gesamt = 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="6e1eb-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="6e1eb-136">Rechnungsgesamtbetrag = 200,00 + 50,00 = 250,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="6e1eb-137"> Nettobetrag pro Einheit</span><span class="sxs-lookup"><span data-stu-id="6e1eb-137">Net amount per unit</span></span>
<span data-ttu-id="6e1eb-138">Wählen Sie diese Option aus, um die Mehrwertsteuer auf der Grundlage des Werts jeder Einheit ausschließlich sonstiger Steuern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="6e1eb-139">Wenn eine stückbasierte Berechnungsgrundlage ausgewählt wird, muss auch eine Einheit für den Mehrwertsteuercode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="6e1eb-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e1eb-140">Example</span></span>

<span data-ttu-id="6e1eb-141">Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="6e1eb-142">Betrag</span><span class="sxs-lookup"><span data-stu-id="6e1eb-142">Amount</span></span>             | <span data-ttu-id="6e1eb-143">Steuersatz</span><span class="sxs-lookup"><span data-stu-id="6e1eb-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="6e1eb-144">0 bis 50</span><span class="sxs-lookup"><span data-stu-id="6e1eb-144">0 - 50</span></span>             | <span data-ttu-id="6e1eb-145">30 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-145">30%</span></span>      |
| <span data-ttu-id="6e1eb-146">50 bis 100</span><span class="sxs-lookup"><span data-stu-id="6e1eb-146">50 - 100</span></span>           | <span data-ttu-id="6e1eb-147">20 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-147">20%</span></span>      |
| <span data-ttu-id="6e1eb-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="6e1eb-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="6e1eb-149">10 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-149">10%</span></span>      |

<span data-ttu-id="6e1eb-150">Berechnungsgrundlage: **Menge pro Einheit**</span><span class="sxs-lookup"><span data-stu-id="6e1eb-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="6e1eb-151">Berechnungsmethode "**Gesamtbetrag**"</span><span class="sxs-lookup"><span data-stu-id="6e1eb-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="6e1eb-152">Sie kaufen 8 Lampen für jeweils 25,00 Euro.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="6e1eb-153">Der Nettobetrag der Rechnungsposition ist 200,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="6e1eb-154">Die Steuer wird berechnet, wie folgt: Mehrwertsteuer pro Einheit = 25,00 x 30 % = 7,50 Euro; Gesamtumsatzsteuer = 7,50 x 8 Einheiten = 60,00 Euro; Rechnungsgesamtbetrag = 200,00 + 60,00 = 260,00 Euro</span><span class="sxs-lookup"><span data-stu-id="6e1eb-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="6e1eb-155"> Nettobetrag des Rechnungssaldos</span><span class="sxs-lookup"><span data-stu-id="6e1eb-155">Net amount of invoice balance</span></span>

<span data-ttu-id="6e1eb-156">Wählen Sie diese Option, um die Mehrwertsteuer auf der Grundlage des Gesamtwerts der Rechnung ausschließlich sonstiger Steuern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="6e1eb-157">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e1eb-157">Example</span></span>

<span data-ttu-id="6e1eb-158">Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="6e1eb-159">Betrag</span><span class="sxs-lookup"><span data-stu-id="6e1eb-159">Amount</span></span>            | <span data-ttu-id="6e1eb-160">Steuersatz</span><span class="sxs-lookup"><span data-stu-id="6e1eb-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="6e1eb-161">0 bis 50</span><span class="sxs-lookup"><span data-stu-id="6e1eb-161">0 - 50</span></span>            | <span data-ttu-id="6e1eb-162">30 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-162">30%</span></span>      |
| <span data-ttu-id="6e1eb-163">50 bis 100</span><span class="sxs-lookup"><span data-stu-id="6e1eb-163">50 - 100</span></span>          | <span data-ttu-id="6e1eb-164">20 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-164">20%</span></span>      |
| <span data-ttu-id="6e1eb-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="6e1eb-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="6e1eb-166">10 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-166">10%</span></span>      |

<span data-ttu-id="6e1eb-167">Berechnungsgrundlage: **Nettobetrag des Rechnungssaldos**</span><span class="sxs-lookup"><span data-stu-id="6e1eb-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="6e1eb-168">Berechnungsmethode: **Intervall** eine Verkaufsrechnung besitzt 2 Positionen mit 4 Lampen auf jedem Positionen für 25,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="6e1eb-169">Der Nettobetrag des Rechnungssaldos ist 4 x 25,00 + 4 x 25,00 = 200,00 Euro.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="6e1eb-170">Die Steuer wird berechnet, wie folgt: Gesamtumsatzsteuer = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Euro; Rechnungsgesamtbetrag = 200,00 + 35,00 = 235,00 Euro</span><span class="sxs-lookup"><span data-stu-id="6e1eb-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="6e1eb-171"> Bruttobetrag pro Position</span><span class="sxs-lookup"><span data-stu-id="6e1eb-171">Gross amount per line</span></span>

<span data-ttu-id="6e1eb-172">Wählen Sie diese Option, um die Mehrwertsteuer auf der Grundlage des Positionswerts einschließlich aller sonstigen Steuern für diese Position zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="6e1eb-173">In einer Mehrwertsteuergruppe darf nur ein Mehrwertsteuercode mit dieser Auswahl im Feld Berechnungsgrundlage vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="6e1eb-174">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e1eb-174">Example</span></span>

<span data-ttu-id="6e1eb-175">Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="6e1eb-176">Betrag</span><span class="sxs-lookup"><span data-stu-id="6e1eb-176">Amount</span></span>             | <span data-ttu-id="6e1eb-177">Steuersatz</span><span class="sxs-lookup"><span data-stu-id="6e1eb-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="6e1eb-178">0 bis 50</span><span class="sxs-lookup"><span data-stu-id="6e1eb-178">0 - 50</span></span>             | <span data-ttu-id="6e1eb-179">30 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-179">30%</span></span>      |
| <span data-ttu-id="6e1eb-180">50 bis 100</span><span class="sxs-lookup"><span data-stu-id="6e1eb-180">50 - 100</span></span>           | <span data-ttu-id="6e1eb-181">20 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-181">20%</span></span>      |
| <span data-ttu-id="6e1eb-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="6e1eb-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="6e1eb-183">10 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-183">10%</span></span>      |

<span data-ttu-id="6e1eb-184">Begrenzte Basis: **Bruttobetrag pro Position** Berechnungsmethode: **Intervall** Darüber hinaus gibt es einen weiteren Steuercode, der für eine spezielle Abgabe von 5,00 Euro auf jede Lampe berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="6e1eb-185">Die Abgabe wird vor der Berechnung der Mehrwertsteuer zum Nettobetrag hinzuaddiert.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="6e1eb-186">Sie kaufen 8 Lampen für jeweils 25,00 Euro.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="6e1eb-187">Der Nettobetrag der Rechnungsposition ist 200,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="6e1eb-188">Der Bruttobetrag für die Rechnungsposition ist 8 x 25,00 + 8 x 5,00 = 240,00 Euro.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="6e1eb-189">Die Steuer wird berechnet, wie folgt: Gesamtumsatzsteuer = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Euro; gesamte Abgabe = 5,00 x 8 = 40,00 Euro; Rechnungsgesamtbetrag = 200,00 + 39,00 + 40,00 = 279,00 Euro</span><span class="sxs-lookup"><span data-stu-id="6e1eb-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="6e1eb-190">**Variante**</span><span class="sxs-lookup"><span data-stu-id="6e1eb-190">**Variation**</span></span> 

<span data-ttu-id="6e1eb-191">Wenn die Rechnung unter Verwendung von zwei Rechnungspositionen mit 4 Artikeln in jeder Position erstellt wird, beträgt der Nettobetrag pro Rechnungsposition EUR 100.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="6e1eb-192">Der Bruttobetrag (einschließlich Abgaben von 4 x 5,00 Euro) pro Rechnungsposition wäre 120,00 Euro, und die Mehrwertsteuer wird erstellt, wie folgt: Mehrwertsteuerrechnungsposition 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Euro; Mehrwertsteuerrechnungsposition 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Euro; Gesamtumsatzsteuer = 27,00 + 27,00 = 54,00 Euro; gesamte Abgabe = 5,00 x 8 = 40,00 Euro; Rechnungsgesamtbetrag = 200,00 + 54,00 + 40,00 = 294,00 Euro</span><span class="sxs-lookup"><span data-stu-id="6e1eb-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="6e1eb-193"> Bruttobetrag pro Einheit</span><span class="sxs-lookup"><span data-stu-id="6e1eb-193">Gross amount per unit</span></span>

<span data-ttu-id="6e1eb-194">Wählen Sie diese Option aus, um die Mehrwertsteuer auf der Grundlage des Werts der Einheit einschließlich sonstiger Steuern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="6e1eb-195">In einer Mehrwertsteuergruppe darf nur ein Mehrwertsteuercode mit dieser Auswahl im Feld Berechnungsgrundlage vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="6e1eb-196">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e1eb-196">Example</span></span>

<span data-ttu-id="6e1eb-197">Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="6e1eb-198">Betrag</span><span class="sxs-lookup"><span data-stu-id="6e1eb-198">Amount</span></span>             | <span data-ttu-id="6e1eb-199">Steuersatz</span><span class="sxs-lookup"><span data-stu-id="6e1eb-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="6e1eb-200">0 bis 50</span><span class="sxs-lookup"><span data-stu-id="6e1eb-200">0 - 50</span></span>             | <span data-ttu-id="6e1eb-201">30 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-201">30%</span></span>      |
| <span data-ttu-id="6e1eb-202">50 bis 100</span><span class="sxs-lookup"><span data-stu-id="6e1eb-202">50 - 100</span></span>           | <span data-ttu-id="6e1eb-203">20 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-203">20%</span></span>      |
| <span data-ttu-id="6e1eb-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="6e1eb-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="6e1eb-205">10 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-205">10%</span></span>      |

<span data-ttu-id="6e1eb-206">Berechnungsgrundlage: **Bruttobetrag pro Einheit** Es gibt eine spezielle Abgabe von 5,00 Euro auf jede Lampe.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="6e1eb-207">Die Abgabe wird vor der Berechnung der Mehrwertsteuer zum Nettobetrag hinzuaddiert.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="6e1eb-208">Sie kaufen 8 Lampen für jeweils 25,00 Euro.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="6e1eb-209">Der Bruttobetrag pro Einheit ist 30,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="6e1eb-210">Die Steuer wird berechnet, wie folgt: Umsatzsteuer pro Einheit = 30 x 30 % = 9,00 Euro; Gesamtumsatzsteuer = 9,00 x 8 = 72,00 Euro; Gesamtabgabe = 5,00 x 8 = 40,00 Euro; Gesamtrechnungsbetrag = 200,00 + 72,00 + 40,00 = 312,00 Euro</span><span class="sxs-lookup"><span data-stu-id="6e1eb-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="6e1eb-211"> Rechnungssumme einschließlich sonstiger Mehrwertsteuerbeträge</span><span class="sxs-lookup"><span data-stu-id="6e1eb-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="6e1eb-212">Wählen Sie diese Option, um die Mehrwertsteuer auf der Grundlage des Gesamtwerts der Rechnung einschließlich sonstiger Steuern zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="6e1eb-213">In einer Mehrwertsteuergruppe darf nur ein Mehrwertsteuercode mit dieser Auswahl im Feld Berechnungsgrundlage vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="6e1eb-214">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e1eb-214">Example</span></span>

<span data-ttu-id="6e1eb-215">Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="6e1eb-216">Betrag</span><span class="sxs-lookup"><span data-stu-id="6e1eb-216">Amount</span></span>             | <span data-ttu-id="6e1eb-217">Steuersatz</span><span class="sxs-lookup"><span data-stu-id="6e1eb-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="6e1eb-218">0 bis 50</span><span class="sxs-lookup"><span data-stu-id="6e1eb-218">0 - 50</span></span>             | <span data-ttu-id="6e1eb-219">30 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-219">30%</span></span>      |
| <span data-ttu-id="6e1eb-220">50 bis 100</span><span class="sxs-lookup"><span data-stu-id="6e1eb-220">50 - 100</span></span>           | <span data-ttu-id="6e1eb-221">20 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-221">20%</span></span>      |
| <span data-ttu-id="6e1eb-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="6e1eb-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="6e1eb-223">10 %</span><span class="sxs-lookup"><span data-stu-id="6e1eb-223">10%</span></span>      |

<span data-ttu-id="6e1eb-224">Berechnungsgrundlage: **Rechnungssumme einschließlich sonstiger Mehrwertsteuerbeträge** Berechnungsmethode: **Intervall** </span><span class="sxs-lookup"><span data-stu-id="6e1eb-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="6e1eb-225">Für jede Lampe gilt eine spezielle Abgabe von 5,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="6e1eb-226">Die Abgabe wird vor der Berechnung der Mehrwertsteuer zum Nettobetrag hinzuaddiert.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="6e1eb-227">Sie kaufen 8 Lampen für jeweils 25,00 Euro.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="6e1eb-228">Der Nettobetrag der Rechnung ist 200,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="6e1eb-229">Der Bruttobetrag der Rechnung ist 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="6e1eb-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="6e1eb-230">Die Steuer wird berechnet, wie folgt: Gesamtumsatzsteuer = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Euro; gesamte Abgabe = 5,00 x 8 = 40,00 Euro; Rechnungsgesamtbetrag = 200,00 + 39,00 + 40,00 = 279,00 Euro</span><span class="sxs-lookup"><span data-stu-id="6e1eb-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="6e1eb-231">Weitere Informationen unter [Optionen für Gesamtbetrags- und Intervalloptionen für Verkaufssteuercodes](whole-amount-interval-options-sales-tax-codes.md) und [Verkaufssteuerkalkulationsmethode im Ursprungsfeld](sales-tax-calculation-methods-origin-field.md)</span><span class="sxs-lookup"><span data-stu-id="6e1eb-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]