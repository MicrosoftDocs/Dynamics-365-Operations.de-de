---
title: "Anzeigen der Kundenaufträge"
description: "Dieses Thema enthält Informationen zu Bestellungen in n Retail Modern POS (MPOS). Debitorenaufträge sind auch Sonderauftrag. Das Thema enthält eine Diskussion zu zugehörigen Parametern und Buchungsflüssen."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ce6774ede836eb29e6ef2cd8d4baa9efb931020c
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="customer-orders-overview"></a><span data-ttu-id="a441c-105">Anzeigen der Kundenaufträge</span><span class="sxs-lookup"><span data-stu-id="a441c-105">Customer orders overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a441c-106">Dieses Thema enthält Informationen zu Bestellungen in n Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="a441c-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="a441c-107">Debitorenaufträge sind auch Sonderauftrag.</span><span class="sxs-lookup"><span data-stu-id="a441c-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="a441c-108">Das Thema enthält eine Diskussion zu zugehörigen Parametern und Buchungsflüssen.</span><span class="sxs-lookup"><span data-stu-id="a441c-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="a441c-109">In einer Omni-Channel-Welt stellen viele Einzelhändler von Debitorenaufträgen als Option oder Sonderaufträge, um die verschiedenen Produkt- und Erfüllungsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a441c-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="a441c-110">Nachfolgend sind einige typische Szenarios:</span><span class="sxs-lookup"><span data-stu-id="a441c-110">Here are some typical scenarios:</span></span>

-   <span data-ttu-id="a441c-111">Ein Debitor fordert, dass Produkte für eine bestimmten Adresse an einem bestimmten Datum geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="a441c-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
-   <span data-ttu-id="a441c-112">Ein Debitor möchte Produkte von einem Shop oder einem Lagerplatz aufheben, der aus Filiale oder vom Lagerplatz abweicht, an dem der Debitor die Produkte gekauft hat.</span><span class="sxs-lookup"><span data-stu-id="a441c-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
-   <span data-ttu-id="a441c-113">Ein Debitor fordert einer anderen Person auf, Produkte aufzuheben, die der Debitor erworben.</span><span class="sxs-lookup"><span data-stu-id="a441c-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="a441c-114">Einzelhändler können auch Debitorenaufträge verwenden, um verlorenen Verkäufe zu minimieren, den vordefinierten Ausfälle möglicherweise nicht anzeigen, da die Waren zu unterschiedlichen Zeiten oder an einem Ort geliefert oder verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a441c-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="a441c-115">Debitorenbestellungen einrichten</span><span class="sxs-lookup"><span data-stu-id="a441c-115">Set up customer orders</span></span>
<span data-ttu-id="a441c-116">Nachfolgend sind einige der Parameter, die auf der Seite e **Einzelhandelsparameter** eingerichtet sind, um zu definiueren, wie Debitorenaufträge erfüllt werden:</span><span class="sxs-lookup"><span data-stu-id="a441c-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

