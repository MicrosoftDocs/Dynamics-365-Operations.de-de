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
ms.search.form: SalesTable, SalesTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889456"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="db0a9-103">Fehlerbehebung bei Aufträgen</span><span class="sxs-lookup"><span data-stu-id="db0a9-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="db0a9-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Aufträgen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="db0a9-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="db0a9-105">Die Steuerinformationen werden nicht aktualisiert, wenn ich den Standort in einem Auftragskopf ändere.</span><span class="sxs-lookup"><span data-stu-id="db0a9-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="db0a9-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="db0a9-106">Issue description</span></span>

<span data-ttu-id="db0a9-107">Wenn der Standort, das Lager oder die Lieferadresse entweder in einem Auftragskopf oder auf Positionsebene geändert wird, werden die Fallsteuerinformationen für die Positionen nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="db0a9-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db0a9-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="db0a9-108">Issue resolution</span></span>

<span data-ttu-id="db0a9-109">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="db0a9-109">This behavior is by design.</span></span> <span data-ttu-id="db0a9-110">Das Problem tritt auf, weil die Lieferadresse, der Standort und das Lager nicht auch automatisch auf Positionsebene geändert werden.</span><span class="sxs-lookup"><span data-stu-id="db0a9-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="db0a9-111">Sie müssen sie manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db0a9-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="db0a9-112">Wenn es zwei Handelsvereinbarungen für denselben Zeitraum oder überlappende Zeiträume gibt, wird immer dieselbe Vertragsposition ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="db0a9-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="db0a9-113">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="db0a9-113">Issue description</span></span>

<span data-ttu-id="db0a9-114">Wenn zwei Handelsvereinbarungen für denselben Zeitraum oder überlappende Zeiträume definiert sind, scheint jedes Mal, wenn Sie Auftragspositionen erstellen, die diese Artikel enthalten, dieselbe Handelsvereinbarung ausgewählt zu werden.</span><span class="sxs-lookup"><span data-stu-id="db0a9-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db0a9-115">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="db0a9-115">Issue resolution</span></span>

