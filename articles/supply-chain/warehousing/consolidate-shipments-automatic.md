---
title: Lieferungen mithilfe der automatischen Auftragsfreigabe konsolidieren, wenn sie im Lager freigegeben werden
description: In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen in derselben automatisierten periodischen Freigabe an das Lager freigegeben werden.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: c02c8b4cd43e17d6dcf34e1912dbc68c19e60694
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116950"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a><span data-ttu-id="2b51a-103">Lieferungen mithilfe der automatischen Auftragsfreigabe konsolidieren, wenn sie im Lager freigegeben werden</span><span class="sxs-lookup"><span data-stu-id="2b51a-103">Consolidate shipments released to the warehouse using automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b51a-104">In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen in derselben automatisierten periodischen Freigabe an das Lager freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2b51a-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="2b51a-105">Die Bestellungen werden automatisch in Lieferungen konsolidiert, basierend auf Regeln, die als Richtlinien zur Lieferungskonsolidierung definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2b51a-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="2b51a-106">Während des Szenarios erstellen Sie Sätze von Kundenaufträgen und geben jeden Satz an das Lager frei.</span><span class="sxs-lookup"><span data-stu-id="2b51a-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="2b51a-107">Anschließend überprüfen Sie die Lieferungen, die während der Lieferungskonsolidierung erstellt oder aktualisiert werden, basierend auf den konfigurierten Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="2b51a-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="2b51a-108">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="2b51a-108">Make demo data available</span></span>

<span data-ttu-id="2b51a-109">Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2b51a-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2b51a-110">Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="2b51a-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="2b51a-111">Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein</span><span class="sxs-lookup"><span data-stu-id="2b51a-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="2b51a-112">In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2b51a-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="2b51a-113">Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.</span><span class="sxs-lookup"><span data-stu-id="2b51a-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="2b51a-114">Erstellen Sie die Kundenaufträge für dieses Szenario</span><span class="sxs-lookup"><span data-stu-id="2b51a-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="2b51a-115">Erstellen Sie zunächst eine Sammlung von Kundenaufträgen, mit denen Sie arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="2b51a-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="2b51a-116">Sie müssen mit einem Lagerort arbeiten, der für WMS-Prozesse (Advanced Warehouse) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2b51a-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="2b51a-117">Sofern nicht ausdrücklich ein anderes Lager erwähnt wird, muss dasselbe Lager für jeden der folgenden Auftragssätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b51a-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="2b51a-118">Wechseln Sie zu **Debitoren \> Aufträge \> Alle Kundenaufträge**, und erstellen Sie eine Sammlung von Kundenaufträgen mit den Einstellungen, die in den folgenden Unterabschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2b51a-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="2b51a-119">Auftragssatz 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="2b51a-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="2b51a-120">Auftrag 1-1</span><span class="sxs-lookup"><span data-stu-id="2b51a-120">Sales order 1-1</span></span>

1. <span data-ttu-id="2b51a-121">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-122">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2b51a-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2b51a-123">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2b51a-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="2b51a-124">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-125">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-126">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="2b51a-127">Auftrag 1-2</span><span class="sxs-lookup"><span data-stu-id="2b51a-127">Sales order 1-2</span></span>

1. <span data-ttu-id="2b51a-128">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-129">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2b51a-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2b51a-130">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2b51a-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="2b51a-131">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-132">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-133">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="2b51a-134">Auftrag 1-3</span><span class="sxs-lookup"><span data-stu-id="2b51a-134">Sales order 1-3</span></span>

1. <span data-ttu-id="2b51a-135">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-136">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2b51a-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2b51a-137">**Lieferart:** *10*</span><span class="sxs-lookup"><span data-stu-id="2b51a-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="2b51a-138">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-139">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-140">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2b51a-141">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="2b51a-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-142">**Artikelnummer:** *A0002* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-143">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="2b51a-144">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2b51a-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="2b51a-145">Auftragssatz 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="2b51a-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="2b51a-146">Aufträge 2-1 und 2-2</span><span class="sxs-lookup"><span data-stu-id="2b51a-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="2b51a-147">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2b51a-148">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="2b51a-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="2b51a-149">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-150">**Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="2b51a-151">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2b51a-152">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="2b51a-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-153">**Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="2b51a-154">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="2b51a-155">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2b51a-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="2b51a-156">Auftragssatz 3 erstellen</span><span class="sxs-lookup"><span data-stu-id="2b51a-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="2b51a-157">Auftrag 3-1</span><span class="sxs-lookup"><span data-stu-id="2b51a-157">Sales order 3-1</span></span>