-   <span data-ttu-id="a441c-117">**Standardanzahlung in Prozent** –  Geben Sie den Betrag, den der Debitor bezahlen muss ein als eine Anzahlung, bevor ein Auftrag bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a441c-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="a441c-118">Der Standardanzahlungsbetrag wird als Prozentsatz der Summe des Auftragswerts berechnet.</span><span class="sxs-lookup"><span data-stu-id="a441c-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="a441c-119">Abhängig von Rechten kann ein Shopmitarbeiter den Betrag überschreiben, indem er **Anzahlung überschreiben verwendet**. </span><span class="sxs-lookup"><span data-stu-id="a441c-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
-   <span data-ttu-id="a441c-120">**Annullierungsgebührprozentsatz** – Wenn ein Zuschlag angewendet wird, wenn ein Kundenauftrag zurückgezogen wurde, geben Sie den Betrag dieses Zuschlages an.</span><span class="sxs-lookup"><span data-stu-id="a441c-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
-   <span data-ttu-id="a441c-121">**Annullierungsgebührcode** – Wenn ein Zuschlag angewendet wird, wenn ein Kundenauftrag zurückgezogen wird, wird diese Belastung auf einen Zuschlagscode im Auftrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a441c-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="a441c-122">Verwenden Sie diesen Parameter, um den Annullierungsgebührcode zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a441c-122">Use this parameter to define the cancellation charge code.</span></span>
-   <span data-ttu-id="a441c-123">**Versandkostencode** - Einzelhändler können eine Zuschlagsgebühr für den Versand von Waren an einen Debitor erheben.</span><span class="sxs-lookup"><span data-stu-id="a441c-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="a441c-124">Der Betrag der Versandkosten wird unter einem Zuschlagscode im Auftrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a441c-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="a441c-125">Verwenden Sie diesen Parameter, um den Versandkostencode den Versandkosten im Kundenauftrag zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a441c-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
-   <span data-ttu-id="a441c-126">**Rückerstattungsversandkosten**  – Gibt an, ob Versandkosten, die einem Kundenauftrag zugeordnet werden, rückvergütbar sind.</span><span class="sxs-lookup"><span data-stu-id="a441c-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
-   <span data-ttu-id="a441c-127">**Maximaler Betrag ohne Genehmigung** – wenn Versandkosten rückvergütbar sind, geben den Höchstbetrag der Versandkostenrückerstattungen über Rücklieferungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a441c-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="a441c-128">Wenn dieser Betrag überschritten wird, ist eine Manageraußerkraftsetzung erforderlich, um die Rückerstattung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="a441c-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="a441c-129">Um die folgenden Szenarien zu gewährleisten, kann eine Gebührenerstattung der Versandkosten den Betrag  überschreiten, der ursprünglich geleistet wurde:</span><span class="sxs-lookup"><span data-stu-id="a441c-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>
    -   <span data-ttu-id="a441c-130">Zuschläge werden auf Ebene Auftragsüberschrift angewendet und wenn eine beliebige Menge einer Produktgruppe zurückgegeben wird, kann die Gebührenerstattung für die maximalen Versandkosten, die für die Produkte und die Menge zugelassen ist nicht für alle Einzelhandelskunden gleich angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a441c-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    -   <span data-ttu-id="a441c-131">Versandkosten werden für jede Versandinstanz erhoben.</span><span class="sxs-lookup"><span data-stu-id="a441c-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="a441c-132">Wenn ein Kunde Produkte mehrmals zurücksendet und die Richtlinie des Einzelhändlers angibt, dass der Einzelhändler die Kosten für den Rückversand übernimmt, dann sind die Rückholversandkosten höher als die tatsächlichen Versandkosten.</span><span class="sxs-lookup"><span data-stu-id="a441c-132">If a customer returns products multiple times, and the retailer’s policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="a441c-133">Transaktionsfluss für Kundenbestellungen</span><span class="sxs-lookup"><span data-stu-id="a441c-133">Transaction flow for customer orders</span></span>
### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="a441c-134">Debitorenauftrag im Retail Modern POS erstellen</span><span class="sxs-lookup"><span data-stu-id="a441c-134">Create a customer order in Retail Modern POS</span></span>

1.  <span data-ttu-id="a441c-135">Dient zum Hinzufügen eines Debitors zur Buchung.</span><span class="sxs-lookup"><span data-stu-id="a441c-135">Add a customer to the transaction.</span></span>
2.  <span data-ttu-id="a441c-136">Produkte zum Warenkorb hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a441c-136">Add products to the cart.</span></span>
3.  <span data-ttu-id="a441c-137">Klicken Sie auf **Kundenauftrag erstellen** und wählen Sie dann den Auftragstyp aus.</span><span class="sxs-lookup"><span data-stu-id="a441c-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="a441c-138">Der Auftragstyp kann entweder **Kundenauftrag** oder **Angebot** sein.</span><span class="sxs-lookup"><span data-stu-id="a441c-138">The order type can be either **Customer order** or **Quote**.</span></span>
4.  <span data-ttu-id="a441c-139">Klicken Sie auf **Versand aktivier** oder  **Alle versenden**, um die Produkte für eine Adresse im Feld Debitorenkonto zu versenden, geben das angeforderte Versanddatum und geben die Versandkosten an.</span><span class="sxs-lookup"><span data-stu-id="a441c-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5.  <span data-ttu-id="a441c-140">Klicken Sie auf **Ausgewählte entnehmen** oder **Alle entnehmen**, um die Produkte auswählen, die vom aktuellen Shop oder aus einem anderen Shop an einem bestimmten Datum verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a441c-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6.  <span data-ttu-id="a441c-141">Fordern Sie den Anzahlungsbetrag ein, wenn eine Anzahlung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a441c-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="a441c-142">Bearbeiten eines bestehenden Kundenauftrags.</span><span class="sxs-lookup"><span data-stu-id="a441c-142">Edit an existing customer order</span></span>

