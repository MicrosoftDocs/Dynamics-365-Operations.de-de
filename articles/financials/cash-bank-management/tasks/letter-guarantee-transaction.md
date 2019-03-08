---
title: Bankgarantiebuchung
description: Diese Prozedur führt Sie Schritt für Schritt durch den Garantiebriefprozess.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4dc6ee178121fae05d538f5103919442d91e65eb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "333644"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="f4f56-103">Bankgarantiebuchung</span><span class="sxs-lookup"><span data-stu-id="f4f56-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4f56-104">Diese Prozedur führt Sie Schritt für Schritt durch den Garantiebriefprozess.</span><span class="sxs-lookup"><span data-stu-id="f4f56-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="f4f56-105">Schließen Sie folgende Aufgaben ab, bevor Sie diese starten:</span><span class="sxs-lookup"><span data-stu-id="f4f56-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="f4f56-106">Einrichten der Bankfazilitäten und Buchungsprofile für eine Bankgarantie.</span><span class="sxs-lookup"><span data-stu-id="f4f56-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="f4f56-107">Erstellen einer Bankfazilitätsvereinbarung für einen Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="f4f56-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="f4f56-108">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4f56-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="f4f56-109">Auftrag mit Garantiebrief erstellen</span><span class="sxs-lookup"><span data-stu-id="f4f56-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="f4f56-110">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="f4f56-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f4f56-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f4f56-111">Click New.</span></span>
3. <span data-ttu-id="f4f56-112">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="f4f56-113">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="f4f56-113">Expand the General section.</span></span>
5. <span data-ttu-id="f4f56-114">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="f4f56-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4f56-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f4f56-116">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="f4f56-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4f56-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f4f56-118">Wählen Sie im Feld "Bankdokumenttyp" "Garantiebrief" aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="f4f56-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-119">Click OK.</span></span>
11. <span data-ttu-id="f4f56-120">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="f4f56-121">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f4f56-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="f4f56-122">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="f4f56-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="f4f56-123">Klicken Sie auf die Registerkarte "Lieferung".</span><span class="sxs-lookup"><span data-stu-id="f4f56-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="f4f56-124">Hinweis: Wählen Sie "Lieferdatumskontrolle = keine"</span><span class="sxs-lookup"><span data-stu-id="f4f56-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="f4f56-125">Geben Sie im Feld "Angefordertes Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f4f56-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="f4f56-126">Geben Sie im Feld "Bestätigtes Versanddatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f4f56-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="f4f56-127">letter of guarantee_Request verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f4f56-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="f4f56-128">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="f4f56-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="f4f56-129">Klicken Sie "Garantiebrief".</span><span class="sxs-lookup"><span data-stu-id="f4f56-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="f4f56-130">Klicken Sie im Aktivitätsbereich auf Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="f4f56-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="f4f56-131">Klicken Sie "Anforderung" zum Öffnen des Dropdown-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="f4f56-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="f4f56-132">Geben Sie im Typfeld einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="f4f56-133">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4f56-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f4f56-134">Geben Sie im Feld "Wert" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f4f56-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="f4f56-135">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="f4f56-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="f4f56-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-136">Click OK.</span></span>
10. <span data-ttu-id="f4f56-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4f56-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="f4f56-138">letter of guarantee_Submit to bank verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f4f56-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="f4f56-139">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".</span><span class="sxs-lookup"><span data-stu-id="f4f56-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="f4f56-140">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f4f56-141">Klicken Sie auf "An Bank übermitteln", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4f56-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="f4f56-142">Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="f4f56-143">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4f56-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f4f56-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="f4f56-145">letter of guarantee_Receive from bank verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f4f56-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="f4f56-146">Klicken Sie auf "Von Bank empfangen", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4f56-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="f4f56-147">Geben Sie im Feld "Banknummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f4f56-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="f4f56-148">Überprüfen Sie die Werte in den berechneten Gewinnspannen- und Ausgabenfeldern.</span><span class="sxs-lookup"><span data-stu-id="f4f56-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="f4f56-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-149">Click OK.</span></span>
4. <span data-ttu-id="f4f56-150">Erweitern Sie den Abschnitt "Aktionen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="f4f56-151">Überprüfen Sie den "Von Bank empfangen" Datensatz.</span><span class="sxs-lookup"><span data-stu-id="f4f56-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="f4f56-152">Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="f4f56-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="f4f56-153">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-153">Click Lines.</span></span>
    * <span data-ttu-id="f4f56-154">Überprüfen Sie die Buchung der Erfassungseinträge.</span><span class="sxs-lookup"><span data-stu-id="f4f56-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="f4f56-155">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4f56-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="f4f56-156">letter of guarantee_Give to beneficiary verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f4f56-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="f4f56-157">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="f4f56-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f4f56-158">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4f56-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f4f56-159">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="f4f56-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f4f56-160">Klicken Sie "Garantiebrief".</span><span class="sxs-lookup"><span data-stu-id="f4f56-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f4f56-161">Klicken Sie im Aktivitätsbereich auf Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="f4f56-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f4f56-162">Klicken Sie auf "An Begünstigten übergeben", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4f56-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="f4f56-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-163">Click OK.</span></span>
