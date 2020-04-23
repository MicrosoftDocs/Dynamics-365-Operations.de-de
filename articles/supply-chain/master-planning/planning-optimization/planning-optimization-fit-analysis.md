---
title: Planungsoptimierung Fit-Analyse
description: In diesem Thema wird erläutert, wie Sie Ihr aktuelles Setup und Ihre Daten mit den Möglichkeiten der Planungsoptimierungsfunktionalität verifizieren können.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
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
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208753"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="69fb6-103">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="69fb6-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69fb6-104">Um zu sehen, wie kompatibel Ihr aktuelles Setup und Ihre Daten mit der Funktionalität der Planungsoptimierung sind, gehen Sie zu **Masterplanung** \> **Setup** \> **Planungsoptimierung Fit-Analyse**, und wählen Sie dann **Laufanalyse**.</span><span class="sxs-lookup"><span data-stu-id="69fb6-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="69fb6-105">Wenn die Analyse Inkonsistenzen feststellt, werden diese auf der gleichen Seite aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="69fb6-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="69fb6-106">(Die Analyse kann einige Minuten dauern.)</span><span class="sxs-lookup"><span data-stu-id="69fb6-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="69fb6-107">Wenn Inkonsistenzen festgestellt werden, können Sie die Planungsoptimierung trotzdem nutzen.</span><span class="sxs-lookup"><span data-stu-id="69fb6-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="69fb6-108">Die Ergebnisse der Fit-Analyse zeigen nur, an welchen Stellen der Planungsservice Ihr aktuelles Setup nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="69fb6-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="69fb6-109">Input</span><span class="sxs-lookup"><span data-stu-id="69fb6-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="69fb6-110">Analyseergebnisse: Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69fb6-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="69fb6-111">**Funktion:** Produktion</span><span class="sxs-lookup"><span data-stu-id="69fb6-111">**Feature:** Production</span></span>
- <span data-ttu-id="69fb6-112">**Problem:** Positionen mit Stücklistenstufe größer als Null: 56</span><span class="sxs-lookup"><span data-stu-id="69fb6-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="69fb6-113">**Erklärung:** Die Fit-Analyse ergab 56 Artikel, die eine Stückliste für die Produktion eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="69fb6-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="69fb6-114">Da die aktuelle Version der Planungsoptimierung die Produktion nicht unterstützt, erzeugt die Planungsoptimierung Planbestellungen anstelle von Planfertigungsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="69fb6-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="69fb6-115">Es wird auch eine Warnung angezeigt, die die betroffenen Elemente auflistet.</span><span class="sxs-lookup"><span data-stu-id="69fb6-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="69fb6-116">Analyseergebnisse: Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="69fb6-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="69fb6-117">**Funktion:** Aktionen</span><span class="sxs-lookup"><span data-stu-id="69fb6-117">**Feature:** Actions</span></span>
- <span data-ttu-id="69fb6-118">**Problem:** Deckungsgruppen mit aktivierter Aktionsberechnung: 6</span><span class="sxs-lookup"><span data-stu-id="69fb6-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="69fb6-119">**Erklärung:** Die Fit-Analyse ergab sechs Deckungsgruppen, in denen die Aktionsberechnung eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="69fb6-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="69fb6-120">Da die aktuelle Version der Planungsoptimierung keine Aktionen unterstützt, werden bei der Masterplanung keine Aktionen generiert.</span><span class="sxs-lookup"><span data-stu-id="69fb6-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="69fb6-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="69fb6-121">Related resources</span></span>

[<span data-ttu-id="69fb6-122">Planungsoptimierung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="69fb6-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="69fb6-123">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="69fb6-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="69fb6-124">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="69fb6-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="69fb6-125">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="69fb6-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="69fb6-126">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="69fb6-126">Cancel a planning job</span></span>](cancel-planning-job.md)
