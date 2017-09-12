---
title: "Neubewertung der Währung in einem Konsolidierungsunternehmen"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: de-de
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="78367-102">Neubewertung der Währung in einem Konsolidierungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="78367-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="78367-103">Wenn Sie Daten aus einer Buchhaltungswährung zu anderen konsolidieren, müssen Sie die Neubewertung der Währung noch durchführen, wenn es eine Änderung in den Wechselkursen gibt, damit die Kontosalden ordnungsgemäß neu bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="78367-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="78367-104">Wenn Sie ursprünglich die Daten konsolidieren, verwenden Sie die **Währungsumrechnung**-Registerkarte, um die ursprünglichen Wechselkurse für die Übersetzung während des Konsolidierungsprozesses auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="78367-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="78367-105">Nachdem ein neuer Wechselkurs eingegeben wurde (beispielsweise im nächsten Monat), müssen die Kontosalden neu bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="78367-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="78367-106">Die unrealisierten Gewinne oder Verluste werden dann entsprechend aktualisiert, basierend auf dem neuen Wechselkurs und -datum .</span><span class="sxs-lookup"><span data-stu-id="78367-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="78367-107">Das folgende Beispiel veranschaulicht die Buchhaltungseinträge, die beim Ausführen des Prozesses erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="78367-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="78367-108">Unternehmenseinrichtung</span><span class="sxs-lookup"><span data-stu-id="78367-108">Company setup</span></span>
-   <span data-ttu-id="78367-109">**Quell-/Betreiberunternehmen (USMF)** – US-Dollar (USD) werden als Buchhaltungs- und Berichtswährung verwendet.</span><span class="sxs-lookup"><span data-stu-id="78367-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="78367-110">**Konsolidiertes Unternehmen (CON)** - Euro (EUR) werden als Buchhaltungs- und Berichtswährung verwendet.</span><span class="sxs-lookup"><span data-stu-id="78367-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="78367-111">**Realisierter Gewinn **– Sachkonto 801500</span><span class="sxs-lookup"><span data-stu-id="78367-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="78367-112">**Realisierter Verlust** – Sachkonto 801600</span><span class="sxs-lookup"><span data-stu-id="78367-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="78367-113">**Unrealisierter Gewinn** – Sachkonto 801600</span><span class="sxs-lookup"><span data-stu-id="78367-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="78367-114">**Unrealisierter Verlust** – Sachkonto 801400</span><span class="sxs-lookup"><span data-stu-id="78367-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="78367-115">Originalbuchungen</span><span class="sxs-lookup"><span data-stu-id="78367-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="78367-116">Barbelegbuchungen in USMF</span><span class="sxs-lookup"><span data-stu-id="78367-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="78367-117">Datum</span><span class="sxs-lookup"><span data-stu-id="78367-117">Date</span></span>       | <span data-ttu-id="78367-118">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="78367-118">Ledger account</span></span>               | <span data-ttu-id="78367-119">Währung</span><span class="sxs-lookup"><span data-stu-id="78367-119">Currency</span></span> | <span data-ttu-id="78367-120">Betrag</span><span class="sxs-lookup"><span data-stu-id="78367-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="78367-121">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="78367-121">10/11/2015</span></span> | <span data-ttu-id="78367-122">110110 – Bargeld</span><span class="sxs-lookup"><span data-stu-id="78367-122">110110 – Cash</span></span>                | <span data-ttu-id="78367-123">USD</span><span class="sxs-lookup"><span data-stu-id="78367-123">USD</span></span>      | <span data-ttu-id="78367-124">500</span><span class="sxs-lookup"><span data-stu-id="78367-124">500</span></span>    |
| <span data-ttu-id="78367-125">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="78367-125">10/11/2015</span></span> | <span data-ttu-id="78367-126">130100 – Debitoren</span><span class="sxs-lookup"><span data-stu-id="78367-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="78367-127">USD</span><span class="sxs-lookup"><span data-stu-id="78367-127">USD</span></span>      | <span data-ttu-id="78367-128">‑500</span><span class="sxs-lookup"><span data-stu-id="78367-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="78367-129">Wechselkurse</span><span class="sxs-lookup"><span data-stu-id="78367-129">Exchange rates</span></span>
| <span data-ttu-id="78367-130">Ausgangswährung</span><span class="sxs-lookup"><span data-stu-id="78367-130">From currency</span></span> | <span data-ttu-id="78367-131">Zielwährung</span><span class="sxs-lookup"><span data-stu-id="78367-131">To currency</span></span> | <span data-ttu-id="78367-132">Startdatum</span><span class="sxs-lookup"><span data-stu-id="78367-132">Start date</span></span> | <span data-ttu-id="78367-133">Kurs</span><span class="sxs-lookup"><span data-stu-id="78367-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="78367-134">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-134">EUR</span></span>           | <span data-ttu-id="78367-135">USD</span><span class="sxs-lookup"><span data-stu-id="78367-135">USD</span></span>         | <span data-ttu-id="78367-136">01.10.2015</span><span class="sxs-lookup"><span data-stu-id="78367-136">10/1/2015</span></span>  | <span data-ttu-id="78367-137">200</span><span class="sxs-lookup"><span data-stu-id="78367-137">200</span></span>           |
| <span data-ttu-id="78367-138">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-138">EUR</span></span>           | <span data-ttu-id="78367-139">USD</span><span class="sxs-lookup"><span data-stu-id="78367-139">USD</span></span>         | <span data-ttu-id="78367-140">01.11.2015</span><span class="sxs-lookup"><span data-stu-id="78367-140">11/1/2015</span></span>  | <span data-ttu-id="78367-141">150</span><span class="sxs-lookup"><span data-stu-id="78367-141">150</span></span>           |
| <span data-ttu-id="78367-142">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-142">EUR</span></span>           | <span data-ttu-id="78367-143">USD</span><span class="sxs-lookup"><span data-stu-id="78367-143">USD</span></span>         | <span data-ttu-id="78367-144">01.12.2012</span><span class="sxs-lookup"><span data-stu-id="78367-144">12/1/2012</span></span>  | <span data-ttu-id="78367-145">100</span><span class="sxs-lookup"><span data-stu-id="78367-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="78367-146">Die Konsolidierung für Oktober 2015 ausführen</span><span class="sxs-lookup"><span data-stu-id="78367-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="78367-147">Salden im Konsolidierungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="78367-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="78367-148">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="78367-148">Ledger account</span></span> | <span data-ttu-id="78367-149">Währung</span><span class="sxs-lookup"><span data-stu-id="78367-149">Currency</span></span> | <span data-ttu-id="78367-150">Betrag</span><span class="sxs-lookup"><span data-stu-id="78367-150">Amount</span></span> | <span data-ttu-id="78367-151">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="78367-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="78367-152">110110</span><span class="sxs-lookup"><span data-stu-id="78367-152">110110</span></span>         | <span data-ttu-id="78367-153">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-153">EUR</span></span>      | <span data-ttu-id="78367-154">250</span><span class="sxs-lookup"><span data-stu-id="78367-154">250</span></span>    | <span data-ttu-id="78367-155">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="78367-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="78367-156">130100</span><span class="sxs-lookup"><span data-stu-id="78367-156">130100</span></span>         | <span data-ttu-id="78367-157">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-157">EUR</span></span>      | <span data-ttu-id="78367-158">‑250</span><span class="sxs-lookup"><span data-stu-id="78367-158">-250</span></span>   | <span data-ttu-id="78367-159">‑500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="78367-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="78367-160">Ausführen einer Neubewertung der Währung für die Konten ab dem 1. Oktober 2015 bis zum 30. November 2015</span><span class="sxs-lookup"><span data-stu-id="78367-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="78367-161">Salden im Konsolidierungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="78367-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="78367-162">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="78367-162">Ledger account</span></span> | <span data-ttu-id="78367-163">Währung</span><span class="sxs-lookup"><span data-stu-id="78367-163">Currency</span></span> | <span data-ttu-id="78367-164">Betrag</span><span class="sxs-lookup"><span data-stu-id="78367-164">Amount</span></span>  | <span data-ttu-id="78367-165">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="78367-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="78367-166">110110</span><span class="sxs-lookup"><span data-stu-id="78367-166">110110</span></span>         | <span data-ttu-id="78367-167">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-167">EUR</span></span>      | <span data-ttu-id="78367-168">333,33</span><span class="sxs-lookup"><span data-stu-id="78367-168">333.33</span></span>  | <span data-ttu-id="78367-169">Ursprünglicher Betrag 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="78367-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="78367-170">130100</span><span class="sxs-lookup"><span data-stu-id="78367-170">130100</span></span>         | <span data-ttu-id="78367-171">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-171">EUR</span></span>      | <span data-ttu-id="78367-172">‑333,33</span><span class="sxs-lookup"><span data-stu-id="78367-172">-333.33</span></span> | <span data-ttu-id="78367-173">Ursprünglicher Betrag -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="78367-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="78367-174">801400</span><span class="sxs-lookup"><span data-stu-id="78367-174">801400</span></span>         | <span data-ttu-id="78367-175">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-175">EUR</span></span>      | <span data-ttu-id="78367-176">83,33</span><span class="sxs-lookup"><span data-stu-id="78367-176">83.33</span></span>   | <span data-ttu-id="78367-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="78367-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="78367-178">801600</span><span class="sxs-lookup"><span data-stu-id="78367-178">801600</span></span>         | <span data-ttu-id="78367-179">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-179">EUR</span></span>      | <span data-ttu-id="78367-180">‑83,33</span><span class="sxs-lookup"><span data-stu-id="78367-180">-83.33</span></span>  | <span data-ttu-id="78367-181">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="78367-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="78367-182">Sie finden zusätzliche Buchungen für die Berichtswährungsbeträge.</span><span class="sxs-lookup"><span data-stu-id="78367-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="78367-183">Ausführen einer Neubewertung der Währung für die Konten ab dem 1. Oktober 2015 bis zum 31. Dezember 2015</span><span class="sxs-lookup"><span data-stu-id="78367-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="78367-184">Salden im Konsolidierungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="78367-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="78367-185">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="78367-185">Ledger account</span></span> | <span data-ttu-id="78367-186">Währung</span><span class="sxs-lookup"><span data-stu-id="78367-186">Currency</span></span> | <span data-ttu-id="78367-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="78367-187">Amount</span></span>  | <span data-ttu-id="78367-188">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="78367-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="78367-189">110110</span><span class="sxs-lookup"><span data-stu-id="78367-189">110110</span></span>         | <span data-ttu-id="78367-190">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-190">EUR</span></span>      | <span data-ttu-id="78367-191">500,00</span><span class="sxs-lookup"><span data-stu-id="78367-191">500.00</span></span>  | <span data-ttu-id="78367-192">Ursprünglicher Betrag 500 × 1</span><span class="sxs-lookup"><span data-stu-id="78367-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="78367-193">130100</span><span class="sxs-lookup"><span data-stu-id="78367-193">130100</span></span>         | <span data-ttu-id="78367-194">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-194">EUR</span></span>      | <span data-ttu-id="78367-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="78367-195">-500.00</span></span> | <span data-ttu-id="78367-196">Ursprünglicher Betrag -500 × 1</span><span class="sxs-lookup"><span data-stu-id="78367-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="78367-197">801400</span><span class="sxs-lookup"><span data-stu-id="78367-197">801400</span></span>         | <span data-ttu-id="78367-198">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-198">EUR</span></span>      | <span data-ttu-id="78367-199">250</span><span class="sxs-lookup"><span data-stu-id="78367-199">250</span></span>     | <span data-ttu-id="78367-200">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="78367-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="78367-201">801600</span><span class="sxs-lookup"><span data-stu-id="78367-201">801600</span></span>         | <span data-ttu-id="78367-202">EUR</span><span class="sxs-lookup"><span data-stu-id="78367-202">EUR</span></span>      | <span data-ttu-id="78367-203">‑250</span><span class="sxs-lookup"><span data-stu-id="78367-203">-250</span></span>    | <span data-ttu-id="78367-204">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="78367-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






