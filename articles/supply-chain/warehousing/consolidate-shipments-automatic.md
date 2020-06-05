---
title: Lieferungen mithilfe der automatischen Auftragsfreigabe konsolidieren, wenn sie im Lager freigegeben werden
description: In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen in derselben automatisierten periodischen Freigabe an das Lager freigegeben werden.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 373b6bf6219ef76bacef3c67a816aec4c084c405
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383775"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="b6cb1-103">Lieferungen mithilfe der automatischen Auftragsfreigabe konsolidieren, wenn sie im Lager freigegeben werden</span><span class="sxs-lookup"><span data-stu-id="b6cb1-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6cb1-104">In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen in derselben automatisierten periodischen Freigabe an das Lager freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="b6cb1-105">Die Bestellungen werden automatisch in Lieferungen konsolidiert, basierend auf Regeln, die als Richtlinien zur Lieferungskonsolidierung definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="b6cb1-106">Während des Szenarios erstellen Sie Sätze von Kundenaufträgen und geben jeden Satz an das Lager frei.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="b6cb1-107">Anschließend überprüfen Sie die Lieferungen, die während der Lieferungskonsolidierung erstellt oder aktualisiert werden, basierend auf den konfigurierten Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="b6cb1-108">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="b6cb1-108">Make demo data available</span></span>

<span data-ttu-id="b6cb1-109">Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b6cb1-110">Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="b6cb1-111">Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein</span><span class="sxs-lookup"><span data-stu-id="b6cb1-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="b6cb1-112">In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="b6cb1-113">Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="b6cb1-114">Erstellen Sie die Kundenaufträge für dieses Szenario</span><span class="sxs-lookup"><span data-stu-id="b6cb1-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="b6cb1-115">Erstellen Sie zunächst eine Sammlung von Kundenaufträgen, mit denen Sie arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="b6cb1-116">Sie müssen mit einem Lagerort arbeiten, der für WMS-Prozesse (Advanced Warehouse) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="b6cb1-117">Sofern nicht ausdrücklich ein anderes Lager erwähnt wird, muss dasselbe Lager für jeden der folgenden Auftragssätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="b6cb1-118">Wechseln Sie zu **Debitoren \> Aufträge \> Alle Kundenaufträge**, und erstellen Sie eine Sammlung von Kundenaufträgen mit den Einstellungen, die in den folgenden Unterabschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="b6cb1-119">Auftragssatz 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="b6cb1-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="b6cb1-120">Auftrag 1-1</span><span class="sxs-lookup"><span data-stu-id="b6cb1-120">Sales order 1-1</span></span>

1. <span data-ttu-id="b6cb1-121">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-122">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6cb1-123">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b6cb1-124">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-125">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-126">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="b6cb1-127">Auftrag 1-2</span><span class="sxs-lookup"><span data-stu-id="b6cb1-127">Sales order 1-2</span></span>

1. <span data-ttu-id="b6cb1-128">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-129">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6cb1-130">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b6cb1-131">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-132">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-133">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="b6cb1-134">Auftrag 1-3</span><span class="sxs-lookup"><span data-stu-id="b6cb1-134">Sales order 1-3</span></span>

1. <span data-ttu-id="b6cb1-135">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-136">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6cb1-137">**Lieferart:** *10*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="b6cb1-138">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-139">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-140">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b6cb1-141">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-142">**Artikelnummer:** *A0002* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-143">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b6cb1-144">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="b6cb1-145">Auftragssatz 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="b6cb1-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="b6cb1-146">Aufträge 2-1 und 2-2</span><span class="sxs-lookup"><span data-stu-id="b6cb1-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="b6cb1-147">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b6cb1-148">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="b6cb1-149">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-150">**Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="b6cb1-151">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b6cb1-152">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-153">**Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="b6cb1-154">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b6cb1-155">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="b6cb1-156">Auftragssatz 3 erstellen</span><span class="sxs-lookup"><span data-stu-id="b6cb1-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="b6cb1-157">Auftrag 3-1</span><span class="sxs-lookup"><span data-stu-id="b6cb1-157">Sales order 3-1</span></span>

1. <span data-ttu-id="b6cb1-158">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-159">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="b6cb1-160">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-161">**Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="b6cb1-162">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b6cb1-163">Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-164">**Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="b6cb1-165">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b6cb1-166">**Lieferart:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="b6cb1-167">Diese Bestellung ist identisch mit den beiden Bestellungen, die Sie für Auftragssatz 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="b6cb1-168">Es wird jedoch als eigener Auftragssatz aufgeführt, da Sie ihn später in diesem Szenario separat freigeben werden.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="b6cb1-169">Auftragssatz 4 erstellen</span><span class="sxs-lookup"><span data-stu-id="b6cb1-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="b6cb1-170">Auftrag 4-1</span><span class="sxs-lookup"><span data-stu-id="b6cb1-170">Sales order 4-1</span></span>

