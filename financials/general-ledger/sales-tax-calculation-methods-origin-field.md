---
title: Mehrwertsteuer-Berechnungsmethoden im Feld "Ursprung"
description: "In diesem Artikel wird beschrieben die Optionen im Feld \"Ursprung\" auf der Mehrwertsteuercodeseite und wie Mehrwertsteuer basierend auf der ausgewählten Option für einen Mehrwertsteuercode berechnet wird."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: f5683b8b3e5457a05e5039876eed40357ae84e4b
ms.contentlocale: de-de
ms.lasthandoff: 07/18/2017

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="4ce3c-103">Mehrwertsteuer-Berechnungsmethoden im Feld "Ursprung"</span><span class="sxs-lookup"><span data-stu-id="4ce3c-103">Sales tax calculation methods in the Origin field</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="4ce3c-104">In diesem Artikel wird beschrieben die Optionen im Feld "Ursprung" auf der Mehrwertsteuercodeseite und wie Mehrwertsteuer basierend auf der ausgewählten Option für einen Mehrwertsteuercode berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="4ce3c-105">Für jeden Mehrwertsteuercode, der auf der Seite "Mehrwertsteuercodes" erstellt wird, wählen Sie im Feld "Ursprung" die Berechnungsmethode aus, die auf den Steuergrundbetrag angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="4ce3c-106">Prozentanteil am Nettobetrag</span><span class="sxs-lookup"><span data-stu-id="4ce3c-106">Percentage of net amount</span></span>
<span data-ttu-id="4ce3c-107">Die Berechnungsmethode "Prozentanteil am Nettobetrag" ist der Standardwert im Feld "Ursprung".</span><span class="sxs-lookup"><span data-stu-id="4ce3c-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="4ce3c-108">Hierbei wird die Mehrwertsteuer als Prozentanteil der Einkaufs- oder Verkaufssumme ohne irgendwelche anderen Verkaufssteuern berechnet.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="4ce3c-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ce3c-109">Example</span></span>

<span data-ttu-id="4ce3c-110">Mehrwertsteuersatz = 25 %</span><span class="sxs-lookup"><span data-stu-id="4ce3c-110">The tax rate is 25%.</span></span> <span data-ttu-id="4ce3c-111">Unter der Rechnungsposition wird eine Menge von 10 Artikeln zu je 1,00 angezeigt, und der Debitor erhält einen Positionsrabatt von 10 %.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="4ce3c-112">Nettobetrag: (10 x 1,00) Mehrwertsteuer -10 % = 9,00: 9,00 x 25 % = 2,25 Gesamtbetrag: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="4ce3c-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="4ce3c-113"> Prozentanteil am Bruttobetrag</span><span class="sxs-lookup"><span data-stu-id="4ce3c-113">Percentage of gross amount</span></span>
<span data-ttu-id="4ce3c-114">Wenn Sie die Methode "Prozentanteil am Bruttobetrag" auswählen, wird die Mehrwertsteuer als Prozentanteil der Bruttoverkaufssumme berechnet.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="4ce3c-115">Der Bruttobetrag ist der Positionsnettobetrag einschließlich aller Steuern und Gebühren für die Position mit Ausnahme der Steuer mit Ursprung = Prozentanteil am Bruttobetrag.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="4ce3c-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ce3c-116">Example</span></span>

