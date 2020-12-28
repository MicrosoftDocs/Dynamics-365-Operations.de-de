---
title: Degressive Abschreibung
description: Dieser Artikel gibt eine Übersicht die Reduktionssaldomethode der Abschreibung.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd4a8726ca194de2e5d95128659f3b212eaace5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443632"
---
# <a name="reduce-balance-depreciation"></a><span data-ttu-id="6b9e8-103">Degressive Abschreibung</span><span class="sxs-lookup"><span data-stu-id="6b9e8-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b9e8-104">Dieser Artikel gibt eine Übersicht die Reduktionssaldomethode der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="6b9e8-105">Wenn Sie ein Anlagenabschreibungsprofil einrichten und „Degressiv“ im Feld „Methode“ der Seite „Abschreibungsprofile“ auswählen, werden die Anlagen, denen dieses Abschreibungsprofil zugeordnet ist, in jedem Abschreibungszeitraum um den gleichen Prozentsatz abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="6b9e8-106">Zum Einrichten der degressiven Abschreibung müssen Sie auch in den Feldern auf dem Inforegister „Allgemein“ der Seite „Abschreibungsprofile“ eine Auswahl treffen.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="6b9e8-107">Wählen Sie zunächst im Feld „Abschreibungsjahr“ ein Jahr aus.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="6b9e8-108">Je nach Auswahl werden im Feld Periodenhäufigkeit unterschiedliche Optionen angezeigt, wie in den nachstehenden Abschnitten erläutert.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="6b9e8-109">Sie müssen einen Wert in das Feld Prozentwert für das Abschreibungsprofil auch eingeben.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="6b9e8-110">Wenn Sie die Option „Vollständige Abschreibung“ aktivieren, wird die verbleibende Abschreibung auf dem letzten Abschreibungszeitraum ausgeführt und es kann sich um einen großen Betrags handeln.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="6b9e8-111">Einigen Ländern/Regionen verwenden keinen Wechsel zu einer linearen Methode.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="6b9e8-112">Ein Abschreibungswechsel tritt auf, wenn der Betrag der alternativen Abschreibungsmethode größer oder gleich dem primären Abschreibungsprofilbetrag ist, und als Abschreibungsbetrag wird der Betrag nach der alternativen Methode übernommen.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="6b9e8-113">Da eine Anlage niemals vollständig auf Basis einer Prozentberechnung abgeschrieben wird, müssen Sie die Option „Vollständige Abschreibung“ aktivieren, um eine Anlage vollständig abzuschreiben.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="6b9e8-114">Auswählen eines Abschreibungsjahrs</span><span class="sxs-lookup"><span data-stu-id="6b9e8-114">Select a depreciation year</span></span>
<span data-ttu-id="6b9e8-115">Sie können entweder Kalender oder Steuerlich im Feld Abschreibungsjahr auf der Seite Abschreibungsprofile auswählen.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="6b9e8-116">Durch Ihre Auswahl werden die Optionen definiert, die im Feld Periodenhäufigkeit zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="6b9e8-117">Die Standardoption ist Kalender.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="6b9e8-118">Kalender</span><span class="sxs-lookup"><span data-stu-id="6b9e8-118">Calendar</span></span>

<span data-ttu-id="6b9e8-119">Mit der Option Kalender wird die Abschreibungsbasis – in der Regel der Nettobuchwert abzüglich des Schrottwerts – am 1. Januar jedes Jahres aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="6b9e8-120">Im Beispiel für degressive Abschreibung später in diesem Thema handelt es sich bei der Abschreibungsbasis um den Zähler im ersten Ausdruck in der Spalte "Berechnung".</span><span class="sxs-lookup"><span data-stu-id="6b9e8-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="6b9e8-121">Bei Auswahl der Option Kalender stehen im Feld Periodenhäufigkeit die folgenden Optionen zur Verfügung. Dieses Feld dient zum Definieren der Abgrenzung der Buchungsdaten und Beträge für Abschreibungen im Laufe des Kalenderjahrs:</span><span class="sxs-lookup"><span data-stu-id="6b9e8-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="6b9e8-122">Bei Auswahl von Jährlich erfolgt die Buchung am 31. Dezember.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="6b9e8-123">Bei Auswahl von Monatlich wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="6b9e8-124">Bei Auswahl von Vierteljährlich wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="6b9e8-125">Bei Auswahl von Halbjährlich wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="6b9e8-126">Bei Auswahl von Täglich wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="6b9e8-127">Wenn Sie z. B. Jährlich auswählen, wird die jährliche Abschreibung nur einmal am 31. Dezember eines Jahres gebucht.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="6b9e8-128">Bei Auswahl von Monatlich wird die monatliche Abschreibung jeden Monat als 1/12 des jährlichen Abschreibungsbetrags gebucht.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="6b9e8-129">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="6b9e8-129">Fiscal</span></span>

