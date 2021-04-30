---
title: Leasingbuchungsarten
description: In diesem Thema werden die Buchungsarten beschrieben, die für Anlagenleasing-Transaktionen verwendet werden.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881131"
---
# <a name="lease-posting-types"></a><span data-ttu-id="90096-103">Leasingbuchungsarten</span><span class="sxs-lookup"><span data-stu-id="90096-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90096-104">In diesem Thema werden die Buchungsarten beschrieben, die für Anlagenleasing-Transaktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90096-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="90096-105">Leasingobjekt</span><span class="sxs-lookup"><span data-stu-id="90096-105">Lease asset</span></span>

<span data-ttu-id="90096-106">Das Konto ist mit dem Nutzungsrecht am Leasingobjekt verknüpft.</span><span class="sxs-lookup"><span data-stu-id="90096-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="90096-107">Dieses Konto wird belastet, wenn ein Mietvertrag zum ersten Mal gemäß den neuen Mietbilanzierungsstandards, dem Kodifizierungsthema 842 (ASC 842) und dem International Financial Reporting Standard 16 (IFRS 16) erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="90096-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="90096-108">Bei einem geänderten Mietvertrag kann dieses Konto entweder belastet oder gutgeschrieben werden, je nachdem, ob die Änderung die Mietverbindlichkeit erhöht oder verringert.</span><span class="sxs-lookup"><span data-stu-id="90096-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="90096-109">**Beispieljournaleinträge:** Erstmalige Erfassung</span><span class="sxs-lookup"><span data-stu-id="90096-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="90096-110">**Soll:** Mietanlage XXX</span><span class="sxs-lookup"><span data-stu-id="90096-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="90096-111">**Haben:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="90096-112">Leasingverbindlichkeit</span><span class="sxs-lookup"><span data-stu-id="90096-112">Lease liability</span></span>

<span data-ttu-id="90096-113">Das Konto ist mit der Leasingverbindlichkeit verbunden, die entsteht, wenn Zahlungen nach den neuen Standards IFRS 16 und ASC 842 abgezinst werden.</span><span class="sxs-lookup"><span data-stu-id="90096-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="90096-114">Dieses Konto wird gutgeschrieben, wenn ein Mietvertrag nach den neuen Standards erstmals anerkannt wird.</span><span class="sxs-lookup"><span data-stu-id="90096-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="90096-115">Es wird für Mietzahlungen belastet und für Zinsabgrenzungen gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="90096-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="90096-116">**Beispieljournaleinträge:** Erstmalige Erfassung</span><span class="sxs-lookup"><span data-stu-id="90096-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="90096-117">**Soll:** Mietanlage XXX</span><span class="sxs-lookup"><span data-stu-id="90096-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="90096-118">**Haben:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="90096-119">**Beispieljournaleinträge:** Zinsabgrenzung</span><span class="sxs-lookup"><span data-stu-id="90096-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="90096-120">**Soll:** Zinsausgaben XXX</span><span class="sxs-lookup"><span data-stu-id="90096-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="90096-121">**Haben:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="90096-122">**Beispieljournaleinträge:** Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="90096-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="90096-123">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="90096-124">**Haben:** Kreditorenzahlung/Leasingzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="90096-125">Kurzfristige Leasingverbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="90096-125">Short-term lease liability</span></span>

<span data-ttu-id="90096-126">Das Konto ist mit der kurzfristigen Leasingverbindlichkeit verbunden, wenn der Journaleintrag für die kurzfristige Leasingverbindlichkeit neu gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="90096-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="90096-127">Diesem Konto wird die kurzfristige Verbindlichkeit aus dem Tilgungsplan am letzten Tag des Monats gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="90096-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="90096-128">Der gleiche Betrag wird jedoch am ersten Tag des nächsten Monats abgebucht.</span><span class="sxs-lookup"><span data-stu-id="90096-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="90096-129">**Beispieljournaleinträge:** Umgliederung der kurzfristigen Leasingverbindlichkeit</span><span class="sxs-lookup"><span data-stu-id="90096-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="90096-130">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="90096-131">**Haben:** Kurzfristige Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="90096-132">**Soll:** Kurzfristige Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="90096-133">**Haben:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="90096-134">Abschreibungsausgaben</span><span class="sxs-lookup"><span data-stu-id="90096-134">Depreciation expense</span></span>

