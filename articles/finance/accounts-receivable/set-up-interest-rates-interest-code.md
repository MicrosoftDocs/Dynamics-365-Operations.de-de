---
title: Einrichten von Zinssätzen für einen Zinscode
description: Zinscodes enthalten Einstellungen, die festlegen, wann Zinsen erhoben werden und wie Zinsen für fällige Rechnungen berechnet werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d9ff856e34eb894c5d0ab5fe17c8e95f62fff57
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555364"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="8057f-103">Einrichten von Zinssätzen für einen Zinscode</span><span class="sxs-lookup"><span data-stu-id="8057f-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8057f-104">Zinscodes enthalten Einstellungen, die festlegen, wann Zinsen erhoben werden und wie Zinsen für fällige Rechnungen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="8057f-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="8057f-105">Sie können einen einzelnen Zinscode einrichten und diesen auf mehrere Debitorenbuchungsprofile, Abrechnungscodes  oder auf bestimmte Rechnungspositionen anwenden.</span><span class="sxs-lookup"><span data-stu-id="8057f-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="8057f-106">Wenn die Details des Zinscodes geändert werden, werden diese Änderungen für alle Funktionen, in denen dieser Code verwendet wird, automatisch bei neuen Buchungen übernommen.</span><span class="sxs-lookup"><span data-stu-id="8057f-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="8057f-107">Für jeden Zinscode können Sie zwei Typen von Sätzen einrichten:</span><span class="sxs-lookup"><span data-stu-id="8057f-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="8057f-108">Sätze für Zinserträge − diese stellen Umsatzerlöse dar, die durch die Berechnung von Zinsen auf Rechnungen oder Zinsrechnungen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="8057f-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="8057f-109">Sätze für die Zinszahlungen − diese stellen Kosten dar, die für Zinsen auf Gutschriften bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="8057f-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="8057f-110">Beide Satztypen können im gleichen Zinscode gleichzeitig vorhanden ein.</span><span class="sxs-lookup"><span data-stu-id="8057f-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="8057f-111">Zinssätze können auf drei Berechnungstypen basieren:</span><span class="sxs-lookup"><span data-stu-id="8057f-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="8057f-112">Zinsen nach Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="8057f-112">Interest by percentage.</span></span>
-   <span data-ttu-id="8057f-113">Zinsen nach Betrag.</span><span class="sxs-lookup"><span data-stu-id="8057f-113">Interest by amount.</span></span>
-   <span data-ttu-id="8057f-114">Zinsen nach Bereich, was zu einem einzelnen Prozentsatz oder Betrag führt.</span><span class="sxs-lookup"><span data-stu-id="8057f-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="8057f-115">Bei der Berechnung der Zinsen mit einem Zinscode, wird für jeden Zinssatz, der für den Zeitraum gilt, in dem die Zahlung das Buchungsfälligkeitsdatum überschritten hat, eine separate Zinsrechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="8057f-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="8057f-116">Verwenden Sie die **Einnahmen**-Registerkarte auf der **Zinscode**-Seite, um Zinssätze für Zinsen einzurichten, die Sie über Zinsen erzielen.</span><span class="sxs-lookup"><span data-stu-id="8057f-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="8057f-117">Um Zinssätze für Zinsen einzurichten, die Sie zahlen, verwenden Sie stattdessen die Registerkarte **Zahlungen**.</span><span class="sxs-lookup"><span data-stu-id="8057f-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="8057f-118">Zinssätzen auf der Basis von Prozentsätzen</span><span class="sxs-lookup"><span data-stu-id="8057f-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="8057f-119">Sie können Zinssätze einrichten, die einen angegebenen Prozentsatz berechnen.</span><span class="sxs-lookup"><span data-stu-id="8057f-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="8057f-120">Der Zinsbetrag gilt für alle Währungen.</span><span class="sxs-lookup"><span data-stu-id="8057f-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="8057f-121">Es können optional Zinsbetraggrenzen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8057f-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="8057f-122">Der **Prozentsatz** wird im Feld **Grundlage für Zinsberechnung** auf der Seite **Zinscodes einrichten** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8057f-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="8057f-123">Um beispielsweise einen Zinscode einzurichten, der Zinsen in Höhe von 5 Prozent für alle 2 Monate festlegt die die Rechnungszahlung das Fälligkeitsdatum überschreitet, geben Sie 2 im Feld **Zinsen berechnen alle** ein wählen Sie **Monat** aus.</span><span class="sxs-lookup"><span data-stu-id="8057f-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="8057f-124">Der neue Algorithmus zur Berechnung der Zinsrechnung wird mithilfe der Funktionsverwaltung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8057f-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="8057f-125">Aktivieren Sie zur Verwendung dieses Algorithmus die Funktion **(GBL) Berechnung der Zinsen pro Tag als jährlichen Prozentsatz geteilt durch 365 zulassen**.</span><span class="sxs-lookup"><span data-stu-id="8057f-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="8057f-126">Informationen zur Aktivierung der Funktionen finden Sie unter [Funktionsverwaltungsüberblick](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8057f-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="8057f-127">Die Formel zur Berechnung des Zinsrechnungsbetrags lautet:</span><span class="sxs-lookup"><span data-stu-id="8057f-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="8057f-128">Zinsrechnungsbetrag = geschuldeter Betrag \* jährliche Zinsen % / 365 \* Anzahl der verspäteten Tage</span><span class="sxs-lookup"><span data-stu-id="8057f-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="8057f-129">Diese Funktion ist ab Version 10.0.18 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8057f-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="8057f-130">Zinssätzen auf der Basis von Beträgen</span><span class="sxs-lookup"><span data-stu-id="8057f-130">Interest rates based on amounts</span></span>
<span data-ttu-id="8057f-131">Sie können Zinssätze einrichten, die einen angegebenen Betrag pro Währung berechnen.</span><span class="sxs-lookup"><span data-stu-id="8057f-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="8057f-132">Für jede Währung wird im Zinscode ein Zinsbetrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="8057f-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="8057f-133">Es können optional Zinsbetraggrenzen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8057f-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="8057f-134">Der **Betrag** wird im Feld **Grundlage für Zinsberechnung** auf der Seite **Einrichten von Zinscodes** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8057f-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="8057f-135">Um beispielsweise einen Zinscode einzurichten, der Zinsen in Höhe von 25,00 für alle 20 Tage festlegt die die Rechnungszahlung das Fälligkeitsdatum überschreitet, geben Sie 20 im Feld **Zinsen berechnen alle** ein wählen Sie **Tag** aus.</span><span class="sxs-lookup"><span data-stu-id="8057f-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="8057f-136">Zinssätzen auf der Basis von Bereichen</span><span class="sxs-lookup"><span data-stu-id="8057f-136">Interest rates based on ranges</span></span>
<span data-ttu-id="8057f-137">Sie können Zinssätze einrichten, die je nach überfälligem Betrag, der Anzahl der Überfälligkeitstage oder der Anzahl der Überfälligkeitsmonate variieren.</span><span class="sxs-lookup"><span data-stu-id="8057f-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="8057f-138">Sie können die Registerkarte **Einnahmen nach Währung** verwenden, um bestimmte Zinseneinstellungen für jede Währung festlegen.</span><span class="sxs-lookup"><span data-stu-id="8057f-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="8057f-139">Hier definieren Sie auch den Bereich.</span><span class="sxs-lookup"><span data-stu-id="8057f-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="8057f-140">Verwenden Sie die **Bereiche** Schaltfläche, um Positionen hinzuzufügen, die die Bereiche darstellen, die Sie einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="8057f-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="8057f-141">Der **Von**-Wert stellt den Beginn des Zeitraums dar und die **Zinswert** repräsentiert entweder einen Prozentsatz oder einen Betrag, abhängig von der Auswahl im **Grundlage für Zinsberechnung**-Feld auf der **Einrichten von Zinscodes**-Seite.</span><span class="sxs-lookup"><span data-stu-id="8057f-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="8057f-142">Beispiel 1: Zinsen nach Bereich = Betrag</span><span class="sxs-lookup"><span data-stu-id="8057f-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="8057f-143">Sie richten einen Zinscode ein, der Zinsen einmal für alle drei Monate, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt.</span><span class="sxs-lookup"><span data-stu-id="8057f-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="8057f-144">Sie möchten die Berechnung auf einem Prozentsatzzinsenwert basieren, gemäß bestimmten Betragsschritten.</span><span class="sxs-lookup"><span data-stu-id="8057f-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="8057f-145">Der Zinsenwert beträgt 1 Prozent für Rechnungsbeträge bis 1.000,00, 2 Prozent für Beträge von 1.001,00 bis 5.000,00 und 3 Prozent für die Beträge, die größer 5.000,00 sind.</span><span class="sxs-lookup"><span data-stu-id="8057f-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="8057f-146">Sie richten die Zinscodefeldwerte wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="8057f-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="8057f-147">**Feldname**</span><span class="sxs-lookup"><span data-stu-id="8057f-147">**Field name**</span></span>                  | <span data-ttu-id="8057f-148">**Feldwert**</span><span class="sxs-lookup"><span data-stu-id="8057f-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="8057f-149">**Zinscode**</span><span class="sxs-lookup"><span data-stu-id="8057f-149">**Interest code**</span></span>               | <span data-ttu-id="8057f-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="8057f-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="8057f-151">**Zinsen berechnen alle**</span><span class="sxs-lookup"><span data-stu-id="8057f-151">**Calculate interest every**</span></span>    | <span data-ttu-id="8057f-152">3/Monat</span><span class="sxs-lookup"><span data-stu-id="8057f-152">3/Month</span></span>         |
| <span data-ttu-id="8057f-153">**Zinsen nach Bereich**</span><span class="sxs-lookup"><span data-stu-id="8057f-153">**Interest by range**</span></span>           | <span data-ttu-id="8057f-154">Betrag</span><span class="sxs-lookup"><span data-stu-id="8057f-154">Amount</span></span>          |
| <span data-ttu-id="8057f-155">**Grundlage für Zinsberechnung**</span><span class="sxs-lookup"><span data-stu-id="8057f-155">**Calculate interest based on**</span></span> | <span data-ttu-id="8057f-156">Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="8057f-156">Percentage</span></span>      |

