--- 
title: Akkreditiv exportieren
description: Diese Prozedur zeigt Ihnen den Prozess des Exportkreditbriefs.
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8d2782291a7471291720830a18d739aeb1eca8d0
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="export-a-letter-of-credit"></a><span data-ttu-id="5ed34-103">Akkreditiv exportieren</span><span class="sxs-lookup"><span data-stu-id="5ed34-103">Export a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ed34-104">Diese Prozedur zeigt Ihnen den Prozess des Exportkreditbriefs.</span><span class="sxs-lookup"><span data-stu-id="5ed34-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="5ed34-105">Ein Kreditbrief stellt eine Vereinbarung dar, die von einer Bank ausgegeben wird. Darin gewährleistet die Bank die Zahlung im Auftrag des Einkäufers, sofern die Vertragsbedingungen zwischen Einkäufer und Verkäufer erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="5ed34-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="5ed34-106">Führen Sie die Prozedur "Einrichten der Bankfazilitäten und Buchungsprofile" und die Prozedur "Letter of Credit_Create a bank facility agreement" vor dieser Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="5ed34-107">Das Demo-Unternehmen USMF muss ausgewählt werden, um diese Prozedur erfolgreich ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="5ed34-108">Erstellen eines Exportkreditbrief-Auftrags</span><span class="sxs-lookup"><span data-stu-id="5ed34-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="5ed34-109">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="5ed34-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="5ed34-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5ed34-110">Click New.</span></span>
3. <span data-ttu-id="5ed34-111">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5ed34-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5ed34-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5ed34-114">Erweitern oder reduzieren Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="5ed34-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="5ed34-115">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5ed34-116">Wählen Sie den Standort, an dem der ausgegebene Artikel gelagert wird.</span><span class="sxs-lookup"><span data-stu-id="5ed34-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="5ed34-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5ed34-118">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5ed34-119">Wählen Sie den Lagerort, an dem der ausgegebene Artikel gelagert wird.</span><span class="sxs-lookup"><span data-stu-id="5ed34-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="5ed34-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5ed34-121">Hinweis: Wählen Sie im Feld "Bankdokumenttyp" den Wert "Kreditbrief" aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="5ed34-122">Wählen Sie im Feld "Bankdokumenttyp" "Kreditbrief" aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="5ed34-123">Erweitern oder reduzieren Sie den Abschnitt 'Lieferung'.</span><span class="sxs-lookup"><span data-stu-id="5ed34-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="5ed34-124">Hinweis: Wählen Sie "Lieferdatumskontrolle = keine".</span><span class="sxs-lookup"><span data-stu-id="5ed34-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="5ed34-125">Geben Sie im Feld "Angefordertes Wareneingangsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="5ed34-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5ed34-126">Click OK.</span></span>
15. <span data-ttu-id="5ed34-127">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5ed34-128">Wählen Sie den erforderlichen Artikel zur Entnahme/Verkauf.</span><span class="sxs-lookup"><span data-stu-id="5ed34-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="5ed34-129">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="5ed34-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="5ed34-131">Geben Sie im Feld "Einzelpreis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="5ed34-132">Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="5ed34-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="5ed34-133">Klicken Sie auf die Registerkarte "Lieferung".</span><span class="sxs-lookup"><span data-stu-id="5ed34-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="5ed34-134">Geben Sie im Feld "Angefordertes Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="5ed34-135">Geben Sie im Feld "Bestätigtes Versanddatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="5ed34-136">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="5ed34-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="5ed34-137">Klicken Sie Bankbürgschaft.</span><span class="sxs-lookup"><span data-stu-id="5ed34-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="5ed34-138">Geben Sie im Feld "Bankdokumentnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="5ed34-139">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="5ed34-140">Erweitern oder reduzieren Sie den Abschnitt "Bankverbindung".</span><span class="sxs-lookup"><span data-stu-id="5ed34-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="5ed34-141">Klicken Sie im Feld "Ausgebende Bank" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="5ed34-142">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="5ed34-143">Klicken Sie im Feld "Avisierende Bank" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="5ed34-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="5ed34-145">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="5ed34-146">Klicken Sie auf "Auftragslieferungen abrufen".</span><span class="sxs-lookup"><span data-stu-id="5ed34-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="5ed34-147">Klicken Sie auf "Bankdokument ausgeben".</span><span class="sxs-lookup"><span data-stu-id="5ed34-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="5ed34-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5ed34-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="5ed34-149">Lieferschein buchen</span><span class="sxs-lookup"><span data-stu-id="5ed34-149">Post Packing slip</span></span>
1. <span data-ttu-id="5ed34-150">Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".</span><span class="sxs-lookup"><span data-stu-id="5ed34-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="5ed34-151">Klicken Sie auf "Lieferschein buchen".</span><span class="sxs-lookup"><span data-stu-id="5ed34-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="5ed34-152">Erweitern oder reduzieren Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="5ed34-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="5ed34-153">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="5ed34-154">Erweitern oder reduzieren Sie den Abschnitt 'Einrichten'.</span><span class="sxs-lookup"><span data-stu-id="5ed34-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="5ed34-155">Geben Sie im Feld "Lieferscheindatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="5ed34-156">Wählen Sie eine Liefernummer.</span><span class="sxs-lookup"><span data-stu-id="5ed34-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="5ed34-157">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5ed34-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5ed34-158">Click OK.</span></span>
10. <span data-ttu-id="5ed34-159">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5ed34-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="5ed34-160">Verkaufsrechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-160">Post sales invoice</span></span>
1. <span data-ttu-id="5ed34-161">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="5ed34-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="5ed34-162">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="5ed34-162">Click Invoice.</span></span>
3. <span data-ttu-id="5ed34-163">Erweitern oder reduzieren Sie den Abschnitt 'Überblick'.</span><span class="sxs-lookup"><span data-stu-id="5ed34-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="5ed34-164">Wählen Sie eine Liefernummer.</span><span class="sxs-lookup"><span data-stu-id="5ed34-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="5ed34-165">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5ed34-166">Erweitern oder reduzieren Sie den Abschnitt 'Einrichten'.</span><span class="sxs-lookup"><span data-stu-id="5ed34-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="5ed34-167">Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="5ed34-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5ed34-168">Click OK.</span></span>
9. <span data-ttu-id="5ed34-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5ed34-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="5ed34-170">Übermittelter Status der Lieferdokumente</span><span class="sxs-lookup"><span data-stu-id="5ed34-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="5ed34-171">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="5ed34-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="5ed34-172">Klicken Sie Bankbürgschaft.</span><span class="sxs-lookup"><span data-stu-id="5ed34-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="5ed34-173">Erweitern oder reduzieren Sie den Abschnitt 'Positionen'.</span><span class="sxs-lookup"><span data-stu-id="5ed34-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="5ed34-174">Hinweis: Das Feld "Dokument übermittelt" sollte auf "Ja" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5ed34-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="5ed34-175">Exportkreditbrief überprüfen</span><span class="sxs-lookup"><span data-stu-id="5ed34-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="5ed34-176">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Exportkreditbrief und Importinkasso".</span><span class="sxs-lookup"><span data-stu-id="5ed34-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="5ed34-177">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5ed34-178">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5ed34-179">Vergewissern Sie sich, dass der Lieferstatus des Exportkreditbriefs auf" Fakturiert" steht.</span><span class="sxs-lookup"><span data-stu-id="5ed34-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="5ed34-180">Debitorenzahlung</span><span class="sxs-lookup"><span data-stu-id="5ed34-180">Customer payment</span></span>
1. <span data-ttu-id="5ed34-181">Wechseln Sie zu "Debitoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="5ed34-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="5ed34-182">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5ed34-182">Click New.</span></span>
3. <span data-ttu-id="5ed34-183">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5ed34-184">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5ed34-185">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5ed34-186">Klicken Sie auf Positionen.</span><span class="sxs-lookup"><span data-stu-id="5ed34-186">Click Lines.</span></span>
7. <span data-ttu-id="5ed34-187">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="5ed34-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="5ed34-188">Geben Sie im Feld "Konto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="5ed34-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="5ed34-189">Klicken Sie auf "Ausgleich".</span><span class="sxs-lookup"><span data-stu-id="5ed34-189">Click Settlement.</span></span>
10. <span data-ttu-id="5ed34-190">Aktivieren Sie das Kontrollkästchen in der Kopfzeile von 'Summen'.</span><span class="sxs-lookup"><span data-stu-id="5ed34-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="5ed34-191">Hinweis: Legen Sie das Feld "Anzeigen"auf "Kreditbrief" fest.</span><span class="sxs-lookup"><span data-stu-id="5ed34-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="5ed34-192">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5ed34-193">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen 'Markieren'.</span><span class="sxs-lookup"><span data-stu-id="5ed34-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="5ed34-194">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5ed34-194">Click OK.</span></span>
14. <span data-ttu-id="5ed34-195">Klicken Sie auf die Registerkarte Zahlung.</span><span class="sxs-lookup"><span data-stu-id="5ed34-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="5ed34-196">Überprüfen Sie die Bankdokumentnummer und Liefernummerdetails.</span><span class="sxs-lookup"><span data-stu-id="5ed34-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="5ed34-197">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="5ed34-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="5ed34-198">Überprüfen Sie den Exportkreditbrief nach der Zahlung.</span><span class="sxs-lookup"><span data-stu-id="5ed34-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="5ed34-199">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Exportkreditbrief und Importinkasso".</span><span class="sxs-lookup"><span data-stu-id="5ed34-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="5ed34-200">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5ed34-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5ed34-201">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5ed34-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5ed34-202">Überprüfen Sie, ob Lieferstatus = empfangene Zahlung und Saldobetrag = 0.00.</span><span class="sxs-lookup"><span data-stu-id="5ed34-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  


