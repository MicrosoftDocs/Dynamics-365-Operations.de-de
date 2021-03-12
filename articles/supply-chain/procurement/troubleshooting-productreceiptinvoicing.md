---
title: Fehlerbehebung bei Produktzugängen und Fakturierung
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Produktzugängen und Fakturierung auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 22b1abec0c6dd5f571e604c5c07379b397b8bdaa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999052"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="a0bc2-103">Fehlerbehebung bei Produktzugängen und Fakturierung</span><span class="sxs-lookup"><span data-stu-id="a0bc2-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="a0bc2-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Produktzugängen und Fakturierung auftreten können.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="a0bc2-105">Ich kann nicht mehr als eine Rechnung für eine Bestellposition mit kategorienbasierten Artikeln buchen.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="a0bc2-106">Eine Menge ist obligatorisch, wenn Sie Rechnungen buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="a0bc2-107">Wenn die gesamte Menge einer Position nur für einen Teilbetrag in Rechnung gestellt wurde, können Sie den verbleibenden Betrag nicht auf einer anderen Rechnung in Rechnung stellen.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="a0bc2-108">Während der Bestellbestätigung wird der Fehler „Objektreferenz nicht festgelegt“ angezeigt, oder während der Buchung der Lieferantenrechnung tritt die Ausnahme „Ausnahme wurde vom Ziel eines Aufrufs ausgelöst“ auf.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="a0bc2-109">Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="a0bc2-110">So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="a0bc2-111">Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="a0bc2-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="a0bc2-112">Ich kann nicht mehrere Produktzugänge in einer einzigen Bestellung zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="a0bc2-113">Sie können nicht mehrere Produktzugänge in einer Bestellung zusammenfassen, wenn die verschiedenen Produktzugangspositionen unterschiedliche Abrechnungsdaten haben.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="a0bc2-114">In früheren Versionen von Microsoft Dynamics 365 Supply Chain Management war in dieser Situation eine Konsolidierung zulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="a0bc2-115">Die Praxis ist jedoch fehleranfällig.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-115">However, the practice is prone to error.</span></span> <span data-ttu-id="a0bc2-116">Das Abrechnungsdatum in den erstellten Bestellpositionen sollte nicht vom Abrechnungsdatum in den Produktzugangspositionen abweichen, aus denen diese Bestellpositionen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="a0bc2-117">(Das Abrechnungsdatum in den Bestellpositionen stimmt mit dem Abrechnungsdatum im Bestellkopf überein.) Daher ist die Konsolidierung mehrerer Produkteingänge zu einer einzigen Bestellung nicht mehr zulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="a0bc2-118">Das Abrechnungsdatum wird beispielsweise für Budgetreservierungen und Belastungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="a0bc2-119">Daher sollte es beim Übergang vom Produktzugang zur Bestellung beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="a0bc2-120">Wenn Produktzugänge storniert werden, können Transaktionen auf ein gesperrtes Sachkonto gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a0bc2-121">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="a0bc2-121">Issue description</span></span>

<span data-ttu-id="a0bc2-122">Wenn ein Produktzugang storniert wird, können Transaktionen auf gesperrte Sachkonten gebucht werden, obwohl die Hauptkonten gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="a0bc2-123">Reproduzieren Sie das Problem</span><span class="sxs-lookup"><span data-stu-id="a0bc2-123">Reproduce the issue</span></span>

<span data-ttu-id="a0bc2-124">Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="a0bc2-125">Stellen Sie auf der **Lieferantenparameter**-Seite auf der Registerkarte **Allgemeines** sicher, dass die **Produktzugang auf Sachkonto buchen**-Option auf *Ja* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="a0bc2-126">Erstellen Sie eine Bestellung und fügen Sie eine Bestellposition mit einer Menge von *1.000* für ein Produkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="a0bc2-127">Bestätigen Sie die Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="a0bc2-128">Buchen Sie den Produktzugang und überprüfen Sie die Gutscheine.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="a0bc2-129">Sperren Sie die relevanten Hauptkonten *200140* und *140200*.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="a0bc2-130">Stornieren Sie den gebuchten Produktzugang.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="a0bc2-131">Beachten Sie, dass Transaktionen auf die gesperrten Sachkonten gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a0bc2-132">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="a0bc2-132">Issue resolution</span></span>

