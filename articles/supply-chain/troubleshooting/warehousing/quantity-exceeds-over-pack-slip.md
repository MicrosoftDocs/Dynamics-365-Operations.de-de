---
title: Menge überschreitet Überlieferungsprozentsatz bei Lieferscheinerstellung
description: Wenn Sie einen Lieferschein generieren, enthält die ausgehende Ladung eine Menge, die den Überlieferungsprozentsatz überschreitet.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249106"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="80356-103">Menge überschreitet Überlieferungsprozentsatz bei Lieferscheinerstellung</span><span class="sxs-lookup"><span data-stu-id="80356-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="80356-104">Fehlercode: SYS24920</span><span class="sxs-lookup"><span data-stu-id="80356-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="80356-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="80356-105">Symptoms</span></span>

<span data-ttu-id="80356-106">Wenn Sie einen Lieferschein generieren, enthält die ausgehende Ladung eine Menge, die den Überlieferungsprozentsatz überschreitet.</span><span class="sxs-lookup"><span data-stu-id="80356-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="80356-107">Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="80356-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="80356-108">Überlieferung von Position ist %1 Prozent, doch die erlaubte Überlieferung beträgt nur %2 Prozent.</span><span class="sxs-lookup"><span data-stu-id="80356-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="80356-109">Daher können Sie den Lieferschein für die Ladung nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="80356-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="80356-110">Ursache</span><span class="sxs-lookup"><span data-stu-id="80356-110">Cause</span></span>

<span data-ttu-id="80356-111">Die kommissionierte Menge für die Ladung oder den Transport ist größer als die bestellte Menge und liegt nicht im Bereich der Überlieferungsquote.</span><span class="sxs-lookup"><span data-stu-id="80356-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="80356-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="80356-112">Resolution</span></span>

<span data-ttu-id="80356-113">Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="80356-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="80356-114">Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="80356-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="80356-115">Passen Sie die Menge für die Ladung an.</span><span class="sxs-lookup"><span data-stu-id="80356-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="80356-116">Passen Sie den Überlieferungsprozentsatz an.</span><span class="sxs-lookup"><span data-stu-id="80356-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="80356-117">Stornieren Sie und nehmen Sie Anpassungen vor.</span><span class="sxs-lookup"><span data-stu-id="80356-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="80356-118">Justieren Sie die Menge der Ladung in der Zeile</span><span class="sxs-lookup"><span data-stu-id="80356-118">Adjust the load line quantity</span></span>

<span data-ttu-id="80356-119">Gehen Sie wie folgt vor, um die Menge der Ladung in der Zeile anzupassen.</span><span class="sxs-lookup"><span data-stu-id="80356-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="80356-120">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="80356-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="80356-121">Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="80356-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="80356-122">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.</span><span class="sxs-lookup"><span data-stu-id="80356-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="80356-123">Wählen Sie auf der Registerkarte **Ladungszeilen** die Zeile der Ladung für das Element aus, das den Überlieferungsprozentsatz überschreitet.</span><span class="sxs-lookup"><span data-stu-id="80356-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="80356-124">Wählen Sie **Reduzieren Sie die kommissionierte Menge**, um die kommissionierte Menge anzupassen.</span><span class="sxs-lookup"><span data-stu-id="80356-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="80356-125">Wählen Sie auf der Registerkarte  **Zeilendetails** die Option **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="80356-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="80356-126">Legen Sie das Feld **Menge** auf die kommissionierte Menge fest (d. h. den Wert des Feldes **Werk erstellte Menge**), damit die Erstellung des Lieferscheins fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="80356-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="80356-127">Anpassen des Überlieferungsprozentsatzes</span><span class="sxs-lookup"><span data-stu-id="80356-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="80356-128">Gehen Sie wie folgt vor, um den Überlieferungsprozentsatz anzupassen.</span><span class="sxs-lookup"><span data-stu-id="80356-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="80356-129">Gehen Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="80356-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="80356-130">Wählen Sie den Verkaufsauftrag aus, für den Sie keinen Lieferschein für die Ladung buchen können.</span><span class="sxs-lookup"><span data-stu-id="80356-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="80356-131">Wählen Sie auf der Registerkarte **Kundenauftragszeilen** die Zeile des Verkaufsauftrags für das Element, das den Überlieferungsprozentsatz überschreitet.</span><span class="sxs-lookup"><span data-stu-id="80356-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="80356-132">Auf der Registerkarte  **Zeilendetails** wählen Sie **Lieferung**.</span><span class="sxs-lookup"><span data-stu-id="80356-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="80356-133">Legen Sie das Feld **Überlieferung** auf einen größeren Prozentsatz fest, der die kommissionierte Menge gegen die Ladungsmenge aufwiegt, so dass die Lieferscheinerstellung fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="80356-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="80356-134">Stornieren und Anpassungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="80356-134">Reverse and make adjustments</span></span>

<span data-ttu-id="80356-135">Stornieren Sie alles, was für die Ladung gebucht wurde (z. B. den Lieferschein, die Versandbestätigung und die Arbeit), nehmen Sie Anpassungen am Verkaufsauftrag vor, geben Sie den Auftrag erneut für das Lagerort frei und schließen Sie den Versandvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="80356-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="80356-136">Gehen Sie wie folgt vor, um einen Lieferschein zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="80356-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="80356-137">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="80356-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="80356-138">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Lieferscheine stornieren**.</span><span class="sxs-lookup"><span data-stu-id="80356-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="80356-139">Gehen Sie wie folgt vor, um eine Versandbestätigung zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="80356-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="80356-140">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="80356-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="80356-141">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.</span><span class="sxs-lookup"><span data-stu-id="80356-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="80356-142">Gehen Sie wie folgt vor, um Arbeiten zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="80356-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="80356-143">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="80356-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="80356-144">Wählen Sie im Aktionsbereich auf der Registerkarte **Ladungen** in der Gruppe **Arbeit** die Option **Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="80356-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
