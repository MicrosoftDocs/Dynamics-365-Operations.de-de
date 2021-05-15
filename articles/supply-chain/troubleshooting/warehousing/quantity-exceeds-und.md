---
title: Sie können eine Sendung nicht bestätigen, weil die Menge den Prozentsatz für die Unterlieferung überschreitet
description: Sie können eine Sendung nicht bestätigen, weil die Menge den Prozentsatz für die Unterlieferung überschreitet
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938474"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="519a4-103">Sie können eine Sendung nicht bestätigen, weil die Menge den Prozentsatz für die Unterlieferung überschreitet</span><span class="sxs-lookup"><span data-stu-id="519a4-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="519a4-104">Fehlercode: WAX1687</span><span class="sxs-lookup"><span data-stu-id="519a4-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="519a4-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="519a4-105">Symptoms</span></span>

<span data-ttu-id="519a4-106">Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="519a4-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="519a4-107">Die Lieferung für Ladung %1 konnte nicht bestätigt werden, weil die Menge für Element %2 den Prozentsatz überschreitet, der für Unterlieferung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="519a4-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="519a4-108">Daher können Sie die Sendung für die Ladung nicht bestätigen.</span><span class="sxs-lookup"><span data-stu-id="519a4-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="519a4-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="519a4-109">Cause</span></span>

<span data-ttu-id="519a4-110">Die Menge der Ladung oder Sendung wurde nur teilweise entnommen.</span><span class="sxs-lookup"><span data-stu-id="519a4-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="519a4-111">Die Menge ist derzeit um einen Prozentsatz geringer als die entnommene Menge, der außerhalb des zulässigen Prozentsatzes für die Unterlieferung liegt.</span><span class="sxs-lookup"><span data-stu-id="519a4-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="519a4-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="519a4-112">Resolution</span></span>

<span data-ttu-id="519a4-113">Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="519a4-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="519a4-114">Legen Sie die Menge der Ladung in der Zeile fest.</span><span class="sxs-lookup"><span data-stu-id="519a4-114">Set the load line quantity.</span></span>
- <span data-ttu-id="519a4-115">Legen Sie den Prozentsatz für die Unterlieferung fest.</span><span class="sxs-lookup"><span data-stu-id="519a4-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="519a4-116">Die Menge der Ladung der Zeile festlegen</span><span class="sxs-lookup"><span data-stu-id="519a4-116">Set the load line quantity</span></span>

<span data-ttu-id="519a4-117">Um die Menge für die Ladung festzulegen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="519a4-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="519a4-118">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="519a4-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="519a4-119">Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="519a4-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="519a4-120">Wählen Sie auf der Registerkarte **Ladezeilen** die Zeile für die Ladung des Elements aus, das den Prozentsatz der Unterlieferung überschreitet.</span><span class="sxs-lookup"><span data-stu-id="519a4-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="519a4-121">Wählen Sie auf der Registerkarte **Zeilendetails** Inforegister **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="519a4-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="519a4-122">Legen Sie im Feld **Menge** den Wert auf die entnommene Menge fest (d.h. auf den Wert **Werk erstellte Menge**), damit die Versandbestätigung erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="519a4-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="519a4-123">Den Prozentsatz der Unterlieferung festlegen</span><span class="sxs-lookup"><span data-stu-id="519a4-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="519a4-124">Um den Prozentsatz der Unterlieferung festzulegen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="519a4-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="519a4-125">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="519a4-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="519a4-126">Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="519a4-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="519a4-127">Wählen Sie auf der Registerkarte **Ladezeilen** die Zeile für die Ladung des Elements aus, das den Prozentsatz der Unterlieferung überschreitet.</span><span class="sxs-lookup"><span data-stu-id="519a4-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="519a4-128">Wählen Sie auf der Seite **Zeilendetails** Inforegister **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="519a4-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="519a4-129">Legen Sie im Feld **Unterlieferung** den Wert auf einen größeren Prozentsatz fest, der die entnommene Menge gegen die Ladungsmenge aufwiegt, damit eine Versandbestätigung erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="519a4-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
