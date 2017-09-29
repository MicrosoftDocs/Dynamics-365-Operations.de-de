--- 
title: "Geplante Kanban-Einzelvorgänge verschieben"
description: "Der Schwerpunkt dieser Prozedur liegt auf dem Verschieben von geplanten Kanban-Bearbeitungseinzelvorgängen in eine andere Periode."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="06579-103">Geplante Kanban-Einzelvorgänge verschieben</span><span class="sxs-lookup"><span data-stu-id="06579-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06579-104">Der Schwerpunkt dieser Prozedur liegt auf dem Verschieben von geplanten Kanban-Bearbeitungseinzelvorgängen in eine andere Periode.</span><span class="sxs-lookup"><span data-stu-id="06579-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="06579-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="06579-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="06579-106">Dieses Verfahren ist für die Fertigungsbereichsvorgesetzten und Produktionsplaner vorgesehen, die mit Kanbans arbeiten.</span><span class="sxs-lookup"><span data-stu-id="06579-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="06579-107">Geplante Kanban-Einzelvorgänge auswählen</span><span class="sxs-lookup"><span data-stu-id="06579-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="06579-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="06579-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="06579-109">!MtCMR!Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="06579-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="06579-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="06579-110">áçêìõý !</span></span>
3. <span data-ttu-id="06579-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="06579-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="06579-112">Wählen Sie die Arbeitsgruppe 1250 aus.</span><span class="sxs-lookup"><span data-stu-id="06579-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="06579-113">Klik på Select.</span><span class="sxs-lookup"><span data-stu-id="06579-113">Klik på Select.</span></span>
5. <span data-ttu-id="06579-114">Vælg 'Planlagt' i feltet Display job status.</span><span class="sxs-lookup"><span data-stu-id="06579-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="06579-115">Dieses filtert die Einzelvorgangsliste, um nur die geplanten Kanban-Einzelvorgänge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="06579-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="06579-116">Verschieben von Kanban-Einzelvorgängen in eine andere Planungsperiode</span><span class="sxs-lookup"><span data-stu-id="06579-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="06579-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="06579-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="06579-118">Wählen Sie einen Einzelvorgang aus, der den Status "Geplante Einzelvorgänge" hat, beispielsweise einen Einzelvorgang, der für den 20. Dezember 2012 geplant war, im Feld "Geplante Periode" aus.</span><span class="sxs-lookup"><span data-stu-id="06579-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="06579-119">Verschieben Sie dann den Einzelvorgang in die vorherige Periode.</span><span class="sxs-lookup"><span data-stu-id="06579-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="06579-120">Klik på Previous period.</span><span class="sxs-lookup"><span data-stu-id="06579-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="06579-121">Klik på End.</span><span class="sxs-lookup"><span data-stu-id="06579-121">Klik på End.</span></span>
    * <span data-ttu-id="06579-122">Dies verschiebt den Einzelvorgang an das Ende der Einzelvorgangsliste als den letzten Einzelvorgang in der vorherigen Periode.</span><span class="sxs-lookup"><span data-stu-id="06579-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="06579-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="06579-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="06579-124">Wählen Sie einen Einzelvorgang aus, der den Status "Geplante Einzelvorgänge" hat, beispielsweise einen Einzelvorgang, der für den 18. Dezember 2012 geplant war, im Feld "Geplante Periode" aus.</span><span class="sxs-lookup"><span data-stu-id="06579-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="06579-125">Verschieben Sie dann den Einzelvorgang in die nächste Periode.</span><span class="sxs-lookup"><span data-stu-id="06579-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="06579-126">Klik på Next period.</span><span class="sxs-lookup"><span data-stu-id="06579-126">Klik på Next period.</span></span>
6. <span data-ttu-id="06579-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="06579-127">Klik på Start.</span></span>
    * <span data-ttu-id="06579-128">Dies verschiebt den Einzelvorgang an den Beginn der Einzelvorgangsliste als den ersten Einzelvorgang in der vorherigen Periode.</span><span class="sxs-lookup"><span data-stu-id="06579-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="06579-129">Aufgabe: Verschieben Sie einen Einzelvorgang innerhalb einer Periode</span><span class="sxs-lookup"><span data-stu-id="06579-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="06579-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="06579-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="06579-131">Wählen Sie einen Einzelvorgang aus, der den Status "Geplante Einzelvorgänge" hat, beispielsweise den zweiten Einzelvorgang, der für den 19. Dezember 2012 geplant war, im Feld "Geplante Periode" aus.</span><span class="sxs-lookup"><span data-stu-id="06579-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="06579-132">Verschieben Sie dann den Einzelvorgang in die geplante Periode.</span><span class="sxs-lookup"><span data-stu-id="06579-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="06579-133">Klik på Forward.</span><span class="sxs-lookup"><span data-stu-id="06579-133">Klik på Forward.</span></span>
    * <span data-ttu-id="06579-134">Beachten Sie, dass der Einzelvorgang um eine Position in der Liste nach unten verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="06579-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="06579-135">Klik på Backward.</span><span class="sxs-lookup"><span data-stu-id="06579-135">Klik på Backward.</span></span>
    * <span data-ttu-id="06579-136">Beachten Sie, dass der Einzelvorgang um eine Position in der Liste nach oben verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="06579-136">Notice that the job is moved one line up on the list.</span></span>  