1.  <span data-ttu-id="a441c-143">Auf der Startseite klicken Sie auf **Bestellung suchen**. </span><span class="sxs-lookup"><span data-stu-id="a441c-143">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="a441c-144">Suchen und wählen Sie den zu bearbeitenden Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="a441c-144">Find and select the order to edit.</span></span> <span data-ttu-id="a441c-145">Klicken Sie unten auf der Seite auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="a441c-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="a441c-146">Einen Auftrag entnehmen</span><span class="sxs-lookup"><span data-stu-id="a441c-146">Pick up an order</span></span>

1.  <span data-ttu-id="a441c-147">Auf der Startseite klicken Sie auf **Bestellung suchen**. </span><span class="sxs-lookup"><span data-stu-id="a441c-147">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="a441c-148">Wählen Sie den Auftrag aus, der gewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a441c-148">Select the order to pick up.</span></span> <span data-ttu-id="a441c-149">Klicken Sie unten auf der Seite auf **Bearbeiten und verpacken**.</span><span class="sxs-lookup"><span data-stu-id="a441c-149">At the bottom of the page, click **Picking and packing**.</span></span>
3.  <span data-ttu-id="a441c-150">Klicken Sie auf **Abholen**.</span><span class="sxs-lookup"><span data-stu-id="a441c-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="a441c-151">Stornieren einer Auftragsposition</span><span class="sxs-lookup"><span data-stu-id="a441c-151">Cancel an order</span></span>

1.  <span data-ttu-id="a441c-152">Auf der Startseite klicken Sie auf **Bestellung suchen**. </span><span class="sxs-lookup"><span data-stu-id="a441c-152">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="a441c-153">Wählen Sie den Auftrag aus, der storniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a441c-153">Select the order to cancel.</span></span> <span data-ttu-id="a441c-154">Klicken Sie unten auf der Seite auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="a441c-154">At the bottom of the page, click **Cancel**.</span></span>

#### <a name="create-a-return-order"></a><span data-ttu-id="a441c-155">Erstellen einer Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="a441c-155">Create a return order</span></span>

1.  <span data-ttu-id="a441c-156">Auf der Startseite klicken Sie auf **Bestellung suchen**. </span><span class="sxs-lookup"><span data-stu-id="a441c-156">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="a441c-157">Wählen Sie den Auftrag aus, zu dem Sie zurückkehren möchten, wählen Sie die Rechnung für den Auftrag aus, und wählen Sie dann die Produktgruppe aus, um zu den Waren zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a441c-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3.  <span data-ttu-id="a441c-158">Klicken Sie unten auf der Seite auf **Zur Bestellung zurückkehren**.</span><span class="sxs-lookup"><span data-stu-id="a441c-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="a441c-159">Asynchroner Transaktionsfluss für Kundenbestellungen</span><span class="sxs-lookup"><span data-stu-id="a441c-159">Asynchronous transaction flow for customer orders</span></span>
<span data-ttu-id="a441c-160">Debitorenaufträge können von den Verkaufsstellen (POS)-Kunden entweder im synchronen Modus oder im asynchronen Modus erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a441c-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="a441c-161">Aktivieren Sie Kundenaufträge, um diese im asynchronen Modus zu erstellen</span><span class="sxs-lookup"><span data-stu-id="a441c-161">Enable customer orders to be created in asynchronous mode</span></span>

1.  <span data-ttu-id="a441c-162">Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS-Profil** &gt; **Funktionsprofile**.</span><span class="sxs-lookup"><span data-stu-id="a441c-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2.  <span data-ttu-id="a441c-163">Wählen Sie im Inforegister **Allgemein** unter **Kundenauftrag in asynchronem Modus erstellen** die Option **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="a441c-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="a441c-164">Wenn die Option **Kundenauftrag in asynchronem Modus** auf **Ja** gesetzt ist, werden Debitorenaufträge immer in asynchronen Modus erstellt, selbst wenn Retail Transaction Service (RTS) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a441c-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="a441c-165">Wenn Sie diesen Option auf **Nein** setzen, werden Debitorenaufträge immer im Modus synchronen mithilfe von RTS erstellt.</span><span class="sxs-lookup"><span data-stu-id="a441c-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="a441c-166">Wenn Debitorenaufträge asynchronen erstellt werden, werden sie in Retail mittels Pulles (P)-Aufträgen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a441c-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="a441c-167">Die entsprechenden Aufträge werden in Retail erstellt, wenn **Aufträge synchronisieren** entweder manuell oder mithilfe von Chargenaufträgen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a441c-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

<a name="see-also"></a><span data-ttu-id="a441c-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a441c-168">See also</span></span>
--------

[<span data-ttu-id="a441c-169">Hybrid-Kundenaufträge</span><span class="sxs-lookup"><span data-stu-id="a441c-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)