<span data-ttu-id="8057f-157">Sie richten die Bereichsinformationen wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="8057f-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="8057f-158">**Von Wert**</span><span class="sxs-lookup"><span data-stu-id="8057f-158">**From value**</span></span> | <span data-ttu-id="8057f-159">**Zinswert**</span><span class="sxs-lookup"><span data-stu-id="8057f-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="8057f-160">0</span><span class="sxs-lookup"><span data-stu-id="8057f-160">0</span></span>              | <span data-ttu-id="8057f-161">1</span><span class="sxs-lookup"><span data-stu-id="8057f-161">1</span></span>                  |
| <span data-ttu-id="8057f-162">1,001</span><span class="sxs-lookup"><span data-stu-id="8057f-162">1,001</span></span>          | <span data-ttu-id="8057f-163">2</span><span class="sxs-lookup"><span data-stu-id="8057f-163">2</span></span>                  |
| <span data-ttu-id="8057f-164">5,001</span><span class="sxs-lookup"><span data-stu-id="8057f-164">5,001</span></span>          | <span data-ttu-id="8057f-165">3</span><span class="sxs-lookup"><span data-stu-id="8057f-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="8057f-166">Beispiel 2: Zinsen nach Bereich = Tage</span><span class="sxs-lookup"><span data-stu-id="8057f-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="8057f-167">Sie richten einen Zinscode ein, der Zinsen einmal für alle 15 Tage, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt.</span><span class="sxs-lookup"><span data-stu-id="8057f-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="8057f-168">Sie möchten die Berechnung auf einem Zinsbetragswert basieren, gemäß bestimmten Tagesschritten.</span><span class="sxs-lookup"><span data-stu-id="8057f-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="8057f-169">Der Zinsenwert ist 10,00 pro 15 Tage für die ersten 60 Tage, 15,00 pro 15 Tage für die Tage 61 bis 90 und 20,00 pro 15 Tagen nach Tag 91.</span><span class="sxs-lookup"><span data-stu-id="8057f-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="8057f-170">Sie richten die Zinscodefeldwerte wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="8057f-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="8057f-171">**Feldname**</span><span class="sxs-lookup"><span data-stu-id="8057f-171">**Field name**</span></span>                  | <span data-ttu-id="8057f-172">**Feldwert**</span><span class="sxs-lookup"><span data-stu-id="8057f-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="8057f-173">**Zinscode**</span><span class="sxs-lookup"><span data-stu-id="8057f-173">**Interest code**</span></span>               | <span data-ttu-id="8057f-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="8057f-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="8057f-175">**Zinsen berechnen alle**</span><span class="sxs-lookup"><span data-stu-id="8057f-175">**Calculate interest every**</span></span>    | <span data-ttu-id="8057f-176">15/Tag</span><span class="sxs-lookup"><span data-stu-id="8057f-176">15/Day</span></span>          |
| <span data-ttu-id="8057f-177">**Zinsen nach Bereich**</span><span class="sxs-lookup"><span data-stu-id="8057f-177">**Interest by range**</span></span>           | <span data-ttu-id="8057f-178">Tage</span><span class="sxs-lookup"><span data-stu-id="8057f-178">Days</span></span>            |
| <span data-ttu-id="8057f-179">**Grundlage für Zinsberechnung**</span><span class="sxs-lookup"><span data-stu-id="8057f-179">**Calculate interest based on**</span></span> | <span data-ttu-id="8057f-180">Betrag</span><span class="sxs-lookup"><span data-stu-id="8057f-180">Amount</span></span>          |

