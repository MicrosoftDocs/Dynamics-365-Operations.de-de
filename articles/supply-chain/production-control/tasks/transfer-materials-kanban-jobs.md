---
title: Übergangsmaterialien mit Kanban-Einzelvorgängen
description: Der Schwerpunkt dieser Prozedur liegt auf dem Ausführen eines Entnahme-Kanban-Einzelvorgangs, um Material zu übertragen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96cb77b7b37fe6519a812735d9a41749da078cf2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210363"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="f0562-103">Übergangsmaterialien mit Kanban-Einzelvorgängen</span><span class="sxs-lookup"><span data-stu-id="f0562-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0562-104">Der Schwerpunkt dieser Prozedur liegt auf dem Ausführen eines Entnahme-Kanban-Einzelvorgangs, um Material zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="f0562-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="f0562-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="f0562-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f0562-106">Diese Prozedur ist für Lagerarbeitskräfte vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f0562-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="f0562-107">Umlagerungseinzelvorgänge anzeigen</span><span class="sxs-lookup"><span data-stu-id="f0562-107">Display transfer jobs</span></span>
1. <span data-ttu-id="f0562-108">Wechseln Sie zu "Produktionssteuerung" > "Kanban" >"Kanban-Übersicht für Umlagerungseinzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="f0562-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="f0562-109">Erweitern oder reduzieren Sie den Abschnitt ''Filter".</span><span class="sxs-lookup"><span data-stu-id="f0562-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="f0562-110">Im Abschnitt "Filter" können Sie angeben, welche Einzelvorgänge Sie anzeigen möchten, indem Sie nach Produktionsfluss, Name der Aktivität, Von-Lagerort und Ort sowie An-Lagerort und Ort filtern.</span><span class="sxs-lookup"><span data-stu-id="f0562-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="f0562-111">Geben Sie im Feld "Von Lagerort" "11" ein.</span><span class="sxs-lookup"><span data-stu-id="f0562-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="f0562-112">Geben Sie im Feld "An Lagerplatz" "12" ein.</span><span class="sxs-lookup"><span data-stu-id="f0562-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="f0562-113">Umlagerungseinzelvorgang starten</span><span class="sxs-lookup"><span data-stu-id="f0562-113">Start a transfer job</span></span>
1. <span data-ttu-id="f0562-114">Deaktivieren Sie ggf. die ausgewählte Zeile in der Liste.</span><span class="sxs-lookup"><span data-stu-id="f0562-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="f0562-115">Wählen Sie in der Liste die Zeile "4" aus.</span><span class="sxs-lookup"><span data-stu-id="f0562-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="f0562-116">Wählen Sie den ersten Einzelvorgang mit dem Status "Nicht geplant" aus.</span><span class="sxs-lookup"><span data-stu-id="f0562-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="f0562-117">Stellen Sie sicher, dass dies der einzige ausgewählte Einzelvorgang ist.</span><span class="sxs-lookup"><span data-stu-id="f0562-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="f0562-118">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="f0562-118">Click Start.</span></span>
    * <span data-ttu-id="f0562-119">Beachten Sie, dass ein Symbol anzeigt, dass der Einzelvorgang gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="f0562-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="f0562-120">Wählen Sie einen zweiten Umlagerungseinzelvorgang aus und ändern Sie die Menge</span><span class="sxs-lookup"><span data-stu-id="f0562-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="f0562-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f0562-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f0562-122">Sie können mehrere Einzelvorgänge ausgewählt haben, wählen Sie hier jedoch Zeile 5 aus.</span><span class="sxs-lookup"><span data-stu-id="f0562-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="f0562-123">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f0562-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f0562-124">Stellen Sie sicher, dass der Einzelvorgang im vorherigen Schritt der einzige ausgewählte Einzelvorgang ist.</span><span class="sxs-lookup"><span data-stu-id="f0562-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="f0562-125">Heben Sie die Auswahl anderer Einzelvorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="f0562-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="f0562-126">Notieren Sie sich den Wert im Feld "Einzelvorgangsmenge" für Ihre Unterlagen</span><span class="sxs-lookup"><span data-stu-id="f0562-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="f0562-127">Legen Sie "Einzelvorgangsmenge" auf "30" fest.</span><span class="sxs-lookup"><span data-stu-id="f0562-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="f0562-128">Beachten Sie die Warnung!</span><span class="sxs-lookup"><span data-stu-id="f0562-128">Notice the warning!</span></span> <span data-ttu-id="f0562-129">Sie sind nicht zulässig, 30 zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="f0562-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="f0562-130">Entsprechend den Einstellungen der Kanban-Regel, können Sie nur die ursprüngliche Menge übertragen.</span><span class="sxs-lookup"><span data-stu-id="f0562-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="f0562-131">Den zuvor im Feld "Einzelvorgangsmenge" notierten Wert verwenden</span><span class="sxs-lookup"><span data-stu-id="f0562-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="f0562-132">Legen Sie die Einzelvorgangsmenge auf den vorherigen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="f0562-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="f0562-133">Starten Sie den zweiten Umlagerungseinzelvorgang</span><span class="sxs-lookup"><span data-stu-id="f0562-133">Start the second transfer job</span></span>
1. <span data-ttu-id="f0562-134">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="f0562-134">Click Start.</span></span>
    * <span data-ttu-id="f0562-135">Dadurch beginnt die Übertragung des Einzelvorgangs in Zeile 5.</span><span class="sxs-lookup"><span data-stu-id="f0562-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="f0562-136">Schließen Sie beide Umlagerungseinzelvorgänge ab</span><span class="sxs-lookup"><span data-stu-id="f0562-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="f0562-137">Wählen Sie in der Liste die Zeile "4" aus.</span><span class="sxs-lookup"><span data-stu-id="f0562-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="f0562-138">Es sind jetzt zwei Umlagerungseinzelvorgänge in Zeile 4 und Zeile 5 ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f0562-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="f0562-139">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="f0562-139">Click Complete.</span></span>
    * <span data-ttu-id="f0562-140">Dadurch wird die Übertragung beider Einzelvorgänge abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f0562-140">This will complete the transfer of both jobs.</span></span>  

