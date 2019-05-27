---
title: Workflowsystem
description: In diesem Thema wird das Workflowsystem in Microsoft Dynamics 365 for Finance and Operations beschrieben.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545808"
---
# <a name="workflow-system"></a><span data-ttu-id="79595-103">Workflowsystem</span><span class="sxs-lookup"><span data-stu-id="79595-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79595-104">In diesem Thema wird das Workflowsystem in Microsoft Dynamics 365 for Finance and Operations beschrieben.</span><span class="sxs-lookup"><span data-stu-id="79595-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="79595-105">Was ist ein Arbeitsplan?</span><span class="sxs-lookup"><span data-stu-id="79595-105">What is workflow?</span></span>

<span data-ttu-id="79595-106">Der Begriff *Workflow* kann auf zwei Arten definiert werden: als System und als Geschäftsprozess.</span><span class="sxs-lookup"><span data-stu-id="79595-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="79595-107">Workflow als System</span><span class="sxs-lookup"><span data-stu-id="79595-107">Workflow is a system</span></span>

<span data-ttu-id="79595-108">Workflow ist ein System, das mit Finance and Operations installiert wird und auf dem Anwendungsobjektserver (AOS/Application Object Server) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79595-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="79595-109">Das Workflowsystem verfügt über Funktionen, die zum Erstellen einzelner Workflows oder Geschäftsprozesse verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="79595-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="79595-110">Workflow als Geschäftsprozess</span><span class="sxs-lookup"><span data-stu-id="79595-110">Workflow is a business process</span></span>

<span data-ttu-id="79595-111">Ein Workflow stellt einen Geschäftsprozess dar.</span><span class="sxs-lookup"><span data-stu-id="79595-111">A workflow represents a business process.</span></span> <span data-ttu-id="79595-112">Ein Workflow definiert, wie ein Dokument das System durchläuft, indem angezeigt wird, wer eine Aufgabe abschließen, eine Entscheidung treffen oder ein Dokument genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="79595-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="79595-113">Die folgende Abbildung zeigt z. B. einen Workflow für Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="79595-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Workflow mit Elementen, die Benutzern zugewiesen sind](./media/workflow_user.gif)

<span data-ttu-id="79595-115">Beispiel zum besseren Verständnis dieses Workflows: Steffen reicht eine Spesenabrechnung in Höhe von 7.000 Euro ein.</span><span class="sxs-lookup"><span data-stu-id="79595-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="79595-116">In diesem Szenario muss Joachim die Belege prüfen, die Steffen an ihn weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="79595-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="79595-117">Anschließend muss die Spesenabrechnung von Frank und Saskia genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="79595-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="79595-118">Nehmen wir nun an, Steffen reicht eine Spesenabrechnung in Höhe von 11.000 Euro ein.</span><span class="sxs-lookup"><span data-stu-id="79595-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="79595-119">In diesem Szenario muss Joachim die Belege prüfen, und Frank, Saskia und Anne müssen die Spesenabrechnung genehmigen.</span><span class="sxs-lookup"><span data-stu-id="79595-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="79595-120">Vorteile des Workflowsystems</span><span class="sxs-lookup"><span data-stu-id="79595-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="79595-121">Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="79595-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="79595-122">**Konsistente Prozesse** – Sie können die Verarbeitung bestimmter Dokumente definieren, z. B. von Bestellanforderungen und Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="79595-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="79595-123">Das Workflowsystem gewährleistet, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="79595-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="79595-124">**Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen von Workflowinstanzen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="79595-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="79595-125">So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="79595-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="79595-126">**Zentralisierte Arbeitsliste** – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="79595-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="79595-127">Workflowinhalt</span><span class="sxs-lookup"><span data-stu-id="79595-127">Workflow content</span></span>

+ [<span data-ttu-id="79595-128">Workflowarchitektur</span><span class="sxs-lookup"><span data-stu-id="79595-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="79595-129">Workflowelemente</span><span class="sxs-lookup"><span data-stu-id="79595-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="79595-130">Workflowaktivitäten</span><span class="sxs-lookup"><span data-stu-id="79595-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="79595-131">Erstellen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="79595-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="79595-132">Konfigurieren von Workfloweigenschaften</span><span class="sxs-lookup"><span data-stu-id="79595-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="79595-133">Konfigurieren einer manuellen Entscheidung in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="79595-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="79595-134">Konfigurieren einer automatisierten Aufgabe in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="79595-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="79595-135">Einen Genehmigungsschritt in einem Workflow konfirgurieren</span><span class="sxs-lookup"><span data-stu-id="79595-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="79595-136">Einen Genehmigungsschritt in einem Workflow genehmigen</span><span class="sxs-lookup"><span data-stu-id="79595-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="79595-137">Konfigurieren einer manuellen Entscheidung in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="79595-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="79595-138">Konfigurieren einer bedingten Entscheidung in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="79595-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="79595-139">Konfigurieren einer parallelen Aktivität in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="79595-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="79595-140">Konfigurieren eines Parallelzweigs in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="79595-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="79595-141">Konfigurieren eines Positionsworkflows</span><span class="sxs-lookup"><span data-stu-id="79595-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="79595-142">Workflow-FAQs</span><span class="sxs-lookup"><span data-stu-id="79595-142">Workflow FAQ</span></span>](workflow-FAQ.md)
