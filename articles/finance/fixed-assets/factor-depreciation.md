---
title: Faktorabschreibung
description: Dieser Artikel gibt einen Überblick über die Faktorabschreibungsmethode.
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
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87cca8b3472f572cd1c4ba3d894269f7ba0f248a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241073"
---
# <a name="factor-depreciation"></a><span data-ttu-id="e7957-103">Faktorabschreibung</span><span class="sxs-lookup"><span data-stu-id="e7957-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7957-104">Dieser Artikel gibt einen Überblick über die Faktorabschreibungsmethode.</span><span class="sxs-lookup"><span data-stu-id="e7957-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="e7957-105">Faktoren sind die zum Abschreiben von Anlagen verwendeten Prozentsätze.</span><span class="sxs-lookup"><span data-stu-id="e7957-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="e7957-106">Wenn Sie ein Anlagenabschreibungsprofil einrichten und **Faktor** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, können Sie progressive, degressive oder lineare Abschreibung einrichten:</span><span class="sxs-lookup"><span data-stu-id="e7957-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="e7957-107">Bei der progressiven Abschreibung nimmt der Abschreibungsbetrag mit jedem Abschreibungszeitraum zu.</span><span class="sxs-lookup"><span data-stu-id="e7957-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="e7957-108">Bei degressiver Abschreibung nimmt der Abschreibungsbetrag pro Zeitraum im zeitlichen Verlauf ab.</span><span class="sxs-lookup"><span data-stu-id="e7957-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="e7957-109">Bei der linearen Abschreibung ist die Abschreibung in jedem Zeitraum identisch.</span><span class="sxs-lookup"><span data-stu-id="e7957-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="e7957-110">In den nachstehenden Regeln und Beispielen wird gezeigt, wie Sie Faktoren für die einzelnen Abschreibungstypen einrichten können.</span><span class="sxs-lookup"><span data-stu-id="e7957-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="e7957-111">Hinweis: Wenn Sie  **Faktor** im Feld  **Methode** auswählen, werden die Felder **Faktor** und **Intervall**  angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7957-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="e7957-112">Progressive Abschreibung</span><span class="sxs-lookup"><span data-stu-id="e7957-112">Progressive depreciation</span></span>
<span data-ttu-id="e7957-113">Der Wert im Feld **Faktor** ist größer als **50**.</span><span class="sxs-lookup"><span data-stu-id="e7957-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="e7957-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7957-114">Example</span></span>

<span data-ttu-id="e7957-115">Der Anschaffungspreis beträgt 100.000, der Faktor ist 70, die Nutzungsdauer liegt bei 10 Jahren, und die Abschreibung beginnt am 1. Januar.</span><span class="sxs-lookup"><span data-stu-id="e7957-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="e7957-116">Die Abschreibungsbeträge und die Nettobuchwerte werden nur für die ersten sechs Jahre der Nutzungsdauer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7957-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="e7957-117">Jahr</span><span class="sxs-lookup"><span data-stu-id="e7957-117">Year</span></span> | <span data-ttu-id="e7957-118">Periode</span><span class="sxs-lookup"><span data-stu-id="e7957-118">Period</span></span>      | <span data-ttu-id="e7957-119">Abschreibungsbetrag</span><span class="sxs-lookup"><span data-stu-id="e7957-119">Depreciation amount</span></span> | <span data-ttu-id="e7957-120">Nettobuchwert</span><span class="sxs-lookup"><span data-stu-id="e7957-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="e7957-121">1</span><span class="sxs-lookup"><span data-stu-id="e7957-121">1</span></span>    | <span data-ttu-id="e7957-122">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-122">December 31</span></span> | <span data-ttu-id="e7957-123">307,69</span><span class="sxs-lookup"><span data-stu-id="e7957-123">307.69</span></span>              | <span data-ttu-id="e7957-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="e7957-124">99,692.31</span></span>             |
| <span data-ttu-id="e7957-125">2</span><span class="sxs-lookup"><span data-stu-id="e7957-125">2</span></span>    | <span data-ttu-id="e7957-126">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-126">December 31</span></span> | <span data-ttu-id="e7957-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="e7957-127">1,447.21</span></span>            | <span data-ttu-id="e7957-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="e7957-128">98,245.10</span></span>             |
| <span data-ttu-id="e7957-129">3</span><span class="sxs-lookup"><span data-stu-id="e7957-129">3</span></span>    | <span data-ttu-id="e7957-130">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-130">December 31</span></span> | <span data-ttu-id="e7957-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="e7957-131">3,104.50</span></span>            | <span data-ttu-id="e7957-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="e7957-132">95,140.60</span></span>             |
| <span data-ttu-id="e7957-133">4</span><span class="sxs-lookup"><span data-stu-id="e7957-133">4</span></span>    | <span data-ttu-id="e7957-134">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-134">December 31</span></span> | <span data-ttu-id="e7957-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="e7957-135">5,150.21</span></span>            | <span data-ttu-id="e7957-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="e7957-136">89,990.39</span></span>             |
| <span data-ttu-id="e7957-137">5</span><span class="sxs-lookup"><span data-stu-id="e7957-137">5</span></span>    | <span data-ttu-id="e7957-138">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-138">December 31</span></span> | <span data-ttu-id="e7957-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="e7957-139">7,522.95</span></span>            | <span data-ttu-id="e7957-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="e7957-140">82,467.44</span></span>             |
| <span data-ttu-id="e7957-141">6</span><span class="sxs-lookup"><span data-stu-id="e7957-141">6</span></span>    | <span data-ttu-id="e7957-142">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-142">December 31</span></span> | <span data-ttu-id="e7957-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="e7957-143">10,184.06</span></span>           | <span data-ttu-id="e7957-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="e7957-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="e7957-145">Degressive Abschreibung</span><span class="sxs-lookup"><span data-stu-id="e7957-145">Digressive depreciation</span></span>
<span data-ttu-id="e7957-146">Der Wert im Feld **Faktor** ist kleiner als **50**.</span><span class="sxs-lookup"><span data-stu-id="e7957-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="e7957-147">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7957-147">Example</span></span>

