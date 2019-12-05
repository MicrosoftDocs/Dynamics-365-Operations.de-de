---
title: Abbrechen eines Planungsauftrags
description: In diesem Thema wird erläutert, wie Sie einen aktiven Planungseinzelvorgang stornieren, der die Funktion „Planungsoptimierung“ verwendet.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773968"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="fe6fe-103">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="fe6fe-103">Cancel a planning job</span></span>

<span data-ttu-id="fe6fe-104">In Microsoft Dynamics 365 Supply Chain Management können Sie einen aktiven Planungseinzelvorgang stornieren, der die Funktion „Planungsoptimierung“ verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="fe6fe-105">Um einen aktiven Planungseinzelvorgang zu stornieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="fe6fe-106">Es können nur aktive Aufträge abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="fe6fe-107">Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne**.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="fe6fe-108">Wählen Sie einen entsprechenden Plan für den Planungslauf aus.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="fe6fe-109">Wählen Sie **Verlauf** aus.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-109">Select **History**.</span></span>
4. <span data-ttu-id="fe6fe-110">Wählen Sie den zu stornierenden Planungseinzelvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="fe6fe-111">Wählen Sie **Abbrechen** aus.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-111">Select **Cancel**.</span></span>

<span data-ttu-id="fe6fe-112">Der Status des Einzelvorgangs lautet **Wird storniert**, bis der Planungsoptimierungsdienst bestätigt, dass der Auftrag storniert wurde.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="fe6fe-113">Der Status wird anschließend in **Storniert** geändert.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="fe6fe-114">Um Statusänderungen anzuzeigen, müssen Sie die Seite aktualisieren, indem Sie die Schaltfläche **Aktualisieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="fe6fe-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="fe6fe-115">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe6fe-115">Related resources</span></span>

[<span data-ttu-id="fe6fe-116">Planungsoptimierung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="fe6fe-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="fe6fe-117">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="fe6fe-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="fe6fe-118">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="fe6fe-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="fe6fe-119">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="fe6fe-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="fe6fe-120">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="fe6fe-120">Apply filters to a plan</span></span>](plan-filters.md)
