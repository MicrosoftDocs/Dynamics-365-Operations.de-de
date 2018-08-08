---
title: "Rücklieferungseinstandspreis und Rücklieferungsloskennung"
description: "Unter Umständen sollen die Kosten der zurückgegebenen Produkte jedoch den Produktkosten zum Zeitpunkt des Verkaufs an den Debitor entsprechen. Sie können dies über die **Rücklieferungsloskennung** tun."
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 33cd3d50fe342ba12a17419f4e759c243a60b3e0
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="9199b-104">Rücklieferungseinstandspreis und Rücklieferungsloskennung</span><span class="sxs-lookup"><span data-stu-id="9199b-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="9199b-105">Die Kosten von Produkten, die an das Lager zurückgegeben werden, werden anhand der aktuellen Kosten der Produkte berechnet.</span><span class="sxs-lookup"><span data-stu-id="9199b-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="9199b-106">Unter Umständen sollen die Kosten der zurückgegebenen Produkte jedoch den Produktkosten zum Zeitpunkt des Verkaufs an den Debitor entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9199b-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="9199b-107">Sie können dies tun, indem Sie im **Auftragsformular** das Feld **Rücklieferungsloskennung** auf der Registerkarte **Positionsdetails** verwenden.</span><span class="sxs-lookup"><span data-stu-id="9199b-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="9199b-108">Betrachten Sie beispielsweise das folgende Szenario.</span><span class="sxs-lookup"><span data-stu-id="9199b-108">For example, consider the following scenario.</span></span> <span data-ttu-id="9199b-109">Sie stellen dem Debitoren Produkte in Rechnung.</span><span class="sxs-lookup"><span data-stu-id="9199b-109">You invoice a customer.</span></span> <span data-ttu-id="9199b-110">Anschließend gibt der Kunde (Debitor) die gelieferten Produkte zurück.</span><span class="sxs-lookup"><span data-stu-id="9199b-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="9199b-111">Sie geben die Produkte in den Bestand zurück.</span><span class="sxs-lookup"><span data-stu-id="9199b-111">You return the products to stock.</span></span> <span data-ttu-id="9199b-112">Wenn Sie dem Debitor die zurückgegebenen Produkte gutschreiben, werden in diesem Fall die Produktkosten anhand der aktuellen Kosten der Produkte berechnet.</span><span class="sxs-lookup"><span data-stu-id="9199b-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="9199b-113">Wenn Sie jedoch das Feld **Rücklieferungsloskennung** verwenden, werden die Kosten der zurückgegebenen Produkte auf der Grundlage der Rechnung des ursprünglichen Verkaufs an den Debitor verwendet.</span><span class="sxs-lookup"><span data-stu-id="9199b-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="9199b-114">Um andere Kosten als die aktuellen Kosten für Rückgaben von einem Debitor zu verwenden, verwenden Sie eine der folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="9199b-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="9199b-115">Methode 1: Geben Sie manuell den Rücklieferungseinstandspreis ein.</span><span class="sxs-lookup"><span data-stu-id="9199b-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="9199b-116">Wenn Sie Artikel einer Rücklieferung hinzufügen, werden die Artikel standardmäßig zum aktuellen Einstandspreis in den Bestand zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9199b-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="9199b-117">Um einen anderen Rücklieferungseinstandspreis anzugeben, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="9199b-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="9199b-118">Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.</span><span class="sxs-lookup"><span data-stu-id="9199b-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="9199b-119">Klicken Sie im **Aktivitätsbereich** in der Gruppe **Neu** auf **Rücklieferung**.</span><span class="sxs-lookup"><span data-stu-id="9199b-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="9199b-120">In der **Rücklieferung erstellen** Formular wählen Sie ein Debitorenkonto aus, und klicken Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="9199b-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="9199b-121">Wählen Sie im Formular **Rücklieferung - RMA-Nummer: %1, %2** eine Position aus und geben Sie dann im Feld **Menge** eine negative Menge ein.</span><span class="sxs-lookup"><span data-stu-id="9199b-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="9199b-122">Klicken Sie auf das Inforegister "**Positionsdetails**".</span><span class="sxs-lookup"><span data-stu-id="9199b-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="9199b-123">Wählen Sie auf der Registerkarte **Allgemeines** im Feld **Rücklieferungseinstandspreis** die gewünschte Option aus.</span><span class="sxs-lookup"><span data-stu-id="9199b-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="9199b-124">Dieser Wert wird verwendet, wenn die Waren in den Bestand zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9199b-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="9199b-125">Wenn Sie keinen Wert eingeben, wird der aktuelle Einstandspreis verwendet, wenn die Waren in den Bestand zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9199b-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="9199b-126">Methode 2: Automatisches Generieren der auf dem Einstandspreis basierenden Debitorenrechnungsposition</span><span class="sxs-lookup"><span data-stu-id="9199b-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="9199b-127">Dies ist die bevorzugte Methode zum Erstellen von Rückgabepositionen.</span><span class="sxs-lookup"><span data-stu-id="9199b-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="9199b-128">Um die Produktkosten zum Zeitpunkt des Verkaufs an den Debitor zu verwenden, erstellen Sie eine Rücklieferung und geben die zurückzugebende Verkaufsposition an.</span><span class="sxs-lookup"><span data-stu-id="9199b-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="9199b-129">Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.</span><span class="sxs-lookup"><span data-stu-id="9199b-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="9199b-130">Klicken Sie im **Aktivitätsbereich** in der Gruppe **Neu** auf **Rücklieferung**.</span><span class="sxs-lookup"><span data-stu-id="9199b-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="9199b-131">In der **Rücklieferung erstellen** Formular wählen Sie ein Debitorenkonto aus, und klicken Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="9199b-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="9199b-132">Klicken Sie im Formular **Rücklieferung - RMA-Nummer: %1, %2** im **Aktivitätsbereich** ein auf **Auftrag suchen**.</span><span class="sxs-lookup"><span data-stu-id="9199b-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="9199b-133">Wählen Sie im Formular **Auftrag suchen** die zurückzugebende Rechnungsposition, und klicken Sie anschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9199b-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="9199b-134">Im Inforegister **Positionsdetails** auf der Registerkarte **Allgemein** wird im Feld **Rücklieferungsloskennung** der Wert aus der ursprünglichen Auftragsposition angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9199b-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="9199b-135">Darüber hinaus wird im Feld **Rücklieferungseinstandspreis** der Einstandswert aus der ursprünglichen Auftragsposition angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9199b-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="9199b-136">Kostenberechnungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="9199b-136">Cost calculation example</span></span>