<span data-ttu-id="8057f-181">Sie richten die Bereichsinformationen wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="8057f-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="8057f-182">**Von Wert**</span><span class="sxs-lookup"><span data-stu-id="8057f-182">**From value**</span></span> | <span data-ttu-id="8057f-183">**Zinswert**</span><span class="sxs-lookup"><span data-stu-id="8057f-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="8057f-184">0</span><span class="sxs-lookup"><span data-stu-id="8057f-184">0</span></span>              | <span data-ttu-id="8057f-185">10</span><span class="sxs-lookup"><span data-stu-id="8057f-185">10</span></span>                 |
| <span data-ttu-id="8057f-186">61</span><span class="sxs-lookup"><span data-stu-id="8057f-186">61</span></span>             | <span data-ttu-id="8057f-187">15</span><span class="sxs-lookup"><span data-stu-id="8057f-187">15</span></span>                 |
| <span data-ttu-id="8057f-188">91</span><span class="sxs-lookup"><span data-stu-id="8057f-188">91</span></span>             | <span data-ttu-id="8057f-189">20</span><span class="sxs-lookup"><span data-stu-id="8057f-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="8057f-190">Beispiel 3: Zinsen nach Bereich = Monate</span><span class="sxs-lookup"><span data-stu-id="8057f-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="8057f-191">Sie richten einen Zinscode ein, der Zinsen einmal für jeden Monat, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt.</span><span class="sxs-lookup"><span data-stu-id="8057f-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="8057f-192">Sie möchten die Berechnung auf einem Prozentsatzzinsenwert basieren, gemäß bestimmten Monatsschritten.</span><span class="sxs-lookup"><span data-stu-id="8057f-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="8057f-193">Der Zinsenwert beträgt 1,5 Prozent pro Monat für die ersten drei Monate Überfälligkeit, 2,0 Prozent pro Monat für die zweiten drei Monate und 2,5 Prozent pro Monat für jeden Monat nach den ersten sechs Monaten.</span><span class="sxs-lookup"><span data-stu-id="8057f-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="8057f-194">Sie richten die Zinscodefeldwerte wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="8057f-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="8057f-195">**Feldname**</span><span class="sxs-lookup"><span data-stu-id="8057f-195">**Field name**</span></span>                  | <span data-ttu-id="8057f-196">**Feldwert**</span><span class="sxs-lookup"><span data-stu-id="8057f-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="8057f-197">**Zinscode**</span><span class="sxs-lookup"><span data-stu-id="8057f-197">**Interest code**</span></span>               | <span data-ttu-id="8057f-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="8057f-198">1M%ByMth</span></span>        |
| <span data-ttu-id="8057f-199">**Zinsen berechnen alle**</span><span class="sxs-lookup"><span data-stu-id="8057f-199">**Calculate interest every**</span></span>    | <span data-ttu-id="8057f-200">1/Monat</span><span class="sxs-lookup"><span data-stu-id="8057f-200">1/Month</span></span>         |
| <span data-ttu-id="8057f-201">**Zinsen nach Bereich**</span><span class="sxs-lookup"><span data-stu-id="8057f-201">**Interest by range**</span></span>           | <span data-ttu-id="8057f-202">Monate</span><span class="sxs-lookup"><span data-stu-id="8057f-202">Months</span></span>          |
| <span data-ttu-id="8057f-203">**Grundlage für Zinsberechnung**</span><span class="sxs-lookup"><span data-stu-id="8057f-203">**Calculate interest based on**</span></span> | <span data-ttu-id="8057f-204">Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="8057f-204">Percentage</span></span>      |

