---
title: Überarbeiten und Übermitteln eines Projektbudgets
description: Diese Prozedur zeigt Ihnen, wie Sie das Budget für ein Projekt erstellen und übermitteln.
author: mkirknel
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14683554c45db72061ecbbf4a528656df3132692
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428516"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="e8f33-103">Überarbeiten und Übermitteln eines Projektbudgets</span><span class="sxs-lookup"><span data-stu-id="e8f33-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8f33-104">Diese Prozedur zeigt Ihnen, wie Sie das Budget für ein Projekt erstellen und übermitteln.</span><span class="sxs-lookup"><span data-stu-id="e8f33-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="e8f33-105">Wenn Sie ein Projektbudget erstellen, können Sie die vorkalkulierten Umsatzerlöse und Kosten für ein Projekt eingegeben und diese anschließend zum Steuern der tatsächlichen Projektbuchungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8f33-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="e8f33-106">Bei der Projektbudgetierung müssen alle ursprünglichen Budgets und Überarbeitungen an den Projektworkflow zur Genehmigung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8f33-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="e8f33-107">Der Workflow ermöglicht eine bessere Steuerung des Prozesses, und der Änderungsverlauf wird aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e8f33-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="e8f33-108">Diese Aufgabe wurde mit dem USSI-Dataset erstellt.</span><span class="sxs-lookup"><span data-stu-id="e8f33-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="e8f33-109">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Projektmanagement und Rechnungswesen > Projekte > Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="e8f33-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e8f33-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e8f33-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e8f33-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e8f33-112">Klicken Sie im **Aktivitätsbereich** auf **Plan**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="e8f33-113">Klicken Sie auf **Projektbudget**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="e8f33-114">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e8f33-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="e8f33-115">Erweitern Sie die **Kosten** FastTab.</span><span class="sxs-lookup"><span data-stu-id="e8f33-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="e8f33-116">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-116">Click **New**.</span></span>
9. <span data-ttu-id="e8f33-117">Wählen Sie im Feld **Transaktionsart** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="e8f33-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="e8f33-118">Geben Sie im Feld **Kategorie** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8f33-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="e8f33-119">Geben Sie im Feld **Originalbudget** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="e8f33-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="e8f33-120">Erweitern Sie die **Erlöse** fastTab.</span><span class="sxs-lookup"><span data-stu-id="e8f33-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="e8f33-121">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-121">Click **New**.</span></span>
14. <span data-ttu-id="e8f33-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="e8f33-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="e8f33-123">Wählen Sie im Feld **Transaktionsart** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="e8f33-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="e8f33-124">Geben Sie im Feld **Kategorie** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8f33-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="e8f33-125">Geben Sie im Feld **Originalbudget** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="e8f33-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="e8f33-126">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-126">Click **Save**.</span></span>
19. <span data-ttu-id="e8f33-127">Klicken Sie auf **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="e8f33-128">Klicken Sie auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-128">Click **Submit**.</span></span>
21. <span data-ttu-id="e8f33-129">Geben Sie in das Feld **Kommentar** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e8f33-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="e8f33-130">Klicken Sie auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="e8f33-130">Click **Submit**.</span></span>

