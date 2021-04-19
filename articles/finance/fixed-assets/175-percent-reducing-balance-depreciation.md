---
title: Degressive Abschreibung (175 Prozent)
description: Dieser Artikel gibt eine Übersicht der 175 prozentigen Reduktionssaldomethode der Abschreibung.
author: saraschi2
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0747c34a4b28340227209adadf367f672deb1ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827145"
---
# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="cd51b-103">Degressive Abschreibung (175 Prozent)</span><span class="sxs-lookup"><span data-stu-id="cd51b-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd51b-104">Dieser Artikel gibt eine Übersicht der 175 prozentigen Reduktionssaldomethode der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="cd51b-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="cd51b-105">Wenn Sie ein Abschreibungsprofil für Anlagen einrichten und **175 % degressiv** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, werden Anlagen, denen das Abschreibungsprofil zugewiesen wird, in jedem Abschreibungszeitraum um denselben Prozentsatz abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="cd51b-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="cd51b-106">Zum Einrichten der 175% degressiven Abschreibung müssen Sie auch Optionen im Feld **Abschreibungsjahr** und im Feld **Periodenhäufigkeit** auf der Seite **Abschreibungsprofile** auswählen.</span><span class="sxs-lookup"><span data-stu-id="cd51b-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="cd51b-107">Die Optionen, die im Feld **Periodenhäufigkeit** zur Verfügung stehen, variieren abhängig vom Wert, der im Feld **Abschreibungsjahr** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="cd51b-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="cd51b-108">Auswählen eines Abschreibungsjahrs</span><span class="sxs-lookup"><span data-stu-id="cd51b-108">Select a depreciation year</span></span>
<span data-ttu-id="cd51b-109">Sie können entweder **Kalender** oder **Steuerlich** im Feld **Abschreibungsjahr** auf der Seite **Abschreibungsprofile** auswählen.</span><span class="sxs-lookup"><span data-stu-id="cd51b-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="cd51b-110">Der Standardwert ist **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="cd51b-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="cd51b-111">Durch Ihre Auswahl werden die Optionen bestimmt, die im Feld **Periodenhäufigkeit** zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="cd51b-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="cd51b-112">In diesem Feld wird die Abgrenzung der Buchungsdaten und Beträge für Abschreibungen über das Kalenderjahr definiert.</span><span class="sxs-lookup"><span data-stu-id="cd51b-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="cd51b-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="cd51b-113">Calendar</span></span>

<span data-ttu-id="cd51b-114">Falls gewünscht, können Sie im Feld **Abschreibungsjahr** den Standardwert **Kalender** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="cd51b-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="cd51b-115">Die **Kalender** Option aktualisiert die Abschreibungsbasis am 1. Januar jedes Jahres.</span><span class="sxs-lookup"><span data-stu-id="cd51b-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="cd51b-116">Normalerweise ist die Abschreibungsbasis der Nettobuchwert abzüglich des Restwerts.</span><span class="sxs-lookup"><span data-stu-id="cd51b-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="cd51b-117">In den Beispielen weiter unten in diesem Thema ist der Zähler im ersten Ausdruck in Berechnungen in der Spalte "Berechnung" die Abschreibungsbasis.</span><span class="sxs-lookup"><span data-stu-id="cd51b-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="cd51b-118">Wenn als Abschreibungsjahr **Kalender** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="cd51b-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="cd51b-119">Bei Auswahl von **Jährlich** wird ein Betrag am 31. Dezember gebucht.</span><span class="sxs-lookup"><span data-stu-id="cd51b-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="cd51b-120">Bei Auswahl von **Monatlich** wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.</span><span class="sxs-lookup"><span data-stu-id="cd51b-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="cd51b-121">Bei Auswahl von **Vierteljährlich** wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.</span><span class="sxs-lookup"><span data-stu-id="cd51b-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="cd51b-122">Bei Auswahl von **Halbjährlich** wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="cd51b-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="cd51b-123">Bei Auswahl von **Täglich** wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.</span><span class="sxs-lookup"><span data-stu-id="cd51b-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="cd51b-124">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="cd51b-124">Fiscal</span></span>

