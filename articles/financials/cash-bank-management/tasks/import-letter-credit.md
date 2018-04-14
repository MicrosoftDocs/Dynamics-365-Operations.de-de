--- 
title: Akkreditiv importieren
description: Diese Prozedur zeigt Ihnen, wie Sie einen Kreditbrief importieren.
author: kweekley
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c4996f77cee1611c1bcb3ed015447747fd03fad1
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="import-a-letter-of-credit"></a><span data-ttu-id="9acfc-103">Akkreditiv importieren</span><span class="sxs-lookup"><span data-stu-id="9acfc-103">Import a letter of credit</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9acfc-104">Diese Prozedur zeigt Ihnen, wie Sie einen Kreditbrief importieren.</span><span class="sxs-lookup"><span data-stu-id="9acfc-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="9acfc-105">Folgendes muss eingerichtet werden, bevor sie das Verfahren beginnen: - Bankfazilitäten, Buchungsprofile, eine Bankfazilitätsvereinbarung und die Bankdetails des Kreditors.</span><span class="sxs-lookup"><span data-stu-id="9acfc-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="9acfc-106">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="9acfc-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="9acfc-107">Erstellen Sie eine Bestellung mit Kreditbrief.</span><span class="sxs-lookup"><span data-stu-id="9acfc-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="9acfc-108">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="9acfc-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9acfc-109">Click New.</span></span>
3. <span data-ttu-id="9acfc-110">Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="9acfc-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9acfc-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9acfc-113">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="9acfc-113">Expand the General section.</span></span>
7. <span data-ttu-id="9acfc-114">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="9acfc-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9acfc-116">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="9acfc-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9acfc-118">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="9acfc-119">Geben Sie im Feld "Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="9acfc-120">Hinweis: Wählen Sie im Feld "Bankdokumenttyp" den Wert "Kreditbrief" aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="9acfc-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9acfc-121">Click OK.</span></span>
14. <span data-ttu-id="9acfc-122">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="9acfc-123">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="9acfc-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9acfc-125">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="9acfc-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="9acfc-126">Klicken Sie auf die Registerkarte "Lieferung".</span><span class="sxs-lookup"><span data-stu-id="9acfc-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="9acfc-127">Geben Sie im Feld "Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="9acfc-128">Geben Sie im Feld "Bestätigtes Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="9acfc-129">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="9acfc-130">Definieren Sie die Kreditbrief-Details.</span><span class="sxs-lookup"><span data-stu-id="9acfc-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="9acfc-131">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="9acfc-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="9acfc-132">Klicken Sie Kreditbrief/Importinkasso.</span><span class="sxs-lookup"><span data-stu-id="9acfc-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="9acfc-133">Geben Sie im Feld "Datum des Antrags" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="9acfc-134">Vergewissern Sie sich, dass im "Bankkonto" Feld das standardmäßig aktive Bankkonto steht, das auf dem Datum des Antrags basiert.</span><span class="sxs-lookup"><span data-stu-id="9acfc-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="9acfc-135">Geben Sie im Feld "Bankdokumentnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="9acfc-136">Geben Sie im Feld "Wareneingangsdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="9acfc-137">Erweitern Sie den Abschnitt 'Bankdokument'.</span><span class="sxs-lookup"><span data-stu-id="9acfc-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="9acfc-138">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="9acfc-139">Erweitern Sie den Abschnitt 'Bankverbindung'.</span><span class="sxs-lookup"><span data-stu-id="9acfc-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="9acfc-140">Geben Sie im Feld 'Avisierende Bank' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="9acfc-141">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="9acfc-142">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9acfc-142">Click Save.</span></span>
33. <span data-ttu-id="9acfc-143">Klicken Sie "Lieferungen von Bestellungen abrufen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="9acfc-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-144">Close the page.</span></span>
35. <span data-ttu-id="9acfc-145">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="9acfc-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="9acfc-146">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-146">Click Confirm.</span></span>
37. <span data-ttu-id="9acfc-147">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="9acfc-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="9acfc-148">Klicken Sie Kreditbrief/Importinkasso.</span><span class="sxs-lookup"><span data-stu-id="9acfc-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="9acfc-149">Prozess anklicken.</span><span class="sxs-lookup"><span data-stu-id="9acfc-149">Click Process.</span></span>
40. <span data-ttu-id="9acfc-150">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-150">Click Confirm.</span></span>
    * <span data-ttu-id="9acfc-151">Überprüfen Sie, ob der Fazilitätssaldo den Bestellbetrag verringert.</span><span class="sxs-lookup"><span data-stu-id="9acfc-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="9acfc-152">In diesem Beispiel ist der Einkaufsbetrag = 500.00, Einrichtungsgrenze = 10000.00 daher Einrichtungssaldo = 9500.00.</span><span class="sxs-lookup"><span data-stu-id="9acfc-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="9acfc-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-153">Close the page.</span></span>
