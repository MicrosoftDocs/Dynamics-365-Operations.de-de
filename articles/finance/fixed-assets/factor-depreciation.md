---
title: Faktorabschreibung
description: Dieser Artikel gibt einen Überblick über die Faktorabschreibungsmethode.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8adfc91251ba1707c688fac6da04adaa9af1a47f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815691"
---
# <a name="factor-depreciation"></a><span data-ttu-id="3f2de-103">Faktorabschreibung</span><span class="sxs-lookup"><span data-stu-id="3f2de-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f2de-104">Dieser Artikel gibt einen Überblick über die Faktorabschreibungsmethode.</span><span class="sxs-lookup"><span data-stu-id="3f2de-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="3f2de-105">Faktoren sind die zum Abschreiben von Anlagen verwendeten Prozentsätze.</span><span class="sxs-lookup"><span data-stu-id="3f2de-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="3f2de-106">Wenn Sie ein Anlagenabschreibungsprofil einrichten und **Faktor** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, können Sie progressive, degressive oder lineare Abschreibung einrichten:</span><span class="sxs-lookup"><span data-stu-id="3f2de-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="3f2de-107">Bei der progressiven Abschreibung nimmt der Abschreibungsbetrag mit jedem Abschreibungszeitraum zu.</span><span class="sxs-lookup"><span data-stu-id="3f2de-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="3f2de-108">Bei degressiver Abschreibung nimmt der Abschreibungsbetrag pro Zeitraum im zeitlichen Verlauf ab.</span><span class="sxs-lookup"><span data-stu-id="3f2de-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="3f2de-109">Bei der linearen Abschreibung ist die Abschreibung in jedem Zeitraum identisch.</span><span class="sxs-lookup"><span data-stu-id="3f2de-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="3f2de-110">In den nachstehenden Regeln und Beispielen wird gezeigt, wie Sie Faktoren für die einzelnen Abschreibungstypen einrichten können.</span><span class="sxs-lookup"><span data-stu-id="3f2de-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="3f2de-111">Hinweis: Wenn Sie  **Faktor** im Feld  **Methode** auswählen, werden die Felder **Faktor** und **Intervall**  angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f2de-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="3f2de-112">Progressive Abschreibung</span><span class="sxs-lookup"><span data-stu-id="3f2de-112">Progressive depreciation</span></span>
<span data-ttu-id="3f2de-113">Der Wert im Feld **Faktor** ist größer als **50**.</span><span class="sxs-lookup"><span data-stu-id="3f2de-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="3f2de-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3f2de-114">Example</span></span>

<span data-ttu-id="3f2de-115">Der Anschaffungspreis beträgt 100.000, der Faktor ist 70, die Nutzungsdauer liegt bei 10 Jahren, und die Abschreibung beginnt am 1. Januar.</span><span class="sxs-lookup"><span data-stu-id="3f2de-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="3f2de-116">Die Abschreibungsbeträge und die Nettobuchwerte werden nur für die ersten sechs Jahre der Nutzungsdauer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f2de-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="3f2de-117">Jahr</span><span class="sxs-lookup"><span data-stu-id="3f2de-117">Year</span></span> | <span data-ttu-id="3f2de-118">Periode</span><span class="sxs-lookup"><span data-stu-id="3f2de-118">Period</span></span>      | <span data-ttu-id="3f2de-119">Abschreibungsbetrag</span><span class="sxs-lookup"><span data-stu-id="3f2de-119">Depreciation amount</span></span> | <span data-ttu-id="3f2de-120">Nettobuchwert</span><span class="sxs-lookup"><span data-stu-id="3f2de-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="3f2de-121">1</span><span class="sxs-lookup"><span data-stu-id="3f2de-121">1</span></span>    | <span data-ttu-id="3f2de-122">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-122">December 31</span></span> | <span data-ttu-id="3f2de-123">307,69</span><span class="sxs-lookup"><span data-stu-id="3f2de-123">307.69</span></span>              | <span data-ttu-id="3f2de-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="3f2de-124">99,692.31</span></span>             |
| <span data-ttu-id="3f2de-125">2</span><span class="sxs-lookup"><span data-stu-id="3f2de-125">2</span></span>    | <span data-ttu-id="3f2de-126">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-126">December 31</span></span> | <span data-ttu-id="3f2de-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="3f2de-127">1,447.21</span></span>            | <span data-ttu-id="3f2de-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="3f2de-128">98,245.10</span></span>             |
| <span data-ttu-id="3f2de-129">3</span><span class="sxs-lookup"><span data-stu-id="3f2de-129">3</span></span>    | <span data-ttu-id="3f2de-130">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-130">December 31</span></span> | <span data-ttu-id="3f2de-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="3f2de-131">3,104.50</span></span>            | <span data-ttu-id="3f2de-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="3f2de-132">95,140.60</span></span>             |
| <span data-ttu-id="3f2de-133">4</span><span class="sxs-lookup"><span data-stu-id="3f2de-133">4</span></span>    | <span data-ttu-id="3f2de-134">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-134">December 31</span></span> | <span data-ttu-id="3f2de-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="3f2de-135">5,150.21</span></span>            | <span data-ttu-id="3f2de-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="3f2de-136">89,990.39</span></span>             |
| <span data-ttu-id="3f2de-137">5</span><span class="sxs-lookup"><span data-stu-id="3f2de-137">5</span></span>    | <span data-ttu-id="3f2de-138">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-138">December 31</span></span> | <span data-ttu-id="3f2de-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="3f2de-139">7,522.95</span></span>            | <span data-ttu-id="3f2de-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="3f2de-140">82,467.44</span></span>             |
| <span data-ttu-id="3f2de-141">6</span><span class="sxs-lookup"><span data-stu-id="3f2de-141">6</span></span>    | <span data-ttu-id="3f2de-142">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-142">December 31</span></span> | <span data-ttu-id="3f2de-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="3f2de-143">10,184.06</span></span>           | <span data-ttu-id="3f2de-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="3f2de-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="3f2de-145">Degressive Abschreibung</span><span class="sxs-lookup"><span data-stu-id="3f2de-145">Digressive depreciation</span></span>
<span data-ttu-id="3f2de-146">Der Wert im Feld **Faktor** ist kleiner als **50**.</span><span class="sxs-lookup"><span data-stu-id="3f2de-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="3f2de-147">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3f2de-147">Example</span></span>

