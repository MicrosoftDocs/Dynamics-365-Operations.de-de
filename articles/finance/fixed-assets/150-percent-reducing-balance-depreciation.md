---
title: Degressiven Abschreibung von 150 Prozent
description: Dieser Artikel gibt eine Übersicht die 150 Prozent Reduktionssaldomethode der Abschreibung.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc7fa705681c3f1fde96cabc430dad1dd0045b4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009317"
---
# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="5dde5-103">Degressiven Abschreibung von 150 Prozent</span><span class="sxs-lookup"><span data-stu-id="5dde5-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dde5-104">Dieser Artikel gibt eine Übersicht die 150 Prozent Reduktionssaldomethode der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="5dde5-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="5dde5-105">Wenn Sie ein Abschreibungsprofil für Anlagen einrichten und **150 % degressiv** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, werden Anlagen, denen das Abschreibungsprofil zugewiesen wird, in jedem Abschreibungszeitraum um denselben Prozentsatz abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="5dde5-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="5dde5-106">Dieser Prozentsatz wird auf Grundlage der Nutzungsdauer der Anlage berechnet.</span><span class="sxs-lookup"><span data-stu-id="5dde5-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="5dde5-107">Wenn eine Anlage beispielsweise eine Nutzungsdauer von fünf Jahren hat, beträgt der Prozentsatz 30 Prozent (150 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="5dde5-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="5dde5-108">Zum Einrichten der 150% degressiven Abschreibung müssen Sie auch Optionen im Feld **Abschreibungsjahr** und im Feld **Periodenhäufigkeit** auf der Seite **Abschreibungsprofile** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5dde5-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="5dde5-109">Die Optionen, die im Feld **Periodenhäufigkeit** zur Verfügung stehen, variieren abhängig vom Wert, der im Feld **Abschreibungsjahr** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="5dde5-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="5dde5-110">Auswahl des Abschreibungsjahres</span><span class="sxs-lookup"><span data-stu-id="5dde5-110">Selection of depreciation year</span></span>
<span data-ttu-id="5dde5-111">Sie können entweder **Kalender** oder **Steuerlich** im Feld **Abschreibungsjahr** auf der Seite **Abschreibungsprofile** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5dde5-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="5dde5-112">Der Standardwert ist **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="5dde5-112">The default value is **Calendar**.</span></span> <span data-ttu-id="5dde5-113">Durch Ihre Auswahl werden die Optionen bestimmt, die im Feld **Periodenhäufigkeit** zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="5dde5-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="5dde5-114">In diesem Feld wird die Abgrenzung der Buchungsdaten und Beträge für Abschreibungen über das Kalenderjahr definiert.</span><span class="sxs-lookup"><span data-stu-id="5dde5-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="5dde5-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="5dde5-115">Calendar</span></span>

<span data-ttu-id="5dde5-116">Falls gewünscht, können Sie im Feld **Abschreibungsjahr** den Standardwert **Kalender** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="5dde5-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="5dde5-117">Die **Kalender** Option aktualisiert die Abschreibungsbasis am 1. Januar jedes Jahres.</span><span class="sxs-lookup"><span data-stu-id="5dde5-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="5dde5-118">Normalerweise ist die Abschreibungsbasis der Nettobuchwert abzüglich des Restwerts.</span><span class="sxs-lookup"><span data-stu-id="5dde5-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="5dde5-119">In den Beispielen weiter unten in diesem Thema ist der Zähler im ersten Ausdruck in Berechnungen in der Spalte "Berechnung" die Abschreibungsbasis.</span><span class="sxs-lookup"><span data-stu-id="5dde5-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="5dde5-120">Wenn als Abschreibungsjahr **Kalender** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="5dde5-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="5dde5-121">Bei Auswahl von **Jährlich** wird ein Betrag am 31. Dezember gebucht.</span><span class="sxs-lookup"><span data-stu-id="5dde5-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="5dde5-122">Bei Auswahl von **Monatlich** wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.</span><span class="sxs-lookup"><span data-stu-id="5dde5-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="5dde5-123">Bei Auswahl von **Vierteljährlich** wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.</span><span class="sxs-lookup"><span data-stu-id="5dde5-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="5dde5-124">Bei Auswahl von **Halbjährlich** wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="5dde5-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="5dde5-125">Bei Auswahl von **Täglich** wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.</span><span class="sxs-lookup"><span data-stu-id="5dde5-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="5dde5-126">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5dde5-126">Fiscal</span></span>

