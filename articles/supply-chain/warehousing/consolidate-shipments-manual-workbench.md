---
title: Lieferungen mithilfe der Workbench zur Lieferungskonsolidierung konsolidieren
description: In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen an das Lager freigegeben werden und anschließend mit der Workbench zur Lieferungskonsolidierung später in Lieferungen automatisch konsolidiert werden.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9d0a2671e18603f701d343a4150128a04c626952
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963384"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="e60e6-103">Lieferungen mithilfe der Workbench zur Lieferungskonsolidierung konsolidieren</span><span class="sxs-lookup"><span data-stu-id="e60e6-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e60e6-104">In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen an das Lager freigegeben werden und anschließend mit der Workbench zur Lieferungskonsolidierung später in Lieferungen automatisch konsolidiert werden.</span><span class="sxs-lookup"><span data-stu-id="e60e6-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="e60e6-105">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="e60e6-105">Make demo data available</span></span>

<span data-ttu-id="e60e6-106">Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e60e6-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e60e6-107">Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="e60e6-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="e60e6-108">Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein</span><span class="sxs-lookup"><span data-stu-id="e60e6-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="e60e6-109">In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e60e6-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="e60e6-110">Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="e60e6-111">Manuelle Lieferungskonsolidierung aktivieren</span><span class="sxs-lookup"><span data-stu-id="e60e6-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="e60e6-112">Bevor Sie die Funktion *Manuelle Lieferungskonsolidierung* verwenden können, müssen Sie sie in Ihrem System aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="e60e6-113">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e60e6-114">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="e60e6-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e60e6-115">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="e60e6-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e60e6-116">**Funktionsname:** *Manuelle Lieferungskonsolidierung*</span><span class="sxs-lookup"><span data-stu-id="e60e6-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="e60e6-117">Wie unter [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) erwähnt, müssen Sie auch die *Lieferung konsolidieren*-Funktion einschalten, bevor Sie Richtlinien erstellen können.</span><span class="sxs-lookup"><span data-stu-id="e60e6-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="e60e6-118">Sie sollten diesen Schritt jedoch bereits abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="e60e6-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="e60e6-119">Erstellen Sie die Kundenaufträge für dieses Szenario</span><span class="sxs-lookup"><span data-stu-id="e60e6-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="e60e6-120">Erstellen Sie zunächst eine Sammlung von Kundenaufträgen, mit denen Sie arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="e60e6-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="e60e6-121">Sie müssen mit einem Lagerort arbeiten, der für WMS-Prozesse (Advanced Warehouse) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e60e6-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="e60e6-122">Sofern nicht ausdrücklich ein anderes Lager erwähnt wird, muss dasselbe Lager für jeden der folgenden Auftragssätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e60e6-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="e60e6-123">Wechseln Sie zu **Debitoren \> Aufträge \> Alle Kundenaufträge**, und erstellen Sie eine Sammlung von Kundenaufträgen mit den Einstellungen, die in den folgenden Unterabschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e60e6-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="e60e6-124">Auftragssatz 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="e60e6-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="e60e6-125">Aufträge 1-1 und 1-2</span><span class="sxs-lookup"><span data-stu-id="e60e6-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="e60e6-126">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e60e6-127">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e60e6-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e60e6-128">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="e60e6-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e60e6-129">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-130">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-131">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-132">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="e60e6-133">Auftrag 1-3</span><span class="sxs-lookup"><span data-stu-id="e60e6-133">Sales order 1-3</span></span>

