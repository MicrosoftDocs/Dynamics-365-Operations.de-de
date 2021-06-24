---
title: Degressiven Abschreibung von 200 Prozent
description: Dieser Artikel gibt eine Übersicht die 200 Prozent Reduktionssaldomethode der Abschreibung.
author: saraschi2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91876ae28d088a52b12ac58db06cb0cd84b129ad
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193515"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="9934d-103">Degressiven Abschreibung von 200 Prozent</span><span class="sxs-lookup"><span data-stu-id="9934d-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9934d-104">Dieser Artikel gibt eine Übersicht die 200 Prozent Reduktionssaldomethode der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="9934d-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="9934d-105">Wenn Sie ein Abschreibungsprofil für Anlagen einrichten und **200% degressiv** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, werden Anlagen, denen das Abschreibungsprofil zugewiesen wird, in jedem Abschreibungszeitraum um denselben Prozentsatz abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="9934d-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="9934d-106">Der Prozentsatz wird auf Grundlage der Nutzungsdauer der Anlage berechnet.</span><span class="sxs-lookup"><span data-stu-id="9934d-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="9934d-107">Wenn eine Anlage beispielsweise eine Nutzungsdauer von fünf Jahren hat, beträgt der Prozentsatz 40 Prozent (200% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="9934d-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="9934d-108">Diese Methode wird auch als "degressive Doppelratenabschreibung" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9934d-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="9934d-109">Zum Einrichten der 200% degressiven Abschreibung müssen Sie auch Optionen im Feld **Abschreibungsjahr** und im Feld **Periodenhäufigkeit** auf der Seite **Abschreibungsprofile** auswählen.</span><span class="sxs-lookup"><span data-stu-id="9934d-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="9934d-110">Die Optionen, die im Feld **Periodenhäufigkeit** zur Verfügung stehen, variieren abhängig vom Wert, den Sie im Feld **Abschreibungsjahr** auswählen.</span><span class="sxs-lookup"><span data-stu-id="9934d-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="9934d-111">Auswählen eines Abschreibungsjahrs</span><span class="sxs-lookup"><span data-stu-id="9934d-111">Select a depreciation year</span></span>
<span data-ttu-id="9934d-112">Sie können entweder **Kalender** oder **Steuerlich** im Feld **Abschreibungsjahr** auf der Seite **Abschreibungsprofile** auswählen.</span><span class="sxs-lookup"><span data-stu-id="9934d-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="9934d-113">Der Standardwert ist **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="9934d-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="9934d-114">Durch Ihre Auswahl werden die Optionen bestimmt, die im Feld **Periodenhäufigkeit** zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="9934d-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="9934d-115">In diesem Feld wird die Abgrenzung der Buchungsdaten und Beträge für Abschreibungen über das Kalenderjahr definiert.</span><span class="sxs-lookup"><span data-stu-id="9934d-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="9934d-116">Kalender</span><span class="sxs-lookup"><span data-stu-id="9934d-116">Calendar</span></span>

<span data-ttu-id="9934d-117">Falls gewünscht, können Sie im Feld **Abschreibungsjahr** den Standardwert **Kalender** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="9934d-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="9934d-118">Die **Kalender** Option aktualisiert die Abschreibungsbasis am 1. Januar jedes Jahres.</span><span class="sxs-lookup"><span data-stu-id="9934d-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="9934d-119">Normalerweise ist die Abschreibung der Nettobuchwert abzüglich des Restwerts.</span><span class="sxs-lookup"><span data-stu-id="9934d-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="9934d-120">In den Beispielen weiter unten in diesem Thema ist der Zähler im ersten Ausdruck in Berechnungen in der Spalte "Berechnung" die Abschreibungsbasis.</span><span class="sxs-lookup"><span data-stu-id="9934d-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="9934d-121">Wenn als Abschreibungsjahr **Kalender** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="9934d-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="9934d-122">Bei Auswahl von **Jährlich** wird ein Betrag am 31. Dezember gebucht.</span><span class="sxs-lookup"><span data-stu-id="9934d-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="9934d-123">Bei Auswahl von **Monatlich** wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.</span><span class="sxs-lookup"><span data-stu-id="9934d-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="9934d-124">Bei Auswahl von **Vierteljährlich** wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.</span><span class="sxs-lookup"><span data-stu-id="9934d-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="9934d-125">Bei Auswahl von **Halbjährlich** wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="9934d-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="9934d-126">Bei Auswahl von **Täglich** wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.</span><span class="sxs-lookup"><span data-stu-id="9934d-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="9934d-127">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="9934d-127">Fiscal</span></span>

<span data-ttu-id="9934d-128">Wenn Sie **Steuerlich** im Jahrfeld **Abschreibung** auswählen, wird die Abschreibungsmethode "200 % degressiv" auf Grundlage des Geschäftsjahres für den Steuerkalender berechnet, der für das Wertmodell oder das Abschreibungsbuch angegeben wird, oder für den Steuerkalender, der auf der Seite **Sachkonto** ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9934d-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="9934d-129">Steuerkalender werden auf der Seite **Steuerkalender** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="9934d-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="9934d-130">Für das Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli.</span><span class="sxs-lookup"><span data-stu-id="9934d-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="9934d-131">Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein.</span><span class="sxs-lookup"><span data-stu-id="9934d-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="9934d-132">Die Abschreibung wird für jede Periode angepasst.</span><span class="sxs-lookup"><span data-stu-id="9934d-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="9934d-133">Die Länge des nächsten Geschäftsjahrs wird anhand der Finanzzeiträume bestimmt, die auf der Seite **Steuerkalender** eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="9934d-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="9934d-134">Wenn **Steuerlich** als Abschreibungsjahr ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="9934d-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="9934d-135">Bei Auswahl von **Jährlich** wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wird, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="9934d-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="9934d-136">**Finanzzeitraum** bucht den Gesamtbetrag der Abschreibung, die für das Geschäftsjahr berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="9934d-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="9934d-137">Dieser Betrag wird auf Steuerperioden aufgeteilt, die auf der Seite **Steuerkalender** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9934d-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="9934d-138">Beispiel für die Abschreibungsmethode "200 % degressiv"</span><span class="sxs-lookup"><span data-stu-id="9934d-138">Example of 200% reducing balance depreciation</span></span>

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| <span data-ttu-id="9934d-139">Anschaffungskosten</span><span class="sxs-lookup"><span data-stu-id="9934d-139">Acquisition cost</span></span>               | <span data-ttu-id="9934d-140">11.000</span><span class="sxs-lookup"><span data-stu-id="9934d-140">11,000</span></span> |
| <span data-ttu-id="9934d-141">Schrottwert</span><span class="sxs-lookup"><span data-stu-id="9934d-141">Salvage value</span></span>                  | <span data-ttu-id="9934d-142">1, 000</span><span class="sxs-lookup"><span data-stu-id="9934d-142">1, 000</span></span> |
| <span data-ttu-id="9934d-143">Abschreibungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="9934d-143">Depreciation base</span></span>              | <span data-ttu-id="9934d-144">10.000</span><span class="sxs-lookup"><span data-stu-id="9934d-144">10,000</span></span> |
| <span data-ttu-id="9934d-145">Nutzungsdauer (Jahre)</span><span class="sxs-lookup"><span data-stu-id="9934d-145">Service life years</span></span>             | <span data-ttu-id="9934d-146">5</span><span class="sxs-lookup"><span data-stu-id="9934d-146">5</span></span>      |
| <span data-ttu-id="9934d-147">Jährlicher Abschreibungsprozentsatz</span><span class="sxs-lookup"><span data-stu-id="9934d-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="9934d-148">40 %</span><span class="sxs-lookup"><span data-stu-id="9934d-148">40%</span></span>    |

<span data-ttu-id="9934d-149">Bei der Abschreibungsmethode „200 % degressiv“ werden 200 Prozent durch die Anzahl der Jahre der Nutzungsdauer dividiert.</span><span class="sxs-lookup"><span data-stu-id="9934d-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="9934d-150">Der sich ergebende Prozentsatz wird mit dem Nettobuchwert der Anlage multipliziert, um den Abschreibungsbetrag für das Jahr zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9934d-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="9934d-151">Zeitraum</span><span class="sxs-lookup"><span data-stu-id="9934d-151">Period</span></span> | <span data-ttu-id="9934d-152">Berechnung des jährlichen Abschreibungsbetrags</span><span class="sxs-lookup"><span data-stu-id="9934d-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="9934d-153">Buchwert</span><span class="sxs-lookup"><span data-stu-id="9934d-153">Book value</span></span>             | <span data-ttu-id="9934d-154">Nettobuchwert am Ende des Jahres</span><span class="sxs-lookup"><span data-stu-id="9934d-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="9934d-155">Jahr 1</span><span class="sxs-lookup"><span data-stu-id="9934d-155">Year 1</span></span> | <span data-ttu-id="9934d-156">(11.000 – 1.000) × 40 % = 4.000</span><span class="sxs-lookup"><span data-stu-id="9934d-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="9934d-157">11.000 – 4.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="9934d-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="9934d-158">11.000 – 1.000 – 4.000 = 6.000</span><span class="sxs-lookup"><span data-stu-id="9934d-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="9934d-159">Jahr 2</span><span class="sxs-lookup"><span data-stu-id="9934d-159">Year 2</span></span> | <span data-ttu-id="9934d-160">6.000 × 40 % = 2.400</span><span class="sxs-lookup"><span data-stu-id="9934d-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="9934d-161">7.000 – 2.400 = 4.600</span><span class="sxs-lookup"><span data-stu-id="9934d-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="9934d-162">6.000 – 2.400 = 3.600</span><span class="sxs-lookup"><span data-stu-id="9934d-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="9934d-163">Jahr 3</span><span class="sxs-lookup"><span data-stu-id="9934d-163">Year 3</span></span> | <span data-ttu-id="9934d-164">3.600 × 40 % = 1.440</span><span class="sxs-lookup"><span data-stu-id="9934d-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="9934d-165">4.600 – 1.440 = 3.160</span><span class="sxs-lookup"><span data-stu-id="9934d-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="9934d-166">3.600 – 1.440 = 2.160</span><span class="sxs-lookup"><span data-stu-id="9934d-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="9934d-167">Hinweis: Wenn der Betrag, der mithilfe der Abschreibungsmethode "200% degressiv" berechnet wird, geringer ausfällt, als der Betrag, der mithilfe der Methode "Linear" berechnet würde, gibt es eine Umrechnung zur linearen Methode für die verbleibende Nutzungsdauer.</span><span class="sxs-lookup"><span data-stu-id="9934d-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]