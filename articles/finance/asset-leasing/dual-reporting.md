---
title: Dioppelte Berichterstellung
description: Dieses Thema führt Sie durch ein Beispiel, das zeigt, wie Sie die Anforderungen sowohl für die Berichterstattung nach dem International Financial Reporting Standard (IFRS) als auch für die gesetzliche Berichterstattung im Analgenleasing erfüllen können.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c9f2bae330e688e1e941277d46ddcbd38916f8c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815979"
---
# <a name="dual-reporting"></a><span data-ttu-id="016bc-103">Dioppelte Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="016bc-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="016bc-104">Dieses Thema führt Sie durch ein Beispiel, das zeigt, wie Sie die Anforderungen sowohl für die Berichterstattung nach dem International Financial Reporting Standard (IFRS) als auch für die gesetzliche Berichterstattung im Analgenleasing erfüllen können.</span><span class="sxs-lookup"><span data-stu-id="016bc-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="016bc-105">Sie müssen mit Buchungsbenenen in Microsoft Dynamics 365 Finance vertraut sein. Dies erleichtert das Verständnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="016bc-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="016bc-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="016bc-106">Example</span></span>

<span data-ttu-id="016bc-107">Das folgende Beispiel berücksichtigt einen Mietvertrag nach italienischer gesetzlicher Berichterstattung, wobei sowohl die Cash-Basis-Methode als auch die IFRS-Berichtsmethode angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="016bc-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="016bc-108">Das Unternehmen muss drei Bücher erstellen, um sowohl die italienischen gesetzlichen Anforderungen als auch die Anforderungen von IFRS 16 zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="016bc-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="016bc-109">Für IFRS 16 ist ein Buch erforderlich, für die gesetzlichen Anforderungen ein Buch und für die automatische Stornierung gesetzlicher Buchungen ein Buch.</span><span class="sxs-lookup"><span data-stu-id="016bc-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="016bc-110">Die Bücher sind wie in den folgenden Tabellen gezeigt aufgebaut.</span><span class="sxs-lookup"><span data-stu-id="016bc-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="016bc-111">**IFRS 16-Buch**</span><span class="sxs-lookup"><span data-stu-id="016bc-111">**IFRS 16 book**</span></span>

<span data-ttu-id="016bc-112">Das IFRS 16-Buch ist so angelegt, dass es dem Rechnungslegungsstandard IFRS 16 entspricht.</span><span class="sxs-lookup"><span data-stu-id="016bc-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="016bc-113">Alle Einträge, die in diesem Buch gebucht werden, werden auf einer benutzerdefinierten Ebene gebucht.</span><span class="sxs-lookup"><span data-stu-id="016bc-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="016bc-114">Name</span><span class="sxs-lookup"><span data-stu-id="016bc-114">Name</span></span>                                    | <span data-ttu-id="016bc-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="016bc-116">Buchtyp</span><span class="sxs-lookup"><span data-stu-id="016bc-116">Book type</span></span>                               | <span data-ttu-id="016bc-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="016bc-117">IFRS 16</span></span>        |
| <span data-ttu-id="016bc-118">Buchbeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-118">Book description</span></span>                        | <span data-ttu-id="016bc-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="016bc-119">IFRS 16</span></span>        |
| <span data-ttu-id="016bc-120">Buchungsebene</span><span class="sxs-lookup"><span data-stu-id="016bc-120">Posting Layer</span></span>                           | <span data-ttu-id="016bc-121">Benutzerdefinierte Ebene 1</span><span class="sxs-lookup"><span data-stu-id="016bc-121">Custom layer 1</span></span> |
| <span data-ttu-id="016bc-122">Mietvertragstyp</span><span class="sxs-lookup"><span data-stu-id="016bc-122">Lease Type</span></span>                              | <span data-ttu-id="016bc-123">Finance</span><span class="sxs-lookup"><span data-stu-id="016bc-123">Finance</span></span>        |
| <span data-ttu-id="016bc-124">Buchhaltungsframework</span><span class="sxs-lookup"><span data-stu-id="016bc-124">Accounting Framework</span></span>                    | <span data-ttu-id="016bc-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="016bc-125">IFRS 16</span></span>        |
| <span data-ttu-id="016bc-126">Einrichtung von Mietdauer/Nutzungsdauer</span><span class="sxs-lookup"><span data-stu-id="016bc-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="016bc-127">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-127">0.00</span></span>           |
| <span data-ttu-id="016bc-128">Einrichtung von Barwert/Anlagenzeitwert</span><span class="sxs-lookup"><span data-stu-id="016bc-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="016bc-129">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-129">0.00</span></span>           |
| <span data-ttu-id="016bc-130">Kurzfristiger Schwellenwert</span><span class="sxs-lookup"><span data-stu-id="016bc-130">Short-term threshold</span></span>                    | <span data-ttu-id="016bc-131">12</span><span class="sxs-lookup"><span data-stu-id="016bc-131">12</span></span>             |
| <span data-ttu-id="016bc-132">Schwellenwert für geringen Wert</span><span class="sxs-lookup"><span data-stu-id="016bc-132">Low Value Threshold</span></span>                     | <span data-ttu-id="016bc-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-133">5,000.00</span></span>       |
| <span data-ttu-id="016bc-134">An Kreditor bezahlen</span><span class="sxs-lookup"><span data-stu-id="016bc-134">Pay to Vendor</span></span>                           | <span data-ttu-id="016bc-135">Nr.</span><span class="sxs-lookup"><span data-stu-id="016bc-135">No</span></span>             |

<span data-ttu-id="016bc-136">**Gesetzliches Buch**</span><span class="sxs-lookup"><span data-stu-id="016bc-136">**Statutory book**</span></span>

