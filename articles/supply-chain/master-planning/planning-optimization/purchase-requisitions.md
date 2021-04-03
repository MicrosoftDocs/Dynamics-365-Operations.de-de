---
title: Bestellanforderungen
description: In diesem Thema wird beschrieben, wie Bestellanforderungen in der Planungsoptimierung unterstützt werden.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 20b4012e054a25d7d21c6f017d8ebcf18f6ee28d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501077"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="e3c5f-103">Bestellanforderungen</span><span class="sxs-lookup"><span data-stu-id="e3c5f-103">Purchase requisitions</span></span>

<span data-ttu-id="e3c5f-104">Die Masterplanung kann genehmigte Bestellanforderungen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="e3c5f-105">Um Bestellanforderungen abzudecken, müssen Benutzer daher keinen Workflow zum Erstellen von Bestellungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="e3c5f-106">Stattdessen können Bestellanforderungen durch die Masterplanung abgedeckt werden.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="e3c5f-107">Aufgrund dieser Funktionalität kann eine Bestellanforderung abhängig vom Wert von **Geplante Auftragsart**, der für das zugehörige Produkt festgelegt wird, eine Bestellung, einen Umlagerungsauftrag oder einen Produktionsauftrag erzeugen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="e3c5f-108">Aktivieren von Masterplänen einschließlich Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3c5f-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="e3c5f-109">Führen Sie die folgenden Schritte aus, um Anforderungen in die Abdeckungsberechnung für einen Masterplan einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="e3c5f-110">Wechseln Sie zu **Masterplanung** \> **Einrichten** \> **Pläne** \> **Masterpläne**.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="e3c5f-111">Erstellen Sie einen Masterplan oder wählen Sie einen aus.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="e3c5f-112">Legen Sie im Inforegister **Allgemein** die Option **Anforderungen einbeziehen** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="e3c5f-113">Wiederholen Sie die Schritte 2 und 3 für jeden weiteren Masterplan, in den Sie Anforderungen einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="e3c5f-114">Genehmigter Anforderungsplanungszeitraum</span><span class="sxs-lookup"><span data-stu-id="e3c5f-114">Approved requisitions time fence</span></span>

<span data-ttu-id="e3c5f-115">Die Option *Zeitraum für genehmigte Anforderungen* legt fest, wie lange (in Tagen) ein Masterplan die Nachfrage aus genehmigten Wiederbeschaffungsanforderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="e3c5f-116">Sie können einen genehmigten Zeitraum für Anforderungen sowohl auf der Ebene der Deckungsgruppe als auch auf der Ebene des Masterplans festlegen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="e3c5f-117">Festlegen des Zeitraums für genehmigte Anforderungen für eine Abdeckungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e3c5f-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="e3c5f-118">Gehen Sie zu **Produktprogrammplanung** \> **Einrichten** \> **Deckung** \> **Deckungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="e3c5f-119">Erstellen oder Sie eine Abdeckungsgruppe oder wählen Sie eine aus.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="e3c5f-120">Legen Sie im Inforegister **Sonstiges** das Feld **Zeitraum für genehmigte Anforderungen (Tage)** auf die Anzahl der Tage fest, die in den Zeitraum aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="e3c5f-121">Wiederholen Sie die Schritte 2 und 3 für jede zusätzliche Abdeckungsgruppe, für die Sie einen Zeitraum für genehmigte Anforderungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="e3c5f-122">Festlegen des Zeitraums für genehmigte Anforderungen für einzelne Masterpläne</span><span class="sxs-lookup"><span data-stu-id="e3c5f-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="e3c5f-123">Wenn Sie für einen einzelnen Masterplan einen Zeitraum für eine genehmigte Anforderung festlegen, überschreibt die Einstellung die Zeitraumeinstellung für jede anwendbare Abdeckungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="e3c5f-124">Wechseln Sie zu **Masterplanung** \> **Einrichten** \> **Pläne** \> **Masterpläne**.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="e3c5f-125">Erstellen Sie einen Masterplan oder wählen Sie einen aus.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="e3c5f-126">Legen Sie im Inforegister **Planungszeiträume in Tagen** das Feld **Zeitraum für genehmigte Anforderungen (Tage)** auf die Anzahl der Tage fest, die in den Zeitraum aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="e3c5f-127">Wiederholen Sie die Schritte 2 und 3 für jeden zusätzliche Masterplan, für den Sie einen Zeitraum für genehmigte Anforderungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3c5f-128">**Bald verfügbar:** Zeiträume für genehmigte Anforderungen werden für die Planungsoptimierung noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="e3c5f-129">Bis sie unterstützt werden, werden alle Werte ignoriert, die Sie in das Feld **Zeitraum für genehmigte Anforderungen (Tage)** eingeben.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="e3c5f-130">Unabhängige Lieferung, unabhängig vom Abdeckungscode</span><span class="sxs-lookup"><span data-stu-id="e3c5f-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="e3c5f-131">Bestellanforderungen werden unabhängig vom Abdeckungscode immer von unabhängigen geplanten Aufträgen abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="e3c5f-132">Dieses Verhalten gewährleistet eine eindeutige Rückverfolgbarkeit und Workflows zwischen Bestellanforderungen und Wiederbeschaffungsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="e3c5f-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3c5f-133">Example 1</span></span>

