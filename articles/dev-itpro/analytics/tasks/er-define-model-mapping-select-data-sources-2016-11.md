---
title: EB-Modellzuordnungen definieren und Datenquellen für sie auswählen
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, ein Modell der elektronischen Berichterstellung auswählen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46dc13416aa094f33879c017c1a1815fc791409d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850350"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="9fffa-103">EB-Modellzuordnungen definieren und Datenquellen für sie auswählen</span><span class="sxs-lookup"><span data-stu-id="9fffa-103">Define ER model mappings and select data sources for them</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fffa-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, ein Modell der elektronischen Berichterstellung (ER) auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="9fffa-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="9fffa-105">Die Datenquellen werden einzelnen Komponenten des ausgewählten Datenmodells zur Entwurfszeit und Daten zu diesem Datenmodell zur Laufzeit aufzufüllen verbunden.</span><span class="sxs-lookup"><span data-stu-id="9fffa-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="9fffa-106">In diesem Beispiel wählen Sie Datenquellen für ein bestehendes Datenmodell, das für das Beispielunternehmen Litware, Inc. erstellt wurde. Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in der Prozedur "Erstellen eines neuen Datenmodells abschließen".</span><span class="sxs-lookup"><span data-stu-id="9fffa-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="9fffa-107">Die Konfigurationsstruktur „Elektronische Berichterstellung” öffnen</span><span class="sxs-lookup"><span data-stu-id="9fffa-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="9fffa-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="9fffa-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9fffa-109">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="9fffa-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="9fffa-110">Hinzufügen einer Zuordnung des neuen Modells</span><span class="sxs-lookup"><span data-stu-id="9fffa-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="9fffa-111">Wählen Sie 'Zahlungen (vereinfachtes Modell)' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="9fffa-112">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="9fffa-112">Click Designer.</span></span>
3. <span data-ttu-id="9fffa-113">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="9fffa-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="9fffa-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9fffa-114">Click New.</span></span>
    * <span data-ttu-id="9fffa-115">Dieses erstellt einen neuen Datensatzes, der das Datenmodell Datenquellen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="9fffa-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="9fffa-116">In diesem Beispiel ordnen Sie das Datenmodell Datenquellen für den gewünschten Zahlungstyp zu: Banküberweisung.</span><span class="sxs-lookup"><span data-stu-id="9fffa-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="9fffa-117">Es ist möglich, mehr als eine Zuordnung für ein bestimmtes Datenmodell zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="9fffa-118">So können Sie beispielsweise eine Zuordnung für unterschiedliche Arten von Zahlungen, wie für Direktbelastung oder für Banküberweisungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="9fffa-119">In diesem Beispiel erstellen Sie eine Verknüpfung für Banküberweisungen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="9fffa-120">Geben Sie im Feld "Name" "CT mapping" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="9fffa-121">BÜ-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="9fffa-121">CT mapping</span></span>  
6. <span data-ttu-id="9fffa-122">Geben Sie im Feld "Beschreibung" "Payment model mapping CT" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="9fffa-123">Zahlungsmodell zuordnen BÜ</span><span class="sxs-lookup"><span data-stu-id="9fffa-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="9fffa-124">Geben Sie im Feld „Definition” die Bezeichnung „CustomerCreditTransferInitiation” ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="9fffa-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="9fffa-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="9fffa-126">ResolveChanges die Definition.</span><span class="sxs-lookup"><span data-stu-id="9fffa-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="9fffa-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9fffa-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="9fffa-128">Benötigte Datenquellen für die Strommodellzuordnung definieren</span><span class="sxs-lookup"><span data-stu-id="9fffa-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="9fffa-129">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="9fffa-129">Click Designer.</span></span>
2. <span data-ttu-id="9fffa-130">Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabellendatensätze' aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="9fffa-131">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="9fffa-131">Click Add root.</span></span>
    * <span data-ttu-id="9fffa-132">Geben Sie diese Datenquelle ein, um Zahlungsbuchungen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="9fffa-133">Geben Sie im Feld "Name" 'Transactions' ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="9fffa-134">Buchungen</span><span class="sxs-lookup"><span data-stu-id="9fffa-134">Transactions</span></span>  
5. <span data-ttu-id="9fffa-135">Geben Sie im Feld Beschreibung "Transactions" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="9fffa-136">Buchungen</span><span class="sxs-lookup"><span data-stu-id="9fffa-136">Transactions</span></span>  
6. <span data-ttu-id="9fffa-137">Geben Sie ins Feld Hilfe "Sachkontenerfassungs-Positionen" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="9fffa-138">Sachkontoerfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="9fffa-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="9fffa-139">Wählen Sie "Ja" im Feld "Ask for query".</span><span class="sxs-lookup"><span data-stu-id="9fffa-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="9fffa-140">Wählen Sie Ja aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-140">Select Yes.</span></span>  
8. <span data-ttu-id="9fffa-141">Im Tabellenfeld geben Sie "LedgerJournalTrans" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="9fffa-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="9fffa-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="9fffa-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9fffa-143">Click OK.</span></span>
    * <span data-ttu-id="9fffa-144">Wählen Sie die Tabelle "LedgerJournalTrans" als Datenquelle für das Modell der aktuellen Daten aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="9fffa-145">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="9fffa-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-146">Click Add.</span></span>
    * <span data-ttu-id="9fffa-147">Klicken Sie auf Hinzufügen, um ein neues berechnetes Feld hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="9fffa-148">Geben Sie im Feld "Name" '$EndToEndID' ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="9fffa-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="9fffa-149">$EndToEndID</span></span>  