1. <span data-ttu-id="2b51a-158">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-159">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="2b51a-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="2b51a-160">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-161">**Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="2b51a-162">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="2b51a-163">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="2b51a-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-164">**Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="2b51a-165">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="2b51a-166">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="2b51a-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="2b51a-167">Diese Bestellung ist identisch mit den beiden Bestellungen, die Sie für Auftragssatz 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2b51a-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="2b51a-168">Es wird jedoch als eigener Auftragssatz aufgeführt, da Sie ihn später in diesem Szenario separat freigeben werden.</span><span class="sxs-lookup"><span data-stu-id="2b51a-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="2b51a-169">Auftragssatz 4 erstellen</span><span class="sxs-lookup"><span data-stu-id="2b51a-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="2b51a-170">Auftrag 4-1</span><span class="sxs-lookup"><span data-stu-id="2b51a-170">Sales order 4-1</span></span>

1. <span data-ttu-id="2b51a-171">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-172">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2b51a-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2b51a-173">**Debitorenanforderung:** *1*</span><span class="sxs-lookup"><span data-stu-id="2b51a-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="2b51a-174">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-175">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-176">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="2b51a-177">Auftragssatz 5 erstellen</span><span class="sxs-lookup"><span data-stu-id="2b51a-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="2b51a-178">Aufträge 5-1 und 5-2</span><span class="sxs-lookup"><span data-stu-id="2b51a-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="2b51a-179">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2b51a-180">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2b51a-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2b51a-181">**Debitorenanforderung:** *2*</span><span class="sxs-lookup"><span data-stu-id="2b51a-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="2b51a-182">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-183">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-184">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="2b51a-185">Auftrag 5-3</span><span class="sxs-lookup"><span data-stu-id="2b51a-185">Sales order 5-3</span></span>