8. <span data-ttu-id="f4f56-164">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".</span><span class="sxs-lookup"><span data-stu-id="f4f56-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="f4f56-165">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f4f56-166">Klicken Sie auf "An Begünstigten übergeben", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4f56-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="f4f56-167">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-167">Click OK.</span></span>
12. <span data-ttu-id="f4f56-168">Erweitern Sie den Abschnitt "Aktionen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="f4f56-169">Überprüfen Sie den "An Begünstigten übergeben" Datensatz.</span><span class="sxs-lookup"><span data-stu-id="f4f56-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="f4f56-170">letter of guarantee_Increase value verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f4f56-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="f4f56-171">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="f4f56-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f4f56-172">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4f56-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f4f56-173">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="f4f56-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f4f56-174">Klicken Sie "Garantiebrief".</span><span class="sxs-lookup"><span data-stu-id="f4f56-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f4f56-175">Klicken Sie im Aktivitätsbereich auf Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="f4f56-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f4f56-176">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Wert erhöhen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="f4f56-177">Geben Sie eine Zahl in das Feld "Hinzuzufügender Wert" ein.</span><span class="sxs-lookup"><span data-stu-id="f4f56-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="f4f56-178">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-178">Click OK.</span></span>
9. <span data-ttu-id="f4f56-179">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".</span><span class="sxs-lookup"><span data-stu-id="f4f56-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="f4f56-180">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f4f56-181">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Wert erhöhen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="f4f56-182">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-182">Click OK.</span></span>
13. <span data-ttu-id="f4f56-183">Erweitern Sie den Abschnitt "Aktionen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="f4f56-184">Überprüfen Sie den "Wert erhöhen" Datensatz.</span><span class="sxs-lookup"><span data-stu-id="f4f56-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="f4f56-185">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f4f56-186">Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="f4f56-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="f4f56-187">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-187">Click Lines.</span></span>
    * <span data-ttu-id="f4f56-188">Überprüfen Sie die gebuchten Erfassungseinträge.</span><span class="sxs-lookup"><span data-stu-id="f4f56-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="f4f56-189">letter of guarantee_Liquidate verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f4f56-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="f4f56-190">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="f4f56-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f4f56-191">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4f56-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f4f56-192">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="f4f56-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f4f56-193">Klicken Sie "Garantiebrief".</span><span class="sxs-lookup"><span data-stu-id="f4f56-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f4f56-194">Klicken Sie im Aktivitätsbereich auf Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="f4f56-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f4f56-195">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Liquidieren".</span><span class="sxs-lookup"><span data-stu-id="f4f56-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="f4f56-196">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-196">Click OK.</span></span>
8. <span data-ttu-id="f4f56-197">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".</span><span class="sxs-lookup"><span data-stu-id="f4f56-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="f4f56-198">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f4f56-199">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Liquidieren".</span><span class="sxs-lookup"><span data-stu-id="f4f56-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="f4f56-200">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4f56-200">Click OK.</span></span>
12. <span data-ttu-id="f4f56-201">Erweitern Sie den Abschnitt "Aktionen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="f4f56-202">Überprüfen Sie den "Liquidieren" Datensatz.</span><span class="sxs-lookup"><span data-stu-id="f4f56-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="f4f56-203">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f4f56-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f4f56-204">Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="f4f56-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="f4f56-205">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="f4f56-205">Click Lines.</span></span>
    * <span data-ttu-id="f4f56-206">Überprüfen Sie die gebuchten Erfassungseinträge.</span><span class="sxs-lookup"><span data-stu-id="f4f56-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="f4f56-207">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4f56-207">Close the page.</span></span>

