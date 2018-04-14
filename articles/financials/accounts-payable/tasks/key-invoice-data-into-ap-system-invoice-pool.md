--- 
title: Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben
description: Diese Aufgabenanleitung zeigt Ihnen, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fd5f9bb94817478939eeaea5890349c138de977b
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="6d939-103">Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben</span><span class="sxs-lookup"><span data-stu-id="6d939-103">Key invoice data into the AP system using invoice pool</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d939-104">Diese Aufgabenanleitung zeigt Ihnen, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6d939-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="6d939-105">Nehmen Sie anschließend den Rechnungspool, um die Rechnung mit einer Bestellung abzugleichen und die Ausgaben auf der Kreditorenrechnungsseite abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6d939-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="6d939-106">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="6d939-106">Create a purchase order</span></span>
1. <span data-ttu-id="6d939-107">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="6d939-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="6d939-108">Klicken Sie auf "Neu", um eine neue Bestellung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6d939-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="6d939-109">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6d939-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="6d939-110">Wählen Sie in der Liste einen Händler aus.</span><span class="sxs-lookup"><span data-stu-id="6d939-110">Select the vendor from the list.</span></span> <span data-ttu-id="6d939-111">Beispielsweise Händler 1001.</span><span class="sxs-lookup"><span data-stu-id="6d939-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="6d939-112">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6d939-112">Click OK.</span></span>
6. <span data-ttu-id="6d939-113">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6d939-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="6d939-114">Suchen Sie die Services-Artikelnummer in der Liste.</span><span class="sxs-lookup"><span data-stu-id="6d939-114">Find the services item number in the list.</span></span> <span data-ttu-id="6d939-115">Wählen Sie z. B. S0001 aus.</span><span class="sxs-lookup"><span data-stu-id="6d939-115">For example, select S0001.</span></span>
8. <span data-ttu-id="6d939-116">Klicken Sie auf die Artikelnummer und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="6d939-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="6d939-117">Der Nettobetrag ist 75,00.</span><span class="sxs-lookup"><span data-stu-id="6d939-117">The net amount is 75.00.</span></span>  <span data-ttu-id="6d939-118">Der ist der Betrag, den wir auf der Rechnung erwarten.</span><span class="sxs-lookup"><span data-stu-id="6d939-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="6d939-119">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="6d939-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="6d939-120">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="6d939-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="6d939-121">Erstellen und buchen und fakturieren</span><span class="sxs-lookup"><span data-stu-id="6d939-121">Create and post and invoice</span></span>
1. <span data-ttu-id="6d939-122">Wechseln Sie zu "Kreditoren" > "Rechnungen" > "Rechnungsregister".</span><span class="sxs-lookup"><span data-stu-id="6d939-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="6d939-123">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6d939-123">Click New.</span></span>
3. <span data-ttu-id="6d939-124">Öffnen Sie die Suche, um den Namen des Rechnungsregisters auswählen, das Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6d939-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="6d939-125">Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="6d939-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="6d939-126">Klicken Sie auf "Positionen", um das Register zu öffnen und Ausgabenpositionen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="6d939-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="6d939-127">Wählen Sie in der Suche einen Händler aus.</span><span class="sxs-lookup"><span data-stu-id="6d939-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="6d939-128">Beispielsweise klicken Sie auf Händler 1001.</span><span class="sxs-lookup"><span data-stu-id="6d939-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="6d939-129">Geben Sie im Feld "Rechnung" die Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="6d939-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="6d939-130">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6d939-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="6d939-131">Geben Sie im Feld "Kredit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="6d939-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="6d939-132">Klicken Sie im Feld "Bestellung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6d939-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="6d939-133">Wählen Sie die Bestellung aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="6d939-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="6d939-134">Klicken Sie im Feld "Genehmigt von" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6d939-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="6d939-135">Heben Sie eine genehmigende Person hervor und klicken Sie auf "Auswählen", um die genehmigende Person auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6d939-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="6d939-136">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="6d939-136">Click Post.</span></span>
15. <span data-ttu-id="6d939-137">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="6d939-137">Close the form.</span></span>
16. <span data-ttu-id="6d939-138">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="6d939-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="6d939-139">Öffnen einer Rechnung aus dem Pool und Abgleichen mit einer Bestellung, um den Rechnungsprozess abzuschließen</span><span class="sxs-lookup"><span data-stu-id="6d939-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="6d939-140">Wechseln Sie zu "Kreditoren" > "Rechnungen" > "Rechnungspool".</span><span class="sxs-lookup"><span data-stu-id="6d939-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="6d939-141">Klicken Sie auf "Bestellung", um eine Kreditorenrechnung aus der Rechnung im Pool zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6d939-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="6d939-142">Wählen Sie die Rechnung aus, die Sie prüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="6d939-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="6d939-143">Klicken Sie auf "Abgleichstatus", um den Abgleich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6d939-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="6d939-144">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="6d939-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="6d939-145">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="6d939-145">Click Change view.</span></span>
7. <span data-ttu-id="6d939-146">Klicken Sie auf "Rasteransicht".</span><span class="sxs-lookup"><span data-stu-id="6d939-146">Click Grid view.</span></span>
8. <span data-ttu-id="6d939-147">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="6d939-147">Click Post.</span></span>
9. <span data-ttu-id="6d939-148">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="6d939-148">Close the form.</span></span>
10. <span data-ttu-id="6d939-149">Wechseln Sie zu "Kreditoren" > "Kreditoren" > "Kreditoren".</span><span class="sxs-lookup"><span data-stu-id="6d939-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="6d939-150">Wählen Sie den Händler aus, der auf der Bestellung war.</span><span class="sxs-lookup"><span data-stu-id="6d939-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="6d939-151">Wählen Sie z. B. Händler 1001 aus.</span><span class="sxs-lookup"><span data-stu-id="6d939-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="6d939-152">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6d939-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="6d939-153">Klicken Sie im Aktivitätsbereich auf "Händler".</span><span class="sxs-lookup"><span data-stu-id="6d939-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="6d939-154">Klicken Sie auf "Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="6d939-154">Click Transactions.</span></span>
15. <span data-ttu-id="6d939-155">Wählen Sie die Rechnung aus, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="6d939-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="6d939-156">Die Rechnungsbuchabgrenzung wurde storniert und auf das entsprechende Ausgabenkonto gebucht.</span><span class="sxs-lookup"><span data-stu-id="6d939-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  


