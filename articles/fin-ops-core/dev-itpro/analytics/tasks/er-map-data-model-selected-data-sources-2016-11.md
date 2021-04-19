---
title: Er-Datenmodell zu den ausgewählten Datenquellen zuordnen
description: In diesem Thema wird beschrieben, wie Sie ein EB-Datenmodell (elektronische Berichterstellung) ausgewählten Microsoft Dynamics 365 Finance-Datenquellen zuordnen.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0eb7f48a50e32637003c1488d80899a704709068
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751485"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="cea40-103">Er-Datenmodell zu den ausgewählten Datenquellen zuordnen</span><span class="sxs-lookup"><span data-stu-id="cea40-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cea40-104">In den folgenden Schritten wird erläutert, wie ein Benutzer in der Rolle „Systemadministrator” oder „Entwickler für elektronische Berichterstellung” ein Datenmodell der elektronischen Berichterstellung (EB) ausgewählten Datenquellen, zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="cea40-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="cea40-105">Diese vorbildliche Zuordnung wird später als Datenquelle in einer Formatkonfiguration verwendet, die verwendet wird, um Dokumente für den elektronischen Zahlungsverkehr zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="cea40-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="cea40-106">In diesem Beispiel verknüpfen Sie ein Datenmodell für das Beispielunternehmen, Litware, Inc. mit Datenquellen.</span><span class="sxs-lookup"><span data-stu-id="cea40-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="cea40-107">Um diese Schritte abzuschließen, die folgenden Schritte in der „Datenquellen für Modell-Zuordnung“ im Verfahren zuerst abschließen.</span><span class="sxs-lookup"><span data-stu-id="cea40-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="cea40-108">Öffnen Sie ER-Konfigurationsstruktur</span><span class="sxs-lookup"><span data-stu-id="cea40-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="cea40-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="cea40-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cea40-110">Klicken Sie auf "Konfigurationen".</span><span class="sxs-lookup"><span data-stu-id="cea40-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="cea40-111">Wählen Sie erstellte Model-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="cea40-111">Select created model mapping</span></span>
1. <span data-ttu-id="cea40-112">Wählen Sie 'Zahlungen (vereinfachtes Modell)' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="cea40-113">Stellen Sie sicher, dass die Modellkonfiguration „Zahlungen (vereinfachtes Modell)“ im Voraus erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cea40-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="cea40-114">Andernfalls beenden Sie jetzt und kehren nach Abschluss des Aufgabenleitfadens „Erstellen einer neuer Konfiguration mit dem Datenmodell der ausgewählten Domäne“ zurück.</span><span class="sxs-lookup"><span data-stu-id="cea40-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="cea40-115">Klicken Sie auf "Modelldesigner".</span><span class="sxs-lookup"><span data-stu-id="cea40-115">Click Model designer.</span></span>
3. <span data-ttu-id="cea40-116">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="cea40-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="cea40-117">Wählen Sie den "CT-Zuordnungs" Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="cea40-118">BÜ-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="cea40-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="cea40-119">Binden Sie erstellte Datenquellen an Datenmodell-Elemente</span><span class="sxs-lookup"><span data-stu-id="cea40-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="cea40-120">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="cea40-120">Click Designer.</span></span>
2. <span data-ttu-id="cea40-121">In der Struktur wählen Sie Datums und Zeit (ProcessingDateTime) aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="cea40-122">In der Struktur wählen Sie "Datum" (ProcessingDateTime)".</span><span class="sxs-lookup"><span data-stu-id="cea40-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="cea40-123">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-123">Click Bind.</span></span>
5. <span data-ttu-id="cea40-124">Wählen Sie in der Strukturdarstellung "Zahlungsnachrichtenkennung (MessageIdentification )" aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="cea40-125">Erweitern Sie in der Struktur den Knoten 'Transactions'.</span><span class="sxs-lookup"><span data-stu-id="cea40-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="cea40-126">In der Struktur ausgewählte "Buchungs- \ Erfassungsstapelnummer (JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="cea40-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="cea40-127">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-127">Click Bind.</span></span>
9. <span data-ttu-id="cea40-128">Wählen Sie in der Struktur 'Zahlungen' aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="cea40-129">Wählen Sie in der Struktur 'Transactions' aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="cea40-130">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-130">Click Bind.</span></span>
12. <span data-ttu-id="cea40-131">Erweitern Sie 'Payments= Transactions' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="cea40-132">Erweitern Sie 'Payments= Transactions\Creditor' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="cea40-133">Erweitern Sie 'Payments= Transactions\Creditor\Account' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="cea40-134">In der Struktur ausgewählte "Payments=-Buchungen\Kreditgeber\Konto\Währungscode (Währung)".</span><span class="sxs-lookup"><span data-stu-id="cea40-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="cea40-135">In der Struktur erweitern Sie "Transactions\vendBankAccountInTransactionCompany()".</span><span class="sxs-lookup"><span data-stu-id="cea40-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="cea40-136">In der Struktur ausgewählte "Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="cea40-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="cea40-137">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-137">Click Bind.</span></span>
19. <span data-ttu-id="cea40-138">In der Struktur ausgewählte "Payments=-Buchungen\Kreditgeber\Konto\IBAN code(IBAN)".</span><span class="sxs-lookup"><span data-stu-id="cea40-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="cea40-139">In der Struktur wählen Sie aus "Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)".</span><span class="sxs-lookup"><span data-stu-id="cea40-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="cea40-140">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-140">Click Bind.</span></span>
22. <span data-ttu-id="cea40-141">Wählen Sie 'Payments= Transactions\Creditor\Account\Number' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="cea40-142">In der Struktur ausgewählte "Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="cea40-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="cea40-143">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-143">Click Bind.</span></span>
25. <span data-ttu-id="cea40-144">Erweitern Sie 'Payments= Transactions\Creditor\Agent' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="cea40-145">Wählen Sie 'Payments= Transactions\Creditor\Account\Agent\Name' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="cea40-146">In der Struktur wählen Sie "Transactions\vendBankAccountInTransactionCompany()\Name" aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="cea40-147">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-147">Click Bind.</span></span>
29. <span data-ttu-id="cea40-148">Wählen Sie 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="cea40-149">In der Struktur ausgewählte "Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)".</span><span class="sxs-lookup"><span data-stu-id="cea40-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="cea40-150">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-150">Click Bind.</span></span>
32. <span data-ttu-id="cea40-151">In der Struktur ausgewählte "Payments=-Buchungen\Kreditgeber\Agent\SWIFT code(SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="cea40-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="cea40-152">In der Struktur ausgewählte "Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="cea40-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="cea40-153">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-153">Click Bind.</span></span>
35. <span data-ttu-id="cea40-154">Wählen Sie 'Payments= Transactions\Creditor\Account\Name' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="cea40-155">Erweitern Sie 'Transactions\findVendTable()' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="cea40-156">In der Struktur wählen Sie Transactions\findVendTable()\name()'.</span><span class="sxs-lookup"><span data-stu-id="cea40-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="cea40-157">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-157">Click Bind.</span></span>
39. <span data-ttu-id="cea40-158">In der Struktur ausgewählte "Payments=-Buchungen\Währungscode (Währung)".</span><span class="sxs-lookup"><span data-stu-id="cea40-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="cea40-159">Erweitern Sie 'Transactions\>Relations' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="cea40-160">In der Struktur erweitern Sie "Buchungen\>Geschäftsbeziehung \ Währungstabelle (Währung)".</span><span class="sxs-lookup"><span data-stu-id="cea40-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="cea40-161">Wählen Sie in der Strukturdarstellung "Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)".</span><span class="sxs-lookup"><span data-stu-id="cea40-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="cea40-162">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-162">Click Bind.</span></span>
44. <span data-ttu-id="cea40-163">Erweitern Sie 'Payments= Transactions\Debtor' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="cea40-164">Erweitern Sie 'Payments= Transactions\Debtor\Account' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="cea40-165">In der Struktur ausgewählte "Payments=-Buchungen\Debtor\Konto\Währungscode (Währung)".</span><span class="sxs-lookup"><span data-stu-id="cea40-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="cea40-166">Wählen Sie in der Struktur 'Bank Account(BankAccount)' aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="cea40-167">Erweitern Sie in der Struktur 'Bank Account(BankAccount)'.</span><span class="sxs-lookup"><span data-stu-id="cea40-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="cea40-168">In der Struktur ausgewählte "Bank Account(BankAccount)\Currency(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="cea40-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="cea40-169">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-169">Click Bind.</span></span>
51. <span data-ttu-id="cea40-170">Wählen Sie in der Struktur 'Bank Account(BankAccount)\IBAN' aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="cea40-171">In der Struktur ausgewählte "Payments=-Buchungen\Debtor\Konto\IBAN code(IBAN)".</span><span class="sxs-lookup"><span data-stu-id="cea40-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="cea40-172">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-172">Click Bind.</span></span>
54. <span data-ttu-id="cea40-173">Wählen Sie 'Payments= Transactions\Debtor\Account\Number' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="cea40-174">In Struktur, auswählen "Bank Account(BankAccount)\Bank account number(AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="cea40-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="cea40-175">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-175">Click Bind.</span></span>
57. <span data-ttu-id="cea40-176">Erweitern Sie 'Payments= Transactions\Debtor\Agent' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea40-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="cea40-177">Wählen Sie 'Payments= Transactions\Debtor\Account\Agent\Name' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="cea40-178">Wählen Sie in der Struktur 'Bank Account(BankAccount)\Name' aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="cea40-179">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-179">Click Bind.</span></span>
61. <span data-ttu-id="cea40-180">Wählen Sie 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="cea40-181">In Struktur, auswählen "Bank Account(BankAccount)\Routing number(RegistrationNum)".</span><span class="sxs-lookup"><span data-stu-id="cea40-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="cea40-182">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-182">Click Bind.</span></span>
64. <span data-ttu-id="cea40-183">In der Struktur ausgewählte "Payments=-Buchungen\Debtor\Agent\SWIFT code(SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="cea40-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="cea40-184">In der Struktur ausgewählte "Bank Account(BankAccount)\SWIFT code(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="cea40-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="cea40-185">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-185">Click Bind.</span></span>
67. <span data-ttu-id="cea40-186">Wählen Sie 'Payments= Transactions\Debtor\Account\Name' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="cea40-187">Wählen Sie in der Strukturdarstellung "Unternehmensdaten (Unternehmen") aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="cea40-188">Erweitern Sie in der Strukturdarstellung "Unternehmensdaten (Unternehmen)".</span><span class="sxs-lookup"><span data-stu-id="cea40-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="cea40-189">Wählen Sie in der Strukturdarstellung "Unternehmensdaten (Unternehmen)\Name" aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="cea40-190">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-190">Click Bind.</span></span>
72. <span data-ttu-id="cea40-191">Wählen Sie 'Payments= Transactions\Description' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="cea40-192">Wählen Sie 'Transactions\Description(Txt)' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="cea40-193">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-193">Click Bind.</span></span>
75. <span data-ttu-id="cea40-194">In der Struktur ausgewählte "Payments= Transactions\End to end identification code(End2EndID)".</span><span class="sxs-lookup"><span data-stu-id="cea40-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="cea40-195">Wählen Sie in der Struktur\$TransactionsEndToEndID' aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="cea40-196">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-196">Click Bind.</span></span>
78. <span data-ttu-id="cea40-197">In der Struktur wählen Sie "Payments=-Buchungen \ Betrag (InstructedAmount)" aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="cea40-198">Wählen Sie in der Struktur 'Transaktion\$Betrag' aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="cea40-199">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-199">Click Bind.</span></span>
81. <span data-ttu-id="cea40-200">Wählen Sie in der Strukturdarstellung "Payments= Transactions\Transaction date(TransactionDate)" aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="cea40-201">Wählen Sie 'Transactions\Date(TransDate)' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="cea40-202">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cea40-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="cea40-203">Erstellte Zuordnung validieren</span><span class="sxs-lookup"><span data-stu-id="cea40-203">Validate created mapping</span></span>
1. <span data-ttu-id="cea40-204">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="cea40-204">Click Validate.</span></span>
    * <span data-ttu-id="cea40-205">Überprüft die neue Zuordnung, um sicherzustellen, dass alle Bindungen in Ordnung sind.</span><span class="sxs-lookup"><span data-stu-id="cea40-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="cea40-206">Klicken Sie zum Erweitern oder Reduzieren des Abschnitts Fehlerliste auf den Pfeil.</span><span class="sxs-lookup"><span data-stu-id="cea40-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="cea40-207">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="cea40-207">Click Save.</span></span>
