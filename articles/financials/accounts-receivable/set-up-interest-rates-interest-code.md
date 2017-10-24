---
title: "Einrichten von Zinssätzen für einen Zinscode"
description: "Zinscodes enthalten Einstellungen, die festlegen, wann Zinsen erhoben werden und wie Zinsen für fällige Rechnungen berechnet werden."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59acfaa93b1352f2be6d750dea6bdd740bac0312
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="0fb58-103">Einrichten von Zinssätzen für einen Zinscode</span><span class="sxs-lookup"><span data-stu-id="0fb58-103">Set up interest rates for an interest code</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0fb58-104">Zinscodes enthalten Einstellungen, die festlegen, wann Zinsen erhoben werden und wie Zinsen für fällige Rechnungen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb58-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="0fb58-105">Sie können einen einzelnen Zinscode einrichten und diesen auf mehrere Debitorenbuchungsprofile, Abrechnungscodes  oder auf bestimmte Rechnungspositionen anwenden.</span><span class="sxs-lookup"><span data-stu-id="0fb58-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="0fb58-106">Wenn die Details des Zinscodes geändert werden, werden diese Änderungen für alle Funktionen, in denen dieser Code verwendet wird, automatisch bei neuen Buchungen übernommen.</span><span class="sxs-lookup"><span data-stu-id="0fb58-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="0fb58-107">Für jeden Zinscode können Sie zwei Typen von Sätzen einrichten:</span><span class="sxs-lookup"><span data-stu-id="0fb58-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="0fb58-108">Sätze für Zinserträge − diese stellen Umsatzerlöse dar, die durch die Berechnung von Zinsen auf Rechnungen oder Zinsrechnungen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="0fb58-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="0fb58-109">Sätze für die Zinszahlungen − diese stellen Kosten dar, die für Zinsen auf Gutschriften bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="0fb58-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="0fb58-110">Beide Satztypen können im gleichen Zinscode gleichzeitig vorhanden ein.</span><span class="sxs-lookup"><span data-stu-id="0fb58-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="0fb58-111">Zinssätze können auf drei Berechnungstypen basieren:</span><span class="sxs-lookup"><span data-stu-id="0fb58-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="0fb58-112">Zinsen nach Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="0fb58-112">Interest by percentage.</span></span>
-   <span data-ttu-id="0fb58-113">Zinsen nach Betrag.</span><span class="sxs-lookup"><span data-stu-id="0fb58-113">Interest by amount.</span></span>
-   <span data-ttu-id="0fb58-114">Zinsen nach Bereich, was zu einem einzelnen Prozentsatz oder Betrag führt.</span><span class="sxs-lookup"><span data-stu-id="0fb58-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="0fb58-115">Bei der Berechnung der Zinsen mit einem Zinscode, wird für jeden Zinssatz, der für den Zeitraum gilt, in dem die Zahlung das Buchungsfälligkeitsdatum überschritten hat, eine separate Zinsrechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb58-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="0fb58-116">Verwenden Sie die **Einnahmen**-Registerkarte auf der **Zinscode**-Seite, um Zinssätze für Zinsen einzurichten, die Sie über Zinsen erzielen.</span><span class="sxs-lookup"><span data-stu-id="0fb58-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="0fb58-117">Um Zinssätze für Zinsen einzurichten, die Sie zahlen, verwenden Sie stattdessen die Registerkarte **Zahlungen**.</span><span class="sxs-lookup"><span data-stu-id="0fb58-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="0fb58-118">Zinssätzen auf der Basis von Prozentsätzen</span><span class="sxs-lookup"><span data-stu-id="0fb58-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="0fb58-119">Sie können Zinssätze einrichten, die einen angegebenen Prozentsatz berechnen.</span><span class="sxs-lookup"><span data-stu-id="0fb58-119">You can set up interest rates that calculate a specified percentage.</span></span>

