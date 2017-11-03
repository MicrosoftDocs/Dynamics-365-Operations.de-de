---
title: Degressiven Abschreibung von 125 Prozent
description: "Dieser Artikel gibt eine Übersicht die 125 Prozent Reduktionssaldomethode der Abschreibung."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="bd663-103">Degressiven Abschreibung von 125 Prozent</span><span class="sxs-lookup"><span data-stu-id="bd663-103">125 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bd663-104">Dieser Artikel gibt eine Übersicht die 125 Prozent Reduktionssaldomethode der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="bd663-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="bd663-105">Wenn Sie ein Abschreibungsprofil für Anlagen einrichten und **125 % degressiv** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, werden Anlagen, denen das Abschreibungsprofil zugewiesen wird, in jedem Abschreibungszeitraum um denselben Prozentsatz abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd663-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="bd663-106">Dieser Prozentsatz wird auf Grundlage der Nutzungsdauer der Anlage berechnet.</span><span class="sxs-lookup"><span data-stu-id="bd663-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="bd663-107">Wenn eine Anlage beispielsweise eine Nutzungsdauer von fünf Jahren hat, beträgt der Prozentsatz 25 Prozent (125 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="bd663-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="bd663-108">Zum Einrichten der 125% degressiven Abschreibung müssen Sie auch Optionen im Feld **Abschreibungsjahr** und im Feld **Periodenhäufigkeit** auf der Seite **Abschreibungsprofile** auswählen.</span><span class="sxs-lookup"><span data-stu-id="bd663-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="bd663-109">Die Optionen, die im Feld **Periodenhäufigkeit** zur Verfügung stehen, variieren abhängig vom Wert, der im Feld **Abschreibungsjahr** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="bd663-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="bd663-110">Auswählen eines Abschreibungsjahrs</span><span class="sxs-lookup"><span data-stu-id="bd663-110">Select a depreciation year</span></span>
<span data-ttu-id="bd663-111">Sie können entweder **Kalender** oder **Steuerlich** im Feld **Abschreibungsjahr** auf der Seite **Abschreibungsprofile** auswählen.</span><span class="sxs-lookup"><span data-stu-id="bd663-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="bd663-112">Der Standardwert ist **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="bd663-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="bd663-113">Durch Ihre Auswahl werden die Optionen bestimmt, die im Feld **Periodenhäufigkeit** zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="bd663-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="bd663-114">In diesem Feld wird die Abgrenzung der Buchungsdaten und Beträge für Abschreibungen über das Kalenderjahr definiert.</span><span class="sxs-lookup"><span data-stu-id="bd663-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="bd663-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="bd663-115">Calendar</span></span>

<span data-ttu-id="bd663-116">Falls gewünscht, können Sie im Feld **Abschreibungsjahr** den Standardwert **Kalender** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="bd663-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="bd663-117">Die **Kalender** Option aktualisiert die Abschreibungsbasis am 1. Januar jedes Jahres.</span><span class="sxs-lookup"><span data-stu-id="bd663-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="bd663-118">Normalerweise ist die Abschreibungsbasis der Nettobuchwert abzüglich des Restwerts.</span><span class="sxs-lookup"><span data-stu-id="bd663-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="bd663-119">In den Beispielen weiter unten in diesem Thema ist der Zähler im ersten Ausdruck in Berechnungen in der Spalte "Berechnung" die Abschreibungsbasis.</span><span class="sxs-lookup"><span data-stu-id="bd663-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="bd663-120">Wenn als Abschreibungsjahr **Kalender** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="bd663-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="bd663-121">Bei Auswahl von **Jährlich** wird ein Betrag am 31. Dezember gebucht.</span><span class="sxs-lookup"><span data-stu-id="bd663-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="bd663-122">Bei Auswahl von **Monatlich** wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.</span><span class="sxs-lookup"><span data-stu-id="bd663-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="bd663-123">Bei Auswahl von **Vierteljährlich** wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.</span><span class="sxs-lookup"><span data-stu-id="bd663-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="bd663-124">Bei Auswahl von **Halbjährlich** wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="bd663-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="bd663-125">Bei Auswahl von **Täglich** wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.</span><span class="sxs-lookup"><span data-stu-id="bd663-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="bd663-126">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="bd663-126">Fiscal</span></span>