42. <span data-ttu-id="9acfc-154">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="9acfc-155">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9acfc-155">Click Save.</span></span>
44. <span data-ttu-id="9acfc-156">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="9acfc-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="9acfc-157">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-157">Click Confirm.</span></span>
    * <span data-ttu-id="9acfc-158">Ergänzen Sie den Kreditbrief aufgrund der Preisänderung je Einheit.</span><span class="sxs-lookup"><span data-stu-id="9acfc-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="9acfc-159">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="9acfc-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="9acfc-160">Klicken Sie Kreditbrief/Importinkasso.</span><span class="sxs-lookup"><span data-stu-id="9acfc-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="9acfc-161">Ergänzen Sie den Kreditbrief aufgrund der Preisänderung je Bestelleinheit.</span><span class="sxs-lookup"><span data-stu-id="9acfc-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="9acfc-162">Prozess anklicken.</span><span class="sxs-lookup"><span data-stu-id="9acfc-162">Click Process.</span></span>
49. <span data-ttu-id="9acfc-163">Klicken Sie auf "Ergänzen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-163">Click Amend.</span></span>
50. <span data-ttu-id="9acfc-164">Klicken Sie auf "Entfernen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-164">Click Remove.</span></span>
51. <span data-ttu-id="9acfc-165">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="9acfc-165">Click Yes.</span></span>
52. <span data-ttu-id="9acfc-166">Klicken Sie "Lieferungen von Bestellungen abrufen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="9acfc-167">Prozess anklicken.</span><span class="sxs-lookup"><span data-stu-id="9acfc-167">Click Process.</span></span>
54. <span data-ttu-id="9acfc-168">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-168">Click Confirm.</span></span>
    * <span data-ttu-id="9acfc-169">Überprüfen Sie, ob der Fazilitätssaldo den Bestellbetrag verringert.</span><span class="sxs-lookup"><span data-stu-id="9acfc-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="9acfc-170">In diesem Beispiel ist der bearbeitete Einkaufsbetrag = 600.00, Fazilitätslimit= 10000.00 daher Fazilitätssaldo = 9400.00.</span><span class="sxs-lookup"><span data-stu-id="9acfc-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="9acfc-171">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="9acfc-172">Lieferschein buchen</span><span class="sxs-lookup"><span data-stu-id="9acfc-172">Post Packing slip</span></span>
1. <span data-ttu-id="9acfc-173">Klicken Sie im Aktivitätsbereich auf "Empfangen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="9acfc-174">Klicken Sie auf "Produktzugang".</span><span class="sxs-lookup"><span data-stu-id="9acfc-174">Click Product receipt.</span></span>
3. <span data-ttu-id="9acfc-175">Geben Sie im Feld "PurchParmTable_Num" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="9acfc-176">Wählen Sie den Liefernummer aus, der mit Bezug auf den Kreditbrief erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9acfc-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="9acfc-177">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9acfc-178">Geben Sie im Feld "Produktzugangsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="9acfc-179">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9acfc-179">Click OK.</span></span>
7. <span data-ttu-id="9acfc-180">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-180">Close the page.</span></span>
8. <span data-ttu-id="9acfc-181">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="9acfc-182">Überprüfen Sie den Status des Importkreditbriefs.</span><span class="sxs-lookup"><span data-stu-id="9acfc-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="9acfc-183">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Importkreditbrief und Importinkasso".</span><span class="sxs-lookup"><span data-stu-id="9acfc-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="9acfc-184">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9acfc-185">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9acfc-186">Überprüfen Sie den Importkreditbriefstatus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-186">Verify the Import letter of credit status.</span></span>  
4. <span data-ttu-id="9acfc-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-187">Close the page.</span></span>
5. <span data-ttu-id="9acfc-188">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="9acfc-189">Einkaufsrechnung buchen</span><span class="sxs-lookup"><span data-stu-id="9acfc-189">Post purchase invoice</span></span>
1. <span data-ttu-id="9acfc-190">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="9acfc-191">Wählen Sie die Bestellung aus, die mit Kreditbrief erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9acfc-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="9acfc-192">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9acfc-193">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9acfc-194">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="9acfc-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="9acfc-195">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="9acfc-195">Click Invoice.</span></span>
6. <span data-ttu-id="9acfc-196">Geben Sie im Feld "Zahl" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="9acfc-197">Geben Sie im Feld "Liefernummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="9acfc-198">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9acfc-199">Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="9acfc-200">Klicken Sie auf "Status des Abgleichs aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="9acfc-200">Click Update match status.</span></span>
11. <span data-ttu-id="9acfc-201">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-201">Click Post.</span></span>
12. <span data-ttu-id="9acfc-202">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-202">Close the page.</span></span>
13. <span data-ttu-id="9acfc-203">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="9acfc-204">Überprüfen Sie den Status des Importkreditbriefs.</span><span class="sxs-lookup"><span data-stu-id="9acfc-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="9acfc-205">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Importkreditbrief und Importinkasso".</span><span class="sxs-lookup"><span data-stu-id="9acfc-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="9acfc-206">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9acfc-207">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9acfc-208">Überprüfen Sie den Importkreditbrief2.</span><span class="sxs-lookup"><span data-stu-id="9acfc-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="9acfc-209">Überprüfen Sie: Lieferstatus = fakturierte Bankfazilitätsdetails</span><span class="sxs-lookup"><span data-stu-id="9acfc-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="9acfc-210">Klicken Sie auf "Ansicht".</span><span class="sxs-lookup"><span data-stu-id="9acfc-210">Click View.</span></span>
5. <span data-ttu-id="9acfc-211">Klicken Sie auf "Antrag drucken".</span><span class="sxs-lookup"><span data-stu-id="9acfc-211">Click Print application.</span></span>
6. <span data-ttu-id="9acfc-212">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9acfc-212">Click OK.</span></span>
    * <span data-ttu-id="9acfc-213">Vergewissern Sie sich, dass der Kreditbriefantrag gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="9acfc-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="9acfc-214">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-214">Close the page.</span></span>