<span data-ttu-id="016bc-137">Das gesetzliche Buch ist ein Cash-Basis-Buch, in dem das Unternehmen die Mietkosten als den Betrag an Bargeld verbucht, der jeden Monat für die Miete gezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="016bc-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="016bc-138">Dieses Buch enthält keine Nutzungsrechte (ROU) für Vermögenswerte oder Mietverbindlichkeiten.</span><span class="sxs-lookup"><span data-stu-id="016bc-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="016bc-139">Name</span><span class="sxs-lookup"><span data-stu-id="016bc-139">Name</span></span>                                    | <span data-ttu-id="016bc-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="016bc-141">Buchtyp</span><span class="sxs-lookup"><span data-stu-id="016bc-141">Book type</span></span>                               | <span data-ttu-id="016bc-142">Gesetzlich</span><span class="sxs-lookup"><span data-stu-id="016bc-142">Statutory</span></span>   |
| <span data-ttu-id="016bc-143">Buchbeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-143">Book description</span></span>                        | <span data-ttu-id="016bc-144">Lokale GAAP</span><span class="sxs-lookup"><span data-stu-id="016bc-144">Local GAAP</span></span>  |
| <span data-ttu-id="016bc-145">Buchungsebene</span><span class="sxs-lookup"><span data-stu-id="016bc-145">Posting Layer</span></span>                           | <span data-ttu-id="016bc-146">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-146">Current</span></span>     |
| <span data-ttu-id="016bc-147">Mietvertragstyp</span><span class="sxs-lookup"><span data-stu-id="016bc-147">Lease Type</span></span>                              | <span data-ttu-id="016bc-148">Automatisch</span><span class="sxs-lookup"><span data-stu-id="016bc-148">Automatic</span></span>   |
| <span data-ttu-id="016bc-149">Buchhaltungsframework</span><span class="sxs-lookup"><span data-stu-id="016bc-149">Accounting Framework</span></span>                    | <span data-ttu-id="016bc-150">Einnahmen/Ausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-150">Cash basis</span></span>  |
| <span data-ttu-id="016bc-151">Einrichtung von Mietdauer/Nutzungsdauer</span><span class="sxs-lookup"><span data-stu-id="016bc-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="016bc-152">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-152">0.00</span></span>        |
| <span data-ttu-id="016bc-153">Einrichtung von Barwert/Anlagenzeitwert</span><span class="sxs-lookup"><span data-stu-id="016bc-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="016bc-154">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-154">0.00</span></span>        |
| <span data-ttu-id="016bc-155">Kurzfristiger Schwellenwert</span><span class="sxs-lookup"><span data-stu-id="016bc-155">Short-term threshold</span></span>                    | <span data-ttu-id="016bc-156">0</span><span class="sxs-lookup"><span data-stu-id="016bc-156">0</span></span>           |
| <span data-ttu-id="016bc-157">Schwellenwert für geringen Wert</span><span class="sxs-lookup"><span data-stu-id="016bc-157">Low Value Threshold</span></span>                     | <span data-ttu-id="016bc-158">0</span><span class="sxs-lookup"><span data-stu-id="016bc-158">0</span></span>           |
| <span data-ttu-id="016bc-159">An Kreditor bezahlen</span><span class="sxs-lookup"><span data-stu-id="016bc-159">Pay to Vendor</span></span>                           | <span data-ttu-id="016bc-160">Nr.</span><span class="sxs-lookup"><span data-stu-id="016bc-160">No</span></span>          |

<span data-ttu-id="016bc-161">**Gesetzliches Stornobuch**</span><span class="sxs-lookup"><span data-stu-id="016bc-161">**Statutory reversal book**</span></span>

<span data-ttu-id="016bc-162">Das gesetzliche Stornobuch ist wie das gesetzliche Buch aufgebaut.</span><span class="sxs-lookup"><span data-stu-id="016bc-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="016bc-163">Name</span><span class="sxs-lookup"><span data-stu-id="016bc-163">Name</span></span>                                    | <span data-ttu-id="016bc-164">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="016bc-165">Buchtyp</span><span class="sxs-lookup"><span data-stu-id="016bc-165">Book type</span></span>                               | <span data-ttu-id="016bc-166">Gesetzliches Buch – Stornobuchungen</span><span class="sxs-lookup"><span data-stu-id="016bc-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="016bc-167">Buchbeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-167">Book description</span></span>                        | <span data-ttu-id="016bc-168">Buch für die Rückbuchung des gesetzlichen Buchs</span><span class="sxs-lookup"><span data-stu-id="016bc-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="016bc-169">Buchungsebene</span><span class="sxs-lookup"><span data-stu-id="016bc-169">Posting Layer</span></span>                           | <span data-ttu-id="016bc-170">Benutzerdefinierte Ebene 1</span><span class="sxs-lookup"><span data-stu-id="016bc-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="016bc-171">Mietvertragstyp</span><span class="sxs-lookup"><span data-stu-id="016bc-171">Lease Type</span></span>                              | <span data-ttu-id="016bc-172">Automatisch</span><span class="sxs-lookup"><span data-stu-id="016bc-172">Automatic</span></span>                      |
| <span data-ttu-id="016bc-173">Buchhaltungsframework</span><span class="sxs-lookup"><span data-stu-id="016bc-173">Accounting Framework</span></span>                    | <span data-ttu-id="016bc-174">Einnahmen/Ausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-174">Cash basis</span></span>                     |
| <span data-ttu-id="016bc-175">Einrichtung von Mietdauer/Nutzungsdauer</span><span class="sxs-lookup"><span data-stu-id="016bc-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="016bc-176">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-176">0.00</span></span>                           |
| <span data-ttu-id="016bc-177">Einrichtung von Barwert/Anlagenzeitwert</span><span class="sxs-lookup"><span data-stu-id="016bc-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="016bc-178">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-178">0.00</span></span>                           |
| <span data-ttu-id="016bc-179">Kurzfristiger Schwellenwert</span><span class="sxs-lookup"><span data-stu-id="016bc-179">Short-term threshold</span></span>                    | <span data-ttu-id="016bc-180">0</span><span class="sxs-lookup"><span data-stu-id="016bc-180">0</span></span>                              |
| <span data-ttu-id="016bc-181">Schwellenwert für geringen Wert</span><span class="sxs-lookup"><span data-stu-id="016bc-181">Low Value Threshold</span></span>                     | <span data-ttu-id="016bc-182">0</span><span class="sxs-lookup"><span data-stu-id="016bc-182">0</span></span>                              |
| <span data-ttu-id="016bc-183">An Kreditor bezahlen</span><span class="sxs-lookup"><span data-stu-id="016bc-183">Pay to Vendor</span></span>                           | <span data-ttu-id="016bc-184">Nr.</span><span class="sxs-lookup"><span data-stu-id="016bc-184">No</span></span>                             |

<span data-ttu-id="016bc-185">In diesem Beispiel wurde ein Mietvertrag mit den folgenden Einstellungen auf den Registerkarten **Allgemein** und **Zahlungspläne** erstellt.</span><span class="sxs-lookup"><span data-stu-id="016bc-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="016bc-186">**Registerkarte „Allgemeines“**</span><span class="sxs-lookup"><span data-stu-id="016bc-186">**General tab**</span></span>

