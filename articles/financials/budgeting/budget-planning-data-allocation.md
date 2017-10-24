---
title: "Datenzuteilung für die Budgetplanung"
description: "Dieser Artikel beschreibt die verschiedenen Zuordnungsmethoden, die in der Enterprise edition von Microsoft Dynamics 365 for Finance and Operations verfügbar sind, und wie sie verwendet werden können."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fd7ec30c8253f343b3d41d54c78696cd512b2ef7
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="0d03b-103">Datenzuteilung für Budgetplanung</span><span class="sxs-lookup"><span data-stu-id="0d03b-103">Budget planning data allocation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0d03b-104">Dieser Artikel beschreibt die verschiedenen Zuordnungsmethoden, die in der Enterprise edition von Microsoft Dynamics 365 for Finance and Operations verfügbar sind, und wie sie verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0d03b-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and how they can be used.</span></span>  

<span data-ttu-id="0d03b-105">Sie können die Daten in einem Budgetplan auf vielfältige Weise verteilen, um die geplanten Beträge genau zu darzustellen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="0d03b-106">Zuweisungsmethoden</span><span class="sxs-lookup"><span data-stu-id="0d03b-106">Allocation methods</span></span>
<span data-ttu-id="0d03b-107">Drei Zuordnungsmethoden (Auf Perioden verteilen, Zu Dimensionen zuordnen und Sachkonto-Zuordnungsregeln verwenden) können Budgetplanpositionen erstellen, die auf den Positionen im gleichen Budgetplan basieren.</span><span class="sxs-lookup"><span data-stu-id="0d03b-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="0d03b-108">Drei andere Methoden (Zusammenführen, Verteilen und Aus Budgetplan kopieren), können Budgetplanpositionen in anderen Budgetplänen erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="0d03b-109">Für alle sechs Zuordnungsmethoden geben Sie das Zielszenario an.</span><span class="sxs-lookup"><span data-stu-id="0d03b-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="0d03b-110">Das Zielszenario kann entweder dem Quellszenario gleichen oder sich davon sich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="0d03b-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="0d03b-111">Darüber hinaus können Sie angeben, ob dem Haushaltsplan neue Positionen angehängt oder die aktuellen Positionen im Budgetplan ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="0d03b-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="0d03b-112">[![Auf Perioden verteilen](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Auf Perioden verteilen** – Eine Zuteilungskategorie wird verwendet, um die Budgetplanpositionen von den Quellbudgetplanszenarioperioden im Zielszenario zuzuteilen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="0d03b-113">Der Quellbetrag wird mehreren Positionen im Zielszenario basierend auf dem Prozentsatz und dem Datum zugewiesen, die in der Periodenzuteilungskategorie definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0d03b-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="0d03b-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Zu Dimensionen zuordnen** - die Budgetplanpositionen werden vom Quellbudgetplanungsszenario an einen oder mehrere Positionen im Zielszenario auf Grundlage der Prozentsätze und der Finanzdimensionen zugeordnet, die in einer ausgewählten Bedingung für Budgetzuteilung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0d03b-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="0d03b-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Zusammenführen** - Die Budgetplanpositionen werden aus dem Quellbudgetplanszenario in zugeordneten (untergeordneten) Budgetplänen auf das Zielszenario in den übergeordneten Budgetplan verteilt.</span><span class="sxs-lookup"><span data-stu-id="0d03b-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="0d03b-116">Diese Methode erlaubt Budgetbeträge, die auf einer niedrigeren Ebene in der Organisation vorbereitet werden, auf einer höheren Ebene zu konsolidierenden.</span><span class="sxs-lookup"><span data-stu-id="0d03b-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="0d03b-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Verteilen** - Die Budgetplanpositionen werden vom Quellbudgetplanungsszenario im übergeordneten Budgetplan dem Zielszenario in den zugehörigen (untergeordneten)Budgetplänen auf Grundlage die Finanzdimensionen der Organisationseinheiten der zugeordneten Pläne verteilt.</span><span class="sxs-lookup"><span data-stu-id="0d03b-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="0d03b-118">Diese Methode erlaubt Budgetbeträge, die auf einer höheren Ebene in der Organisation vorbereitet werden, für eine örtlichere Überprüfung auszubreiten.</span><span class="sxs-lookup"><span data-stu-id="0d03b-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="0d03b-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Sachkonto-Zuordnungsregeln verwenden** - Die Budgetplanpositionen werden vom Quellbudgetplanungsszenario auf Grundlage der ausgewählten Sachkonto-Zuordnungsregel auf das Zielbudgetplanszenario verteilt.</span><span class="sxs-lookup"><span data-stu-id="0d03b-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="0d03b-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopie des Haushaltsplans** - Wie bei der Verteilungszuordnungsmethode, Budgetplanpositionen werden im Ziel, auf Grundlage der Positionen in einem dazugehörigen Budgetplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d03b-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="0d03b-121">Für diese Methode muss der Quellbudgetplan nicht der übergeordnete Plan sein, kann jedoch auf jeder höheren Ebene in der Budgetplanhierarchie stehen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="0d03b-122">Diese Zuordnungsmethode ist hilfreich, wenn konsolidierte Beträge ursprünglich auf einer viel höheren Ebene geplant werden, und muss einer untergeordneten Ebene der Organisation für detaillierten Prüfung und Regulierung übertragen werden, bevor sie höhere Genehmigung erhalten können.</span><span class="sxs-lookup"><span data-stu-id="0d03b-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="0d03b-123">Verwenden der Zuordnungsmethoden in einem Budgetplan</span><span class="sxs-lookup"><span data-stu-id="0d03b-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="0d03b-124">Um Zuweisungen auf der Budgetplanseite auszuführen, wählen Sie die zuzuweisenden Positionen aus, und klicken Sie anschließend auf **Budget zuteilen**.</span><span class="sxs-lookup"><span data-stu-id="0d03b-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="0d03b-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="0d03b-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="0d03b-126">Wählen Sie anschließend eine Zuordnungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="0d03b-126">Next, select an allocation method.</span></span> <span data-ttu-id="0d03b-127">Die übrigen Felder werden dann auf Grundlage der Methode festgelegt, die Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="0d03b-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="0d03b-128">Diese Felder enthalten die Quelle und das Ziel der Budgetplandaten und eine Option, mit der Sie die Quelle durch einen angegebenen Faktor multiplizieren können, wenn die Zielbeträge erstellt werden, um die Massenregulierung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="0d03b-129">Sie können auch die Option **An Plan anheften** festlegen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="0d03b-130">Wählen Sie **Nein** aus, um die vorhandenen Budgetplanpositionen zu ersetzen, oder **Ja**, um die vorhandenen Budgetplanpositionen zu verwalten und neue Positionen für die zugeteilten Beträge hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="0d03b-131">Automatisieren von Zuweisungen während eines Workflows</span><span class="sxs-lookup"><span data-stu-id="0d03b-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="0d03b-132">Eine leistungsfähige Funktion ermöglicht es Zuweisungen als Teil eines Budgetplanungsworkflows automatisch ausführen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="0d03b-133">Während ein Budgetplan den Workflow durchläuft, können automatisierte Aufgaben eine Zuteilung in einem angegebenen Budgetplanungsstadium aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="0d03b-134">Um die automatisierte Zuweisung einrichten, müssen Sie auf der Seite **Budgetplanungskonfiguration** zunächst einen Zuteilungszeitplan erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d03b-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="0d03b-135">Der Zuteilungszeitplan definiert die Zuteilungsmethode, die verwendet wird, wenn die automatisierte Zuteilung ausgeführt wird, und die Werte der verschiedenen Zuteilungsoptionen (Informationen dazu finden Sie im vorherigen Abschnitt zu Beschreibungen).</span><span class="sxs-lookup"><span data-stu-id="0d03b-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="0d03b-136">Anschließend erstellen Sie eine Phasenzuteilung auf der Seite **Budgetplanungskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0d03b-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="0d03b-137">Die Phasenzuteilung weist einen Zuteilungsplan dem Budgetplanungsworkflow und der -phase zu.</span><span class="sxs-lookup"><span data-stu-id="0d03b-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="0d03b-138">Schließlich fügen Sie in dem gewünschten Workflowstadium eine automatisierte Aufgabe für Budgetplanungsphasenzuteilung hinzu.</span><span class="sxs-lookup"><span data-stu-id="0d03b-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="0d03b-139">Im folgenden Beispiel wurden zwei Budgetplanungsphasenzuteilungen (in rot umrissen) in den Workflow eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0d03b-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="0d03b-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="0d03b-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