<span data-ttu-id="db0a9-116">Wenn es für ein bestimmtes Datum mehr als eine Handelsvereinbarung gibt, wird immer die Handelsvereinbarung mit dem niedrigsten Preis ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="db0a9-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="db0a9-117">Laden Sie für weitere Informationen das folgende Whitepaper herunter: [Handelsvereinbarungen in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="db0a9-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="db0a9-118">Kann ich eine Bestellung mit einem Auftrag verknüpfen, um die Nachfrage zu befriedigen?</span><span class="sxs-lookup"><span data-stu-id="db0a9-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="db0a9-119">Sie können einer Bestellung auf Grundlage eines Auftrags erstellen.</span><span class="sxs-lookup"><span data-stu-id="db0a9-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="db0a9-120">Weitere Informationen finden Sie unter [Erstellen einer Bestellung auf Grundlage eines Auftrags](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="db0a9-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="db0a9-121">Ich kann eine Rücklieferung oder einen Auftrag nicht stornieren oder löschen.</span><span class="sxs-lookup"><span data-stu-id="db0a9-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="db0a9-122">Sie können nur Aufträge und Rücklieferungsaufträge stornieren, die sich im *Erstellt*-Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="db0a9-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="db0a9-123">Weitere Informationen finden Sie unter [Stornieren einer Rücklieferung](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="db0a9-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="db0a9-124">Wenn ich versuche, einen Auftrag zu stornieren, wird der Fehler „Reservierungen können nicht entfernt werden, da Arbeiten erstellt wurden, die auf den Reservierungen beruhen“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db0a9-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="db0a9-125">Wenn einem Auftrag eine Arbeit zugeordnet ist, können Sie den Auftrag erst stornieren, wenn die Arbeit storniert und entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="db0a9-125">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="db0a9-126">Diese Anforderung gilt auch dann, wenn die mit dem Auftrag verbundene Arbeit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="db0a9-126">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="db0a9-127">Führen Sie folgende Schritte aus, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="db0a9-127">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="db0a9-128">Stornieren Sie die Arbeit ab und legen Sie den Bestand wieder an den gewünschten Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="db0a9-128">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="db0a9-129">Gehen Sie zur entsprechenden Auslastung des Auftrags und wählen Sie entweder **Entnommene Menge reduzieren** auf der Ladungsposition oder **Arbeit stornieren** im Aktionsbereich.</span><span class="sxs-lookup"><span data-stu-id="db0a9-129">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="db0a9-130">Die Arbeit hat jetzt den Status *Storniert* und neue Bestandsbewegungsarbeiten werden automatisch erstellt und verarbeitet, um den Bestand wieder an den Lagerplatz zu bringen, der zum Zeitpunkt der Stornierung beschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="db0a9-130">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="db0a9-131">Löschen Sie die Auslastung.</span><span class="sxs-lookup"><span data-stu-id="db0a9-131">Delete the load.</span></span> <span data-ttu-id="db0a9-132">Die Lieferung wird ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="db0a9-132">The shipment is also deleted.</span></span>
3. <span data-ttu-id="db0a9-133">Sie sollten nun in der Lage sein, zum Auftrag zu gehen und ihn zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="db0a9-133">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="db0a9-134">Ich kann eine Intercompany-Bestellung, die mit einem Auftrag verknüpft ist, nicht stornieren.</span><span class="sxs-lookup"><span data-stu-id="db0a9-134">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="db0a9-135">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="db0a9-135">Issue description</span></span>

<span data-ttu-id="db0a9-136">Wenn Sie versuchen, eine Intercompany-Bestellung zu stornieren, die mit einem Kundenauftrag verknüpft ist, wird möglicherweise die folgende Fehlermeldung angezeigt: „Die Menge kann nicht reduziert werden, da die verbleibende Aktualisierungsmenge das Vorzeichen ändert.“</span><span class="sxs-lookup"><span data-stu-id="db0a9-136">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db0a9-137">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="db0a9-137">Issue resolution</span></span>

<span data-ttu-id="db0a9-138">Dieses Problem wurde in Microsoft Dynamics 365 Supply Chain Management Version 10.0.13 behoben.</span><span class="sxs-lookup"><span data-stu-id="db0a9-138">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="db0a9-139">In dieser und späteren Versionen können Sie jetzt eine Intercompany-Bestellung stornieren, die mit einem Kundenauftrag verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="db0a9-139">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="db0a9-140">Kann ich einen in Rechnung gestellten Auftrag wiederherstellen, der gelöscht wurde?</span><span class="sxs-lookup"><span data-stu-id="db0a9-140">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="db0a9-141">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="db0a9-141">Issue description</span></span>

<span data-ttu-id="db0a9-142">Ein in Rechnung gestellter Auftrag wurde versehentlich gelöscht, und Sie möchten ihn wiederherstellen oder seine Details anzeigen.</span><span class="sxs-lookup"><span data-stu-id="db0a9-142">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db0a9-143">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="db0a9-143">Issue resolution</span></span>

<span data-ttu-id="db0a9-144">Wenn der gelöschte Auftrag bereits in Rechnung gestellt wurde, gehen Sie zu **Kundenkonto \> Transaktionen \> Originaldokument \>Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="db0a9-144">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="db0a9-145">Suchen Sie die gesuchte Rechnung und wählen Sie sie aus, um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="db0a9-145">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="db0a9-146">Diese Details enthalten die Auftragsreferenz.</span><span class="sxs-lookup"><span data-stu-id="db0a9-146">These details include the sales order reference.</span></span> <span data-ttu-id="db0a9-147">Sie sollten von der Seite auch auf die Auftragsdetails zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="db0a9-147">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="db0a9-148">Die Frist eines Auftragskopfes kann nicht in der SalesOrderHeaderV2Entity-Datenentität gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="db0a9-148">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="db0a9-149">Das Fristfeld existiert auf der *SalesOrderHeaderV2Entity*-Entität nicht.</span><span class="sxs-lookup"><span data-stu-id="db0a9-149">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="db0a9-150">Ich muss verwaiste Auftragsdatensätze löschen.</span><span class="sxs-lookup"><span data-stu-id="db0a9-150">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="db0a9-151">Führen Sie den periodischen Einzelvorgang *Auftragslöschung* aus, um verwaiste Auftragsdatensätze zu bereinigen, indem Sie zu einem der folgenden Orte gehen:</span><span class="sxs-lookup"><span data-stu-id="db0a9-151">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="db0a9-152">Klicken Sie auf Vertrieb und Marketing \> Periodische Aufgaben \> Bereinigen \> Aufträge löschen</span><span class="sxs-lookup"><span data-stu-id="db0a9-152">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="db0a9-153">Retail und Commerce \> Retail und Commerce IT \> Bereinigen \> Aufträge löschen</span><span class="sxs-lookup"><span data-stu-id="db0a9-153">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="db0a9-154">Gibt es eine Möglichkeit, Provisionen für bereits gebuchte Rechnungen zu berechnen?</span><span class="sxs-lookup"><span data-stu-id="db0a9-154">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="db0a9-155">Supply Chain Management unterstützt derzeit die Berechnung von Provisionen für gebuchte Rechnungen nicht.</span><span class="sxs-lookup"><span data-stu-id="db0a9-155">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="db0a9-156">Ein Bündelartikel wird in einem Intercompany-Prozess nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db0a9-156">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="db0a9-157">Der Bündelartikel ist für die Bestellung nicht verfügbar, da Sie bei Prüfung der Auftragspositionen für den Bündelartikel feststellen, dass die Menge *0* (Null) und der Status *Storniert* ist.</span><span class="sxs-lookup"><span data-stu-id="db0a9-157">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Cancelled*.</span></span> <span data-ttu-id="db0a9-158">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="db0a9-158">This behavior is by design.</span></span> <span data-ttu-id="db0a9-159">Der Auftrag kauft nur die Komponenten des Bündelartikels.</span><span class="sxs-lookup"><span data-stu-id="db0a9-159">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="db0a9-160">Der Bündelartikel selbst wird nicht gekauft.</span><span class="sxs-lookup"><span data-stu-id="db0a9-160">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="db0a9-161">Wenn Sie ein Bündel kaufen müssen, prüfen Sie, ob Sie ihn als Bündelartikel markieren müssen, da diese Funktionalität tatsächlich für Szenarien zur Umsatzrealisierung konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="db0a9-161">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is actually designed for revenue recognition scenarios.</span></span> <span data-ttu-id="db0a9-162">Weitere Informationen zu Bündelartikeln finden Sie unter [Bündel](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="db0a9-162">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
