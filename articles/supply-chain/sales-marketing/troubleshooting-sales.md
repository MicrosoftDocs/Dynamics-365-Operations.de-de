---
title: Fehlerbehebung bei Aufträgen
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Aufträgen auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974784"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="c660b-103">Fehlerbehebung bei Aufträgen</span><span class="sxs-lookup"><span data-stu-id="c660b-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="c660b-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Aufträgen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="c660b-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="c660b-105">Die Steuerinformationen werden nicht aktualisiert, wenn ich den Standort in einem Auftragskopf ändere.</span><span class="sxs-lookup"><span data-stu-id="c660b-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c660b-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="c660b-106">Issue description</span></span>

<span data-ttu-id="c660b-107">Wenn der Standort, das Lager oder die Lieferadresse entweder in einem Auftragskopf oder auf Positionsebene geändert wird, werden die Fallsteuerinformationen für die Positionen nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c660b-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c660b-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="c660b-108">Issue resolution</span></span>

<span data-ttu-id="c660b-109">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="c660b-109">This behavior is by design.</span></span> <span data-ttu-id="c660b-110">Das Problem tritt auf, weil die Lieferadresse, der Standort und das Lager nicht auch automatisch auf Positionsebene geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c660b-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="c660b-111">Sie müssen sie manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c660b-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="c660b-112">Wenn es zwei Handelsvereinbarungen für denselben Zeitraum oder überlappende Zeiträume gibt, wird immer dieselbe Vertragsposition ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c660b-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c660b-113">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="c660b-113">Issue description</span></span>

<span data-ttu-id="c660b-114">Wenn zwei Handelsvereinbarungen für denselben Zeitraum oder überlappende Zeiträume definiert sind, scheint jedes Mal, wenn Sie Auftragspositionen erstellen, die diese Artikel enthalten, dieselbe Handelsvereinbarung ausgewählt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c660b-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c660b-115">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="c660b-115">Issue resolution</span></span>

