---
title: Filter auf einen Plan anwenden
description: In diesem Thema wird erläutert, wie Sie Filter auf einem Plan verwenden, wenn Sie die Funktionalität der Planungsoptimierung verwenden.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 73e4a045ff5a9912b898a7115d3d8f530846ebdd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209788"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="40311-103">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="40311-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40311-104">Wenn Sie die Funktionalität der Planungsoptimierung nutzen, können Sie einen Filter auf einen Plan anwenden.</span><span class="sxs-lookup"><span data-stu-id="40311-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="40311-105">Der **Planfilter** wird immer während einer Masterplanungsausführung angewendet.</span><span class="sxs-lookup"><span data-stu-id="40311-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="40311-106">Ein **Planfilter** ist sinnvoll, wenn Sie einen Plan auf eine bestimmte Gruppe von Positionen beschränken und sicherstellen wollen, dass keine weiteren Positionen in die resultierende Masterplanung einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="40311-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="40311-107">Wenn ein **Planfilter** angewendet wird und während der Masterplanungsausführung auch ein Laufzeitfilter angewendet wird, wird nur die Schnittmenge der beiden Filter in die Planungsausführung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="40311-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="40311-108">Der **Planungsfilter** kann über **Masterpläne** aufgerufen werden, wenn die Planungsoptimierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40311-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="40311-109">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="40311-109">Example scenario</span></span>

<span data-ttu-id="40311-110">Es wird ein Planfilter eingerichtet, der die Positionen A, B und C enthält. Die Masterplanungsläufe werden dann für den gleichen Plan ausgeführt, wobei jedoch unterschiedliche Laufzeitfilter angewendet werden:</span><span class="sxs-lookup"><span data-stu-id="40311-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="40311-111">**Laufzeitfilter, der Element D enthält:** Es werden keine Elemente geplant, da es keinen Schnittpunkt zwischen dem Planfilter und dem Laufzeitfilter gibt.</span><span class="sxs-lookup"><span data-stu-id="40311-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="40311-112">**Laufzeitfilter, der Position A und D enthält:** Nur Position A wird in den Planungslauf einbezogen, da Position D nicht Teil des Planfilters ist.</span><span class="sxs-lookup"><span data-stu-id="40311-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="40311-113">**Laufzeitfilter, der Position B enthält:** Nur Position B wird in den Planungslauf einbezogen, und die bisherige Planungsausgabe für Position A bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="40311-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="40311-114">**Laufzeitfilter, der alle Positionen beinhaltet (Blindfilter):** Die Positionen A, B und C werden in den Planungslauf einbezogen, und die bisherige Planungsausgabe für die Positionen A und B wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="40311-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="40311-115">Sie sollten es vermeiden, einen Planfilter auf den Plan zu setzen, der als **Aktueller dynamischer Masterplan** auf der Seite **Masterplanparameter** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="40311-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="40311-116">Andernfalls beschränkt sich die Funktionalität des dynamischen Masterplans auf die gefilterten Elemente.</span><span class="sxs-lookup"><span data-stu-id="40311-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="40311-117">Wenn beispielsweise der Nettobedarf für eine Position aktualisiert wird, die nicht Teil des Planfilters ist, wird kein Ergebnis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="40311-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="40311-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40311-118">Related resources</span></span>

[<span data-ttu-id="40311-119">Planungsoptimierung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="40311-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="40311-120">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="40311-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="40311-121">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="40311-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="40311-122">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="40311-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="40311-123">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="40311-123">Cancel a planning job</span></span>](cancel-planning-job.md)