-   <span data-ttu-id="0fb58-120">Der Zinsbetrag gilt für alle Währungen.</span><span class="sxs-lookup"><span data-stu-id="0fb58-120">Interest amount applies to all currencies.</span></span>
-   <span data-ttu-id="0fb58-121">Es können optional Zinsbetraggrenzen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0fb58-121">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="0fb58-122">Der **Prozentsatz** wird im Feld **Grundlage für Zinsberechnung** auf der Seite **Einrichten von Zinscodes** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="0fb58-122">**Percentage** is selected** **in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="0fb58-123">Um beispielsweise einen Zinscode einzurichten, der Zinsen in Höhe von 5 Prozent für alle 2 Monate festlegt die die Rechnungszahlung das Fälligkeitsdatum überschreitet, geben Sie 2 im Feld **Zinsen berechnen alle** ein wählen Sie **Monat** aus.</span><span class="sxs-lookup"><span data-stu-id="0fb58-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="0fb58-124">Zinssätzen auf der Basis von Beträgen</span><span class="sxs-lookup"><span data-stu-id="0fb58-124">Interest rates based on amounts</span></span>
<span data-ttu-id="0fb58-125">Sie können Zinssätze einrichten, die einen angegebenen Betrag pro Währung berechnen.</span><span class="sxs-lookup"><span data-stu-id="0fb58-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
-   <span data-ttu-id="0fb58-126">Für jede Währung wird im Zinscode ein Zinsbetrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="0fb58-126">An interest amount is specified for each currency in the interest code.</span></span>
-   <span data-ttu-id="0fb58-127">Es können optional Zinsbetraggrenzen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0fb58-127">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="0fb58-128">Der **Betrag** wird im Feld **Grundlage für Zinsberechnung** auf der Seite **Einrichten von Zinscodes** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="0fb58-128">**Amount **is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="0fb58-129">Um beispielsweise einen Zinscode einzurichten, der Zinsen in Höhe von 25,00 für alle 20 Tage festlegt die die Rechnungszahlung das Fälligkeitsdatum überschreitet, geben Sie 20 im Feld **Zinsen berechnen alle** ein wählen Sie **Tag** aus.</span><span class="sxs-lookup"><span data-stu-id="0fb58-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="0fb58-130">Zinssätzen auf der Basis von Bereichen</span><span class="sxs-lookup"><span data-stu-id="0fb58-130">Interest rates based on ranges</span></span>
<span data-ttu-id="0fb58-131">Sie können Zinssätze einrichten, die je nach überfälligem Betrag, der Anzahl der Überfälligkeitstage oder der Anzahl der Überfälligkeitsmonate variieren.</span><span class="sxs-lookup"><span data-stu-id="0fb58-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="0fb58-132">Sie können die Registerkarte **Einnahmen nach Währung** verwenden, um bestimmte Zinseneinstellungen für jede Währung festlegen.</span><span class="sxs-lookup"><span data-stu-id="0fb58-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="0fb58-133">Hier definieren Sie auch den Bereich.</span><span class="sxs-lookup"><span data-stu-id="0fb58-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="0fb58-134">Verwenden Sie die **Bereiche** Schaltfläche, um Positionen hinzuzufügen, die die Bereiche darstellen, die Sie einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="0fb58-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="0fb58-135">Der **Von**-Wert stellt den Beginn des Zeitraums dar und die **Zinswert** repräsentiert entweder einen Prozentsatz oder einen Betrag, abhängig von der Auswahl im **Grundlage für Zinsberechnung**-Feld auf der **Einrichten von Zinscodes**-Seite.</span><span class="sxs-lookup"><span data-stu-id="0fb58-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="0fb58-136">Beispiel 1: Zinsen nach Bereich = Betrag</span><span class="sxs-lookup"><span data-stu-id="0fb58-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="0fb58-137">Sie richten einen Zinscode ein, der Zinsen einmal für alle drei Monate, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt.</span><span class="sxs-lookup"><span data-stu-id="0fb58-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="0fb58-138">Sie möchten die Berechnung auf einem Prozentsatzzinsenwert basieren, gemäß bestimmten Betragsschritten.</span><span class="sxs-lookup"><span data-stu-id="0fb58-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="0fb58-139">Der Zinsenwert beträgt 1 Prozent für Rechnungsbeträge bis 1.000,00, 2 Prozent für Beträge von 1.001,00 bis 5.000,00 und 3 Prozent für die Beträge, die größer 5.000,00 sind.</span><span class="sxs-lookup"><span data-stu-id="0fb58-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="0fb58-140">Sie richten die Zinscodefeldwerte wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="0fb58-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="0fb58-141">**Feldname**</span><span class="sxs-lookup"><span data-stu-id="0fb58-141">**Field name**</span></span>                  | <span data-ttu-id="0fb58-142">**Feldwert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="0fb58-143">**Zinscode**</span><span class="sxs-lookup"><span data-stu-id="0fb58-143">**Interest code**</span></span>               | <span data-ttu-id="0fb58-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="0fb58-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="0fb58-145">**Zinsen berechnen alle**</span><span class="sxs-lookup"><span data-stu-id="0fb58-145">**Calculate interest every**</span></span>    | <span data-ttu-id="0fb58-146">3/Monat</span><span class="sxs-lookup"><span data-stu-id="0fb58-146">3/Month</span></span>         |
| <span data-ttu-id="0fb58-147">**Zinsen nach Bereich**</span><span class="sxs-lookup"><span data-stu-id="0fb58-147">**Interest by range**</span></span>           | <span data-ttu-id="0fb58-148">Betrag</span><span class="sxs-lookup"><span data-stu-id="0fb58-148">Amount</span></span>          |
| <span data-ttu-id="0fb58-149">**Grundlage für Zinsberechnung**</span><span class="sxs-lookup"><span data-stu-id="0fb58-149">**Calculate interest based on**</span></span> | <span data-ttu-id="0fb58-150">Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="0fb58-150">Percentage</span></span>      |

