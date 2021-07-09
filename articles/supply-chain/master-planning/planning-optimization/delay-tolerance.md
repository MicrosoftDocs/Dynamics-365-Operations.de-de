---
title: Verzögerungstoleranz (negative Tage)
description: Dieses Thema enthält Informationen über die Berechnung der Verzögerungstoleranz und wie sie sich auf die Erstellung geplanter Aufträge in der Planungsoptimierung auswirkt.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306462"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="74a20-103">Verzögerungstoleranz (negative Tage)</span><span class="sxs-lookup"><span data-stu-id="74a20-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="74a20-104">Die Verzögerungstoleranz-Funktionalität ermöglicht der Planungsoptimierung, den Wert **Negative Tage** zu berücksichtigen, der für Deckungsgruppen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="74a20-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="74a20-105">Sie wird verwendet, um die Verzögerungstoleranz zu verlängern, die während der Produktprogrammplanung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="74a20-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="74a20-106">Auf diese Weise können Sie vermeiden, neue Vorräte zu erstellen, wenn der vorhandene Vorrat den Bedarf nach einer kurzen Verzögerung decken kann.</span><span class="sxs-lookup"><span data-stu-id="74a20-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="74a20-107">Der Zweck der Funktionalität besteht darin, festzustellen, ob es sinnvoll ist, einen neuen Vorrat für einen bestimmten Bedarf zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="74a20-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="74a20-108">Funktion in Ihrem System aktivieren</span><span class="sxs-lookup"><span data-stu-id="74a20-108">Turn on the feature in your system</span></span>

