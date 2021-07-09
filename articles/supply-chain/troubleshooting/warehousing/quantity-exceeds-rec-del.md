---
title: Die Menge, die Sie zu aktualisieren versuchen, übersteigt die empfangene/gelieferte Menge.
description: Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die die für den Arbeitsauftrag kommissionierte und reservierte Arbeitsmenge übersteigt.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249109"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="576de-103">Die Menge, die Sie zu aktualisieren versuchen, übersteigt die empfangene/gelieferte Menge</span><span class="sxs-lookup"><span data-stu-id="576de-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="576de-104">Fehlercode: SYS7676</span><span class="sxs-lookup"><span data-stu-id="576de-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="576de-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="576de-105">Symptoms</span></span>

<span data-ttu-id="576de-106">Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die die für den Arbeitsauftrag kommissionierte und reservierte Arbeitsmenge übersteigt.</span><span class="sxs-lookup"><span data-stu-id="576de-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="576de-107">Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="576de-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="576de-108">Physische Restmenge und Gesamtmenge müssen dasselbe Vorzeichen haben.</span><span class="sxs-lookup"><span data-stu-id="576de-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="576de-109">Daher können Sie den Lieferschein für die Ladung nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="576de-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="576de-110">Ursache</span><span class="sxs-lookup"><span data-stu-id="576de-110">Cause</span></span>

<span data-ttu-id="576de-111">Die entnommene Arbeitsmenge stimmt nicht mit der erstellten Arbeitsmenge in der Ladung überein.</span><span class="sxs-lookup"><span data-stu-id="576de-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="576de-112">Dieses Problem kann z. B. auftreten, wenn die Menge der Ladungszeile, der erstellten Arbeit oder der kommissionierten Menge nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="576de-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="576de-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="576de-113">Resolution</span></span>

<span data-ttu-id="576de-114">Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="576de-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="576de-115">Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="576de-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="576de-116">Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="576de-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="576de-117">Passen Sie die Menge für die Ladung an.</span><span class="sxs-lookup"><span data-stu-id="576de-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="576de-118">Stornieren Sie alle Kommissionierregistrierungen und führen Sie die Kommissionierung erneut durch.</span><span class="sxs-lookup"><span data-stu-id="576de-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="576de-119">Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen sind und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="576de-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="576de-120">Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="576de-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="576de-121">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="576de-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="576de-122">Wählen Sie die Ladung aus, für die die Sendung nicht erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="576de-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="576de-123">Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.</span><span class="sxs-lookup"><span data-stu-id="576de-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="576de-124">Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.</span><span class="sxs-lookup"><span data-stu-id="576de-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="576de-125">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="576de-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="576de-126">Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="576de-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="576de-127">Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="576de-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="576de-128">Justieren Sie die Menge der Ladung in der Zeile</span><span class="sxs-lookup"><span data-stu-id="576de-128">Adjust the load line quantity</span></span>

<span data-ttu-id="576de-129">Gehen Sie wie folgt vor, um die Menge der Ladung in der Zeile anzupassen.</span><span class="sxs-lookup"><span data-stu-id="576de-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="576de-130">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="576de-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="576de-131">Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="576de-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="576de-132">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.</span><span class="sxs-lookup"><span data-stu-id="576de-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="576de-133">Wählen Sie auf der Registerkarte **Ladungszeilen** die Ladung des Elements, das ein Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="576de-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="576de-134">Wählen Sie **Reduzieren Sie die kommissionierte Menge**, um die kommissionierte Menge anzupassen.</span><span class="sxs-lookup"><span data-stu-id="576de-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="576de-135">Legen Sie das Feld **Ladung reduzieren** fest, um Anpassungen an der Ladung zu reflektieren.</span><span class="sxs-lookup"><span data-stu-id="576de-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="576de-136">Stornieren Sie alle Kommissionierregistrierungen und wiederholen Sie die Kommissionierung.</span><span class="sxs-lookup"><span data-stu-id="576de-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="576de-137">Wenn jemand die Kommissionierregistrierung verwendet hat, um eine Ladung ohne Arbeit zu schließen, kann eine Diskrepanz zwischen der Ladelinienmenge und der kommissionierten Menge auftreten.</span><span class="sxs-lookup"><span data-stu-id="576de-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="576de-138">In diesem Fall muss die manuelle Kommissionierregistrierung rückgängig gemacht werden, und die Kommissionierung muss dann mit der Warehouse Management Mobile-App abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="576de-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="576de-139">Gehen Sie wie folgt vor, um die Kommissionierregistrierung rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="576de-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="576de-140">Gehen Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="576de-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="576de-141">Wählen Sie den Verkaufsauftrag aus, für den Sie keinen Lieferschein für die Ladung buchen können.</span><span class="sxs-lookup"><span data-stu-id="576de-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="576de-142">Wählen Sie auf der Registerkarte  **Verkaufsauftragszeilen** die Zeile des Verkaufsauftrags, für den die Kommissionierregistrierung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="576de-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="576de-143">Wählen Sie **Zeile \> Kommissionierung rückgängig machen**, um die Entnahme rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="576de-143">Select **Update line \> Pick** to unpick the items.</span></span>