1. <span data-ttu-id="e60e6-134">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-135">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e60e6-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e60e6-136">**Lieferart:** *10*</span><span class="sxs-lookup"><span data-stu-id="e60e6-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="e60e6-137">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-138">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-139">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-140">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="e60e6-141">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e60e6-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-142">**Artikelnummer:** *A0002* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-143">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="e60e6-144">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="e60e6-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e60e6-145">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die zweite Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="e60e6-146">Auftragssatz 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="e60e6-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="e60e6-147">Aufträge 2-1 und 2-2</span><span class="sxs-lookup"><span data-stu-id="e60e6-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="e60e6-148">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e60e6-149">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="e60e6-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="e60e6-150">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="e60e6-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e60e6-151">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-152">**Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="e60e6-153">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-154">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="e60e6-155">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e60e6-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-156">**Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="e60e6-157">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="e60e6-158">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="e60e6-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e60e6-159">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die zweite Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="e60e6-160">Auftragssatz 3 erstellen</span><span class="sxs-lookup"><span data-stu-id="e60e6-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="e60e6-161">Aufträge 3-1 und 3-2</span><span class="sxs-lookup"><span data-stu-id="e60e6-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="e60e6-162">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e60e6-163">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e60e6-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e60e6-164">**Debitorenanforderung:** *1*</span><span class="sxs-lookup"><span data-stu-id="e60e6-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="e60e6-165">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-166">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-167">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-168">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="e60e6-169">Aufträge 3-3 und 3-4</span><span class="sxs-lookup"><span data-stu-id="e60e6-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="e60e6-170">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e60e6-171">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e60e6-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e60e6-172">**Debitorenanforderung:** *2*</span><span class="sxs-lookup"><span data-stu-id="e60e6-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="e60e6-173">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-174">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-175">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-176">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="e60e6-177">Auftragssatz 4 erstellen</span><span class="sxs-lookup"><span data-stu-id="e60e6-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="e60e6-178">Aufträge 4-1 und 4-2</span><span class="sxs-lookup"><span data-stu-id="e60e6-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="e60e6-179">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e60e6-180">**Debitorenkonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="e60e6-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="e60e6-181">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-182">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-183">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-184">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="e60e6-185">Aufträge 4-3 und 4-4</span><span class="sxs-lookup"><span data-stu-id="e60e6-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="e60e6-186">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e60e6-187">**Debitorenkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="e60e6-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="e60e6-188">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-189">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-190">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-191">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="e60e6-192">Aufträge 4-5 und 4-6</span><span class="sxs-lookup"><span data-stu-id="e60e6-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="e60e6-193">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e60e6-194">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="e60e6-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e60e6-195">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="e60e6-195">**Site:** *6*</span></span>
    - <span data-ttu-id="e60e6-196">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="e60e6-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="e60e6-197">**Pool:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="e60e6-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="e60e6-198">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-199">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-200">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-201">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="e60e6-202">Aufträge 4-7 und 4-8</span><span class="sxs-lookup"><span data-stu-id="e60e6-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="e60e6-203">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e60e6-204">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="e60e6-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e60e6-205">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="e60e6-205">**Site:** *6*</span></span>
    - <span data-ttu-id="e60e6-206">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="e60e6-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="e60e6-207">**Pool:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="e60e6-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="e60e6-208">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e60e6-209">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="e60e6-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e60e6-210">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e60e6-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e60e6-211">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e60e6-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="e60e6-212">Aufträge für den Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="e60e6-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="e60e6-213">Führen Sie die folgenden Schritte aus, um jeden Auftrag, den Sie für dieses Szenario erstellt haben, für das Lager freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e60e6-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="e60e6-214">Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="e60e6-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e60e6-215">Suchen und wählen Sie den freizugebenden Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="e60e6-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="e60e6-216">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten \> Für Lagerort freigeben**, um die ausgewählten Aufträge freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e60e6-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="e60e6-217">Wiederholen Sie diesen Vorgang für alle anderen Aufträge, die Sie für dieses Szenario erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e60e6-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="e60e6-218">Lieferungen mithilfe der Workbench zur Lieferungskonsolidierung konsolidieren</span><span class="sxs-lookup"><span data-stu-id="e60e6-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="e60e6-219">Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> Lieferungskonsolidierungs-Workbench**.</span><span class="sxs-lookup"><span data-stu-id="e60e6-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="e60e6-220">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e60e6-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e60e6-221">Wählen Sie im Abfrageeditor-Dialogfeld auf der Registerkarte **Bereich** **Hinzufügen** aus, um eine Zeile mit den folgenden Einstellungen zum Raster hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="e60e6-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="e60e6-222">**Tabelle:** *Aufträge*</span><span class="sxs-lookup"><span data-stu-id="e60e6-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="e60e6-223">**Feld:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="e60e6-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="e60e6-224">**Kriterien:** Geben Sie eine durch Kommas getrennte Liste der Auftragsnummern für jeden Auftragssatz ein, den Sie für dieses Szenario erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e60e6-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="e60e6-225">Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e60e6-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="e60e6-226">Wählen Sie im Aktionsbereich **Lieferungen konsolidieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e60e6-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="e60e6-227">Wählen Sie alle Lieferungen und dann im Aktionsbereich **Konsolidieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e60e6-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="e60e6-228">Überprüfen Sie die Lieferungen</span><span class="sxs-lookup"><span data-stu-id="e60e6-228">Verify the shipments</span></span>

