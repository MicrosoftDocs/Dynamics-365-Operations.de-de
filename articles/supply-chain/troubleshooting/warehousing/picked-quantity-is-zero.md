---
title: Sie können eine Sendung nicht bestätigen, weil die Menge gleich Null ist
description: Sie können eine Sendung nicht bestätigen, weil die Menge gleich Null ist
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938475"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="f53f0-103">Sie können eine Sendung nicht bestätigen, weil die Menge gleich Null ist</span><span class="sxs-lookup"><span data-stu-id="f53f0-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="f53f0-104">Fehlercode: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="f53f0-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="f53f0-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="f53f0-105">Symptoms</span></span>

<span data-ttu-id="f53f0-106">Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="f53f0-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="f53f0-107">Die Auslastungsposition für Artikel „%1“ und Lieferung „%2“ wurde auf die Menge „Null“ aktualisiert, da die Einstellungen für Unterlieferung keine Liefermengen für diesen Artikel zulassen.</span><span class="sxs-lookup"><span data-stu-id="f53f0-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="f53f0-108">Daher können Sie die Sendung für die Ladung nicht bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f53f0-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f53f0-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="f53f0-109">Cause</span></span>

<span data-ttu-id="f53f0-110">Das System wertet aus, ob die entnommene Menge innerhalb der erwarteten Grenzen liegt, basierend auf der entnommenen Menge, der Menge der Ladung in der Zeile und dem Prozentsatz der Unterlieferung.</span><span class="sxs-lookup"><span data-stu-id="f53f0-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="f53f0-111">Wenn das System feststellt, dass die entnommene Menge in der Zeile mit der Ladung 0 (Null) ist, können Sie die Sendung nicht bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f53f0-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="f53f0-112">Dieses Problem könnte z. B. auftreten, wenn Arbeit storniert wurde und der Prozentsatz der Unterlieferung auf der Ladung 100 Prozent beträgt.</span><span class="sxs-lookup"><span data-stu-id="f53f0-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="f53f0-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="f53f0-113">Resolution</span></span>

<span data-ttu-id="f53f0-114">Überprüfen Sie Ihre Zeilen für die Ladung, um sicherzustellen, dass der Prozentsatz der Unterlieferung und die Mengen mit der entnommenen Arbeit übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f53f0-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="f53f0-115">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="f53f0-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f53f0-116">Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f53f0-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f53f0-117">Wählen Sie auf der Registerkarte **Ladezeilen** die Zeile für die Ladung des Elements aus, das den Prozentsatz der Unterlieferung überschreitet.</span><span class="sxs-lookup"><span data-stu-id="f53f0-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="f53f0-118">Passen Sie den Wert des Feldes **Unterlieferung** oder des Feldes **Menge** nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="f53f0-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="f53f0-119">Wenn das Problem immer noch nicht behoben ist, müssen Sie möglicherweise weitere Entnahmearbeiten für die zugehörigen Verkaufsaufträge oder Umlagerungsaufträge durchführen, bis die verfügbare Menge mit der Ladung oder dem Versand abgeglichen ist.</span><span class="sxs-lookup"><span data-stu-id="f53f0-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
