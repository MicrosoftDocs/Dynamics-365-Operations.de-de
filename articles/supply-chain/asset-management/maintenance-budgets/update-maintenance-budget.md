---
title: Aktualisierung der Wartungsbudgets
description: In diesem Abschnitt erfahren Sie, wie Sie ein Instandhaltungsbudget im Anlagenmanagement aktualisieren.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b04549700b51f73a3629fe9cd67a3e1f6c1bafbb
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021023"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="5c593-103">Aktualisierung der Wartungsbudgets</span><span class="sxs-lookup"><span data-stu-id="5c593-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5c593-104">Auf der Seite **Wartungsbudgetzeilen** werden alle Budgetzeilen angezeigt, die für das Budget angelegt wurden, das auf der Seite **Wartungsbudgets** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="5c593-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="5c593-105">(Weitere Informationen finden Sie unter [Wartungsbudgets anlegen](create-maintenance-budget.md).) Sie können Wartungsbudgetpositionen neu berechnen und anpassen, bis das Wartungsbudget genehmigt ist.</span><span class="sxs-lookup"><span data-stu-id="5c593-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="5c593-106">Nach Ablauf der Budgetperiode und der Buchung von Kosten im Anlagenmanagement können Sie die Budgetpositionen auch mit Istkosten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5c593-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="5c593-107">Neuberechnung eines Wartungsbudgets</span><span class="sxs-lookup"><span data-stu-id="5c593-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="5c593-108">Sie können ein Wartungsbudget auf der Seite **Wartungsbudgetzeilen** neu berechnen.</span><span class="sxs-lookup"><span data-stu-id="5c593-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="5c593-109">Wenn Sie ein Wartungsbudget neu berechnen, werden die vorhandenen Budgetpositionen gelöscht und eine Neuberechnung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c593-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="5c593-110">Wählen Sie auf der Seite **Wartungsbudgetlinien** **Neu berechnen**.</span><span class="sxs-lookup"><span data-stu-id="5c593-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="5c593-111">Nehmen Sie im Dialogfenster **Budget neu berechnen** die erforderlichen Änderungen für die neue Kalkulation vor und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c593-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="5c593-112">Neue Budgetpositionen werden entsprechend den von Ihnen festgelegten Werten angelegt.</span><span class="sxs-lookup"><span data-stu-id="5c593-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="5c593-113">Anpassung der Budgetzeilen</span><span class="sxs-lookup"><span data-stu-id="5c593-113">Adjust budget lines</span></span>

<span data-ttu-id="5c593-114">Anstatt das gesamte Wartungsbudget neu zu berechnen, können Sie ausgewählte Zeilen, die sich auf die Budgetkosten beziehen, anpassen.</span><span class="sxs-lookup"><span data-stu-id="5c593-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="5c593-115">Markieren Sie auf der Seite **Wartungsbudgetlinien** die Zeilen, für die die Budgetkosten aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c593-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="5c593-116">Wählen Sie **Anpassen**.</span><span class="sxs-lookup"><span data-stu-id="5c593-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="5c593-117">Um einen Betrag zu den ausgewählten Zeilen hinzuzufügen, aktivieren Sie das Kontrollkästchen **Kosten hinzufügen**, und geben Sie dann den Wert in das Feld **Wert hinzufügen** ein.</span><span class="sxs-lookup"><span data-stu-id="5c593-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="5c593-118">Um die Budgetkosten auf den ausgewählten Budgetpositionen mit einem Faktor zu multiplizieren, aktivieren Sie das Kontrollkästchen **Kosten multiplizieren** und geben Sie den Faktor in das Feld **Wert multiplizieren** ein.</span><span class="sxs-lookup"><span data-stu-id="5c593-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="5c593-119">Wenn Sie z.B. **1,2** in das Feld **Multiplizierter Wert** eingeben, erhöhen Sie die Budgetkosten für die ausgewählten Zeilen um 20 Prozent.</span><span class="sxs-lookup"><span data-stu-id="5c593-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="5c593-120">Wenn Sie **0,7** eingeben, reduzieren Sie die Budgetkosten auf den ausgewählten Zeilen um 30 Prozent.</span><span class="sxs-lookup"><span data-stu-id="5c593-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="5c593-121">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c593-121">Select **OK**.</span></span>

<span data-ttu-id="5c593-122">Die ausgewählten Budgetpositionen werden entsprechend den Werten aktualisiert, die Sie in Schritt 3 oder 4 festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="5c593-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="5c593-123">Fortschreibung der Istkosten</span><span class="sxs-lookup"><span data-stu-id="5c593-123">Update actual costs</span></span>

<span data-ttu-id="5c593-124">Nachdem die Termine der Budgetzeilen abgelaufen sind und die Istkosten in der Anlagenbuchhaltung gebucht wurden, können Sie die Istkosten auf dem Wartungsbudget aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5c593-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="5c593-125">Wählen Sie auf der Seite **Wartungsbudgetlinien** **Aktualisierungskosten**.</span><span class="sxs-lookup"><span data-stu-id="5c593-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="5c593-126">Wählen Sie im Dialogfenster **Istkosten berechnen** **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c593-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="5c593-127">Die Felder **Istkosten** auf den Budgetzeilen werden aktualisiert, wenn Istkosten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="5c593-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="5c593-128">Neue Budgetpositionen können erzeugt werden, wenn seit der Erstellung des Budgets neue Anlagenarten angelegt wurden und wenn diese Anlagenarten auf Anlagen verwendet wurden, für die Arbeitsaufträge angelegt wurden und für die entsprechende Kosten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="5c593-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="5c593-129">Neue Budgetpositionen zeigen nur die Istkosten an, da für sie keine Budgetkosten berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="5c593-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="5c593-130">Um eine Übersicht über die Istkosten gegliedert nach Präventions-, Korrektur- und Investitionskosten zu erhalten, können Sie auf der Seite **Assetkostenkontrolle** eine Berechnung für den gleichen Zeitraum durchführen.</span><span class="sxs-lookup"><span data-stu-id="5c593-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="5c593-131">Budgetpositionen manuell hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5c593-131">Manually add budget lines</span></span>

<span data-ttu-id="5c593-132">Auf der Seite **Wartungsbudgetlinien** können Sie manuell eine neue Budgetposition hinzufügen, indem Sie **Neu** auswählen und dann auf der Position auswählen.</span><span class="sxs-lookup"><span data-stu-id="5c593-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="5c593-133">Hier sind einige Beispiele für Situationen, in denen dieser Ansatz nützlich sein könnte:</span><span class="sxs-lookup"><span data-stu-id="5c593-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="5c593-134">Sie wissen, dass sich die Renovierung einiger Anlagen derzeit in der Planungsphase befindet, aber damit verbundene Arbeitsplätze im Asset Management noch nicht geschaffen wurden.</span><span class="sxs-lookup"><span data-stu-id="5c593-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="5c593-135">Sie möchten jedoch, dass die Budgetkosten für diese Stellen in das Wartungsbudget aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="5c593-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="5c593-136">Neue Anlagen oder Anlagenarten wurden seit der Erstellung des Wartungsbudgets angelegt, aber für diese Anlagen oder Anlagenarten wurden noch keine Wartungspläne eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="5c593-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="5c593-137">Sie möchten jedoch, dass die Budgetkosten für diese Anlagenarten in das Wartungsbudget aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="5c593-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
