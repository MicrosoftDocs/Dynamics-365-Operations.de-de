---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 2: Modellzuordnung)'
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eedb8321b43ab5f5d9cb56166b68d6e9508c104f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182461"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2-model-mapping"></a><span data-ttu-id="b5e15-103">ER - Verwendung von Finanzdimensionen als Datenquelle (Teil 2: Modellzuordnung)</span><span class="sxs-lookup"><span data-stu-id="b5e15-103">ER Use financial dimensions as a data source (Part 2: Model mapping)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5e15-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="b5e15-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="b5e15-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b5e15-106">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren "ER - Finanzdimensionen als Datenquelle nutzen (Teil 1: Design des Datenmodells)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5e15-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="b5e15-107">Hinzufügen von erforderlichen Datenquellen zur Modellzuordnung</span><span class="sxs-lookup"><span data-stu-id="b5e15-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="b5e15-108">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b5e15-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b5e15-109">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="b5e15-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b5e15-110">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="b5e15-110">Click Designer.</span></span>
4. <span data-ttu-id="b5e15-111">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="b5e15-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="b5e15-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b5e15-112">Click New.</span></span>
6. <span data-ttu-id="b5e15-113">Wählen Sie im Feld "Definition" "Erfassung" aus.</span><span class="sxs-lookup"><span data-stu-id="b5e15-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="b5e15-114">Geben Sie im Feld "Name" "Dimensionsdatenzuordnung" ein.</span><span class="sxs-lookup"><span data-stu-id="b5e15-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="b5e15-115">Geben Sie im Feld "Beschreibung" "Dimensionsdatenzuordnung" ein.</span><span class="sxs-lookup"><span data-stu-id="b5e15-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="b5e15-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b5e15-116">Click Save.</span></span>
10. <span data-ttu-id="b5e15-117">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="b5e15-117">Click Designer.</span></span>
11. <span data-ttu-id="b5e15-118">Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabelle' aus.</span><span class="sxs-lookup"><span data-stu-id="b5e15-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="b5e15-119">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b5e15-119">Click Add root.</span></span>
13. <span data-ttu-id="b5e15-120">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="b5e15-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="b5e15-121">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="b5e15-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="b5e15-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b5e15-122">Click OK.</span></span>
16. <span data-ttu-id="b5e15-123">Wählen Sie in der Struktur "Funktionen\Finanzdimensionsdetails".</span><span class="sxs-lookup"><span data-stu-id="b5e15-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="b5e15-124">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b5e15-124">Click Add root.</span></span>
    * <span data-ttu-id="b5e15-125">Diese Datenquelle gibt an, wie der Bereich der Finanzdimensionen für einen Bericht definiert wird, der dieses Modell als Datenquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5e15-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="b5e15-126">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b5e15-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="b5e15-127">Wählen Sie "Ja" im Feld "Dimensionen anfordern".</span><span class="sxs-lookup"><span data-stu-id="b5e15-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="b5e15-128">Wählen Sie die Option Ja aus, um dem Benutzer die Auswahl zur Laufzeit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b5e15-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="b5e15-129">Bei "Neun" werden standardmäßig alle Finanzdimensionen der aktuellen Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5e15-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="b5e15-130">Wählen Sie im Feld Finanzdimensionen "Juristische Person" aus.</span><span class="sxs-lookup"><span data-stu-id="b5e15-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="b5e15-131">Wählen Sie "Alle" aus, um dem Benutzer die Auswahl der gewünschten Dimensionen für die aktuelle Instanz zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b5e15-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="b5e15-132">Wählen Sie "Juristische Person" aus, um dem Benutzer die Auswahl der Dimensionen für das Unternehmen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b5e15-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="b5e15-133">Wählen Sie "Dimension" aus, um dem Benutzer die Auswahl von Dimensionen über einen einzelnen Dimensionssatzes zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b5e15-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="b5e15-134">Wählen Sie "Ja" im Feld "Hauptkonto anfordern".</span><span class="sxs-lookup"><span data-stu-id="b5e15-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="b5e15-135">Legen Sie "Hauptkonto anfordern" auf "Ja" fest, um Benutzern zu ermöglichen, das Hauptkonto als Teil der Liste mit den Dimensionen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b5e15-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="b5e15-136">Bei "Nein" wird das Hauptkonto nicht in der Liste mit den Dimensionen aufgenommen und die Option "Hauptkonto erforderlich" ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b5e15-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="b5e15-137">Wenn "Hauptkonto erforderlich" auf Ja festgelegt ist, wird das Hauptkonto unabhängig von der Auswahl des Benutzers in der Liste mit den Dimensionen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b5e15-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="b5e15-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b5e15-138">Click OK.</span></span>
