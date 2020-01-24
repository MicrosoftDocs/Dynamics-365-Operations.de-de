---
title: Planungsoptimierung Fit-Analyse
description: In diesem Thema wird erläutert, wie Sie Ihr aktuelles Setup und Ihre Daten mit den Möglichkeiten der Planungsoptimierungsfunktionalität verifizieren können.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
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
ms.openlocfilehash: a61529da63bc20fdd591afc94db960b05c284bb9
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935874"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="7bfba-103">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="7bfba-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="7bfba-104">Um zu sehen, wie kompatibel Ihr aktuelles Setup und Ihre Daten mit der Funktionalität der Planungsoptimierung sind, gehen Sie zu **Masterplanung** \> **Setup** \> **Planungsoptimierung Fit-Analyse**, und wählen Sie dann **Laufanalyse**.</span><span class="sxs-lookup"><span data-stu-id="7bfba-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="7bfba-105">Wenn die Analyse Inkonsistenzen feststellt, werden diese auf der gleichen Seite aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7bfba-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="7bfba-106">(Die Analyse kann einige Minuten dauern.)</span><span class="sxs-lookup"><span data-stu-id="7bfba-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="7bfba-107">Wenn Inkonsistenzen festgestellt werden, können Sie die Planungsoptimierung trotzdem nutzen.</span><span class="sxs-lookup"><span data-stu-id="7bfba-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="7bfba-108">Die Ergebnisse der Fit-Analyse zeigen nur, an welchen Stellen der Planungsservice Ihr aktuelles Setup nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="7bfba-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="7bfba-109">Input</span><span class="sxs-lookup"><span data-stu-id="7bfba-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="7bfba-110">Analyseergebnisse: Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bfba-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="7bfba-111">**Funktion:** Produktion</span><span class="sxs-lookup"><span data-stu-id="7bfba-111">**Feature:** Production</span></span>
- <span data-ttu-id="7bfba-112">**Problem:** Positionen mit Stücklistenstufe größer als Null: 56</span><span class="sxs-lookup"><span data-stu-id="7bfba-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="7bfba-113">**Erklärung:** Die Fit-Analyse ergab 56 Artikel, die eine Stückliste für die Produktion eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="7bfba-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="7bfba-114">Da die aktuelle Version der Planungsoptimierung die Produktion nicht unterstützt, erzeugt die Planungsoptimierung Planbestellungen anstelle von Planfertigungsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="7bfba-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="7bfba-115">Es wird auch eine Warnung angezeigt, die die betroffenen Elemente auflistet.</span><span class="sxs-lookup"><span data-stu-id="7bfba-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="7bfba-116">Analyseergebnisse: Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7bfba-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="7bfba-117">**Funktion:** Aktionen</span><span class="sxs-lookup"><span data-stu-id="7bfba-117">**Feature:** Actions</span></span>
- <span data-ttu-id="7bfba-118">**Problem:** Deckungsgruppen mit aktivierter Aktionsberechnung: 6</span><span class="sxs-lookup"><span data-stu-id="7bfba-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="7bfba-119">**Erklärung:** Die Fit-Analyse ergab sechs Deckungsgruppen, in denen die Aktionsberechnung eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="7bfba-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="7bfba-120">Da die aktuelle Version der Planungsoptimierung keine Aktionen unterstützt, werden bei der Masterplanung keine Aktionen generiert.</span><span class="sxs-lookup"><span data-stu-id="7bfba-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="7bfba-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7bfba-121">Related resources</span></span>

[<span data-ttu-id="7bfba-122">Planungsoptimierung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="7bfba-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="7bfba-123">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="7bfba-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="7bfba-124">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="7bfba-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="7bfba-125">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="7bfba-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="7bfba-126">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="7bfba-126">Cancel a planning job</span></span>](cancel-planning-job.md)
