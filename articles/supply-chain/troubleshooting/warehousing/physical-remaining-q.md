---
title: Physikalische Restmenge in der Einheit darf nicht Null sein
description: Wenn Sie einen Lieferschein erzeugen, haben die Daten, die ihm zugeführt werden, eine Bestandsmenge ungleich Null, aber eine Verkaufsmenge von Null.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248782"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="70c37-103">Physikalische Restmenge in der Einheit darf nicht Null sein</span><span class="sxs-lookup"><span data-stu-id="70c37-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="70c37-104">Fehlercode: SYS19591</span><span class="sxs-lookup"><span data-stu-id="70c37-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="70c37-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="70c37-105">Symptoms</span></span>

<span data-ttu-id="70c37-106">Wenn Sie einen Lieferschein erzeugen, haben die Daten, die ihm zugeführt werden, eine Bestandsmenge ungleich Null, aber eine Verkaufsmenge von Null.</span><span class="sxs-lookup"><span data-stu-id="70c37-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="70c37-107">Wenn Sie versuchen, den Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="70c37-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="70c37-108">Physische Restmenge in Einheit '%1' darf nicht Null sein.</span><span class="sxs-lookup"><span data-stu-id="70c37-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="70c37-109">Daher können Sie den Lieferschein für die Ladung nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="70c37-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="70c37-110">Ursache</span><span class="sxs-lookup"><span data-stu-id="70c37-110">Cause</span></span>

<span data-ttu-id="70c37-111">Das System wertet die physische Restmenge in der Einheit des Bestands und die physische Restmenge im Versandelement aus.</span><span class="sxs-lookup"><span data-stu-id="70c37-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="70c37-112">Wenn das System feststellt, dass die physische Restmenge in der Versandeinheit 0 (Null) ist, die physische Restmenge in der Bestandseinheit aber nicht 0 ist, können Sie den Lieferschein nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="70c37-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="70c37-113">Dieses Problem kann z. B. auftreten, wenn die Verkaufseinheit und die Bestandseinheit für das Element unterschiedlich sind und die Umrechnung zwischen den Einheiten nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="70c37-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="70c37-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="70c37-114">Resolution</span></span>

<span data-ttu-id="70c37-115">Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="70c37-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="70c37-116">Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="70c37-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="70c37-117">Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="70c37-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="70c37-118">Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Mengen sauber umgerechnet werden können, ohne dass Rundungsprobleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="70c37-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="70c37-119">Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="70c37-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="70c37-120">Stellen Sie sicher, dass die Maßeinheit des Bestands kleiner ist als die Maßeinheit des Verkaufs.</span><span class="sxs-lookup"><span data-stu-id="70c37-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="70c37-121">Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen sind und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="70c37-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="70c37-122">Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="70c37-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="70c37-123">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="70c37-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="70c37-124">Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="70c37-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="70c37-125">Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.</span><span class="sxs-lookup"><span data-stu-id="70c37-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="70c37-126">Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.</span><span class="sxs-lookup"><span data-stu-id="70c37-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="70c37-127">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="70c37-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="70c37-128">Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="70c37-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="70c37-129">Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="70c37-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="70c37-130">Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Menge sauber und ohne Rundungsprobleme umgerechnet werden kann</span><span class="sxs-lookup"><span data-stu-id="70c37-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="70c37-131">Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und Anpassungen vorzunehmen, um sicherzustellen, dass die Menge sauber und ohne Rundungsprobleme umgerechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="70c37-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="70c37-132">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="70c37-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="70c37-133">Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="70c37-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="70c37-134">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.</span><span class="sxs-lookup"><span data-stu-id="70c37-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="70c37-135">Wählen Sie auf der Registerkarte **Ladungszeilen** die Ladungszeile für das Element aus, das die Überlieferung überschreitet.</span><span class="sxs-lookup"><span data-stu-id="70c37-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="70c37-136">Wählen Sie **Reduzieren Sie die kommissionierte Menge**, um die kommissionierte Menge anzupassen.</span><span class="sxs-lookup"><span data-stu-id="70c37-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="70c37-137">Wählen Sie auf der Registerkarte  **Zeilendetails** die Option **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="70c37-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="70c37-138">Legen Sie das Feld **Menge** auf die kommissionierte Menge fest (d. h. den Wert des Feldes **Werk erstellte Menge**), damit die Erstellung des Lieferscheins fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="70c37-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="70c37-139">Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="70c37-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="70c37-140">Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und Anpassungen vorzunehmen, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="70c37-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="70c37-141">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="70c37-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="70c37-142">Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="70c37-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="70c37-143">Wählen Sie im Inforegister **Ladungszeilen** die Ladungszeile für das Element, das ein Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="70c37-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="70c37-144">Notieren Sie sich den Wert der Felder **Menge** und **Einheit**.</span><span class="sxs-lookup"><span data-stu-id="70c37-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="70c37-145">Gehen Sie zu **Organisationsverwaltung \> Einheiten \> Einheiten**.</span><span class="sxs-lookup"><span data-stu-id="70c37-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="70c37-146">Wählen Sie die Einheit aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="70c37-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="70c37-147">Passen Sie den Wert des Feldes **Dezimalgenauigkeit** wie gewünscht an.</span><span class="sxs-lookup"><span data-stu-id="70c37-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="70c37-148">Stellen Sie sicher, dass die Maßeinheit des Bestandes kleiner ist als die Maßeinheit des Verkaufs.</span><span class="sxs-lookup"><span data-stu-id="70c37-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="70c37-149">Stellen Sie sicher, dass die Maßeinheit des Bestands kleiner ist als die Maßeinheit des Verkaufs.</span><span class="sxs-lookup"><span data-stu-id="70c37-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="70c37-150">Ziehen Sie in Erwägung, die Maßeinheit für das Element bei Bedarf neu zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="70c37-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
