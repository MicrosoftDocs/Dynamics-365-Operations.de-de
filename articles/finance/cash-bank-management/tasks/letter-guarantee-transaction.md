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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443669"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="9eed9-103">Bankgarantiebuchung</span><span class="sxs-lookup"><span data-stu-id="9eed9-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9eed9-104">Diese Prozedur führt Sie Schritt für Schritt durch den Garantiebriefprozess.</span><span class="sxs-lookup"><span data-stu-id="9eed9-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="9eed9-105">Schließen Sie folgende Aufgaben ab, bevor Sie diese starten:</span><span class="sxs-lookup"><span data-stu-id="9eed9-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="9eed9-106">Einrichten der Bankfazilitäten und Buchungsprofile für eine Bankgarantie.</span><span class="sxs-lookup"><span data-stu-id="9eed9-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="9eed9-107">Erstellen einer Bankfazilitätsvereinbarung für einen Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="9eed9-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="9eed9-108">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="9eed9-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="9eed9-109">Auftrag mit Garantiebrief erstellen</span><span class="sxs-lookup"><span data-stu-id="9eed9-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="9eed9-110">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="9eed9-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="9eed9-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9eed9-111">Click New.</span></span>
3. <span data-ttu-id="9eed9-112">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="9eed9-113">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="9eed9-113">Expand the General section.</span></span>
5. <span data-ttu-id="9eed9-114">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="9eed9-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9eed9-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9eed9-116">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="9eed9-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9eed9-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9eed9-118">Wählen Sie im Feld "Bankdokumenttyp" "Garantiebrief" aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="9eed9-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-119">Click OK.</span></span>
11. <span data-ttu-id="9eed9-120">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="9eed9-121">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9eed9-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="9eed9-122">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="9eed9-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="9eed9-123">Klicken Sie auf die Registerkarte "Lieferung".</span><span class="sxs-lookup"><span data-stu-id="9eed9-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="9eed9-124">Hinweis: Wählen Sie "Lieferdatumskontrolle = keine"</span><span class="sxs-lookup"><span data-stu-id="9eed9-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="9eed9-125">Geben Sie im Feld "Angefordertes Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9eed9-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="9eed9-126">Geben Sie im Feld "Bestätigtes Versanddatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9eed9-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="9eed9-127">letter of guarantee_Request verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9eed9-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="9eed9-128">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="9eed9-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="9eed9-129">Klicken Sie "Garantiebrief".</span><span class="sxs-lookup"><span data-stu-id="9eed9-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="9eed9-130">Klicken Sie im Aktivitätsbereich auf Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="9eed9-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="9eed9-131">Klicken Sie "Anforderung" zum Öffnen des Dropdown-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="9eed9-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="9eed9-132">Geben Sie im Typfeld einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="9eed9-133">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9eed9-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9eed9-134">Geben Sie im Feld "Wert" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9eed9-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="9eed9-135">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="9eed9-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="9eed9-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-136">Click OK.</span></span>
10. <span data-ttu-id="9eed9-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9eed9-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="9eed9-138">letter of guarantee_Submit to bank verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9eed9-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="9eed9-139">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".</span><span class="sxs-lookup"><span data-stu-id="9eed9-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="9eed9-140">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9eed9-141">Klicken Sie auf "An Bank übermitteln", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9eed9-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="9eed9-142">Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="9eed9-143">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9eed9-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9eed9-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="9eed9-145">letter of guarantee_Receive from bank verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9eed9-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="9eed9-146">Klicken Sie auf "Von Bank empfangen", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9eed9-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="9eed9-147">Geben Sie im Feld "Banknummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9eed9-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="9eed9-148">Überprüfen Sie die Werte in den berechneten Gewinnspannen- und Ausgabenfeldern.</span><span class="sxs-lookup"><span data-stu-id="9eed9-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="9eed9-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-149">Click OK.</span></span>
4. <span data-ttu-id="9eed9-150">Erweitern Sie den Abschnitt "Aktionen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="9eed9-151">Überprüfen Sie den "Von Bank empfangen" Datensatz.</span><span class="sxs-lookup"><span data-stu-id="9eed9-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="9eed9-152">Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="9eed9-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="9eed9-153">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-153">Click Lines.</span></span>
    * <span data-ttu-id="9eed9-154">Überprüfen Sie die Buchung der Erfassungseinträge.</span><span class="sxs-lookup"><span data-stu-id="9eed9-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="9eed9-155">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9eed9-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="9eed9-156">letter of guarantee_Give to beneficiary verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9eed9-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="9eed9-157">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="9eed9-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="9eed9-158">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9eed9-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="9eed9-159">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="9eed9-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="9eed9-160">Klicken Sie "Garantiebrief".</span><span class="sxs-lookup"><span data-stu-id="9eed9-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="9eed9-161">Klicken Sie im Aktivitätsbereich auf Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="9eed9-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="9eed9-162">Klicken Sie auf "An Begünstigten übergeben", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9eed9-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="9eed9-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-163">Click OK.</span></span>
