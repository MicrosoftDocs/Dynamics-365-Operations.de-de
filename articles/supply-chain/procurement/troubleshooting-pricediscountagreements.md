---
title: Problembehandlung bei Preisen, Ermäßigungen, Vereinbarungen und Rabatten
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Preisen, Ermäßigungen, Vereinbarungen und Rabatten auftreten können.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 12bc3cbccb1577c278489f640299510b3ced17e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811085"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="271b0-103">Problembehandlung bei Preisen, Ermäßigungen, Vereinbarungen und Rabatten</span><span class="sxs-lookup"><span data-stu-id="271b0-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="271b0-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Preisen, Ermäßigungen, Vereinbarungen und Rabatten auftreten können.</span><span class="sxs-lookup"><span data-stu-id="271b0-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="271b0-105">Ich kann einen Kaufvertrag nicht mit einer Bestellposition verknüpfen, nachdem die Bestellung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="271b0-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="271b0-106">Ein Kaufvertrag muss einer Bestellung zugewiesen werden, wenn die Bestellung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="271b0-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="271b0-107">Andernfalls können Bestellpositionen nicht mit Kaufvertragspositionen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="271b0-108">Welche Prüfung löst die Meldung „Manuell eingegebene Preise und Rabatte oder externes Dokument aktualisieren“ aus?</span><span class="sxs-lookup"><span data-stu-id="271b0-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="271b0-109">Wenn Sie das Versanddatum ändern, erhalten Sie möglicherweise die Meldung „Manuell eingegebene Preise und Rabatte oder externes Dokument aktualisieren“.</span><span class="sxs-lookup"><span data-stu-id="271b0-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="271b0-110">Sie erhalten diese Nachricht, da bei einer Änderung des Versanddatums möglicherweise ein anderer Handels- oder Verkaufsvertrag ausgelöst wird und eine Preisänderung verursacht.</span><span class="sxs-lookup"><span data-stu-id="271b0-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="271b0-111">Eine Änderung des Versanddatums kann sich auch auf Lagerpläne und andere verwandte Informationen auswirken.</span><span class="sxs-lookup"><span data-stu-id="271b0-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="271b0-112">Die Nachricht wird ausgelöst, wenn eine der Daten oder andere Parameter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="271b0-113">Der Zweck der Nachricht besteht darin, sicherzustellen, dass Sie über Preisänderungen informiert sind, die aufgrund dieser Änderungen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="271b0-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="271b0-114">Die Nachricht ist die Eingabeaufforderung zur Bewertung des Handelsabkommens (TAE).</span><span class="sxs-lookup"><span data-stu-id="271b0-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="271b0-115">Eine vollständige Beschreibung finden Sie unter [Bewertungsrichtlinien für Handelsabkommen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="271b0-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="271b0-116">Ein Bestellungsbeleg enthält nicht alle Gebühren.</span><span class="sxs-lookup"><span data-stu-id="271b0-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="271b0-117">Reproduzieren Sie das Problem</span><span class="sxs-lookup"><span data-stu-id="271b0-117">Reproduce the issue</span></span>

<span data-ttu-id="271b0-118">Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="271b0-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="271b0-119">Stellen Sie auf der **Beschaffungs- und Ursprungsparameter**-Seite auf der Registerkarte **Lieferung** sicher, dass die **Auf Produktbeleg Gebühren generieren**-Option auf *Ja* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="271b0-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="271b0-120">Erstellen einer Bestellung, die Gebühren enthält.</span><span class="sxs-lookup"><span data-stu-id="271b0-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="271b0-121">Bestätigen Sie die Bestellung.</span><span class="sxs-lookup"><span data-stu-id="271b0-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="271b0-122">Erhalten Sie die Bestellung.</span><span class="sxs-lookup"><span data-stu-id="271b0-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="271b0-123">Sehen Sie sich die Quittungssumme an und vergleichen Sie sie mit der erwarteten Gesamtsumme.</span><span class="sxs-lookup"><span data-stu-id="271b0-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="271b0-124">Beachten Sie, dass nicht alle Gebühren auf dem Bestellbeleg enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="271b0-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="271b0-125">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="271b0-125">Issue resolution</span></span>

<span data-ttu-id="271b0-126">Die Auflösung hängt davon ab, wie die verschiedenen Gebühren eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="271b0-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="271b0-127">Informationen zum Einrichten verschiedener Gebühren zur Erfüllung Ihrer Anforderungen finden Sie im folgenden Blogbeitrag: [Sonstiges Gebühren zum Zeitpunkt des Produkteingangs buchen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="271b0-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="271b0-128">Preise und Rabatte für Handelsabkommen gelten nicht für Verkaufs- oder Bestellpositionen, die über die Datenverwaltung importiert werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="271b0-129">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="271b0-129">Issue description</span></span>

<span data-ttu-id="271b0-130">Handelsabkommen, die für Verkaufs- oder Bestellpositionen gelten, werden nicht auf Positionen angewendet, die über die Datenverwaltung importiert werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="271b0-131">Dieselben Handelsabkommen gelten jedoch für manuell erstellte Verkaufs- oder Bestellpositionen.</span><span class="sxs-lookup"><span data-stu-id="271b0-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="271b0-132">Grund für das Problem</span><span class="sxs-lookup"><span data-stu-id="271b0-132">Reason for the issue</span></span>

<span data-ttu-id="271b0-133">Wenn Bestellpositionen, die über die Datenverwaltung importiert werden, bereits Preisinformationen enthalten, wird das Handelsabkommen für diese Positionen nicht neu bewertet.</span><span class="sxs-lookup"><span data-stu-id="271b0-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="271b0-134">Wenn zum Beispiel **Positionsrabatt in Prozent** oder einer der Preis- und Rabattwerte für eine Position festgelegt ist, werden Handelsabkommen für diese Position nicht nachgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="271b0-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="271b0-135">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="271b0-135">Issue workaround</span></span>

<span data-ttu-id="271b0-136">Dieses Verhalten wird erwartet und ist sowohl für Aufträge als auch für Bestellungen ähnlich.</span><span class="sxs-lookup"><span data-stu-id="271b0-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="271b0-137">Importieren Sie zur Umgehung dieses Problems die Bestellpositionen, ohne Preisinformationen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="271b0-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="271b0-138">Die Handelsabkommen werden dann angewendet und die Bestellpositionen werden basierend auf den definierten Handelsabkommen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="271b0-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="271b0-139">Ein Lieferantenrabatt wird nicht auf der Grundlage von Rechnungen kumuliert.</span><span class="sxs-lookup"><span data-stu-id="271b0-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="271b0-140">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="271b0-140">Issue description</span></span>

<span data-ttu-id="271b0-141">Wenn gebuchte Rechnungen unterschiedliche Fälligkeitstermine haben, werden diese Rechnungen nicht in Lieferantenrabatten berücksichtigt, die daraus generiert werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="271b0-142">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="271b0-142">Issue resolution</span></span>

<span data-ttu-id="271b0-143">Das Fälligkeitsdatum wird bei der Berechnung des Lieferantenrabattes nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="271b0-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="271b0-144">Ziehen Sie in Betracht, das System so anzupassen, dass das Fälligkeitsdatum und die Beziehung zur Rechnung in Bezug auf den tatsächlichen Lieferantenrabatt deutlicher werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="271b0-145">Stückpreise auf Bestellungen werden nicht basierend auf der Stückumrechnung berechnet.</span><span class="sxs-lookup"><span data-stu-id="271b0-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="271b0-146">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="271b0-146">Issue description</span></span>

<span data-ttu-id="271b0-147">Wenn eine Einheit in einer Bestellung geändert wird, werden die Handelsvertragspreise nicht gemäß den Definitionen der Einheitenumrechnung neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="271b0-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="271b0-148">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="271b0-148">Issue resolution</span></span>

<span data-ttu-id="271b0-149">Die Preise werden immer aus Handelsabkommen (oder anderen Preiseinstellungen im System, wie z. B. Verkaufsvereinbarungen oder Artikelpreisen) ermittelt und für eine Einheit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="271b0-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="271b0-150">Wenn die Einheit in einer Bestellposition geändert wird, sucht das System nach einem Preis für die neue Einheit und wendet diesen Preis an.</span><span class="sxs-lookup"><span data-stu-id="271b0-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="271b0-151">Wenn für das Gerät kein Preis gefunden wird, wendet das System keinen Preis an.</span><span class="sxs-lookup"><span data-stu-id="271b0-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="271b0-152">Die Einheitenumrechnung kann nicht verwendet werden, um den Preis in eine andere Einheit umzurechnen.</span><span class="sxs-lookup"><span data-stu-id="271b0-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="271b0-153">Theoretisch entspricht der Preis für eine Schachtel mit zehn Stück möglicherweise nicht dem Zehnfachen des Preises einer Schachtel.</span><span class="sxs-lookup"><span data-stu-id="271b0-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="271b0-154">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="271b0-154">Issue workaround</span></span>

<span data-ttu-id="271b0-155">Eine Möglichkeit, dieses Problem zu umgehen, besteht darin, sicherzustellen, dass Handelsabkommen für die Einheiten bestehen, von denen Sie erwarten, dass sie in den Bestellpositionen für den Artikel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="271b0-156">Währungsumrechnungsprobleme treten bei Handelsabkommen auf.</span><span class="sxs-lookup"><span data-stu-id="271b0-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="271b0-157">Preise von Handelsabkommen werden nicht nach der Währung neu berechnet, wenn die Währung in einer Bestellung abweicht.</span><span class="sxs-lookup"><span data-stu-id="271b0-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="271b0-158">Mit der Funktion *Allgemeine Währung* können Sie Preise und Rabatte in nur einer Währung definieren.</span><span class="sxs-lookup"><span data-stu-id="271b0-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="271b0-159">Sie können dann nach Bedarf in andere Währungen umrechnen.</span><span class="sxs-lookup"><span data-stu-id="271b0-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="271b0-160">Darüber hinaus kann die Funktion nach Abschluss der Umrechnung automatisch eine intelligente Rundung anwenden.</span><span class="sxs-lookup"><span data-stu-id="271b0-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="271b0-161">Wenn ich die Seite „Kaufvertrag“ in einem Positionsansichtsmodus öffne, kann ich die Seite nicht personalisieren, indem ich das Feld „Preiseinheit“ in der Übersicht der Position hinzufüge.</span><span class="sxs-lookup"><span data-stu-id="271b0-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="271b0-162">Einige gemeinsam genutzte Felder im Vereinbarungsframework können nicht in Personalisierungen einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="271b0-163">Diese Einschränkung tritt aufgrund des implementierten Datenmodells auf.</span><span class="sxs-lookup"><span data-stu-id="271b0-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="271b0-164">Daher können Sie das **Preiseinheit**-Feld nicht personalisieren.</span><span class="sxs-lookup"><span data-stu-id="271b0-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="271b0-165">Das maximale Limit aus einem Kaufvertrag gilt nicht für eine Bestellanforderung.</span><span class="sxs-lookup"><span data-stu-id="271b0-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="271b0-166">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="271b0-166">Issue description</span></span>

<span data-ttu-id="271b0-167">Wenn eine Bestellanforderung mit einem Kaufvertrag verknüpft ist, gilt das maximale Limit aus dem Kaufvertrag nicht für die Bestellanforderung.</span><span class="sxs-lookup"><span data-stu-id="271b0-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="271b0-168">Die Standardpreisinformationen werden korrekt eingegeben, es kann jedoch mehr als das maximale Limit aus dem Kaufvertrag in der Bestellanforderung bestellt werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="271b0-169">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="271b0-169">Issue resolution</span></span>

<span data-ttu-id="271b0-170">Dieses Verhalten wird erwartet.</span><span class="sxs-lookup"><span data-stu-id="271b0-170">This behavior is expected.</span></span> <span data-ttu-id="271b0-171">Da Anforderungen nicht immer genehmigt werden, sollte eine Menge oder ein Betrag nicht im Kaufvertrag reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="271b0-172">Daher werden Sie das Höchstlimit aus dem Kaufvertrag nicht erreichen.</span><span class="sxs-lookup"><span data-stu-id="271b0-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="271b0-173">Handelsabkommen können aus abgelehnten Angebotsanforderungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="271b0-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="271b0-174">Daher verhindert das System nicht, dass Handelsabkommensjournale erstellt werden, wenn die Angebotsanforderungen-Position nicht akzeptiert wurde.</span><span class="sxs-lookup"><span data-stu-id="271b0-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="271b0-175">Sie können Handelsabkommen für alle Antworten auf eine Angebotsanforderungen (RFQ) erstellen, unabhängig davon, ob sie akzeptiert oder abgelehnt wurden.</span><span class="sxs-lookup"><span data-stu-id="271b0-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="271b0-176">Weitere Informationen finden Sie unter [ÜBersicht der Angebotsanforderungen (RFQs)](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="271b0-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]