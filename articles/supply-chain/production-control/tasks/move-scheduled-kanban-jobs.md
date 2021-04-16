---
title: Geplante Kanban-Einzelvorgänge verschieben
description: Der Schwerpunkt dieser Prozedur liegt auf dem Verschieben von geplanten Kanban-Bearbeitungseinzelvorgängen in eine andere Periode.
author: ChristianRytt
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d58ee740824809f15da68db66616bb01d5dbfab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825013"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="50290-103">Geplante Kanban-Einzelvorgänge verschieben</span><span class="sxs-lookup"><span data-stu-id="50290-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50290-104">Der Schwerpunkt dieser Prozedur liegt auf dem Verschieben von geplanten Kanban-Bearbeitungseinzelvorgängen in eine andere Periode.</span><span class="sxs-lookup"><span data-stu-id="50290-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="50290-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="50290-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="50290-106">Dieses Verfahren ist für die Fertigungsbereichsvorgesetzten und Produktionsplaner vorgesehen, die mit Kanbans arbeiten.</span><span class="sxs-lookup"><span data-stu-id="50290-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="50290-107">Wählen Sie geplante Kanban-Einzelvorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="50290-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="50290-108">Wechseln Sie zu **Produktionssteuerung > Kanban > Kanban-Einzelvorgangsplanung**.</span><span class="sxs-lookup"><span data-stu-id="50290-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="50290-109">Klicken Sie im Feld **Arbeitsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="50290-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="50290-110">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="50290-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="50290-111">Wählen Sie die Arbeitsgruppe 1250 aus.</span><span class="sxs-lookup"><span data-stu-id="50290-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="50290-112">Klicken Sie auf **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="50290-112">Click **Select**.</span></span> 

5. <span data-ttu-id="50290-113">Wählen Sie im Feld **Einzelvorgangsstatus anzeigen** die Option **Geplant** aus.</span><span class="sxs-lookup"><span data-stu-id="50290-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="50290-114">Dieses filtert die Einzelvorgangsliste, um nur die geplanten Kanban-Einzelvorgänge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="50290-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="50290-115">Verschieben Sie Kanban-Einzelvorgänge in eine andere Periode.</span><span class="sxs-lookup"><span data-stu-id="50290-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="50290-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="50290-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="50290-117">Wählen Sie einen Einzelvorgang aus, der den Status **Geplanter Einzelvorgang** hat, beispielsweise einen Einzelvorgang, der für den 20. Dezember 2012 geplant war, im Feld **Geplante Periode** aus.</span><span class="sxs-lookup"><span data-stu-id="50290-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="50290-118">Verschieben Sie dann den Einzelvorgang in die vorherige Periode.</span><span class="sxs-lookup"><span data-stu-id="50290-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="50290-119">Klicken sie auf **Vorherige Periode**.</span><span class="sxs-lookup"><span data-stu-id="50290-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="50290-120">Klicken Sie auf **Ende**, um den Einzelvorgang an das Ende der Einzelvorgangsliste als den letzten Einzelvorgang in der vorherigen Periode zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="50290-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="50290-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="50290-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="50290-122">Wählen Sie einen Einzelvorgang aus, der den Status **Geplanter Einzelvorgang** hat, beispielsweise einen Einzelvorgang, der für den 18. Dezember 2012 geplant war, im Feld **Geplante Periode** aus.</span><span class="sxs-lookup"><span data-stu-id="50290-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="50290-123">Verschieben Sie dann den Einzelvorgang in die nächste Periode.</span><span class="sxs-lookup"><span data-stu-id="50290-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="50290-124">Klicken Sie auf **Nächste Periode**.</span><span class="sxs-lookup"><span data-stu-id="50290-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="50290-125">Klicken Sie auf **Start**, um den Einzelvorgang an den Anfang der Einzelvorgangsliste als den ersten Einzelvorgang in der vorherigen Periode zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="50290-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="50290-126">Verschieben Sie einen Einzelvorgang innerhalb einer Periode.</span><span class="sxs-lookup"><span data-stu-id="50290-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="50290-127">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="50290-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="50290-128">Wählen Sie einen Einzelvorgang aus, der den Status „Geplanter Einzelvorgang” hat, beispielsweise den zweiten Einzelvorgang, der für den 19. Dezember 2012 geplant war, im Feld **Geplante Periode** aus.</span><span class="sxs-lookup"><span data-stu-id="50290-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="50290-129">Verschieben Sie dann den Einzelvorgang in die geplante Periode.</span><span class="sxs-lookup"><span data-stu-id="50290-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="50290-130">Klicken Sie auf **Vorwärts**.</span><span class="sxs-lookup"><span data-stu-id="50290-130">Click **Forward**.</span></span> <span data-ttu-id="50290-131">Beachten Sie, dass der Einzelvorgang um eine Position in der Liste nach unten verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="50290-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="50290-132">Klicken Sie auf **Rückwärts**.</span><span class="sxs-lookup"><span data-stu-id="50290-132">Click **Backward**.</span></span> <span data-ttu-id="50290-133">Beachten Sie, dass der Einzelvorgang um eine Position in der Liste nach oben verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="50290-133">Notice that the job is moved one line up on the list.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]