<span data-ttu-id="e7957-148">Der Anschaffungspreis beträgt 100.000, der Faktor ist 20, die Nutzungsdauer liegt bei 10 Jahren, und die Abschreibung beginnt am 1. Januar.</span><span class="sxs-lookup"><span data-stu-id="e7957-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="e7957-149">Die Abschreibungsbeträge und die Nettobuchwerte werden nur für die ersten sechs Jahre der Nutzungsdauer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7957-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="e7957-150">Jahr</span><span class="sxs-lookup"><span data-stu-id="e7957-150">Year</span></span> | <span data-ttu-id="e7957-151">Periode</span><span class="sxs-lookup"><span data-stu-id="e7957-151">Period</span></span>      | <span data-ttu-id="e7957-152">Abschreibungsbetrag</span><span class="sxs-lookup"><span data-stu-id="e7957-152">Depreciation amount</span></span> | <span data-ttu-id="e7957-153">Nettobuchwert</span><span class="sxs-lookup"><span data-stu-id="e7957-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="e7957-154">1</span><span class="sxs-lookup"><span data-stu-id="e7957-154">1</span></span>    | <span data-ttu-id="e7957-155">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-155">December 31</span></span> | <span data-ttu-id="e7957-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="e7957-156">56,080.43</span></span>           | <span data-ttu-id="e7957-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="e7957-157">43,919.57</span></span>             |
| <span data-ttu-id="e7957-158">2</span><span class="sxs-lookup"><span data-stu-id="e7957-158">2</span></span>    | <span data-ttu-id="e7957-159">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-159">December 31</span></span> | <span data-ttu-id="e7957-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="e7957-160">10,665.70</span></span>           | <span data-ttu-id="e7957-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="e7957-161">33,253.87</span></span>             |
| <span data-ttu-id="e7957-162">3</span><span class="sxs-lookup"><span data-stu-id="e7957-162">3</span></span>    | <span data-ttu-id="e7957-163">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-163">December 31</span></span> | <span data-ttu-id="e7957-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="e7957-164">7,156.22</span></span>            | <span data-ttu-id="e7957-165">26.097,65</span><span class="sxs-lookup"><span data-stu-id="e7957-165">26,097.65</span></span>             |
| <span data-ttu-id="e7957-166">4</span><span class="sxs-lookup"><span data-stu-id="e7957-166">4</span></span>    | <span data-ttu-id="e7957-167">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-167">December 31</span></span> | <span data-ttu-id="e7957-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="e7957-168">5,538.06</span></span>            | <span data-ttu-id="e7957-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="e7957-169">20,559.59</span></span>             |
| <span data-ttu-id="e7957-170">5</span><span class="sxs-lookup"><span data-stu-id="e7957-170">5</span></span>    | <span data-ttu-id="e7957-171">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-171">December 31</span></span> | <span data-ttu-id="e7957-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="e7957-172">4,579.89</span></span>            | <span data-ttu-id="e7957-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="e7957-173">15,979.70</span></span>             |
| <span data-ttu-id="e7957-174">6</span><span class="sxs-lookup"><span data-stu-id="e7957-174">6</span></span>    | <span data-ttu-id="e7957-175">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="e7957-175">December 31</span></span> | <span data-ttu-id="e7957-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="e7957-176">3,937.36</span></span>            | <span data-ttu-id="e7957-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="e7957-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="e7957-178">Lineare Abschreibung</span><span class="sxs-lookup"><span data-stu-id="e7957-178">Straight line depreciation</span></span>
<span data-ttu-id="e7957-179">Der Wert im Feld **Faktor** ist gleich **50**.</span><span class="sxs-lookup"><span data-stu-id="e7957-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="e7957-180">In diesem Fall ist die Abschreibung in jedem Zeitraum identisch. Sie sollten die Konsequenzen Ihrer Wertangaben in anderen Feldern entsprechend der Beschreibung in [Abschreibungsmethode "Lineare Nutzungsdauer"](straight-line-service-life-depreciation.md) berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="e7957-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]