1. <span data-ttu-id="b6cb1-171">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-172">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6cb1-173">**Debitorenanforderung:** *1*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b6cb1-174">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-175">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-176">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="b6cb1-177">Auftragssatz 5 erstellen</span><span class="sxs-lookup"><span data-stu-id="b6cb1-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="b6cb1-178">Aufträge 5-1 und 5-2</span><span class="sxs-lookup"><span data-stu-id="b6cb1-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="b6cb1-179">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b6cb1-180">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6cb1-181">**Debitorenanforderung:** *2*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="b6cb1-182">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-183">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-184">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="b6cb1-185">Auftrag 5-3</span><span class="sxs-lookup"><span data-stu-id="b6cb1-185">Sales order 5-3</span></span>

1. <span data-ttu-id="b6cb1-186">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-187">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6cb1-188">**Debitorenanforderung:** *1*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b6cb1-189">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-190">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-191">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="b6cb1-192">Auftragssatz 6 erstellen</span><span class="sxs-lookup"><span data-stu-id="b6cb1-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="b6cb1-193">Aufträge 6-1 und 6-2</span><span class="sxs-lookup"><span data-stu-id="b6cb1-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="b6cb1-194">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b6cb1-195">**Debitorenkonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="b6cb1-196">**Debitorenanforderung:** *2*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="b6cb1-197">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-198">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-199">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="b6cb1-200">Aufträge 6-3 und 6-4</span><span class="sxs-lookup"><span data-stu-id="b6cb1-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="b6cb1-201">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b6cb1-202">**Debitorenkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="b6cb1-203">**Debitorenanforderung:** *1*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b6cb1-204">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-205">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-206">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="b6cb1-207">Aufträge 6-5 und 6-6</span><span class="sxs-lookup"><span data-stu-id="b6cb1-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="b6cb1-208">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b6cb1-209">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b6cb1-210">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-210">**Site:** *6*</span></span>
    - <span data-ttu-id="b6cb1-211">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b6cb1-212">**Pool:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="b6cb1-213">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-214">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-215">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="b6cb1-216">Aufträge 6-7 und 6-8</span><span class="sxs-lookup"><span data-stu-id="b6cb1-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="b6cb1-217">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b6cb1-218">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b6cb1-219">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-219">**Site:** *6*</span></span>
    - <span data-ttu-id="b6cb1-220">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b6cb1-221">**Pool:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="b6cb1-222">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b6cb1-223">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="b6cb1-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b6cb1-224">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="b6cb1-225">Automatische Freigabe von Aufträgen für den Lagerort</span><span class="sxs-lookup"><span data-stu-id="b6cb1-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="b6cb1-226">Für jeden Satz von Kundenaufträgen, den Sie zuvor erstellt haben, führen Sie einen Vorgang für die automatische Freigabe an das Lager durch.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="b6cb1-227">In jedem Fall werden Sie [grundlegende Verfahren für die Freigabe an das Lager](#release-procedure) durcharbeiten, die hier beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="b6cb1-228">Grundlegendes Lagerfreigabeverfahren</span><span class="sxs-lookup"><span data-stu-id="b6cb1-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="b6cb1-229">Für jeden Satz von Kundenaufträgen, den Sie zuvor erstellt haben, führen Sie die drei in den folgenden Unterabschnitten beschriebenen Verfahren aus.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="b6cb1-230">Aktualisieren Sie die Wellenvorlage, die während der Veröffentlichung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="b6cb1-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="b6cb1-231">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b6cb1-232">Stellen Sie das Feld **Wellenvorlagentyp** auf *Versand* ein.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="b6cb1-233">Suchen Sie die Wellenvorlage, die dem Lager zugeordnet ist, das Sie in den Auftragssätzen verwendet haben, die Sie für dieses Szenario erstellt haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="b6cb1-234">Zum Beispiel, wenn Sie ein Lager *24* verwendet haben, wählen Sie **Standard-24-Lieferung**-Wellenvorlage.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="b6cb1-235">Wenn Sie ein Lager *61* verwendet haben, wählen Sie die **61-Lieferung**-Wellenvorlage.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="b6cb1-236">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b6cb1-237">Legen Sie die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Nein* fest.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="b6cb1-238">Für Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="b6cb1-238">Release to the warehouse</span></span>

