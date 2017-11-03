---
title: Beschaffungsworkflows
description: "Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat. Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3bf244786e308ebcaee27a16fae378f41086f963
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="20449-104">Beschaffungsworkflows</span><span class="sxs-lookup"><span data-stu-id="20449-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="20449-105">Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="20449-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="20449-106">Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen.</span><span class="sxs-lookup"><span data-stu-id="20449-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="20449-107">Ein Workflow stellt einen Geschäftsprozess dar.</span><span class="sxs-lookup"><span data-stu-id="20449-107">A workflow represents a business process.</span></span> <span data-ttu-id="20449-108">Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="20449-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="20449-109">Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="20449-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="20449-110">**Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="20449-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="20449-111">Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="20449-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="20449-112">**Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="20449-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="20449-113">So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="20449-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="20449-114">**Zentralisierte Arbeitsliste**- Benutzer können eine zentralisierte Arbeitsliste öffnen, um die Workflowaufgaben und ‑genehmigungen anzuzeigen, die ihnen zu allen Workflows zugewiesen werden, an denen sie teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="20449-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="20449-115">Dies ist in der Arbeitsaufgabenseite verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20449-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="20449-116"> Erstellbare Workflowtypen</span><span class="sxs-lookup"><span data-stu-id="20449-116">The types of workflows that you can create</span></span>
<span data-ttu-id="20449-117">Die folgenden Workflowtypen stehen für die Beschaffung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="20449-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="20449-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="20449-118">**Type**</span></span>                         | <span data-ttu-id="20449-119">**Mit diesem Typ können Sie folgende Aufgaben ausführen:**</span><span class="sxs-lookup"><span data-stu-id="20449-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="20449-120">Prüfung der Bestellanforderungen</span><span class="sxs-lookup"><span data-stu-id="20449-120">Purchase requisition review</span></span>      | <span data-ttu-id="20449-121">Erstellen Sie Prüfungsworkflows für Bestellanforderungen.</span><span class="sxs-lookup"><span data-stu-id="20449-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="20449-122">Prüfung der Bestellanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="20449-122">Purchase requisition line review</span></span> | <span data-ttu-id="20449-123">Erstellen Sie Prüfungsworkflows für Bestellanforderungspositionen.</span><span class="sxs-lookup"><span data-stu-id="20449-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="20449-124">Bestellworkflow</span><span class="sxs-lookup"><span data-stu-id="20449-124">Purchase order workflow</span></span>          | <span data-ttu-id="20449-125">Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellungen.</span><span class="sxs-lookup"><span data-stu-id="20449-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="20449-126">Bestellpositionsworkflow</span><span class="sxs-lookup"><span data-stu-id="20449-126">Purchase order line workflow</span></span>     | <span data-ttu-id="20449-127">Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellpositionen.</span><span class="sxs-lookup"><span data-stu-id="20449-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="20449-128">Erstellen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="20449-128">Creating a workflow</span></span>
<span data-ttu-id="20449-129">Um einen Workflow zu erstellen, wechseln Sie zu Beschaffung &gt; Einrichtung &gt; Beschaffungsworkflows und erstellen Sie einen neuen Workflow, indem sie den Workflowtyp auswählen, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="20449-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="20449-130">Auf der Workflowarbeitsfläche können Sie Workflowelemente in den Designer ziehen und die Elemente in einen Fluss verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="20449-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="20449-131">Die Workflowelemente sollten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="20449-131">The workflow elements should be configured.</span></span> <span data-ttu-id="20449-132">Für Genehmigungs- und Aufgabenworkflowelemente können Sie konfigurieren, welcher Teilnehmer Aktivitäten ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="20449-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="20449-133">Teilnehmertypen</span><span class="sxs-lookup"><span data-stu-id="20449-133">Types of participants</span></span>
----------------------

<span data-ttu-id="20449-134">Sie können folgenden Teilnehmergruppen einen Genehmigungsschritt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="20449-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="20449-135">Benutzergruppe</span><span class="sxs-lookup"><span data-stu-id="20449-135">User group</span></span>    | <span data-ttu-id="20449-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20449-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="20449-137">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="20449-137">Participant</span></span>   | <span data-ttu-id="20449-138">Weisen Sie den Genehmigungsschritt den Mitgliedern einer Gruppe oder Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="20449-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="20449-139">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="20449-139">Hierarchy</span></span>     | <span data-ttu-id="20449-140">Weisen Sie den Genehmigungsschritt den Benutzern in einer bestimmten Organisationshierarchie zu.</span><span class="sxs-lookup"><span data-stu-id="20449-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="20449-141">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="20449-141">Workflow user</span></span> | <span data-ttu-id="20449-142">Weisen Sie den Genehmigungsschritt den Benutzern dieses Workflows zu.</span><span class="sxs-lookup"><span data-stu-id="20449-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="20449-143">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="20449-143">Queue</span></span>         | <span data-ttu-id="20449-144">Weisen Sie den Genehmigungsschritt einer Warteschlange für Arbeitsaufgaben zu.</span><span class="sxs-lookup"><span data-stu-id="20449-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="20449-145">Benutzer</span><span class="sxs-lookup"><span data-stu-id="20449-145">User</span></span>          | <span data-ttu-id="20449-146">Weisen Sie den Genehmigungsschritt bestimmten Benutzern zu.</span><span class="sxs-lookup"><span data-stu-id="20449-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="20449-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20449-147">See also</span></span>
--------

[<span data-ttu-id="20449-148">Definieren von geschäftlichen Prozessworkflows für Bestellanforderungen.</span><span class="sxs-lookup"><span data-stu-id="20449-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="20449-149">Bestellanforderungsworkflow</span><span class="sxs-lookup"><span data-stu-id="20449-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




