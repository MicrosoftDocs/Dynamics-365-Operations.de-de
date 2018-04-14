---
title: "Neubewertung der Währung in einem Konsolidierungsunternehmen"
description: "In diesem Thema wird beschrieben, wie Währung in einem Konsolidierungsunternehmen neu bewertet werden."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2330939ddd7ccf4555cf1eff1e264c51f779c4eb
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="9a2a1-103">Neubewertung der Währung in einem Konsolidierungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="9a2a1-103">Currency revaluation in a consolidation company</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="9a2a1-104">Wenn Sie Daten aus einer Buchhaltungswährung zu anderen konsolidieren, müssen Sie die Neubewertung der Währung noch durchführen, wenn es eine Änderung in den Wechselkursen gibt, damit die Kontosalden ordnungsgemäß neu bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="9a2a1-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="9a2a1-105">Wenn Sie ursprünglich die Daten konsolidieren, verwenden Sie die **Währungsumrechnung**-Registerkarte, um die ursprünglichen Wechselkurse für die Übersetzung während des Konsolidierungsprozesses auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9a2a1-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="9a2a1-106">Nachdem ein neuer Wechselkurs eingegeben wurde (beispielsweise im nächsten Monat), müssen die Kontosalden neu bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="9a2a1-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="9a2a1-107">Die unrealisierten Gewinne oder Verluste werden dann entsprechend aktualisiert, basierend auf dem neuen Wechselkurs und -datum .</span><span class="sxs-lookup"><span data-stu-id="9a2a1-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="9a2a1-108">Das folgende Beispiel veranschaulicht die Buchhaltungseinträge, die beim Ausführen des Prozesses erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9a2a1-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="9a2a1-109">Unternehmenseinrichtung</span><span class="sxs-lookup"><span data-stu-id="9a2a1-109">Company setup</span></span>
-   <span data-ttu-id="9a2a1-110">**Quell-/Betreiberunternehmen (USMF)** – US-Dollar (USD) werden als Buchhaltungs- und Berichtswährung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a2a1-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="9a2a1-111">**Konsolidiertes Unternehmen (CON)** - Euro (EUR) werden als Buchhaltungs- und Berichtswährung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a2a1-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="9a2a1-112">**Realisierter Gewinn **– Sachkonto 801500</span><span class="sxs-lookup"><span data-stu-id="9a2a1-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="9a2a1-113">**Realisierter Verlust** – Sachkonto 801600</span><span class="sxs-lookup"><span data-stu-id="9a2a1-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="9a2a1-114">**Unrealisierter Gewinn** – Sachkonto 801600</span><span class="sxs-lookup"><span data-stu-id="9a2a1-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="9a2a1-115">**Unrealisierter Verlust** – Sachkonto 801400</span><span class="sxs-lookup"><span data-stu-id="9a2a1-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="9a2a1-116">Originalbuchungen</span><span class="sxs-lookup"><span data-stu-id="9a2a1-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="9a2a1-117">Barbelegbuchungen in USMF</span><span class="sxs-lookup"><span data-stu-id="9a2a1-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="9a2a1-118">Datum</span><span class="sxs-lookup"><span data-stu-id="9a2a1-118">Date</span></span>       | <span data-ttu-id="9a2a1-119">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="9a2a1-119">Ledger account</span></span>               | <span data-ttu-id="9a2a1-120">Währung</span><span class="sxs-lookup"><span data-stu-id="9a2a1-120">Currency</span></span> | <span data-ttu-id="9a2a1-121">Betrag</span><span class="sxs-lookup"><span data-stu-id="9a2a1-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="9a2a1-122">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="9a2a1-122">10/11/2015</span></span> | <span data-ttu-id="9a2a1-123">110110 – Bargeld</span><span class="sxs-lookup"><span data-stu-id="9a2a1-123">110110 – Cash</span></span>                | <span data-ttu-id="9a2a1-124">USD</span><span class="sxs-lookup"><span data-stu-id="9a2a1-124">USD</span></span>      | <span data-ttu-id="9a2a1-125">500</span><span class="sxs-lookup"><span data-stu-id="9a2a1-125">500</span></span>    |
| <span data-ttu-id="9a2a1-126">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="9a2a1-126">10/11/2015</span></span> | <span data-ttu-id="9a2a1-127">130100 – Debitoren</span><span class="sxs-lookup"><span data-stu-id="9a2a1-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="9a2a1-128">USD</span><span class="sxs-lookup"><span data-stu-id="9a2a1-128">USD</span></span>      | <span data-ttu-id="9a2a1-129">‑500</span><span class="sxs-lookup"><span data-stu-id="9a2a1-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="9a2a1-130">Wechselkurse</span><span class="sxs-lookup"><span data-stu-id="9a2a1-130">Exchange rates</span></span>