<span data-ttu-id="5dde5-127">Wenn Sie **Steuerlich** im Feld **Jahresabschreibung** auswählen, wird die Abschreibungsmethode "150 % degressiv" auf Grundlage des Geschäftsjahres für den Steuerkalender berechnet, der für das Wertmodell oder das Abschreibungsbuch angegeben wird, oder für den Steuerkalender, der auf der Seite **Sachkonto** ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5dde5-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="5dde5-128">Steuerkalender werden auf der Seite **Steuerkalender** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="5dde5-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="5dde5-129">Für das Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli.</span><span class="sxs-lookup"><span data-stu-id="5dde5-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="5dde5-130">Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein.</span><span class="sxs-lookup"><span data-stu-id="5dde5-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="5dde5-131">Die Abschreibung wird für jede Periode angepasst.</span><span class="sxs-lookup"><span data-stu-id="5dde5-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="5dde5-132">Die Länge des nächsten Geschäftsjahrs wird anhand der Finanzzeiträume bestimmt, die auf der Seite **Steuerkalender** eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="5dde5-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="5dde5-133">Wenn als Abschreibungsjahr **Steuerlich** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="5dde5-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="5dde5-134">Bei Auswahl von **Jährlich** wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wurde, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="5dde5-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="5dde5-135">**Finanzzeitraum** bucht den Gesamtbetrag der Abschreibung, die für das Geschäftsjahr berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="5dde5-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="5dde5-136">Dieser Betrag wird auf Steuerperioden aufgeteilt, die auf der Seite **Steuerkalender** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5dde5-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="5dde5-137">Beispiel für die Abschreibungsmethode "150 % degressiv"</span><span class="sxs-lookup"><span data-stu-id="5dde5-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="5dde5-138">Anschaffungskosten</span><span class="sxs-lookup"><span data-stu-id="5dde5-138">Acquisition cost</span></span>               | <span data-ttu-id="5dde5-139">11.000</span><span class="sxs-lookup"><span data-stu-id="5dde5-139">11,000</span></span> |
| <span data-ttu-id="5dde5-140">Schrottwert</span><span class="sxs-lookup"><span data-stu-id="5dde5-140">Salvage value</span></span>                  | <span data-ttu-id="5dde5-141">1.000</span><span class="sxs-lookup"><span data-stu-id="5dde5-141">1,000</span></span>  |
| <span data-ttu-id="5dde5-142">Abschreibungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="5dde5-142">Depreciation base</span></span>              | <span data-ttu-id="5dde5-143">10.000</span><span class="sxs-lookup"><span data-stu-id="5dde5-143">10,000</span></span> |
| <span data-ttu-id="5dde5-144">Nutzungsdauer (Jahre)</span><span class="sxs-lookup"><span data-stu-id="5dde5-144">Service life years</span></span>             | <span data-ttu-id="5dde5-145">5</span><span class="sxs-lookup"><span data-stu-id="5dde5-145">5</span></span>      |
| <span data-ttu-id="5dde5-146">Jährlicher Abschreibungsprozentsatz</span><span class="sxs-lookup"><span data-stu-id="5dde5-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="5dde5-147">30 %</span><span class="sxs-lookup"><span data-stu-id="5dde5-147">30%</span></span>    |

<span data-ttu-id="5dde5-148">Bei der Abschreibungsmethode „150 % degressiv“ werden 150 Prozent durch die Anzahl der Jahre der Nutzungsdauer dividiert.</span><span class="sxs-lookup"><span data-stu-id="5dde5-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="5dde5-149">Der sich ergebende Prozentsatz wird mit dem Nettobuchwert der Anlage multipliziert, um den Abschreibungsbetrag für das Jahr zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5dde5-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="5dde5-150">Zeitraum</span><span class="sxs-lookup"><span data-stu-id="5dde5-150">Period</span></span> | <span data-ttu-id="5dde5-151">Berechnung des jährlichen Abschreibungsbetrags</span><span class="sxs-lookup"><span data-stu-id="5dde5-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="5dde5-152">Buchwert</span><span class="sxs-lookup"><span data-stu-id="5dde5-152">Book value</span></span>             | <span data-ttu-id="5dde5-153">Nettobuchwert am Ende des Jahres</span><span class="sxs-lookup"><span data-stu-id="5dde5-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="5dde5-154">Jahr 1</span><span class="sxs-lookup"><span data-stu-id="5dde5-154">Year 1</span></span> | <span data-ttu-id="5dde5-155">(11.000 – 1.000) × 30 % = 3.000</span><span class="sxs-lookup"><span data-stu-id="5dde5-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="5dde5-156">11.000 – 3.000 = 8.000</span><span class="sxs-lookup"><span data-stu-id="5dde5-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="5dde5-157">11.000 – 1.000 – 3.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="5dde5-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="5dde5-158">Jahr 2</span><span class="sxs-lookup"><span data-stu-id="5dde5-158">Year 2</span></span> | <span data-ttu-id="5dde5-159">7.000 × 30 % = 2.100</span><span class="sxs-lookup"><span data-stu-id="5dde5-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="5dde5-160">8.000 – 2.100 = 5.900</span><span class="sxs-lookup"><span data-stu-id="5dde5-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="5dde5-161">7.000 – 2.100 = 4.900</span><span class="sxs-lookup"><span data-stu-id="5dde5-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="5dde5-162">Jahr 3</span><span class="sxs-lookup"><span data-stu-id="5dde5-162">Year 3</span></span> | <span data-ttu-id="5dde5-163">4.900 × 30 % = 1.470</span><span class="sxs-lookup"><span data-stu-id="5dde5-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="5dde5-164">5.900 – 1.470 = 4.430</span><span class="sxs-lookup"><span data-stu-id="5dde5-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="5dde5-165">4.900 – 1.470 = 3.430</span><span class="sxs-lookup"><span data-stu-id="5dde5-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="5dde5-166">Hinweis: Wenn der Betrag, der mithilfe der Abschreibungsmethode "150% degressiv" berechnet wird, geringer ausfällt, als der Betrag, der mithilfe der Methode "Linear" berechnet würde, gibt es eine Umrechnung zur linearen Methode für die verbleibende Nutzungsdauer.</span><span class="sxs-lookup"><span data-stu-id="5dde5-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