<span data-ttu-id="4ce3c-117">Die Steuerbehörde sieht für einen Artikel die Zahlung spezieller Abgaben vor.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="4ce3c-118">Der Abgabenbetrag wird zum Nettobetrag hinzuaddiert, bevor die Mehrwertsteuer berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="4ce3c-119">Folgende Mehrwertsteuercodes werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="4ce3c-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="4ce3c-120">ABGABE 1 = 10 %, mit Berechnungsmethode "Prozentanteil am Nettobetrag"</span><span class="sxs-lookup"><span data-stu-id="4ce3c-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="4ce3c-121">ABGABE 2 = 20 %, mit Berechnungsmethode "Prozentanteil am Nettobetrag"</span><span class="sxs-lookup"><span data-stu-id="4ce3c-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="4ce3c-122">MEHRWERTSTEUER = 25 %, mit Berechnungsmethode "Prozentanteil am Bruttobetrag"</span><span class="sxs-lookup"><span data-stu-id="4ce3c-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="4ce3c-123">Wenn der Nettobetrag 10,00 beträgt, dann ist ABGABE 1 "1,00 (10,00 x 10 %)" und ABGABE 2 "2,00 (10,00 x 20 %)".</span><span class="sxs-lookup"><span data-stu-id="4ce3c-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="4ce3c-124">Die Beträge wären wie folgt: Bruttobetrag: Nettobetrag + Betrag ABGABE 1 + Betrag ABGABE 2 (10,00 + 1,00 + 2,00) = 13,00 MEHRWERTSTEUER = 13,00 x 25 % = 3,25 gesamte ABGABEN und MEHRWERTSTEUER: 1,00 + 2,00 + 3,25 = 6,25 Gesamtbetrag: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="4ce3c-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>
| <span data-ttu-id="4ce3c-125">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="4ce3c-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce3c-126">Nur ein Steuercode mit Ursprung = "Prozentanteil des Bruttobetrags" kann für eine Buchung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="4ce3c-127">Wenn mehr als ein Steuercode für eine Buchung bestimmt wird, wird ein Fehler angezeigt, dass keine Steuer berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |

 
<a name="percentage-of-sales-tax"></a><span data-ttu-id="4ce3c-128">Mehrwertsteuer-Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="4ce3c-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="4ce3c-129">Wenn Sie im Feld "Ursprung" die Berechnungsmethode "Mehrwertsteuer-Prozentsatz" auswählen, wird die Mehrwertsteuer als Prozentsatz der im Feld "Mehrwertsteuer auf Mehrwertsteuer" ausgewählten Mehrwertsteuer berechnet.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="4ce3c-130">Die im Feld "Mehrwertsteuer auf Mehrwertsteuer" ausgewählte Mehrwertsteuer wird zuerst berechnet.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="4ce3c-131">Die zweite Mehrwertsteuer wird anschließend auf Basis des ersten Mehrwertsteuerbetrags berechnet.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="4ce3c-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ce3c-132">Example</span></span>

<span data-ttu-id="4ce3c-133">Folgende Mehrwertsteuercodes werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="4ce3c-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="4ce3c-134">ABGABE 1 = 10 %, mit Methode "Prozentanteil am Nettobetrag"</span><span class="sxs-lookup"><span data-stu-id="4ce3c-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="4ce3c-135">ABGABE 2 = 20 %, mithilfe der Methode "Mehrwertsteuer-Prozentsatz" und mit Abgabe 1 im Feld "Mehrwertsteuer auf Mehrwertsteuer"</span><span class="sxs-lookup"><span data-stu-id="4ce3c-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="4ce3c-136">MEHRWERTSTEUER = 25 %, mit Methode "Prozentanteil am Bruttobetrag"</span><span class="sxs-lookup"><span data-stu-id="4ce3c-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="4ce3c-137">Nettobetrag: 10,00 ABGABE 1: 10,00 x 10 % = 1,00 ABGABE 2: 1,00 x 20 % = 0,20 Bruttobetrag: 10,00 + 1,00 + 0,20 = 11,20 MEHRWERTSTEUER: 11,20 x 25 % = 2,80 ABGABE und MEHRWERTSTEUER gesamt: 1,00 + 0,20 + 2,80 = 4,00 Gesamtbetrag: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="4ce3c-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>
| <span data-ttu-id="4ce3c-138">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="4ce3c-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce3c-139">Mehrstufige Berechnungen für Steuer auf Steuer sind nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="4ce3c-140">Eine Steuer kann nicht basierend auf einer Steuer berechnet werden, die bereits auf Basis einer anderen Steuer berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="4ce3c-141">Mehrere einstufige "Steuer auf Steuer"-Codes können für eine Buchung berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="4ce3c-142"> Betrag pro Einheit</span><span class="sxs-lookup"><span data-stu-id="4ce3c-142">Amount per unit</span></span>
<span data-ttu-id="4ce3c-143">Wenn Sie "Betrag pro Einheit" im Feld "Ursprung" auswählen, wird die Mehrwertsteuer als fester Betrag pro Einheit multipliziert mit der Menge berechnet, die für die Dokumentposition eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="4ce3c-144">Eine Einheit muss im Feld "Einheit" ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="4ce3c-145">Der Betrag pro Einheit wird auf der Seite "Mehrwertsteuer-Codewerte" angegeben.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="4ce3c-146">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ce3c-146">Example</span></span>

