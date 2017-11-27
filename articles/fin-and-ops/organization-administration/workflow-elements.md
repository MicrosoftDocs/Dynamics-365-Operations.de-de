---
title: Workflowelemente
description: Dieses Thema beschreibt die verschiedenen Elemente, die einen Workflow darstellen.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 15cac09a97305c1b467cbb97da2d4b8a864ccbc7
ms.contentlocale: de-de
ms.lasthandoff: 11/14/2017

---

# <a name="workflow-elements"></a><span data-ttu-id="df5d6-103">Workflowelemente</span><span class="sxs-lookup"><span data-stu-id="df5d6-103">Workflow elements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="df5d6-104">Dieses Thema beschreibt die verschiedenen Elemente, die einen Workflow darstellen.</span><span class="sxs-lookup"><span data-stu-id="df5d6-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="df5d6-105">Ein Workflow besteht aus Elementen.</span><span class="sxs-lookup"><span data-stu-id="df5d6-105">A workflow consists of elements.</span></span> <span data-ttu-id="df5d6-106">In den folgenden Abschnitten wird jeder Elementtyp beschrieben.</span><span class="sxs-lookup"><span data-stu-id="df5d6-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="df5d6-107">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="df5d6-107">Tasks</span></span>
<span data-ttu-id="df5d6-108">Bei einer *Aufgabe* handelt es sich um eine auszuführende Arbeitseinheit.</span><span class="sxs-lookup"><span data-stu-id="df5d6-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="df5d6-109">Es können zwei Arten von Aufgaben zu einem Workflow hinzugefügt werden: manuelle Aufgaben und automatisierte Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="df5d6-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="df5d6-110">Manuelle Aufgabe</span><span class="sxs-lookup"><span data-stu-id="df5d6-110">Manual task</span></span>

<span data-ttu-id="df5d6-111">Bei einer *manuellen Aufgabe* handelt es sich um eine Arbeitseinheit, die von einem Benutzer auszuführen ist.</span><span class="sxs-lookup"><span data-stu-id="df5d6-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="df5d6-112">Beispielsweise beinhaltet ein Workflow für Spesenabrechnungen manuelle Aufgaben, die von den zugewiesenen Benutzern folgende Aktionen erfordern:</span><span class="sxs-lookup"><span data-stu-id="df5d6-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="df5d6-113">Prüfen der zusammen mit einer Spesenabrechnung eingereichten Belege.</span><span class="sxs-lookup"><span data-stu-id="df5d6-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="df5d6-114">Anrufen des Vorgesetzten eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="df5d6-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="df5d6-115">Automatisierte Aufgabe</span><span class="sxs-lookup"><span data-stu-id="df5d6-115">Automated task</span></span>

<span data-ttu-id="df5d6-116">Bei einer *automatisierten Aufgabe* handelt es sich um eine Arbeitseinheit, die vom System auszuführen ist.</span><span class="sxs-lookup"><span data-stu-id="df5d6-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="df5d6-117">Es sind keine manuellen Benutzeraktivitäten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="df5d6-117">No human interaction is required.</span></span> <span data-ttu-id="df5d6-118">Beispielsweise beinhaltet ein Workflow für Aufträge automatisierte Aufgaben, die vom System folgende Aktionen erfordern:</span><span class="sxs-lookup"><span data-stu-id="df5d6-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="df5d6-119">Ausführen einer Kreditprüfung.</span><span class="sxs-lookup"><span data-stu-id="df5d6-119">Perform a credit check.</span></span>
-   <span data-ttu-id="df5d6-120">Erstellen eines Debitorendatensatzes für den Debitor, sofern noch nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="df5d6-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="df5d6-121">Genehmigungsprozesse</span><span class="sxs-lookup"><span data-stu-id="df5d6-121">Approval processes</span></span>
<span data-ttu-id="df5d6-122">Bei einem *Genehmigungsprozess* handelt es sich um einen Prozess, der aus getrennten Schritten besteht.</span><span class="sxs-lookup"><span data-stu-id="df5d6-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="df5d6-123">Bei jedem Genehmigungsschritt kann der Benutzer die folgenden Aktivitäten ausführen:</span><span class="sxs-lookup"><span data-stu-id="df5d6-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="df5d6-124">Dient zum Genehmigen des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="df5d6-124">Approve the document.</span></span>
-   <span data-ttu-id="df5d6-125">Dient zum Ablehnen des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="df5d6-125">Reject the document.</span></span>
-   <span data-ttu-id="df5d6-126">eine Änderung am Dokument anzufordern,</span><span class="sxs-lookup"><span data-stu-id="df5d6-126">Request a change to the document.</span></span>
-   <span data-ttu-id="df5d6-127">Dokument einem anderen Benutzer zur Genehmigung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="df5d6-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="df5d6-128">Elemente von Positionsworkflows</span><span class="sxs-lookup"><span data-stu-id="df5d6-128">Line-item workflow elements</span></span>
<span data-ttu-id="df5d6-129">Ein Workflow kann zum Verarbeiten von Dokumenten oder der Positionen in einem Dokument erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="df5d6-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="df5d6-130">Angenommen, Sie haben einen Genehmigungsworkflow für Arbeitszeitnachweise erstellt.</span><span class="sxs-lookup"><span data-stu-id="df5d6-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="df5d6-131">(Wir bezeichnen diesen Workflow als *Dokumentworkflow*.) Sie können ein *Positionsworkflow*-Element zu diesem Dokumentworkflow hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="df5d6-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="df5d6-132">Bei der Ausführung des Positionselements wird jede Position im Dokument zur Verarbeitung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="df5d6-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="df5d6-133">Dabei können alle Positionen durch denselben Positionsworkflow oder jede Position durch einen anderen Positionsworkflow verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="df5d6-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="df5d6-134">Angenommen, ein Mitarbeiter hat einen Arbeitszeitnachweis übermittelt, der der folgenden Abbildung ähnelt.</span><span class="sxs-lookup"><span data-stu-id="df5d6-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Workflow mit Positionen](./media/workflow_lineitemworkflow.gif) 

