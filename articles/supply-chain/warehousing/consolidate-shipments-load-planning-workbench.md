---
title: Lieferungen mithilfe von An Lager freigeben von der Ladungsplanungs-Workbench aus konsolidieren
description: In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen in derselben Ladung an das Lager freigegeben werden und anschließend in Lieferungen automatisch konsolidiert werden.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 30824bf1c8e84bab08b6885ee812ed5e3e9937bb
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117180"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="2af07-103">Lieferungen mithilfe von An Lager freigeben von der Ladungsplanungs-Workbench aus konsolidieren</span><span class="sxs-lookup"><span data-stu-id="2af07-103">Consolidate shipments by releasing to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2af07-104">In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen in derselben Ladung an das Lager freigegeben werden und anschließend in Lieferungen automatisch konsolidiert werden.</span><span class="sxs-lookup"><span data-stu-id="2af07-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="2af07-105">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="2af07-105">Make demo data available</span></span>

<span data-ttu-id="2af07-106">Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2af07-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2af07-107">Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="2af07-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="2af07-108">Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein</span><span class="sxs-lookup"><span data-stu-id="2af07-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="2af07-109">In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2af07-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="2af07-110">Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.</span><span class="sxs-lookup"><span data-stu-id="2af07-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="2af07-111">Erstellen Sie die Kundenaufträge für dieses Szenario</span><span class="sxs-lookup"><span data-stu-id="2af07-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="2af07-112">Erstellen Sie zunächst eine Sammlung von Kundenaufträgen, mit denen Sie arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="2af07-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="2af07-113">Sie müssen mit einem Lagerort arbeiten, der für WMS-Prozesse (Advanced Warehouse) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2af07-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="2af07-114">Sofern nicht ausdrücklich ein anderes Lager erwähnt wird, muss dasselbe Lager für jeden der folgenden Auftragssätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2af07-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="2af07-115">Wechseln Sie zu **Debitoren \> Aufträge \> Alle Kundenaufträge**, und erstellen Sie eine Sammlung von Kundenaufträgen mit den Einstellungen, die in den folgenden Unterabschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2af07-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="2af07-116">Auftragssatz 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="2af07-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="2af07-117">Auftrag 1-1</span><span class="sxs-lookup"><span data-stu-id="2af07-117">Sales order 1-1</span></span>

1. <span data-ttu-id="2af07-118">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2af07-119">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2af07-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2af07-120">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2af07-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="2af07-121">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-122">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-123">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-124">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="2af07-125">Auftrag 1-2</span><span class="sxs-lookup"><span data-stu-id="2af07-125">Sales order 1-2</span></span>

1. <span data-ttu-id="2af07-126">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2af07-127">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2af07-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2af07-128">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2af07-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="2af07-129">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-130">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-131">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-132">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="2af07-133">Auftrag 1-3</span><span class="sxs-lookup"><span data-stu-id="2af07-133">Sales order 1-3</span></span>

