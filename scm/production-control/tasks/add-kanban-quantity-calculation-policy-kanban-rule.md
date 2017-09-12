--- 
title: "Kanban-Mengen-Berechnungsrichtlinie zu einer Kanban-Regel hinzufügen"
description: "Der Schwerpunkt dieser Prozedur liegt auf dem Erstellen einer Richtlinie zur Kanban-Mengenberechnung und dem Hinzufügen dieser zu einer Kanban-Regel, mit der die Kanban-Größe und -menge optimiert wird."
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6a947d4a5302c6ed1848396d50cfbfcb78aabf97
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="4ff36-103">Kanban-Mengen-Berechnungsrichtlinie zu einer Kanban-Regel hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4ff36-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ff36-104">Der Schwerpunkt dieser Prozedur liegt auf dem Erstellen einer Richtlinie zur Kanban-Mengenberechnung und dem Hinzufügen dieser zu einer Kanban-Regel, mit der die Kanban-Größe und -menge optimiert wird.</span><span class="sxs-lookup"><span data-stu-id="4ff36-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="4ff36-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="4ff36-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4ff36-106">Diese Vorgehensweise ist für den Wertstrommanager vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4ff36-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="4ff36-107">Dieses Verfahren wird für die Erstellung des Verfahrens "Kanban-Mengenvorschläge berechnen" vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4ff36-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="4ff36-108">Richtlinie zur Kanban-Mengenberechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="4ff36-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="4ff36-109">Wechseln Sie zu "Produktionssteuerung" > "Periodische Aufgaben" > "Kanban-Mengenberechnung" > "Richtlinien zur Kanban-Mengenberechnung".</span><span class="sxs-lookup"><span data-stu-id="4ff36-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="4ff36-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4ff36-110">Click New.</span></span>
3. <span data-ttu-id="4ff36-111">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4ff36-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="4ff36-112">Geben Sie beispielsweise "Speaker2016" ein.</span><span class="sxs-lookup"><span data-stu-id="4ff36-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="4ff36-113">Klicken Sie im Feld "Produktprogrammplan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4ff36-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4ff36-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4ff36-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4ff36-115">Wählen Sie "StaticPlan" aus, um Bedarf zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="4ff36-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="4ff36-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ff36-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4ff36-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4ff36-117">Click Save.</span></span>
8. <span data-ttu-id="4ff36-118">Geben Sie im Feld "Kanban-Mindestmenge" "1"ein.</span><span class="sxs-lookup"><span data-stu-id="4ff36-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="4ff36-119">Dies ist die zusätzliche Anzahl von Kanbans, die in die Kanban-Mengenberechnung einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="4ff36-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="4ff36-120">Legen Sie den Sicherheitsfaktor auf "1" fest.</span><span class="sxs-lookup"><span data-stu-id="4ff36-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="4ff36-121">Dies ist der Faktor, der zum Berechnen der zusätzlichen Menge des Sicherheitslagerbestands verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ff36-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="4ff36-122">Geben Sie im Feld "Tage voraus" den Wert "30" ein.</span><span class="sxs-lookup"><span data-stu-id="4ff36-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="4ff36-123">Dies ist die Anzahl der Tage vor dem Datum der Kanban-Mengenberechnung, für die der Bedarf in die Berechnung einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="4ff36-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="4ff36-124">Geben Sie im Feld "Tage zurück" den Wert "30" ein.</span><span class="sxs-lookup"><span data-stu-id="4ff36-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="4ff36-125">Dies ist die Anzahl der Tage ab dem Datum der Kanban-Mengenberechnung, für die der Bedarf in die Berechnung einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="4ff36-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="4ff36-126">Die Formel, die für die Berechnung verwendet wird, wird mit den Istwerten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ff36-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="4ff36-127">Beispiel: Kanban-Menge = ((Durchschnittlicher Tagesbedarf x Durchlaufzeit x 2.00)/Produktmenge pro Handhabungseinheit) + 1</span><span class="sxs-lookup"><span data-stu-id="4ff36-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="4ff36-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4ff36-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="4ff36-129">Richtlinie zur Kanban-Mengenberechnung zu einer Kanban-Regel hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4ff36-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="4ff36-130">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="4ff36-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="4ff36-131">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4ff36-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4ff36-132">Wählen Sie Kanban-Regel 000020 für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="4ff36-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="4ff36-133">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ff36-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4ff36-134">Schalten Sie die Erweiterung des Abschnitts "Richtlinien zur Kanban-Mengenberechnung" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="4ff36-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="4ff36-135">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4ff36-135">Click Add.</span></span>
    * <span data-ttu-id="4ff36-136">Fügen Sie die Richtlinie zur Kanban-Mengenberechnung hinzu, die Sie in der vorherigen Unteraufgabe erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4ff36-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="4ff36-137">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ff36-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="4ff36-138">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4ff36-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4ff36-139">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ff36-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4ff36-140">Wählen Sie die Speaker2016-Richtlinie aus, die Sie in der vorherigen Unteraufgabe erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4ff36-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  