<span data-ttu-id="a0bc2-133">Transaktionen können auf die gesperrten Sachkonten gebucht werden, wenn Produktbelege storniert werden, da dieses Verhalten korrekte Buchungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="a0bc2-134">Eine Produktzugangs-Belegnummer wird verbraucht, auch wenn während des Produktzugangs kein Finanzbeleg generiert wird.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="a0bc2-135">Wenn die **Verbindlichkeiten bei Produktzugang abgrenzen**-Option für die Artikelmodellgruppe auf *Nein* festgelegt ist, werden keine Buchungen im Hauptbuch vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="a0bc2-136">Ein physisches Ereignis wird jedoch zum Zwecke der Abrechnung in einem Nebenbuch aufgezeichnet, und für dieses Ereignis ist eine Belegnummer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="a0bc2-137">Diese Belegnummer ist die Belegnummer, auf die in den Bestandstransaktionen verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="a0bc2-138">Wir empfehlen Ihnen, die **Verbindlichkeiten bei Produktzugang abgrenzen**-Option auf *Ja* festzulegen, wie im folgenden Blogbeitrag beschrieben: [Sonstige Zuschläge zum Zeitpunkt des Produktzugangs buchen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="a0bc2-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="a0bc2-139">Das Konto „Auf Belastungskonto im Sachkonto buchen“-Einstellung ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a0bc2-140">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="a0bc2-140">Issue description</span></span>

<span data-ttu-id="a0bc2-141">Dieses Problem tritt auf, wenn eine Bestellung in Rechnung gestellt wird, wenn die **Auf Belastungskonto im Sachkonto buchen**-Option auf der **Rechnung**-Registerkarte der **Lieferantenparameter**-Seite auf *Ja* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="a0bc2-142">Reproduzieren Sie das Problem</span><span class="sxs-lookup"><span data-stu-id="a0bc2-142">Reproduce the issue</span></span>

<span data-ttu-id="a0bc2-143">Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="a0bc2-144">Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="a0bc2-145">Legen Sie auf der **Rechnung**-Registerkarte die **Auf Belastungskonto im Sachkonto buchen**-Option auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="a0bc2-146">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Buchung \> Buchung**.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="a0bc2-147">Stellen Sie auf der **Bestellung**-Registerkarte sicher, dass Sie alle Positionen in den Kaufausgaben für das Produkt gelöscht haben.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="a0bc2-148">Wechseln Sie zu **Kreditorenkonten \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="a0bc2-149">Erstellen einer Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-149">Create a purchase order.</span></span> <span data-ttu-id="a0bc2-150">Wählen Sie in dem **Lieferantenkonto**-Feld *1001 Acme Büromaterial* aus.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="a0bc2-151">Fügen Sie eine Bestellung mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="a0bc2-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="a0bc2-152">**Artikelnummer:** *D0011 Laserprojektor*</span><span class="sxs-lookup"><span data-stu-id="a0bc2-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="a0bc2-153">**Standort:** *1*</span><span class="sxs-lookup"><span data-stu-id="a0bc2-153">**Site:** *1*</span></span>
    - <span data-ttu-id="a0bc2-154">**Lagerort:** *11*</span><span class="sxs-lookup"><span data-stu-id="a0bc2-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="a0bc2-155">**Menge** *4*</span><span class="sxs-lookup"><span data-stu-id="a0bc2-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="a0bc2-156">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kauf** in der Gruppe **Aktion** auf **Bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="a0bc2-157">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Empfangen** in der Gruppe **Generieren** auf **Produktzugang**.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="a0bc2-158">Geben Sie im **Buchen des Produktzugangs**-Dialogfeld im **Produktzugang**-Feld eine beliebige Zahl ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="a0bc2-159">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="a0bc2-160">Geben Sie im **Nummer**-Feld eine beliebige Nummer als Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="a0bc2-161">Status des Abgleichs aktualisieren und buchen.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="a0bc2-162">Beachten Sie, dass Sie jetzt die folgende Fehlermeldung erhalten, wenn Sie eine Rechnung aus einer Bestellung erstellen: „Kontonummer für den Transaktionstyp Einkaufsausgaben für Produkt ist nicht vorhanden.“</span><span class="sxs-lookup"><span data-stu-id="a0bc2-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a0bc2-163">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="a0bc2-163">Issue resolution</span></span>

<span data-ttu-id="a0bc2-164">Dies hängt von den Parametereinstellungen für Rechnungen und Rechnungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="a0bc2-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="a0bc2-165">Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Buchhaltung für Einkaufskosten und Bestandsabweichungen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="a0bc2-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
