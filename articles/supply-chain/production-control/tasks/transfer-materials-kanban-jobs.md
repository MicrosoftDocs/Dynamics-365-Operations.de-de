--- 
title: "Materialien mit Kanban-Einzelvorgängen übertragen (nur Februar 2016)"
description: "Der Schwerpunkt dieser Prozedur liegt auf dem Ausführen eines Entnahme-Kanban-Einzelvorgangs, um Material zu übertragen."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c79480d844627a7eed8129515924f1f70ad04f95
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a><span data-ttu-id="2eed1-103">Materialien mit Kanban-Einzelvorgängen übertragen (nur Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="2eed1-103">Transfer materials with kanban jobs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2eed1-104">Der Schwerpunkt dieser Prozedur liegt auf dem Ausführen eines Entnahme-Kanban-Einzelvorgangs, um Material zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="2eed1-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="2eed1-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="2eed1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2eed1-106">Diese Prozedur ist für Lagerarbeitskräfte vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="2eed1-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="2eed1-107">Umlagerungseinzelvorgänge anzeigen</span><span class="sxs-lookup"><span data-stu-id="2eed1-107">Display transfer jobs</span></span>
1. <span data-ttu-id="2eed1-108">Wechseln Sie zu "Produktionssteuerung" > "Kanban" >"Kanban-Übersicht für Umlagerungseinzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="2eed1-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="2eed1-109">Erweitern oder reduzieren Sie den Abschnitt ''Filter".</span><span class="sxs-lookup"><span data-stu-id="2eed1-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="2eed1-110">Im Abschnitt "Filter" können Sie angeben, welche Einzelvorgänge Sie anzeigen möchten, indem Sie nach Produktionsfluss, Name der Aktivität, Von-Lagerort und Ort sowie An-Lagerort und Ort filtern.</span><span class="sxs-lookup"><span data-stu-id="2eed1-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="2eed1-111">Geben Sie im Feld "Von Lagerort" "11" ein.</span><span class="sxs-lookup"><span data-stu-id="2eed1-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="2eed1-112">Geben Sie im Feld "An Lagerplatz" "12" ein.</span><span class="sxs-lookup"><span data-stu-id="2eed1-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="2eed1-113">Umlagerungseinzelvorgang starten</span><span class="sxs-lookup"><span data-stu-id="2eed1-113">Start a transfer job</span></span>
1. <span data-ttu-id="2eed1-114">Deaktivieren Sie ggf. die ausgewählte Zeile in der Liste.</span><span class="sxs-lookup"><span data-stu-id="2eed1-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="2eed1-115">Wählen Sie in der Liste die Zeile "4" aus.</span><span class="sxs-lookup"><span data-stu-id="2eed1-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="2eed1-116">Wählen Sie den ersten Einzelvorgang mit dem Status "Nicht geplant" aus.</span><span class="sxs-lookup"><span data-stu-id="2eed1-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="2eed1-117">Stellen Sie sicher, dass dies der einzige ausgewählte Einzelvorgang ist.</span><span class="sxs-lookup"><span data-stu-id="2eed1-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="2eed1-118">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="2eed1-118">Click Start.</span></span>
    * <span data-ttu-id="2eed1-119">Beachten Sie, dass ein Symbol anzeigt, dass der Einzelvorgang gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="2eed1-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="2eed1-120">Wählen Sie einen zweiten Umlagerungseinzelvorgang aus und ändern Sie die Menge</span><span class="sxs-lookup"><span data-stu-id="2eed1-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="2eed1-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2eed1-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2eed1-122">Sie können mehrere Einzelvorgänge ausgewählt haben, wählen Sie hier jedoch Zeile 5 aus.</span><span class="sxs-lookup"><span data-stu-id="2eed1-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="2eed1-123">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2eed1-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2eed1-124">Stellen Sie sicher, dass der Einzelvorgang im vorherigen Schritt der einzige ausgewählte Einzelvorgang ist.</span><span class="sxs-lookup"><span data-stu-id="2eed1-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="2eed1-125">Heben Sie die Auswahl anderer Einzelvorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="2eed1-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="2eed1-126">Notieren Sie sich den Wert im Feld "Einzelvorgangsmenge" für Ihre Unterlagen</span><span class="sxs-lookup"><span data-stu-id="2eed1-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="2eed1-127">Legen Sie "Einzelvorgangsmenge" auf "30" fest.</span><span class="sxs-lookup"><span data-stu-id="2eed1-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="2eed1-128">Beachten Sie die Warnung!</span><span class="sxs-lookup"><span data-stu-id="2eed1-128">Notice the warning!</span></span> <span data-ttu-id="2eed1-129">Sie sind nicht zulässig, 30 zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="2eed1-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="2eed1-130">Entsprechend den Einstellungen der Kanban-Regel, können Sie nur die ursprüngliche Menge übertragen.</span><span class="sxs-lookup"><span data-stu-id="2eed1-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="2eed1-131">Den zuvor im Feld "Einzelvorgangsmenge" notierten Wert verwenden</span><span class="sxs-lookup"><span data-stu-id="2eed1-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="2eed1-132">Legen Sie die Einzelvorgangsmenge auf den vorherigen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="2eed1-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="2eed1-133">Starten Sie den zweiten Umlagerungseinzelvorgang</span><span class="sxs-lookup"><span data-stu-id="2eed1-133">Start the second transfer job</span></span>
1. <span data-ttu-id="2eed1-134">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="2eed1-134">Click Start.</span></span>
    * <span data-ttu-id="2eed1-135">Dadurch beginnt die Übertragung des Einzelvorgangs in Zeile 5.</span><span class="sxs-lookup"><span data-stu-id="2eed1-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="2eed1-136">Schließen Sie beide Umlagerungseinzelvorgänge ab</span><span class="sxs-lookup"><span data-stu-id="2eed1-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="2eed1-137">Wählen Sie in der Liste die Zeile "4" aus.</span><span class="sxs-lookup"><span data-stu-id="2eed1-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="2eed1-138">Es sind jetzt zwei Umlagerungseinzelvorgänge in Zeile 4 und Zeile 5 ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="2eed1-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="2eed1-139">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="2eed1-139">Click Complete.</span></span>
    * <span data-ttu-id="2eed1-140">Dadurch wird die Übertragung beider Einzelvorgänge abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2eed1-140">This will complete the transfer of both jobs.</span></span>  