| <span data-ttu-id="016bc-187">Feld</span><span class="sxs-lookup"><span data-stu-id="016bc-187">Field</span></span>                      | <span data-ttu-id="016bc-188">Wert</span><span class="sxs-lookup"><span data-stu-id="016bc-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="016bc-189">Zinssatz für Neukredit</span><span class="sxs-lookup"><span data-stu-id="016bc-189">Incremental borrowing rate</span></span> | <span data-ttu-id="016bc-190">5 %</span><span class="sxs-lookup"><span data-stu-id="016bc-190">5%</span></span>               |
| <span data-ttu-id="016bc-191">Anfangsdatum</span><span class="sxs-lookup"><span data-stu-id="016bc-191">Commencement date</span></span>          | <span data-ttu-id="016bc-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="016bc-192">1/1/2020</span></span>         |
| <span data-ttu-id="016bc-193">Mietvertragsgruppe</span><span class="sxs-lookup"><span data-stu-id="016bc-193">Lease group</span></span>                | <span data-ttu-id="016bc-194">Gebäude</span><span class="sxs-lookup"><span data-stu-id="016bc-194">Buildings</span></span>        |
| <span data-ttu-id="016bc-195">Lieferant</span><span class="sxs-lookup"><span data-stu-id="016bc-195">Vendor</span></span>                     | <span data-ttu-id="016bc-196">1001</span><span class="sxs-lookup"><span data-stu-id="016bc-196">1001</span></span>             |
| <span data-ttu-id="016bc-197">Zeitwert der Anlage</span><span class="sxs-lookup"><span data-stu-id="016bc-197">Fair value of the asset</span></span>    | <span data-ttu-id="016bc-198">245,000</span><span class="sxs-lookup"><span data-stu-id="016bc-198">245,000</span></span>          |
| <span data-ttu-id="016bc-199">Nutzungsdauer für Anlagen</span><span class="sxs-lookup"><span data-stu-id="016bc-199">Asset useful life</span></span>          | <span data-ttu-id="016bc-200">120</span><span class="sxs-lookup"><span data-stu-id="016bc-200">120</span></span>              |
| <span data-ttu-id="016bc-201">Annuitätstyp</span><span class="sxs-lookup"><span data-stu-id="016bc-201">Annuity type</span></span>               | <span data-ttu-id="016bc-202">Normale Annuität</span><span class="sxs-lookup"><span data-stu-id="016bc-202">Ordinary annuity</span></span> |
| <span data-ttu-id="016bc-203">Aufzinsungsintervall</span><span class="sxs-lookup"><span data-stu-id="016bc-203">Compounding interval</span></span>       | <span data-ttu-id="016bc-204">Monatlich</span><span class="sxs-lookup"><span data-stu-id="016bc-204">Monthly</span></span>          |

<span data-ttu-id="016bc-205">**Registerkarte „Zahlungsplanpositionen“**</span><span class="sxs-lookup"><span data-stu-id="016bc-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="016bc-206">Feld</span><span class="sxs-lookup"><span data-stu-id="016bc-206">Field</span></span>             | <span data-ttu-id="016bc-207">Wert</span><span class="sxs-lookup"><span data-stu-id="016bc-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="016bc-208">Startdatum</span><span class="sxs-lookup"><span data-stu-id="016bc-208">Start date</span></span>        | <span data-ttu-id="016bc-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="016bc-209">1/1/2020</span></span>   |
| <span data-ttu-id="016bc-210">Periodenintervall</span><span class="sxs-lookup"><span data-stu-id="016bc-210">Period interval</span></span>   | <span data-ttu-id="016bc-211">Monate</span><span class="sxs-lookup"><span data-stu-id="016bc-211">Months</span></span>     |
| <span data-ttu-id="016bc-212">Perioden</span><span class="sxs-lookup"><span data-stu-id="016bc-212">Periods</span></span>           | <span data-ttu-id="016bc-213">24</span><span class="sxs-lookup"><span data-stu-id="016bc-213">24</span></span>         |
| <span data-ttu-id="016bc-214">Enddatum</span><span class="sxs-lookup"><span data-stu-id="016bc-214">End date</span></span>          | <span data-ttu-id="016bc-215">31/12/2020</span><span class="sxs-lookup"><span data-stu-id="016bc-215">12/31/2020</span></span> |
| <span data-ttu-id="016bc-216">Zahlungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="016bc-216">Payment frequency</span></span> | <span data-ttu-id="016bc-217">Monatlich</span><span class="sxs-lookup"><span data-stu-id="016bc-217">Monthly</span></span>    |
| <span data-ttu-id="016bc-218">Zahlungsbetrag</span><span class="sxs-lookup"><span data-stu-id="016bc-218">Payment amount</span></span>    | <span data-ttu-id="016bc-219">1.000</span><span class="sxs-lookup"><span data-stu-id="016bc-219">1,000</span></span>      |