<span data-ttu-id="4ce3c-147">Der Mehrwertsteuercode wird folgendermaßen eingerichtet: EUR 1,20 pro Einheit = Schachtel, bei einer Verkaufsrechnungsposition von 25 Schachteln eines verkauften Artikels wird die Verkaufsmehrwertsteuer berechnet als 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="4ce3c-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>
| <span data-ttu-id="4ce3c-148">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="4ce3c-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce3c-149">Wenn die Buchung in einer anderen Einheit eingegeben wurde als die im Mehrwertsteuercode angegebene, wird sie automatisch basierend auf der Einheitenumrechnung umgewandelt, die auf der Seite "Einheitenumrechnungen" eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="4ce3c-150"> Berechnungsmethode "Betrag pro Einheit", zusätzliche Option</span><span class="sxs-lookup"><span data-stu-id="4ce3c-150">Amount per unit, additional option</span></span>

<span data-ttu-id="4ce3c-151">Auf der Registerkarte "Berechnung" können Sie auswählen, ob ein berechneter Steuerbetrag pro Einheit vor einem anderen Steuercode berechnet und zum Nettobetrag hinzuaddiert wird, bevor andere Steuercodes mit Ursprung = "Prozentanteil am Nettobetrag" berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="4ce3c-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ce3c-152">Examples</span></span>

