---
title: Fehlerbehebung bei Bestellungen
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Bestellungen auftreten können.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018559"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="f0d08-103">Fehlerbehebung bei Bestellungen</span><span class="sxs-lookup"><span data-stu-id="f0d08-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="f0d08-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Bestellungen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f0d08-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="f0d08-105">Eine Aktion kann erst abgeschlossen werden, nachdem die Positionsnummer vollständig verteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="f0d08-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="f0d08-106">Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="f0d08-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="f0d08-107">So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf* -Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**.</span><span class="sxs-lookup"><span data-stu-id="f0d08-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="f0d08-108">Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="f0d08-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="f0d08-109">Wenn Bestellungen über die Datenverwaltung importiert werden, folgen die Bestellpositionsnummern nicht dem in den Systemparametern definierten Inkrement.</span><span class="sxs-lookup"><span data-stu-id="f0d08-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f0d08-110">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d08-110">Issue description</span></span>

<span data-ttu-id="f0d08-111">Standardmäßig verwenden automatisch generierte Positionsnummern für Bestellpositionen, die über die *Bestellpositionen V2* -Datenentität importiert werden nicht das in den Systemparametern angegebene Systempositionsnummerninkrement.</span><span class="sxs-lookup"><span data-stu-id="f0d08-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="f0d08-112">Wenn Sie manuell eine Bestellung erstellen und Positionen über die Benutzeroberfläche hinzufügen, werden die Positionsnummern korrekt erhöht.</span><span class="sxs-lookup"><span data-stu-id="f0d08-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="f0d08-113">Wenn Sie jedoch das Datenverwaltungs-Framework (DMF) verwenden, werden sie nicht korrekt inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="f0d08-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="f0d08-114">Dieses Problem tritt auf, weil das System beim Importieren von Positionen über DMF die DMF-Methode zum Zuweisen verwendet, wenn in der importierten Entität noch keine Positionsnummern zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="f0d08-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="f0d08-115">Diese Methode erhöht die Positionsnummern immer um eins.</span><span class="sxs-lookup"><span data-stu-id="f0d08-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="f0d08-116">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="f0d08-116">Issue workaround</span></span>

<span data-ttu-id="f0d08-117">Stellen Sie sicher, dass die gewünschten Positionsnummern bereits in den Feldern für Positionsnummern der Datenentität angegeben sind, wenn Sie die Bestellpositionen importieren.</span><span class="sxs-lookup"><span data-stu-id="f0d08-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="f0d08-118">In diesem Fall überschreibt DMF die Positionsnummern nicht.</span><span class="sxs-lookup"><span data-stu-id="f0d08-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="f0d08-119">Eine Standardsteuergruppe und ein Standard-Skonto werden nicht vom Rechnungskonto ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="f0d08-120">Wenn Sie ein vom Kundenkonto abweichendes Rechnungskonto verwenden, werden beim Erstellen einer Bestellung weder eine Standardsteuergruppe noch ein Standard-Skonto vom Rechnungskonto ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="f0d08-121">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-121">This behavior is by design.</span></span> <span data-ttu-id="f0d08-122">Die Standardwerte für die Steuergruppe, Skonti und andere Preisinformationen basieren auf dem Kundenkonto und nicht auf dem Rechnungskonto.</span><span class="sxs-lookup"><span data-stu-id="f0d08-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="f0d08-123">Während der Bestellbestätigung wird der Fehler „Objektreferenz nicht festgelegt“ angezeigt, oder während der Buchung der Lieferantenrechnung tritt die Ausnahme „Ausnahme wurde vom Ziel eines Aufrufs ausgelöst“ auf.</span><span class="sxs-lookup"><span data-stu-id="f0d08-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="f0d08-124">Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="f0d08-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="f0d08-125">So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf* -Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**.</span><span class="sxs-lookup"><span data-stu-id="f0d08-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="f0d08-126">Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="f0d08-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="f0d08-127">Eine oder mehrere Buchhaltungsverteilungen sind entweder über- oder unterverteilt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f0d08-128">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d08-128">Issue description</span></span>

<span data-ttu-id="f0d08-129">Sie erhalten folgenden Fehler: „Mindestens eine Buchhaltungsverteilungen ist entweder über- oder unterverteilt.“</span><span class="sxs-lookup"><span data-stu-id="f0d08-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f0d08-130">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="f0d08-130">Issue resolution</span></span>