<span data-ttu-id="016bc-220">Um diesen Mietvertrag in zwei Frameworks zu berücksichtigen, verwenden Sie eine aktuelle Buchungsebene und eine benutzerdefinierte Buchungsebene.</span><span class="sxs-lookup"><span data-stu-id="016bc-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="016bc-221">Die folgende Tabelle zeigt ein Beispiel für jeden Journaleintrag, der erforderlich ist, um die Finanzdaten unter den einzelnen Berichtsstandards fair darzustellen.</span><span class="sxs-lookup"><span data-stu-id="016bc-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="016bc-222">Anschließend wird eine detaillierte Beschreibung jedes Journaleintrags für den ersten Monat des Mietvertrags bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="016bc-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="016bc-223">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="016bc-224">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="016bc-225">Gesetzliches Buch (aktuelle Ebene)</span><span class="sxs-lookup"><span data-stu-id="016bc-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="016bc-226">Aktuelle Ebene insgesamt</span><span class="sxs-lookup"><span data-stu-id="016bc-226">Current layer total</span></span></th>
<th><span data-ttu-id="016bc-227">Stornobuch (benutzerdefinierte Ebene)</span><span class="sxs-lookup"><span data-stu-id="016bc-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="016bc-228">IFRS 16-Buch (benutzerdefinierte Ebene)</span><span class="sxs-lookup"><span data-stu-id="016bc-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="016bc-229">Aktuelle Ebene + benutzerdefinierte Ebene insgesamt</span><span class="sxs-lookup"><span data-stu-id="016bc-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="016bc-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="016bc-230">JE-100</span></span></th>
<th><span data-ttu-id="016bc-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="016bc-231">JE-110</span></span></th>
<th><span data-ttu-id="016bc-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="016bc-232">JE-120</span></span></th>
<th><span data-ttu-id="016bc-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="016bc-233">JE-130</span></span></th>
<th><span data-ttu-id="016bc-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="016bc-234">JE-140</span></span></th>
<th><span data-ttu-id="016bc-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="016bc-235">JE-150</span></span></th>
<th><span data-ttu-id="016bc-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="016bc-236">JE-160</span></span></th>
<th><span data-ttu-id="016bc-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="016bc-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="016bc-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="016bc-246">1</span><span class="sxs-lookup"><span data-stu-id="016bc-246">1</span></span></td>
<td><span data-ttu-id="016bc-247">Mietvertragsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-247">Lease expense</span></span></td>
<td><span data-ttu-id="016bc-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-249">1,000.00</span></span></td>
<td><span data-ttu-id="016bc-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="016bc-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-251">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-252">2</span><span class="sxs-lookup"><span data-stu-id="016bc-252">2</span></span></td>
<td><span data-ttu-id="016bc-253">Bankgebühr</span><span class="sxs-lookup"><span data-stu-id="016bc-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-254">3.00</span><span class="sxs-lookup"><span data-stu-id="016bc-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-255">3.00</span><span class="sxs-lookup"><span data-stu-id="016bc-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-256">3.00</span><span class="sxs-lookup"><span data-stu-id="016bc-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-257">3</span><span class="sxs-lookup"><span data-stu-id="016bc-257">3</span></span></td>
<td><span data-ttu-id="016bc-258">MwSt.-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-259">5.00</span><span class="sxs-lookup"><span data-stu-id="016bc-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-260">5.00</span><span class="sxs-lookup"><span data-stu-id="016bc-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-261">5.00</span><span class="sxs-lookup"><span data-stu-id="016bc-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-262">4</span><span class="sxs-lookup"><span data-stu-id="016bc-262">4</span></span></td>
<td><span data-ttu-id="016bc-263">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="016bc-263">Clearing account</span></span></td>
<td><span data-ttu-id="016bc-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="016bc-264">-1,000.00</span></span></td>
<td><span data-ttu-id="016bc-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-266">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-266">0.00</span></span></td>
<td><span data-ttu-id="016bc-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="016bc-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-269">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-270">5</span><span class="sxs-lookup"><span data-stu-id="016bc-270">5</span></span></td>
<td><span data-ttu-id="016bc-271">Kreditorenkonten</span><span class="sxs-lookup"><span data-stu-id="016bc-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="016bc-272">-1,008.00</span></span></td>
<td><span data-ttu-id="016bc-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="016bc-273">1,008.00</span></span></td>
<td><span data-ttu-id="016bc-274">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-275">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-276">6</span><span class="sxs-lookup"><span data-stu-id="016bc-276">6</span></span></td>
<td><span data-ttu-id="016bc-277">Nutzungsrecht am Leasingobjekt</span><span class="sxs-lookup"><span data-stu-id="016bc-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-278">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="016bc-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="016bc-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-281">7</span><span class="sxs-lookup"><span data-stu-id="016bc-281">7</span></span></td>
<td><span data-ttu-id="016bc-282">Finanzierungsleasingsverpflichtung</span><span class="sxs-lookup"><span data-stu-id="016bc-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-283">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="016bc-284">-22,794.00</span></span></td>
<td><span data-ttu-id="016bc-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-285">1,000.00</span></span></td>
<td><span data-ttu-id="016bc-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="016bc-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="016bc-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-288">8</span><span class="sxs-lookup"><span data-stu-id="016bc-288">8</span></span></td>
<td><span data-ttu-id="016bc-289">Zinsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-290">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-291">94.97</span><span class="sxs-lookup"><span data-stu-id="016bc-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-292">94.97</span><span class="sxs-lookup"><span data-stu-id="016bc-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-293">9</span><span class="sxs-lookup"><span data-stu-id="016bc-293">9</span></span></td>
<td><span data-ttu-id="016bc-294">Bargeld</span><span class="sxs-lookup"><span data-stu-id="016bc-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="016bc-295">-1,008.00</span></span></td>
<td><span data-ttu-id="016bc-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="016bc-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="016bc-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-298">10</span><span class="sxs-lookup"><span data-stu-id="016bc-298">10</span></span></td>
<td><span data-ttu-id="016bc-299">Abschreibungsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-300">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-301">949.75</span><span class="sxs-lookup"><span data-stu-id="016bc-301">949.75</span></span></td>
<td><span data-ttu-id="016bc-302">949.75</span><span class="sxs-lookup"><span data-stu-id="016bc-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-303">11</span><span class="sxs-lookup"><span data-stu-id="016bc-303">11</span></span></td>
<td><span data-ttu-id="016bc-304">Kumulierte Abschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-305">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="016bc-306">-949.75</span></span></td>
<td><span data-ttu-id="016bc-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="016bc-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="016bc-308">Wie die vorstehende Tabelle zeigt, müssen drei Bücher sowohl nach der gesetzlichen Berichterstattung als auch nach der IFRS-Berichterstattung ausgewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="016bc-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="016bc-309">Das gesetzliche Buch erfasst die Mietzahlung gemäß den Regeln für die Barabrechnung unter der aktuellen Ebene.</span><span class="sxs-lookup"><span data-stu-id="016bc-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="016bc-310">Das gesetzliche Stornobuch storniert die gesetzlichen Journaleinträgen.</span><span class="sxs-lookup"><span data-stu-id="016bc-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="016bc-311">Das IFRS 16-Buch erstellt die Journaleinträgen, die nach IFRS 16 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="016bc-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="016bc-312">Sie müssen einen Mietvertrag nur einmal abschließen.</span><span class="sxs-lookup"><span data-stu-id="016bc-312">You must enter a lease only one time.</span></span> <span data-ttu-id="016bc-313">Sie können dann die Seite **Bücher** öffnen, um alle Bücher zu sehen, die mit dem Mietvertrag verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="016bc-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="016bc-314">Wenn Sie die Bücher erstellen, müssen alle drei mit demselben Mietvertragsdatensatz verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="016bc-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="016bc-315">Der erste Journaleintrag erfasst die Mietkosten im gesetzlichen Buch.</span><span class="sxs-lookup"><span data-stu-id="016bc-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="016bc-316">Sie können die Zahlungen entweder in einem Batch oder durch Auswahl des Zahlungsplans im gesetzlichen Buch erstellen.</span><span class="sxs-lookup"><span data-stu-id="016bc-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="016bc-317">In diesem Beispiel wird der folgende Journaleintrag für das gesetzliche Buch aus dem Zahlungsplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="016bc-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="016bc-318">Mietzahlung – 31.01.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="016bc-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="016bc-319">Kontenart</span><span class="sxs-lookup"><span data-stu-id="016bc-319">Account type</span></span> | <span data-ttu-id="016bc-320">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-320">Account number</span></span> | <span data-ttu-id="016bc-321">Ebene</span><span class="sxs-lookup"><span data-stu-id="016bc-321">Layer</span></span>   | <span data-ttu-id="016bc-322">Kontobeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-322">Account description</span></span> | <span data-ttu-id="016bc-323">Belastung</span><span class="sxs-lookup"><span data-stu-id="016bc-323">Debit</span></span>    | <span data-ttu-id="016bc-324">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="016bc-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="016bc-325">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-325">Ledger</span></span>       | <span data-ttu-id="016bc-326">1</span><span class="sxs-lookup"><span data-stu-id="016bc-326">1</span></span>              | <span data-ttu-id="016bc-327">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-327">Current</span></span> | <span data-ttu-id="016bc-328">Mietvertragsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-328">Lease expense</span></span>       | <span data-ttu-id="016bc-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-329">1,000.00</span></span> |          |
| <span data-ttu-id="016bc-330">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-330">Ledger</span></span>       | <span data-ttu-id="016bc-331">4</span><span class="sxs-lookup"><span data-stu-id="016bc-331">4</span></span>              | <span data-ttu-id="016bc-332">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-332">Current</span></span> | <span data-ttu-id="016bc-333">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="016bc-333">Clearing account</span></span>    |          | <span data-ttu-id="016bc-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-334">1,000.00</span></span> |

