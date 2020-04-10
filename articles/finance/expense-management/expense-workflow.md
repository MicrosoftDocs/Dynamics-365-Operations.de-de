---
title: Spesenverwaltungsworkflow
description: In diesem Thema wird erläutert, wie Sie das Workflowsystem in Microsoft Dynamics 365 Finance verwenden können, um einen Prüfprozess für Spesenabrechnungen in der Spesenverwaltung einzurichten.
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
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153970"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="96e96-103">Spesenverwaltungsworkflow</span><span class="sxs-lookup"><span data-stu-id="96e96-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96e96-104">Mithilfe des Workflowsystems können Sie einen Prüfprozess für Spesenabrechnungen in „Ausgabenverwaltung“ einrichten.</span><span class="sxs-lookup"><span data-stu-id="96e96-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="96e96-105">Sie können einen Workflow einrichten, um zu bestimmen, wer Spesenabrechnungen unter den folgenden Kriterien genehmigt werden:</span><span class="sxs-lookup"><span data-stu-id="96e96-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="96e96-106">Die Mitarbeiterunterstellungshierarchie und die vordefinierten Genehmigungslimits</span><span class="sxs-lookup"><span data-stu-id="96e96-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="96e96-107">Genehmigung in mehreren Ebenen, die Zwischengenehmiger und einen letzten Genehmiger unterstützt</span><span class="sxs-lookup"><span data-stu-id="96e96-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="96e96-108">Finanzdimensionen und Projektzuständigkeit</span><span class="sxs-lookup"><span data-stu-id="96e96-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="96e96-109">Zuweisung zu bestimmten Benutzern oder Benutzergruppen</span><span class="sxs-lookup"><span data-stu-id="96e96-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="96e96-110">Workflowgenehmigungen können für Spesenabrechnungen, Reiseanforderungen, Barvorschüsse, Kreditkartenstreitigkeiten und Mehrwertsteuer (MwSt.)-Beitreibung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="96e96-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="96e96-111">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="96e96-111">**Example**</span></span>

<span data-ttu-id="96e96-112">Im Folgenden finden Sie ein Beispiel für einen Spesenverwaltungsworkflow für eine Spesenabrechnung:</span><span class="sxs-lookup"><span data-stu-id="96e96-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="96e96-113">Ein Mitarbeiter erstellt und speichert eine Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="96e96-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="96e96-114">Der Mitarbeiter übermittelt die Spesenabrechnung zur Genehmigung.</span><span class="sxs-lookup"><span data-stu-id="96e96-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="96e96-115">Die genehmigende Person wird basierend auf den Regeln identifiziert, die definiert wurden, als der Standardworkflow eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="96e96-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="96e96-116">Die genehmigende Person wird benachrichtigt, dass eine zu genehmigende Spesenabrechnung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="96e96-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="96e96-117">Die genehmigende Person prüft die Spesenabrechnung und überprüft, dass die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="96e96-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="96e96-118">Die Ausgaben verstoßen nicht gegen Ausgabenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="96e96-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="96e96-119">Wenn Ausgaben eine Richtlinie verletzen, überprüft die genehmigende Person, dass eine gültiger Geschäftsbegründung im Bericht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="96e96-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="96e96-120">Der Spesenabrechnung sind elektronische Belege angefügt.</span><span class="sxs-lookup"><span data-stu-id="96e96-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="96e96-121">Die genehmigende Person genehmigt die Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="96e96-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="96e96-122">Die Spesenabrechnung wird dem Kreditorenkoordinator zur Buchung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="96e96-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="96e96-123">Einer der folgenden Schritte erfolgt, abhängig davon an, ob die automatische Buchung konfiguriert ist:</span><span class="sxs-lookup"><span data-stu-id="96e96-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="96e96-124">Wenn die automatische Buchungen konfiguriert ist, wird die Spesenabrechnung für die Zahlung verarbeitet, und der Status der Spesenabrechnung wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="96e96-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="96e96-125">Wenn die automatische Buchung nicht konfiguriert ist, überprüft der Kreditorenkoordinator, dass alle ursprünglichen Zugänge gesendet wurden und dass die Zugänge den Ausgaben in der Spesenabrechnung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="96e96-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="96e96-126">Alle Steuercodes, die auf der Spesenabrechnung eingegeben werden, müssen ebenfalls auf Korrektheit geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="96e96-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="96e96-127">Nachdem diese Anforderungen überprüft wurden, wird die Spesenabrechnung gebucht.</span><span class="sxs-lookup"><span data-stu-id="96e96-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="96e96-128">Nachdem die Spesenabrechnung gebucht wurde, wird die Zahlung für die Spesenabrechnung autorisiert und dem Mitarbeiter erstattet.</span><span class="sxs-lookup"><span data-stu-id="96e96-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