1. <span data-ttu-id="2b51a-186">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-187">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2b51a-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2b51a-188">**Debitorenanforderung:** *1*</span><span class="sxs-lookup"><span data-stu-id="2b51a-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="2b51a-189">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-190">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-191">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="2b51a-192">Auftragssatz 6 erstellen</span><span class="sxs-lookup"><span data-stu-id="2b51a-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="2b51a-193">Aufträge 6-1 und 6-2</span><span class="sxs-lookup"><span data-stu-id="2b51a-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="2b51a-194">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2b51a-195">**Debitorenkonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="2b51a-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="2b51a-196">**Debitorenanforderung:** *2*</span><span class="sxs-lookup"><span data-stu-id="2b51a-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="2b51a-197">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-198">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-199">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="2b51a-200">Aufträge 6-3 und 6-4</span><span class="sxs-lookup"><span data-stu-id="2b51a-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="2b51a-201">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2b51a-202">**Debitorenkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="2b51a-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="2b51a-203">**Debitorenanforderung:** *1*</span><span class="sxs-lookup"><span data-stu-id="2b51a-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="2b51a-204">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-205">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-206">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="2b51a-207">Aufträge 6-5 und 6-6</span><span class="sxs-lookup"><span data-stu-id="2b51a-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="2b51a-208">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2b51a-209">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="2b51a-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="2b51a-210">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="2b51a-210">**Site:** *6*</span></span>
    - <span data-ttu-id="2b51a-211">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="2b51a-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="2b51a-212">**Pool:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="2b51a-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="2b51a-213">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-214">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-215">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="2b51a-216">Aufträge 6-7 und 6-8</span><span class="sxs-lookup"><span data-stu-id="2b51a-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="2b51a-217">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="2b51a-218">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="2b51a-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="2b51a-219">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="2b51a-219">**Site:** *6*</span></span>
    - <span data-ttu-id="2b51a-220">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="2b51a-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="2b51a-221">**Pool:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="2b51a-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="2b51a-222">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="2b51a-223">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="2b51a-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="2b51a-224">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="2b51a-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="2b51a-225">Automatische Freigabe von Aufträgen für den Lagerort</span><span class="sxs-lookup"><span data-stu-id="2b51a-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="2b51a-226">Für jeden Satz von Kundenaufträgen, den Sie zuvor erstellt haben, führen Sie einen Vorgang für die automatische Freigabe an das Lager durch.</span><span class="sxs-lookup"><span data-stu-id="2b51a-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="2b51a-227">In jedem Fall werden Sie [grundlegende Verfahren für die Freigabe an das Lager](#release-procedure) durcharbeiten, die hier beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="2b51a-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="2b51a-228">Grundlegendes Lagerfreigabeverfahren</span><span class="sxs-lookup"><span data-stu-id="2b51a-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="2b51a-229">Für jeden Satz von Kundenaufträgen, den Sie zuvor erstellt haben, führen Sie die drei in den folgenden Unterabschnitten beschriebenen Verfahren aus.</span><span class="sxs-lookup"><span data-stu-id="2b51a-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="2b51a-230">Aktualisieren Sie die Wellenvorlage, die während der Veröffentlichung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2b51a-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="2b51a-231">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="2b51a-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="2b51a-232">Stellen Sie das Feld **Wellenvorlagentyp** auf *Versand* ein.</span><span class="sxs-lookup"><span data-stu-id="2b51a-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="2b51a-233">Suchen Sie die Wellenvorlage, die dem Lager zugeordnet ist, das Sie in den Auftragssätzen verwendet haben, die Sie für dieses Szenario erstellt haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="2b51a-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="2b51a-234">Zum Beispiel, wenn Sie ein Lager *24* verwendet haben, wählen Sie **Standard-24-Lieferung**-Wellenvorlage.</span><span class="sxs-lookup"><span data-stu-id="2b51a-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="2b51a-235">Wenn Sie ein Lager *61* verwendet haben, wählen Sie die **61-Lieferung**-Wellenvorlage.</span><span class="sxs-lookup"><span data-stu-id="2b51a-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="2b51a-236">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2b51a-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2b51a-237">Legen Sie die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Nein* fest.</span><span class="sxs-lookup"><span data-stu-id="2b51a-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="2b51a-238">Für Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="2b51a-238">Release to the warehouse</span></span>

1. <span data-ttu-id="2b51a-239">Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> Automatische Freigabe von Aufträgen für den Lagerort**.</span><span class="sxs-lookup"><span data-stu-id="2b51a-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="2b51a-240">Stellen Sie die **Freizugebende Menge** auf *Alle* ein.</span><span class="sxs-lookup"><span data-stu-id="2b51a-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="2b51a-241">Wählen Sie auf dem Inforegister **Aufzeichnungen enthalten** **Filter** aus, um das Abfragedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2b51a-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="2b51a-242">Wählen Sie auf der Registerkarte **Bereich** **Hinzufügen** aus, um eine Zeile mit den folgenden Einstellungen zum Raster hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="2b51a-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="2b51a-243">**Tabelle:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="2b51a-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="2b51a-244">**Abgeleitete Tabelle:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="2b51a-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="2b51a-245">**Feld:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="2b51a-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="2b51a-246">**Kriterien:** Geben Sie eine durch Kommas getrennte Liste der Kundenauftragsnummern aus dem gewünschten Auftragssatz ein.</span><span class="sxs-lookup"><span data-stu-id="2b51a-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="2b51a-247">Wählen Sie **OK** aus, um Ihre Anfrage zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2b51a-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="2b51a-248">Wählen Sie **OK** aus, um das Verfahren *Automatische Freigabe an das Lager* zu starten.</span><span class="sxs-lookup"><span data-stu-id="2b51a-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="2b51a-249">Überprüfen Sie die Lieferung, die erstellt oder aktualisiert wurde</span><span class="sxs-lookup"><span data-stu-id="2b51a-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="2b51a-250">Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.</span><span class="sxs-lookup"><span data-stu-id="2b51a-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="2b51a-251">Suchen Sie die gewünschte Lieferung und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="2b51a-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="2b51a-252">Wenn beim Erstellen oder Aktualisieren der Lieferung eine Konsolidierungsrichtlinie verwendet wurde, sollte diese im Feld **Richtlinie für Lieferungskonsolidierung** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2b51a-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="2b51a-253">Kundenaufträge aus Auftragssatz 1 freigeben</span><span class="sxs-lookup"><span data-stu-id="2b51a-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="2b51a-254">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 1 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2b51a-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="2b51a-255">Wenn Sie fertig sind, sollten Sie sehen, dass zwei Lieferungen erstellt wurden:</span><span class="sxs-lookup"><span data-stu-id="2b51a-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="2b51a-256">Die erste Lieferung enthält drei Zeilen und wurde mit der *CustomerMode*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b51a-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="2b51a-257">Die zweite Lieferung, die nicht *Airways* als Transportart der Lieferung verwendet, wurde unter Verwendung der *CustomerOrderNo*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b51a-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="2b51a-258">Kundenaufträge aus Auftragssatz 2 freigeben</span><span class="sxs-lookup"><span data-stu-id="2b51a-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="2b51a-259">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 2 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2b51a-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="2b51a-260">Wenn Sie fertig sind, sollten Sie sehen, dass drei Lieferungen erstellt wurden:</span><span class="sxs-lookup"><span data-stu-id="2b51a-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="2b51a-261">Die erste Lieferung enthält die *Brennbar*-Artikel.</span><span class="sxs-lookup"><span data-stu-id="2b51a-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="2b51a-262">Jede der beiden anderen Lieferungen enthält eine Position mit dem *Explosiv*-Artikel.</span><span class="sxs-lookup"><span data-stu-id="2b51a-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="2b51a-263">Kundenaufträge aus Auftragssatz 3 freigeben</span><span class="sxs-lookup"><span data-stu-id="2b51a-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="2b51a-264">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 3 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2b51a-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="2b51a-265">Wenn Sie fertig sind, sollten Sie sehen, dass die folgenden Aktionen ausgeführt wurden:</span><span class="sxs-lookup"><span data-stu-id="2b51a-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="2b51a-266">Eine vorhandene Lieferung (die Lieferung, die erstellt wurde, als Auftragssatz 2 für das Lager freigegeben wurde) wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2b51a-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="2b51a-267">Eine Zeile mit dem *Brennbar*-Artikel wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2b51a-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="2b51a-268">Es wurde eine neue Lieferung erstellt, die die *Explosiv*-Artikel enthält.</span><span class="sxs-lookup"><span data-stu-id="2b51a-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="2b51a-269">Kundenaufträge aus Auftragssatz 4 freigeben</span><span class="sxs-lookup"><span data-stu-id="2b51a-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="2b51a-270">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 4 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2b51a-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="2b51a-271">Wenn Sie fertig sind, sollten Sie sehen, dass eine vorhandene Lieferung (wo das **Debitorenanforderung**-Feld auf *1* gesetzt ist) aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2b51a-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="2b51a-272">Eine neue Zeile wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2b51a-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="2b51a-273">Kundenaufträge aus Auftragssatz 5 freigeben</span><span class="sxs-lookup"><span data-stu-id="2b51a-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="2b51a-274">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 5 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2b51a-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="2b51a-275">Wenn Sie fertig sind, sollten Sie sehen, dass die folgenden Aktionen ausgeführt wurden:</span><span class="sxs-lookup"><span data-stu-id="2b51a-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="2b51a-276">Eine vorhandene Lieferung (wo das **Debitorenanforderung**-Feld auf *1* gesetzt ist) wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2b51a-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="2b51a-277">Eine Zeile aus Kundenauftrag 5-3 (wo das **Kundenanforderung**-Feld auf *1* gesetzt ist) wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2b51a-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="2b51a-278">Eine neue Lieferung wurde erstellt, in der die Zeilen aus den Kundenaufträgen 5-1 und 5-2 zu einer Lieferung zusammengefasst sind.</span><span class="sxs-lookup"><span data-stu-id="2b51a-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="2b51a-279">Kundenaufträge aus Auftragssatz 6 freigeben</span><span class="sxs-lookup"><span data-stu-id="2b51a-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="2b51a-280">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 6 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2b51a-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="2b51a-281">Wenn Sie fertig sind, sollten Sie sehen, dass vier Lieferungen erstellt wurden:</span><span class="sxs-lookup"><span data-stu-id="2b51a-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="2b51a-282">Positionen aus zwei Bestellungen für Debitor *US-003* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2b51a-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="2b51a-283">Positionen aus zwei Bestellungen für Debitor *US-004* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2b51a-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="2b51a-284">Positionen aus aus den Aufträgen 6-5 und 6-6 für Debitor *US-007* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2b51a-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="2b51a-285">Positionen aus aus den Aufträgen 6-7 und 6-8 für Debitor *US-007* wurden unter Verwendung der *CrossOrder*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2b51a-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b51a-286">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2b51a-286">Additional resources</span></span>

- [<span data-ttu-id="2b51a-287">Lieferungskonsolidierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="2b51a-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="2b51a-288">Richtlinien zur Lieferungskonsolidierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2b51a-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]