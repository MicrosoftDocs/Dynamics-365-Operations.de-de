---
title: Beschaffungsworkflows
description: Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat. Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e591007a1330fe11b3f586185f9daca845798908
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218464"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="d5920-104">Beschaffungsworkflows</span><span class="sxs-lookup"><span data-stu-id="d5920-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5920-105">Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d5920-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="d5920-106">Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5920-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="d5920-107">Ein Workflow stellt einen Geschäftsprozess dar.</span><span class="sxs-lookup"><span data-stu-id="d5920-107">A workflow represents a business process.</span></span> <span data-ttu-id="d5920-108">Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="d5920-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="d5920-109">Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="d5920-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="d5920-110">**Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="d5920-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="d5920-111">Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="d5920-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="d5920-112">**Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="d5920-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="d5920-113">So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="d5920-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="d5920-114">**Zentralisierte Arbeitsliste**- Benutzer können eine zentralisierte Arbeitsliste öffnen, um die Workflowaufgaben und ‑genehmigungen anzuzeigen, die ihnen zu allen Workflows zugewiesen werden, an denen sie teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="d5920-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="d5920-115">Dies ist in der Arbeitsaufgabenseite verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5920-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="d5920-116">Erstellbare Workflowtypen</span><span class="sxs-lookup"><span data-stu-id="d5920-116">The types of workflows that you can create</span></span>

<span data-ttu-id="d5920-117">Die folgenden Workflowtypen stehen für die Beschaffung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d5920-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="d5920-118">Typ</span><span class="sxs-lookup"><span data-stu-id="d5920-118">Type</span></span> | <span data-ttu-id="d5920-119">Mit diesem Typ können Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="d5920-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="d5920-120">Prüfung der Bestellanforderungen</span><span class="sxs-lookup"><span data-stu-id="d5920-120">Purchase requisition review</span></span> | <span data-ttu-id="d5920-121">Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellanforderungen.</span><span class="sxs-lookup"><span data-stu-id="d5920-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="d5920-122">Prüfung der Bestellanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="d5920-122">Purchase requisition line review</span></span> | <span data-ttu-id="d5920-123">Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellanforderungspositionen.</span><span class="sxs-lookup"><span data-stu-id="d5920-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="d5920-124">Bestellworkflow</span><span class="sxs-lookup"><span data-stu-id="d5920-124">Purchase order workflow</span></span> | <span data-ttu-id="d5920-125">Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellungen.</span><span class="sxs-lookup"><span data-stu-id="d5920-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="d5920-126">Bestellpositionsworkflow</span><span class="sxs-lookup"><span data-stu-id="d5920-126">Purchase order line workflow</span></span> | <span data-ttu-id="d5920-127">Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellpositionen.</span><span class="sxs-lookup"><span data-stu-id="d5920-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="d5920-128">Workflow für Antrag zum Hinzufügen eines Kreditors</span><span class="sxs-lookup"><span data-stu-id="d5920-128">Vendor add application workflow</span></span> | <span data-ttu-id="d5920-129">Erstellen Sie Prüfungs- und Genehmigungsworkflows zum Hinzufügen neuer Kreditoren über Kreditorenanforderungen.</span><span class="sxs-lookup"><span data-stu-id="d5920-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="d5920-130">Wenn Sie einen neuen Workflow hinzufügen, werden möglicherweise auch die folgenden veralteten Workflows im Dialogfeld **Workflow erstellen** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5920-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="d5920-131">Diese beziehen sich auf die *Empfangsbestätigung*-Funktionalität, die in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows) verfügbar war, die aber jetzt außer Betrieb genommen wurde.</span><span class="sxs-lookup"><span data-stu-id="d5920-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="d5920-132">Diese Workflows werden derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5920-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="d5920-133">Workflow für Benachrichtigung über Lieferfälligkeit</span><span class="sxs-lookup"><span data-stu-id="d5920-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="d5920-134">Workflow für Benachrichtigung über Rechnungseingang</span><span class="sxs-lookup"><span data-stu-id="d5920-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="d5920-135">Workflow für Benachrichtigung über Produktzugangsfehler</span><span class="sxs-lookup"><span data-stu-id="d5920-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="d5920-136">Workflow für Benachrichtigung über einen abgelehnten, nicht bestätigten Produktzugang</span><span class="sxs-lookup"><span data-stu-id="d5920-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="d5920-137">Erstellen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="d5920-137">Creating a workflow</span></span>

<span data-ttu-id="d5920-138">Um einen Workflow zu erstellen, wechseln Sie zu Beschaffung &gt; Einrichtung &gt; Beschaffungsworkflows und erstellen Sie einen neuen Workflow, indem sie den Workflowtyp auswählen, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="d5920-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="d5920-139">Auf der Workflowarbeitsfläche können Sie Workflowelemente in den Designer ziehen und die Elemente in einen Fluss verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d5920-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="d5920-140">Die Workflowelemente sollten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d5920-140">The workflow elements should be configured.</span></span> <span data-ttu-id="d5920-141">Für Genehmigungs- und Aufgabenworkflowelemente können Sie konfigurieren, welcher Teilnehmer Aktivitäten ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="d5920-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="d5920-142">Teilnehmertypen</span><span class="sxs-lookup"><span data-stu-id="d5920-142">Types of participants</span></span>

<span data-ttu-id="d5920-143">Sie können folgenden Teilnehmergruppen einen Genehmigungsschritt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d5920-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="d5920-144">Benutzergruppe</span><span class="sxs-lookup"><span data-stu-id="d5920-144">User group</span></span> | <span data-ttu-id="d5920-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5920-145">Description</span></span> |
|---|---|
| <span data-ttu-id="d5920-146">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="d5920-146">Participant</span></span> | <span data-ttu-id="d5920-147">Weisen Sie den Genehmigungsschritt den Mitgliedern einer Gruppe oder Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="d5920-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="d5920-148">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="d5920-148">Hierarchy</span></span> | <span data-ttu-id="d5920-149">Weisen Sie den Genehmigungsschritt den Benutzern in einer bestimmten Organisationshierarchie zu.</span><span class="sxs-lookup"><span data-stu-id="d5920-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="d5920-150">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="d5920-150">Workflow user</span></span> | <span data-ttu-id="d5920-151">Weisen Sie den Genehmigungsschritt den Benutzern dieses Workflows zu.</span><span class="sxs-lookup"><span data-stu-id="d5920-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="d5920-152">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="d5920-152">Queue</span></span> | <span data-ttu-id="d5920-153">Weisen Sie den Genehmigungsschritt einer Warteschlange für Arbeitsaufgaben zu.</span><span class="sxs-lookup"><span data-stu-id="d5920-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="d5920-154">Benutzer</span><span class="sxs-lookup"><span data-stu-id="d5920-154">User</span></span> | <span data-ttu-id="d5920-155">Weisen Sie den Genehmigungsschritt bestimmten Benutzern zu.</span><span class="sxs-lookup"><span data-stu-id="d5920-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d5920-156">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d5920-156">Additional resources</span></span>

- [<span data-ttu-id="d5920-157">Definieren von geschäftlichen Prozessworkflows für Bestellanforderungen.</span><span class="sxs-lookup"><span data-stu-id="d5920-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="d5920-158">Bestellanforderungs-Workflow</span><span class="sxs-lookup"><span data-stu-id="d5920-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="d5920-159">Kreditoren aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d5920-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]