---
title: Manuelle Abschreibung
description: Dieser Artikel enthält eine Übersicht der manuellen Abschreibungsmethode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443435"
---
# <a name="manual-depreciation"></a><span data-ttu-id="5d8aa-103">Manuelle Abschreibung</span><span class="sxs-lookup"><span data-stu-id="5d8aa-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d8aa-104">Dieser Artikel enthält eine Übersicht der manuellen Abschreibungsmethode.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="5d8aa-105">Wenn Sie ein Anlagenabschreibungsprofil einrichten und auf der Seite **Abschreibungsprofile** im Feld **Methode** die Option **Manuell** auswählen, entspricht die Abschreibung von Anlagen, die diesem Abschreibungsprofil zugeordnet sind, dem Prozentsatz, den Sie für jedes Intervall im Kalenderjahr eingeben.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="5d8aa-106">Die Intervalle, für die Sie Prozentsätze einrichten, werden gemäß Ihrer Auswahl auf der Seite **Abschreibungsprofile** auf dem Inforegister **Allgemeines** im Feld **Periodenhäufigkeit** gebucht.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="5d8aa-107">Folgende Werte stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="5d8aa-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="5d8aa-108">Jährlich</span><span class="sxs-lookup"><span data-stu-id="5d8aa-108">Yearly</span></span>
-   <span data-ttu-id="5d8aa-109">Monatlich</span><span class="sxs-lookup"><span data-stu-id="5d8aa-109">Monthly</span></span>
-   <span data-ttu-id="5d8aa-110">Vierteljährlich</span><span class="sxs-lookup"><span data-stu-id="5d8aa-110">Quarterly</span></span>
-   <span data-ttu-id="5d8aa-111">Halbjährlich</span><span class="sxs-lookup"><span data-stu-id="5d8aa-111">Half-Yearly</span></span>
-   <span data-ttu-id="5d8aa-112">Täglich</span><span class="sxs-lookup"><span data-stu-id="5d8aa-112">Daily</span></span>

<span data-ttu-id="5d8aa-113">Klicken Sie nach Auswahl der Periodenhäufigkeit auf **Manuelle Zeitpläne**, und richten Sie Prozentsätze für jedes Buchungsintervall ein.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="5d8aa-114">Die manuellen Zeitpläne und die Buchungsintervalle definieren zusammen den Abschreibungsbetrag (siehe Beispiele weiter unten in diesem Artikel).</span><span class="sxs-lookup"><span data-stu-id="5d8aa-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="5d8aa-115">Die manuelle Abschreibung wird immer als Prozentsatz des Anschaffungspreises berechnet.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="5d8aa-116">Für manuellen Abschreibung müssen die von Ihnen für die Abschreibungsintervalle eingegebenen Prozentsätze nicht unbedingt 100 Prozent ergeben.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="5d8aa-117">Bei manueller Abschreibung handelt es sich um eine flexible Abschreibungsmethode, die häufig verwendet wird, um auf der Seite **Bücher** ein außerordentliches Abschreibungsprofil zu definieren – beispielsweise eine nicht periodische Abschreibung für besondere (ggf. steuerliche) Zwecke.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="5d8aa-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d8aa-118">Examples</span></span>
<span data-ttu-id="5d8aa-119">Anschaffungspreis: 11.000,00 Euro; Erwarteter Schrottwert: 1.000,00 Euro. Folgende Tabelle zeigt die Intervalle und Prozentsätze, die Sie auf der Seite **Zeitplan für Anlagenabschreibungsprofil** einrichten.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="5d8aa-120">Intervallnummer</span><span class="sxs-lookup"><span data-stu-id="5d8aa-120">Interval number</span></span> | <span data-ttu-id="5d8aa-121">Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="5d8aa-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="5d8aa-122">1</span><span class="sxs-lookup"><span data-stu-id="5d8aa-122">1</span></span>               | <span data-ttu-id="5d8aa-123">10,00</span><span class="sxs-lookup"><span data-stu-id="5d8aa-123">10.00</span></span>      |
| <span data-ttu-id="5d8aa-124">2</span><span class="sxs-lookup"><span data-stu-id="5d8aa-124">2</span></span>               | <span data-ttu-id="5d8aa-125">50,00</span><span class="sxs-lookup"><span data-stu-id="5d8aa-125">50.00</span></span>      |
| <span data-ttu-id="5d8aa-126">3</span><span class="sxs-lookup"><span data-stu-id="5d8aa-126">3</span></span>               | <span data-ttu-id="5d8aa-127">8,00</span><span class="sxs-lookup"><span data-stu-id="5d8aa-127">8.00</span></span>       |