| <span data-ttu-id="9a2a1-131">Ausgangswährung</span><span class="sxs-lookup"><span data-stu-id="9a2a1-131">From currency</span></span> | <span data-ttu-id="9a2a1-132">Zielwährung</span><span class="sxs-lookup"><span data-stu-id="9a2a1-132">To currency</span></span> | <span data-ttu-id="9a2a1-133">Startdatum</span><span class="sxs-lookup"><span data-stu-id="9a2a1-133">Start date</span></span> | <span data-ttu-id="9a2a1-134">Kurs</span><span class="sxs-lookup"><span data-stu-id="9a2a1-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="9a2a1-135">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-135">EUR</span></span>           | <span data-ttu-id="9a2a1-136">USD</span><span class="sxs-lookup"><span data-stu-id="9a2a1-136">USD</span></span>         | <span data-ttu-id="9a2a1-137">01.10.2015</span><span class="sxs-lookup"><span data-stu-id="9a2a1-137">10/1/2015</span></span>  | <span data-ttu-id="9a2a1-138">200</span><span class="sxs-lookup"><span data-stu-id="9a2a1-138">200</span></span>           |
| <span data-ttu-id="9a2a1-139">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-139">EUR</span></span>           | <span data-ttu-id="9a2a1-140">USD</span><span class="sxs-lookup"><span data-stu-id="9a2a1-140">USD</span></span>         | <span data-ttu-id="9a2a1-141">01.11.2015</span><span class="sxs-lookup"><span data-stu-id="9a2a1-141">11/1/2015</span></span>  | <span data-ttu-id="9a2a1-142">150</span><span class="sxs-lookup"><span data-stu-id="9a2a1-142">150</span></span>           |
| <span data-ttu-id="9a2a1-143">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-143">EUR</span></span>           | <span data-ttu-id="9a2a1-144">USD</span><span class="sxs-lookup"><span data-stu-id="9a2a1-144">USD</span></span>         | <span data-ttu-id="9a2a1-145">01.12.2012</span><span class="sxs-lookup"><span data-stu-id="9a2a1-145">12/1/2012</span></span>  | <span data-ttu-id="9a2a1-146">100</span><span class="sxs-lookup"><span data-stu-id="9a2a1-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="9a2a1-147">Die Konsolidierung für Oktober 2015 ausführen</span><span class="sxs-lookup"><span data-stu-id="9a2a1-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="9a2a1-148">Salden im Konsolidierungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="9a2a1-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="9a2a1-149">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="9a2a1-149">Ledger account</span></span> | <span data-ttu-id="9a2a1-150">Währung</span><span class="sxs-lookup"><span data-stu-id="9a2a1-150">Currency</span></span> | <span data-ttu-id="9a2a1-151">Betrag</span><span class="sxs-lookup"><span data-stu-id="9a2a1-151">Amount</span></span> | <span data-ttu-id="9a2a1-152">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="9a2a1-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="9a2a1-153">110110</span><span class="sxs-lookup"><span data-stu-id="9a2a1-153">110110</span></span>         | <span data-ttu-id="9a2a1-154">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-154">EUR</span></span>      | <span data-ttu-id="9a2a1-155">250</span><span class="sxs-lookup"><span data-stu-id="9a2a1-155">250</span></span>    | <span data-ttu-id="9a2a1-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="9a2a1-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="9a2a1-157">130100</span><span class="sxs-lookup"><span data-stu-id="9a2a1-157">130100</span></span>         | <span data-ttu-id="9a2a1-158">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-158">EUR</span></span>      | <span data-ttu-id="9a2a1-159">‑250</span><span class="sxs-lookup"><span data-stu-id="9a2a1-159">-250</span></span>   | <span data-ttu-id="9a2a1-160">‑500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="9a2a1-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="9a2a1-161">Ausführen einer Neubewertung der Währung für die Konten ab dem 1. Oktober 2015 bis zum 30. November 2015</span><span class="sxs-lookup"><span data-stu-id="9a2a1-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="9a2a1-162">Salden im Konsolidierungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="9a2a1-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="9a2a1-163">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="9a2a1-163">Ledger account</span></span> | <span data-ttu-id="9a2a1-164">Währung</span><span class="sxs-lookup"><span data-stu-id="9a2a1-164">Currency</span></span> | <span data-ttu-id="9a2a1-165">Betrag</span><span class="sxs-lookup"><span data-stu-id="9a2a1-165">Amount</span></span>  | <span data-ttu-id="9a2a1-166">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="9a2a1-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="9a2a1-167">110110</span><span class="sxs-lookup"><span data-stu-id="9a2a1-167">110110</span></span>         | <span data-ttu-id="9a2a1-168">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-168">EUR</span></span>      | <span data-ttu-id="9a2a1-169">333,33</span><span class="sxs-lookup"><span data-stu-id="9a2a1-169">333.33</span></span>  | <span data-ttu-id="9a2a1-170">Ursprünglicher Betrag 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="9a2a1-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="9a2a1-171">130100</span><span class="sxs-lookup"><span data-stu-id="9a2a1-171">130100</span></span>         | <span data-ttu-id="9a2a1-172">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-172">EUR</span></span>      | <span data-ttu-id="9a2a1-173">‑333,33</span><span class="sxs-lookup"><span data-stu-id="9a2a1-173">-333.33</span></span> | <span data-ttu-id="9a2a1-174">Ursprünglicher Betrag -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="9a2a1-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="9a2a1-175">801400</span><span class="sxs-lookup"><span data-stu-id="9a2a1-175">801400</span></span>         | <span data-ttu-id="9a2a1-176">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-176">EUR</span></span>      | <span data-ttu-id="9a2a1-177">83,33</span><span class="sxs-lookup"><span data-stu-id="9a2a1-177">83.33</span></span>   | <span data-ttu-id="9a2a1-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="9a2a1-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="9a2a1-179">801600</span><span class="sxs-lookup"><span data-stu-id="9a2a1-179">801600</span></span>         | <span data-ttu-id="9a2a1-180">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-180">EUR</span></span>      | <span data-ttu-id="9a2a1-181">‑83,33</span><span class="sxs-lookup"><span data-stu-id="9a2a1-181">-83.33</span></span>  | <span data-ttu-id="9a2a1-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="9a2a1-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="9a2a1-183">Sie finden zusätzliche Buchungen für die Berichtswährungsbeträge.</span><span class="sxs-lookup"><span data-stu-id="9a2a1-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="9a2a1-184">Ausführen einer Neubewertung der Währung für die Konten ab dem 1. Oktober 2015 bis zum 31. Dezember 2015</span><span class="sxs-lookup"><span data-stu-id="9a2a1-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="9a2a1-185">Salden im Konsolidierungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="9a2a1-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="9a2a1-186">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="9a2a1-186">Ledger account</span></span> | <span data-ttu-id="9a2a1-187">Währung</span><span class="sxs-lookup"><span data-stu-id="9a2a1-187">Currency</span></span> | <span data-ttu-id="9a2a1-188">Betrag</span><span class="sxs-lookup"><span data-stu-id="9a2a1-188">Amount</span></span>  | <span data-ttu-id="9a2a1-189">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="9a2a1-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="9a2a1-190">110110</span><span class="sxs-lookup"><span data-stu-id="9a2a1-190">110110</span></span>         | <span data-ttu-id="9a2a1-191">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-191">EUR</span></span>      | <span data-ttu-id="9a2a1-192">500,00</span><span class="sxs-lookup"><span data-stu-id="9a2a1-192">500.00</span></span>  | <span data-ttu-id="9a2a1-193">Ursprünglicher Betrag 500 × 1</span><span class="sxs-lookup"><span data-stu-id="9a2a1-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="9a2a1-194">130100</span><span class="sxs-lookup"><span data-stu-id="9a2a1-194">130100</span></span>         | <span data-ttu-id="9a2a1-195">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-195">EUR</span></span>      | <span data-ttu-id="9a2a1-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="9a2a1-196">-500.00</span></span> | <span data-ttu-id="9a2a1-197">Ursprünglicher Betrag -500 × 1</span><span class="sxs-lookup"><span data-stu-id="9a2a1-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="9a2a1-198">801400</span><span class="sxs-lookup"><span data-stu-id="9a2a1-198">801400</span></span>         | <span data-ttu-id="9a2a1-199">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-199">EUR</span></span>      | <span data-ttu-id="9a2a1-200">250</span><span class="sxs-lookup"><span data-stu-id="9a2a1-200">250</span></span>     | <span data-ttu-id="9a2a1-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="9a2a1-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="9a2a1-202">801600</span><span class="sxs-lookup"><span data-stu-id="9a2a1-202">801600</span></span>         | <span data-ttu-id="9a2a1-203">EUR</span><span class="sxs-lookup"><span data-stu-id="9a2a1-203">EUR</span></span>      | <span data-ttu-id="9a2a1-204">‑250</span><span class="sxs-lookup"><span data-stu-id="9a2a1-204">-250</span></span>    | <span data-ttu-id="9a2a1-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="9a2a1-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






