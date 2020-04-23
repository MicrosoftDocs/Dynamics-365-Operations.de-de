---
title: Kanban-Einzelvorgänge planen
description: Der Schwerpunkt dieser Prozedur liegt auf der Planung von Kanban-Bearbeitungseinzelvorgängen für eine spezielle Arbeitsgruppe.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8342bf6c56adc41cc4944dc709152246ad93a3e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210455"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="82f5a-103">Kanban-Einzelvorgänge planen</span><span class="sxs-lookup"><span data-stu-id="82f5a-103">Schedule kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82f5a-104">Der Schwerpunkt dieser Prozedur liegt auf der Planung von Kanban-Bearbeitungseinzelvorgängen für eine spezielle Arbeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="82f5a-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="82f5a-105">Das Verfahren "Bereiten Sie einen Kanban-Bearbeitungseinzelvorgang vor, wenn Materialien für die Arbeitsgruppe verfügbar sind" ist für dieses Verfahren vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="82f5a-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="82f5a-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="82f5a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="82f5a-107">Diese Aufgabe ist für die Fertigungsbereichsvorgesetzten und Produktionsplaner vorgesehen, die mit Kanbans arbeiten.</span><span class="sxs-lookup"><span data-stu-id="82f5a-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="82f5a-108">Kanban-Einzelvorgänge für eine Arbeitsgruppe auswählen</span><span class="sxs-lookup"><span data-stu-id="82f5a-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="82f5a-109">Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Einzelvorgangsplanung".</span><span class="sxs-lookup"><span data-stu-id="82f5a-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="82f5a-110">Periodenkapazität-Infobox erweitern</span><span class="sxs-lookup"><span data-stu-id="82f5a-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="82f5a-111">Kanban-Infobox erweitern.</span><span class="sxs-lookup"><span data-stu-id="82f5a-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="82f5a-112">Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="82f5a-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="82f5a-113">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="82f5a-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="82f5a-114">Wählen Sie die Arbeitsgruppe 1250 aus.</span><span class="sxs-lookup"><span data-stu-id="82f5a-114">Select work cell 1250.</span></span> <span data-ttu-id="82f5a-115">Dies filtert die Ansicht, sodass nur die Einzelvorgänge für Arbeitsgruppe 1250 angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="82f5a-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="82f5a-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="82f5a-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="82f5a-117">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="82f5a-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="82f5a-118">Kanban-Einzelvorgang in der ersten verfügbaren Periode planen</span><span class="sxs-lookup"><span data-stu-id="82f5a-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="82f5a-119">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="82f5a-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="82f5a-120">Wählen Sie die erste Zeile in der Liste aus, die den Status "Nicht geplant" aufweist.</span><span class="sxs-lookup"><span data-stu-id="82f5a-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="82f5a-121">Das gepunktete Symbol im Feld "Einzelvorgangsstatus" gibt "Nicht geplant" an.</span><span class="sxs-lookup"><span data-stu-id="82f5a-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="82f5a-122">Klicken Sie auf "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="82f5a-122">Click Schedule.</span></span>
    * <span data-ttu-id="82f5a-123">Dies plant den Kanban-Einzelvorgang in der ersten verfügbaren Periode.</span><span class="sxs-lookup"><span data-stu-id="82f5a-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="82f5a-124">Beachten Sie, dass der Kanban-Einzelvorgang an das Ende der Liste verschoben wird, da er in der Periode hinzugefügt wurde, die ab dem heutigen Tag beginnt.</span><span class="sxs-lookup"><span data-stu-id="82f5a-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="82f5a-125">Wenn die ab dem heutigen Tag beginnende Periode vollständig gebucht ist, wird der Einzelvorgang in die erste verfügbare Periode verschoben.</span><span class="sxs-lookup"><span data-stu-id="82f5a-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="82f5a-126">Zwei Kanban-Einzelvorgänge für einen bestimmten Tag planen</span><span class="sxs-lookup"><span data-stu-id="82f5a-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="82f5a-127">Wählen Sie in der Liste die Zeile "1" aus.</span><span class="sxs-lookup"><span data-stu-id="82f5a-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="82f5a-128">Sie sollten sehen, dass die erste Zeile den Status "Nicht geplant" im Feld "Einzelvorgangsstatus" hat.</span><span class="sxs-lookup"><span data-stu-id="82f5a-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="82f5a-129">Wählen Sie in der Liste die Zeile "2" aus.</span><span class="sxs-lookup"><span data-stu-id="82f5a-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="82f5a-130">Sie sollten sehen, dass die zweite Zeile den Status "Nicht geplant" im Feld "Einzelvorgangsstatus" hat.</span><span class="sxs-lookup"><span data-stu-id="82f5a-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="82f5a-131">Jetzt haben Sie die ersten zwei Stellen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="82f5a-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="82f5a-132">Klicken Sie auf "Anfangsdatum für Zeitplan", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="82f5a-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="82f5a-133">Aktivieren oder deaktivieren Sie "Reaktion auf Kapazitätsmangel überschreiben".</span><span class="sxs-lookup"><span data-stu-id="82f5a-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="82f5a-134">Diese Option ermöglicht es Ihnen, die standardmäßige Reaktion auf Kapazitätsmangel zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="82f5a-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="82f5a-135">Wählen Sie im Feld "Reaktion auf Kapazitätsmangel" "Zur angeforderten Periode hinzufügen" aus.</span><span class="sxs-lookup"><span data-stu-id="82f5a-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="82f5a-136">Durch diese Option wird sichergestellt, dass der Einzelvorgang zur angeforderten Periode hinzugefügt wird, unabhängig von, ob die Arbeitsgruppe möglicherweise überlastet wird.</span><span class="sxs-lookup"><span data-stu-id="82f5a-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="82f5a-137">Klicken Sie auf "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="82f5a-137">Click Schedule.</span></span>
    * <span data-ttu-id="82f5a-138">Beachten Sie, dass beide Einzelvorgänge zur gewünschten Periode hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="82f5a-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="82f5a-139">Im Abschnitt "Periodenkapazität" können Sie die Auslastung für jede Periode sehen.</span><span class="sxs-lookup"><span data-stu-id="82f5a-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="82f5a-140">Das Feld "Verbrauch" zeigt den geplanten Verbrauch in dieser Periode an.</span><span class="sxs-lookup"><span data-stu-id="82f5a-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="82f5a-141">Wenn der geplante Verbrauch höher als die verfügbare Kapazität in dieser Periode ist, wird der überladene Verbrauch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="82f5a-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