<span data-ttu-id="e60e6-229">Mit dem folgenden Verfahren können Sie die Lieferungen überprüfen, die als Ergebnis der Lieferungskonsolidierung erstellt oder aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e60e6-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="e60e6-230">Verwenden Sie diese Option, um jeden Auftragssatz zu überprüfen, den Sie für dieses Szenario erstellt haben, und überprüfen Sie anschließend die folgenden Unterabschnitte, um sicherzustellen, dass Sie die erwarteten Ergebnisse erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="e60e6-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="e60e6-231">Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.</span><span class="sxs-lookup"><span data-stu-id="e60e6-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="e60e6-232">Suchen Sie die gewünschte Lieferung und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="e60e6-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="e60e6-233">Wenn beim Erstellen oder Aktualisieren der Lieferung eine Konsolidierungsrichtlinie verwendet wurde, sollte diese im Feld **Richtlinie für Lieferungskonsolidierung** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e60e6-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="e60e6-234">Verwandte Lieferungen für Auftragssatz 1</span><span class="sxs-lookup"><span data-stu-id="e60e6-234">Related shipments for order set 1</span></span>

<span data-ttu-id="e60e6-235">Es sollten zwei Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="e60e6-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="e60e6-236">Die erste Lieferung enthält drei Zeilen und wurde mit der *CustomerMode*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="e60e6-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="e60e6-237">Die zweite Lieferung, die nicht *Airways* als Transportart der Lieferung verwendet, wurde unter Verwendung der *CustomerOrderNo*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="e60e6-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="e60e6-238">Verwandte Lieferungen für Auftragssatz 2</span><span class="sxs-lookup"><span data-stu-id="e60e6-238">Related shipments for order set 2</span></span>

<span data-ttu-id="e60e6-239">Es sollten drei Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="e60e6-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="e60e6-240">Die erste Lieferung enthält die *Brennbar*-Artikel.</span><span class="sxs-lookup"><span data-stu-id="e60e6-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="e60e6-241">Jede der beiden anderen Lieferungen enthält eine Position mit dem *Explosiv*-Artikel.</span><span class="sxs-lookup"><span data-stu-id="e60e6-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="e60e6-242">Verwandte Lieferungen für Auftragssatz 3</span><span class="sxs-lookup"><span data-stu-id="e60e6-242">Related shipments for order set 3</span></span>

<span data-ttu-id="e60e6-243">Es sollten zwei Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="e60e6-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="e60e6-244">Die erste Lieferung enthält Bestellpositionen aus dem Auftrag, in dem das **Debitorenanforderung**-Feld auf *1* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="e60e6-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="e60e6-245">Die zweite Lieferung enthält Bestellpositionen aus dem Auftrag, in dem das **Debitorenanforderung**-Feld auf *2* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="e60e6-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="e60e6-246">Verwandte Lieferungen für Auftragssatz 4</span><span class="sxs-lookup"><span data-stu-id="e60e6-246">Related shipments for order set 4</span></span>

<span data-ttu-id="e60e6-247">Es sollten vier Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="e60e6-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="e60e6-248">Positionen aus zwei Bestellungen für Debitor *US-003* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e60e6-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e60e6-249">Positionen aus zwei Bestellungen für Debitor *US-004* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e60e6-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e60e6-250">Positionen aus aus den Aufträgen 4-5 und 4-6 für Debitor *US-007* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e60e6-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e60e6-251">Positionen aus aus den Aufträgen 4-7 und 4-8 für Debitor *US-007* wurden unter Verwendung der *CrossOrder*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e60e6-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e60e6-252">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e60e6-252">Additional resources</span></span>

- [<span data-ttu-id="e60e6-253">Lieferungskonsolidierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="e60e6-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="e60e6-254">Richtlinien zur Lieferungskonsolidierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e60e6-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
