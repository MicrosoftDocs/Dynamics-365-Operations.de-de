---
title: Workflows für Ausgaben einrichten
description: Sie können einen Workflowprozess zum Prüfen und Genehmigen von Reisekosten- und Ausgabendokumenten einrichten.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177905"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="249ea-103">Workflows für Ausgaben einrichten</span><span class="sxs-lookup"><span data-stu-id="249ea-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="249ea-104"> Sie können einen Workflowprozess zum Prüfen und Genehmigen von Reisekosten- und Ausgabendokumenten einrichten.</span><span class="sxs-lookup"><span data-stu-id="249ea-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="249ea-105">Zu den Dokumenten, für die Workflows definiert werden können, gehören Spesenabrechnungen, Reiseanforderungen, Kreditkartenstreitigkeiten und Barvorschussanforderungen.</span><span class="sxs-lookup"><span data-stu-id="249ea-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="249ea-106">Ein Workflow stellt einen Geschäftsprozess dar.</span><span class="sxs-lookup"><span data-stu-id="249ea-106">A workflow represents a business process.</span></span> <span data-ttu-id="249ea-107">Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="249ea-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="249ea-108">Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="249ea-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="249ea-109">**Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="249ea-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="249ea-110">Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="249ea-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="249ea-111">Prozesssichtbarkeit – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="249ea-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="249ea-112">So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="249ea-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="249ea-113">Zentralisierte Arbeitsliste – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="249ea-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="249ea-114">**Erstellbare Workflowtypen**</span><span class="sxs-lookup"><span data-stu-id="249ea-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="249ea-115">In der folgenden Tabelle sind die Workflowtypen aufgeführt, die unter **Ausgaben** erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="249ea-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="249ea-116"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="249ea-117"><strong>Mit diesem Typ können Sie folgende Aufgaben ausführen:</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="249ea-118"><strong>Spesenabrechnung</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="249ea-119">Erstellen von Genehmigungsworkflows für Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="249ea-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="249ea-120"><strong>Automatische Buchung von Spesenabrechnung</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="249ea-121">Erstellen automatischer Buchungsworkflows für Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="249ea-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="249ea-122"><strong>Ausgabenposition</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="249ea-123">Erstellen von Genehmigungsworkflows für Positionsartikel in Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="249ea-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="249ea-124"><strong>Automatische Buchung von Ausgabenpositionen</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="249ea-125">Erstellen von Workflows zum automatischen Buchen von Positionsartikeln in Spesenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="249ea-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="249ea-126"><strong>Reiseanforderung</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="249ea-127">Erstellen von Workflows für die Genehmigung von Reiseanforderungen</span><span class="sxs-lookup"><span data-stu-id="249ea-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="249ea-128"><strong>Barvorschussanforderung</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="249ea-129">Erstellen von Genehmigungsworkflows für Barvorschussanforderungen</span><span class="sxs-lookup"><span data-stu-id="249ea-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="249ea-130"><strong>USt.-Beitreibung</strong></span><span class="sxs-lookup"><span data-stu-id="249ea-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="249ea-131">Erstellen von Genehmigungsworkflows für die Beitreibung der Mehrwertsteuer (MwSt.)</span><span class="sxs-lookup"><span data-stu-id="249ea-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

