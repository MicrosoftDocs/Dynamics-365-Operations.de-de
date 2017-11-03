---
title: Buchung (Definitionen)
description: "Dieser Artikel enthält Beispiele, die zeigen, wie Bestellbelastungen für Budgetzuteilungen und Buchungsdefinitionen verwendet werden."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1bbd9230219f11407bc7afbd59670c6287b77c02
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="posting-definition-examples"></a><span data-ttu-id="6f304-103">Buchungsdefinitionsbeispiele</span><span class="sxs-lookup"><span data-stu-id="6f304-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6f304-104">Dieser Artikel enthält Beispiele, die zeigen, wie Bestellbelastungen für Budgetzuteilungen und Buchungsdefinitionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f304-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="6f304-105">Bevor Sie dieses Thema lesen, sollten Sie sich mit Buchungsdefinitionen und Transaktionsbuchungsdefinitionen vertraut gemacht haben.</span><span class="sxs-lookup"><span data-stu-id="6f304-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="6f304-106">Informationen zu den Buchungsebenen finden Sie unter [Buchungsdefinitionen](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="6f304-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="6f304-107">Die folgenden Beispiele können im Formular **Buchungsdefinitionen** eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6f304-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="6f304-108">Jedes Beispiel umfasst folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6f304-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="6f304-109">Buchungsdefinition – Übereinstimmungskriterien</span><span class="sxs-lookup"><span data-stu-id="6f304-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="6f304-110">Buchungsdefinition – Generierte Einträge</span><span class="sxs-lookup"><span data-stu-id="6f304-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="6f304-111">Buchungen mit Konten, Dimensionswerten und Beträgen</span><span class="sxs-lookup"><span data-stu-id="6f304-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="6f304-112">Aus der Buchungsdefinition generierte Sachkontoeinträge</span><span class="sxs-lookup"><span data-stu-id="6f304-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="6f304-113">Wenn die Konten und Dimensionswerte im Bereich **Übereinstimmungskriterien** für die Buchungsdefinition mit den Konten und Dimensionswerten der Buchung übereinstimmen, werden Sachkontoeinträge basierend auf dem Bereich **Generierte Einträge** für die Buchungsdefinition generiert.</span><span class="sxs-lookup"><span data-stu-id="6f304-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="6f304-114">Verwenden Sie die Seite **Transaktions-Buchungsdefinitionen**, um eine Buchungsdefinition einer bestimmten Buchungsart zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6f304-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="6f304-115">Nachdem Sie einer Buchungsart eine Buchungsdefinition zugeordnet und auf der Seite **Hauptbuch-Parameter** **Buchungsdefinitionen verwenden** ausgewählt haben, müssen für alle Buchungen der ausgewählten Buchungsart Buchungsdefinitionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f304-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="6f304-116">Beispiel: Bestellbelastungen</span><span class="sxs-lookup"><span data-stu-id="6f304-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="6f304-117">Wenn Sie die Belastungsverarbeitung aktivieren, indem Sie **Belastungsprozess aktivieren** auf der Seite **Hauptbuchparameter** auswählen, müssen Buchungsdefinitionen verwendet werden, um im Hauptbuch Belastungen für beliebige Konten zu erfassen, die reserviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f304-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="6f304-118">In den meisten Fällen werden alle Spesenkonten in der Bilanz reserviert.</span><span class="sxs-lookup"><span data-stu-id="6f304-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="6f304-119">Buchungsdefinitionen für Belastungen werden für das Modul **Einkauf** auf der Seite **Buchungsdefinitionen** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6f304-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="6f304-120">Im Bereich **Einkauf** der Seite **Transaktionsbuchungsdefinitionen** können Sie dann die Buchungsart **Bestellung** auswählen, um die Buchungsdefinition Bestellungen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6f304-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="6f304-121">Alle Belegbuchungen für Bestellbelastungen müssen in jeder eindeutigen Dimension auf einem Beleg ausgeglichen sein (Soll muss gleich Haben sein).</span><span class="sxs-lookup"><span data-stu-id="6f304-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="6f304-122">Buchungsdefinition – Übereinstimmungskriterien</span><span class="sxs-lookup"><span data-stu-id="6f304-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="6f304-123">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="6f304-123">Account structure</span></span>       | <span data-ttu-id="6f304-124">Kontonummer abgleichen</span><span class="sxs-lookup"><span data-stu-id="6f304-124">Match account number</span></span> | <span data-ttu-id="6f304-125">Priorität</span><span class="sxs-lookup"><span data-stu-id="6f304-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="6f304-126">Kontostruktur - GuV</span><span class="sxs-lookup"><span data-stu-id="6f304-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="6f304-127">1</span><span class="sxs-lookup"><span data-stu-id="6f304-127">1</span></span>        |