<span data-ttu-id="90096-135">Das Konto ist mit dem Aufwand verbunden, der im Zusammenhang mit der Abschreibung des Nutzungsrecht am Leasingobjekt nach IFRS 16, ASC 842 und Finanzierungsleasing nach IAS 17 und ASC 840 steht.</span><span class="sxs-lookup"><span data-stu-id="90096-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="90096-136">Dieses Konto wird belastet, wenn ein Nutzungsrecht am Leasingobjekt jeden Monat abgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="90096-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="90096-137">**Beispieljournaleinträge:** Abschreibungsabgrenzung</span><span class="sxs-lookup"><span data-stu-id="90096-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="90096-138">**Soll:** Abschreibungsausgaben XXX</span><span class="sxs-lookup"><span data-stu-id="90096-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="90096-139">**Haben:** Kumulierte Abschreibung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="90096-140">Gewinn/Verlust bei Änderung des Mietvertrags</span><span class="sxs-lookup"><span data-stu-id="90096-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="90096-141">Das Konto ist mit Gewinnen oder Verlusten verbunden, die sich aus Mietvertragsänderungen ergeben.</span><span class="sxs-lookup"><span data-stu-id="90096-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="90096-142">Ein Gewinn kann während einer Mietvertragsänderung entstehen, wenn die Änderung die Leasingverbindlichkeit um einen Betrag verringert, der den Buchwert des Nutzungsrecht am Leasingobjekts übersteigt.</span><span class="sxs-lookup"><span data-stu-id="90096-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="90096-143">Beispielsweise hat ein Mietvertrag einen aktuellen Buchwert der Leasingverbindlichkeit von 150.000 USD und einen Buchwert des Nutzungsrecht am Leasingobjekts von 100.000 USD.</span><span class="sxs-lookup"><span data-stu-id="90096-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="90096-144">Der mietvertrag wird geändert, und diese Änderung ergibt einen neuen Barwert der zukünftigen Mindestleasingzahlungen (PVFMLP) von 40.000 USD.</span><span class="sxs-lookup"><span data-stu-id="90096-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="90096-145">Daher wird die Leasingverbindlichkeit von 110.000 USD (150.000 USD – 40.000 USD) belastet.</span><span class="sxs-lookup"><span data-stu-id="90096-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="90096-146">Da das Nutzungsrecht am Leasingobjekt nur 100.000 USD ist, verringert die Verringerung von 110.000 USD der Anlage nach 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="90096-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="90096-147">In den Bilanzierungsrichtlinien heißt es daher, dass der Rest auf ein Gewinnkonto gebucht werden sollte.</span><span class="sxs-lookup"><span data-stu-id="90096-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="90096-148">In diesem Fall ist der endgültige Journaleintrag eine Belastung der Leasingverbindlichkeit für 110.000 USD, eine Gutschrift für das Mietobjekt für 100.000 USD und eine Gutschrift für das Gewinnkonto für 10.000 USD.</span><span class="sxs-lookup"><span data-stu-id="90096-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="90096-149">**Beispieljournaleinträge:** Mietvertragsänderungen</span><span class="sxs-lookup"><span data-stu-id="90096-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="90096-150">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="90096-151">**Haben:** Mietanlage XXX</span><span class="sxs-lookup"><span data-stu-id="90096-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="90096-152">**Haben:** Gewinn XXX</span><span class="sxs-lookup"><span data-stu-id="90096-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="90096-153">Kumulierte Abschreibung</span><span class="sxs-lookup"><span data-stu-id="90096-153">Accumulated depreciation</span></span>

<span data-ttu-id="90096-154">Das Konto ist dem Gegen-Anlagenkonto des Nutzungsrecht am Leasingobjekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="90096-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="90096-155">Auf diesem Konto erfolgt beim Buchen einer Abschreibungsausgabe eine Habenbuchung.</span><span class="sxs-lookup"><span data-stu-id="90096-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="90096-156">**Beispieljournaleinträge:** Abschreibungsabgrenzung</span><span class="sxs-lookup"><span data-stu-id="90096-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="90096-157">**Soll:** Abschreibungsausgaben XXX</span><span class="sxs-lookup"><span data-stu-id="90096-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="90096-158">**Haben:** Kumulierte Abschreibung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="90096-159">Variable Zahlung</span><span class="sxs-lookup"><span data-stu-id="90096-159">Variable payment</span></span>

