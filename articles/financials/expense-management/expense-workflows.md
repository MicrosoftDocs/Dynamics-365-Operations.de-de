---
title: "Workflows für Ausgaben einrichten"
description: "Sie können einen Workflowprozess zum Prüfen und Genehmigen von Reisekosten- und Ausgabendokumenten einrichten."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="43a67-103">Workflows für Ausgaben einrichten</span><span class="sxs-lookup"><span data-stu-id="43a67-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="43a67-104"> Sie können einen Workflowprozess zum Prüfen und Genehmigen von Reisekosten- und Ausgabendokumenten einrichten.</span><span class="sxs-lookup"><span data-stu-id="43a67-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="43a67-105">Zu den Dokumenten, für die Workflows definiert werden können, gehören Spesenabrechnungen, Reiseanforderungen, Kreditkartenstreitigkeiten und Barvorschussanforderungen.</span><span class="sxs-lookup"><span data-stu-id="43a67-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="43a67-106">Ein Workflow stellt einen Geschäftsprozess dar.</span><span class="sxs-lookup"><span data-stu-id="43a67-106">A workflow represents a business process.</span></span> <span data-ttu-id="43a67-107">Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="43a67-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="43a67-108">Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="43a67-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="43a67-109">**Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="43a67-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="43a67-110">Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="43a67-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="43a67-111">Prozesssichtbarkeit – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="43a67-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="43a67-112">So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="43a67-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="43a67-113">Zentralisierte Arbeitsliste – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="43a67-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="43a67-114">**Erstellbare Workflowtypen**</span><span class="sxs-lookup"><span data-stu-id="43a67-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="43a67-115">In der folgenden Tabelle sind die Workflowtypen aufgeführt, die unter **Ausgaben** erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="43a67-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="43a67-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="43a67-116">**Type**</span></span>                           | <span data-ttu-id="43a67-117">**Mit diesem Typ können Sie folgende Aufgaben ausführen:**</span><span class="sxs-lookup"><span data-stu-id="43a67-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="43a67-118">**Spesenabrechnung**</span><span class="sxs-lookup"><span data-stu-id="43a67-118">**Expense report**</span></span>                 | <span data-ttu-id="43a67-119">Erstellen von Genehmigungsworkflows für Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="43a67-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="43a67-120">**Automatische Buchung von Spesenabrechnung**</span><span class="sxs-lookup"><span data-stu-id="43a67-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="43a67-121">Erstellen automatischer Buchungsworkflows für Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="43a67-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="43a67-122">**Ausgabenposition**</span><span class="sxs-lookup"><span data-stu-id="43a67-122">**Expense line item**</span></span>              | <span data-ttu-id="43a67-123">Erstellen von Genehmigungsworkflows für Positionsartikel in Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="43a67-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="43a67-124">**Automatische Buchung von Ausgabenpositionen**</span><span class="sxs-lookup"><span data-stu-id="43a67-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="43a67-125">Erstellen von Workflows zum automatischen Buchen von Positionsartikeln in Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="43a67-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="43a67-126">**Reiseanforderung**</span><span class="sxs-lookup"><span data-stu-id="43a67-126">**Travel requisition**</span></span>             | <span data-ttu-id="43a67-127">Erstellen von Workflows für die Genehmigung von Reiseanforderungen</span><span class="sxs-lookup"><span data-stu-id="43a67-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="43a67-128">**Barvorschussanforderung**</span><span class="sxs-lookup"><span data-stu-id="43a67-128">**Cash advance request**</span></span>           | <span data-ttu-id="43a67-129">Erstellen von Genehmigungsworkflows für Barvorschussanforderungen</span><span class="sxs-lookup"><span data-stu-id="43a67-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="43a67-130">**USt.-Beitreibung**</span><span class="sxs-lookup"><span data-stu-id="43a67-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="43a67-131">Erstellen von Genehmigungsworkflows für die Beitreibung der Mehrwertsteuer (MwSt.)</span><span class="sxs-lookup"><span data-stu-id="43a67-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

