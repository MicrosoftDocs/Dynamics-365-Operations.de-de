---
title: Intercompany-Plan erstellen
description: Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.
author: ShylaThompson
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0fb787955a67776b24b626eb23b7c1a9df87a0c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841694"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="bd633-103">Intercompany-Plan erstellen</span><span class="sxs-lookup"><span data-stu-id="bd633-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd633-104">Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bd633-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="bd633-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="bd633-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="bd633-106">Intercompany-Planungsgruppe einrichten</span><span class="sxs-lookup"><span data-stu-id="bd633-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="bd633-107">Gehen Sie im **Navigationsbereich** zu **Module > Produktprogrammplanung > Einstellungen > Intercompany-Planungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="bd633-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="bd633-108">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bd633-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bd633-109">Filtern Sie beispielsweise im Feld "Name" mit einem Wert "10".</span><span class="sxs-lookup"><span data-stu-id="bd633-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="bd633-110">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="bd633-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bd633-111">Klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="bd633-111">Click **Delete**.</span></span> <span data-ttu-id="bd633-112">Dieser Schritt ist erforderlich, um die Intercompany-Planung zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="bd633-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="bd633-113">Die Intercompany-Planung für die Produktprogrammplanung in allen Unternehmen in einer aus Planungsgruppe aus (ab dem niedrigsten Nummernkreis).</span><span class="sxs-lookup"><span data-stu-id="bd633-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="bd633-114">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bd633-114">Click **Yes**.</span></span>
6. <span data-ttu-id="bd633-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bd633-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="bd633-116">Intercompany-Plan erstellen</span><span class="sxs-lookup"><span data-stu-id="bd633-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="bd633-117">Gehen Sie im **Navigationsbereich** zu **Module > Produktprogrammplanung > Arbeitsbereiche > Produktprogrammplanung**.</span><span class="sxs-lookup"><span data-stu-id="bd633-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="bd633-118">Klicken Sie auf **Intercompany-Produktprogrammplanungslauf**.</span><span class="sxs-lookup"><span data-stu-id="bd633-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="bd633-119">Klicken Sie im Feld **Intercompany-Planungsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bd633-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bd633-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="bd633-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="bd633-121">Wählen Sie die Intercompany-Planungsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="bd633-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="bd633-122">Geben Sie im Feld **Anzahl der Intercompany-Planungsiterationen** '2' ein.</span><span class="sxs-lookup"><span data-stu-id="bd633-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="bd633-123">Intercompany-Planungsgruppe 10 hat zwei Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="bd633-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="bd633-124">Um die Verzögerungen aus dem Ausgangsunternehmen (USMF) an das Kundenunternehmen (DEMF) weiterzugeben, müssen Sie Intercompany in beiden Unternehmen einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd633-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="bd633-125">Der erste Durchlauf gibt den Bedarf weiter und identifiziert die Verzögerungen im Quellunternehmen (USMF).</span><span class="sxs-lookup"><span data-stu-id="bd633-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="bd633-126">Der zweite Durchlauf gibt die Verzögerungen von USMF an DEMF weiter.</span><span class="sxs-lookup"><span data-stu-id="bd633-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="bd633-127">Wählen Sie im Feld **Erste Iteration** 'Neu erzeugen' aus.</span><span class="sxs-lookup"><span data-stu-id="bd633-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="bd633-128">Wählen Sie im Feld **Nachfolgende Iterationen** 'Neu erzeugen' aus.</span><span class="sxs-lookup"><span data-stu-id="bd633-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="bd633-129">Geben Sie im Feld **Anzahl von Threads** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="bd633-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="bd633-130">Dies stellt die Anzahl von parallelen Threads für die Planung dar.</span><span class="sxs-lookup"><span data-stu-id="bd633-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="bd633-131">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd633-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="bd633-132">Ergebnis der Planung anzeigen</span><span class="sxs-lookup"><span data-stu-id="bd633-132">View the result of the plan</span></span>
1. <span data-ttu-id="bd633-133">Klicken Sie im Feld **Plan** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bd633-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="bd633-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="bd633-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="bd633-135">Klicken Sie auf den Link für StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="bd633-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="bd633-136">Sie müssen im Unternehmen USMF sein.</span><span class="sxs-lookup"><span data-stu-id="bd633-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="bd633-137">Klicken Sie auf **Bestellvorschläge**.</span><span class="sxs-lookup"><span data-stu-id="bd633-137">Click **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]