23. <span data-ttu-id="b5e15-139">Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabellendatensätze' aus.</span><span class="sxs-lookup"><span data-stu-id="b5e15-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="b5e15-140">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b5e15-140">Click Add root.</span></span>
25. <span data-ttu-id="b5e15-141">Geben Sie im Feld "Name" "LedgerJournal" ein.</span><span class="sxs-lookup"><span data-stu-id="b5e15-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="b5e15-142">Wählen Sie "Ja" im Feld "Ask for query".</span><span class="sxs-lookup"><span data-stu-id="b5e15-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="b5e15-143">Im Tabellenfeld geben Sie "LedgerJournalTable" ein.</span><span class="sxs-lookup"><span data-stu-id="b5e15-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="b5e15-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b5e15-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="b5e15-145">Zuordnen von Datenmodell-Elementen zu hinzugefügten Datenquellen</span><span class="sxs-lookup"><span data-stu-id="b5e15-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="b5e15-146">Erweitern Sie in der Struktur 'Erfassung'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="b5e15-147">Erweitern Sie in der Struktur 'Erfassung\Buchung'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="b5e15-148">Erweitern Sie in der Struktur 'Erfassung\Buchung\Dimensionsdaten'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="b5e15-149">Erweitern Sie 'Dimensionseinstellung' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5e15-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="b5e15-150">Erweitern Sie in der Struktur "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="b5e15-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="b5e15-151">Erweitern Sie 'LedgerJournal\\<Relations' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5e15-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="b5e15-152">Erweitern Sie 'LedgerJournal\<Relations\LedgerJournalTrans' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5e15-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="b5e15-153">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5e15-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="b5e15-154">Wählen Sie in der Struktur 'Erfassung\Buchung\Beleg'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="b5e15-155">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-155">Click Bind.</span></span>
11. <span data-ttu-id="b5e15-156">Wählen Sie in der Strukturdarstellung 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="b5e15-157">Beachten Sie, dass für jede Referenz zu Finanzdimensionen, die beispielsweise auf LedgerDimension festgelegt ist, ein entsprechender Datenquellenartikel verfügbar ist (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="b5e15-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="b5e15-158">Dieser Datenquellenartikel bietet die Finanzdimensionen des Dimensionssatzes als Liste des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="b5e15-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="b5e15-159">Erweitern Sie in der Strukturdarstellung 'LedgerJournal\\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="b5e15-160">Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="b5e15-161">Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="b5e15-162">Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Definitionen'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="b5e15-163">Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Definitionen\Name'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="b5e15-164">Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Name'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="b5e15-165">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-165">Click Bind.</span></span>
19. <span data-ttu-id="b5e15-166">Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="b5e15-167">Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Description'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="b5e15-168">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-168">Click Bind.</span></span>
22. <span data-ttu-id="b5e15-169">Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="b5e15-170">Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Code'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="b5e15-171">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-171">Click Bind.</span></span>
25. <span data-ttu-id="b5e15-172">Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="b5e15-173">Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="b5e15-174">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-174">Click Bind.</span></span>
28. <span data-ttu-id="b5e15-175">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="b5e15-176">Wählen Sie in der Struktur 'Erfassung\Buchung\Debit'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="b5e15-177">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-177">Click Bind.</span></span>
31. <span data-ttu-id="b5e15-178">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="b5e15-179">Wählen Sie in der Struktur 'Erfassung\Buchung\Date'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="b5e15-180">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-180">Click Bind.</span></span>
34. <span data-ttu-id="b5e15-181">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="b5e15-182">Wählen Sie in der Struktur 'Journal\Transaction\Currency'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="b5e15-183">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-183">Click Bind.</span></span>
37. <span data-ttu-id="b5e15-184">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="b5e15-185">Wählen Sie in der Struktur 'Journal\Transaction\Credit'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="b5e15-186">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-186">Click Bind.</span></span>
40. <span data-ttu-id="b5e15-187">Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5e15-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="b5e15-188">Wählen Sie in der Struktur 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="b5e15-189">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-189">Click Bind.</span></span>
43. <span data-ttu-id="b5e15-190">In der Struktur ausgewählte 'LedgerJournal\Journal batch number(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="b5e15-191">Wählen Sie in der Struktur 'Journal\Batch'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="b5e15-192">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-192">Click Bind.</span></span>
46. <span data-ttu-id="b5e15-193">Wählen Sie in der Struktur 'LedgerJournal' aus.</span><span class="sxs-lookup"><span data-stu-id="b5e15-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="b5e15-194">Wählen Sie in der Struktur 'Journal' aus.</span><span class="sxs-lookup"><span data-stu-id="b5e15-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="b5e15-195">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-195">Click Bind.</span></span>
49. <span data-ttu-id="b5e15-196">Erweitern Sie in der Struktur 'Dimensions'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="b5e15-197">In der Struktur erweitern Sie 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="b5e15-198">In der Struktur erweitern Sie 'Dimensions\Main account and dimensions\Definition'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="b5e15-199">In der Struktur wählen Sie 'Dimensions\Main account and dimensions\Name'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="b5e15-200">Wählen Sie 'Dimensionseinstellung\Code' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5e15-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="b5e15-201">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-201">Click Bind.</span></span>
55. <span data-ttu-id="b5e15-202">In der Struktur wählen Sie 'Dimensions\Main account and dimensions\Definition\Report column name'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="b5e15-203">Wählen Sie 'Dimensionseinstellung\Name' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5e15-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="b5e15-204">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-204">Click Bind.</span></span>
58. <span data-ttu-id="b5e15-205">In der Struktur wählen Sie 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="b5e15-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="b5e15-206">Wählen Sie 'Dimensions setting' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5e15-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="b5e15-207">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b5e15-207">Click Bind.</span></span>
61. <span data-ttu-id="b5e15-208">Wählen Sie in der Struktur 'Company' aus.</span><span class="sxs-lookup"><span data-stu-id="b5e15-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="b5e15-209">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="b5e15-209">Click Edit.</span></span>
63. <span data-ttu-id="b5e15-210">Geben Sie im Feld "expressionAsStringText" 'Company.'find()'.'name()'' ein.</span><span class="sxs-lookup"><span data-stu-id="b5e15-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="b5e15-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="b5e15-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="b5e15-212">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b5e15-212">Click Save.</span></span>
65. <span data-ttu-id="b5e15-213">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b5e15-213">Close the page.</span></span>
66. <span data-ttu-id="b5e15-214">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b5e15-214">Click Save.</span></span>
67. <span data-ttu-id="b5e15-215">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b5e15-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="b5e15-216">Abschließen dieser Version dieses Entwurfsmodells</span><span class="sxs-lookup"><span data-stu-id="b5e15-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="b5e15-217">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b5e15-217">Close the page.</span></span>
2. <span data-ttu-id="b5e15-218">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b5e15-218">Close the page.</span></span>
3. <span data-ttu-id="b5e15-219">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="b5e15-219">Click Change status.</span></span>
4. <span data-ttu-id="b5e15-220">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="b5e15-220">Click Complete.</span></span>
5. <span data-ttu-id="b5e15-221">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b5e15-221">Click OK.</span></span>

