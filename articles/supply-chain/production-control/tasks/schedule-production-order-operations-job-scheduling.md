---
title: Einen Produktionsauftrag mit Vorgängen und Feinterminierung planen
description: Dieses Verfahren konzentriert sich auf die Planung eines Fertigungsauftrags mit Grobterminierung und Feinterminierung.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562137"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="bce0a-103">Einen Produktionsauftrag mit Vorgängen und Feinterminierung planen</span><span class="sxs-lookup"><span data-stu-id="bce0a-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bce0a-104">Dieses Verfahren konzentriert sich auf die Planung eines Fertigungsauftrags mit Grobterminierung und Feinterminierung.</span><span class="sxs-lookup"><span data-stu-id="bce0a-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="bce0a-105">Es werden keine Einzelvorgänge mit Grobterminierung erstellt. Es werden jedoch Einzelvorgänge mit Feinterminierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="bce0a-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="bce0a-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="bce0a-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bce0a-107">Dieses Verfahren ist für Produktionsleiter, Produktionsplaner oder Werkstattleiter gedacht, die in einer Einzelfertigungsumgebung arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bce0a-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="bce0a-108">Produktionsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="bce0a-108">Create a production order</span></span>
1. <span data-ttu-id="bce0a-109">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="bce0a-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="bce0a-110">Klicken Sie auf "Neuer Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="bce0a-110">Click New production order.</span></span>
3. <span data-ttu-id="bce0a-111">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="bce0a-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bce0a-112">Wählen Sie Artikelnummer D0001 aus.</span><span class="sxs-lookup"><span data-stu-id="bce0a-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="bce0a-113">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="bce0a-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="bce0a-114">Planen von Vorgängen für den Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="bce0a-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="bce0a-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="bce0a-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bce0a-116">Wählen Sie den soeben erstellten Produktionsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="bce0a-116">Select the production order that you have just created.</span></span> <span data-ttu-id="bce0a-117">Er sollte am Anfang der Liste stehen.</span><span class="sxs-lookup"><span data-stu-id="bce0a-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="bce0a-118">Klicken Sie im Aktivitätsbereich auf "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="bce0a-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="bce0a-119">Klicken Sie auf "Arbeitsgänge planen".</span><span class="sxs-lookup"><span data-stu-id="bce0a-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="bce0a-120">Wählen Sie im Feld Planungsrichtung "Vorwärts ab Planungsdatum" aus.</span><span class="sxs-lookup"><span data-stu-id="bce0a-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="bce0a-121">Geben Sie ein Datum in das Feld "Planungsdatum" ein.</span><span class="sxs-lookup"><span data-stu-id="bce0a-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="bce0a-122">Wählen Sie ein zukünftiges Datum (beispielsweise heute plus eine Woche).</span><span class="sxs-lookup"><span data-stu-id="bce0a-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="bce0a-123">Mit der ausgewählten Planungsrichtung wird der Produktionsauftrag vorwärts ab diesem Datum geplant.</span><span class="sxs-lookup"><span data-stu-id="bce0a-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="bce0a-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bce0a-124">Click OK.</span></span>
7. <span data-ttu-id="bce0a-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="bce0a-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bce0a-126">Beachten Sie, dass sich der Status in "Geplant" ändert.</span><span class="sxs-lookup"><span data-stu-id="bce0a-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="bce0a-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="bce0a-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bce0a-128">Klicken Sie auf "Alle Einzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="bce0a-128">Click All jobs.</span></span>
    * <span data-ttu-id="bce0a-129">Beachten Sie, dass keine Aufträge mit geplanten Vorgängen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bce0a-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="bce0a-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bce0a-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="bce0a-131">Planen von Einzelvorgängen für den Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="bce0a-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="bce0a-132">Klicken Sie im Aktivitätsbereich auf "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="bce0a-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="bce0a-133">Klicken Sie auf Einzelvorgänge planen.</span><span class="sxs-lookup"><span data-stu-id="bce0a-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="bce0a-134">Wählen Sie im Feld Planungsrichtung "Vorwärts ab Planungsdatum" aus.</span><span class="sxs-lookup"><span data-stu-id="bce0a-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="bce0a-135">Geben Sie ein Datum in das Feld "Planungsdatum" ein.</span><span class="sxs-lookup"><span data-stu-id="bce0a-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="bce0a-136">Wählen Sie ein zukünftiges Datum (beispielsweise heute plus eine Woche).</span><span class="sxs-lookup"><span data-stu-id="bce0a-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="bce0a-137">Mit der ausgewählten Planungsrichtung wird der Produktionsauftrag vorwärts ab diesem Datum geplant.</span><span class="sxs-lookup"><span data-stu-id="bce0a-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="bce0a-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bce0a-138">Click OK.</span></span>
6. <span data-ttu-id="bce0a-139">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="bce0a-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="bce0a-140">Klicken Sie auf "Alle Einzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="bce0a-140">Click All jobs.</span></span>
    * <span data-ttu-id="bce0a-141">Beachten Sie, dass (basieren auf der aktiven Route) 5 neue Einzelaufträge mit Feinterminierung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bce0a-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

