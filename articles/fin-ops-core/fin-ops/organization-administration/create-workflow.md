---
title: Erstellen von Workflows – Übersicht
description: Dieses Thema erläutert, wie Sie einen Workflow erstellen.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: bcd548bf8e03e0e6df4d413afe8c9ae01c570899
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698017"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="b3fb4-103">Erstellen von Workflows – Übersicht</span><span class="sxs-lookup"><span data-stu-id="b3fb4-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3fb4-104">Dieses Thema erläutert, wie Sie einen Workflow erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="b3fb4-105">Öffnen des Workflow-Editors</span><span class="sxs-lookup"><span data-stu-id="b3fb4-105">Open the workflow editor</span></span>

<span data-ttu-id="b3fb4-106">Das Modul, in dem Sie arbeiten, bestimmt die Workflowtypen, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="b3fb4-107">Gehen Sie folgendermaßen vor, um den Workflowtyp zum Erstellen und Öffnen des Workflow-Editors auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="b3fb4-108">Öffnen Sie das Modul, für das Sie einen neuen Workflow erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="b3fb4-109">Sie können beispielsweise einen Workflow für Bestellanforderungen erstellen. Klicken Sie dazu auf **Beschaffung**.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="b3fb4-110">Klicken Sie auf **Einrichten** &gt; **\[Modulname\] Workflows**.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="b3fb4-111">Klicken Sie auf der Listenseite im Aktivitätsbereich auf der Registerkarte auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="b3fb4-112">Wählen Sie auf der Seite **Workflow erstellen** den Typ des Workflows aus, den Sie erstellen möchten und klicken Sie dann **Workflow erstellen**.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="b3fb4-113">Der Workflow-Editor wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-113">The workflow editor appears.</span></span> <span data-ttu-id="b3fb4-114">Verwenden Sie jetzt die folgenden Verfahren zum Entwerfen des Workflows.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="b3fb4-115">Ziehen von Workflowelementen auf die Canvas</span><span class="sxs-lookup"><span data-stu-id="b3fb4-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="b3fb4-116">Der Bereich **Workflow-Elemente** des Workflow-Editors enthält die Elemente, die Sie dem Workflow hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="b3fb4-117">Um dem Workflow Elemente hinzuzufügen, ziehen Sie die Elemente aus dem Bereich auf die Canvas.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="b3fb4-118">Verbinden der Elemente</span><span class="sxs-lookup"><span data-stu-id="b3fb4-118">Connect the elements</span></span>

<span data-ttu-id="b3fb4-119">Wenn Sie ein Workflowelement mit einem anderen verbinden möchten, halten Sie den Zeiger über ein Element, bis Verbindungspunkte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="b3fb4-120">Klicken Sie auf einen Verbindungspunkt, und ziehen Sie ihn zum anderen Element.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="b3fb4-121">Stellen Sie sicher, dass Sie alle Elemente verbinden.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="b3fb4-122">Konfigurieren der Eigenschaften des Workflows</span><span class="sxs-lookup"><span data-stu-id="b3fb4-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="b3fb4-123">Gehen Sie folgendermaßen vor, um die Eigenschaften des Workflows zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="b3fb4-124">Klicken Sie auf die Canvas, um sicherzustellen, dass kein Workflowelement ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="b3fb4-125">Klicken Sie auf **Eigenschaften** **, um die Seite** Eigenschaften für den Workflow zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="b3fb4-126">Folgen Sie den Schritten des Verfahrens unter [Konfigurieren von Workfloweigenschaften](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="b3fb4-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="b3fb4-127">Konfigurieren der Elemente des Workflows</span><span class="sxs-lookup"><span data-stu-id="b3fb4-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="b3fb4-128">Konfigurieren Sie jedes auf die Canvas gezogene Element.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="b3fb4-129">Informationen zum Konfigurieren jedes Workflowelements finden Sie unter folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b3fb4-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="b3fb4-130">Manuelle Aufgaben in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b3fb4-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="b3fb4-131">Konfigurieren von automatisierten Aufgaben in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="b3fb4-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="b3fb4-132">Genehmigungsprozesse in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b3fb4-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="b3fb4-133">Genehmigungsschritte in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b3fb4-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="b3fb4-134">Manuellen Entscheidungen in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b3fb4-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="b3fb4-135">Konfigurieren von bedingten Entscheidungen in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="b3fb4-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="b3fb4-136">Konfigurieren paralleler Verzweigungen in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="b3fb4-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="b3fb4-137">Konfigurieren eines Parallelzweigs</span><span class="sxs-lookup"><span data-stu-id="b3fb4-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="b3fb4-138">Konfigurieren von Positionsworkflows</span><span class="sxs-lookup"><span data-stu-id="b3fb4-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="b3fb4-139">Beheben von Fehlern oder Warnungen</span><span class="sxs-lookup"><span data-stu-id="b3fb4-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="b3fb4-140">Im Bereich **Fehler und Warnungen** im unteren Bereich des Workflow-Editors werden für den Workflow generierte Meldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="b3fb4-141">Doppelklicken Sie auf die Fehler- oder Warnmeldung, um das Element zu suchen, in dem ein Fehler oder eine Warnung auftritt.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="b3fb4-142">Bevor der Workflow aktiviert werden kann, müssen alle Fehler und Warnungen behoben sein.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="b3fb4-143">Speichern und Aktivieren des Workflows</span><span class="sxs-lookup"><span data-stu-id="b3fb4-143">Save and activate the workflow</span></span>

<span data-ttu-id="b3fb4-144">Führen Sie zum Speichern und Aktivieren des Workflows die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="b3fb4-145">Klicken Sie auf **Speichern und schließen**, um den Workflow-Editor zu schließen und die Seite **Workflow speichern** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="b3fb4-146">Geben Sie Kommentare zu den Änderungen am Workflow ein und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="b3fb4-147">Wenn alle Fehler und Warnungen behoben wurden, wird die Seite **Workflow aktivieren** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="b3fb4-148">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="b3fb4-148">Select one of the following options:</span></span>

    - <span data-ttu-id="b3fb4-149">Klicken Sie zum Aktivieren dieser Version des Workflows auf **Neue Version aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="b3fb4-150">Wenn ein Workflow aktiv ist, können Benutzer Dokumente zwecks Verarbeitung übermitteln.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="b3fb4-151">Wenn diese Version nicht aktiviert werden soll, klicken Sie **Neue Version nicht aktivieren** an.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="b3fb4-152">Der Workflow kann auch später aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b3fb4-152">You can activate the workflow later.</span></span>
