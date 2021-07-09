---
title: Die kommissionierte Menge ist bei der Lieferscheinerstellung nicht ausreichend
description: Wenn Sie einen Lieferschein generieren, enthält die ausgehende Ladung eine kommissionierte Menge, die nicht mit der erstellten Arbeitsmenge auf der Ladelinie übereinstimmt.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249108"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="a7fb9-103">Die kommissionierte Menge ist bei der Lieferscheinerstellung nicht ausreichend</span><span class="sxs-lookup"><span data-stu-id="a7fb9-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="a7fb9-104">Fehlercode: SYS54073</span><span class="sxs-lookup"><span data-stu-id="a7fb9-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="a7fb9-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="a7fb9-105">Symptoms</span></span>

<span data-ttu-id="a7fb9-106">Wenn Sie einen Lieferschein generieren, enthält die ausgehende Ladung eine kommissionierte Menge, die nicht mit der erstellten Arbeitsmenge auf der Ladelinie übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="a7fb9-107">Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="a7fb9-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="a7fb9-108">Da %1 entnommen wurden, ist es nicht ausreichend, %2 zu aktualisieren, wenn der Rest anschließend %3 sein muss.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="a7fb9-109">Daher können Sie den Lieferschein für die Ladung nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="a7fb9-110">Ursache</span><span class="sxs-lookup"><span data-stu-id="a7fb9-110">Cause</span></span>

<span data-ttu-id="a7fb9-111">Der Lieferschein kann in seinem aktuellen Status nicht generiert werden, weil eine der folgenden Bedingungen vorliegen könnte:</span><span class="sxs-lookup"><span data-stu-id="a7fb9-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="a7fb9-112">Die zugehörige Arbeit wurde noch nicht entnommen und an den endgültigen Versandort gebracht.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="a7fb9-113">Die entnommene Arbeitsmenge stimmt nicht mit der erstellten Arbeitsmenge in der Ladung überein.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="a7fb9-114">Die Menge der Ladelinie, die erstellte Arbeitsmenge und die kommissionierte Menge stimmen nicht überein.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="a7fb9-115">Lösung</span><span class="sxs-lookup"><span data-stu-id="a7fb9-115">Resolution</span></span>

<span data-ttu-id="a7fb9-116">Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="a7fb9-117">Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="a7fb9-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="a7fb9-118">Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="a7fb9-119">Passen Sie die Menge für die Ladung an.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="a7fb9-120">Stornieren Sie alle Kommissionierregistrierungen und führen Sie die Kommissionierung erneut durch.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="a7fb9-121">Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen sind und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="a7fb9-122">Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="a7fb9-123">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a7fb9-124">Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="a7fb9-125">Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="a7fb9-126">Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="a7fb9-127">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="a7fb9-128">Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="a7fb9-129">Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="a7fb9-130">Justieren Sie die Menge der Ladung in der Zeile</span><span class="sxs-lookup"><span data-stu-id="a7fb9-130">Adjust the load line quantity</span></span>

<span data-ttu-id="a7fb9-131">Gehen Sie wie folgt vor, um die Menge der Ladung in der Zeile anzupassen.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="a7fb9-132">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a7fb9-133">Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="a7fb9-134">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="a7fb9-135">Wählen Sie auf der Registerkarte **Ladungszeilen** die Ladung des Elements, das ein Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="a7fb9-136">Wählen Sie **Reduzieren Sie die kommissionierte Menge**, um die kommissionierte Menge anzupassen.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="a7fb9-137">Legen Sie das Feld **Ladung reduzieren** fest, um Anpassungen an der Ladung zu reflektieren.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="a7fb9-138">Stornieren Sie alle Kommissionierregistrierungen und wiederholen Sie die Kommissionierung.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="a7fb9-139">Das Problem kann auftreten, weil jemand die Kommissionierregistrierung verwendet hat, um eine Ladung ohne Arbeit zu schließen.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="a7fb9-140">In diesem Fall muss die manuelle Kommissionierregistrierung rückgängig gemacht werden, und die Kommissionierung muss dann mit der Warehouse Management Mobile-App abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="a7fb9-141">Gehen Sie wie folgt vor, um die Kommissionierregistrierung rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="a7fb9-142">Gehen Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="a7fb9-143">Wählen Sie den Verkaufsauftrag aus, für den Sie keinen Lieferschein für die Ladung buchen können.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="a7fb9-144">Wählen Sie auf der Registerkarte  **Verkaufsauftragszeilen** die Zeile des Verkaufsauftrags, für den die Kommissionierregistrierung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="a7fb9-145">Wählen Sie **Zeile \> Kommissionierung rückgängig machen**, um die Entnahme rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="a7fb9-145">Select **Update line \> Pick** to unpick the items.</span></span>
