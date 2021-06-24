---
title: Die Menge kann nicht reduziert werden, wenn ein Auftrag storniert wird
description: Die Menge kann nicht reduziert werden, wenn ein Auftrag storniert wird.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230835"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="2b766-103">Die Menge kann nicht reduziert werden, wenn ein Auftrag storniert wird</span><span class="sxs-lookup"><span data-stu-id="2b766-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="2b766-104">Fehlercode: SYS138831</span><span class="sxs-lookup"><span data-stu-id="2b766-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="2b766-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="2b766-105">Symptoms</span></span>

<span data-ttu-id="2b766-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="2b766-106">The system shows the following error message:</span></span>

> <span data-ttu-id="2b766-107">Die Menge kann nicht reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="2b766-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="2b766-108">Die Anzahl der Lagerbuchungen auf Bestellung ist zu gering, weil die Menge oder ein Teil davon von einem Ausgabeauftrag oder einem Produktionsauftrag referenziert wird oder gegen andere Buchungen gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="2b766-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="2b766-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="2b766-109">Cause</span></span>

<span data-ttu-id="2b766-110">Wenn einem Auftrag eine Arbeit zugeordnet ist, können Sie den Auftrag erst stornieren, wenn die Arbeit storniert und entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="2b766-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="2b766-111">Diese Anforderung gilt auch dann, wenn die mit dem Auftrag verbundene Arbeit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2b766-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="2b766-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="2b766-112">Resolution</span></span>

<span data-ttu-id="2b766-113">Um dieses Problem zu beheben, führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="2b766-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="2b766-114">Offene Arbeit abbrechen.</span><span class="sxs-lookup"><span data-stu-id="2b766-114">Cancel open work.</span></span>
1. <span data-ttu-id="2b766-115">Löschen Sie die Auslastung.</span><span class="sxs-lookup"><span data-stu-id="2b766-115">Delete the load.</span></span>
1. <span data-ttu-id="2b766-116">Die entnommenen Mengen reduzieren.</span><span class="sxs-lookup"><span data-stu-id="2b766-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="2b766-117">Offene Arbeit abbrechen</span><span class="sxs-lookup"><span data-stu-id="2b766-117">Cancel open work</span></span>

<span data-ttu-id="2b766-118">Um die offene Arbeit abzubrechen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="2b766-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="2b766-119">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="2b766-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="2b766-120">Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie stornieren möchten und die derzeit einen **Arbeitsstatus**-Wert von *Offen*, *In Bearbeitung*, *Abgebrochen*, *Zusammengeführt* oder *Geschlossen* hat.</span><span class="sxs-lookup"><span data-stu-id="2b766-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="2b766-121">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2b766-121">Select **OK**.</span></span>
1. <span data-ttu-id="2b766-122">Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="2b766-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="2b766-123">Die Auslastung löschen</span><span class="sxs-lookup"><span data-stu-id="2b766-123">Delete the load</span></span>

<span data-ttu-id="2b766-124">Um eine Auslastung zu löschen, tun Sie Folgendes.</span><span class="sxs-lookup"><span data-stu-id="2b766-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="2b766-125">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="2b766-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2b766-126">Öffnen Sie den entsprechenden Auftrag.</span><span class="sxs-lookup"><span data-stu-id="2b766-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="2b766-127">Wählen Sie auf dem Inforegister **Auftragspositionen** **Lagerort \> Arbeitsdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="2b766-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="2b766-128">Wählen Sie auf der Seite **Arbeit** im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Arbeit aufteilen**.</span><span class="sxs-lookup"><span data-stu-id="2b766-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="2b766-129">Bestätigen Sie, dass das Feld **Arbeitsstatus** auf *Storniert* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="2b766-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="2b766-130">Schließen Sie die Seite **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="2b766-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="2b766-131">Wählen Sie auf der Auftragsdetailseite im Inforegister **Auftragspositionen** **Lagerort \> Details laden**.</span><span class="sxs-lookup"><span data-stu-id="2b766-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="2b766-132">Wählen Sie im Aktivitätsbereich **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="2b766-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="2b766-133">Wählen Sie **Ja**, um zu bestätigen, dass Sie die Auslastung löschen wollen.</span><span class="sxs-lookup"><span data-stu-id="2b766-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="2b766-134">Schließen Sie die Seite **Auslastung**.</span><span class="sxs-lookup"><span data-stu-id="2b766-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="2b766-135">Die entnommenen Mengen reduzieren</span><span class="sxs-lookup"><span data-stu-id="2b766-135">Reduce the picked quantity</span></span>

<span data-ttu-id="2b766-136">Nachdem alle Arbeiten storniert wurden, führen Sie diese Schritte aus, um die kommissionierte Menge zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="2b766-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="2b766-137">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="2b766-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2b766-138">Öffnen Sie den entsprechenden Auftrag.</span><span class="sxs-lookup"><span data-stu-id="2b766-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="2b766-139">Wählen Sie im Inforegister **Auftragspositionen** **Position aktualisieren \> Wählen** aus der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="2b766-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="2b766-140">Wählen Sie auf der Seite **Wählen** im Abschnitt **Transaktionen** die Zeile aus, in der das Feld **Problemstatus** auf *Ausgewählt* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="2b766-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="2b766-141">Wählen Sie im Abschnitt **Transaktionen** **Entnahmeposition hinzufügen** aus der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="2b766-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="2b766-142">Wählen Sie im Abschnitt **Entnahmeposition** **Alle entnehmen bestätigen** aus der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="2b766-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="2b766-143">Schließen Sie die Seite **Wählen**.</span><span class="sxs-lookup"><span data-stu-id="2b766-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="2b766-144">Auf der Seite Auftragsdetails im Aktivitätsbereich, auf der Registerkarte **Auftrag** in der Gruppe **Verwalten** wählen Sie **Abbrechen** aus.</span><span class="sxs-lookup"><span data-stu-id="2b766-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="2b766-145">Wählen Sie **Ja**, um zu bestätigen, dass Sie den Auftrag abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="2b766-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
