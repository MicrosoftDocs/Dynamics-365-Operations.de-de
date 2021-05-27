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
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020385"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="740b1-103">Workflows für Rückvergütungsverwaltungsdeals</span><span class="sxs-lookup"><span data-stu-id="740b1-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="740b1-104">Um Rückvergütungsdeals zu genehmigen, verwendet die Rückvergütungsverwaltung dieselbe Workflow-Plattform wie andere Finance and Operations-Apps.</span><span class="sxs-lookup"><span data-stu-id="740b1-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="740b1-105">Jedem Workflow sind zwei Auftragsprozesse zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="740b1-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="740b1-106">Ein Element des Workflows aktiviert den Deal, sodass der Benutzer oder der Workflowprozess die Transaktionen genehmigen kann.</span><span class="sxs-lookup"><span data-stu-id="740b1-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="740b1-107">Ein Element des Workflows genehmigt den Deal.</span><span class="sxs-lookup"><span data-stu-id="740b1-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="740b1-108">Bevor Sie einen Rückvergütungsdeal verwenden können, muss der im Modul **Rückvergütungsverwaltung** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="740b1-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="740b1-109">Um einen Deal zu aktivieren, müssen Sie zuerst einen *Workflow für Rückvergütungsverwaltungsdeals* erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="740b1-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="740b1-110">Nachdem ein Workflow für die Rückvergütungsverwaltung aktiviert wurde, können Benutzer Deals nicht manuell genehmigen.</span><span class="sxs-lookup"><span data-stu-id="740b1-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="740b1-111">Der Workflow muss immer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="740b1-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="740b1-112">Workflows für Rückvergütungsverwaltungsdeals erstellen und verwalten</span><span class="sxs-lookup"><span data-stu-id="740b1-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="740b1-113">Um mit Ihren Workflows für Rückvergütungsverwaltungsdeals zu arbeiten, gehen Sie zu **Rückvergütungsverwaltung \> Einstellungen \> Workflows für Rückvergütungsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="740b1-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="740b1-114">Dort können Sie Workflows nach Bedarf anzeigen, erstellen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="740b1-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="740b1-115">Nur jeweils ein Workflow dieses Typs kann aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="740b1-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="740b1-116">Weitere Informationen zu Workflows, zum Arbeiten mit der Seite **Workflows für Rückvergütungsverwaltungsdeals** und zum Erstellen von Workflows finden Sie unter [Workflowsystem – Übersicht](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) und den dazugehörigen Themen.</span><span class="sxs-lookup"><span data-stu-id="740b1-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="740b1-117">Einen Workflow zum Aktivieren eines Deals verwenden</span><span class="sxs-lookup"><span data-stu-id="740b1-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="740b1-118">Um einen Deal über einen Workflow zu aktivieren, öffnen Sie den Deal (z. B. auf der Seite **Alle Rückvergütungsverwaltungsdeals**).</span><span class="sxs-lookup"><span data-stu-id="740b1-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="740b1-119">Wählen Sie im Aktivitätsbereich **Workflow \> Senden**.</span><span class="sxs-lookup"><span data-stu-id="740b1-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="740b1-120">Nachdem der neue Deal über den Workflow verarbeitet und genehmigt wurde, ist es aktiv und einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="740b1-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="740b1-121">Nachdem ein Deal aktiviert wurde, können Sie dessen Einstellungen nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="740b1-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="740b1-122">Wenn Sie einen aktiven Deal ändern müssen, deaktivieren Sie ihn und erstellen Sie einen neuen.</span><span class="sxs-lookup"><span data-stu-id="740b1-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="740b1-123">Wenn der neue Deal dem alten ähnelt, können Sie ihn erstellen, indem Sie den alten Deal kopieren.</span><span class="sxs-lookup"><span data-stu-id="740b1-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