<span data-ttu-id="0fb58-151">Sie richten die Bereichsinformationen wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="0fb58-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="0fb58-152">**Von Wert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-152">**From value**</span></span> | <span data-ttu-id="0fb58-153">**Zinswert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="0fb58-154">0</span><span class="sxs-lookup"><span data-stu-id="0fb58-154">0</span></span>              | <span data-ttu-id="0fb58-155">1</span><span class="sxs-lookup"><span data-stu-id="0fb58-155">1</span></span>                  |
| <span data-ttu-id="0fb58-156">1,001</span><span class="sxs-lookup"><span data-stu-id="0fb58-156">1,001</span></span>          | <span data-ttu-id="0fb58-157">2</span><span class="sxs-lookup"><span data-stu-id="0fb58-157">2</span></span>                  |
| <span data-ttu-id="0fb58-158">5,001</span><span class="sxs-lookup"><span data-stu-id="0fb58-158">5,001</span></span>          | <span data-ttu-id="0fb58-159">3</span><span class="sxs-lookup"><span data-stu-id="0fb58-159">3</span></span>                  |

 
## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="0fb58-160">Beispiel 2: Zinsen nach Bereich = Tage</span><span class="sxs-lookup"><span data-stu-id="0fb58-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="0fb58-161">Sie richten einen Zinscode ein, der Zinsen einmal für alle 15 Tage, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt.</span><span class="sxs-lookup"><span data-stu-id="0fb58-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="0fb58-162">Sie möchten die Berechnung auf einem Zinsbetragswert basieren, gemäß bestimmten Tagesschritten.</span><span class="sxs-lookup"><span data-stu-id="0fb58-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="0fb58-163">Der Zinsenwert ist 10,00 pro 15 Tage für die ersten 60 Tage, 15,00 pro 15 Tage für die Tage 61 bis 90 und 20,00 pro 15 Tagen nach Tag 91.</span><span class="sxs-lookup"><span data-stu-id="0fb58-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="0fb58-164">Sie richten die Zinscodefeldwerte wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="0fb58-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="0fb58-165">**Feldname**</span><span class="sxs-lookup"><span data-stu-id="0fb58-165">**Field name**</span></span>                  | <span data-ttu-id="0fb58-166">**Feldwert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="0fb58-167">**Zinscode**</span><span class="sxs-lookup"><span data-stu-id="0fb58-167">**Interest code**</span></span>               | <span data-ttu-id="0fb58-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="0fb58-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="0fb58-169">**Zinsen berechnen alle**</span><span class="sxs-lookup"><span data-stu-id="0fb58-169">**Calculate interest every**</span></span>    | <span data-ttu-id="0fb58-170">15/Tag</span><span class="sxs-lookup"><span data-stu-id="0fb58-170">15/Day</span></span>          |
| <span data-ttu-id="0fb58-171">**Zinsen nach Bereich**</span><span class="sxs-lookup"><span data-stu-id="0fb58-171">**Interest by range**</span></span>           | <span data-ttu-id="0fb58-172">Tage</span><span class="sxs-lookup"><span data-stu-id="0fb58-172">Days</span></span>            |
| <span data-ttu-id="0fb58-173">**Grundlage für Zinsberechnung**</span><span class="sxs-lookup"><span data-stu-id="0fb58-173">**Calculate interest based on**</span></span> | <span data-ttu-id="0fb58-174">Betrag</span><span class="sxs-lookup"><span data-stu-id="0fb58-174">Amount</span></span>          |

