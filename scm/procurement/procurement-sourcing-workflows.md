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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 80853a06e599786e2dcaf049ac733c47dfe4d9a5
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="5bfcb-104">Beschaffungsworkflows</span><span class="sxs-lookup"><span data-stu-id="5bfcb-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5bfcb-105">Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="5bfcb-106">Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="5bfcb-107">Ein Workflow stellt einen Geschäftsprozess dar.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-107">A workflow represents a business process.</span></span> <span data-ttu-id="5bfcb-108">Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="5bfcb-109">Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="5bfcb-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="5bfcb-110">**Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="5bfcb-111">Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="5bfcb-112">**Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="5bfcb-113">So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="5bfcb-114">**Zentralisierte Arbeitsliste**- Benutzer können eine zentralisierte Arbeitsliste öffnen, um die Workflowaufgaben und ‑genehmigungen anzuzeigen, die ihnen zu allen Workflows zugewiesen werden, an denen sie teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="5bfcb-115">Dies ist in der Arbeitsaufgabenseite verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="5bfcb-116"> Erstellbare Workflowtypen</span><span class="sxs-lookup"><span data-stu-id="5bfcb-116">The types of workflows that you can create</span></span>
<span data-ttu-id="5bfcb-117">Die folgenden Workflowtypen stehen für die Beschaffung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5bfcb-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5bfcb-118">**Type**</span></span>                         | <span data-ttu-id="5bfcb-119">**Mit diesem Typ können Sie folgende Aufgaben ausführen:**</span><span class="sxs-lookup"><span data-stu-id="5bfcb-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="5bfcb-120">Prüfung der Bestellanforderungen</span><span class="sxs-lookup"><span data-stu-id="5bfcb-120">Purchase requisition review</span></span>      | <span data-ttu-id="5bfcb-121">Erstellen Sie Prüfungsworkflows für Bestellanforderungen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="5bfcb-122">Prüfung der Bestellanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="5bfcb-122">Purchase requisition line review</span></span> | <span data-ttu-id="5bfcb-123">Erstellen Sie Prüfungsworkflows für Bestellanforderungspositionen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="5bfcb-124">Bestellworkflow</span><span class="sxs-lookup"><span data-stu-id="5bfcb-124">Purchase order workflow</span></span>          | <span data-ttu-id="5bfcb-125">Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellungen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="5bfcb-126">Bestellpositionsworkflow</span><span class="sxs-lookup"><span data-stu-id="5bfcb-126">Purchase order line workflow</span></span>     | <span data-ttu-id="5bfcb-127">Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellpositionen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="5bfcb-128">Erstellen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="5bfcb-128">Creating a workflow</span></span>
<span data-ttu-id="5bfcb-129">Um einen Workflow zu erstellen, wechseln Sie zu Beschaffung &gt; Einrichtung &gt; Beschaffungsworkflows und erstellen Sie einen neuen Workflow, indem sie den Workflowtyp auswählen, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="5bfcb-130">Auf der Workflowarbeitsfläche können Sie Workflowelemente in den Designer ziehen und die Elemente in einen Fluss verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="5bfcb-131">Die Workflowelemente sollten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-131">The workflow elements should be configured.</span></span> <span data-ttu-id="5bfcb-132">Für Genehmigungs- und Aufgabenworkflowelemente können Sie konfigurieren, welcher Teilnehmer Aktivitäten ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="5bfcb-133">Teilnehmertypen</span><span class="sxs-lookup"><span data-stu-id="5bfcb-133">Types of participants</span></span>
----------------------

<span data-ttu-id="5bfcb-134">Sie können folgenden Teilnehmergruppen einen Genehmigungsschritt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="5bfcb-135">Benutzergruppe</span><span class="sxs-lookup"><span data-stu-id="5bfcb-135">User group</span></span>    | <span data-ttu-id="5bfcb-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bfcb-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="5bfcb-137">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="5bfcb-137">Participant</span></span>   | <span data-ttu-id="5bfcb-138">Weisen Sie den Genehmigungsschritt den Mitgliedern einer Gruppe oder Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="5bfcb-139">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="5bfcb-139">Hierarchy</span></span>     | <span data-ttu-id="5bfcb-140">Weisen Sie den Genehmigungsschritt den Benutzern in einer bestimmten Organisationshierarchie zu.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="5bfcb-141">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="5bfcb-141">Workflow user</span></span> | <span data-ttu-id="5bfcb-142">Weisen Sie den Genehmigungsschritt den Benutzern dieses Workflows zu.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="5bfcb-143">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="5bfcb-143">Queue</span></span>         | <span data-ttu-id="5bfcb-144">Weisen Sie den Genehmigungsschritt einer Warteschlange für Arbeitsaufgaben zu.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="5bfcb-145">Benutzer</span><span class="sxs-lookup"><span data-stu-id="5bfcb-145">User</span></span>          | <span data-ttu-id="5bfcb-146">Weisen Sie den Genehmigungsschritt bestimmten Benutzern zu.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="5bfcb-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bfcb-147">See also</span></span>
--------

[<span data-ttu-id="5bfcb-148">Definieren von geschäftlichen Prozessworkflows für Bestellanforderungen.</span><span class="sxs-lookup"><span data-stu-id="5bfcb-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="5bfcb-149">Bestellanforderungsworkflow</span><span class="sxs-lookup"><span data-stu-id="5bfcb-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