<span data-ttu-id="016bc-335">Ein Kreditorenbuchhalter verwendet die Standardfunktionalität von Dynamics 365, um eine Rechnung für die Zahlung des Mietvertrags außerhalb des Anlagenleasings zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="016bc-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="016bc-336">Anstatt jedoch **Mietaufwand** als Debitkonto auszuwählen, wählt der Kreditorenbuchhalter ein Verrechnungskonto aus, um den folgenden Eintrag zu generieren.</span><span class="sxs-lookup"><span data-stu-id="016bc-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="016bc-337">AP-Prozess – 31.01.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="016bc-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="016bc-338">Kontenart</span><span class="sxs-lookup"><span data-stu-id="016bc-338">Account type</span></span> | <span data-ttu-id="016bc-339">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-339">Account number</span></span> | <span data-ttu-id="016bc-340">Ebene</span><span class="sxs-lookup"><span data-stu-id="016bc-340">Layer</span></span>   | <span data-ttu-id="016bc-341">Kontobeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-341">Account description</span></span> | <span data-ttu-id="016bc-342">Belastung</span><span class="sxs-lookup"><span data-stu-id="016bc-342">Debit</span></span>    | <span data-ttu-id="016bc-343">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="016bc-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="016bc-344">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-344">Ledger</span></span>       | <span data-ttu-id="016bc-345">4</span><span class="sxs-lookup"><span data-stu-id="016bc-345">4</span></span>              | <span data-ttu-id="016bc-346">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-346">Current</span></span> | <span data-ttu-id="016bc-347">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="016bc-347">Clearing account</span></span>    | <span data-ttu-id="016bc-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-348">1,000.00</span></span> |          |
| <span data-ttu-id="016bc-349">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-349">Ledger</span></span>       | <span data-ttu-id="016bc-350">2</span><span class="sxs-lookup"><span data-stu-id="016bc-350">2</span></span>              | <span data-ttu-id="016bc-351">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-351">Current</span></span> | <span data-ttu-id="016bc-352">Bankgebühr</span><span class="sxs-lookup"><span data-stu-id="016bc-352">Bank fee</span></span>            | <span data-ttu-id="016bc-353">3.00</span><span class="sxs-lookup"><span data-stu-id="016bc-353">3.00</span></span>     |          |
| <span data-ttu-id="016bc-354">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-354">Ledger</span></span>       | <span data-ttu-id="016bc-355">3</span><span class="sxs-lookup"><span data-stu-id="016bc-355">3</span></span>              | <span data-ttu-id="016bc-356">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-356">Current</span></span> | <span data-ttu-id="016bc-357">MwSt.-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-357">VAT expense</span></span>         | <span data-ttu-id="016bc-358">5.00</span><span class="sxs-lookup"><span data-stu-id="016bc-358">5.00</span></span>     |          |
| <span data-ttu-id="016bc-359">Lieferant</span><span class="sxs-lookup"><span data-stu-id="016bc-359">Vendor</span></span>       | <span data-ttu-id="016bc-360">5</span><span class="sxs-lookup"><span data-stu-id="016bc-360">5</span></span>              | <span data-ttu-id="016bc-361">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-361">Current</span></span> | <span data-ttu-id="016bc-362">Kreditorenkonten</span><span class="sxs-lookup"><span data-stu-id="016bc-362">Accounts payable</span></span>    |          | <span data-ttu-id="016bc-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="016bc-363">1,008.00</span></span> |

<span data-ttu-id="016bc-364">Wenn die Abrechnung an den Verkäufer ausgestellt wird, folgen Sie dem regulären Zahlungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="016bc-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="016bc-365">Während dieses Vorgangs wird der folgende Journaleintrag generiert.</span><span class="sxs-lookup"><span data-stu-id="016bc-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="016bc-366">Barzahlung – 31.01.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="016bc-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="016bc-367">Kontenart</span><span class="sxs-lookup"><span data-stu-id="016bc-367">Account type</span></span> | <span data-ttu-id="016bc-368">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-368">Account number</span></span> | <span data-ttu-id="016bc-369">Ebene</span><span class="sxs-lookup"><span data-stu-id="016bc-369">Layer</span></span>   | <span data-ttu-id="016bc-370">Kontobeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-370">Account description</span></span> | <span data-ttu-id="016bc-371">Belastung</span><span class="sxs-lookup"><span data-stu-id="016bc-371">Debit</span></span>    | <span data-ttu-id="016bc-372">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="016bc-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="016bc-373">Lieferant</span><span class="sxs-lookup"><span data-stu-id="016bc-373">Vendor</span></span>       | <span data-ttu-id="016bc-374">5</span><span class="sxs-lookup"><span data-stu-id="016bc-374">5</span></span>              | <span data-ttu-id="016bc-375">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-375">Current</span></span> | <span data-ttu-id="016bc-376">Kreditoren</span><span class="sxs-lookup"><span data-stu-id="016bc-376">Accounts Payable</span></span>    | <span data-ttu-id="016bc-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="016bc-377">1,008.00</span></span> |          |
| <span data-ttu-id="016bc-378">Bank</span><span class="sxs-lookup"><span data-stu-id="016bc-378">Bank</span></span>         | <span data-ttu-id="016bc-379">9</span><span class="sxs-lookup"><span data-stu-id="016bc-379">9</span></span>              | <span data-ttu-id="016bc-380">Aktuell</span><span class="sxs-lookup"><span data-stu-id="016bc-380">Current</span></span> | <span data-ttu-id="016bc-381">Bargeld</span><span class="sxs-lookup"><span data-stu-id="016bc-381">Cash</span></span>                |          | <span data-ttu-id="016bc-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="016bc-382">1,008.00</span></span> |