<span data-ttu-id="6f304-128">*Ein leerer Wert im Feld **Kontonummer abgleichen** bedeutet, dass alle übereinstimmenden Konten in der definierten Kontostruktur Teil der Übereinstimmungsregel sind.</span><span class="sxs-lookup"><span data-stu-id="6f304-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="6f304-129">Buchungsdefinition – Generierte Einträge</span><span class="sxs-lookup"><span data-stu-id="6f304-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="6f304-130">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="6f304-130">Account structure</span></span> | <span data-ttu-id="6f304-131">Generierte Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6f304-131">Generated account number</span></span>                    | <span data-ttu-id="6f304-132">Generierter Soll-/Habenbetrag</span><span class="sxs-lookup"><span data-stu-id="6f304-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="6f304-133">Gesamtbetrag</span><span class="sxs-lookup"><span data-stu-id="6f304-133">Balance</span></span>           | <span data-ttu-id="6f304-134">300143 - -(Belastungskonto)</span><span class="sxs-lookup"><span data-stu-id="6f304-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="6f304-135">Gleich</span><span class="sxs-lookup"><span data-stu-id="6f304-135">Same</span></span>                   |
| <span data-ttu-id="6f304-136">Gesamtbetrag</span><span class="sxs-lookup"><span data-stu-id="6f304-136">Balance</span></span>           | <span data-ttu-id="6f304-137">300144 - -(Reserve für Belastungskonto)</span><span class="sxs-lookup"><span data-stu-id="6f304-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="6f304-138">Ausbalancieren</span><span class="sxs-lookup"><span data-stu-id="6f304-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="6f304-139">Buchungen mit Konten, Dimensionswerten und Beträgen</span><span class="sxs-lookup"><span data-stu-id="6f304-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="6f304-140">Die Konten und Dimensionswerte stammen entweder aus den Buchhaltungsverteilungen, die Sie für eine Bestellposition eingeben, oder aus den Konten und Dimensionen, die automatisch basierend auf den Standardeinstellungen für Kreditoren, Artikel, Kategorien und Dimensionsvorlagen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="6f304-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="6f304-141">Konto + Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6f304-141">Account + dimensions</span></span>           | <span data-ttu-id="6f304-142">Soll</span><span class="sxs-lookup"><span data-stu-id="6f304-142">Debit</span></span>  | <span data-ttu-id="6f304-143">Entlastung</span><span class="sxs-lookup"><span data-stu-id="6f304-143">Credit</span></span> | <span data-ttu-id="6f304-144">Kommentar</span><span class="sxs-lookup"><span data-stu-id="6f304-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="6f304-145">606400-OU\_1-OU\_3566-Schulung</span><span class="sxs-lookup"><span data-stu-id="6f304-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="6f304-146">250,00</span><span class="sxs-lookup"><span data-stu-id="6f304-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="6f304-147">Aus der Buchungsdefinition generierte Sachkontoeinträge</span><span class="sxs-lookup"><span data-stu-id="6f304-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="6f304-148">Generierte Sachkontoeinträge werden erstellt, um die Belastungen zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6f304-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="6f304-149">Konto + Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6f304-149">Account + dimensions</span></span>           | <span data-ttu-id="6f304-150">Soll</span><span class="sxs-lookup"><span data-stu-id="6f304-150">Debit</span></span>  | <span data-ttu-id="6f304-151">Entlastung</span><span class="sxs-lookup"><span data-stu-id="6f304-151">Credit</span></span> | <span data-ttu-id="6f304-152">Kommentar</span><span class="sxs-lookup"><span data-stu-id="6f304-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="6f304-153">300143-OU\_1-OU\_3566-Schulung</span><span class="sxs-lookup"><span data-stu-id="6f304-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="6f304-154">250,00</span><span class="sxs-lookup"><span data-stu-id="6f304-154">250.00</span></span> |        |         |
| <span data-ttu-id="6f304-155">300144-OU\_1-OU\_3566-Schulung</span><span class="sxs-lookup"><span data-stu-id="6f304-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="6f304-156">250,00</span><span class="sxs-lookup"><span data-stu-id="6f304-156">250.00</span></span> |         |