<span data-ttu-id="9199b-137">Wenn Sie das Feld **Rücklieferungsloskennung** in einer Rücklieferungsposition verwenden, um den Rücklieferungseinstandspreis anzugeben, werden die Kosten der Rücklieferungsposition verwendet.</span><span class="sxs-lookup"><span data-stu-id="9199b-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="9199b-138">Wenn Sie die Bestandsabschluss- oder -Neuberechnungsfunktionen ausführen, werden die Kosten der ursprünglichen Auftragsposition reguliert.</span><span class="sxs-lookup"><span data-stu-id="9199b-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="9199b-139">Die Kosten der Rücklieferungsposition werden automatisch angepasst, um die gleichen Kosten pro Artikel widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="9199b-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="9199b-140">Erstellen Sie ein Produkt namens Test, und geben Sie es frei.</span><span class="sxs-lookup"><span data-stu-id="9199b-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="9199b-141">In der **Details für freigegebene Produkte** Formular geben Sie folgende Informationen an:</span><span class="sxs-lookup"><span data-stu-id="9199b-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="9199b-142">Wählen Sie auf dem Inforegister **Kosten verwalten** die standardmäßige **Artikelgruppe** im Feld **Teile** aus.</span><span class="sxs-lookup"><span data-stu-id="9199b-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="9199b-143">Wählen Sie auf dem Inforegister **Allgemein** im Feld **Lagersteuerungsgruppe** **DEF** aus.</span><span class="sxs-lookup"><span data-stu-id="9199b-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="9199b-144">Geben Sie auf dem Inforegister **Einkauf** im Feld **Preis** den Wert 10,00 als Einstandspreis des Artikels ein.</span><span class="sxs-lookup"><span data-stu-id="9199b-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="9199b-145">Klicken Sie im **Aktivitätsbereich** auf **Dimensionensgruppen.**</span><span class="sxs-lookup"><span data-stu-id="9199b-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="9199b-146">Wählen Sie im Feld **Lagerdimensionsgruppe** **Nur Standort und Lagert** aus.</span><span class="sxs-lookup"><span data-stu-id="9199b-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="9199b-147">Wählen Sie im Feld **Rückverfolgungsangabengruppe** **Keine aktiven Rückverfolgungsangaben** aus.</span><span class="sxs-lookup"><span data-stu-id="9199b-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="9199b-148">Erstellen Sie eine Bestellung über 10 Stück des Artikels Test zu 6,00 pro Artikel, und buchen Sie anschließend eine Rechnung für die Bestellung.</span><span class="sxs-lookup"><span data-stu-id="9199b-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="9199b-149">Erstellen Sie eine zweite Bestellung über 10 Stück des Artikels Test zu 8,00 pro Artikel, und buchen Sie anschließend eine Rechnung für die Bestellung.</span><span class="sxs-lookup"><span data-stu-id="9199b-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="9199b-150">Buchen Sie eine Rechnung für einen Auftrag zum Verkauf von fünf Stück des Artikels Test.</span><span class="sxs-lookup"><span data-stu-id="9199b-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="9199b-151">In diesem Fall wird die Auftragsposition mit 35,00 vorkalkuliert (5 Stück \* 7,00 durchschnittlicher Einstandspreis pro Artikel).</span><span class="sxs-lookup"><span data-stu-id="9199b-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="9199b-152">Erstellen Sie eine Rücklieferung für den ausgewählten Debitor.</span><span class="sxs-lookup"><span data-stu-id="9199b-152">Create a return order for the customer.</span></span> <span data-ttu-id="9199b-153">Wählen Sie im Formular **Auftrag suchen** die Rechnungsposition, und klicken Sie anschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9199b-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="9199b-154">Vergewissern Sie sich im Formular **Rücklieferung - RMA-Nummer: %1, %2**, dass eine Rücklieferung für die Rückgabe des Artikels Test generiert wird.</span><span class="sxs-lookup"><span data-stu-id="9199b-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="9199b-155">Die Menge der Rücklieferung wird auf -5,00 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9199b-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="9199b-156">Die **Rücklieferungsloskennung** zeigt eine Kennung an.</span><span class="sxs-lookup"><span data-stu-id="9199b-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="9199b-157">Diese Loskennung wird aus dem Originalauftrag des Artikels übernommen, der an den Debitor verkauft wurde.</span><span class="sxs-lookup"><span data-stu-id="9199b-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="9199b-158">Im Feld **Rücklieferungseinstandspreis** wird der Einstandspreis aus der ursprünglichen Auftragsposition angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9199b-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="9199b-159">Erfassen Sie den Empfang zurückgelieferter Artikel.</span><span class="sxs-lookup"><span data-stu-id="9199b-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="9199b-160">Buchen Sie einen Lieferschein für die zurückgelieferten Artikel.</span><span class="sxs-lookup"><span data-stu-id="9199b-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="9199b-161">Buchen Sie eine Rechnung für die Rücklieferung.</span><span class="sxs-lookup"><span data-stu-id="9199b-161">Post an invoice for the return order.</span></span> <span data-ttu-id="9199b-162">Auf der Listenseite **Alle Aufträge** wählen Sie einen Auftrag aus, für den der Auftragstyp **Zurückgegebener Auftrag** ist.</span><span class="sxs-lookup"><span data-stu-id="9199b-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="9199b-163">Öffnen Sie das Formular **Lagerbuchungen**.</span><span class="sxs-lookup"><span data-stu-id="9199b-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="9199b-164">Überprüfen Sie, ob die Rücklieferung mit dem Einstandspreis 7,00 pro Artikel vorkalkuliert wird, indem der Wert im Feld **Rücklieferungseinstandspreis** verwendet wird, sodass sich im Feld **Kostenbetrag** die Summe 35,00 ergibt.</span><span class="sxs-lookup"><span data-stu-id="9199b-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="9199b-165">Sie können **Lagerbuchungen** das Formular über das Formular **Retoure -: Rücksendungsnummer "%1", " %2 "** öffnen.</span><span class="sxs-lookup"><span data-stu-id="9199b-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="9199b-166">Klicken Sie im Raster **Positionen** auf **Bestand** \> **Transaktion**.</span><span class="sxs-lookup"><span data-stu-id="9199b-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="9199b-167">In der Bestands- und Lagerortverwaltung verwenden Sie das Formular **Abschluss und Regulierung**, um die Prozedur **3. Schließen** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9199b-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="9199b-168">Hiermit werden die Kosten in der ursprünglichen Auftragsposition, die mit -35,00 vorkalkuliert wurden (5 Stück \* 7,00), in -30,00 (5 Stück \* 6,00) geändert.</span><span class="sxs-lookup"><span data-stu-id="9199b-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="9199b-169">Dies ist so, weil für die Lagersteuerungsgruppe das FIFO-Prinzip (First in, First out) verwendet wird, und 6,00 pro Artikel sind die FIFO-Kosten aus der ersten Bestellung.</span><span class="sxs-lookup"><span data-stu-id="9199b-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="9199b-170">Zudem werden mit dieser Aktivität die Kosten in der Rückholverkaufsposition angepasst, sodass die Kosten pro Artikel der ursprünglichen Auftragsposition entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9199b-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="9199b-171">Daher werden die Kosten der Rückgabeposition von 35,00 in 30,00 geändert.</span><span class="sxs-lookup"><span data-stu-id="9199b-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>