<span data-ttu-id="016bc-383">Zu diesem Zeitpunkt haben Sie diesen Mietvertrag gemäß den gesetzlichen Meldepflichten vollständig bilanziert und können mithilfe der aktuellen Ebene einen Probesaldo erstellen.</span><span class="sxs-lookup"><span data-stu-id="016bc-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="016bc-384">Das System gibt eine Testbilanz mit den folgenden Zahlen zurück.</span><span class="sxs-lookup"><span data-stu-id="016bc-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="016bc-385">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="016bc-386">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="016bc-387">Gesetzliches Buch (aktuelle Ebene)</span><span class="sxs-lookup"><span data-stu-id="016bc-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="016bc-388">Aktuelle Ebene insgesamt</span><span class="sxs-lookup"><span data-stu-id="016bc-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="016bc-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="016bc-389">JE-100</span></span></th>
<th><span data-ttu-id="016bc-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="016bc-390">JE-110</span></span></th>
<th><span data-ttu-id="016bc-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="016bc-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="016bc-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="016bc-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="016bc-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="016bc-395">1</span><span class="sxs-lookup"><span data-stu-id="016bc-395">1</span></span></td>
<td><span data-ttu-id="016bc-396">Mietvertragsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-396">Lease expense</span></span></td>
<td><span data-ttu-id="016bc-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-399">2</span><span class="sxs-lookup"><span data-stu-id="016bc-399">2</span></span></td>
<td><span data-ttu-id="016bc-400">Bankgebühr</span><span class="sxs-lookup"><span data-stu-id="016bc-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-401">3.00</span><span class="sxs-lookup"><span data-stu-id="016bc-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-402">3.00</span><span class="sxs-lookup"><span data-stu-id="016bc-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-403">3</span><span class="sxs-lookup"><span data-stu-id="016bc-403">3</span></span></td>
<td><span data-ttu-id="016bc-404">MwSt.-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-405">5.00</span><span class="sxs-lookup"><span data-stu-id="016bc-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-406">5.00</span><span class="sxs-lookup"><span data-stu-id="016bc-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-407">4</span><span class="sxs-lookup"><span data-stu-id="016bc-407">4</span></span></td>
<td><span data-ttu-id="016bc-408">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="016bc-408">Clearing account</span></span></td>
<td><span data-ttu-id="016bc-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="016bc-409">-1,000.00</span></span></td>
<td><span data-ttu-id="016bc-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-411">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-412">5</span><span class="sxs-lookup"><span data-stu-id="016bc-412">5</span></span></td>
<td><span data-ttu-id="016bc-413">Kreditorenkonten</span><span class="sxs-lookup"><span data-stu-id="016bc-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="016bc-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="016bc-414">-1,008.00</span></span></td>
<td><span data-ttu-id="016bc-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="016bc-415">1,008.00</span></span></td>
<td><span data-ttu-id="016bc-416">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-417">6</span><span class="sxs-lookup"><span data-stu-id="016bc-417">6</span></span></td>
<td><span data-ttu-id="016bc-418">Nutzungsrecht am Leasingobjekt</span><span class="sxs-lookup"><span data-stu-id="016bc-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-419">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-420">7</span><span class="sxs-lookup"><span data-stu-id="016bc-420">7</span></span></td>
<td><span data-ttu-id="016bc-421">Finanzierungsleasingsverpflichtung</span><span class="sxs-lookup"><span data-stu-id="016bc-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-422">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-423">8</span><span class="sxs-lookup"><span data-stu-id="016bc-423">8</span></span></td>
<td><span data-ttu-id="016bc-424">Zinsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-425">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-426">9</span><span class="sxs-lookup"><span data-stu-id="016bc-426">9</span></span></td>
<td><span data-ttu-id="016bc-427">Bargeld</span><span class="sxs-lookup"><span data-stu-id="016bc-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="016bc-428">-1,008.00</span></span></td>
<td><span data-ttu-id="016bc-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="016bc-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-430">10</span><span class="sxs-lookup"><span data-stu-id="016bc-430">10</span></span></td>
<td><span data-ttu-id="016bc-431">Abschreibungsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-432">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="016bc-433">11</span><span class="sxs-lookup"><span data-stu-id="016bc-433">11</span></span></td>
<td><span data-ttu-id="016bc-434">Kumulierte Abschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="016bc-435">0,00</span><span class="sxs-lookup"><span data-stu-id="016bc-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="016bc-436">Wenn Sie die IFRS 16-Zahlen verwenden möchten, um denselben Probesaldo zu erstellen, müssen die gesetzlichen Buchungsführungsjournaleinträge storniert und die IFRS 16-Journaleinträge gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="016bc-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="016bc-437">Um die gesetzlichen Journaleinträge zu stornieren, enthält dieses Beispiel ein gesetzliches Stornobuch, das den gleichen Aufbau wie das gesetzliche Buch hat, jedoch ein entgegengesetztes Buchungsprofil aufweist.</span><span class="sxs-lookup"><span data-stu-id="016bc-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="016bc-438">Zum Beispiel *belastet* das gesetzliche Buch ein Mietaufwandskonto, aber im Stornobuch wird in diesem Konto ein *Haben* verbucht.</span><span class="sxs-lookup"><span data-stu-id="016bc-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="016bc-439">Diese Beziehungen lassen sich leicht in den Buchungen für das Anlagenleasing auf dem Konto **Parameter für das Anlagenleasing** auf der Seite (**Anlagenleasing \> Einrichtung \> Parameter für das Anlagenleasing**) definieren.</span><span class="sxs-lookup"><span data-stu-id="016bc-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="016bc-440">Wenn derselbe Prozess, der für das gesetzliche Buch verwendet wurde, für das Stornobuch verwendet wird, wird der folgende Journaleintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="016bc-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="016bc-441">Der Unterschied besteht darin, dass das Stornobuch die Stornobuchungen aus dem gesetzlichen Buch bucht.</span><span class="sxs-lookup"><span data-stu-id="016bc-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="016bc-442">Die Stornoeinträge werden auch auf der benutzerdefinierten Ebene vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="016bc-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="016bc-443">Wenn auf der aktuellen Ebene ein Testhaben ausgeführt wird, sind die Stornojournaleinträge nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="016bc-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="016bc-444">Mietzahlung – 31.01.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="016bc-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="016bc-445">Kontenart</span><span class="sxs-lookup"><span data-stu-id="016bc-445">Account type</span></span> | <span data-ttu-id="016bc-446">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-446">Account number</span></span> | <span data-ttu-id="016bc-447">Ebene</span><span class="sxs-lookup"><span data-stu-id="016bc-447">Layer</span></span>  | <span data-ttu-id="016bc-448">Kontobeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-448">Account description</span></span> | <span data-ttu-id="016bc-449">Belastung</span><span class="sxs-lookup"><span data-stu-id="016bc-449">Debit</span></span>    | <span data-ttu-id="016bc-450">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="016bc-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="016bc-451">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-451">Ledger</span></span>       | <span data-ttu-id="016bc-452">4</span><span class="sxs-lookup"><span data-stu-id="016bc-452">4</span></span>              | <span data-ttu-id="016bc-453">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-453">Custom</span></span> | <span data-ttu-id="016bc-454">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="016bc-454">Clearing account</span></span>    | <span data-ttu-id="016bc-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-455">1,000.00</span></span> |          |
| <span data-ttu-id="016bc-456">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-456">Ledger</span></span>       | <span data-ttu-id="016bc-457">1</span><span class="sxs-lookup"><span data-stu-id="016bc-457">1</span></span>              | <span data-ttu-id="016bc-458">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-458">Custom</span></span> | <span data-ttu-id="016bc-459">Mietvertragsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-459">Lease expense</span></span>       |          | <span data-ttu-id="016bc-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-460">1,000.00</span></span> |

<span data-ttu-id="016bc-461">Nachdem Sie die gesetzlichen Journaleinträge entfernt haben, buchen Sie alle Journaleinträge , die nach IFRS 16 erforderlich sind, im IFRS 16-Buch.</span><span class="sxs-lookup"><span data-stu-id="016bc-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="016bc-462">Diese Einträge umfassen die erstmaligen Erfassung des Nutzungsrechts am Leasingobjekt und der Verbindlichkeit sowie die Aufzeichnung von Zinsen und Abschreibungen.</span><span class="sxs-lookup"><span data-stu-id="016bc-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="016bc-463">Erstmalige Erfassung – 01.01.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="016bc-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="016bc-464">Kontenart</span><span class="sxs-lookup"><span data-stu-id="016bc-464">Account type</span></span> | <span data-ttu-id="016bc-465">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-465">Account number</span></span> | <span data-ttu-id="016bc-466">Ebene</span><span class="sxs-lookup"><span data-stu-id="016bc-466">Layer</span></span>  | <span data-ttu-id="016bc-467">Kontobeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-467">Account description</span></span>      | <span data-ttu-id="016bc-468">Belastung</span><span class="sxs-lookup"><span data-stu-id="016bc-468">Debit</span></span>     | <span data-ttu-id="016bc-469">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="016bc-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="016bc-470">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-470">Ledger</span></span>       | <span data-ttu-id="016bc-471">6</span><span class="sxs-lookup"><span data-stu-id="016bc-471">6</span></span>              | <span data-ttu-id="016bc-472">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-472">Custom</span></span> | <span data-ttu-id="016bc-473">Nutzungsrecht am Leasingobjekt</span><span class="sxs-lookup"><span data-stu-id="016bc-473">ROU Asset</span></span>                | <span data-ttu-id="016bc-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="016bc-474">22,793.90</span></span> |           |
| <span data-ttu-id="016bc-475">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-475">Ledger</span></span>       | <span data-ttu-id="016bc-476">7</span><span class="sxs-lookup"><span data-stu-id="016bc-476">7</span></span>              | <span data-ttu-id="016bc-477">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-477">Custom</span></span> | <span data-ttu-id="016bc-478">Finanzierungsleasingsverpflichtung</span><span class="sxs-lookup"><span data-stu-id="016bc-478">Finance lease obligation</span></span> |           | <span data-ttu-id="016bc-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="016bc-479">22,793.90</span></span> |

