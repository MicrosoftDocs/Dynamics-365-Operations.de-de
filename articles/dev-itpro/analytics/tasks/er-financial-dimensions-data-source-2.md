--- 
title: "Zuordnen von Modellen zum Verwenden von Finanzdimensionen als Datenquelle für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: a5fa6fb07fb2ba08812826acba748b38738bb468
ms.contentlocale: de-de
ms.lasthandoff: 03/09/2018

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="f213c-103">Zuordnen von Modellen zum Verwenden von Finanzdimensionen als Datenquelle für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="f213c-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f213c-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="f213c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f213c-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f213c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f213c-106">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren "ER - Finanzdimensionen als Datenquelle nutzen (Teil 1: Design des Datenmodells)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="f213c-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="f213c-107">Hinzufügen von erforderlichen Datenquellen zur Modellzuordnung</span><span class="sxs-lookup"><span data-stu-id="f213c-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="f213c-108">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f213c-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f213c-109">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="f213c-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f213c-110">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="f213c-110">Click Designer.</span></span>
4. <span data-ttu-id="f213c-111">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="f213c-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="f213c-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f213c-112">Click New.</span></span>
6. <span data-ttu-id="f213c-113">Wählen Sie im Feld "Definition" "Erfassung" aus.</span><span class="sxs-lookup"><span data-stu-id="f213c-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="f213c-114">Geben Sie im Feld "Name" "Dimensionsdatenzuordnung" ein.</span><span class="sxs-lookup"><span data-stu-id="f213c-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="f213c-115">Geben Sie im Feld "Beschreibung" "Dimensionsdatenzuordnung" ein.</span><span class="sxs-lookup"><span data-stu-id="f213c-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="f213c-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f213c-116">Click Save.</span></span>
10. <span data-ttu-id="f213c-117">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="f213c-117">Click Designer.</span></span>
11. <span data-ttu-id="f213c-118">Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabelle" aus.</span><span class="sxs-lookup"><span data-stu-id="f213c-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="f213c-119">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f213c-119">Click Add root.</span></span>
13. <span data-ttu-id="f213c-120">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="f213c-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="f213c-121">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="f213c-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="f213c-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f213c-122">Click OK.</span></span>
16. <span data-ttu-id="f213c-123">Wählen Sie in der Struktur "Funktionen\Finanzdimensionsdetails".</span><span class="sxs-lookup"><span data-stu-id="f213c-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="f213c-124">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f213c-124">Click Add root.</span></span>
    * <span data-ttu-id="f213c-125">Diese Datenquelle gibt an, wie der Bereich der Finanzdimensionen für einen Bericht definiert wird, der dieses Modell als Datenquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="f213c-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="f213c-126">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f213c-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="f213c-127">Wählen Sie "Ja" im Feld "Dimensionen anfordern".</span><span class="sxs-lookup"><span data-stu-id="f213c-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="f213c-128">Wählen Sie die Option Ja aus, um dem Benutzer die Auswahl zur Laufzeit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f213c-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="f213c-129">Bei "Neun" werden standardmäßig alle Finanzdimensionen der aktuellen Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="f213c-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="f213c-130">Wählen Sie im Feld Finanzdimensionen "Juristische Person" aus.</span><span class="sxs-lookup"><span data-stu-id="f213c-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="f213c-131">Wählen Sie "Alle" aus, um dem Benutzer die Auswahl der gewünschten Dimensionen für die aktuelle Instanz zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f213c-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="f213c-132">Wählen Sie "Juristische Person" aus, um dem Benutzer die Auswahl der Dimensionen für das Unternehmen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f213c-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="f213c-133">Wählen Sie "Dimension" aus, um dem Benutzer die Auswahl von Dimensionen über einen einzelnen Dimensionssatzes zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f213c-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="f213c-134">Wählen Sie "Ja" im Feld "Hauptkonto anfordern".</span><span class="sxs-lookup"><span data-stu-id="f213c-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="f213c-135">Legen Sie "Hauptkonto anfordern" auf "Ja" fest, um Benutzern zu ermöglichen, das Hauptkonto als Teil der Liste mit den Dimensionen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f213c-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="f213c-136">Bei "Nein" wird das Hauptkonto nicht in der Liste mit den Dimensionen aufgenommen und die Option "Hauptkonto erforderlich" ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f213c-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="f213c-137">Wenn "Hauptkonto erforderlich" auf Ja festgelegt ist, wird das Hauptkonto unabhängig von der Auswahl des Benutzers in der Liste mit den Dimensionen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f213c-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="f213c-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f213c-138">Click OK.</span></span>
