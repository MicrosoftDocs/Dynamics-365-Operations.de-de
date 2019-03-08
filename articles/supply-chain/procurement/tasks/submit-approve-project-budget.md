---
title: Überarbeiten und Übermitteln eines Projektbudgets
description: Diese Prozedur zeigt Ihnen, wie Sie das Budget für ein Projekt erstellen und übermitteln.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f727e19d3f8c424b1c59e52602b7e907151f4492
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "328722"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="7c03c-103">Überarbeiten und Übermitteln eines Projektbudgets</span><span class="sxs-lookup"><span data-stu-id="7c03c-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c03c-104">Diese Prozedur zeigt Ihnen, wie Sie das Budget für ein Projekt erstellen und übermitteln.</span><span class="sxs-lookup"><span data-stu-id="7c03c-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="7c03c-105">Wenn Sie ein Projektbudget erstellen, können Sie die vorkalkulierten Umsatzerlöse und Kosten für ein Projekt eingegeben und diese anschließend zum Steuern der tatsächlichen Projektbuchungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c03c-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="7c03c-106">Bei der Projektbudgetierung müssen alle ursprünglichen Budgets und Überarbeitungen an den Projektworkflow zur Genehmigung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c03c-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="7c03c-107">Der Workflow ermöglicht eine bessere Steuerung des Prozesses, und der Änderungsverlauf wird aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7c03c-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="7c03c-108">Diese Aufgabe wurde mit dem USSI-Dataset erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c03c-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="7c03c-109">Wechseln Sie zu "Projektverwaltung und -verrechnung" > "Projekte" > "Alle Projekte".</span><span class="sxs-lookup"><span data-stu-id="7c03c-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="7c03c-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7c03c-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7c03c-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7c03c-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7c03c-112">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="7c03c-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="7c03c-113">Klicken Sie auf „Projektbudget”.</span><span class="sxs-lookup"><span data-stu-id="7c03c-113">Click Project budget.</span></span>
6. <span data-ttu-id="7c03c-114">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7c03c-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="7c03c-115">Den Abschnitt „Kosten” erweitern</span><span class="sxs-lookup"><span data-stu-id="7c03c-115">Expand the Cost section</span></span>
8. <span data-ttu-id="7c03c-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="7c03c-116">Click New.</span></span>
9. <span data-ttu-id="7c03c-117">Wählen Sie im Feld „Transaktionstyp” eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7c03c-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="7c03c-118">Geben Sie im Feld 'Kategorie' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7c03c-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="7c03c-119">Geben Sie im Feld „Ursprüngliches Budget” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7c03c-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="7c03c-120">Erweitern Sie den Abschnitt „Umsatzerlöse”.</span><span class="sxs-lookup"><span data-stu-id="7c03c-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="7c03c-121">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="7c03c-121">Click New.</span></span>
14. <span data-ttu-id="7c03c-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="7c03c-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="7c03c-123">Wählen Sie im Feld „Transaktionstyp” eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7c03c-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="7c03c-124">Geben Sie im Feld 'Kategorie' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7c03c-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="7c03c-125">Geben Sie im Feld „Ursprüngliches Budget” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7c03c-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="7c03c-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="7c03c-126">Click Save.</span></span>
19. <span data-ttu-id="7c03c-127">Klicken Sie auf „Workflow”.</span><span class="sxs-lookup"><span data-stu-id="7c03c-127">Click Workflow.</span></span>
20. <span data-ttu-id="7c03c-128">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="7c03c-128">Click Submit.</span></span>
21. <span data-ttu-id="7c03c-129">Geben Sie im Feld "Kommentar" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7c03c-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="7c03c-130">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="7c03c-130">Click Submit.</span></span>