<span data-ttu-id="6f304-157">In diesem Beispiel stimmt jedes Konto, das Teil der Kontostruktur - GuV ist, mit den Buchungsdefinitionskriterien überein.</span><span class="sxs-lookup"><span data-stu-id="6f304-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="6f304-158">Wenn daher 606500-OU\_1-OU\_3566-Schulung ausgewertet wird, werden für Konten, die im Bereich **Generierte Einträge** für die Buchungsdefinition definiert sind, Einträge generiert.</span><span class="sxs-lookup"><span data-stu-id="6f304-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="6f304-159">Beispiel: Budgetzuteilungen</span><span class="sxs-lookup"><span data-stu-id="6f304-159">Example: Budget appropriations</span></span>
<span data-ttu-id="6f304-160">Wenn Sie die Budgetzuteilung aktivieren, indem Sie **Budgetzuteilung aktivieren** auf der Seite **Hauptbuchparameter** auswählen, müssen Buchungsdefinitionen verwendet werden, um Budgetregistereinträge im Hauptbuch zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6f304-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="6f304-161">Wenn eine Budgetsteuerungskonfiguration aktiv und aktiviert ist, können Buchungsdefinitionen und Transaktionsbuchungsdefinitionen verwendet werden, um die Erfassung von Einträgen in Bezug auf Verteilung, Überarbeitung, Übertragung, Projekte, Anlagen und die Angebots- sowie Bedarfsplanung im Hauptbuch zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6f304-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="6f304-162">Eine Buchungsdefinition für Budgetregistereinträge mit dem Budgettyp **Ursprüngliches Budget**, für die Verteilungen aktiviert sind, kann mit dem Modul **Budget** auf der Seite **Buchungsdefinitionen** eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6f304-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="6f304-163">Sie können dann im Bereich **Budget** auf der Seite **Transaktionsbuchungsdefinitionen** Budgetcodes verwenden, um die Buchungsdefinition den Budgetregistereinträgen mit dem Budgettyp **Ursprüngliches Budget** zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6f304-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="6f304-164">Wenn Budgetzuteilungen und Buchungsdefinitionen aktiviert sind, werden die Budgetregistereinträge für die Budgetsteuerung und im Hauptbuch erfasst.</span><span class="sxs-lookup"><span data-stu-id="6f304-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="6f304-165">Buchungsdefinition – Übereinstimmungskriterien</span><span class="sxs-lookup"><span data-stu-id="6f304-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="6f304-166">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="6f304-166">Account structure</span></span>       | <span data-ttu-id="6f304-167">Kontonummer abgleichen</span><span class="sxs-lookup"><span data-stu-id="6f304-167">Match account number</span></span> | <span data-ttu-id="6f304-168">Priorität</span><span class="sxs-lookup"><span data-stu-id="6f304-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="6f304-169">Kontostruktur - GuV</span><span class="sxs-lookup"><span data-stu-id="6f304-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="6f304-170">1</span><span class="sxs-lookup"><span data-stu-id="6f304-170">1</span></span>        |