<span data-ttu-id="5d8aa-128">Die folgende Tabelle zeigt, wie die Abschreibung für jedes Intervall berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="5d8aa-129">Intervallnummer</span><span class="sxs-lookup"><span data-stu-id="5d8aa-129">Interval number</span></span> | <span data-ttu-id="5d8aa-130">Berechnung des jährlichen Abschreibungsbetrags</span><span class="sxs-lookup"><span data-stu-id="5d8aa-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="5d8aa-131">Nettobuchwert am Ende des Intervalls</span><span class="sxs-lookup"><span data-stu-id="5d8aa-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="5d8aa-132">1</span><span class="sxs-lookup"><span data-stu-id="5d8aa-132">1</span></span>                | <span data-ttu-id="5d8aa-133">(11.000 – 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="5d8aa-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="5d8aa-134">10.000 (11.000 – 1.000)</span><span class="sxs-lookup"><span data-stu-id="5d8aa-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="5d8aa-135">2</span><span class="sxs-lookup"><span data-stu-id="5d8aa-135">2</span></span>                | <span data-ttu-id="5d8aa-136">(11.000 – 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="5d8aa-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="5d8aa-137">5.000 (10.000 – 5.000)</span><span class="sxs-lookup"><span data-stu-id="5d8aa-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="5d8aa-138">3</span><span class="sxs-lookup"><span data-stu-id="5d8aa-138">3</span></span>                | <span data-ttu-id="5d8aa-139">(11.000 – 1.000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="5d8aa-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="5d8aa-140">4.200 (5.000 – 800)</span><span class="sxs-lookup"><span data-stu-id="5d8aa-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="5d8aa-141">Wenn Sie im Feld **Periodenhäufigkeit** die Option **Monatlich** auswählen, haben Sie im manuellen Zeitplan 12 Intervalle eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="5d8aa-142">Die folgende Tabelle zeigt die Abschreibungsbeträge für die ersten beiden Intervalle.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="5d8aa-143">Intervall</span><span class="sxs-lookup"><span data-stu-id="5d8aa-143">Interval</span></span> | <span data-ttu-id="5d8aa-144">Abschreibungsbetrag</span><span class="sxs-lookup"><span data-stu-id="5d8aa-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="5d8aa-145">Januar</span><span class="sxs-lookup"><span data-stu-id="5d8aa-145">January</span></span>  | <span data-ttu-id="5d8aa-146">(11.000 – 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="5d8aa-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="5d8aa-147">Februar</span><span class="sxs-lookup"><span data-stu-id="5d8aa-147">February</span></span> | <span data-ttu-id="5d8aa-148">(11.000 – 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="5d8aa-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="5d8aa-149">Wenn Sie <strong>Halbjährlich</strong> im Feld *<strong><em>Periodenhäufigkeit</em>*</strong> auswählen, richten Sie zwei manuelle Zeitplanintervalle ein.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="5d8aa-150">Die folgende Tabelle zeigt die Abschreibungsbeträge für diese beiden Intervalle.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="5d8aa-151">Intervall</span><span class="sxs-lookup"><span data-stu-id="5d8aa-151">Interval</span></span>    | <span data-ttu-id="5d8aa-152">Abschreibungsbetrag</span><span class="sxs-lookup"><span data-stu-id="5d8aa-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="5d8aa-153">30. Juni</span><span class="sxs-lookup"><span data-stu-id="5d8aa-153">June 30</span></span>     | <span data-ttu-id="5d8aa-154">(11.000 – 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="5d8aa-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="5d8aa-155">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="5d8aa-155">December 31</span></span> | <span data-ttu-id="5d8aa-156">(11.000 – 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="5d8aa-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="5d8aa-157">Die Summe der Prozentsätze für alle Intervalle muss nicht unbedingt 100 ergeben.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="5d8aa-158">Allerdings wird eine Meldung angezeigt, wenn der Wert im Feld **Kumulierter Prozentsatz** Feld auf der Seite **Zeitplan für Anlagenabschreibungsprofil** ist nicht **100**.</span><span class="sxs-lookup"><span data-stu-id="5d8aa-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



