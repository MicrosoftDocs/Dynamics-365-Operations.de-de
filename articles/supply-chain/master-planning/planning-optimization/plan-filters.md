---
title: Filter auf einen Plan anwenden
description: In diesem Thema wird erläutert, wie Sie Filter auf einem Plan verwenden, wenn Sie die Funktionalität der Planungsoptimierung verwenden.
author: ChristianRytt
manager: AnnBe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ca28953846b4f1978a453d2ab2aa9759e4f45221
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076108"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="a1dc3-103">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="a1dc3-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1dc3-104">Wenn Sie die Funktionalität der Planungsoptimierung nutzen, können Sie einen Filter auf einen Plan anwenden.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="a1dc3-105">Der **Planfilter** wird immer während einer Masterplanungsausführung angewendet.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="a1dc3-106">Ein **Planfilter** ist sinnvoll, wenn Sie einen Plan auf eine bestimmte Gruppe von Positionen beschränken und sicherstellen wollen, dass keine weiteren Positionen in die resultierende Masterplanung einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="a1dc3-107">Wenn ein **Planfilter** angewendet wird und während der Masterplanungsausführung auch ein Laufzeitfilter angewendet wird, wird nur die Schnittmenge der beiden Filter in die Planungsausführung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="a1dc3-108">Der **Planungsfilter** kann über **Masterpläne** aufgerufen werden, wenn die Planungsoptimierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="a1dc3-109">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="a1dc3-109">Example scenario</span></span>

<span data-ttu-id="a1dc3-110">Es wird ein Planfilter eingerichtet, der die Positionen A, B und C enthält. Die Masterplanungsläufe werden dann für den gleichen Plan ausgeführt, wobei jedoch unterschiedliche Laufzeitfilter angewendet werden:</span><span class="sxs-lookup"><span data-stu-id="a1dc3-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="a1dc3-111">**Laufzeitfilter, der Element D enthält:** Es werden keine Elemente geplant, da es keinen Schnittpunkt zwischen dem Planfilter und dem Laufzeitfilter gibt.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="a1dc3-112">**Laufzeitfilter, der Position A und D enthält:** Nur Position A wird in den Planungslauf einbezogen, da Position D nicht Teil des Planfilters ist.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="a1dc3-113">**Laufzeitfilter, der Position B enthält:** Nur Position B wird in den Planungslauf einbezogen, und die bisherige Planungsausgabe für Position A bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="a1dc3-114">**Laufzeitfilter, der alle Positionen beinhaltet (Blindfilter):** Die Positionen A, B und C werden in den Planungslauf einbezogen, und die bisherige Planungsausgabe für die Positionen A und B wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="a1dc3-115">Sie sollten es vermeiden, einen Planfilter auf den Plan zu setzen, der als **Aktueller dynamischer Masterplan** auf der Seite **Masterplanparameter** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="a1dc3-116">Andernfalls beschränkt sich die Funktionalität des dynamischen Masterplans auf die gefilterten Elemente.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="a1dc3-117">Wenn beispielsweise der Nettobedarf für eine Position aktualisiert wird, die nicht Teil des Planfilters ist, wird kein Ergebnis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a1dc3-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="a1dc3-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a1dc3-118">Related resources</span></span>

[<span data-ttu-id="a1dc3-119">Planungsoptimierung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="a1dc3-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="a1dc3-120">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="a1dc3-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="a1dc3-121">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="a1dc3-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="a1dc3-122">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="a1dc3-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="a1dc3-123">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="a1dc3-123">Cancel a planning job</span></span>](cancel-planning-job.md)
