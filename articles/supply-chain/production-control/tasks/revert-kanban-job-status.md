---
title: Kanban-Einzelvorgangsstatus zurücksetzen
description: Ziel dieser Prozedur ist das Zurücksetzen eines falschen Kanban-Einzelvorgangsstatus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27874f89cede151b52b869fa0d58e320d548e6d3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562206"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="ca033-103">Kanban-Einzelvorgangsstatus zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="ca033-103">Revert kanban job status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca033-104">Ziel dieser Prozedur ist das Zurücksetzen eines falschen Kanban-Einzelvorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="ca033-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="ca033-105">Dies ist hilfreich, falls der Maschinenbediener den falschen Einzelvorgang aktualisiert, oder versehentlich den falschen Status festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="ca033-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="ca033-106">In diesem Verfahren wird ein Kanban-Einzelvorgang versehentlich als vorbereitet erfasst und der Status wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ca033-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="ca033-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="ca033-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ca033-108">Diese Prozedur ist für Filialleiter oder Maschinenbediener vorgesehen, die in einem Lean Manufacturing-Unternehmen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ca033-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="ca033-109">Öffnen Sie die Prozessübersicht für Arbeitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="ca033-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="ca033-110">Gehen Sie zu "Kanban Tafel für Prozesseinzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="ca033-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="ca033-111">Geben Sie im Feld 'Arbeitsgruppe' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ca033-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="ca033-112">Wählen Sie die Arbeitsgruppe 1260 aus.</span><span class="sxs-lookup"><span data-stu-id="ca033-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="ca033-113">Kanban-Einzelvorgang vorbereiten</span><span class="sxs-lookup"><span data-stu-id="ca033-113">Prepare kanban job</span></span>
1. <span data-ttu-id="ca033-114">Klicken Sie auf "Vorbereiten".</span><span class="sxs-lookup"><span data-stu-id="ca033-114">Click Prepare.</span></span>
    * <span data-ttu-id="ca033-115">Wenn Sie nicht auf "Vorbereiten" klicken können, da es ausgeblendet ist, sollten Sie überprüfen, dass der ausgewählte Kanban-Einzelvorgang den Status "Geplant" hat, der durch das leere Kanbansymbol angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca033-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="ca033-116">Wenn "Vorbereiten" fehlschlägt, überprüfen Sie, ob alle Materialien in der Kommissionierliste verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ca033-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="ca033-117">Wählen Sie in der Liste den gewünschten Einzelvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="ca033-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="ca033-118">Wählen Sie den ersten Einzelvorgang aus, den Sie soeben vorbereitet haben.</span><span class="sxs-lookup"><span data-stu-id="ca033-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="ca033-119">Beachten Sie, dass der Einzelvorgangsstatus vorbereitet ist, der mit einem Dreieck innerhalb des Kanbansymbols angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ca033-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="ca033-120">Hiermit wird der Status des vorbereiteten Kanban-Einzelvorgangs wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ca033-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="ca033-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ca033-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ca033-122">Wählen Sie den ersten Einzelvorgang aus, den Sie bereits vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ca033-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="ca033-123">Klicken Sie im Aktivitätsbereich auf "Fertigung".</span><span class="sxs-lookup"><span data-stu-id="ca033-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="ca033-124">Klicken Sie auf "Status wiederherstellen".</span><span class="sxs-lookup"><span data-stu-id="ca033-124">Click Revert status.</span></span>
    * <span data-ttu-id="ca033-125">Sie können eine alternative Kanban-Regel verwenden, wenn die folgenden Bedingungen erfüllt sind: - Die Wiederbeschaffungsstrategie ist die gleiche für beide Regeln.</span><span class="sxs-lookup"><span data-stu-id="ca033-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="ca033-126">- Die Version des Produktionsflusses ist die gleiche für beide Regeln.</span><span class="sxs-lookup"><span data-stu-id="ca033-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="ca033-127">- Das Produkt, das beschafft wird, ist das gleiche für beide Regeln.</span><span class="sxs-lookup"><span data-stu-id="ca033-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="ca033-128">- Alle Downstream-Aktivitäten, die für die letzte Aktivität der Kanban-Regeln konfiguriert werden, müssen die gleichen für beide Regeln sein.</span><span class="sxs-lookup"><span data-stu-id="ca033-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="ca033-129">- Die gleichen angegebene Lagerungsdimensionen müssen für beide Regeln konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ca033-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="ca033-130">- Der Status der Handhabungseinheit muss "Nicht zugewiesen" sein.</span><span class="sxs-lookup"><span data-stu-id="ca033-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="ca033-131">- Die Konfiguration für Ereignis-Kanbans muss die gleiche sein.</span><span class="sxs-lookup"><span data-stu-id="ca033-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="ca033-132">Stellen Sie sicher, dass der neue Status "Geplant" lautet.</span><span class="sxs-lookup"><span data-stu-id="ca033-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="ca033-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ca033-133">Click OK.</span></span>
5. <span data-ttu-id="ca033-134">Heben Sie in der Liste die Markierung der ausgewählten Zeile auf.</span><span class="sxs-lookup"><span data-stu-id="ca033-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="ca033-135">Wählen Sie den gleichen Einzelvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="ca033-135">Select the same job.</span></span>  
    * <span data-ttu-id="ca033-136">Beachten Sie, dass der Einzelvorgangsstatus für den Kanban-Einzelvorgang auf "Geplant" zurückgesetzt wurde und von einem leeren Kanbansymbol angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca033-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  

