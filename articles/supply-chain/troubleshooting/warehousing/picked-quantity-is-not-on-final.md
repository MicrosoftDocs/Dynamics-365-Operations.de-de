---
title: Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind
description: Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938476"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="f54d6-103">Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind</span><span class="sxs-lookup"><span data-stu-id="f54d6-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="f54d6-104">Fehlercode: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="f54d6-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="f54d6-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="f54d6-105">Symptoms</span></span>

<span data-ttu-id="f54d6-106">Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="f54d6-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="f54d6-107">Einige der Artikel, die für Ladung %1 benötigt werden, sind noch nicht entnommen und zum endgültigen Versandort verschoben worden.</span><span class="sxs-lookup"><span data-stu-id="f54d6-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="f54d6-108">Daher können Sie die Sendung für die Ladung nicht bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f54d6-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f54d6-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="f54d6-109">Cause</span></span>

<span data-ttu-id="f54d6-110">Die Ladung oder Sendung kann in ihrem aktuellen Status nicht bestätigt werden, weil eine der folgenden Bedingungen vorliegen könnte:</span><span class="sxs-lookup"><span data-stu-id="f54d6-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="f54d6-111">Die zugehörige Arbeit wurde noch nicht entnommen und an den endgültigen Versandort gebracht.</span><span class="sxs-lookup"><span data-stu-id="f54d6-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="f54d6-112">Die entnommene Arbeitsmenge stimmt nicht mit der erstellten Arbeitsmenge in der Ladung überein.</span><span class="sxs-lookup"><span data-stu-id="f54d6-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="f54d6-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="f54d6-113">Resolution</span></span>

<span data-ttu-id="f54d6-114">Prüfen Sie die zugehörigen Verkaufsaufträge oder Umlagerungsaufträge für die Ladung oder den Transport.</span><span class="sxs-lookup"><span data-stu-id="f54d6-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="f54d6-115">Stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen sind und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f54d6-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="f54d6-116">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="f54d6-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f54d6-117">Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f54d6-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f54d6-118">Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.</span><span class="sxs-lookup"><span data-stu-id="f54d6-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="f54d6-119">Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.</span><span class="sxs-lookup"><span data-stu-id="f54d6-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="f54d6-120">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="f54d6-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="f54d6-121">Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f54d6-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="f54d6-122">Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="f54d6-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