<span data-ttu-id="90096-160">Das Konto ist mit variablen Mietzahlungen verbunden, die durch eine Indexneubewertung gemäß Mietverträgen nach ASC 842, ASC 840 und IAS 17 erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="90096-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="90096-161">Im Mietzahlungsplan sind variable Zahlungen in der Spalte **Variable Zahlung** enthalten.</span><span class="sxs-lookup"><span data-stu-id="90096-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="90096-162">Dieses Konto wird belastet, wenn eine Rechnung für eine Zahlungsplanzeile erstellt wird, die eine variable Zahlung enthält.</span><span class="sxs-lookup"><span data-stu-id="90096-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="90096-163">**Beispieljournaleinträge:** Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="90096-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="90096-164">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="90096-165">**Soll:** Variable Zahlung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="90096-166">**Haben:** Kreditorenzahlung/Leasingzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="90096-167">Zurückgestellter Mietaufwand für Anlage (Verbindlichkeit)</span><span class="sxs-lookup"><span data-stu-id="90096-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="90096-168">Das Konto ist mit der Forderung des zurückgestellten Mietaufwands oder der Verbindlichkeit aus einem Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand verbunden.</span><span class="sxs-lookup"><span data-stu-id="90096-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="90096-169">Dieses Konto wird belastet, wenn eine Rechnung gegen ein Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand gebucht wird, wenn der Mietzahlungsbetrag den linearen Mietaufwand des Zeitraums übersteigt.</span><span class="sxs-lookup"><span data-stu-id="90096-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="90096-170">Es wird gutgeschrieben, wenn die Mietzahlung unter dem linearen Mietaufwand des Zeitraums liegt.</span><span class="sxs-lookup"><span data-stu-id="90096-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="90096-171">**Beispieljournaleinträge:** Mietzahlung (Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand)</span><span class="sxs-lookup"><span data-stu-id="90096-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="90096-172">**Soll:** Mietkosten XXX</span><span class="sxs-lookup"><span data-stu-id="90096-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="90096-173">**Haben:** Zurückgestellter Mietaufwand für Verbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="90096-174">**Haben:** Kreditorenzahlung/Leasingzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="90096-175">Mietvertragsausgaben</span><span class="sxs-lookup"><span data-stu-id="90096-175">Lease expense</span></span>

<span data-ttu-id="90096-176">Das Konto ist mit dem Mietaufwand verbunden, wenn der Mietvertrag als Mietvertrag mit Behandlung von zurückgestellem Mietaufwand eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="90096-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="90096-177">Dieses Konto wird belastet, wenn eine Rechnung gegen ein Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="90096-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="90096-178">**Beispieljournaleinträge:** Mietzahlung (Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand)</span><span class="sxs-lookup"><span data-stu-id="90096-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="90096-179">**Soll:** Mietkosten XXX</span><span class="sxs-lookup"><span data-stu-id="90096-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="90096-180">**Haben:** Zurückgestellter Mietaufwand für Verbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="90096-181">**Haben:** Kreditorenzahlung/Leasingzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="90096-182">Aufwand der dauerhaften Wertminderung</span><span class="sxs-lookup"><span data-stu-id="90096-182">Impairment expense</span></span>

<span data-ttu-id="90096-183">Das Konto wird gebucht, wenn ein Mietvertrag wertgemindert ist.</span><span class="sxs-lookup"><span data-stu-id="90096-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="90096-184">Dieses Konto wird belastet, während das Konto für das Nutzungsrecht am Leasingobjekt direkt gutgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="90096-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="90096-185">**Beispieljournaleinträge:** Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="90096-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="90096-186">**Soll:** Aufwand der dauerhaften Wertminderung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="90096-187">**Haben:** Nutzungsrecht am Leasingobjekt XXX</span><span class="sxs-lookup"><span data-stu-id="90096-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="90096-188">Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="90096-188">Lease payment</span></span>

<span data-ttu-id="90096-189">Das Konto wird gegen gebucht, wenn der **An Kreditor bezahlen**-Parameter ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="90096-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="90096-190">Dieses Konto wird anstelle des Kreditors gutgeschrieben, wenn der Parameter deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="90096-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="90096-191">**Beispieljournaleinträge:** Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="90096-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="90096-192">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="90096-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="90096-193">**Haben:** Mietzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="90096-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="90096-194">Buchungen des Ausgabentyps</span><span class="sxs-lookup"><span data-stu-id="90096-194">Expense type postings</span></span>

<span data-ttu-id="90096-195">Das für jede Ausgabenart ausgewählte Konto wird belastet, wenn eine Zahlung für diese Ausgabenart generiert wird.</span><span class="sxs-lookup"><span data-stu-id="90096-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="90096-196">Zum Beispiel wird das Konto, das für die Kostenart **Versicherung** angegeben ist, immer dann belastet, wenn eine Rechnung oder ein Zahlungsjournaleintrag aus dem Plan für Nebenkosten beim Leasing bei Versicherungskosten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="90096-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="90096-197">**Beispieljournaleinträge:** Versicherungszahlung</span><span class="sxs-lookup"><span data-stu-id="90096-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="90096-198">**Soll:** Versicherungskostenartkonto XXX</span><span class="sxs-lookup"><span data-stu-id="90096-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="90096-199">**Haben:** Gegenkonto XXX</span><span class="sxs-lookup"><span data-stu-id="90096-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="90096-200">Das Gegenkonto wird auf Mietvertragsebene in den Zeilen für den Zahlungsplan für die Nebenkosten beim Leasing ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="90096-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="90096-201">Dieses Gegenkonto kann dem Kreditor oder einem Sachkonto zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="90096-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