<span data-ttu-id="f0d08-131">Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="f0d08-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="f0d08-132">So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf* -Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**.</span><span class="sxs-lookup"><span data-stu-id="f0d08-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="f0d08-133">Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="f0d08-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="f0d08-134">Kann ich nur Bestellungen anzeigen, die ich erstellt habe?</span><span class="sxs-lookup"><span data-stu-id="f0d08-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="f0d08-135">Diese Funktionalität ist derzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0d08-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="f0d08-136">Kann ich Bestand reservieren und Transaktionen mit dem registrierten Bestand einer Bestellung erstellen?</span><span class="sxs-lookup"><span data-stu-id="f0d08-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="f0d08-137">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d08-137">Issue description</span></span>

<span data-ttu-id="f0d08-138">Auch wenn Artikel in einem *Erfasst* -Zustand auf einer Bestellung sind, können Sie den Bestand trotzdem reservieren.</span><span class="sxs-lookup"><span data-stu-id="f0d08-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="f0d08-139">Mit anderen Worten, Sie können Transaktionen für den registrierten Bestand erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0d08-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="f0d08-140">Reproduzieren Sie das Problem</span><span class="sxs-lookup"><span data-stu-id="f0d08-140">Reproduce the issue</span></span>

<span data-ttu-id="f0d08-141">Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="f0d08-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="f0d08-142">Erstellen einer Bestellung.</span><span class="sxs-lookup"><span data-stu-id="f0d08-142">Create a purchase order.</span></span>
2. <span data-ttu-id="f0d08-143">Registrieren Sie die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="f0d08-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="f0d08-144">Beachten Sie, dass Sie Reservierungen oder Transaktionen für den registrierten Bestand generieren können.</span><span class="sxs-lookup"><span data-stu-id="f0d08-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f0d08-145">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="f0d08-145">Issue resolution</span></span>

<span data-ttu-id="f0d08-146">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-146">This behavior is by design.</span></span> <span data-ttu-id="f0d08-147">Es wird erwartet, dass die registrierten Artikel physisch im Lagerort oder im Bestand angekommen sind und daher für eine Reservierung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f0d08-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="f0d08-148">Bestellungen spiegeln nicht die Spracheinstellungen der juristischen Person wider.</span><span class="sxs-lookup"><span data-stu-id="f0d08-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f0d08-149">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d08-149">Issue description</span></span>

<span data-ttu-id="f0d08-150">Der Produktname einer Bestellung wird in der Systemsprache anstelle der Sprache angezeigt, die für die juristische Person festgelegt wurde, in der die Bestellung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f0d08-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="f0d08-151">Reproduzieren Sie das Problem</span><span class="sxs-lookup"><span data-stu-id="f0d08-151">Reproduce the issue</span></span>

<span data-ttu-id="f0d08-152">Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="f0d08-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="f0d08-153">Stellen Sie die Systemsprache auf *EN-US* (Amerikanisches Englisch) ein.</span><span class="sxs-lookup"><span data-stu-id="f0d08-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="f0d08-154">Stellen Sie sicher, dass es ein Produkt gibt, in dem die *EN-US* und *DE* (Deutschland)-Sprachen für die Übersetzung des Produktnamens gepflegt werden.</span><span class="sxs-lookup"><span data-stu-id="f0d08-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="f0d08-155">Ändern Sie die Sprache einer juristischen Person in *DE*.</span><span class="sxs-lookup"><span data-stu-id="f0d08-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="f0d08-156">In der juristischen Person, in der *DE* als Sprache festgelegt ist, erstellen Sie eine Bestellung, die das Produkt enthält.</span><span class="sxs-lookup"><span data-stu-id="f0d08-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="f0d08-157">Beachten Sie, dass der Produktname weiterhin in US-Englisch (der Systemsprache) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f0d08-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f0d08-158">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="f0d08-158">Issue resolution</span></span>

<span data-ttu-id="f0d08-159">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-159">This behavior is by design.</span></span> <span data-ttu-id="f0d08-160">Bei Bestellungen wird das Produkt immer in der Systemsprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="f0d08-161">Die Bestellsprache wird verwendet, wenn ein Bestätigungsjournal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f0d08-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="f0d08-162">In der Liste der genehmigten Lieferanten nach Produktentitäten kann das Datum des Inkrafttretens nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f0d08-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f0d08-163">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d08-163">Issue description</span></span>

<span data-ttu-id="f0d08-164">Ein Produkt hat einen genehmigten Lieferanten, der beispielsweise ein Datum des Inkrafttretens am 11. Januar 2018 hat ( *01/11/2018* ) und ein Ablaufdatum von *Niemals*.</span><span class="sxs-lookup"><span data-stu-id="f0d08-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 ( *01/11/2018* ), and an expiration date of *Never*.</span></span> <span data-ttu-id="f0d08-165">Wenn Sie versuchen, das Datum des Inkrafttretens auf den 10. Januar 2018 ( *01/10/2018* ) oder den 12. Januar 2018 ( *01/12/2018* ) zu ändern, erhalten Sie folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="f0d08-165">If you try to change the effective date to January 10, 2018 ( *01/10/2018* ), or January 12, 2018 ( *01/12/2018* ), you receive the following error:</span></span>

