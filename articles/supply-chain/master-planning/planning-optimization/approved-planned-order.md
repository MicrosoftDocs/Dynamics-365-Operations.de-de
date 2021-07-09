---
title: Geplante Aufträge anzeigen, verwalten und genehmigen
description: In diesem Thema finden Sie Informationen zum Anzeigen, Verwalten und Genehmigen von geplanten Aufträgen in der Planungsoptimierung.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304366"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="22a56-103">Geplante Aufträge anzeigen, verwalten und genehmigen</span><span class="sxs-lookup"><span data-stu-id="22a56-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22a56-104">In diesem Thema finden Sie Informationen zum Anzeigen, Verwalten und Genehmigen von geplanten Aufträgen in der Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="22a56-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="22a56-105">Geplante Aufträge anzeigen und verwalten</span><span class="sxs-lookup"><span data-stu-id="22a56-105">View and manage planned orders</span></span>

<span data-ttu-id="22a56-106">Sie können geplante Aufträge auf jeder Listenseite für geplante Aufträge anzeigen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="22a56-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="22a56-107">Gehen Sie zu einer der folgenden Stellen, je nach Art der geplanten Aufträge, mit denen Sie arbeiten wollen:</span><span class="sxs-lookup"><span data-stu-id="22a56-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="22a56-108">Produktprogrammplanung \> Arbeitsbereiche \> Gesamtplanung</span><span class="sxs-lookup"><span data-stu-id="22a56-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="22a56-109">Produktprogrammplanung \> Produktprogrammplanung \> Geplante Aufträge</span><span class="sxs-lookup"><span data-stu-id="22a56-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="22a56-110">Produktion Steuerelement \> Produktionsaufträge \> Geplante Produktionsaufträge</span><span class="sxs-lookup"><span data-stu-id="22a56-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="22a56-111">Beschaffung und Sourcing \> Bestellungen \> Geplante Aufträge</span><span class="sxs-lookup"><span data-stu-id="22a56-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="22a56-112">Lagerbestand verwalten \> Eingehende Aufträge \> Geplante Umlagerungen</span><span class="sxs-lookup"><span data-stu-id="22a56-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="22a56-113">Bestandsverwaltung \> Ausgehende Aufträge \> Geplante Umlagerungen</span><span class="sxs-lookup"><span data-stu-id="22a56-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="22a56-114">Anzeigen und Bearbeiten des Status geplanter Aufträge</span><span class="sxs-lookup"><span data-stu-id="22a56-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="22a56-115">Sie können das Feld **Status** jedes geplanten Auftrags verwenden, um Ihren Fortschritt zu verfolgen oder zu ändern, wie ein geplanter Auftrag verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="22a56-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="22a56-116">Die folgenden **Status**-Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="22a56-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="22a56-117">**Unbearbeitet** – Wenn die Produktprogrammplanung geplanter Aufträge erzeugt, erhalten diese diesen Status.</span><span class="sxs-lookup"><span data-stu-id="22a56-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="22a56-118">Geplante Aufträge, die diesen Status haben, werden beim nächsten Planungslauf gelöscht.</span><span class="sxs-lookup"><span data-stu-id="22a56-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="22a56-119">**Erledigt** – Dieser Status zeigt an, dass der geplante Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="22a56-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="22a56-120">Wenn Sie sich entscheiden, einen geplanten Auftrag nicht zu sperren, können Sie seinen Status manuell auf *Erledigt* ändern.</span><span class="sxs-lookup"><span data-stu-id="22a56-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="22a56-121">Beachten Sie, dass das System die Zustände *Unbearbeitet* und *Erledigt* gleich behandelt.</span><span class="sxs-lookup"><span data-stu-id="22a56-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="22a56-122">**Genehmigt** – Dieser Status zeigt an, dass der geplante Auftrag zur Umwandlung genehmigt ist.</span><span class="sxs-lookup"><span data-stu-id="22a56-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="22a56-123">Wenn Sie einen geplanten Auftrag fixieren wollen, können Sie seinen Status auf *Genehmigt* ändern.</span><span class="sxs-lookup"><span data-stu-id="22a56-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="22a56-124">Wenn Sie die Änderungen, die an einem geplanten Auftrag vorgenommen wurden, beibehalten wollen oder wenn Sie planen, einen geplanten Auftrag zu fixieren, ändern Sie seinen Status auf *Genehmigt*.</span><span class="sxs-lookup"><span data-stu-id="22a56-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="22a56-125">Geplante Aufträge, die den Status *Freigegeben* haben, werden von der Produktprogrammplanung als fixiert und erwartete Lieferung betrachtet.</span><span class="sxs-lookup"><span data-stu-id="22a56-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="22a56-126">Daher werden sie bei späteren Ausführungen der Produktprogrammplanung nicht geändert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="22a56-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="22a56-127">Um dieses Verhalten zu erreichen, kopiert die Planungslogik während der Produktprogrammplanung geplanter Aufträge, die den Status *Genehmigt* haben, von der alten Planversion in die neue Planversion.</span><span class="sxs-lookup"><span data-stu-id="22a56-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="22a56-128">Beachten Sie, dass geplanter Aufträge, die den Status *Genehmigt* haben, nur innerhalb des spezifischen Masterplans als Vorrat gelten.</span><span class="sxs-lookup"><span data-stu-id="22a56-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="22a56-129">Um den Status eines einzelnen geplanten Auftrags zu ändern, [öffnen Sie eine beliebige Listenseite für geplante Aufträge](#view-planned-orders), öffnen Sie den Auftrag und führen Sie dann einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="22a56-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="22a56-130">Ändern Sie auf dem Inforegister **Allgemein** den Wert des Feldes **Status**.</span><span class="sxs-lookup"><span data-stu-id="22a56-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="22a56-131">Im Aktivitätsbereich, auf der Registerkarte **Geplanter Auftrag**, in der Gruppe **Verarbeiten**, wählen Sie **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="22a56-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="22a56-132">Wählen Sie im Aktivitätsbereich **Genehmigen**, um den Auftrag als genehmigt zu markieren.</span><span class="sxs-lookup"><span data-stu-id="22a56-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="22a56-133">Um den Status mehrerer geplanter Aufträge gleichzeitig zu ändern, [öffnen Sie eine beliebige Listenseite für geplante Aufträge](#view-planned-orders), aktivieren Sie das Kontrollkästchen für jeden Auftrag, den Sie ändern möchten, und folgen Sie dann einem der folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="22a56-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="22a56-134">Im Aktivitätsbereich, auf der Registerkarte **Geplanter Auftrag**, in der Gruppe **Verarbeiten**, wählen Sie **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="22a56-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="22a56-135">Wählen Sie im Aktivitätsbereich **Freigeben**, um die Aufträge als genehmigt zu markieren.</span><span class="sxs-lookup"><span data-stu-id="22a56-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="22a56-136">Auftragsvorschläge genehmigen</span><span class="sxs-lookup"><span data-stu-id="22a56-136">Approve planned orders</span></span>

<span data-ttu-id="22a56-137">Die Genehmigung geplanter Aufträge ist ein optionaler Schritt im Prozess der Erstellung eines umgewandelten Auftrags aus einem geplanten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="22a56-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="22a56-138">Die folgende Abbildung zeigt, wie Sie den Wert **Status**, der jedem geplanten Auftrag zugeordnet ist, zur Implementierung eines Genehmigungs-Workflows verwenden können.</span><span class="sxs-lookup"><span data-stu-id="22a56-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="22a56-139">Um einen Genehmigungsprozess zu implementieren, passen Sie den **Status**-Wert für jeden geplanten Auftrag manuell an, wie im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="22a56-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Flow des Bestellvorschlags](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="22a56-141">Wir empfehlen, dass Sie alle geänderten geplanten Aufträge genehmigen.</span><span class="sxs-lookup"><span data-stu-id="22a56-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="22a56-142">Andernfalls werden die Bearbeitungen ignoriert und beim nächsten Planungslauf überschrieben.</span><span class="sxs-lookup"><span data-stu-id="22a56-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22a56-143">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="22a56-143">Additional resources</span></span>

- [<span data-ttu-id="22a56-144">Fest geplante Aufträge</span><span class="sxs-lookup"><span data-stu-id="22a56-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
