--- 
title: Delegieren von Arbeitsaufgaben in einem Workflow
description: "Wenn Sie für einige Zeit abwesend oder anderweitig für Arbeitsaufgaben nicht verfügbar sind, können Sie Ihre Arbeitsaufgaben an andere Benutzer delegieren oder diesen neu zuweisen."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4765fec0cdce0e2f8859c979ff97d20aa6b20bfa
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="f3f3f-103">Delegieren von Arbeitsaufgaben in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="f3f3f-103">Delegate work items in a workflow</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3f3f-104">Wenn Sie für einige Zeit abwesend oder anderweitig für Arbeitsaufgaben nicht verfügbar sind, können Sie Ihre Arbeitsaufgaben an andere Benutzer delegieren oder diesen neu zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="f3f3f-105">Mithilfe dieser Prozedur können Sie das System konfigurieren, damit Ihre Arbeitsartikel automatisch an einen anderen Benutzer delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="f3f3f-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="f3f3f-107">Einrichten der automatischen Delegierung</span><span class="sxs-lookup"><span data-stu-id="f3f3f-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="f3f3f-108">Gehen Sie zu > Allgemein > Benutzeroptionen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="f3f3f-109">Klicken Sie auf die Registerkarte „Workflow”.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="f3f3f-110">Stellen Sie sicher, dass der Bereich „Delegation” erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="f3f3f-111">Um das System so zu konfigurieren, dass Ihre Arbeitsaufgaben automatisch an andere Benutzer delegiert werden, müssen Sie Delegierungsregeln erstellen. Diese geben an, wann bestimmte Typen von Arbeitsaufgaben delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="f3f3f-112">Gehen Sie folgendermaßen vor, um eine Delegierungsregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="f3f3f-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-113">Click Add.</span></span>
4. <span data-ttu-id="f3f3f-114">Wählen Sie im Feld „Bereich” eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="f3f3f-115">Alle – Delegiert alle Arbeitsaufgaben, die Ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="f3f3f-116">Modul – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflowtyp zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="f3f3f-117">Wenn Sie diese Option aktivieren, müssen Sie den Workflowtyp im Feld „Name” auswählen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="f3f3f-118">Workflow – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflow zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="f3f3f-119">Wenn Sie diese Option aktivieren, müssen Sie den Workflow im Feld „Name” auswählen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="f3f3f-120">Wählen Sie im Feld „Delegat” den Benutzer aus, an den die Arbeitsaufgaben delegiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="f3f3f-121">Geben Sie in den Feldern Startdatum/-zeit und Enddatum/-zeit an, wann die Arbeitsaufgaben automatisch delegiert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="f3f3f-122">Geben Sie im Feld „Startdaum/-uhrzeit” ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="f3f3f-123">Geben Sie im Feld „Enddatum/-uhrzeit” ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="f3f3f-124">Aktivieren Sie die Delegierungsregel durch Aktivieren des Kontrollkästchens „Aktiviert”.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="f3f3f-125">Wenn Sie „Modul” als den „Bereich” ausgewählt haben, müssen Sie das Modul im Feld „Name” auswählen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="f3f3f-126">Wenn Sie „Workflow” als den „Bereich” ausgewählt haben, müssen Sie den spezfischen zu delegierenden Workflow im Feld „Name” auswählen.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="f3f3f-127">Geben Sie im Feld „Kommentar” einen Kommentar ein, der den Grund für die Delegierung der Arbeitsaufgaben erläutert.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