<span data-ttu-id="8057f-205">Sie richten die Bereichsinformationen wie folgt ein.</span><span class="sxs-lookup"><span data-stu-id="8057f-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="8057f-206">**Von Wert**</span><span class="sxs-lookup"><span data-stu-id="8057f-206">**From value**</span></span> | <span data-ttu-id="8057f-207">**Zinswert**</span><span class="sxs-lookup"><span data-stu-id="8057f-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="8057f-208">0</span><span class="sxs-lookup"><span data-stu-id="8057f-208">0</span></span>              | <span data-ttu-id="8057f-209">1.5</span><span class="sxs-lookup"><span data-stu-id="8057f-209">1.5</span></span>                |
| <span data-ttu-id="8057f-210">4</span><span class="sxs-lookup"><span data-stu-id="8057f-210">4</span></span>              | <span data-ttu-id="8057f-211">2</span><span class="sxs-lookup"><span data-stu-id="8057f-211">2</span></span>                  |
| <span data-ttu-id="8057f-212">7</span><span class="sxs-lookup"><span data-stu-id="8057f-212">7</span></span>              | <span data-ttu-id="8057f-213">2,5</span><span class="sxs-lookup"><span data-stu-id="8057f-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="8057f-214">Neue Versionen</span><span class="sxs-lookup"><span data-stu-id="8057f-214">New versions</span></span>
<span data-ttu-id="8057f-215">Zinscodes sind ein Gültigkeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="8057f-215">Interest codes are date effective.</span></span> <span data-ttu-id="8057f-216">Wenn Sie den Zinssatz ändern möchten, können Sie eine **neue Version** mit einem zukünftigen Gültigkeitsdatum erstellten.</span><span class="sxs-lookup"><span data-stu-id="8057f-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="8057f-217">Um die verschiedenen Versionen anzeigen, können Sie die Menüauswahl **Anfangsdatum.** verwenden, um das Abschnittsdatum auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8057f-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="8057f-218">Sie können auch **Alle Datensätze anzeigen** auswählen, um alle Zinscodes auf der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8057f-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