1. <span data-ttu-id="2af07-134">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2af07-135">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2af07-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2af07-136">**Lieferart:** *10*</span><span class="sxs-lookup"><span data-stu-id="2af07-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="2af07-137">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-138">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-139">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-140">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="2af07-141">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="2af07-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-142">**Artikelnummer:** *A0002* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-143">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="2af07-144">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2af07-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="2af07-145">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die zweite Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="2af07-146">Auftragssatz 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="2af07-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="2af07-147">Aufträge 2-1 und 2-2</span><span class="sxs-lookup"><span data-stu-id="2af07-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="2af07-148">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2af07-149">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="2af07-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="2af07-150">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-151">**Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="2af07-152">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-153">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="2af07-154">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="2af07-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-155">**Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="2af07-156">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="2af07-157">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2af07-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="2af07-158">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die zweite Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="2af07-159">Auftragssatz 3 erstellen</span><span class="sxs-lookup"><span data-stu-id="2af07-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="2af07-160">Aufträge 3-1 und 3-2</span><span class="sxs-lookup"><span data-stu-id="2af07-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="2af07-161">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2af07-162">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2af07-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2af07-163">**Debitorenanforderung:** *1*</span><span class="sxs-lookup"><span data-stu-id="2af07-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="2af07-164">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-165">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-166">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-167">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="2af07-168">Aufträge 3-3 und 3-4</span><span class="sxs-lookup"><span data-stu-id="2af07-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="2af07-169">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2af07-170">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2af07-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2af07-171">**Debitorenanforderung:** *2*</span><span class="sxs-lookup"><span data-stu-id="2af07-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="2af07-172">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-173">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-174">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-175">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="2af07-176">Auftragssatz 4 erstellen</span><span class="sxs-lookup"><span data-stu-id="2af07-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="2af07-177">Aufträge 4-1 und 4-2</span><span class="sxs-lookup"><span data-stu-id="2af07-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="2af07-178">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2af07-179">**Debitorenkonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="2af07-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="2af07-180">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-181">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-182">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-183">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="2af07-184">Aufträge 4-3 und 4-4</span><span class="sxs-lookup"><span data-stu-id="2af07-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="2af07-185">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2af07-186">**Debitorenkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="2af07-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="2af07-187">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-188">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-189">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-190">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="2af07-191">Aufträge 4-5 und 4-6</span><span class="sxs-lookup"><span data-stu-id="2af07-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="2af07-192">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2af07-193">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="2af07-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="2af07-194">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="2af07-194">**Site:** *6*</span></span>
    - <span data-ttu-id="2af07-195">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="2af07-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="2af07-196">**Pool:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="2af07-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="2af07-197">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-198">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-199">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-200">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="2af07-201">Aufträge 4-7 und 4-8</span><span class="sxs-lookup"><span data-stu-id="2af07-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="2af07-202">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2af07-203">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="2af07-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="2af07-204">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="2af07-204">**Site:** *6*</span></span>
    - <span data-ttu-id="2af07-205">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="2af07-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="2af07-206">**Pool:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="2af07-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="2af07-207">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2af07-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2af07-208">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2af07-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2af07-209">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2af07-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2af07-210">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="2af07-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="2af07-211">Verwenden Sie die Ladungsplanungs-Workbench, um Ladungen zu erstellen und an das Lager freizugeben</span><span class="sxs-lookup"><span data-stu-id="2af07-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="2af07-212">Führen Sie die folgenden Schritte aus, um für jeden Auftragssatz, den Sie für dieses Szenario erstellt haben, eine Ladung zu erstellen und diese dann für das Lager freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2af07-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="2af07-213">Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="2af07-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="2af07-214">Suchen Sie auf der Registerkarte **Verkaufspositionen** alle Kundenauftragspositionen, und wählen Sie sie aus einem der Auftragssätze aus, die Sie für dieses Szenario erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2af07-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="2af07-215">Wählen Sie im Aktionsbereich auf der Registerkarte **Angebot und Nachfrage** die Option **Hinzufügen \> An neue Ladung** aus, um die ausgewählten Auftragspositionen zu einer neuen Ladung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2af07-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="2af07-216">Wählen Sie im Dialogfeld **Vorlagenzuordnung** im Feld **Ladungsvorlagen-ID** eine Ladevorlage aus, wie z. B. *Standardladungsvorlage*.</span><span class="sxs-lookup"><span data-stu-id="2af07-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="2af07-217">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="2af07-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="2af07-218">Suchen Sie im Abschnitt **Ladungen** die Ladung, die Sie gerade erstellt haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="2af07-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="2af07-219">Wählen Sie **Freigeben \> An Lager freigeben** aus, um die ausgewählte Ladung an das Lager freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2af07-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="2af07-220">Wiederholen Sie diesen Vorgang für die anderen drei Auftragssätze, die Sie für dieses Szenario erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2af07-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="2af07-221">Überprüfen Sie die Lieferungen</span><span class="sxs-lookup"><span data-stu-id="2af07-221">Verify the shipments</span></span>

