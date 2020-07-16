---
title: Delegieren von Arbeitsaufgaben in einem Workflow
description: Wenn Sie für einige Zeit abwesend oder anderweitig für Arbeitsaufgaben nicht verfügbar sind, können Sie Ihre Arbeitsaufgaben an andere Benutzer delegieren oder diesen neu zuweisen.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515763"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="957ca-103">Delegieren von Arbeitsaufgaben in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="957ca-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="957ca-104">Manuelles Delegieren einer Arbeitsaufgabe</span><span class="sxs-lookup"><span data-stu-id="957ca-104">Manually delegate a work item</span></span>

<span data-ttu-id="957ca-105">Um eine einzelne Arbeitsaufgabe zu delegieren, wählen Sie die Option **Delegieren** im Menü **Workflow** aus, und geben Sie dann den Benutzer an, an den delegiert werden soll, zusammen mit einem Kommentar.</span><span class="sxs-lookup"><span data-stu-id="957ca-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="957ca-106">Dadurch wird die Arbeitsaufgabe an diesen Benutzer neu zugewiesen, sodass sie ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="957ca-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="957ca-107">Manuelles Delegieren mehrerer Arbeitsaufgaben</span><span class="sxs-lookup"><span data-stu-id="957ca-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="957ca-108">Mehrere Arbeitsaufgaben können zusammen über die Seite **Mir zugewiesene Arbeitsaufgaben** delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="957ca-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="957ca-109">Die folgenden Workflowtypen können für die Massendelegierung verwendet werden: Workflow zur Genehmigung von Kaufverträgen, Workflow für Bestellungen, Workflow zur Überprüfung von Bestellanforderungen und Workflow für Kreditorenrechnungen.</span><span class="sxs-lookup"><span data-stu-id="957ca-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="957ca-110">Die Funktion **Mehrere Arbeitsaufgaben delegieren** ist standardmäßig deaktiviert und kann unter **Arbeitsbereiche > Funktionsverwaltung** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="957ca-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="957ca-111">Bitten Sie Ihren Systemadministrator um Hilfe, um diese Funktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="957ca-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="957ca-112">Wechseln Sie zu **Allgemeines > Allgemeines > Arbeitsaufgaben > Mir zugewiesene Arbeitsaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="957ca-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="957ca-113">Wählen Sie die Arbeitsaufgaben aus, die delegiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="957ca-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="957ca-114">Klicken Sie auf das Menü **Arbeitsaufgaben delegieren**.</span><span class="sxs-lookup"><span data-stu-id="957ca-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="957ca-115">Wählen Sie im Feld **Benutzer** den Benutzer aus, an den die Arbeitsaufgaben delegiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="957ca-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="957ca-116">Geben Sie in das Feld **Kommentar** einen Kommentar ein, der den Grund für die Delegierung der Arbeitsaufgaben erläutert.</span><span class="sxs-lookup"><span data-stu-id="957ca-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="957ca-117">Klicken Sie auf die Schaltfläche **Arbeitsaufgaben delegieren**, um die Delegierung der Arbeitsaufgaben abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="957ca-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="957ca-118">Arbeitsaufgaben automatisch delegieren</span><span class="sxs-lookup"><span data-stu-id="957ca-118">Automatically delegate work items</span></span>

<span data-ttu-id="957ca-119">Wenn Sie planen, für einen Zeitraum nicht im Büro anwesend oder anderweitig nicht verfügbar zu sein, um sich um Arbeitsaufgaben zu kümmern, können Sie neue Arbeitsaufgaben automatisch an andere Benutzer mithilfe der Seite **Benutzeroptionen** delegieren.</span><span class="sxs-lookup"><span data-stu-id="957ca-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="957ca-120">Einrichten der automatischen Delegierung</span><span class="sxs-lookup"><span data-stu-id="957ca-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="957ca-121">Gehen Sie zu **Allgemein > Einstellungen > Benutzeroptionen**.</span><span class="sxs-lookup"><span data-stu-id="957ca-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="957ca-122">Klicken Sie auf die Registerkarte **Workflow** und überprüfen Sie, ob der Abschnitt „Delegierungׅ“ erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="957ca-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="957ca-123">Um das System so zu konfigurieren, dass Ihre Arbeitsaufgaben automatisch an andere Benutzer delegiert werden, müssen Sie Delegierungsregeln erstellen. Diese geben an, wann bestimmte Typen von Arbeitsaufgaben delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="957ca-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="957ca-124">Gehen Sie folgendermaßen vor, um eine Delegierungsregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="957ca-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="957ca-125">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="957ca-125">Click **Add**.</span></span>
4. <span data-ttu-id="957ca-126">Wählen Sie im Feld **Bereich** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="957ca-126">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="957ca-127">Alle – Delegiert alle Arbeitsaufgaben, die Ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="957ca-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="957ca-128">Modul – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflowtyp zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="957ca-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="957ca-129">Wenn Sie diese Option aktivieren, müssen Sie den Workflowtyp im Feld „Name” auswählen.</span><span class="sxs-lookup"><span data-stu-id="957ca-129">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="957ca-130">Workflow – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflow zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="957ca-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="957ca-131">Wenn Sie diese Option aktivieren, müssen Sie den Workflow im Feld „Name” auswählen.</span><span class="sxs-lookup"><span data-stu-id="957ca-131">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="957ca-132">Wählen Sie im Feld **Delegat** den Benutzer aus, an den die Arbeitsaufgaben delegiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="957ca-132">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="957ca-133">Geben Sie in den Feldern Startdatum/-zeit und Enddatum/-zeit an, wann die Arbeitsaufgaben automatisch delegiert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="957ca-133">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="957ca-134">Geben Sie im Feld **Startdatum/-uhrzeit** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="957ca-134">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="957ca-135">Geben Sie im Feld **Enddatum/-uhrzeit** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="957ca-135">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="957ca-136">Aktivieren Sie die Delegierungsregel durch Aktivieren des Kontrollkästchens **Aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="957ca-136">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="957ca-137">Wenn Sie **Modul** als den „Bereich“ ausgewählt haben, müssen Sie das Modul im Feld „Name“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="957ca-137">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="957ca-138">Wenn Sie **Workflow** als den „Bereich“ ausgewählt haben, müssen Sie den spezifischen zu delegierenden Workflow im Feld „Name“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="957ca-138">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="957ca-139">Geben Sie in das Feld **Kommentar** einen Kommentar ein, der den Grund für die Delegierung der Arbeitsaufgaben erläutert.</span><span class="sxs-lookup"><span data-stu-id="957ca-139">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>