<span data-ttu-id="4ce3c-153">Wir gehen von der Berechnung von 2 Steuercodes in einer Buchung aus:</span><span class="sxs-lookup"><span data-stu-id="4ce3c-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="4ce3c-154">ABGABE: Ursprung = Betrag pro Einheit und Mehrwertsteuer, der Wert wird auf 5,00 pro Einheit = Stck. festgelegt</span><span class="sxs-lookup"><span data-stu-id="4ce3c-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="4ce3c-155">MEHRWERTSTEUER: Ursprung = (siehe Beispiele weiter unten, der Wert wird auf 25 % festgelegt</span><span class="sxs-lookup"><span data-stu-id="4ce3c-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="4ce3c-156">Wir verkaufen 1 Stück eines Artikels zu einem Einheitenpreis von 10,00</span><span class="sxs-lookup"><span data-stu-id="4ce3c-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="4ce3c-157">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ce3c-157">Example 1</span></span>

<span data-ttu-id="4ce3c-158">MEHRWERTSTEUER: Ursprung = Methode "Prozentanteil des Bruttobetrags", Option "Vor Mehrwertsteuer berechnen"hat keine Auswirkung, denn MEHRWERTSTEUER wird als Prozentanteil des Bruttobetrags berechnet.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="4ce3c-159">ANGABE: 1 x 5,00 = 5.00 Bruttobetrag: 10,00 + 5,00 = 15.00 MEHRWERTSTEUER: 15,00 x 25 % = 3,75 Mehrwertsteuer insgesamt: 5,00 + 3,75 = 8,75 Gesamtbetrag: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="4ce3c-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="4ce3c-160">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ce3c-160">Example 2</span></span>

<span data-ttu-id="4ce3c-161">MEHRWERTSTEUER: Ursprung = "Prozentanteil des Nettobetrags", Option "Vor Mehrwertsteuer berechnen" wird für die Berechnung der ABGABE nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="4ce3c-162">Nettobetrag: 10,00 ABGABE: 1 x 5,00 = 5,00 MEHRWERTSTEUER: 10,00 x 25 % = 2.50 Mehrwertsteuer gesamt: 5,00 + 2,50 = 7,50 Gesamtbetrag: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="4ce3c-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="4ce3c-163">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4ce3c-163">Example 3</span></span>

<span data-ttu-id="4ce3c-164">MEHRWERTSTEUER: Ursprung = "Prozentanteil des Nettobetrags", Option "Vor Mehrwertsteuer berechnen" wird für die Berechnung der ABGABE ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="4ce3c-165">Nettobetrag: 10,00 ABGABE: 1 x 5,00 = 5,00 MEHRWERTSTEUER: (10,00 + 5,00) x 25 % = 3.75 Mehrwertsteuer gesamt: 5,00 + 3,75 = 8,75 Gesamtbetrag: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="4ce3c-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="4ce3c-166">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="4ce3c-166">Example 4</span></span>

<span data-ttu-id="4ce3c-167">Die Ergebnisse von Beispiel 3 und Beispiel 1 sind gleich, da es nur eine Abgabe gibt.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="4ce3c-168">Angenommen, es gibt zwei ABGABEN, und nur eine davon wird in den Nettobetrag für die Mehrwertsteuerberechnung eingeschlossen: ABGABE 1: 5,00, mithilfe der Methode "Betrag pro Einheit" und ausgewählter Option "Vor Mehrwertsteuer berechnen"; ABGABE 2: 2,50, mithilfe der Methode "Betrag pro Einheit" und deaktivierter Option "Vor Mehrwertsteuer berechnen"; Mehrwertsteuer: 25 %, mithilfe der Methode "Prozentanteil am Nettobetrag"; Nettobetrag: 10,00 ABGABE 1: 1 x 5,00 = 5,00 ABGABE 2: 1 x 2,50 = 2,50 Nettobetrag für Mehrwertsteuer: 10,00 + 5,00 = 15,00 MEHRWERTSTEUER: 15,00 x 25 % = 3,75 Gesamtumsatzsteuern, einschließlich Abgaben: 5,00 + 2,50 + 3,75 = 11,25 Gesamtbetrag: 10,00 + 11,25 = 21,25 mit 25 % MEHRWERTSTEUER wird für die Summe aus dem Nettobetrag (10,00) + ABGABE 1 (5,00) = 15,00 berechnet.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="4ce3c-169">ABGABE 2 wird nach der Berechnung der Mehrwertsteuer zum Steuerbetrag hinzuaddiert.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="4ce3c-170"> Berechneter Prozentanteil am Nettobetrag</span><span class="sxs-lookup"><span data-stu-id="4ce3c-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="4ce3c-171">Die Methode "Berechneter Prozentanteil am Nettobetrag" berechnet die Steuer je nach den Einstellungen des Parameters "Beträge einschließlich Mehrwertsteuer" für das Dokument oder die Erfassung anders.</span><span class="sxs-lookup"><span data-stu-id="4ce3c-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="4ce3c-172">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ce3c-172">Example 1</span></span>

<span data-ttu-id="4ce3c-173">Dokument/Erfassung ist auf "Beträge einschließlich Mehrwertsteuer" festgelegt = Ja; Buchungspositionsbetrag: 10,00; Steuersatz: 25 % Mehrwertsteuer; Betrag des Steuersatzes der Buchungsposition x (10,00 x 25 %) = 2,50; Steuergrundlagenbetrag (Ursprungsbetrag): Buchungspositionsbetrag - Mehrwertsteuer (10,00 - 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="4ce3c-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="4ce3c-174">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ce3c-174">Example 2</span></span>

<span data-ttu-id="4ce3c-175">Dokument/Erfassung ist auf "Beträge einschließlich Mehrwertsteuer" festgelegt = Nein; Buchungspositionsbetrag: 10,00; Steuersatz: 25 % Mehrwertsteuer: (Betrag des Steuersatzes der Buchungsposition) / (100 - Steuersatz) (10,00 x 25 %) / (100 % - 25 %) = 3,33; Steuergrundlagenbetrag (Ursprungsbetrag): Buchungspositionsbetrag = 10,00</span><span class="sxs-lookup"><span data-stu-id="4ce3c-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="see-also"></a><span data-ttu-id="4ce3c-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ce3c-176">See also</span></span>
--------

[<span data-ttu-id="4ce3c-177">Bestimmen von Mehrwertsteuersteuersätzen auf Grundlage der Felder Berechnungsgrundlage und Berechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="4ce3c-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="4ce3c-178">Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes</span><span class="sxs-lookup"><span data-stu-id="4ce3c-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)




