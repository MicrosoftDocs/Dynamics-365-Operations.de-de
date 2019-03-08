---
title: Kanban-Bearbeitungseinzelvorgänge durchführen
description: Diese Prozedur konzentriert sich auf das Ausführen von Kanban-Bearbeitungs-Einzelvorgängen.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62be1f116dfecbc4c6ba11053b94efc874baa3e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "357426"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="4e29d-103">Kanban-Bearbeitungseinzelvorgänge durchführen</span><span class="sxs-lookup"><span data-stu-id="4e29d-103">Execute kanban process jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e29d-104">Diese Prozedur konzentriert sich auf das Ausführen von Kanban-Bearbeitungs-Einzelvorgängen.</span><span class="sxs-lookup"><span data-stu-id="4e29d-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="4e29d-105">Der erste Einzelvorgang wird mit der erwarteten Menge abgeschlossen und enthält keine Fehler.</span><span class="sxs-lookup"><span data-stu-id="4e29d-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="4e29d-106">Der zweite Einzelvorgang wird mit Fehlern abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4e29d-106">The second job is completed with errors.</span></span> <span data-ttu-id="4e29d-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="4e29d-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4e29d-108">Diese Prozedur ist für den Maschinenbediener vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4e29d-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="4e29d-109">Wählen Sie einen Kanban-Einzelvorgang aus</span><span class="sxs-lookup"><span data-stu-id="4e29d-109">Select a kanban job</span></span>
1. <span data-ttu-id="4e29d-110">Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Übersicht für Prozesseinzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="4e29d-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="4e29d-111">Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4e29d-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4e29d-112">Klicken Sie auf die Zeile mit Ressourcengruppe 1250.</span><span class="sxs-lookup"><span data-stu-id="4e29d-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="4e29d-113">Dies filtert die Liste "Einzelvorgänge", sodass nur die Einzelvorgänge für Arbeitsgruppe 1250 angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4e29d-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="4e29d-114">Markieren Sie die Zeile, die den Status "Geplanter Einzelvorgang" aufweist.</span><span class="sxs-lookup"><span data-stu-id="4e29d-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="4e29d-115">Schließen Sie einen Einzelvorgang mit erwarteter Menge ab</span><span class="sxs-lookup"><span data-stu-id="4e29d-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="4e29d-116">Erweitern oder reduzieren Sie den Abschnitt "Details".</span><span class="sxs-lookup"><span data-stu-id="4e29d-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="4e29d-117">Dieser Abschnitt zeigt wichtige Informationen zu Kartennummer, Artikelnummer, bestellter Menge und Aktivitätsname an.</span><span class="sxs-lookup"><span data-stu-id="4e29d-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="4e29d-118">Erweitern oder reduzieren Sie den Abschnitt "Produktionsanweisungen".</span><span class="sxs-lookup"><span data-stu-id="4e29d-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="4e29d-119">In diesem Abschnitt werden Produktionsanweisungen für die Aktivität angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4e29d-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="4e29d-120">Die Anweisungen können Text, Bilder, Zeichnungen und andere Dokumente sein.</span><span class="sxs-lookup"><span data-stu-id="4e29d-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="4e29d-121">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="4e29d-121">Click Start.</span></span>
    * <span data-ttu-id="4e29d-122">Wählen Sie einen Einzelvorgang aus, die nicht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4e29d-122">Select a job that is not completed.</span></span> <span data-ttu-id="4e29d-123">Verwenden Sie Statussymbole im Feld "Einzelvorgangsstatus", um Einzelvorgangsstatus anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4e29d-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="4e29d-124">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="4e29d-124">Click Complete.</span></span>
    * <span data-ttu-id="4e29d-125">Der Einzelvorgang wird mit der erwarteten Qualität abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4e29d-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="4e29d-126">Schließen Sie einen Einzelvorgang mit Fehlern ab</span><span class="sxs-lookup"><span data-stu-id="4e29d-126">Complete a job with errors</span></span>
1. <span data-ttu-id="4e29d-127">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="4e29d-127">Click Start.</span></span>
    * <span data-ttu-id="4e29d-128">Wenn ein Einzelvorgang abgeschlossen ist, wird der nächste Einzelvorgang in der Liste automatisch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4e29d-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="4e29d-129">Daher müssen Sie keinen Einzelvorgang auswählen, bevor Sie auf "Start" klicken.</span><span class="sxs-lookup"><span data-stu-id="4e29d-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="4e29d-130">Klicken Sie im Aktivitätsbereich auf "Fertigung".</span><span class="sxs-lookup"><span data-stu-id="4e29d-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="4e29d-131">Klicken Sie auf "Abschließen (Details)".</span><span class="sxs-lookup"><span data-stu-id="4e29d-131">Click Complete (details).</span></span>
4. <span data-ttu-id="4e29d-132">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4e29d-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="4e29d-133">Geben Sie im Feld "Fehlermenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4e29d-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="4e29d-134">Geben Sie im Feld "Gutmenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4e29d-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="4e29d-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4e29d-135">Click OK.</span></span>