<span data-ttu-id="0fb58-175">Sie richten die Bereichsinformationen wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="0fb58-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="0fb58-176">**Von Wert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-176">**From value**</span></span> | <span data-ttu-id="0fb58-177">**Zinswert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="0fb58-178">0</span><span class="sxs-lookup"><span data-stu-id="0fb58-178">0</span></span>              | <span data-ttu-id="0fb58-179">10</span><span class="sxs-lookup"><span data-stu-id="0fb58-179">10</span></span>                 |
| <span data-ttu-id="0fb58-180">61</span><span class="sxs-lookup"><span data-stu-id="0fb58-180">61</span></span>             | <span data-ttu-id="0fb58-181">15</span><span class="sxs-lookup"><span data-stu-id="0fb58-181">15</span></span>                 |
| <span data-ttu-id="0fb58-182">91</span><span class="sxs-lookup"><span data-stu-id="0fb58-182">91</span></span>             | <span data-ttu-id="0fb58-183">20</span><span class="sxs-lookup"><span data-stu-id="0fb58-183">20</span></span>                 |

 
## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="0fb58-184">Beispiel 3: Zinsen nach Bereich = Monate</span><span class="sxs-lookup"><span data-stu-id="0fb58-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="0fb58-185">Sie richten einen Zinscode ein, der Zinsen einmal für jeden Monat, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt.</span><span class="sxs-lookup"><span data-stu-id="0fb58-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="0fb58-186">Sie möchten die Berechnung auf einem Prozentsatzzinsenwert basieren, gemäß bestimmten Monatsschritten.</span><span class="sxs-lookup"><span data-stu-id="0fb58-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="0fb58-187">Der Zinsenwert beträgt 1,5 Prozent pro Monat für die ersten drei Monate Überfälligkeit, 2,0 Prozent pro Monat für die zweiten drei Monate und 2,5 Prozent pro Monat für jeden Monat nach den ersten sechs Monaten.</span><span class="sxs-lookup"><span data-stu-id="0fb58-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="0fb58-188">Sie richten die Zinscodefeldwerte wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="0fb58-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="0fb58-189">**Feldname**</span><span class="sxs-lookup"><span data-stu-id="0fb58-189">**Field name**</span></span>                  | <span data-ttu-id="0fb58-190">**Feldwert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="0fb58-191">**Zinscode**</span><span class="sxs-lookup"><span data-stu-id="0fb58-191">**Interest code**</span></span>               | <span data-ttu-id="0fb58-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="0fb58-192">1M%ByMth</span></span>        |
| <span data-ttu-id="0fb58-193">**Zinsen berechnen alle**</span><span class="sxs-lookup"><span data-stu-id="0fb58-193">**Calculate interest every**</span></span>    | <span data-ttu-id="0fb58-194">1/Monat</span><span class="sxs-lookup"><span data-stu-id="0fb58-194">1/Month</span></span>         |
| <span data-ttu-id="0fb58-195">**Zinsen nach Bereich**</span><span class="sxs-lookup"><span data-stu-id="0fb58-195">**Interest by range**</span></span>           | <span data-ttu-id="0fb58-196">Monate</span><span class="sxs-lookup"><span data-stu-id="0fb58-196">Months</span></span>          |
| <span data-ttu-id="0fb58-197">**Grundlage für Zinsberechnung**</span><span class="sxs-lookup"><span data-stu-id="0fb58-197">**Calculate interest based on**</span></span> | <span data-ttu-id="0fb58-198">Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="0fb58-198">Percentage</span></span>      |

<span data-ttu-id="0fb58-199">Sie richten die Bereichsinformationen wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="0fb58-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="0fb58-200">**Von Wert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-200">**From value**</span></span> | <span data-ttu-id="0fb58-201">**Zinswert**</span><span class="sxs-lookup"><span data-stu-id="0fb58-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="0fb58-202">0</span><span class="sxs-lookup"><span data-stu-id="0fb58-202">0</span></span>              | <span data-ttu-id="0fb58-203">1.5</span><span class="sxs-lookup"><span data-stu-id="0fb58-203">1.5</span></span>                |
| <span data-ttu-id="0fb58-204">4</span><span class="sxs-lookup"><span data-stu-id="0fb58-204">4</span></span>              | <span data-ttu-id="0fb58-205">2</span><span class="sxs-lookup"><span data-stu-id="0fb58-205">2</span></span>                  |
| <span data-ttu-id="0fb58-206">7</span><span class="sxs-lookup"><span data-stu-id="0fb58-206">7</span></span>              | <span data-ttu-id="0fb58-207">2,5</span><span class="sxs-lookup"><span data-stu-id="0fb58-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="0fb58-208">Neue Versionen</span><span class="sxs-lookup"><span data-stu-id="0fb58-208">New versions</span></span>
<span data-ttu-id="0fb58-209">Zinscodes sind ein Gültigkeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="0fb58-209">Interest codes are date effective.</span></span> <span data-ttu-id="0fb58-210">Wenn Sie den Zinssatz ändern möchten, können Sie eine **neue Version** mit einem zukünftigen Gültigkeitsdatum erstellten.</span><span class="sxs-lookup"><span data-stu-id="0fb58-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="0fb58-211">Um die verschiedenen Versionen anzeigen, können Sie die Menüauswahl **Anfangsdatum.** verwenden, um das Abschnittsdatum auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0fb58-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="0fb58-212">Sie können auch **Alle Datensätze anzeigen** auswählen, um alle Zinscodes auf der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0fb58-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>