<span data-ttu-id="6f304-171">*Ein leerer Wert im Feld **Kontonummer abgleichen** bedeutet, dass alle übereinstimmenden Konten in der definierten Kontostruktur Teil der Übereinstimmungsregel sind.</span><span class="sxs-lookup"><span data-stu-id="6f304-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="6f304-172">Buchungsdefinition – Generierte Einträge</span><span class="sxs-lookup"><span data-stu-id="6f304-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="6f304-173">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="6f304-173">Account structure</span></span> | <span data-ttu-id="6f304-174">Generierte Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6f304-174">Generated account number</span></span>              | <span data-ttu-id="6f304-175">Generierter Soll-/Habenbetrag</span><span class="sxs-lookup"><span data-stu-id="6f304-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="6f304-176">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="6f304-176">Account structure</span></span> | <span data-ttu-id="6f304-177">300145 - -(Konto für vorkalkulierten Umsatzerlös)</span><span class="sxs-lookup"><span data-stu-id="6f304-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="6f304-178">Gleich</span><span class="sxs-lookup"><span data-stu-id="6f304-178">Same</span></span>                   |
| <span data-ttu-id="6f304-179">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="6f304-179">Account structure</span></span> | <span data-ttu-id="6f304-180">300146 - -(Zuteilungskonto)</span><span class="sxs-lookup"><span data-stu-id="6f304-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="6f304-181">Ausbalancieren</span><span class="sxs-lookup"><span data-stu-id="6f304-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="6f304-182">Buchungen mit Konten, Dimensionswerten und Beträgen</span><span class="sxs-lookup"><span data-stu-id="6f304-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="6f304-183">Sie geben Konten, Dimensionswerte und Beträge für den Budgetkontoeintrag auf der Seite **Budgetregistereintrag** ein.</span><span class="sxs-lookup"><span data-stu-id="6f304-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="6f304-184">Konto + Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6f304-184">Account + dimensions</span></span>           | <span data-ttu-id="6f304-185">Soll</span><span class="sxs-lookup"><span data-stu-id="6f304-185">Debit</span></span> | <span data-ttu-id="6f304-186">Entlastung</span><span class="sxs-lookup"><span data-stu-id="6f304-186">Credit</span></span> | <span data-ttu-id="6f304-187">Kommentar</span><span class="sxs-lookup"><span data-stu-id="6f304-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="6f304-188">606400-OU\_1-OU\_3566-Schulung</span><span class="sxs-lookup"><span data-stu-id="6f304-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="6f304-189">250,00</span><span class="sxs-lookup"><span data-stu-id="6f304-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="6f304-190">Aus der Buchungsdefinition generierte Sachkontoeinträge</span><span class="sxs-lookup"><span data-stu-id="6f304-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="6f304-191">Generierte Sachkontoeinträge werden erstellt, um das ursprüngliche Budget in jeder Dimension zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6f304-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="6f304-192">Konto + Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6f304-192">Account + dimensions</span></span>           | <span data-ttu-id="6f304-193">Soll</span><span class="sxs-lookup"><span data-stu-id="6f304-193">Debit</span></span>  | <span data-ttu-id="6f304-194">Entlastung</span><span class="sxs-lookup"><span data-stu-id="6f304-194">Credit</span></span> | <span data-ttu-id="6f304-195">Kommentar</span><span class="sxs-lookup"><span data-stu-id="6f304-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="6f304-196">300145-OU\_1-OU\_3566-Schulung</span><span class="sxs-lookup"><span data-stu-id="6f304-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="6f304-197">250,00</span><span class="sxs-lookup"><span data-stu-id="6f304-197">250.00</span></span> |         |
| <span data-ttu-id="6f304-198">300146-OU\_1-OU\_3566-Schulung</span><span class="sxs-lookup"><span data-stu-id="6f304-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="6f304-199">250,00</span><span class="sxs-lookup"><span data-stu-id="6f304-199">250.00</span></span> |        |         |

<span data-ttu-id="6f304-200">In diesem Beispiel stimmt jedes Konto, das Teil der Kontostruktur - GuV ist, mit den Buchungsdefinitionskriterien überein.</span><span class="sxs-lookup"><span data-stu-id="6f304-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="6f304-201">Daher werden die generierten Sachkontoeinträge beim Auswerten von 606400-OU\_1-OU\_3566-Schulung erstellt.</span><span class="sxs-lookup"><span data-stu-id="6f304-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






