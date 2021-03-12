---
title: Workflowsystem – Übersicht
description: In diesem Thema wird das Workflowsystem beschrieben.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660e01618eea66bc611dd51818694d36993ba9ea
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796995"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="8760f-103">Workflowsystem – Übersicht</span><span class="sxs-lookup"><span data-stu-id="8760f-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8760f-104">In diesem Thema wird das Workflowsystem beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8760f-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="8760f-105">Was ist ein Arbeitsplan?</span><span class="sxs-lookup"><span data-stu-id="8760f-105">What is workflow?</span></span>

<span data-ttu-id="8760f-106">Der Begriff *Workflow* kann auf zwei Arten definiert werden: als System und als Geschäftsprozess.</span><span class="sxs-lookup"><span data-stu-id="8760f-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="8760f-107">Workflow als System</span><span class="sxs-lookup"><span data-stu-id="8760f-107">Workflow is a system</span></span>

<span data-ttu-id="8760f-108">Der Workflow ist ein System, das auf dem Anwendungsobjektserver (AOS) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8760f-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="8760f-109">Das Workflowsystem verfügt über Funktionen, die zum Erstellen einzelner Workflows oder Geschäftsprozesse verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8760f-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="8760f-110">Workflow als Geschäftsprozess</span><span class="sxs-lookup"><span data-stu-id="8760f-110">Workflow is a business process</span></span>

<span data-ttu-id="8760f-111">Ein Workflow stellt einen Geschäftsprozess dar.</span><span class="sxs-lookup"><span data-stu-id="8760f-111">A workflow represents a business process.</span></span> <span data-ttu-id="8760f-112">Ein Workflow definiert, wie ein Dokument das System durchläuft, indem angezeigt wird, wer eine Aufgabe abschließen, eine Entscheidung treffen oder ein Dokument genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="8760f-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="8760f-113">Die folgende Abbildung zeigt z. B. einen Workflow für Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="8760f-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Workflow mit Elementen, die Benutzern zugewiesen sind](./media/workflow_user.gif)

<span data-ttu-id="8760f-115">Beispiel zum besseren Verständnis dieses Workflows: Steffen reicht eine Spesenabrechnung in Höhe von 7.000 Euro ein.</span><span class="sxs-lookup"><span data-stu-id="8760f-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="8760f-116">In diesem Szenario muss Joachim die Belege prüfen, die Steffen an ihn weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="8760f-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="8760f-117">Anschließend muss die Spesenabrechnung von Frank und Saskia genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="8760f-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="8760f-118">Nehmen wir nun an, Steffen reicht eine Spesenabrechnung in Höhe von 11.000 Euro ein.</span><span class="sxs-lookup"><span data-stu-id="8760f-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="8760f-119">In diesem Szenario muss Joachim die Belege prüfen, und Frank, Saskia und Anne müssen die Spesenabrechnung genehmigen.</span><span class="sxs-lookup"><span data-stu-id="8760f-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="8760f-120">Vorteile des Workflowsystems</span><span class="sxs-lookup"><span data-stu-id="8760f-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="8760f-121">Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="8760f-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="8760f-122">**Konsistente Prozesse** – Sie können die Verarbeitung bestimmter Dokumente definieren, z. B. von Bestellanforderungen und Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="8760f-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="8760f-123">Das Workflowsystem gewährleistet, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="8760f-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="8760f-124">**Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen von Workflowinstanzen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="8760f-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="8760f-125">So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="8760f-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="8760f-126">**Zentralisierte Arbeitsliste** – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8760f-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="8760f-127">Workflowinhalt</span><span class="sxs-lookup"><span data-stu-id="8760f-127">Workflow content</span></span>

+ [<span data-ttu-id="8760f-128">Workflow-Systemarchitektur</span><span class="sxs-lookup"><span data-stu-id="8760f-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="8760f-129">Workflow-Elemente</span><span class="sxs-lookup"><span data-stu-id="8760f-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="8760f-130">Aktivitäten in Workflow-Genehmigungsprozessen</span><span class="sxs-lookup"><span data-stu-id="8760f-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="8760f-131">Erstellen von Workflows – Übersicht</span><span class="sxs-lookup"><span data-stu-id="8760f-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="8760f-132">Konfigurieren von Workflow-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8760f-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="8760f-133">Manuelle Aufgaben in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="8760f-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="8760f-134">Konfigurieren von automatisierten Aufgaben in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="8760f-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="8760f-135">Genehmigungsprozesse in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="8760f-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="8760f-136">Genehmigungsschritte in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="8760f-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="8760f-137">Manuellen Entscheidungen in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="8760f-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="8760f-138">Konfigurieren von bedingten Entscheidungen in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="8760f-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="8760f-139">Konfigurieren paralleler Aktivitäten in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="8760f-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="8760f-140">Konfigurieren paralleler Verzweigungen in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="8760f-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="8760f-141">Konfigurieren von Positionsworkflows</span><span class="sxs-lookup"><span data-stu-id="8760f-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="8760f-142">Workflow-FAQs</span><span class="sxs-lookup"><span data-stu-id="8760f-142">Workflow FAQ</span></span>](workflow-FAQ.md)
