---
title: Einen Kanban-Einzelvorgang aus der Planung entfernen
description: Der Schwerpunkt dieser Prozedur liegt auf dem Entfernen eines geplanten Kanban-Bearbeitungseinzelvorgang aus der Planung durch das Zurücksetzen des Einzelvorgangsstatus zu "Nicht geplant".
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b2137268301beb85906bf7fb26c41f6eb09534c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148917"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="69298-103">Einen Kanban-Einzelvorgang aus der Planung entfernen</span><span class="sxs-lookup"><span data-stu-id="69298-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69298-104">Der Schwerpunkt dieser Prozedur liegt auf dem Entfernen eines geplanten Kanban-Bearbeitungseinzelvorgang aus der Planung durch das Zurücksetzen des Einzelvorgangsstatus zu "Nicht geplant".</span><span class="sxs-lookup"><span data-stu-id="69298-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="69298-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="69298-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="69298-106">Dieses Verfahren ist für Fertigungsbereichsvorgesetzte und Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="69298-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="69298-107">Geplanten Kanban-Einzelvorgang suchen</span><span class="sxs-lookup"><span data-stu-id="69298-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="69298-108">Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Einzelvorgangsplanung".</span><span class="sxs-lookup"><span data-stu-id="69298-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="69298-109">Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69298-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="69298-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="69298-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="69298-111">Wählen Sie die Arbeitsgruppe 1250 aus.</span><span class="sxs-lookup"><span data-stu-id="69298-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="69298-112">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="69298-112">Click Select.</span></span>
5. <span data-ttu-id="69298-113">Wählen Sie im Feld "Einzelvorgangsstatus anzeigen" "Geplant" aus.</span><span class="sxs-lookup"><span data-stu-id="69298-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="69298-114">Entfernen des geplanten Kanban-Einzelvorgangs aus der Planung</span><span class="sxs-lookup"><span data-stu-id="69298-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="69298-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="69298-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="69298-116">Wählen Sie einen Einzelvorgang aus, der den Statuts "Geplant" hat, beispielsweise einen Einzelvorgang vom 19. Dezember 2012.</span><span class="sxs-lookup"><span data-stu-id="69298-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="69298-117">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="69298-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="69298-118">Klicken Sie auf "Einzelvorgangsstatus zurücksetzen".</span><span class="sxs-lookup"><span data-stu-id="69298-118">Click Revert job status.</span></span>
4. <span data-ttu-id="69298-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="69298-119">Click OK.</span></span>
    * <span data-ttu-id="69298-120">Dadurch wird der aktuelle Status von "Geplant" zu "Nicht geplant" geändert und aus der Prozessübersicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="69298-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

