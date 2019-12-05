---
title: Erstellen von Workflows – Übersicht
description: Dieses Thema erläutert, wie Sie einen Workflow erstellen.
author: sericks007
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
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a643be553f3fcdfbe53f2024982a596e498830a8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811289"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="964d9-103">Erstellen von Workflows – Übersicht</span><span class="sxs-lookup"><span data-stu-id="964d9-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="964d9-104">Dieses Thema erläutert, wie Sie einen Workflow erstellen.</span><span class="sxs-lookup"><span data-stu-id="964d9-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="964d9-105">Öffnen des Workflow-Editors</span><span class="sxs-lookup"><span data-stu-id="964d9-105">Open the workflow editor</span></span>

<span data-ttu-id="964d9-106">Das Modul, in dem Sie arbeiten, bestimmt die Workflowtypen, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="964d9-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="964d9-107">Gehen Sie folgendermaßen vor, um den Workflowtyp zum Erstellen und Öffnen des Workflow-Editors auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="964d9-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="964d9-108">Öffnen Sie das Modul, für das Sie einen neuen Workflow erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="964d9-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="964d9-109">Sie können beispielsweise einen Workflow für Bestellanforderungen erstellen. Klicken Sie dazu auf **Beschaffung**.</span><span class="sxs-lookup"><span data-stu-id="964d9-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="964d9-110">Klicken Sie auf **Einrichten** &gt; **\[Modulname\] Workflows**.</span><span class="sxs-lookup"><span data-stu-id="964d9-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="964d9-111">Klicken Sie auf der Listenseite im Aktivitätsbereich auf der Registerkarte auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="964d9-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="964d9-112">Wählen Sie auf der Seite **Workflow erstellen** den Typ des Workflows aus, den Sie erstellen möchten und klicken Sie dann **Workflow erstellen**.</span><span class="sxs-lookup"><span data-stu-id="964d9-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="964d9-113">Der Workflow-Editor wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="964d9-113">The workflow editor appears.</span></span> <span data-ttu-id="964d9-114">Verwenden Sie jetzt die folgenden Verfahren zum Entwerfen des Workflows.</span><span class="sxs-lookup"><span data-stu-id="964d9-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="964d9-115">Ziehen von Workflowelementen auf die Canvas</span><span class="sxs-lookup"><span data-stu-id="964d9-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="964d9-116">Der Bereich **Workflow-Elemente** des Workflow-Editors enthält die Elemente, die Sie dem Workflow hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="964d9-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="964d9-117">Um dem Workflow Elemente hinzuzufügen, ziehen Sie die Elemente aus dem Bereich auf die Canvas.</span><span class="sxs-lookup"><span data-stu-id="964d9-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="964d9-118">Verbinden der Elemente</span><span class="sxs-lookup"><span data-stu-id="964d9-118">Connect the elements</span></span>

<span data-ttu-id="964d9-119">Wenn Sie ein Workflowelement mit einem anderen verbinden möchten, halten Sie den Zeiger über ein Element, bis Verbindungspunkte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="964d9-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="964d9-120">Klicken Sie auf einen Verbindungspunkt, und ziehen Sie ihn zum anderen Element.</span><span class="sxs-lookup"><span data-stu-id="964d9-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="964d9-121">Stellen Sie sicher, dass Sie alle Elemente verbinden.</span><span class="sxs-lookup"><span data-stu-id="964d9-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="964d9-122">Konfigurieren der Eigenschaften des Workflows</span><span class="sxs-lookup"><span data-stu-id="964d9-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="964d9-123">Gehen Sie folgendermaßen vor, um die Eigenschaften des Workflows zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="964d9-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="964d9-124">Klicken Sie auf die Canvas, um sicherzustellen, dass kein Workflowelement ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="964d9-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="964d9-125">Klicken Sie auf **Eigenschaften** **, um die Seite** Eigenschaften für den Workflow zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="964d9-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="964d9-126">Folgen Sie den Schritten des Verfahrens unter [Konfigurieren von Workfloweigenschaften](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="964d9-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="964d9-127">Konfigurieren der Elemente des Workflows</span><span class="sxs-lookup"><span data-stu-id="964d9-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="964d9-128">Konfigurieren Sie jedes auf die Canvas gezogene Element.</span><span class="sxs-lookup"><span data-stu-id="964d9-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="964d9-129">Informationen zum Konfigurieren jedes Workflowelements finden Sie unter folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="964d9-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="964d9-130">Manuelle Aufgaben in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="964d9-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="964d9-131">Konfigurieren von automatisierten Aufgaben in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="964d9-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="964d9-132">Genehmigungsprozesse in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="964d9-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="964d9-133">Genehmigungsschritte in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="964d9-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="964d9-134">Manuellen Entscheidungen in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="964d9-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="964d9-135">Konfigurieren von bedingten Entscheidungen in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="964d9-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="964d9-136">Konfigurieren paralleler Verzweigungen in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="964d9-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="964d9-137">Konfigurieren eines Parallelzweigs</span><span class="sxs-lookup"><span data-stu-id="964d9-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="964d9-138">Konfigurieren von Positionsworkflows</span><span class="sxs-lookup"><span data-stu-id="964d9-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="964d9-139">Beheben von Fehlern oder Warnungen</span><span class="sxs-lookup"><span data-stu-id="964d9-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="964d9-140">Im Bereich **Fehler und Warnungen** im unteren Bereich des Workflow-Editors werden für den Workflow generierte Meldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="964d9-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="964d9-141">Doppelklicken Sie auf die Fehler- oder Warnmeldung, um das Element zu suchen, in dem ein Fehler oder eine Warnung auftritt.</span><span class="sxs-lookup"><span data-stu-id="964d9-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="964d9-142">Bevor der Workflow aktiviert werden kann, müssen alle Fehler und Warnungen behoben sein.</span><span class="sxs-lookup"><span data-stu-id="964d9-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="964d9-143">Speichern und Aktivieren des Workflows</span><span class="sxs-lookup"><span data-stu-id="964d9-143">Save and activate the workflow</span></span>

<span data-ttu-id="964d9-144">Führen Sie zum Speichern und Aktivieren des Workflows die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="964d9-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="964d9-145">Klicken Sie auf **Speichern und schließen**, um den Workflow-Editor zu schließen und die Seite **Workflow speichern** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="964d9-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="964d9-146">Geben Sie Kommentare zu den Änderungen am Workflow ein und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="964d9-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="964d9-147">Wenn alle Fehler und Warnungen behoben wurden, wird die Seite **Workflow aktivieren** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="964d9-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="964d9-148">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="964d9-148">Select one of the following options:</span></span>

    - <span data-ttu-id="964d9-149">Klicken Sie zum Aktivieren dieser Version des Workflows auf **Neue Version aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="964d9-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="964d9-150">Wenn ein Workflow aktiv ist, können Benutzer Dokumente zwecks Verarbeitung übermitteln.</span><span class="sxs-lookup"><span data-stu-id="964d9-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="964d9-151">Wenn diese Version nicht aktiviert werden soll, klicken Sie **Neue Version nicht aktivieren** an.</span><span class="sxs-lookup"><span data-stu-id="964d9-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="964d9-152">Der Workflow kann auch später aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="964d9-152">You can activate the workflow later.</span></span>