<span data-ttu-id="df5d6-136">In diesem Szenario möchten Sie vielleicht die folgenden Positionsworkflows erstellen:</span><span class="sxs-lookup"><span data-stu-id="df5d6-136">In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="df5d6-137">**Positionsworkflow 1** – Dieser Workflow wird zum Verarbeiten von Positionen mit Projektkennung 1111 verwendet.</span><span class="sxs-lookup"><span data-stu-id="df5d6-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="df5d6-138">**Positionsworkflow 2** – Dieser Workflow wird zum Verarbeiten von Positionen mit Projektkennung 2222 verwendet.</span><span class="sxs-lookup"><span data-stu-id="df5d6-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="df5d6-139">**Positionsworkflow 3** – Dieser Workflow wird zum Verarbeiten von Positionen mit Projektkennung 3333 verwendet.</span><span class="sxs-lookup"><span data-stu-id="df5d6-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="df5d6-140">Flusssteuerelemente</span><span class="sxs-lookup"><span data-stu-id="df5d6-140">Flow-control elements</span></span>
<span data-ttu-id="df5d6-141">Mithilfe der folgenden Elemente können Sie Workflows mit alternativen Verzweigungen oder gleichzeitig ausgeführten Verzweigungen entwerfen.</span><span class="sxs-lookup"><span data-stu-id="df5d6-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="df5d6-142">Manuelle Entscheidung</span><span class="sxs-lookup"><span data-stu-id="df5d6-142">Manual decision</span></span>

<span data-ttu-id="df5d6-143">Eine *manuelle Entscheidung* ist ein Punkt, an dem sich ein Workflow verzweigt.</span><span class="sxs-lookup"><span data-stu-id="df5d6-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="df5d6-144">Ein Benutzer muss eine Entscheidung treffen, und diese Entscheidung bestimmt, welche Verzweigung zum Verarbeiten des übermittelten Dokuments verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df5d6-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="df5d6-145">Bedingte Entscheidung</span><span class="sxs-lookup"><span data-stu-id="df5d6-145">Conditional decision</span></span>

<span data-ttu-id="df5d6-146">Eine *bedingte Entscheidung* ist ein Punkt, an dem sich ein Workflow verzweigt.</span><span class="sxs-lookup"><span data-stu-id="df5d6-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="df5d6-147">Das System entscheidet jedoch, welcher Zweig zum Verarbeiten des übermittelten Dokuments verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df5d6-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="df5d6-148">Um diese Entscheidung zu treffen, wertet das System das Dokument aus, um zu bestimmen, ob es den angegebenen Bedingungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="df5d6-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="df5d6-149">Parallele Aktivität</span><span class="sxs-lookup"><span data-stu-id="df5d6-149">Parallel activity</span></span>

<span data-ttu-id="df5d6-150">Eine *parallele Aktivität* ist ein Workflowelement, das zwei oder mehr Workflowverzweigungen enthält, die gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="df5d6-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="df5d6-151">Untergeordneter Workflow</span><span class="sxs-lookup"><span data-stu-id="df5d6-151">Subworkflow</span></span>

<span data-ttu-id="df5d6-152">Ein *untergeordneter Workflow* ist ein Workflow, der im Kontext eines anderen Workflows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df5d6-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