<span data-ttu-id="cd51b-125">Wenn Sie **Steuerlich** im Feld **Jahresabschreibung** auswählen, wird die Abschreibungsmethode "175 % degressiv" auf Grundlage des Geschäftsjahres für den Steuerkalender berechnet, der für das Wertmodell oder das Abschreibungsbuch angegeben wird, oder für den Steuerkalender, der auf der Seite **Sachkonto** ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="cd51b-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="cd51b-126">Steuerkalender werden auf der Seite **Steuerkalender** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="cd51b-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="cd51b-127">Weitere Informationen finden Sie unter [Steuerkalender, Geschäftsjahre und Perioden](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="cd51b-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="cd51b-128">Für das Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli.</span><span class="sxs-lookup"><span data-stu-id="cd51b-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="cd51b-129">Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein.</span><span class="sxs-lookup"><span data-stu-id="cd51b-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="cd51b-130">Die Abschreibung wird automatisch für jede Periode angepasst, und die Länge des nächsten Geschäftsjahres wird mit den Einstellungen für die Perioden auf der Seite **Steuerkalender** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="cd51b-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="cd51b-131">Wenn als Abschreibungsjahr **Steuerlich** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="cd51b-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="cd51b-132">Bei Auswahl von **Jährlich** wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wurde, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="cd51b-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="cd51b-133">**Finanzzeitraum** berechnet den Gesamtbetrag der Abschreibung für das Geschäftsjahr.</span><span class="sxs-lookup"><span data-stu-id="cd51b-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="cd51b-134">Dieser Betrag wird auf Steuerperioden aufgeteilt, die auf der Seite **Steuerkalender** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd51b-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="cd51b-135">Beispiel für die Abschreibungsmethode "175 % degressiv"</span><span class="sxs-lookup"><span data-stu-id="cd51b-135">Example of 175% reducing balance depreciation</span></span>

| <span data-ttu-id="cd51b-136">Feld</span><span class="sxs-lookup"><span data-stu-id="cd51b-136">Field</span></span>                          | <span data-ttu-id="cd51b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="cd51b-137">Value</span></span>  |
|--------------------------------|--------|
| <span data-ttu-id="cd51b-138">Anschaffungskosten</span><span class="sxs-lookup"><span data-stu-id="cd51b-138">Acquisition cost</span></span>               | <span data-ttu-id="cd51b-139">11,000</span><span class="sxs-lookup"><span data-stu-id="cd51b-139">11,000</span></span> |
| <span data-ttu-id="cd51b-140">Schrottwert</span><span class="sxs-lookup"><span data-stu-id="cd51b-140">Salvage value</span></span>                  | <span data-ttu-id="cd51b-141">1.000</span><span class="sxs-lookup"><span data-stu-id="cd51b-141">1,000</span></span>  |
| <span data-ttu-id="cd51b-142">Abschreibungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="cd51b-142">Depreciation base</span></span>              | <span data-ttu-id="cd51b-143">10.000</span><span class="sxs-lookup"><span data-stu-id="cd51b-143">10,000</span></span> |
| <span data-ttu-id="cd51b-144">Nutzungsdauer (Jahre)</span><span class="sxs-lookup"><span data-stu-id="cd51b-144">Service life years</span></span>             | <span data-ttu-id="cd51b-145">5</span><span class="sxs-lookup"><span data-stu-id="cd51b-145">5</span></span>      |
| <span data-ttu-id="cd51b-146">Jährlicher Abschreibungsprozentsatz</span><span class="sxs-lookup"><span data-stu-id="cd51b-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="cd51b-147">35 %</span><span class="sxs-lookup"><span data-stu-id="cd51b-147">35%</span></span>    |

<span data-ttu-id="cd51b-148">Bei der Abschreibungsmethode „175 % degressiv“ werden 175 Prozent durch die Anzahl der Jahre der Nutzungsdauer dividiert.</span><span class="sxs-lookup"><span data-stu-id="cd51b-148">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="cd51b-149">Der sich ergebende Prozentsatz wird mit dem Nettobuchwert der Anlage multipliziert, um den Abschreibungsbetrag für das Jahr zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cd51b-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="cd51b-150">Zeitraum</span><span class="sxs-lookup"><span data-stu-id="cd51b-150">Period</span></span> | <span data-ttu-id="cd51b-151">Berechnung des jährlichen Abschreibungsbetrags</span><span class="sxs-lookup"><span data-stu-id="cd51b-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="cd51b-152">Buchwert</span><span class="sxs-lookup"><span data-stu-id="cd51b-152">Book value</span></span>                  | <span data-ttu-id="cd51b-153">Nettobuchwert am Ende des Jahres</span><span class="sxs-lookup"><span data-stu-id="cd51b-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="cd51b-154">Jahr 1</span><span class="sxs-lookup"><span data-stu-id="cd51b-154">Year 1</span></span> | <span data-ttu-id="cd51b-155">(11.000 – 1.000) × 35 % = 3.500</span><span class="sxs-lookup"><span data-stu-id="cd51b-155">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="cd51b-156">11.000 – 3.500 = 7.500</span><span class="sxs-lookup"><span data-stu-id="cd51b-156">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="cd51b-157">11.000 – 1.000 – 3.500 = 6.500</span><span class="sxs-lookup"><span data-stu-id="cd51b-157">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="cd51b-158">Jahr 2</span><span class="sxs-lookup"><span data-stu-id="cd51b-158">Year 2</span></span> | <span data-ttu-id="cd51b-159">6.500 × 35 % = 2.275</span><span class="sxs-lookup"><span data-stu-id="cd51b-159">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="cd51b-160">7.500 – 2.275 = 5.225</span><span class="sxs-lookup"><span data-stu-id="cd51b-160">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="cd51b-161">6.500 – 2.275 = 4.225</span><span class="sxs-lookup"><span data-stu-id="cd51b-161">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="cd51b-162">Jahr 3</span><span class="sxs-lookup"><span data-stu-id="cd51b-162">Year 3</span></span> | <span data-ttu-id="cd51b-163">4.225 × 35 % = 1.478,75</span><span class="sxs-lookup"><span data-stu-id="cd51b-163">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="cd51b-164">5.225 – 1.478,75 = 3.746,25</span><span class="sxs-lookup"><span data-stu-id="cd51b-164">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="cd51b-165">4.225 – 1.478,75 = 2.746,25</span><span class="sxs-lookup"><span data-stu-id="cd51b-165">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="cd51b-166">Hinweis: Wenn der Betrag, der mithilfe der Abschreibungsmethode "175% degressiv" berechnet wird, geringer ausfällt, als der Betrag, der mithilfe der Methode "Linear" berechnet würde, gibt es eine Umrechnung zur linearen Methode für die verbleibende Nutzungsdauer.</span><span class="sxs-lookup"><span data-stu-id="cd51b-166">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]