4. <span data-ttu-id="cea40-208">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cea40-208">Close the page.</span></span>
5. <span data-ttu-id="cea40-209">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cea40-209">Close the page.</span></span>
6. <span data-ttu-id="cea40-210">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cea40-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="cea40-211">Ändern Sie den Status der aktuellen Version der Modellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cea40-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="cea40-212">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="cea40-212">Click Change status.</span></span>
    * <span data-ttu-id="cea40-213">Ändern Sie den Status der entworfenen Modellkonfiguration – von „Entwurf” zu „Abgeschlossen”, um es für die Generierung des Zahlungsformatdesigns verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="cea40-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="cea40-214">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="cea40-214">Click Complete.</span></span>
    * <span data-ttu-id="cea40-215">Wählen Sie „Abgeschlossen” aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-215">Select Complete.</span></span>  
3. <span data-ttu-id="cea40-216">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="cea40-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="cea40-217">Beispielsweise „Version 1”.</span><span class="sxs-lookup"><span data-stu-id="cea40-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="cea40-218">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cea40-218">Click OK.</span></span>
5. <span data-ttu-id="cea40-219">Wählen Sie die abgeschlossene Version der aktuellen Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="cea40-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="cea40-220">Beachten Sie, dass die erstellte Konfiguration als abgeschlossene Version 1 gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="cea40-220">Note that the created configuration is saved as completed version 1.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]