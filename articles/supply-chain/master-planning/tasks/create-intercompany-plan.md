---
title: Intercompany-Plan erstellen
description: Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978272"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="2e3a5-103">Intercompany-Plan erstellen</span><span class="sxs-lookup"><span data-stu-id="2e3a5-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e3a5-104">Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="2e3a5-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="2e3a5-106">Intercompany-Planungsgruppe einrichten</span><span class="sxs-lookup"><span data-stu-id="2e3a5-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="2e3a5-107">Gehen Sie im **Navigationsbereich** zu **Module > Produktprogrammplanung > Einstellungen > Intercompany-Planungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="2e3a5-108">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2e3a5-109">Filtern Sie beispielsweise im Feld "Name" mit einem Wert "10".</span><span class="sxs-lookup"><span data-stu-id="2e3a5-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="2e3a5-110">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2e3a5-111">Klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-111">Click **Delete**.</span></span> <span data-ttu-id="2e3a5-112">Dieser Schritt ist erforderlich, um die Intercompany-Planung zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="2e3a5-113">Die Intercompany-Planung für die Produktprogrammplanung in allen Unternehmen in einer aus Planungsgruppe aus (ab dem niedrigsten Nummernkreis).</span><span class="sxs-lookup"><span data-stu-id="2e3a5-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="2e3a5-114">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-114">Click **Yes**.</span></span>
6. <span data-ttu-id="2e3a5-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="2e3a5-116">Intercompany-Plan erstellen</span><span class="sxs-lookup"><span data-stu-id="2e3a5-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="2e3a5-117">Gehen Sie im **Navigationsbereich** zu **Module > Produktprogrammplanung > Arbeitsbereiche > Produktprogrammplanung**.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="2e3a5-118">Klicken Sie auf **Intercompany-Produktprogrammplanungslauf**.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="2e3a5-119">Klicken Sie im Feld **Intercompany-Planungsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2e3a5-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="2e3a5-121">Wählen Sie die Intercompany-Planungsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="2e3a5-122">Geben Sie im Feld **Anzahl der Intercompany-Planungsiterationen** '2' ein.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="2e3a5-123">Intercompany-Planungsgruppe 10 hat zwei Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="2e3a5-124">Um die Verzögerungen aus dem Ausgangsunternehmen (USMF) an das Kundenunternehmen (DEMF) weiterzugeben, müssen Sie Intercompany in beiden Unternehmen einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="2e3a5-125">Der erste Durchlauf gibt den Bedarf weiter und identifiziert die Verzögerungen im Quellunternehmen (USMF).</span><span class="sxs-lookup"><span data-stu-id="2e3a5-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="2e3a5-126">Der zweite Durchlauf gibt die Verzögerungen von USMF an DEMF weiter.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="2e3a5-127">Wählen Sie im Feld **Erste Iteration** 'Neu erzeugen' aus.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="2e3a5-128">Wählen Sie im Feld **Nachfolgende Iterationen** 'Neu erzeugen' aus.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="2e3a5-129">Geben Sie im Feld **Anzahl von Threads** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="2e3a5-130">Dies stellt die Anzahl von parallelen Threads für die Planung dar.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="2e3a5-131">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="2e3a5-132">Ergebnis der Planung anzeigen</span><span class="sxs-lookup"><span data-stu-id="2e3a5-132">View the result of the plan</span></span>
1. <span data-ttu-id="2e3a5-133">Klicken Sie im Feld **Plan** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="2e3a5-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="2e3a5-135">Klicken Sie auf den Link für StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="2e3a5-136">Sie müssen im Unternehmen USMF sein.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="2e3a5-137">Klicken Sie auf **Bestellvorschläge**.</span><span class="sxs-lookup"><span data-stu-id="2e3a5-137">Click **Planned orders**.</span></span>

