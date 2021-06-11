---
title: Konsolidieren Sie Sendungen, wenn die Versandkonsolidierungsrichtlinie überschrieben wird
description: In diesem Thema wird ein Szenario vorgestellt, in dem eine oder mehrere Verkaufspositionen von der Seite „Freigabe an Lager“ manuell an das Lager freigegeben werden müssen und die systemdefinierte Lieferungskonsolidierungsrichtlinie vor der Freigabe überschrieben werden muss.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 6928375c88a199bd9c6b48f05b38343463762920
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117008"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a><span data-ttu-id="a93c9-103">Konsolidieren Sie Sendungen, wenn die Versandkonsolidierungsrichtlinie überschrieben wird</span><span class="sxs-lookup"><span data-stu-id="a93c9-103">Consolidate shipments when the shipment consolidation policy is overridden</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a93c9-104">In diesem Thema wird ein Szenario vorgestellt, in dem eine oder mehrere Verkaufspositionen von der Seite **Freigabe an Lager** manuell an das Lager freigegeben werden müssen und die systemdefinierte Lieferungskonsolidierungsrichtlinie vor der Freigabe überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="a93c9-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="a93c9-105">Eine Überschreibung der Lieferungskonsolidierungsrichtlinie kann erforderlich sein, wenn beispielsweise ein Auftrag, der normalerweise nicht mit offenen Lieferungen konsolidiert wird, mit offenen Lieferungen konsolidiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a93c9-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="a93c9-106">Während des Szenarios erstellen Sie eine Reihe von Aufträgen und überschreiben dann die Standardrichtlinie für die Lieferungskonsolidierung, bevor Sie die Aufträge an das Lager freigeben.</span><span class="sxs-lookup"><span data-stu-id="a93c9-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="a93c9-107">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="a93c9-107">Make demo data available</span></span>

<span data-ttu-id="a93c9-108">Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a93c9-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a93c9-109">Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="a93c9-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="a93c9-110">Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein</span><span class="sxs-lookup"><span data-stu-id="a93c9-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="a93c9-111">In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a93c9-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="a93c9-112">Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a93c9-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="a93c9-113">Erstellen Sie die Kundenaufträge für dieses Szenario</span><span class="sxs-lookup"><span data-stu-id="a93c9-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="a93c9-114">Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**, und erstellen Sie drei identische Aufträge mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="a93c9-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a93c9-115">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a93c9-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="a93c9-116">Eine Auftragsposition hat die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="a93c9-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a93c9-117">**Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="a93c9-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a93c9-118">**Menge** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a93c9-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a93c9-119">Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="a93c9-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="a93c9-120">Geben Sie die Aufträge von der Seite „Freigabe an Lager“ frei</span><span class="sxs-lookup"><span data-stu-id="a93c9-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="a93c9-121">Befolgen Sie diese Schritte, um die Lieferungskonsolidierungsrichtlinie während der Freigabe an das Lager zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a93c9-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="a93c9-122">Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> An Lager freigeben**.</span><span class="sxs-lookup"><span data-stu-id="a93c9-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="a93c9-123">Wählen Sie im oberen Bereich den ersten Auftrag aus, den Sie für dieses Szenario erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a93c9-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="a93c9-124">Wählen Sie **Hinzufügen** aus, um die Position zur Freigabe zum Lager hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a93c9-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="a93c9-125">Beachten Sie, dass die *Standard*-Lieferungskonsolidierungsrichtlinie im unteren Bereich angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a93c9-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="a93c9-126">Wählen Sie im unteren Bereich **Neue Lieferungskonsolidierungsrichtlinie auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="a93c9-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="a93c9-127">Wählen Sie eine Richtlinie aus, die eine Konsolidierung mit anderen offenen Lieferungen derselben Richtlinie ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a93c9-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="a93c9-128">Wählen Sie zum Beispiel die *CustomerOrderNo*-Richtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="a93c9-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="a93c9-129">Wählen Sie **An Lager freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="a93c9-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a93c9-130">Wählen Sie im oberen Bereich den zweiten und dritten Auftrag aus, die Sie für dieses Szenario erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a93c9-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="a93c9-131">Wählen Sie **Hinzufügen** aus, um die Positionen zur Freigabe zum Lager hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a93c9-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="a93c9-132">Beachten Sie, dass die *Standard*-Richtlinie im unteren Bereich angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a93c9-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="a93c9-133">Wählen Sie die zweite Zeile Position und dann im Feld **Neue Lieferungskonsolidierungsrichtlinie auswählen** die *CustomerOrderNo*-Richtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="a93c9-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="a93c9-134">Wählen Sie **An Lager freigeben** für beide Positionen aus.</span><span class="sxs-lookup"><span data-stu-id="a93c9-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="a93c9-135">Überprüfen Sie die Lieferungen</span><span class="sxs-lookup"><span data-stu-id="a93c9-135">Verify the shipments</span></span>

<span data-ttu-id="a93c9-136">Es sollten zwei Lieferungen erstellt worden sein:</span><span class="sxs-lookup"><span data-stu-id="a93c9-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="a93c9-137">Die erste Lieferung enthält zwei Zeilen und wurde mit der *CustomerOrderNo*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="a93c9-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="a93c9-138">Die zweite Lieferung enthält eine Position und wurde mit der *Standard*-Lieferungskonsolidierungsrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="a93c9-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="a93c9-139">Befolgen Sie diese Schritte, um die erstellten Lieferungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a93c9-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="a93c9-140">Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.</span><span class="sxs-lookup"><span data-stu-id="a93c9-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="a93c9-141">Suchen Sie die gewünschte Lieferung und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="a93c9-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="a93c9-142">Überprüfen Sie die Konsolidierungsrichtlinie, die verwendet wurde, als die Lieferung erstellt wurde, im Feld **Richtlinie für Lieferungskonsolidierung**.</span><span class="sxs-lookup"><span data-stu-id="a93c9-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a93c9-143">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a93c9-143">Additional resources</span></span>

- [<span data-ttu-id="a93c9-144">Lieferungskonsolidierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="a93c9-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="a93c9-145">Richtlinien zur Lieferungskonsolidierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a93c9-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]