---
title: Planung mit negativen Vorgabemengen
description: In diesem Thema wird erläutert, wie mit dem Negativ-Bestand umgegangen wird, wenn Sie die Planungsoptimierung einsetzen.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1c403e23309dda36dd1c99e22bbae0aa2d6d76a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813098"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="6adf0-103">Planung mit negativen Vorgabemengen</span><span class="sxs-lookup"><span data-stu-id="6adf0-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6adf0-104">Wenn das System eine negative aggregierte Bestandsmenge anzeigt, behandelt die Planungsmaschine die Menge als 0 (Null), um ein Überangebot zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6adf0-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="6adf0-105">Im Folgenden wird erläutert, wie diese Funktionalität funktioniert:</span><span class="sxs-lookup"><span data-stu-id="6adf0-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="6adf0-106">Die Planungsoptimierung aggregiert die Bestandsmengen auf der untersten Ebene der Deckungsdimensionen.</span><span class="sxs-lookup"><span data-stu-id="6adf0-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="6adf0-107">(Wenn z.B. *Lagerplatz* keine Deckungsdimension ist, aggregiert die Planungsoptimierung die verfügbaren Mengen auf der Ebene *Lager*).</span><span class="sxs-lookup"><span data-stu-id="6adf0-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="6adf0-108">Wenn die aggregierte Bestandsmenge auf der untersten Ebene der Deckungsdimensionen negativ ist, geht das System davon aus, dass die Bestandsmenge tatsächlich 0 (Null) ist.</span><span class="sxs-lookup"><span data-stu-id="6adf0-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6adf0-109">Das Planungssystem kann nur so genau sein wie die Eingabedaten.</span><span class="sxs-lookup"><span data-stu-id="6adf0-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="6adf0-110">Wenn die Eingabedaten ungenau sind, zeigen negative Datensätze auf dem Datenbestand an, dass die Bestandsinformationen in Microsoft Dynamics 365 Supply Chain Management nicht mit der realen Welt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6adf0-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="6adf0-111">Daher wird das Planungsergebnis fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="6adf0-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="6adf0-112">Um ein präzises Planungsergebnis zu erhalten, sollten Sie die Anzahl der Datensätze, die eine negative Bestandsmenge aufweisen, minimieren.</span><span class="sxs-lookup"><span data-stu-id="6adf0-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="6adf0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6adf0-113">Example 1</span></span>

<span data-ttu-id="6adf0-114">Lager 13 ist wie folgt konfiguriert:</span><span class="sxs-lookup"><span data-stu-id="6adf0-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="6adf0-115">**Deckungscode:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="6adf0-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="6adf0-116">**Minimum:** 15 Stück (Stk.)</span><span class="sxs-lookup"><span data-stu-id="6adf0-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="6adf0-117">**Maximal:** 25 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="6adf0-118">Die niedrigste Ebene der Deckungsdimensionen ist *Lager*, und die folgenden vorrätigen Mengen werden auf der Ebene *Lagerplatz* erfasst:</span><span class="sxs-lookup"><span data-stu-id="6adf0-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="6adf0-119">**Standort 1, Lager 13, Lagerplatz 1:** 20 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="6adf0-120">**Standort 1 Lager 13, Lagerplatz 2:** &minus;8 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="6adf0-121">Somit beträgt die aggregierte Bestandsmenge für Lager 13 12 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="6adf0-122">(= 20 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-122">(= 20 pcs.</span></span> <span data-ttu-id="6adf0-123">&minus; 8 Stk.).</span><span class="sxs-lookup"><span data-stu-id="6adf0-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="6adf0-124">In diesem Fall verwendet die Planungsmaschine eine Aggregat-Bestandsmenge von 12 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="6adf0-125">für Lager 13.</span><span class="sxs-lookup"><span data-stu-id="6adf0-125">for warehouse 13.</span></span>

<span data-ttu-id="6adf0-126">Das Ergebnis ist ein Planauftrag von 13 Stück.</span><span class="sxs-lookup"><span data-stu-id="6adf0-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="6adf0-127">(= 25 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-127">(= 25 pcs.</span></span> <span data-ttu-id="6adf0-128">&minus; 12 Stk.), um Lager 13 aus 12 Stk. wieder aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="6adf0-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="6adf0-129">auf 25 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="6adf0-130">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6adf0-130">Example 2</span></span>

<span data-ttu-id="6adf0-131">Lager 13 ist wie folgt konfiguriert:</span><span class="sxs-lookup"><span data-stu-id="6adf0-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="6adf0-132">**Abdeckungscode:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="6adf0-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="6adf0-133">**Minimum:** 15 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="6adf0-134">**Maximum:** 25 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="6adf0-135">Die niedrigste Ebene der Deckungsdimensionen ist *Lager*, und die folgenden vorrätigen Mengen werden auf der Ebene *Lagerplatz* erfasst:</span><span class="sxs-lookup"><span data-stu-id="6adf0-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="6adf0-136">**Standort 1, Lager 13, Lagerplatz 1:** 4 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="6adf0-137">**Standort 1 Lager 13, Lagerplatz 2:** &minus;8 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="6adf0-138">Daher beträgt die gesamte verfügbare Menge für Lager 13 &minus;4 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="6adf0-139">(= 4 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-139">(= 4 pcs.</span></span> <span data-ttu-id="6adf0-140">&minus; 8 Stk.).</span><span class="sxs-lookup"><span data-stu-id="6adf0-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="6adf0-141">Mit anderen Worten, sie ist weniger als 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="6adf0-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="6adf0-142">In diesem Fall geht das Planungsmodul davon aus, dass die vorrätige Menge für Lager 13 0 St. beträgt.</span><span class="sxs-lookup"><span data-stu-id="6adf0-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="6adf0-143">statt &minus;4 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="6adf0-144">Das Ergebnis ist ein Planauftrag von 25 Stück.</span><span class="sxs-lookup"><span data-stu-id="6adf0-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="6adf0-145">(= 25 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-145">(= 25 pcs.</span></span> <span data-ttu-id="6adf0-146">&minus; 0 Stk.), um Lager 13 aus 0 Stk. wieder aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="6adf0-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="6adf0-147">bis 25 Stk.</span><span class="sxs-lookup"><span data-stu-id="6adf0-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="6adf0-148">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6adf0-148">Related resources</span></span>

[<span data-ttu-id="6adf0-149">Übersicht zur Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="6adf0-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="6adf0-150">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="6adf0-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="6adf0-151">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="6adf0-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="6adf0-152">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="6adf0-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="6adf0-153">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="6adf0-153">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]