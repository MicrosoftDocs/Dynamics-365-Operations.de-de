---
title: Erstellen von Wartungsbudgets
description: In diesem Thema wird erläutert, wie Wartungsbudgets in der Anlagenverwaltung erstellt werden.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: aa373a1a15c19154e6c822c3a962c2b43b8d9e10
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205298"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="077bf-103">Erstellen von Wartungsbudgets</span><span class="sxs-lookup"><span data-stu-id="077bf-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="077bf-104">Wartungsbudgets werden verwendet, um eine Übersicht über die erwarteten Kosten für vorbeugende Wartungsaufträge bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="077bf-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="077bf-105">Budgetpositionen werden auf Grundlage der Wartungsplanpositionen berechnet, die ein voraussichtliches Startdatum während der Budgetperiode haben.</span><span class="sxs-lookup"><span data-stu-id="077bf-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="077bf-106">Wartungsbudgets basieren auf den Kostentypen, die in der Anlagenverwaltung verwendet werden: **Vorbeugend**, **Korrektiv** und **Investition**.</span><span class="sxs-lookup"><span data-stu-id="077bf-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="077bf-107">Budgetkosten für die Investitionswartung sind für aktive Anlagen enthalten, die ein Ersetzungsdatum während der Budgetperiode und einen zugehörigen Wiederbeschaffungswert haben.</span><span class="sxs-lookup"><span data-stu-id="077bf-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="077bf-108">Budgetkosten für korrektive Wartung werden eingeschlossen, wenn ein Korrekturdatum in der Vergangenheit in der Budgetkalkulation enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="077bf-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="077bf-109">In diesem Fall werden Korrekturkosten einer früheren Periode für die gleiche zukünftige Periode berechnet, für die Sie das Wartungsbudget berechnen.</span><span class="sxs-lookup"><span data-stu-id="077bf-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="077bf-110">Erstellen eines Wartungsbudgets</span><span class="sxs-lookup"><span data-stu-id="077bf-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="077bf-111">Wählen Sie **Anlagenverwaltung** \> **Abfragen** \> **Wartungsbudget** \> **Budget** aus.</span><span class="sxs-lookup"><span data-stu-id="077bf-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="077bf-112">Wählen Sie **Budget erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="077bf-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="077bf-113">Geben Sie im Feld **Wartungsbudget** eine Budgetkennung ein.</span><span class="sxs-lookup"><span data-stu-id="077bf-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="077bf-114">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="077bf-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="077bf-115">Geben Sie im Inforegister **Periode** in den Feldern **Anfangsdatum** und **Enddatum** das Start- und Enddatum für die Budgetperiode ein.</span><span class="sxs-lookup"><span data-stu-id="077bf-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="077bf-116">Um korrektive Budgetkosten einzubeziehen, die basierend auf den Istkosten aus einer vorherigen Periode berechnet werden, geben Sie im Feld **Anfangsdatum für Korrektur** das Startdatum der Periode an, ab dem diese Kosten enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="077bf-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="077bf-117">Je nach der Detailebene, die im Budget erforderlich ist, legen Sie die entsprechenden Optionen in die fünf Inforegistern **Gruppieren nach** fest.</span><span class="sxs-lookup"><span data-stu-id="077bf-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="077bf-118">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="077bf-118">Select **OK**.</span></span>
8. <span data-ttu-id="077bf-119">Wählen Sie **Budgetpositionen** aus, um die Seite **Wartungsbudgetpositionen** zu öffnen, in der Sie alle Budgetpositionen anzeigen können, die für den Zeitraum erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="077bf-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="077bf-120">Um das Budget zu genehmigen, wählen Sie dieses auf der Seite **Wartungsbudgets** aus, und wählen Sie dann **Genehmigen** aus.</span><span class="sxs-lookup"><span data-stu-id="077bf-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="077bf-121">Im Dialogfeld **Budget genehmigen** wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="077bf-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="077bf-122">Ihr Name wird im Feld **Genehmigt von** auf der Seite **Wartungsbudgets** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="077bf-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="077bf-123">Nachdem Sie ein Wartungsbudget genehmigt haben, können Sie die zugehörigen Positionen der Seite **Wartungsbudgetpositionen** nicht neu berechnen oder anpassen, sofern Sie die Genehmigung nicht zunächst entfernen.</span><span class="sxs-lookup"><span data-stu-id="077bf-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="077bf-124">Um die Genehmigung eines Wartungsbudgets zu entfernen, wählen Sie dieses auf der Seite **Wartungsbudgets** aus, und wählen Sie dann **Genehmigen** aus.</span><span class="sxs-lookup"><span data-stu-id="077bf-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="077bf-125">Im Dialogfeld **Budget genehmigen** wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="077bf-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Wartungsbudgets](media/01-maintenance-budgets.png)

<span data-ttu-id="077bf-127">Sie können auch ein neues Wartungsbudget erstellen, indem Sie ein vorhandenes Budget kopieren.</span><span class="sxs-lookup"><span data-stu-id="077bf-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="077bf-128">Wählen Sie auf der Seite **Wartungsbudgets** das zu kopierende Budget aus, und wählen Sie dann **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="077bf-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="077bf-129">Dieser Ansatz ist hilfreich, wenn Sie z. B. ein Budget für einen Monat erstellt haben und dieses in andere Monate kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="077bf-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="077bf-130">Das Wartungsbudget berechnet nur Budgetkosten auf Grundlage der Wartungsplanpositionen.</span><span class="sxs-lookup"><span data-stu-id="077bf-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="077bf-131">Um Istkosten für die gleiche Periode zu berechnen, können Sie diese Berechnung auf der Seite **Kostensteuerung für Anlagen** vornehmen.</span><span class="sxs-lookup"><span data-stu-id="077bf-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