<span data-ttu-id="016bc-480">Die Mietzahlung wird wie die anderen Mietzahlungen gebucht.</span><span class="sxs-lookup"><span data-stu-id="016bc-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="016bc-481">Der Grund für die Verwendung des Verrechnungskontos besteht darin, sicherzustellen, dass Bargeld nur einmal gutgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="016bc-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="016bc-482">Mietzahlung – 31.01.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="016bc-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="016bc-483">Kontenart</span><span class="sxs-lookup"><span data-stu-id="016bc-483">Account type</span></span> | <span data-ttu-id="016bc-484">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-484">Account number</span></span> | <span data-ttu-id="016bc-485">Ebene</span><span class="sxs-lookup"><span data-stu-id="016bc-485">Layer</span></span>  | <span data-ttu-id="016bc-486">Kontobeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-486">Account description</span></span>      | <span data-ttu-id="016bc-487">Belastung</span><span class="sxs-lookup"><span data-stu-id="016bc-487">Debit</span></span>    | <span data-ttu-id="016bc-488">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="016bc-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="016bc-489">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-489">Ledger</span></span>       | <span data-ttu-id="016bc-490">7</span><span class="sxs-lookup"><span data-stu-id="016bc-490">7</span></span>              | <span data-ttu-id="016bc-491">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-491">Custom</span></span> | <span data-ttu-id="016bc-492">Finanzierungsleasingsverpflichtung</span><span class="sxs-lookup"><span data-stu-id="016bc-492">Finance lease obligation</span></span> | <span data-ttu-id="016bc-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-493">1,000.00</span></span> |          |
| <span data-ttu-id="016bc-494">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-494">Ledger</span></span>       | <span data-ttu-id="016bc-495">4</span><span class="sxs-lookup"><span data-stu-id="016bc-495">4</span></span>              | <span data-ttu-id="016bc-496">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-496">Custom</span></span> | <span data-ttu-id="016bc-497">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="016bc-497">Clearing account</span></span>         |          | <span data-ttu-id="016bc-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="016bc-498">1,000.00</span></span> |

<span data-ttu-id="016bc-499">Die Buchung des Zinsaufwandsjournals wird aus dem Tilgungsplan für Verbindlichkeiten generiert.</span><span class="sxs-lookup"><span data-stu-id="016bc-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="016bc-500">Zinsausgaben – 31.01.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="016bc-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="016bc-501">Kontenart</span><span class="sxs-lookup"><span data-stu-id="016bc-501">Account type</span></span> | <span data-ttu-id="016bc-502">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-502">Account number</span></span> | <span data-ttu-id="016bc-503">Ebene</span><span class="sxs-lookup"><span data-stu-id="016bc-503">Layer</span></span>  | <span data-ttu-id="016bc-504">Kontobeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-504">Account description</span></span>      | <span data-ttu-id="016bc-505">Belastung</span><span class="sxs-lookup"><span data-stu-id="016bc-505">Debit</span></span> | <span data-ttu-id="016bc-506">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="016bc-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="016bc-507">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-507">Ledger</span></span>       | <span data-ttu-id="016bc-508">8</span><span class="sxs-lookup"><span data-stu-id="016bc-508">8</span></span>              | <span data-ttu-id="016bc-509">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-509">Custom</span></span> | <span data-ttu-id="016bc-510">Zinsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-510">Interest expense</span></span>         | <span data-ttu-id="016bc-511">94.97</span><span class="sxs-lookup"><span data-stu-id="016bc-511">94.97</span></span> |        |
| <span data-ttu-id="016bc-512">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-512">Ledger</span></span>       | <span data-ttu-id="016bc-513">7</span><span class="sxs-lookup"><span data-stu-id="016bc-513">7</span></span>              | <span data-ttu-id="016bc-514">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-514">Custom</span></span> | <span data-ttu-id="016bc-515">Finanzierungsleasingsverpflichtung</span><span class="sxs-lookup"><span data-stu-id="016bc-515">Finance lease obligation</span></span> |       | <span data-ttu-id="016bc-516">94.97</span><span class="sxs-lookup"><span data-stu-id="016bc-516">94.97</span></span>  |

<span data-ttu-id="016bc-517">Die Abschreibung des Zinsaufwandsjournals wird aus dem Tilgungsplan für Anlageabschreibungen generiert.</span><span class="sxs-lookup"><span data-stu-id="016bc-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="016bc-518">Abschreibungsausgaben – 31.01.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="016bc-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="016bc-519">Kontenart</span><span class="sxs-lookup"><span data-stu-id="016bc-519">Account type</span></span> | <span data-ttu-id="016bc-520">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="016bc-520">Account number</span></span> | <span data-ttu-id="016bc-521">Ebene</span><span class="sxs-lookup"><span data-stu-id="016bc-521">Layer</span></span>  | <span data-ttu-id="016bc-522">Kontobeschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-522">Account description</span></span>      | <span data-ttu-id="016bc-523">Belastung</span><span class="sxs-lookup"><span data-stu-id="016bc-523">Debit</span></span>  | <span data-ttu-id="016bc-524">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="016bc-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="016bc-525">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-525">Ledger</span></span>       | <span data-ttu-id="016bc-526">10</span><span class="sxs-lookup"><span data-stu-id="016bc-526">10</span></span>             | <span data-ttu-id="016bc-527">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-527">Custom</span></span> | <span data-ttu-id="016bc-528">Abschreibungsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-528">Depreciation expense</span></span>     | <span data-ttu-id="016bc-529">949.75</span><span class="sxs-lookup"><span data-stu-id="016bc-529">949.75</span></span> |        |
| <span data-ttu-id="016bc-530">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="016bc-530">Ledger</span></span>       | <span data-ttu-id="016bc-531">11</span><span class="sxs-lookup"><span data-stu-id="016bc-531">11</span></span>             | <span data-ttu-id="016bc-532">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="016bc-532">Custom</span></span> | <span data-ttu-id="016bc-533">Kumulierte Abschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="016bc-534">949.75</span><span class="sxs-lookup"><span data-stu-id="016bc-534">949.75</span></span> |