8. <span data-ttu-id="9eed9-164">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".</span><span class="sxs-lookup"><span data-stu-id="9eed9-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="9eed9-165">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9eed9-166">Klicken Sie auf "An Begünstigten übergeben", um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9eed9-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="9eed9-167">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-167">Click OK.</span></span>
12. <span data-ttu-id="9eed9-168">Erweitern Sie den Abschnitt "Aktionen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="9eed9-169">Überprüfen Sie den "An Begünstigten übergeben" Datensatz.</span><span class="sxs-lookup"><span data-stu-id="9eed9-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="9eed9-170">letter of guarantee_Increase value verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9eed9-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="9eed9-171">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="9eed9-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="9eed9-172">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9eed9-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="9eed9-173">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="9eed9-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="9eed9-174">Klicken Sie "Garantiebrief".</span><span class="sxs-lookup"><span data-stu-id="9eed9-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="9eed9-175">Klicken Sie im Aktivitätsbereich auf Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="9eed9-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="9eed9-176">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Wert erhöhen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="9eed9-177">Geben Sie eine Zahl in das Feld "Hinzuzufügender Wert" ein.</span><span class="sxs-lookup"><span data-stu-id="9eed9-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="9eed9-178">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-178">Click OK.</span></span>
9. <span data-ttu-id="9eed9-179">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".</span><span class="sxs-lookup"><span data-stu-id="9eed9-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="9eed9-180">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="9eed9-181">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Wert erhöhen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="9eed9-182">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-182">Click OK.</span></span>
13. <span data-ttu-id="9eed9-183">Erweitern Sie den Abschnitt "Aktionen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="9eed9-184">Überprüfen Sie den "Wert erhöhen" Datensatz.</span><span class="sxs-lookup"><span data-stu-id="9eed9-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="9eed9-185">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="9eed9-186">Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="9eed9-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="9eed9-187">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-187">Click Lines.</span></span>
    * <span data-ttu-id="9eed9-188">Überprüfen Sie die gebuchten Erfassungseinträge.</span><span class="sxs-lookup"><span data-stu-id="9eed9-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="9eed9-189">letter of guarantee_Liquidate verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9eed9-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="9eed9-190">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="9eed9-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="9eed9-191">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9eed9-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="9eed9-192">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="9eed9-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="9eed9-193">Klicken Sie "Garantiebrief".</span><span class="sxs-lookup"><span data-stu-id="9eed9-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="9eed9-194">Klicken Sie im Aktivitätsbereich auf Garantiebrief.</span><span class="sxs-lookup"><span data-stu-id="9eed9-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="9eed9-195">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Liquidieren".</span><span class="sxs-lookup"><span data-stu-id="9eed9-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="9eed9-196">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-196">Click OK.</span></span>
8. <span data-ttu-id="9eed9-197">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".</span><span class="sxs-lookup"><span data-stu-id="9eed9-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="9eed9-198">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9eed9-199">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Liquidieren".</span><span class="sxs-lookup"><span data-stu-id="9eed9-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="9eed9-200">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9eed9-200">Click OK.</span></span>
12. <span data-ttu-id="9eed9-201">Erweitern Sie den Abschnitt "Aktionen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="9eed9-202">Überprüfen Sie den "Liquidieren" Datensatz.</span><span class="sxs-lookup"><span data-stu-id="9eed9-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="9eed9-203">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9eed9-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="9eed9-204">Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="9eed9-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="9eed9-205">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="9eed9-205">Click Lines.</span></span>
    * <span data-ttu-id="9eed9-206">Überprüfen Sie die gebuchten Erfassungseinträge.</span><span class="sxs-lookup"><span data-stu-id="9eed9-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="9eed9-207">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9eed9-207">Close the page.</span></span>

