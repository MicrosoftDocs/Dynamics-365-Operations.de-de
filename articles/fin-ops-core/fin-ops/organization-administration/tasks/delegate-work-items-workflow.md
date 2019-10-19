---
title: Delegieren von Arbeitsaufgaben in einem Workflow
description: Wenn Sie für einige Zeit abwesend oder anderweitig für Arbeitsaufgaben nicht verfügbar sind, können Sie Ihre Arbeitsaufgaben an andere Benutzer delegieren oder diesen neu zuweisen.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189958"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="b5188-103">Delegieren von Arbeitsaufgaben in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="b5188-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="b5188-104">Manuelles Delegieren einer Arbeitsaufgabe</span><span class="sxs-lookup"><span data-stu-id="b5188-104">Manually delegate a work item</span></span>

<span data-ttu-id="b5188-105">Um eine einzelne Arbeitsaufgabe zu delegieren, wählen Sie die Option **Delegieren** im Menü **Workflow** aus, und geben Sie dann den Benutzer an, an den delegiert werden soll, zusammen mit einem Kommentar.</span><span class="sxs-lookup"><span data-stu-id="b5188-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="b5188-106">Dadurch wird die Arbeitsaufgabe an diesen Benutzer neu zugewiesen, sodass sie ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5188-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="b5188-107">Arbeitsaufgaben automatisch delegieren</span><span class="sxs-lookup"><span data-stu-id="b5188-107">Automatically delegate work items</span></span>

<span data-ttu-id="b5188-108">Wenn Sie planen, für einen Zeitraum nicht im Büro anwesend oder anderweitig nicht verfügbar zu sein, um sich um Arbeitsaufgaben zu kümmern, können Sie neue Arbeitsaufgaben automatisch an andere Benutzer mithilfe der Seite **Benutzeroptionen** delegieren.</span><span class="sxs-lookup"><span data-stu-id="b5188-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="b5188-109">Einrichten der automatischen Delegierung</span><span class="sxs-lookup"><span data-stu-id="b5188-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="b5188-110">Gehen Sie zu **Allgemein > Einstellungen > Benutzeroptionen**.</span><span class="sxs-lookup"><span data-stu-id="b5188-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="b5188-111">Klicken Sie auf die Registerkarte **Workflow** und überprüfen Sie, ob der Abschnitt „Delegierungׅ“ erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="b5188-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="b5188-112">Um das System so zu konfigurieren, dass Ihre Arbeitsaufgaben automatisch an andere Benutzer delegiert werden, müssen Sie Delegierungsregeln erstellen. Diese geben an, wann bestimmte Typen von Arbeitsaufgaben delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="b5188-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="b5188-113">Gehen Sie folgendermaßen vor, um eine Delegierungsregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b5188-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="b5188-114">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="b5188-114">Click **Add**.</span></span>
4. <span data-ttu-id="b5188-115">Wählen Sie im Feld **Bereich** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="b5188-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="b5188-116">Alle – Delegiert alle Arbeitsaufgaben, die Ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b5188-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="b5188-117">Modul – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflowtyp zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="b5188-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="b5188-118">Wenn Sie diese Option aktivieren, müssen Sie den Workflowtyp im Feld „Name” auswählen.</span><span class="sxs-lookup"><span data-stu-id="b5188-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="b5188-119">Workflow – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflow zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="b5188-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="b5188-120">Wenn Sie diese Option aktivieren, müssen Sie den Workflow im Feld „Name” auswählen.</span><span class="sxs-lookup"><span data-stu-id="b5188-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="b5188-121">Wählen Sie im Feld **Delegat** den Benutzer aus, an den die Arbeitsaufgaben delegiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b5188-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="b5188-122">Geben Sie in den Feldern Startdatum/-zeit und Enddatum/-zeit an, wann die Arbeitsaufgaben automatisch delegiert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="b5188-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="b5188-123">Geben Sie im Feld **Startdatum/-uhrzeit** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="b5188-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="b5188-124">Geben Sie im Feld **Enddatum/-uhrzeit** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="b5188-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="b5188-125">Aktivieren Sie die Delegierungsregel durch Aktivieren des Kontrollkästchens **Aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="b5188-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="b5188-126">Wenn Sie **Modul** als den „Bereich“ ausgewählt haben, müssen Sie das Modul im Feld „Name“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="b5188-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="b5188-127">Wenn Sie **Workflow** als den „Bereich“ ausgewählt haben, müssen Sie den spezifischen zu delegierenden Workflow im Feld „Name“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="b5188-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="b5188-128">Geben Sie im Feld **Kommentar** einen Kommentar ein, der den Grund für die Delegierung der Arbeitsaufgaben erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5188-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