<span data-ttu-id="e3c5f-134">Ein Produkt ist für die Option **Abdeckungscode** mit einem Wert von *Min./Max.* eingerichtet. Es hat die folgenden Bestands- und Anforderungsstatus:</span><span class="sxs-lookup"><span data-stu-id="e3c5f-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="e3c5f-135">Verfügbare Menge im Bestand = 10.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="e3c5f-136">Minimale Bestandsmenge = 15.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="e3c5f-137">Maximale Bestandsmenge = 20.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="e3c5f-138">Es ist eine Bestellanforderung für ein Stück vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="e3c5f-139">Sie hat als gewünschtes Datum den heutigen Tag.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-139">It has a requested date of today.</span></span>

<span data-ttu-id="e3c5f-140">Wenn die Masterplanung ausgeführt wird, werden zwei geplante Aufträge erstellt: einer für 10 Stück, um den Bestand auf die maximale Menge aufzufüllen, und einer für ein Stück, um die Bestellanforderung aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="e3c5f-141">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e3c5f-141">Example 2</span></span>

<span data-ttu-id="e3c5f-142">Ein Produkt ist für die Option **Abdeckungscode** mit einem Wert von *Min./Max.* eingerichtet. Es hat die folgenden Bestands- und Anforderungsstatus:</span><span class="sxs-lookup"><span data-stu-id="e3c5f-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="e3c5f-143">Verfügbare Menge im Bestand = 17.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="e3c5f-144">Minimale Bestandsmenge = 15.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="e3c5f-145">Maximale Bestandsmenge = 20.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="e3c5f-146">Es ist eine Bestellanforderung für ein Stück vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="e3c5f-147">Sie hat als gewünschtes Datum den heutigen Tag.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-147">It has a requested date of today.</span></span>

<span data-ttu-id="e3c5f-148">Wenn die Masterplanung ausgeführt wird, wird ein geplanter Auftrag für ein Stück erstellt, um die Bestellanforderung aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="e3c5f-149">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e3c5f-149">Example 3</span></span>

<span data-ttu-id="e3c5f-150">Ein Produkt ist für die Option **Abdeckungscode** mit einem Wert von *Zeitraum* und eine Periodenlänge von sieben Tagen eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="e3c5f-151">Es hat die folgenden Bestands-, Auftrags- und Anforderungsstatus:</span><span class="sxs-lookup"><span data-stu-id="e3c5f-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="e3c5f-152">Verfügbare Menge im Bestand = 0.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="e3c5f-153">Es ist ein Auftrag für fünf Stück vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="e3c5f-154">Er enthält als voraussichtliches Versanddatum das heutige Datum plus einen Tag.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="e3c5f-155">Es ist eine Bestellanforderung für drei Stück vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="e3c5f-156">Sie hat als angefordertes Datum das heutige Datum plus drei Tage.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="e3c5f-157">Wenn die Masterplanung ausgeführt wird, werden zwei geplante Aufträge erstellt: einer für drei Stück, um die Bestellanforderung aufzufüllen, und einer für fünf Stück, um den Auftragsbedarf aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="e3c5f-158">Nachdem ein geplanter Auftrag, der an eine Bestellanforderung gebunden ist, umgewandelt wurde, behält das Planungsmodul den Bedarfsverursacher für die Bestellanforderung bei.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="e3c5f-159">Wenn später festgestellt wird, dass dem umgewandelten Auftrag eine Menge fehlt, die zur Erfüllung der Bestellanforderung erforderlich ist, erstellt das System einen neuen geplanten Auftrag für die Differenz.</span><span class="sxs-lookup"><span data-stu-id="e3c5f-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="e3c5f-160">Weitere Informationen zu Bestellanforderungen finden Sie unter [Übersicht über Bestellanforderung](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e3c5f-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]