---
title: Workflows für Rückvergütungsverwaltungsdeals
description: In diesem Thema wird erläutert, wie Sie einen Workflow für Rückvergütungsverwaltungsdeals einrichten, um Deals zu genehmigen und zu aktivieren.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270956"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="c28a9-103">Workflows für Rückvergütungsverwaltungsdeals</span><span class="sxs-lookup"><span data-stu-id="c28a9-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c28a9-104">Um Rückvergütungsdeals zu genehmigen, verwendet die Rückvergütungsverwaltung dieselbe Workflow-Plattform wie andere Finance and Operations-Apps.</span><span class="sxs-lookup"><span data-stu-id="c28a9-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="c28a9-105">Jedem Workflow sind zwei Auftragsprozesse zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="c28a9-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="c28a9-106">Ein Element des Workflows genehmigt den Deal.</span><span class="sxs-lookup"><span data-stu-id="c28a9-106">One element of the workflow approves the deal.</span></span>
- <span data-ttu-id="c28a9-107">Ein Element des Workflows aktiviert den Deal, sodass der Benutzer oder der Workflowprozess die Transaktionen genehmigen kann.</span><span class="sxs-lookup"><span data-stu-id="c28a9-107">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>

<span data-ttu-id="c28a9-108">Bevor Sie einen Rückvergütungsdeal verwenden können, muss der im Modul **Rückvergütungsverwaltung** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c28a9-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="c28a9-109">Um einen Deal zu aktivieren, müssen Sie zuerst einen *Workflow für Rückvergütungsverwaltungsdeals* erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c28a9-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="c28a9-110">Benutzer können Geschäfte nicht manuell genehmigen.</span><span class="sxs-lookup"><span data-stu-id="c28a9-110">Users can't manually approve deals.</span></span> <span data-ttu-id="c28a9-111">Es muss immer der Workflow verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c28a9-111">The workflow must always be used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="c28a9-112">Workflows für Rückvergütungsverwaltungsdeals erstellen und verwalten</span><span class="sxs-lookup"><span data-stu-id="c28a9-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="c28a9-113">Um mit Ihren Workflows für Rückvergütungsverwaltungsdeals zu arbeiten, gehen Sie zu **Rückvergütungsverwaltung \> Einstellungen \> Workflows für Rückvergütungsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="c28a9-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="c28a9-114">Dort können Sie Workflows nach Bedarf anzeigen, erstellen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c28a9-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="c28a9-115">Nur jeweils ein Workflow dieses Typs kann aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="c28a9-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="c28a9-116">Weitere Informationen zu Workflows, zum Arbeiten mit der Seite **Workflows für Rückvergütungsverwaltungsdeals** und zum Erstellen von Workflows finden Sie unter [Workflowsystem – Übersicht](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) und den dazugehörigen Themen.</span><span class="sxs-lookup"><span data-stu-id="c28a9-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="c28a9-117">Einen Workflow zum Aktivieren eines Deals verwenden</span><span class="sxs-lookup"><span data-stu-id="c28a9-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="c28a9-118">Um einen Deal über einen Workflow zu aktivieren, öffnen Sie den Deal (z. B. auf der Seite **Alle Rückvergütungsverwaltungsdeals**).</span><span class="sxs-lookup"><span data-stu-id="c28a9-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="c28a9-119">Wählen Sie im Aktivitätsbereich **Workflow \> Senden**.</span><span class="sxs-lookup"><span data-stu-id="c28a9-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="c28a9-120">Nachdem der neue Deal über den Workflow verarbeitet und genehmigt wurde, ist es aktiv und einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="c28a9-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="c28a9-121">Nachdem ein Geschäft aktiviert wurde, können Sie die meisten seiner Einstellungen nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="c28a9-121">After a deal has been activated, you can't change most of its setup.</span></span> <span data-ttu-id="c28a9-122">Wenn Sie ein aktives Geschäft ändern müssen, inaktivieren Sie es zuerst und erstellen Sie dann ein neues Geschäft.</span><span class="sxs-lookup"><span data-stu-id="c28a9-122">If you must change an active deal, first inactivate it, and then create a new deal.</span></span> <span data-ttu-id="c28a9-123">Wenn der neue Deal dem alten ähnelt, können Sie ihn erstellen, indem Sie den alten Deal kopieren.</span><span class="sxs-lookup"><span data-stu-id="c28a9-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

<span data-ttu-id="c28a9-124">Sie können die folgenden Einstellungen für ein Geschäft ändern, nachdem es aktiviert wurde:</span><span class="sxs-lookup"><span data-stu-id="c28a9-124">You can change the following settings for a deal after it has been activated:</span></span>

- <span data-ttu-id="c28a9-125">Abstimmen nach</span><span class="sxs-lookup"><span data-stu-id="c28a9-125">Reconcile by</span></span>
- <span data-ttu-id="c28a9-126">Kumulative Garantie</span><span class="sxs-lookup"><span data-stu-id="c28a9-126">Cumulative guarantee</span></span>
- <span data-ttu-id="c28a9-127">Buchungsprofil</span><span class="sxs-lookup"><span data-stu-id="c28a9-127">Posting profile</span></span>
- <span data-ttu-id="c28a9-128">Buchungsprofil für Garantie</span><span class="sxs-lookup"><span data-stu-id="c28a9-128">Posting profile for guarantee</span></span>
- <span data-ttu-id="c28a9-129">Dokumentnotizen</span><span class="sxs-lookup"><span data-stu-id="c28a9-129">Document notes</span></span>
- <span data-ttu-id="c28a9-130">Währung</span><span class="sxs-lookup"><span data-stu-id="c28a9-130">Currency</span></span>
- <span data-ttu-id="c28a9-131">Anfangsdatum</span><span class="sxs-lookup"><span data-stu-id="c28a9-131">From date</span></span>
- <span data-ttu-id="c28a9-132">Bis-Datum</span><span class="sxs-lookup"><span data-stu-id="c28a9-132">To date</span></span>

<span data-ttu-id="c28a9-133">Darüber hinaus können Bonuszeilen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c28a9-133">In addition, rebate lines can be removed.</span></span>