<span data-ttu-id="bd663-127">Wenn Sie **Steuerlich** im Feld **Jahresabschreibung** auswählen, wird die Abschreibungsmethode "125 % degressiv" auf Grundlage des Geschäftsjahres für den Steuerkalender berechnet, der für das Wertmodell oder das Abschreibungsbuch angegeben wird, oder für den Steuerkalender, der auf der Seite **Sachkonto** ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bd663-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="bd663-128">Steuerkalender werden auf der Seite **Steuerkalender** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bd663-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="bd663-129">Für das Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli.</span><span class="sxs-lookup"><span data-stu-id="bd663-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="bd663-130">Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein.</span><span class="sxs-lookup"><span data-stu-id="bd663-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="bd663-131">Die Abschreibung wird automatisch für jede Periode angepasst, und die Länge des nächsten Geschäftsjahres wird mit den Einstellungen für die Perioden auf der Seite **Steuerkalender** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bd663-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="bd663-132">Wenn als Abschreibungsjahr **Steuerlich** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="bd663-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="bd663-133">Bei Auswahl von **Jährlich** wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wird, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="bd663-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="bd663-134">**Finanzzeitraum** bucht den Gesamtbetrag der Abschreibung, die für das Geschäftsjahr berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="bd663-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="bd663-135">Dieser Betrag wird auf Steuerperioden aufgeteilt, die auf der Seite **Steuerkalender** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd663-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="bd663-136">Beispiel für die Abschreibungsmethode "125 % degressiv"</span><span class="sxs-lookup"><span data-stu-id="bd663-136">Example of 125% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="bd663-137">Anschaffungskosten</span><span class="sxs-lookup"><span data-stu-id="bd663-137">Acquisition cost</span></span>               | <span data-ttu-id="bd663-138">11.000</span><span class="sxs-lookup"><span data-stu-id="bd663-138">11,000</span></span> |
| <span data-ttu-id="bd663-139">Schrottwert</span><span class="sxs-lookup"><span data-stu-id="bd663-139">Salvage value</span></span>                  | <span data-ttu-id="bd663-140">1.000</span><span class="sxs-lookup"><span data-stu-id="bd663-140">1,000</span></span>  |
| <span data-ttu-id="bd663-141">Abschreibungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="bd663-141">Depreciation base</span></span>              | <span data-ttu-id="bd663-142">10.000</span><span class="sxs-lookup"><span data-stu-id="bd663-142">10,000</span></span> |
| <span data-ttu-id="bd663-143">Nutzungsdauer (Jahre)</span><span class="sxs-lookup"><span data-stu-id="bd663-143">Service life years</span></span>             | <span data-ttu-id="bd663-144">5</span><span class="sxs-lookup"><span data-stu-id="bd663-144">5</span></span>      |
| <span data-ttu-id="bd663-145">Jährlicher Abschreibungsprozentsatz</span><span class="sxs-lookup"><span data-stu-id="bd663-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="bd663-146">25 %</span><span class="sxs-lookup"><span data-stu-id="bd663-146">25%</span></span>    |

<span data-ttu-id="bd663-147">Bei der Abschreibungsmethode "125 % degressiv" werden 125 Prozent durch die Anzahl der Jahre der Nutzungsdauer dividiert.</span><span class="sxs-lookup"><span data-stu-id="bd663-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="bd663-148">Der sich ergebende Prozentsatz wird mit dem Nettobuchwert der Anlage multipliziert, um den Abschreibungsbetrag für das Jahr zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="bd663-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="bd663-149">Zeitraum</span><span class="sxs-lookup"><span data-stu-id="bd663-149">Period</span></span> | <span data-ttu-id="bd663-150">Berechnung des jährlichen Abschreibungsbetrags</span><span class="sxs-lookup"><span data-stu-id="bd663-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="bd663-151">Buchwert</span><span class="sxs-lookup"><span data-stu-id="bd663-151">Book value</span></span>                    | <span data-ttu-id="bd663-152">Nettobuchwert am Ende des Jahres</span><span class="sxs-lookup"><span data-stu-id="bd663-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="bd663-153">Jahr 1</span><span class="sxs-lookup"><span data-stu-id="bd663-153">Year 1</span></span> | <span data-ttu-id="bd663-154">(11.000 – 1.000) × 25 % = 2.500</span><span class="sxs-lookup"><span data-stu-id="bd663-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="bd663-155">(11.000 – 2.500) = 8.500</span><span class="sxs-lookup"><span data-stu-id="bd663-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="bd663-156">(11.000 – 1.000 – 2.500) = 7.500</span><span class="sxs-lookup"><span data-stu-id="bd663-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="bd663-157">Jahr 2</span><span class="sxs-lookup"><span data-stu-id="bd663-157">Year 2</span></span> | <span data-ttu-id="bd663-158">7.500 × 25 % = 1.875</span><span class="sxs-lookup"><span data-stu-id="bd663-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="bd663-159">(8.500 – 1.875) = 6.625</span><span class="sxs-lookup"><span data-stu-id="bd663-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="bd663-160">(7.500 – 1.875) = 5.625</span><span class="sxs-lookup"><span data-stu-id="bd663-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="bd663-161">Jahr 3</span><span class="sxs-lookup"><span data-stu-id="bd663-161">Year 3</span></span> | <span data-ttu-id="bd663-162">5.625 × 25 % = 1.406,25</span><span class="sxs-lookup"><span data-stu-id="bd663-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="bd663-163">(6.625 – 1.406,25) = 5.218,75</span><span class="sxs-lookup"><span data-stu-id="bd663-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="bd663-164">(5.625 – 1.406,25) = 4.218,75</span><span class="sxs-lookup"><span data-stu-id="bd663-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="bd663-165">Hinweis: Wenn der Betrag, der mithilfe der Abschreibungsmethode "125% degressiv" berechnet wird, geringer ausfällt, als der Betrag, der mithilfe der Methode "Linear" berechnet würde, gibt es eine Umrechnung zur linearen Methode für die verbleibende Nutzungsdauer.</span><span class="sxs-lookup"><span data-stu-id="bd663-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