<span data-ttu-id="c660b-116">Wenn es für ein bestimmtes Datum mehr als eine Handelsvereinbarung gibt, wird immer die Handelsvereinbarung mit dem niedrigsten Preis ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c660b-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="c660b-117">Laden Sie für weitere Informationen das folgende Whitepaper herunter: [Handelsvereinbarungen in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="c660b-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="c660b-118">Kann ich eine Bestellung mit einem Auftrag verknüpfen, um die Nachfrage zu befriedigen?</span><span class="sxs-lookup"><span data-stu-id="c660b-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="c660b-119">Sie können einer Bestellung auf Grundlage eines Auftrags erstellen.</span><span class="sxs-lookup"><span data-stu-id="c660b-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="c660b-120">Weitere Informationen finden Sie unter [Erstellen einer Bestellung auf Grundlage eines Auftrags](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="c660b-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="c660b-121">Ich kann eine Rücklieferung oder einen Auftrag nicht stornieren oder löschen.</span><span class="sxs-lookup"><span data-stu-id="c660b-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="c660b-122">Sie können nur Aufträge und Rücklieferungsaufträge stornieren, die sich im *Erstellt*-Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="c660b-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="c660b-123">Weitere Informationen finden Sie unter [Stornieren einer Rücklieferung](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="c660b-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="c660b-124">Wenn ich versuche, einen Auftrag zu stornieren, wird der Fehler „Reservierungen können nicht entfernt werden, da Arbeiten erstellt wurden, die auf den Reservierungen beruhen“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c660b-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="c660b-125">Fehlercode: WAX4661</span><span class="sxs-lookup"><span data-stu-id="c660b-125">Error code: WAX4661</span></span>

<span data-ttu-id="c660b-126">Wenn einem Auftrag eine Arbeit zugeordnet ist, können Sie den Auftrag erst stornieren, wenn die Arbeit storniert und entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="c660b-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="c660b-127">Diese Anforderung gilt auch dann, wenn die mit dem Auftrag verbundene Arbeit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c660b-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="c660b-128">Führen Sie folgende Schritte aus, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="c660b-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="c660b-129">Stornieren Sie die Arbeit ab und legen Sie den Bestand wieder an den gewünschten Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="c660b-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="c660b-130">Gehen Sie zur entsprechenden Auslastung des Auftrags und wählen Sie entweder **Entnommene Menge reduzieren** auf der Ladungsposition oder **Arbeit stornieren** im Aktionsbereich.</span><span class="sxs-lookup"><span data-stu-id="c660b-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="c660b-131">Die Arbeit hat jetzt den Status *Storniert* und neue Bestandsbewegungsarbeiten werden automatisch erstellt und verarbeitet, um den Bestand wieder an den Lagerplatz zu bringen, der zum Zeitpunkt der Stornierung beschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="c660b-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="c660b-132">Löschen Sie die Auslastung.</span><span class="sxs-lookup"><span data-stu-id="c660b-132">Delete the load.</span></span> <span data-ttu-id="c660b-133">Die Lieferung wird ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c660b-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="c660b-134">Sie sollten nun in der Lage sein, zum Auftrag zu gehen und ihn zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="c660b-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="c660b-135">Ich kann eine Intercompany-Bestellung, die mit einem Auftrag verknüpft ist, nicht stornieren.</span><span class="sxs-lookup"><span data-stu-id="c660b-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c660b-136">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="c660b-136">Issue description</span></span>

<span data-ttu-id="c660b-137">Wenn Sie versuchen, eine Intercompany-Bestellung zu stornieren, die mit einem Kundenauftrag verknüpft ist, wird möglicherweise die folgende Fehlermeldung angezeigt: „Die Menge kann nicht reduziert werden, da die verbleibende Aktualisierungsmenge das Vorzeichen ändert.“</span><span class="sxs-lookup"><span data-stu-id="c660b-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c660b-138">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="c660b-138">Issue resolution</span></span>

<span data-ttu-id="c660b-139">Dieses Problem wurde in Microsoft Dynamics 365 Supply Chain Management Version 10.0.13 behoben.</span><span class="sxs-lookup"><span data-stu-id="c660b-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="c660b-140">In dieser und späteren Versionen können Sie jetzt eine Intercompany-Bestellung stornieren, die mit einem Kundenauftrag verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c660b-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="c660b-141">Kann ich einen in Rechnung gestellten Auftrag wiederherstellen, der gelöscht wurde?</span><span class="sxs-lookup"><span data-stu-id="c660b-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="c660b-142">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="c660b-142">Issue description</span></span>

<span data-ttu-id="c660b-143">Ein in Rechnung gestellter Auftrag wurde versehentlich gelöscht, und Sie möchten ihn wiederherstellen oder seine Details anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c660b-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c660b-144">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="c660b-144">Issue resolution</span></span>

<span data-ttu-id="c660b-145">Wenn der gelöschte Auftrag bereits in Rechnung gestellt wurde, gehen Sie zu **Kundenkonto \> Transaktionen \> Originaldokument \>Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="c660b-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="c660b-146">Suchen Sie die gesuchte Rechnung und wählen Sie sie aus, um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c660b-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="c660b-147">Diese Details enthalten die Auftragsreferenz.</span><span class="sxs-lookup"><span data-stu-id="c660b-147">These details include the sales order reference.</span></span> <span data-ttu-id="c660b-148">Sie sollten von der Seite auch auf die Auftragsdetails zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="c660b-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="c660b-149">Die Frist eines Auftragskopfes kann nicht in der SalesOrderHeaderV2Entity-Datenentität gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c660b-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="c660b-150">Das Fristfeld existiert auf der *SalesOrderHeaderV2Entity*-Entität nicht.</span><span class="sxs-lookup"><span data-stu-id="c660b-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="c660b-151">Ich muss verwaiste Auftragsdatensätze löschen.</span><span class="sxs-lookup"><span data-stu-id="c660b-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="c660b-152">Führen Sie den periodischen Einzelvorgang *Auftragslöschung* aus, um verwaiste Auftragsdatensätze zu bereinigen, indem Sie zu einem der folgenden Orte gehen:</span><span class="sxs-lookup"><span data-stu-id="c660b-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="c660b-153">Klicken Sie auf Vertrieb und Marketing \> Periodische Aufgaben \> Bereinigen \> Aufträge löschen</span><span class="sxs-lookup"><span data-stu-id="c660b-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="c660b-154">Retail und Commerce \> Retail und Commerce IT \> Bereinigen \> Aufträge löschen</span><span class="sxs-lookup"><span data-stu-id="c660b-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="c660b-155">Gibt es eine Möglichkeit, Provisionen für bereits gebuchte Rechnungen zu berechnen?</span><span class="sxs-lookup"><span data-stu-id="c660b-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="c660b-156">Supply Chain Management unterstützt derzeit die Berechnung von Provisionen für gebuchte Rechnungen nicht.</span><span class="sxs-lookup"><span data-stu-id="c660b-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="c660b-157">Ein Bündelartikel wird in einem Intercompany-Prozess nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c660b-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="c660b-158">Der Bündelartikel ist für die Bestellung nicht verfügbar, da Sie bei Prüfung der Auftragspositionen für den Bündelartikel feststellen werden, dass die Menge *0* (Null) und der Status *Storniert* ist.</span><span class="sxs-lookup"><span data-stu-id="c660b-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="c660b-159">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="c660b-159">This behavior is by design.</span></span> <span data-ttu-id="c660b-160">Der Auftrag kauft nur die Komponenten des Bündelartikels.</span><span class="sxs-lookup"><span data-stu-id="c660b-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="c660b-161">Der Bündelartikel selbst wird nicht gekauft.</span><span class="sxs-lookup"><span data-stu-id="c660b-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="c660b-162">Wenn Sie ein Bündel kaufen müssen, prüfen Sie, ob Sie es als Bündelartikel markieren müssen, da diese Funktion für Szenarien zur Umsatzrealisierung konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="c660b-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="c660b-163">Weitere Informationen zu Bündelartikeln finden Sie unter [Bündel](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="c660b-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