> <span data-ttu-id="f0d08-166">In der Liste der genehmigten Lieferanten (PdsApproveVendorList) kann kein Datensatz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0d08-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="f0d08-167">Der Wert 'Ablauf' muss größer oder gleich dem Wert 'Effektiv' sein.</span><span class="sxs-lookup"><span data-stu-id="f0d08-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f0d08-168">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="f0d08-168">Issue resolution</span></span>

<span data-ttu-id="f0d08-169">Sie können nur den Zeitraum verlängern, für den der Lieferant zugelassen ist.</span><span class="sxs-lookup"><span data-stu-id="f0d08-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="f0d08-170">Dabei gelten folgende Regeln:</span><span class="sxs-lookup"><span data-stu-id="f0d08-170">The following rules apply:</span></span>

- <span data-ttu-id="f0d08-171">Um das Datum des Inkrafttretens so zu ändern, dass es vor den vorhandenen Datensätzen (Zeiträumen) des Artikelanbieters liegt, muss das Ablaufdatum des neuen Zeitraums vor allen Ablaufdaten in den vorhandenen Datensätzen liegen.</span><span class="sxs-lookup"><span data-stu-id="f0d08-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="f0d08-172">Um das Ablaufdatum so zu ändern, dass es nach einem der vorhandenen Zeiträume liegt, muss das Datum des Inkrafttretens in jedem vorhandenen Datensatz nach dem letzten Ablaufdatum liegen.</span><span class="sxs-lookup"><span data-stu-id="f0d08-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="f0d08-173">Um den Gesamtzeitraum zu verkürzen, für den der Lieferant zugelassen ist, müssen Sie vorhandene Datensätze löschen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="f0d08-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="f0d08-174">Alternativ können Sie während des Imports den **kürzen** -Umschalter verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0d08-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="f0d08-175">Dieser Schalter löscht alle vorhandenen Datensätze in der Tabelle für genehmigte Lieferanten nach Artikel.</span><span class="sxs-lookup"><span data-stu-id="f0d08-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="f0d08-176">Für das in der Problembeschreibung beschriebene Beispielszenario, in dem ein Datensatz das Datum des Inkrafttretens von *01/11/2018* hat und ein Ablaufdatum von *Niemals* , können Sie einen neuen Datensatz mit dem Datum des Inkrafttretens von *01/10/2018* und ein Ablaufdatum von *Niemals* importieren.</span><span class="sxs-lookup"><span data-stu-id="f0d08-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never* , you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="f0d08-177">Sie können den Zeitraum jedoch nicht verkürzen, sodass das Datum des Inkrafttretens über die Datenverwaltung auf *01/12/2018* aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f0d08-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="f0d08-178">Sie müssen diese Änderung über die Benutzeroberfläche vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f0d08-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a><span data-ttu-id="f0d08-179">Nachdem ich die Lieferadresse in einem Bestellkopf geändert habe, wird der Lieferungsname nicht synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f0d08-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f0d08-180">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d08-180">Issue description</span></span>

<span data-ttu-id="f0d08-181">Die Adresse in der Kopfzeile einer Bestellung wird auf eine Adresse aktualisiert, die keine Lieferadresse ist.</span><span class="sxs-lookup"><span data-stu-id="f0d08-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="f0d08-182">Obwohl die Adresse in der Bestellung aktualisiert wird, wird der Lieferungsname nicht basierend auf der aktualisierten Adresse aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f0d08-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f0d08-183">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="f0d08-183">Issue resolution</span></span>

<span data-ttu-id="f0d08-184">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-184">This behavior is by design.</span></span> <span data-ttu-id="f0d08-185">Die ausgewählte Adresse muss als Lieferadresse klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f0d08-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="f0d08-186">Andernfalls wird der Lieferungsname nicht basierend auf der ausgewählten Adresse aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f0d08-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="f0d08-187">Kann ich den Benutzer finden, der eine Bestellung storniert hat?</span><span class="sxs-lookup"><span data-stu-id="f0d08-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="f0d08-188">Diese Information wird nur verfolgt, wenn die Bestellung der Änderungsverwaltung unterliegt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="f0d08-189">Wenn Sie die Änderungsverwaltung verwenden, können Sie sehen, wer die Änderung (die Stornierung) eingereicht hat und wer sie genehmigt hat.</span><span class="sxs-lookup"><span data-stu-id="f0d08-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