<span data-ttu-id="2af07-222">Mit dem folgenden Verfahren können Sie die Lieferungen überprüfen, die als Ergebnis der Lieferungskonsolidierung erstellt oder aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2af07-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="2af07-223">Verwenden Sie diese Option, um jeden Auftragssatz zu überprüfen, den Sie für dieses Szenario erstellt haben, und überprüfen Sie anschließend die folgenden Unterabschnitte, um sicherzustellen, dass Sie die erwarteten Ergebnisse erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="2af07-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="2af07-224">Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.</span><span class="sxs-lookup"><span data-stu-id="2af07-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="2af07-225">Suchen Sie die gewünschte Lieferung und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="2af07-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="2af07-226">Wenn beim Erstellen oder Aktualisieren der Lieferung eine Konsolidierungsrichtlinie verwendet wurde, sollte diese im Feld **Richtlinie für Lieferungskonsolidierung** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2af07-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="2af07-227">Freigabeauftragssatz 1 in einer Ladung</span><span class="sxs-lookup"><span data-stu-id="2af07-227">Release order set 1 in one load</span></span>

<span data-ttu-id="2af07-228">Es sollten zwei Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="2af07-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="2af07-229">Die erste Lieferung enthält drei Zeilen und wurde mit der *CustomerMode*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="2af07-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="2af07-230">Die zweite Lieferung, die nicht *Airways* als Transportart der Lieferung verwendet, wurde unter Verwendung der *CustomerOrderNo*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="2af07-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="2af07-231">Freigabeauftragssatz 2 in einer Ladung</span><span class="sxs-lookup"><span data-stu-id="2af07-231">Release order set 2 in one load</span></span>

<span data-ttu-id="2af07-232">Es sollten drei Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="2af07-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="2af07-233">Die erste Lieferung enthält die *Brennbar*-Artikel.</span><span class="sxs-lookup"><span data-stu-id="2af07-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="2af07-234">Jede der beiden anderen Lieferungen enthält eine Position mit dem *Explosiv*-Artikel.</span><span class="sxs-lookup"><span data-stu-id="2af07-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="2af07-235">Freigabeauftragssatz 3 in einer Ladung</span><span class="sxs-lookup"><span data-stu-id="2af07-235">Release order set 3 in one load</span></span>

<span data-ttu-id="2af07-236">Es sollten zwei Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="2af07-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="2af07-237">Die erste Lieferung enthält Bestellpositionen aus dem Auftrag, in dem das **Debitorenanforderung**-Feld auf *1* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="2af07-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="2af07-238">Die zweite Lieferung enthält Bestellpositionen aus dem Auftrag, in dem das **Debitorenanforderung**-Feld auf *2* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="2af07-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="2af07-239">Freigabeauftragssatz 4 in einer Ladung</span><span class="sxs-lookup"><span data-stu-id="2af07-239">Release order set 4 in one load</span></span>

<span data-ttu-id="2af07-240">Es sollten vier Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="2af07-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="2af07-241">Positionen aus zwei Bestellungen für Debitorenkonto *US-003* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2af07-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="2af07-242">Positionen aus zwei Bestellungen für Debitorenkonto *US-004* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2af07-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="2af07-243">Positionen aus aus den Aufträgen 4-5 und 4-6 für Debitorenkonto *US-007* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2af07-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="2af07-244">Positionen aus aus den Aufträgen 4-7 und 4-8 für Debitorenkonto *US-007* wurden unter Verwendung der *CrossOrder*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2af07-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2af07-245">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2af07-245">Additional resources</span></span>

- [<span data-ttu-id="2af07-246">Lieferungskonsolidierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="2af07-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="2af07-247">Richtlinien zur Lieferungskonsolidierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2af07-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]