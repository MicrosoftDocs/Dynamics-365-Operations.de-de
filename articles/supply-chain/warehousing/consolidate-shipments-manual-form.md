---
title: Lieferungen manuell auf der Seite zur Lieferungskonsolidierung konsolidieren
description: In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Aufträge an das Lager freigegeben werden und anschließend später auf der Lieferungskonsolidierungsseite konsolidiert werden.
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
ms.openlocfilehash: acc6e1d09894b57d2bb063bacbcddef239c1a8bd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383774"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="c61b2-103">Lieferungen manuell auf der Seite zur Lieferungskonsolidierung konsolidieren</span><span class="sxs-lookup"><span data-stu-id="c61b2-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c61b2-104">In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Aufträge an das Lager freigegeben werden und anschließend später auf der Seite **Lieferungskonsolidierung** konsolidiert werden.</span><span class="sxs-lookup"><span data-stu-id="c61b2-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="c61b2-105">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="c61b2-105">Make demo data available</span></span>

<span data-ttu-id="c61b2-106">Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c61b2-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c61b2-107">Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="c61b2-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="c61b2-108">Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein</span><span class="sxs-lookup"><span data-stu-id="c61b2-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="c61b2-109">In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c61b2-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="c61b2-110">Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.</span><span class="sxs-lookup"><span data-stu-id="c61b2-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="c61b2-111">Erstellen Sie die Kundenaufträge für dieses Szenario</span><span class="sxs-lookup"><span data-stu-id="c61b2-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="c61b2-112">Erstellen Sie zunächst eine Sammlung von Kundenaufträgen, mit denen Sie arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="c61b2-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="c61b2-113">Sie müssen mit einem Lagerort arbeiten, der für WMS-Prozesse (Advanced Warehouse) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c61b2-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="c61b2-114">Sofern nicht ausdrücklich ein anderes Lager erwähnt wird, muss dasselbe Lager für jeden der folgenden Auftragssätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c61b2-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="c61b2-115">Wechseln Sie zu **Debitoren \> Aufträge \> Alle Kundenaufträge**, und erstellen Sie eine Sammlung von Kundenaufträgen mit den Einstellungen, die in den folgenden Unterabschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c61b2-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="c61b2-116">Aufträge 1 und 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="c61b2-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="c61b2-117">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="c61b2-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c61b2-118">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c61b2-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c61b2-119">**Pool:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="c61b2-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="c61b2-120">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="c61b2-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c61b2-121">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="c61b2-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c61b2-122">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c61b2-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c61b2-123">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="c61b2-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="c61b2-124">Aufträge 3 und 4 erstellen</span><span class="sxs-lookup"><span data-stu-id="c61b2-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="c61b2-125">Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="c61b2-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c61b2-126">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c61b2-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c61b2-127">**Pool:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="c61b2-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="c61b2-128">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="c61b2-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c61b2-129">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="c61b2-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c61b2-130">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c61b2-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c61b2-131">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="c61b2-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="c61b2-132">Aufträge für den Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="c61b2-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="c61b2-133">Führen Sie die folgenden Schritte aus, um jeden Auftrag, den Sie für dieses Szenario erstellt haben, für das Lager freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c61b2-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="c61b2-134">Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="c61b2-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c61b2-135">Suchen und wählen Sie den freizugebenden Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="c61b2-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="c61b2-136">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten \> Für Lagerort freigeben**, um die ausgewählten Aufträge freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c61b2-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="c61b2-137">Wiederholen Sie diesen Vorgang für alle anderen Aufträge, die Sie für dieses Szenario erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c61b2-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="c61b2-138">Lieferungen konsolidieren</span><span class="sxs-lookup"><span data-stu-id="c61b2-138">Consolidate shipments</span></span>

1. <span data-ttu-id="c61b2-139">Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.</span><span class="sxs-lookup"><span data-stu-id="c61b2-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="c61b2-140">Suchen und wählen Sie eine Lieferung aus, die erstellt wurde, als Kundenauftrag 1 für das Lager freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c61b2-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="c61b2-141">(Das **Lieferungskonsolidierungsrichtlinie**-Feld sollte auf *Auftragspool* gesetzt sein.)</span><span class="sxs-lookup"><span data-stu-id="c61b2-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="c61b2-142">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lieferungen** auf **Lieferungen \> Lieferungen konsolidieren**.</span><span class="sxs-lookup"><span data-stu-id="c61b2-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="c61b2-143">Überprüfen Sie die Lieferungen, die zur Konsolidierung vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="c61b2-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="c61b2-144">Für die Konsolidierung sollte nur eine Lieferung mit derselben Richtlinie vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="c61b2-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="c61b2-145">Schließen Sie die Seite **Lieferungskonsolidierung**.</span><span class="sxs-lookup"><span data-stu-id="c61b2-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="c61b2-146">Suchen und wählen Sie eine Lieferung aus, die erstellt wurde, als Kundenauftrag 3 für das Lager freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c61b2-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="c61b2-147">(Das **Lieferungskonsolidierungsrichtlinie**-Feld sollte auf *Standard* gesetzt sein.)</span><span class="sxs-lookup"><span data-stu-id="c61b2-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="c61b2-148">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lieferungen** auf **Lieferungen \> Lieferungen konsolidieren**.</span><span class="sxs-lookup"><span data-stu-id="c61b2-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="c61b2-149">Überprüfen Sie, dass keine Lieferungen zur Konsolidierung vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="c61b2-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="c61b2-150">Wählen Sie **Filter anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="c61b2-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="c61b2-151">Entfernen Sie im **Filter**-Bereich den Filter **Auftragsnummer** und wählen Sie dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="c61b2-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="c61b2-152">Überprüfen Sie die Lieferungen, die zur Konsolidierung vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="c61b2-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="c61b2-153">Für die Konsolidierung sollte nur eine Lieferung mit derselben Richtlinie vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="c61b2-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c61b2-154">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c61b2-154">Additional resources</span></span>

- [<span data-ttu-id="c61b2-155">Lieferungskonsolidierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="c61b2-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="c61b2-156">Richtlinien zur Lieferungskonsolidierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="c61b2-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)