1. <span data-ttu-id="b6cb1-239">Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> Automatische Freigabe von Aufträgen für den Lagerort**.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="b6cb1-240">Stellen Sie die **Freizugebende Menge** auf *Alle* ein.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="b6cb1-241">Wählen Sie auf dem Inforegister **Aufzeichnungen enthalten** **Filter** aus, um das Abfragedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="b6cb1-242">Wählen Sie auf der Registerkarte **Bereich** **Hinzufügen** aus, um eine Zeile mit den folgenden Einstellungen zum Raster hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="b6cb1-243">**Tabelle:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="b6cb1-244">**Abgeleitete Tabelle:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="b6cb1-245">**Feld:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="b6cb1-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="b6cb1-246">**Kriterien:** Geben Sie eine durch Kommas getrennte Liste der Kundenauftragsnummern aus dem gewünschten Auftragssatz ein.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="b6cb1-247">Wählen Sie **OK** aus, um Ihre Anfrage zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="b6cb1-248">Wählen Sie **OK** aus, um das Verfahren *Automatische Freigabe an das Lager* zu starten.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="b6cb1-249">Überprüfen Sie die Lieferung, die erstellt oder aktualisiert wurde</span><span class="sxs-lookup"><span data-stu-id="b6cb1-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="b6cb1-250">Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="b6cb1-251">Suchen Sie die gewünschte Lieferung und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="b6cb1-252">Wenn beim Erstellen oder Aktualisieren der Lieferung eine Konsolidierungsrichtlinie verwendet wurde, sollte diese im Feld **Richtlinie für Lieferungskonsolidierung** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="b6cb1-253">Kundenaufträge aus Auftragssatz 1 freigeben</span><span class="sxs-lookup"><span data-stu-id="b6cb1-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="b6cb1-254">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 1 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="b6cb1-255">Wenn Sie fertig sind, sollten Sie sehen, dass zwei Lieferungen erstellt wurden:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="b6cb1-256">Die erste Lieferung enthält drei Zeilen und wurde mit der *CustomerMode*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="b6cb1-257">Die zweite Lieferung, die nicht *Airways* als Transportart der Lieferung verwendet, wurde unter Verwendung der *CustomerOrderNo*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="b6cb1-258">Kundenaufträge aus Auftragssatz 2 freigeben</span><span class="sxs-lookup"><span data-stu-id="b6cb1-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="b6cb1-259">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 2 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="b6cb1-260">Wenn Sie fertig sind, sollten Sie sehen, dass drei Lieferungen erstellt wurden:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="b6cb1-261">Die erste Lieferung enthält die *Brennbar*-Artikel.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="b6cb1-262">Jede der beiden anderen Lieferungen enthält eine Position mit dem *Explosiv*-Artikel.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="b6cb1-263">Kundenaufträge aus Auftragssatz 3 freigeben</span><span class="sxs-lookup"><span data-stu-id="b6cb1-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="b6cb1-264">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 3 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="b6cb1-265">Wenn Sie fertig sind, sollten Sie sehen, dass die folgenden Aktionen ausgeführt wurden:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="b6cb1-266">Eine vorhandene Lieferung (die Lieferung, die erstellt wurde, als Auftragssatz 2 für das Lager freigegeben wurde) wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="b6cb1-267">Eine Zeile mit dem *Brennbar*-Artikel wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="b6cb1-268">Es wurde eine neue Lieferung erstellt, die die *Explosiv*-Artikel enthält.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="b6cb1-269">Kundenaufträge aus Auftragssatz 4 freigeben</span><span class="sxs-lookup"><span data-stu-id="b6cb1-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="b6cb1-270">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 4 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="b6cb1-271">Wenn Sie fertig sind, sollten Sie sehen, dass eine vorhandene Lieferung (wo das **Debitorenanforderung**-Feld auf *1* gesetzt ist) aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="b6cb1-272">Eine neue Zeile wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="b6cb1-273">Kundenaufträge aus Auftragssatz 5 freigeben</span><span class="sxs-lookup"><span data-stu-id="b6cb1-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="b6cb1-274">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 5 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="b6cb1-275">Wenn Sie fertig sind, sollten Sie sehen, dass die folgenden Aktionen ausgeführt wurden:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="b6cb1-276">Eine vorhandene Lieferung (wo das **Debitorenanforderung**-Feld auf *1* gesetzt ist) wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="b6cb1-277">Eine Zeile aus Kundenauftrag 5-3 (wo das **Kundenanforderung**-Feld auf *1* gesetzt ist) wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="b6cb1-278">Eine neue Lieferung wurde erstellt, in der die Zeilen aus den Kundenaufträgen 5-1 und 5-2 zu einer Lieferung zusammengefasst sind.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="b6cb1-279">Kundenaufträge aus Auftragssatz 6 freigeben</span><span class="sxs-lookup"><span data-stu-id="b6cb1-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="b6cb1-280">Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 6 freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="b6cb1-281">Wenn Sie fertig sind, sollten Sie sehen, dass vier Lieferungen erstellt wurden:</span><span class="sxs-lookup"><span data-stu-id="b6cb1-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="b6cb1-282">Positionen aus zwei Bestellungen für Debitor *US-003* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b6cb1-283">Positionen aus zwei Bestellungen für Debitor *US-004* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b6cb1-284">Positionen aus aus den Aufträgen 6-5 und 6-6 für Debitor *US-007* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b6cb1-285">Positionen aus aus den Aufträgen 6-7 und 6-8 für Debitor *US-007* wurden unter Verwendung der *CrossOrder*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="b6cb1-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6cb1-286">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b6cb1-286">Additional resources</span></span>

- [<span data-ttu-id="b6cb1-287">Lieferungskonsolidierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="b6cb1-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="b6cb1-288">Richtlinien zur Lieferungskonsolidierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b6cb1-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
