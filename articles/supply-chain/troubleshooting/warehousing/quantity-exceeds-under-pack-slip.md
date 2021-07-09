---
title: Menge überschreitet Unterlieferungsprozentsatz bei Lieferscheinerstellung
description: Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die den Unterlieferungsprozentsatz überschreitet.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249104"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="48098-103">Menge überschreitet Unterlieferungsprozentsatz bei Lieferscheinerstellung</span><span class="sxs-lookup"><span data-stu-id="48098-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="48098-104">Fehlercode: SYS24921</span><span class="sxs-lookup"><span data-stu-id="48098-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="48098-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="48098-105">Symptoms</span></span>

<span data-ttu-id="48098-106">Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die den Unterlieferungsprozentsatz überschreitet.</span><span class="sxs-lookup"><span data-stu-id="48098-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="48098-107">Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="48098-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="48098-108">Unterlieferung von Position ist %1 Prozent, doch die erlaubte Unterlieferung beträgt nur %2 Prozent.</span><span class="sxs-lookup"><span data-stu-id="48098-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="48098-109">Daher können Sie den Lieferschein für die Ladung nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="48098-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="48098-110">Ursache</span><span class="sxs-lookup"><span data-stu-id="48098-110">Cause</span></span>

<span data-ttu-id="48098-111">Die kommissionierte Menge für die Ladung oder Sendung ist kleiner als die bestellte Menge und liegt nicht im Bereich des Unterlieferungsprozentsatzes.</span><span class="sxs-lookup"><span data-stu-id="48098-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="48098-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="48098-112">Resolution</span></span>

<span data-ttu-id="48098-113">Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="48098-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="48098-114">Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="48098-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="48098-115">Passen Sie den Unterlieferungsprozentsatz an.</span><span class="sxs-lookup"><span data-stu-id="48098-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="48098-116">Stornieren Sie und nehmen Sie Anpassungen vor.</span><span class="sxs-lookup"><span data-stu-id="48098-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="48098-117">Anpassen des Unterlieferungsprozentsatzes</span><span class="sxs-lookup"><span data-stu-id="48098-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="48098-118">Gehen Sie wie folgt vor, um den Unterlieferungsprozentsatz anzupassen.</span><span class="sxs-lookup"><span data-stu-id="48098-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="48098-119">Gehen Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="48098-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="48098-120">Wählen Sie den Verkaufsauftrag aus, für den Sie keinen Lieferschein für die Ladung buchen können.</span><span class="sxs-lookup"><span data-stu-id="48098-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="48098-121">Wählen Sie auf der Registerkarte  **Kundenauftragszeilen** die Kundenauftragszeile für das Element, das den Unterlieferungsprozentsatz überschreitet.</span><span class="sxs-lookup"><span data-stu-id="48098-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="48098-122">Auf der Registerkarte  **Zeilendetails** wählen Sie **Lieferung**.</span><span class="sxs-lookup"><span data-stu-id="48098-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="48098-123">Legen Sie das Feld **Unterlieferung** auf einen größeren Prozentsatz fest, der die kommissionierte Menge gegen die Ladungsmenge aufwiegt, so dass die Lieferscheinerstellung fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="48098-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="48098-124">Stornieren und Anpassungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="48098-124">Reverse and make adjustments</span></span>

<span data-ttu-id="48098-125">Stornieren Sie alles, was für die Ladung gebucht wurde (z. B. den Lieferschein, die Versandbestätigung und die Arbeit), nehmen Sie Anpassungen am Verkaufsauftrag vor, geben Sie den Auftrag erneut für das Lagerort frei und schließen Sie den Versandvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="48098-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="48098-126">Gehen Sie wie folgt vor, um einen Lieferschein zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="48098-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="48098-127">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="48098-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="48098-128">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Lieferscheine stornieren**.</span><span class="sxs-lookup"><span data-stu-id="48098-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="48098-129">Gehen Sie wie folgt vor, um eine Versandbestätigung zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="48098-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="48098-130">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="48098-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="48098-131">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.</span><span class="sxs-lookup"><span data-stu-id="48098-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="48098-132">Gehen Sie wie folgt vor, um Arbeiten zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="48098-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="48098-133">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="48098-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="48098-134">Wählen Sie im Aktionsbereich auf der Registerkarte **Ladungen** in der Gruppe **Arbeit** die Option **Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="48098-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
