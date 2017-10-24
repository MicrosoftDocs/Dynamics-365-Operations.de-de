--- 
title: Intercompany-Plan erstellen
description: Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="626b6-103">Intercompany-Plan erstellen</span><span class="sxs-lookup"><span data-stu-id="626b6-103">Create an intercompany plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="626b6-104">Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="626b6-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="626b6-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="626b6-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="626b6-106">Intercompany-Planungsgruppe einrichten</span><span class="sxs-lookup"><span data-stu-id="626b6-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="626b6-107">Wechseln Sie zu Intercompany-Planungsgruppen.</span><span class="sxs-lookup"><span data-stu-id="626b6-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="626b6-108">"Produktprogrammplan" > "Einrichten" > "Intercompany-Planungsgruppen"</span><span class="sxs-lookup"><span data-stu-id="626b6-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="626b6-109">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="626b6-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="626b6-110">Filtern Sie beispielsweise im Feld "Name" mit einem Wert "10".</span><span class="sxs-lookup"><span data-stu-id="626b6-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="626b6-111">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="626b6-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="626b6-112">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="626b6-112">Click Delete.</span></span>
    * <span data-ttu-id="626b6-113">Dieser Schritt ist erforderlich, um die Intercompany-Planung zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="626b6-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="626b6-114">Die Intercompany-Planung für die Produktprogrammplanung in allen Unternehmen in einer aus Planungsgruppe aus (ab dem niedrigsten Nummernkreis).</span><span class="sxs-lookup"><span data-stu-id="626b6-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="626b6-115">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="626b6-115">Click Yes.</span></span>
6. <span data-ttu-id="626b6-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="626b6-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="626b6-117">Intercompany-Plan erstellen</span><span class="sxs-lookup"><span data-stu-id="626b6-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="626b6-118">Klicken Sie auf "Intercompany-Produktprogrammplanungslauf".</span><span class="sxs-lookup"><span data-stu-id="626b6-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="626b6-119">Dies ist auf dem Produktprogrammplanungsarbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="626b6-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="626b6-120">Klicken Sie im Feld "Intercompany-Planungsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="626b6-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="626b6-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="626b6-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="626b6-122">Wählen Sie die Intercompany-Planungsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="626b6-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="626b6-123">Geben Sie im Feld "Anzahl der Intercompany-Planungsiterationen" 2 ein.</span><span class="sxs-lookup"><span data-stu-id="626b6-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="626b6-124">Intercompany-Planungsgruppe 10 hat zwei Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="626b6-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="626b6-125">Um die Verzögerungen aus dem Ausgangsunternehmen (USMF) an das Kundenunternehmen (DEMF) weiterzugeben, müssen Sie Intercompany in beiden Unternehmen einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="626b6-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="626b6-126">Der erste Durchlauf gibt den Bedarf weiter und identifiziert die Verzögerungen im Quellunternehmen (USMF).</span><span class="sxs-lookup"><span data-stu-id="626b6-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="626b6-127">Der zweite Durchlauf gibt die Verzögerungen von USMF an DEMF weiter.</span><span class="sxs-lookup"><span data-stu-id="626b6-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="626b6-128">Wählen Sie im Feld 'Erste Iteration' eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="626b6-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="626b6-129">Wählen Sie im Feld 'Erste Iteration' "Neu erzeugen" aus.</span><span class="sxs-lookup"><span data-stu-id="626b6-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="626b6-130">Wählen Sie im Feld 'Nachfolgende Iterationen' "Neu erzeugen" aus.</span><span class="sxs-lookup"><span data-stu-id="626b6-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="626b6-131">Geben Sie im Feld "Anzahl von Threads" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="626b6-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="626b6-132">Dies stellt die Anzahl von parallelen Threads für die Planung dar.</span><span class="sxs-lookup"><span data-stu-id="626b6-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="626b6-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="626b6-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="626b6-134">Ergebnis der Planung anzeigen</span><span class="sxs-lookup"><span data-stu-id="626b6-134">View the result of the plan</span></span>
1. <span data-ttu-id="626b6-135">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="626b6-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="626b6-136">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="626b6-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="626b6-137">Klicken Sie auf den Link für StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="626b6-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="626b6-138">Sie müssen im Unternehmen USMF sein.</span><span class="sxs-lookup"><span data-stu-id="626b6-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="626b6-139">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="626b6-139">Click Planned orders.</span></span>