13. <span data-ttu-id="9fffa-150">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9fffa-150">Click Edit formula.</span></span>
14. <span data-ttu-id="9fffa-151">Wählen Sie in der Struktur 'String\CONCATENATE' aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="9fffa-152">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-152">Click Add function.</span></span>
16. <span data-ttu-id="9fffa-153">Erweitern Sie in der Struktur den Knoten 'Transactions'.</span><span class="sxs-lookup"><span data-stu-id="9fffa-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="9fffa-154">Wählen Sie in der Struktur 'Transactions\Voucher' aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="9fffa-155">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-155">Click Add data source.</span></span>
19. <span data-ttu-id="9fffa-156">Im Feld „Formel” geben Sie „CONCATENATE(Transactions.Voucher, „-", „ ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="9fffa-157">Geben Sie [ , “-“, ] am Ende der Formel ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="9fffa-158">Wählen Sie in der Struktur den Knoten 'String\TEXT'.</span><span class="sxs-lookup"><span data-stu-id="9fffa-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="9fffa-159">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-159">Click Add function.</span></span>
22. <span data-ttu-id="9fffa-160">Wählen Sie in der Strukturdarstellung "Transactions\Record-ID (RecId)" aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="9fffa-161">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-161">Click Add data source.</span></span>
24. <span data-ttu-id="9fffa-162">Im Feld „Formel” geben Sie „CONCATENATE(Transactions.Voucher, „-", TEXT(Transactions.RecId))” ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="9fffa-163">Geben Sie [))] am Ende der Formel ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="9fffa-164">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9fffa-164">Click Save.</span></span>
    * <span data-ttu-id="9fffa-165">Stellen Sie sicher, dass keine Fehler für die erstellte Formel ermittelt worden sind.</span><span class="sxs-lookup"><span data-stu-id="9fffa-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="9fffa-166">Sehen Sie sich die Registerkarte FEHLER unter dem Formeleditorsteuerelement an.</span><span class="sxs-lookup"><span data-stu-id="9fffa-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="9fffa-167">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fffa-167">Close the page.</span></span>
27. <span data-ttu-id="9fffa-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9fffa-168">Click OK.</span></span>
    * <span data-ttu-id="9fffa-169">Fügen Sie das berechnete Feld dieser Datenquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="9fffa-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="9fffa-170">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-170">Click Add.</span></span>
    * <span data-ttu-id="9fffa-171">Klicken Sie auf Hinzufügen, um ein neues berechnetes Feld hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="9fffa-172">Geben Sie im Feld Namen $Amount ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="9fffa-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="9fffa-173">$Amount</span></span>  
30. <span data-ttu-id="9fffa-174">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9fffa-174">Click Edit formula.</span></span>
31. <span data-ttu-id="9fffa-175">Erweitern Sie in der Struktur den Knoten 'Transactions'.</span><span class="sxs-lookup"><span data-stu-id="9fffa-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="9fffa-176">Wählen Sie in der Strukturdarstellung "Transactions\Debit(AmountCurDebit)" aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="9fffa-177">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-177">Click Add data source.</span></span>
34. <span data-ttu-id="9fffa-178">Im Feld „Formel” geben Sie „Transactions.AmountCurDebit - „ ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="9fffa-179">Geben Sie [ - ] am Ende der Formel ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="9fffa-180">Wählen Sie in der Strukturdarstellung "Transactions\Credit(AmountCurCredit)" aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="9fffa-181">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-181">Click Add data source.</span></span>
37. <span data-ttu-id="9fffa-182">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9fffa-182">Click Save.</span></span>
38. <span data-ttu-id="9fffa-183">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fffa-183">Close the page.</span></span>
39. <span data-ttu-id="9fffa-184">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9fffa-184">Click OK.</span></span>
    * <span data-ttu-id="9fffa-185">Hierdurch wird das $Amount-berechnete Feld der ausgewählten Datenquelle für das Modell der aktuellen Daten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9fffa-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="9fffa-186">Wählen Sie in der Struktur 'Transaktion\$Betrag' aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="9fffa-187">Erweitern Sie in der Struktur den Knoten 'Transactions'.</span><span class="sxs-lookup"><span data-stu-id="9fffa-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="9fffa-188">In der Struktur erweitern oder reduzieren Sie „Buchungen\$Betrag”.</span><span class="sxs-lookup"><span data-stu-id="9fffa-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="9fffa-189">Erweitern oder reduzieren Sie „Buchungen” in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="9fffa-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="9fffa-190">Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabellendatensätze' aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="9fffa-191">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="9fffa-191">Click Add root.</span></span>
    * <span data-ttu-id="9fffa-192">Geben Sie diese Datenquelle ein, um die Bankkontodetails des Unternehmens zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="9fffa-193">Geben Sie im Feld "Name" "BankAccount" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="9fffa-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="9fffa-194">BankAccount</span></span>  
47. <span data-ttu-id="9fffa-195">Geben Sie im Feld Beschreibung "Bank Account" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="9fffa-196">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="9fffa-196">Bank Account</span></span>  
48. <span data-ttu-id="9fffa-197">Geben Sie im Feld Hilfe "Bank Account" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="9fffa-198">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="9fffa-198">Bank Account</span></span>  
49. <span data-ttu-id="9fffa-199">Wählen Sie "Ja" im Feld "Ask for query".</span><span class="sxs-lookup"><span data-stu-id="9fffa-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="9fffa-200">Wählen Sie Ja aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-200">Select Yes.</span></span>  
50. <span data-ttu-id="9fffa-201">Im Tabellenfeld geben Sie "BankAccountTable" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="9fffa-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="9fffa-202">BankAccountTable</span></span>  
51. <span data-ttu-id="9fffa-203">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9fffa-203">Click OK.</span></span>
    * <span data-ttu-id="9fffa-204">Wählen Sie die Tabelle "BankAccountTable" als Datenquelle für das Modell der aktuellen Daten aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="9fffa-205">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="9fffa-205">Click Add root.</span></span>
    * <span data-ttu-id="9fffa-206">Geben Sie diese Datenquelle ein, um die Anforderungen des Unternehmens zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="9fffa-207">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="9fffa-208">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="9fffa-208">Company</span></span>  
54. <span data-ttu-id="9fffa-209">Geben Sie im Feld Beschreibung einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="9fffa-210">Unternehmensdaten</span><span class="sxs-lookup"><span data-stu-id="9fffa-210">Company information</span></span>  
55. <span data-ttu-id="9fffa-211">Geben Sie im Feld Hilfe "Company information" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="9fffa-212">Unternehmensdaten</span><span class="sxs-lookup"><span data-stu-id="9fffa-212">Company information</span></span>  
56. <span data-ttu-id="9fffa-213">Wählen Sie "Ja" im Feld "Ask for query".</span><span class="sxs-lookup"><span data-stu-id="9fffa-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="9fffa-214">Wählen Sie Ja aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-214">Select Yes.</span></span>  
57. <span data-ttu-id="9fffa-215">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="9fffa-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="9fffa-216">CompanyInfo</span></span>  
58. <span data-ttu-id="9fffa-217">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9fffa-217">Click OK.</span></span>
    * <span data-ttu-id="9fffa-218">Wählen Sie die Tabelle "CompanyInfo" als Datenquelle für das Modell der aktuellen Daten aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="9fffa-219">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="9fffa-220">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="9fffa-220">Click Add root.</span></span>
    * <span data-ttu-id="9fffa-221">Fügen Sie ein berechnetes Feld als neue Datenquelle ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="9fffa-222">Geben Sie im Feld "Name" 'ProcessingDateTime' ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="9fffa-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="9fffa-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="9fffa-224">Im Feld Beschriftung geben Sie "Verarbeiten von Datum und Zeit" ein.</span><span class="sxs-lookup"><span data-stu-id="9fffa-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="9fffa-225">Datum und Uhrzeit der Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="9fffa-225">Processing date & time</span></span>  
63. <span data-ttu-id="9fffa-226">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9fffa-226">Click Edit formula.</span></span>
64. <span data-ttu-id="9fffa-227">In der Struktur wählen Sie „Datum/Uhrzeit\SESSIONNOW” aus.</span><span class="sxs-lookup"><span data-stu-id="9fffa-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="9fffa-228">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fffa-228">Click Add function.</span></span>
66. <span data-ttu-id="9fffa-229">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9fffa-229">Click Save.</span></span>
67. <span data-ttu-id="9fffa-230">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fffa-230">Close the page.</span></span>
68. <span data-ttu-id="9fffa-231">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9fffa-231">Click OK.</span></span>
    * <span data-ttu-id="9fffa-232">Fügen Sie das ProcessingDateTime-berechnete Feld als Datenquelle für das Modell der aktuellen Daten.</span><span class="sxs-lookup"><span data-stu-id="9fffa-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="9fffa-233">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9fffa-233">Click Save.</span></span>
70. <span data-ttu-id="9fffa-234">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fffa-234">Close the page.</span></span>
71. <span data-ttu-id="9fffa-235">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fffa-235">Close the page.</span></span>
72. <span data-ttu-id="9fffa-236">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fffa-236">Close the page.</span></span>