<span data-ttu-id="74a20-109">Um die Verzögerungstoleranz-Funktionalität in Ihrem System verfügbar zu machen, gehen Sie zu [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Negative Tage für Planungsoptimierung* ein.</span><span class="sxs-lookup"><span data-stu-id="74a20-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="74a20-110">Verzögerungstoleranz in der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="74a20-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="74a20-111">Die Verzögerungstoleranz stellt die Anzahl der Tage über die Vorlaufzeit hinaus dar, die Sie bereit sind, zu warten, bevor Sie eine neue Wiederbeschaffung bestellen, wenn die bestehende Beschaffung bereits geplant ist.</span><span class="sxs-lookup"><span data-stu-id="74a20-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="74a20-112">Die Verzögerungstoleranz wird durch die Verwendung von Kalendertagen und nicht von Geschäftstagen definiert.</span><span class="sxs-lookup"><span data-stu-id="74a20-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="74a20-113">Zum Zeitpunkt der Produktprogrammplanung, wenn das System die Verzögerungstoleranz berechnet, berücksichtigt es die Einstellung **Negative Tage**.</span><span class="sxs-lookup"><span data-stu-id="74a20-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="74a20-114">Sie können den Wert **Negative Tage** entweder auf der Seite **Abdeckungsgruppen** oder auf der Seite **Elementabdeckung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="74a20-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="74a20-115">Das System verknüpft die Berechnung der Verzögerungstoleranz mit dem *frühesten Datum der Wiederbeschaffung*, das dem heutigen Datum plus der Vorlaufzeit entspricht.</span><span class="sxs-lookup"><span data-stu-id="74a20-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="74a20-116">Die Verzögerungstoleranz wird mit Hilfe der folgenden Formel berechnet, wobei *max()* den größeren von zwei Werten findet:</span><span class="sxs-lookup"><span data-stu-id="74a20-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="74a20-117">*max(Frühestes Wiederbeschaffungsdatum, Fälligkeitsdatum des Bedarfs)* – *Fälligkeitsdatum des Bedarfs* + *Negative Tage*</span><span class="sxs-lookup"><span data-stu-id="74a20-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="74a20-118">Diese Formel stellt sicher, dass die Produktprogrammplanung keine neuen Vorratsaufträge erstellt, wenn während der Vorlaufzeit des Produkts genügend Vorrat vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="74a20-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="74a20-119">Die Berechnung der Verzugstoleranz in der Planungsoptimierung verwendet immer die dynamische Berechnung der negativen Tage aus der integrierten Produktprogrammplanung.</span><span class="sxs-lookup"><span data-stu-id="74a20-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="74a20-120">Die Einstellung **Dynamische negative Tage verwenden** auf der Seite **Parameter der Produktprogrammplanung** hat keinen Einfluss auf dieses Verhalten.</span><span class="sxs-lookup"><span data-stu-id="74a20-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="74a20-121">Wenn der vorhandene Vorrat eine Verzögerung des Bedarfs impliziert, die kleiner oder gleich der berechneten Verzögerungstoleranz ist, koppelt die Planungsoptimierung den vorhandenen Vorrat an den Bedarf.</span><span class="sxs-lookup"><span data-stu-id="74a20-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="74a20-122">In einigen Fällen ist es besser, den Bedarf zu verzögern, als mit einem Überangebot zu enden.</span><span class="sxs-lookup"><span data-stu-id="74a20-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="74a20-123">In den folgenden Unterabschnitten finden Sie Beispiele, die zeigen, wie sich die Verzögerungstoleranz auf die Erstellung von geplanten Aufträgen in der Planungsoptimierung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="74a20-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="74a20-124">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74a20-124">Example 1</span></span>

<span data-ttu-id="74a20-125">Ein Produkt hat die folgende Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="74a20-125">A product has the following configuration:</span></span>

- <span data-ttu-id="74a20-126">**Vorlaufzeit:** *10*</span><span class="sxs-lookup"><span data-stu-id="74a20-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="74a20-127">**Negative Tage:** *2*</span><span class="sxs-lookup"><span data-stu-id="74a20-127">**Negative days:** *2*</span></span>

<span data-ttu-id="74a20-128">Für das Produkt bestehen der folgende Vorrat und Bedarf:</span><span class="sxs-lookup"><span data-stu-id="74a20-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="74a20-129">**Bedarf für heute:** Ein Verkaufsauftrag für eine Menge von 10</span><span class="sxs-lookup"><span data-stu-id="74a20-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="74a20-130">**Vorrat in 12 Tagen:** Eine Einkaufsbestellung für eine Menge von 10</span><span class="sxs-lookup"><span data-stu-id="74a20-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="74a20-131">Der vorhandene Vorrat kann den Bedarf innerhalb von 12 Tagen decken, und dieser Zeitraum entspricht der Verzögerungstoleranz.</span><span class="sxs-lookup"><span data-stu-id="74a20-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="74a20-132">Wenn die Produktprogrammplanung ausgeführt wird, werden daher keine geplanter Aufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="74a20-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="74a20-133">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="74a20-133">Example 2</span></span>

<span data-ttu-id="74a20-134">Ein Produkt hat die folgende Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="74a20-134">A product has the following configuration:</span></span>

- <span data-ttu-id="74a20-135">**Vorlaufzeit:** *10*</span><span class="sxs-lookup"><span data-stu-id="74a20-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="74a20-136">**Negative Tage:** *0*</span><span class="sxs-lookup"><span data-stu-id="74a20-136">**Negative days:** *0*</span></span>

<span data-ttu-id="74a20-137">Für das Produkt bestehen der folgende Vorrat und Bedarf:</span><span class="sxs-lookup"><span data-stu-id="74a20-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="74a20-138">**Bedarf für heute:** Ein Verkaufsauftrag für eine Menge von 10</span><span class="sxs-lookup"><span data-stu-id="74a20-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="74a20-139">**Vorrat in 12 Tagen:** Eine Einkaufsbestellung für eine Menge von 10</span><span class="sxs-lookup"><span data-stu-id="74a20-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="74a20-140">Der vorhandene Vorrat kann den Bedarf erst nach 12 Tagen decken.</span><span class="sxs-lookup"><span data-stu-id="74a20-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="74a20-141">Die Verzögerungstoleranz beträgt jedoch 10 Tage.</span><span class="sxs-lookup"><span data-stu-id="74a20-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="74a20-142">Wenn die Produktprogrammplanung ausgeführt wird, wird daher ein geplanter Auftrag für eine Menge von 10 erstellt.</span><span class="sxs-lookup"><span data-stu-id="74a20-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="74a20-143">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="74a20-143">Example 3</span></span>

<span data-ttu-id="74a20-144">Ein Produkt hat die folgende Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="74a20-144">A product has the following configuration:</span></span>

- <span data-ttu-id="74a20-145">**Vorlaufzeit:** *10*</span><span class="sxs-lookup"><span data-stu-id="74a20-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="74a20-146">**Negative Tage:** *2*</span><span class="sxs-lookup"><span data-stu-id="74a20-146">**Negative days:** *2*</span></span>

<span data-ttu-id="74a20-147">Für das Produkt bestehen der folgende Vorrat und Bedarf:</span><span class="sxs-lookup"><span data-stu-id="74a20-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="74a20-148">**Bedarf in 11 Tagen:** Ein Verkaufsauftrag für eine Menge von 10</span><span class="sxs-lookup"><span data-stu-id="74a20-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="74a20-149">**Nachschub in 14 Tagen:** Eine Einkaufsbestellung für eine Menge von 10</span><span class="sxs-lookup"><span data-stu-id="74a20-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="74a20-150">Der vorhandene Vorrat kann den Bedarf erst nach drei Tagen decken.</span><span class="sxs-lookup"><span data-stu-id="74a20-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="74a20-151">Die Verzögerungstoleranz beträgt jedoch zwei Tage.</span><span class="sxs-lookup"><span data-stu-id="74a20-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="74a20-152">(In diesem Fall umfasst die Verzögerungstoleranz nur die beiden negativen Tage.</span><span class="sxs-lookup"><span data-stu-id="74a20-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="74a20-153">Das Datum des Bedarfs wird nicht berücksichtigt, da es nach der Vorlaufzeit des Produkts liegt.) Wenn die Produktprogrammplanung ausgeführt wird, wird daher ein geplanter Auftrag für eine Menge von 10 erstellt.</span><span class="sxs-lookup"><span data-stu-id="74a20-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