<span data-ttu-id="6b9e8-130">Wenn Sie im Feld Abschreibungsjahr die Option Steuerlich auswählen, wird die lineare Abschreibungsmethode verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="6b9e8-131">Er wird anhand des Geschäftsjahres berechnet, das auf der Seite Steuerkalender für den Steuerkalender installiert ist, der auf der Seite Sachkonto ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="6b9e8-132">Für ein Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="6b9e8-133">Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="6b9e8-134">Die Abschreibung wird für jede Steuerperiode angepasst.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="6b9e8-135">Die Länge des nächsten Geschäftsjahres basiert auf den Steuerperioden, die Sie beim Erstellen eines neuen Geschäftsjahres auf der Seite Steuerkalender einrichten.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="6b9e8-136">Bei Auswahl der Option Steuerlich stehen im Feld Periodenhäufigkeit die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="6b9e8-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="6b9e8-137">Bei Auswahl von Jährlich wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wurde, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="6b9e8-138">Steuerperiode bucht den Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wird, das in Steuerperioden aufgeteilt ist, die für den Steuerkalender definiert sind, der auf der Seite Sachkonto ausgewählt ist, oder für den Steuerkalender, der für das Wertmodell oder Abschreibungsbuch für eine Anlage ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="6b9e8-139">Beispiel für degressive Abschreibung</span><span class="sxs-lookup"><span data-stu-id="6b9e8-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="6b9e8-140">Angenommen, der Anlagenanschaffungspreis beträgt 11.000, der Schrottwert 1.000 und der Abschreibungsprozentsatz 30.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="6b9e8-141">Mithilfe der Reduktionssaldomethode werden am Ende des vorherigen Abschreibungszeitraums 30 % der Abschreibungsbasis (Nettobuchwert minus Schrottwert) berechnet.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="6b9e8-142">Die Abschreibung für die ersten drei Jahre wird in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="6b9e8-143">Periode</span><span class="sxs-lookup"><span data-stu-id="6b9e8-143">Period</span></span> | <span data-ttu-id="6b9e8-144">Berechnung des jährlichen Abschreibungsbetrags</span><span class="sxs-lookup"><span data-stu-id="6b9e8-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="6b9e8-145">Nettobuchwert am Ende des Jahres</span><span class="sxs-lookup"><span data-stu-id="6b9e8-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="6b9e8-146">Jahr 1</span><span class="sxs-lookup"><span data-stu-id="6b9e8-146">Year 1</span></span> | <span data-ttu-id="6b9e8-147">(11.000 - 1.000) \* 30% = 3.000</span><span class="sxs-lookup"><span data-stu-id="6b9e8-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="6b9e8-148">(11.000 - 1.000) - 3.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="6b9e8-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="6b9e8-149">Jahr 2</span><span class="sxs-lookup"><span data-stu-id="6b9e8-149">Year 2</span></span> | <span data-ttu-id="6b9e8-150">(7.000 - 1.000) \* 30% = 1.800</span><span class="sxs-lookup"><span data-stu-id="6b9e8-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="6b9e8-151">(7.000 - 1.800) = 5.200</span><span class="sxs-lookup"><span data-stu-id="6b9e8-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="6b9e8-152">Jahr 3</span><span class="sxs-lookup"><span data-stu-id="6b9e8-152">Year 3</span></span> | <span data-ttu-id="6b9e8-153">(5.200 - 1.000) \* 30% = 1.260</span><span class="sxs-lookup"><span data-stu-id="6b9e8-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="6b9e8-154">(5.200 - 1.260) = 3.940</span><span class="sxs-lookup"><span data-stu-id="6b9e8-154">(5,200 - 1,260) = 3,940</span></span>               |


-