<span data-ttu-id="3f2de-148">Der Anschaffungspreis beträgt 100.000, der Faktor ist 20, die Nutzungsdauer liegt bei 10 Jahren, und die Abschreibung beginnt am 1. Januar.</span><span class="sxs-lookup"><span data-stu-id="3f2de-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="3f2de-149">Die Abschreibungsbeträge und die Nettobuchwerte werden nur für die ersten sechs Jahre der Nutzungsdauer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f2de-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="3f2de-150">Jahr</span><span class="sxs-lookup"><span data-stu-id="3f2de-150">Year</span></span> | <span data-ttu-id="3f2de-151">Periode</span><span class="sxs-lookup"><span data-stu-id="3f2de-151">Period</span></span>      | <span data-ttu-id="3f2de-152">Abschreibungsbetrag</span><span class="sxs-lookup"><span data-stu-id="3f2de-152">Depreciation amount</span></span> | <span data-ttu-id="3f2de-153">Nettobuchwert</span><span class="sxs-lookup"><span data-stu-id="3f2de-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="3f2de-154">1</span><span class="sxs-lookup"><span data-stu-id="3f2de-154">1</span></span>    | <span data-ttu-id="3f2de-155">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-155">December 31</span></span> | <span data-ttu-id="3f2de-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="3f2de-156">56,080.43</span></span>           | <span data-ttu-id="3f2de-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="3f2de-157">43,919.57</span></span>             |
| <span data-ttu-id="3f2de-158">2</span><span class="sxs-lookup"><span data-stu-id="3f2de-158">2</span></span>    | <span data-ttu-id="3f2de-159">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-159">December 31</span></span> | <span data-ttu-id="3f2de-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="3f2de-160">10,665.70</span></span>           | <span data-ttu-id="3f2de-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="3f2de-161">33,253.87</span></span>             |
| <span data-ttu-id="3f2de-162">3</span><span class="sxs-lookup"><span data-stu-id="3f2de-162">3</span></span>    | <span data-ttu-id="3f2de-163">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-163">December 31</span></span> | <span data-ttu-id="3f2de-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="3f2de-164">7,156.22</span></span>            | <span data-ttu-id="3f2de-165">26.097,65</span><span class="sxs-lookup"><span data-stu-id="3f2de-165">26,097.65</span></span>             |
| <span data-ttu-id="3f2de-166">4</span><span class="sxs-lookup"><span data-stu-id="3f2de-166">4</span></span>    | <span data-ttu-id="3f2de-167">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-167">December 31</span></span> | <span data-ttu-id="3f2de-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="3f2de-168">5,538.06</span></span>            | <span data-ttu-id="3f2de-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="3f2de-169">20,559.59</span></span>             |
| <span data-ttu-id="3f2de-170">5</span><span class="sxs-lookup"><span data-stu-id="3f2de-170">5</span></span>    | <span data-ttu-id="3f2de-171">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-171">December 31</span></span> | <span data-ttu-id="3f2de-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="3f2de-172">4,579.89</span></span>            | <span data-ttu-id="3f2de-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="3f2de-173">15,979.70</span></span>             |
| <span data-ttu-id="3f2de-174">6</span><span class="sxs-lookup"><span data-stu-id="3f2de-174">6</span></span>    | <span data-ttu-id="3f2de-175">31. Dezember</span><span class="sxs-lookup"><span data-stu-id="3f2de-175">December 31</span></span> | <span data-ttu-id="3f2de-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="3f2de-176">3,937.36</span></span>            | <span data-ttu-id="3f2de-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="3f2de-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="3f2de-178">Lineare Abschreibung</span><span class="sxs-lookup"><span data-stu-id="3f2de-178">Straight line depreciation</span></span>
<span data-ttu-id="3f2de-179">Der Wert im Feld **Faktor** ist gleich **50**.</span><span class="sxs-lookup"><span data-stu-id="3f2de-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="3f2de-180">In diesem Fall ist die Abschreibung in jedem Zeitraum identisch. Sie sollten die Konsequenzen Ihrer Wertangaben in anderen Feldern entsprechend der Beschreibung in [Abschreibungsmethode "Lineare Nutzungsdauer"](straight-line-service-life-depreciation.md) berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="3f2de-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]