<span data-ttu-id="016bc-535">Nachdem alle diese Journaleinträge erstellt und gebucht wurden, werden die folgenden Werte für „benutzerdefinierte Ebene 1“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="016bc-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="016bc-536">Beachten Sie, dass die letzte Spalte die Bankgebühr, den Mehrwertsteueraufwand und die Reduzierung des Bargeldes aus der vorherigen Ebene enthält, jedoch nicht die gesetzlich vorgeschriebenen Journaleinträge.</span><span class="sxs-lookup"><span data-stu-id="016bc-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="016bc-537">Auf diese Weise erzielen Sie echte Funktionen für doppelte Berichterstattung.</span><span class="sxs-lookup"><span data-stu-id="016bc-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="016bc-538">Zu diesem Zeitpunkt muss das Unternehmen lediglich seine Testbilanz ausführen und die aktuelle Ebene und die benutzerdefinierte Ebene kombinieren, um eine IFRS-Testbilanz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="016bc-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="016bc-539">Kontonr.</span><span class="sxs-lookup"><span data-stu-id="016bc-539">Account No</span></span> | <span data-ttu-id="016bc-540">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-540">Description</span></span>              | <span data-ttu-id="016bc-541">Gesetzliches Buch\-Aktuelle Ebene\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="016bc-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="016bc-542">Gesetzliches Buch\-Aktuelle Ebene\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="016bc-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="016bc-543">Gesetzliches Buch\-Aktuelle Ebene\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="016bc-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="016bc-544">Aktuelle Ebene \- Insgesamt</span><span class="sxs-lookup"><span data-stu-id="016bc-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="016bc-545">Stornobuch\-Benutzerdefinierte Ebene\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="016bc-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="016bc-546">IFRS 16-Buch\-Benutzerdefinierte Ebene\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="016bc-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="016bc-547">IFRS 16-Buch\-Benutzerdefinierte Ebene\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="016bc-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="016bc-548">IFRS 16-Buch\-Benutzerdefinierte Ebene\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="016bc-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="016bc-549">IFRS 16-Buch\-Benutzerdefinierte Ebene\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="016bc-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="016bc-550">Benutzerdefinierte Ebene \+ Aktuelle Ebene \- Insgesamt</span><span class="sxs-lookup"><span data-stu-id="016bc-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="016bc-551">1</span><span class="sxs-lookup"><span data-stu-id="016bc-551">1</span></span>          | <span data-ttu-id="016bc-552">Mietvertragsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-552">Lease expense</span></span>            | <span data-ttu-id="016bc-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="016bc-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-554">1,000\.00</span></span>               |   | <span data-ttu-id="016bc-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="016bc-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="016bc-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-556">0\.00</span></span>                                   |
| <span data-ttu-id="016bc-557">2</span><span class="sxs-lookup"><span data-stu-id="016bc-557">2</span></span>          | <span data-ttu-id="016bc-558">Bankgebühr</span><span class="sxs-lookup"><span data-stu-id="016bc-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="016bc-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="016bc-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="016bc-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-561">3\.00</span></span>                                   |
| <span data-ttu-id="016bc-562">3</span><span class="sxs-lookup"><span data-stu-id="016bc-562">3</span></span>          | <span data-ttu-id="016bc-563">MwSt.-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="016bc-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="016bc-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="016bc-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-566">5\.00</span></span>                                   |
| <span data-ttu-id="016bc-567">4</span><span class="sxs-lookup"><span data-stu-id="016bc-567">4</span></span>          | <span data-ttu-id="016bc-568">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="016bc-568">Clearing account</span></span>         | <span data-ttu-id="016bc-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="016bc-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="016bc-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-571">0\.00</span></span>                   |   | <span data-ttu-id="016bc-572">1.000</span><span class="sxs-lookup"><span data-stu-id="016bc-572">1,000</span></span>                                           |                                                | <span data-ttu-id="016bc-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="016bc-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="016bc-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-574">0\.00</span></span>                                   |
| <span data-ttu-id="016bc-575">5</span><span class="sxs-lookup"><span data-stu-id="016bc-575">5</span></span>          | <span data-ttu-id="016bc-576">Kreditorenkonten</span><span class="sxs-lookup"><span data-stu-id="016bc-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="016bc-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="016bc-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-578">1,008\.00</span></span>                                         | <span data-ttu-id="016bc-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="016bc-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-580">0\.00</span></span>                                   |
| <span data-ttu-id="016bc-581">6</span><span class="sxs-lookup"><span data-stu-id="016bc-581">6</span></span>          | <span data-ttu-id="016bc-582">Nutzungsrecht am Leasingobjekt</span><span class="sxs-lookup"><span data-stu-id="016bc-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="016bc-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="016bc-584">22,794</span><span class="sxs-lookup"><span data-stu-id="016bc-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="016bc-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="016bc-585">22,793\.90</span></span>                              |
| <span data-ttu-id="016bc-586">7</span><span class="sxs-lookup"><span data-stu-id="016bc-586">7</span></span>          | <span data-ttu-id="016bc-587">Finanzierungsleasingsverpflichtung</span><span class="sxs-lookup"><span data-stu-id="016bc-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="016bc-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="016bc-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="016bc-589">\-22,794</span></span>                                       | <span data-ttu-id="016bc-590">1.000</span><span class="sxs-lookup"><span data-stu-id="016bc-590">1,000</span></span>                                          | <span data-ttu-id="016bc-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="016bc-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="016bc-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="016bc-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="016bc-593">8</span><span class="sxs-lookup"><span data-stu-id="016bc-593">8</span></span>          | <span data-ttu-id="016bc-594">Zinsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="016bc-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="016bc-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="016bc-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="016bc-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="016bc-597">94\.97</span></span>                                  |
| <span data-ttu-id="016bc-598">9</span><span class="sxs-lookup"><span data-stu-id="016bc-598">9</span></span>          | <span data-ttu-id="016bc-599">Bargeld</span><span class="sxs-lookup"><span data-stu-id="016bc-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="016bc-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="016bc-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="016bc-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="016bc-603">10</span><span class="sxs-lookup"><span data-stu-id="016bc-603">10</span></span>         | <span data-ttu-id="016bc-604">Abschreibungsausgaben</span><span class="sxs-lookup"><span data-stu-id="016bc-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="016bc-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="016bc-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="016bc-606">949\.75</span></span>                                        | <span data-ttu-id="016bc-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="016bc-607">949\.75</span></span>                                 |
| <span data-ttu-id="016bc-608">11</span><span class="sxs-lookup"><span data-stu-id="016bc-608">11</span></span>         | <span data-ttu-id="016bc-609">Kumulierte Abschreibung</span><span class="sxs-lookup"><span data-stu-id="016bc-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="016bc-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="016bc-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="016bc-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="016bc-611">\-949\.75</span></span>                                      | <span data-ttu-id="016bc-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="016bc-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]