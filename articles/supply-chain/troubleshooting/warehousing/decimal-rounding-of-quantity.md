---
title: Dezimale Rundung der physischen Aktualisierungsmenge ist falsch
description: Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die nicht mit der in der Einheit definierten Dezimalgenauigkeit übereinstimmt.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248783"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="076d9-103">Dezimale Rundung der physischen Aktualisierungsmenge ist falsch</span><span class="sxs-lookup"><span data-stu-id="076d9-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="076d9-104">Fehlercode: SYS19589</span><span class="sxs-lookup"><span data-stu-id="076d9-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="076d9-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="076d9-105">Symptoms</span></span>

<span data-ttu-id="076d9-106">Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die nicht mit der in der Einheit definierten Dezimalgenauigkeit übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="076d9-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="076d9-107">Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="076d9-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="076d9-108">Dezimalstelle der physischen Buchungsmenge in Einheit '%1' wurde falsch gerundet.</span><span class="sxs-lookup"><span data-stu-id="076d9-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="076d9-109">Daher können Sie den Lieferschein für die Ladung nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="076d9-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="076d9-110">Ursache</span><span class="sxs-lookup"><span data-stu-id="076d9-110">Cause</span></span>

<span data-ttu-id="076d9-111">Das System wertet aus, ob die dezimale Rundung der Versandmenge mit der dezimalen Genauigkeit übereinstimmt, die für die Versandeinheit definiert ist.</span><span class="sxs-lookup"><span data-stu-id="076d9-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="076d9-112">Wenn das System die Versandmenge auf die angegebene Anzahl von Dezimalstellen rundet und feststellt, dass die gerundete Versandmenge nicht mit der tatsächlichen Versandmenge übereinstimmt, können Sie den Lieferschein nicht erzeugen.</span><span class="sxs-lookup"><span data-stu-id="076d9-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="076d9-113">Dieses Problem kann zum Beispiel auftreten, wenn die Verkaufsmenge 1,75 Kilogramm (kg) beträgt, die Dezimalgenauigkeit aber auf *1* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="076d9-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="076d9-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="076d9-114">Resolution</span></span>

<span data-ttu-id="076d9-115">Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="076d9-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="076d9-116">Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="076d9-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="076d9-117">Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Menge sauber umgewandelt werden kann, ohne Dezimalzahlen und andere Rundungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="076d9-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="076d9-118">Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="076d9-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="076d9-119">Überprüfen Sie die Zeilen mit den Ladungen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Menge sauber umgerechnet werden kann, ohne Dezimalzahlen und andere Rundungsprobleme</span><span class="sxs-lookup"><span data-stu-id="076d9-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="076d9-120">Gehen Sie wie folgt vor, um Ihre Zeilen mit den Ladungen zu überprüfen und Anpassungen vorzunehmen, um sicherzustellen, dass die Menge sauber umgerechnet werden kann, ohne Dezimalzahlen und andere Rundungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="076d9-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="076d9-121">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="076d9-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="076d9-122">Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="076d9-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="076d9-123">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.</span><span class="sxs-lookup"><span data-stu-id="076d9-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="076d9-124">Wählen Sie auf der Registerkarte **Ladungszeilen** die Ladung des Elements, das ein Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="076d9-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="076d9-125">Wählen Sie **Reduzieren Sie die kommissionierte Menge**, um die kommissionierte Menge anzupassen.</span><span class="sxs-lookup"><span data-stu-id="076d9-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="076d9-126">Wählen Sie auf der Registerkarte  **Zeilendetails** die Option **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="076d9-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="076d9-127">Legen Sie das Feld **Menge** auf die kommissionierte Menge fest (d. h. den Wert des Feldes **Werk erstellte Menge**), damit die Erstellung des Lieferscheins fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="076d9-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="076d9-128">Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="076d9-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="076d9-129">Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und Anpassungen vorzunehmen, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="076d9-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="076d9-130">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="076d9-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="076d9-131">Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="076d9-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="076d9-132">Wählen Sie im Inforegister **Ladungszeilen** die Ladungszeile für das Element, das ein Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="076d9-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="076d9-133">Notieren Sie sich den Wert der Felder **Menge** und **Einheit**.</span><span class="sxs-lookup"><span data-stu-id="076d9-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="076d9-134">Gehen Sie zu **Organisationsverwaltung \> Einheiten \> Einheiten**.</span><span class="sxs-lookup"><span data-stu-id="076d9-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="076d9-135">Wählen Sie die Einheit aus, für die der Lieferschein nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="076d9-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="076d9-136">Passen Sie den Wert des Feldes **Dezimalgenauigkeit** wie gewünscht an.</span><span class="sxs-lookup"><span data-stu-id="076d9-136">Adjust the value of the **Decimal precision** field as required.</span></span>
