---
title: Erstellen von Wartungsbudgets
description: In diesem Thema wird erläutert, wie Wartungsbudgets in der Anlagenverwaltung erstellt werden.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b91b398c4ef864a92a5318b7e80f71a5a572844e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836757"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="a78c9-103">Erstellen von Wartungsbudgets</span><span class="sxs-lookup"><span data-stu-id="a78c9-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="a78c9-104">Wartungsbudgets werden verwendet, um eine Übersicht über die erwarteten Kosten für vorbeugende Wartungsaufträge bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a78c9-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="a78c9-105">Budgetpositionen werden auf Grundlage der Wartungsplanpositionen berechnet, die ein voraussichtliches Startdatum während der Budgetperiode haben.</span><span class="sxs-lookup"><span data-stu-id="a78c9-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="a78c9-106">Wartungsbudgets basieren auf den Kostentypen, die in der Anlagenverwaltung verwendet werden: **Vorbeugend**, **Korrektiv** und **Investition**.</span><span class="sxs-lookup"><span data-stu-id="a78c9-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="a78c9-107">Budgetkosten für die Investitionswartung sind für aktive Anlagen enthalten, die ein Ersetzungsdatum während der Budgetperiode und einen zugehörigen Wiederbeschaffungswert haben.</span><span class="sxs-lookup"><span data-stu-id="a78c9-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="a78c9-108">Budgetkosten für korrektive Wartung werden eingeschlossen, wenn ein Korrekturdatum in der Vergangenheit in der Budgetkalkulation enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a78c9-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="a78c9-109">In diesem Fall werden Korrekturkosten einer früheren Periode für die gleiche zukünftige Periode berechnet, für die Sie das Wartungsbudget berechnen.</span><span class="sxs-lookup"><span data-stu-id="a78c9-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="a78c9-110">Erstellen eines Wartungsbudgets</span><span class="sxs-lookup"><span data-stu-id="a78c9-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="a78c9-111">Wählen Sie **Anlagenverwaltung** \> **Abfragen** \> **Wartungsbudget** \> **Budget** aus.</span><span class="sxs-lookup"><span data-stu-id="a78c9-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="a78c9-112">Wählen Sie **Budget erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="a78c9-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="a78c9-113">Geben Sie im Feld **Wartungsbudget** eine Budgetkennung ein.</span><span class="sxs-lookup"><span data-stu-id="a78c9-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="a78c9-114">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="a78c9-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="a78c9-115">Geben Sie auf dem Inforegister **Periode** in den Feldern **Anfangsdatum** und **Enddatum** das Start- und Enddatum für die Budgetperiode ein.</span><span class="sxs-lookup"><span data-stu-id="a78c9-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="a78c9-116">Um korrektive Budgetkosten einzubeziehen, die basierend auf den Istkosten aus einer vorherigen Periode berechnet werden, geben Sie im Feld **Anfangsdatum für Korrektur** das Startdatum der Periode an, ab dem diese Kosten enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="a78c9-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="a78c9-117">Je nach der Detailebene, die im Budget erforderlich ist, legen Sie die entsprechenden Optionen in die fünf Inforegistern **Gruppieren nach** fest.</span><span class="sxs-lookup"><span data-stu-id="a78c9-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="a78c9-118">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="a78c9-118">Select **OK**.</span></span>
8. <span data-ttu-id="a78c9-119">Wählen Sie **Budgetpositionen** aus, um die Seite **Wartungsbudgetpositionen** zu öffnen, in der Sie alle Budgetpositionen anzeigen können, die für den Zeitraum erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a78c9-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="a78c9-120">Um das Budget zu genehmigen, wählen Sie dieses auf der Seite **Wartungsbudgets** aus, und wählen Sie dann **Genehmigen** aus.</span><span class="sxs-lookup"><span data-stu-id="a78c9-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="a78c9-121">Im Dialogfeld **Budget genehmigen** wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a78c9-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="a78c9-122">Ihr Name wird im Feld **Genehmigt von** auf der Seite **Wartungsbudgets** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="a78c9-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a78c9-123">Nachdem Sie ein Wartungsbudget genehmigt haben, können Sie die zugehörigen Positionen der Seite **Wartungsbudgetpositionen** nicht neu berechnen oder anpassen, sofern Sie die Genehmigung nicht zunächst entfernen.</span><span class="sxs-lookup"><span data-stu-id="a78c9-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="a78c9-124">Um die Genehmigung eines Wartungsbudgets zu entfernen, wählen Sie dieses auf der Seite **Wartungsbudgets** aus, und wählen Sie dann **Genehmigen** aus.</span><span class="sxs-lookup"><span data-stu-id="a78c9-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="a78c9-125">Im Dialogfeld **Budget genehmigen** wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a78c9-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Wartungsbudgets](media/01-maintenance-budgets.png)

<span data-ttu-id="a78c9-127">Sie können auch ein neues Wartungsbudget erstellen, indem Sie ein vorhandenes Budget kopieren.</span><span class="sxs-lookup"><span data-stu-id="a78c9-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="a78c9-128">Wählen Sie auf der Seite **Wartungsbudgets** das zu kopierende Budget aus, und wählen Sie dann **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a78c9-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="a78c9-129">Dieser Ansatz ist hilfreich, wenn Sie z. B. ein Budget für einen Monat erstellt haben und dieses in andere Monate kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a78c9-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="a78c9-130">Das Wartungsbudget berechnet nur Budgetkosten auf Grundlage der Wartungsplanpositionen.</span><span class="sxs-lookup"><span data-stu-id="a78c9-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="a78c9-131">Um Istkosten für die gleiche Periode zu berechnen, können Sie diese Berechnung auf der Seite **Kostensteuerung für Anlagen** vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a78c9-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]