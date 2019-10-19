---
title: Kreditbrief exportieren
description: Diese Prozedur zeigt Ihnen den Prozess des Exportkreditbriefs.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d389c4a85bbf39a0974e8e456c781ae839461d87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177927"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="c3eb1-103">Kreditbrief exportieren</span><span class="sxs-lookup"><span data-stu-id="c3eb1-103">Export letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3eb1-104">Diese Prozedur zeigt Ihnen den Prozess des Exportkreditbriefs.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="c3eb1-105">Ein Kreditbrief stellt eine Vereinbarung dar, die von einer Bank ausgegeben wird. Darin gewährleistet die Bank die Zahlung im Auftrag des Einkäufers, sofern die Vertragsbedingungen zwischen Einkäufer und Verkäufer erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="c3eb1-106">Führen Sie die Prozedur "Einrichten der Bankfazilitäten und Buchungsprofile" und die Prozedur "Letter of Credit_Create a bank facility agreement" vor dieser Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="c3eb1-107">Das Demo-Unternehmen USMF muss ausgewählt werden, um diese Prozedur erfolgreich ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="c3eb1-108">Erstellen eines Exportkreditbrief-Auftrags</span><span class="sxs-lookup"><span data-stu-id="c3eb1-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="c3eb1-109">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c3eb1-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-110">Click New.</span></span>
3. <span data-ttu-id="c3eb1-111">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c3eb1-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c3eb1-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c3eb1-114">Erweitern oder reduzieren Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="c3eb1-115">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c3eb1-116">Wählen Sie den Standort, an dem der ausgegebene Artikel gelagert wird.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="c3eb1-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c3eb1-118">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c3eb1-119">Wählen Sie den Lagerort, an dem der ausgegebene Artikel gelagert wird.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="c3eb1-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c3eb1-121">Hinweis: Wählen Sie im Feld "Bankdokumenttyp" den Wert "Kreditbrief" aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="c3eb1-122">Wählen Sie im Feld "Bankdokumenttyp" "Kreditbrief" aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="c3eb1-123">Erweitern oder reduzieren Sie den Abschnitt 'Lieferung'.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="c3eb1-124">Hinweis: Wählen Sie "Lieferdatumskontrolle = keine".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="c3eb1-125">Geben Sie im Feld "Angefordertes Wareneingangsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="c3eb1-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-126">Click OK.</span></span>
15. <span data-ttu-id="c3eb1-127">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c3eb1-128">Wählen Sie den erforderlichen Artikel zur Entnahme/Verkauf.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="c3eb1-129">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="c3eb1-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c3eb1-131">Geben Sie im Feld "Einzelpreis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="c3eb1-132">Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="c3eb1-133">Klicken Sie auf die Registerkarte "Lieferung".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="c3eb1-134">Geben Sie im Feld "Angefordertes Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="c3eb1-135">Geben Sie im Feld "Bestätigtes Versanddatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="c3eb1-136">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="c3eb1-137">Klicken Sie Bankbürgschaft.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="c3eb1-138">Geben Sie im Feld "Bankdokumentnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="c3eb1-139">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="c3eb1-140">Erweitern oder reduzieren Sie den Abschnitt "Bankverbindung".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="c3eb1-141">Klicken Sie im Feld "Ausgebende Bank" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="c3eb1-142">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="c3eb1-143">Klicken Sie im Feld "Avisierende Bank" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="c3eb1-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="c3eb1-145">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="c3eb1-146">Klicken Sie auf "Auftragslieferungen abrufen".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="c3eb1-147">Klicken Sie auf "Bankdokument ausgeben".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="c3eb1-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="c3eb1-149">Lieferschein buchen</span><span class="sxs-lookup"><span data-stu-id="c3eb1-149">Post Packing slip</span></span>
1. <span data-ttu-id="c3eb1-150">Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="c3eb1-151">Klicken Sie auf "Lieferschein buchen".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="c3eb1-152">Erweitern oder reduzieren Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="c3eb1-153">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="c3eb1-154">Erweitern oder reduzieren Sie den Abschnitt 'Einrichten'.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="c3eb1-155">Geben Sie im Feld "Lieferscheindatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="c3eb1-156">Wählen Sie eine Liefernummer.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="c3eb1-157">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c3eb1-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-158">Click OK.</span></span>
10. <span data-ttu-id="c3eb1-159">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="c3eb1-160">Verkaufsrechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-160">Post sales invoice</span></span>
1. <span data-ttu-id="c3eb1-161">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="c3eb1-162">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-162">Click Invoice.</span></span>
3. <span data-ttu-id="c3eb1-163">Erweitern oder reduzieren Sie den Abschnitt 'Überblick'.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="c3eb1-164">Wählen Sie eine Liefernummer.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="c3eb1-165">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c3eb1-166">Erweitern oder reduzieren Sie den Abschnitt 'Einrichten'.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="c3eb1-167">Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="c3eb1-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-168">Click OK.</span></span>
9. <span data-ttu-id="c3eb1-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="c3eb1-170">Übermittelter Status der Lieferdokumente</span><span class="sxs-lookup"><span data-stu-id="c3eb1-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="c3eb1-171">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="c3eb1-172">Klicken Sie Bankbürgschaft.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="c3eb1-173">Erweitern oder reduzieren Sie den Abschnitt 'Positionen'.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="c3eb1-174">Hinweis: Das Feld "Dokument übermittelt" sollte auf "Ja" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="c3eb1-175">Exportkreditbrief überprüfen</span><span class="sxs-lookup"><span data-stu-id="c3eb1-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="c3eb1-176">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Exportkreditbrief und Importinkasso".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="c3eb1-177">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c3eb1-178">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c3eb1-179">Vergewissern Sie sich, dass der Lieferstatus des Exportkreditbriefs auf" Fakturiert" steht.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="c3eb1-180">Debitorenzahlung</span><span class="sxs-lookup"><span data-stu-id="c3eb1-180">Customer payment</span></span>
1. <span data-ttu-id="c3eb1-181">Wechseln Sie zu "Debitoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c3eb1-182">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-182">Click New.</span></span>
3. <span data-ttu-id="c3eb1-183">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c3eb1-184">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c3eb1-185">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c3eb1-186">Klicken Sie auf Positionen.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-186">Click Lines.</span></span>
7. <span data-ttu-id="c3eb1-187">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="c3eb1-188">Geben Sie im Feld "Konto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="c3eb1-189">Klicken Sie auf "Ausgleich".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-189">Click Settlement.</span></span>
10. <span data-ttu-id="c3eb1-190">Aktivieren Sie das Kontrollkästchen in der Kopfzeile von 'Summen'.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="c3eb1-191">Hinweis: Legen Sie das Feld "Anzeigen"auf "Kreditbrief" fest.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="c3eb1-192">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="c3eb1-193">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen 'Markieren'.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="c3eb1-194">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-194">Click OK.</span></span>
14. <span data-ttu-id="c3eb1-195">Klicken Sie auf die Registerkarte Zahlung.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="c3eb1-196">Überprüfen Sie die Bankdokumentnummer und Liefernummerdetails.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="c3eb1-197">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="c3eb1-198">Überprüfen Sie den Exportkreditbrief nach der Zahlung.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="c3eb1-199">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Exportkreditbrief und Importinkasso".</span><span class="sxs-lookup"><span data-stu-id="c3eb1-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="c3eb1-200">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c3eb1-201">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c3eb1-202">Überprüfen Sie, ob Lieferstatus = empfangene Zahlung und Saldobetrag = 0.00.</span><span class="sxs-lookup"><span data-stu-id="c3eb1-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