8. <span data-ttu-id="9acfc-215">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-215">Close the page.</span></span>
9. <span data-ttu-id="9acfc-216">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="9acfc-217">Buchen Sie Kreditorenzahlungserfassung für die erstellte Einkaufsrechnung mit Kreditbrief.</span><span class="sxs-lookup"><span data-stu-id="9acfc-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="9acfc-218">Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="9acfc-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="9acfc-219">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9acfc-219">Click New.</span></span>
3. <span data-ttu-id="9acfc-220">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="9acfc-221">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9acfc-222">Klicken Sie auf Positionen.</span><span class="sxs-lookup"><span data-stu-id="9acfc-222">Click Lines.</span></span>
6. <span data-ttu-id="9acfc-223">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="9acfc-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="9acfc-224">Geben Sie im Feld "Konto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="9acfc-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="9acfc-225">Klicken Sie auf Transaktionen ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="9acfc-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="9acfc-226">Erweitern Sie den Abschnitt "Summen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="9acfc-227">Wählen Sie im Feld 'Anzeigen:' eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="9acfc-228">Überprüfen Sie, ob die Felder "Bankdokumentnummer" und "Liefernummer" aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9acfc-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="9acfc-229">Wählen Sie das Kontrollkästchen "Markieren" aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="9acfc-230">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9acfc-230">Click OK.</span></span>
13. <span data-ttu-id="9acfc-231">Klicken Sie auf die Registerkarte Zahlung.</span><span class="sxs-lookup"><span data-stu-id="9acfc-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="9acfc-232">Überprüfen Sie, ob die Felder "Bankdokumentnummer" und "Liefernummer" aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9acfc-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="9acfc-233">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="9acfc-233">Click Post.</span></span>
15. <span data-ttu-id="9acfc-234">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-234">Close the page.</span></span>
16. <span data-ttu-id="9acfc-235">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="9acfc-236">Überprüfen Sie den Status des Importkreditbriefs nach gezahlter Rechnung.</span><span class="sxs-lookup"><span data-stu-id="9acfc-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="9acfc-237">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Importkreditbrief und Importinkasso".</span><span class="sxs-lookup"><span data-stu-id="9acfc-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="9acfc-238">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9acfc-239">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9acfc-240">Überprüfen Sie den Importkreditbriefstatus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="9acfc-241">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="9acfc-242">Überprüfen Sie das Bankfazilitätslimit und den Auslastungsbericht.</span><span class="sxs-lookup"><span data-stu-id="9acfc-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="9acfc-243">Wechseln Sie zu "Bargeld und Bankverwaltung" > "Abfragen und Berichte" > "Kreditbrief oder Garantie" > "Bankfazilitäten und Auslastungsbericht".</span><span class="sxs-lookup"><span data-stu-id="9acfc-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="9acfc-244">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="9acfc-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="9acfc-245">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="9acfc-245">Click Filter.</span></span>
    * <span data-ttu-id="9acfc-246">Definieren Sie das Feld "Kriterien" über das erforderliche Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="9acfc-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="9acfc-247">Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9acfc-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="9acfc-248">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9acfc-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9acfc-249">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9acfc-249">Click OK.</span></span>
7. <span data-ttu-id="9acfc-250">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9acfc-250">Click OK.</span></span>
    * <span data-ttu-id="9acfc-251">Überprüfen Sie den Bericht, in dem die Transaktionen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="9acfc-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="9acfc-252">Überprüfen Sie, ob der Bericht Transaktionen mit Bankdokumentnummer, Einrichtungsgrenze, Auslastungsbetrag und dem Einrichtungsbilanzbetrag auflistet.</span><span class="sxs-lookup"><span data-stu-id="9acfc-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="9acfc-253">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9acfc-253">Close the page.</span></span>