23. <span data-ttu-id="f213c-139">Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabellendatensätze" aus.</span><span class="sxs-lookup"><span data-stu-id="f213c-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="f213c-140">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f213c-140">Click Add root.</span></span>
25. <span data-ttu-id="f213c-141">Geben Sie im Feld "Name" "LedgerJournal" ein.</span><span class="sxs-lookup"><span data-stu-id="f213c-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="f213c-142">Wählen Sie "Ja" im Feld "Ask for query".</span><span class="sxs-lookup"><span data-stu-id="f213c-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="f213c-143">Im Tabellenfeld geben Sie "LedgerJournalTable" ein.</span><span class="sxs-lookup"><span data-stu-id="f213c-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="f213c-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f213c-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="f213c-145">Zuordnen von Datenmodell-Elementen zu hinzugefügten Datenquellen</span><span class="sxs-lookup"><span data-stu-id="f213c-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="f213c-146">Erweitern Sie in der Struktur 'Erfassung'.</span><span class="sxs-lookup"><span data-stu-id="f213c-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="f213c-147">Erweitern Sie in der Struktur 'Erfassung\Buchung'.</span><span class="sxs-lookup"><span data-stu-id="f213c-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="f213c-148">Erweitern Sie in der Struktur 'Erfassung\Buchung\Dimensionsdaten'.</span><span class="sxs-lookup"><span data-stu-id="f213c-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="f213c-149">Erweitern Sie 'Dimensionseinstellung' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f213c-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="f213c-150">Erweitern Sie in der Struktur "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="f213c-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="f213c-151">Erweitern Sie 'LedgerJournal\\<Relations' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f213c-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="f213c-152">Erweitern Sie 'LedgerJournal\<Relations\LedgerJournalTrans' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f213c-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="f213c-153">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f213c-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="f213c-154">Wählen Sie in der Struktur 'Erfassung\Buchung\Beleg'.</span><span class="sxs-lookup"><span data-stu-id="f213c-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="f213c-155">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-155">Click Bind.</span></span>
11. <span data-ttu-id="f213c-156">Wählen Sie in der Strukturdarstellung 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="f213c-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="f213c-157">Beachten Sie, dass für jede Referenz zu Finanzdimensionen, die beispielsweise auf LedgerDimension festgelegt ist, ein entsprechender Datenquellenartikel verfügbar ist (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="f213c-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="f213c-158">Dieser Datenquellenartikel bietet die Finanzdimensionen des Dimensionssatzes als Liste des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="f213c-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="f213c-159">Erweitern Sie in der Strukturdarstellung 'LedgerJournal\\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="f213c-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="f213c-160">Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="f213c-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="f213c-161">Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span><span class="sxs-lookup"><span data-stu-id="f213c-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="f213c-162">Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Definitionen'.</span><span class="sxs-lookup"><span data-stu-id="f213c-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="f213c-163">Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Definitionen\Name'.</span><span class="sxs-lookup"><span data-stu-id="f213c-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="f213c-164">Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Name'.</span><span class="sxs-lookup"><span data-stu-id="f213c-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="f213c-165">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-165">Click Bind.</span></span>
19. <span data-ttu-id="f213c-166">Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span><span class="sxs-lookup"><span data-stu-id="f213c-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="f213c-167">Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Description'.</span><span class="sxs-lookup"><span data-stu-id="f213c-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="f213c-168">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-168">Click Bind.</span></span>
22. <span data-ttu-id="f213c-169">Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span><span class="sxs-lookup"><span data-stu-id="f213c-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="f213c-170">Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Code'.</span><span class="sxs-lookup"><span data-stu-id="f213c-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="f213c-171">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-171">Click Bind.</span></span>
25. <span data-ttu-id="f213c-172">Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="f213c-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="f213c-173">Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="f213c-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="f213c-174">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-174">Click Bind.</span></span>
28. <span data-ttu-id="f213c-175">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span><span class="sxs-lookup"><span data-stu-id="f213c-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="f213c-176">Wählen Sie in der Struktur 'Erfassung\Buchung\Debit'.</span><span class="sxs-lookup"><span data-stu-id="f213c-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="f213c-177">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-177">Click Bind.</span></span>
31. <span data-ttu-id="f213c-178">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span><span class="sxs-lookup"><span data-stu-id="f213c-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="f213c-179">Wählen Sie in der Struktur 'Erfassung\Buchung\Date'.</span><span class="sxs-lookup"><span data-stu-id="f213c-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="f213c-180">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-180">Click Bind.</span></span>
34. <span data-ttu-id="f213c-181">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="f213c-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="f213c-182">Wählen Sie in der Struktur 'Journal\Transaction\Currency'.</span><span class="sxs-lookup"><span data-stu-id="f213c-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="f213c-183">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-183">Click Bind.</span></span>
37. <span data-ttu-id="f213c-184">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span><span class="sxs-lookup"><span data-stu-id="f213c-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="f213c-185">Wählen Sie in der Struktur 'Journal\Transaction\Credit'.</span><span class="sxs-lookup"><span data-stu-id="f213c-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="f213c-186">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-186">Click Bind.</span></span>
40. <span data-ttu-id="f213c-187">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f213c-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="f213c-188">Wählen Sie in der Struktur 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="f213c-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="f213c-189">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-189">Click Bind.</span></span>
43. <span data-ttu-id="f213c-190">In der Struktur ausgewählte 'LedgerJournal\Journal batch number(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="f213c-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="f213c-191">Wählen Sie in der Struktur 'Journal\Batch'.</span><span class="sxs-lookup"><span data-stu-id="f213c-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="f213c-192">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-192">Click Bind.</span></span>
46. <span data-ttu-id="f213c-193">Wählen Sie in der Struktur 'LedgerJournal' aus.</span><span class="sxs-lookup"><span data-stu-id="f213c-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="f213c-194">Wählen Sie in der Struktur 'Journal' aus.</span><span class="sxs-lookup"><span data-stu-id="f213c-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="f213c-195">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-195">Click Bind.</span></span>
49. <span data-ttu-id="f213c-196">Erweitern Sie in der Struktur 'Dimensions'.</span><span class="sxs-lookup"><span data-stu-id="f213c-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="f213c-197">In der Struktur erweitern Sie 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="f213c-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="f213c-198">In der Struktur erweitern Sie 'Dimensions\Main account and dimensions\Definition'.</span><span class="sxs-lookup"><span data-stu-id="f213c-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="f213c-199">In der Struktur wählen Sie 'Dimensions\Main account and dimensions\Name'.</span><span class="sxs-lookup"><span data-stu-id="f213c-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="f213c-200">Wählen Sie 'Dimensionseinstellung\Code' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f213c-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="f213c-201">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-201">Click Bind.</span></span>
55. <span data-ttu-id="f213c-202">In der Struktur wählen Sie 'Dimensions\Main account and dimensions\Definition\Report column name'.</span><span class="sxs-lookup"><span data-stu-id="f213c-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="f213c-203">Wählen Sie 'Dimensionseinstellung\Name' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f213c-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="f213c-204">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-204">Click Bind.</span></span>
58. <span data-ttu-id="f213c-205">In der Struktur wählen Sie 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="f213c-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="f213c-206">Wählen Sie 'Dimensions setting' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f213c-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="f213c-207">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f213c-207">Click Bind.</span></span>
61. <span data-ttu-id="f213c-208">Wählen Sie in der Struktur 'Company' aus.</span><span class="sxs-lookup"><span data-stu-id="f213c-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="f213c-209">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="f213c-209">Click Edit.</span></span>
63. <span data-ttu-id="f213c-210">Geben Sie im Feld "expressionAsStringText" 'Company.'find()'.'name()'' ein.</span><span class="sxs-lookup"><span data-stu-id="f213c-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="f213c-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="f213c-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="f213c-212">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f213c-212">Click Save.</span></span>
65. <span data-ttu-id="f213c-213">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f213c-213">Close the page.</span></span>
66. <span data-ttu-id="f213c-214">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f213c-214">Click Save.</span></span>
67. <span data-ttu-id="f213c-215">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f213c-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="f213c-216">Abschließen dieser Version dieses Entwurfsmodells</span><span class="sxs-lookup"><span data-stu-id="f213c-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="f213c-217">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f213c-217">Close the page.</span></span>
2. <span data-ttu-id="f213c-218">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f213c-218">Close the page.</span></span>
3. <span data-ttu-id="f213c-219">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="f213c-219">Click Change status.</span></span>
4. <span data-ttu-id="f213c-220">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="f213c-220">Click Complete.</span></span>
5. <span data-ttu-id="f213c-221">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f213c-221">Click OK.</span></span>


