---
title: Leasingbuchungsarten
description: In diesem Thema werden die Buchungsarten beschrieben, die für Anlagenleasing-Transaktionen verwendet werden.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ceb4fbeb4dbf2f535e05a9d46c84169435d2803b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443784"
---
# <a name="lease-posting-types"></a><span data-ttu-id="1e120-103">Leasingbuchungsarten</span><span class="sxs-lookup"><span data-stu-id="1e120-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e120-104">In diesem Thema werden die Buchungsarten beschrieben, die für Anlagenleasing-Transaktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e120-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="1e120-105">Leasingobjekt</span><span class="sxs-lookup"><span data-stu-id="1e120-105">Lease asset</span></span>

<span data-ttu-id="1e120-106">Das Konto ist mit dem Nutzungsrecht am Leasingobjekt verknüpft.</span><span class="sxs-lookup"><span data-stu-id="1e120-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="1e120-107">Dieses Konto wird belastet, wenn ein Mietvertrag zum ersten Mal gemäß den neuen Mietbilanzierungsstandards, dem Kodifizierungsthema 842 (ASC 842) und dem International Financial Reporting Standard 16 (IFRS 16) erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="1e120-108">Bei einem geänderten Mietvertrag kann dieses Konto entweder belastet oder gutgeschrieben werden, je nachdem, ob die Änderung die Mietverbindlichkeit erhöht oder verringert.</span><span class="sxs-lookup"><span data-stu-id="1e120-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="1e120-109">**Beispieljournaleinträge:** Erstmalige Erfassung</span><span class="sxs-lookup"><span data-stu-id="1e120-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="1e120-110">**Soll:** Mietanlage XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="1e120-111">**Haben:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="1e120-112">Leasingverbindlichkeit</span><span class="sxs-lookup"><span data-stu-id="1e120-112">Lease liability</span></span>

<span data-ttu-id="1e120-113">Das Konto ist mit der Leasingverbindlichkeit verbunden, die entsteht, wenn Zahlungen nach den neuen Standards IFRS 16 und ASC 842 abgezinst werden.</span><span class="sxs-lookup"><span data-stu-id="1e120-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="1e120-114">Dieses Konto wird gutgeschrieben, wenn ein Mietvertrag nach den neuen Standards erstmals anerkannt wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="1e120-115">Es wird für Mietzahlungen belastet und für Zinsabgrenzungen gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e120-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="1e120-116">**Beispieljournaleinträge:** Erstmalige Erfassung</span><span class="sxs-lookup"><span data-stu-id="1e120-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="1e120-117">**Soll:** Mietanlage XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="1e120-118">**Haben:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="1e120-119">**Beispieljournaleinträge:** Zinsabgrenzung</span><span class="sxs-lookup"><span data-stu-id="1e120-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="1e120-120">**Soll:** Zinsausgaben XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="1e120-121">**Haben:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="1e120-122">**Beispieljournaleinträge:** Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="1e120-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="1e120-123">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="1e120-124">**Haben:** Kreditorenzahlung/Leasingzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="1e120-125">Kurzfristige Leasingverbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="1e120-125">Short-term lease liability</span></span>

<span data-ttu-id="1e120-126">Das Konto ist mit der kurzfristigen Leasingverbindlichkeit verbunden, wenn der Journaleintrag für die kurzfristige Leasingverbindlichkeit neu gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="1e120-127">Diesem Konto wird die kurzfristige Verbindlichkeit aus dem Tilgungsplan am letzten Tag des Monats gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e120-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="1e120-128">Der gleiche Betrag wird jedoch am ersten Tag des nächsten Monats abgebucht.</span><span class="sxs-lookup"><span data-stu-id="1e120-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="1e120-129">**Beispieljournaleinträge:** Umgliederung der kurzfristigen Leasingverbindlichkeit</span><span class="sxs-lookup"><span data-stu-id="1e120-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="1e120-130">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="1e120-131">**Haben:** Kurzfristige Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="1e120-132">**Soll:** Kurzfristige Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="1e120-133">**Haben:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="1e120-134">Abschreibungsausgaben</span><span class="sxs-lookup"><span data-stu-id="1e120-134">Depreciation expense</span></span>

<span data-ttu-id="1e120-135">Das Konto ist mit dem Aufwand verbunden, der im Zusammenhang mit der Abschreibung des Nutzungsrecht am Leasingobjekt nach IFRS 16, ASC 842 und Finanzierungsleasing nach IAS 17 und ASC 840 steht.</span><span class="sxs-lookup"><span data-stu-id="1e120-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="1e120-136">Dieses Konto wird belastet, wenn ein Nutzungsrecht am Leasingobjekt jeden Monat abgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="1e120-137">**Beispieljournaleinträge:** Abschreibungsabgrenzung</span><span class="sxs-lookup"><span data-stu-id="1e120-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="1e120-138">**Soll:** Abschreibungsausgaben XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="1e120-139">**Haben:** Kumulierte Abschreibung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="1e120-140">Gewinn/Verlust bei Änderung des Mietvertrags</span><span class="sxs-lookup"><span data-stu-id="1e120-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="1e120-141">Das Konto ist mit Gewinnen oder Verlusten verbunden, die sich aus Mietvertragsänderungen ergeben.</span><span class="sxs-lookup"><span data-stu-id="1e120-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="1e120-142">Ein Gewinn kann während einer Mietvertragsänderung entstehen, wenn die Änderung die Leasingverbindlichkeit um einen Betrag verringert, der den Buchwert des Nutzungsrecht am Leasingobjekts übersteigt.</span><span class="sxs-lookup"><span data-stu-id="1e120-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="1e120-143">Beispielsweise hat ein Mietvertrag einen aktuellen Buchwert der Leasingverbindlichkeit von 150.000 USD und einen Buchwert des Nutzungsrecht am Leasingobjekts von 100.000 USD.</span><span class="sxs-lookup"><span data-stu-id="1e120-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="1e120-144">Der mietvertrag wird geändert, und diese Änderung ergibt einen neuen Barwert der zukünftigen Mindestleasingzahlungen (PVFMLP) von 40.000 USD.</span><span class="sxs-lookup"><span data-stu-id="1e120-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="1e120-145">Daher wird die Leasingverbindlichkeit von 110.000 USD (150.000 USD – 40.000 USD) belastet.</span><span class="sxs-lookup"><span data-stu-id="1e120-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="1e120-146">Da das Nutzungsrecht am Leasingobjekt nur 100.000 USD ist, verringert die Verringerung von 110.000 USD der Anlage nach 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="1e120-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="1e120-147">In den Bilanzierungsrichtlinien heißt es daher, dass der Rest auf ein Gewinnkonto gebucht werden sollte.</span><span class="sxs-lookup"><span data-stu-id="1e120-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="1e120-148">In diesem Fall ist der endgültige Journaleintrag eine Belastung der Leasingverbindlichkeit für 110.000 USD, eine Gutschrift für das Mietobjekt für 100.000 USD und eine Gutschrift für das Gewinnkonto für 10.000 USD.</span><span class="sxs-lookup"><span data-stu-id="1e120-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="1e120-149">**Beispieljournaleinträge:** Mietvertragsänderungen</span><span class="sxs-lookup"><span data-stu-id="1e120-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="1e120-150">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="1e120-151">**Haben:** Mietanlage XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="1e120-152">**Haben:** Gewinn XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="1e120-153">Kumulierte Abschreibung</span><span class="sxs-lookup"><span data-stu-id="1e120-153">Accumulated depreciation</span></span>

<span data-ttu-id="1e120-154">Das Konto ist dem Gegen-Anlagenkonto des Nutzungsrecht am Leasingobjekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1e120-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="1e120-155">Auf diesem Konto erfolgt beim Buchen einer Abschreibungsausgabe eine Habenbuchung.</span><span class="sxs-lookup"><span data-stu-id="1e120-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="1e120-156">**Beispieljournaleinträge:** Abschreibungsabgrenzung</span><span class="sxs-lookup"><span data-stu-id="1e120-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="1e120-157">**Soll:** Abschreibungsausgaben XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="1e120-158">**Haben:** Kumulierte Abschreibung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="1e120-159">Nicht ausgeschüttete Gewinne</span><span class="sxs-lookup"><span data-stu-id="1e120-159">Retained earnings</span></span>

<span data-ttu-id="1e120-160">Das den Anfangssalden zugeordnete Konto.</span><span class="sxs-lookup"><span data-stu-id="1e120-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="1e120-161">Dieses Konto kann entweder in einem Journaleintrag für die Übergangsregulierung unter Verwendung der vollständigen retrospektiven Methode oder der Methode der kumulativen Nachholoption A belastet oder gutgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1e120-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="1e120-162">Die Differenz zwischen dem anfänglichen Nutzungsrecht am Leasingobjekt und der Leasingverbindlichkeit wird in den Gewinnrücklagen verbucht.</span><span class="sxs-lookup"><span data-stu-id="1e120-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="1e120-163">In seltenen Fällen können die Gewinnrücklagen auch während der Änderung des Mieterhältnisses beeinflusst werden, wenn die Klassifizierung eines Mietvertrags von „Finanzierung“ in„Betrieb“ geändert wird, um den ROU-Vermögenswert so hoch oder runter zu schreiben, dass er der Leasingverbindlichkeit entspricht.</span><span class="sxs-lookup"><span data-stu-id="1e120-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="1e120-164">**Beispieljournaleinträge:** Übergangsregulierung (vollständige retrospektive oder kumulative Nachholoption A-Methode)</span><span class="sxs-lookup"><span data-stu-id="1e120-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="1e120-165">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="1e120-166">**Haben:** Mietanlage XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="1e120-167">**Haben:** Nicht ausgeschüttete Gewinne XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="1e120-168">Variable Zahlung</span><span class="sxs-lookup"><span data-stu-id="1e120-168">Variable payment</span></span>

<span data-ttu-id="1e120-169">Das Konto ist mit variablen Mietzahlungen verbunden, die durch eine Indexneubewertung gemäß Mietverträgen nach ASC 842, ASC 840 und IAS 17 erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="1e120-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="1e120-170">Im Mietzahlungsplan sind variable Zahlungen in der Spalte **Variable Zahlung** enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e120-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="1e120-171">Dieses Konto wird belastet, wenn eine Rechnung für eine Zahlungsplanzeile erstellt wird, die eine variable Zahlung enthält.</span><span class="sxs-lookup"><span data-stu-id="1e120-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="1e120-172">**Beispieljournaleinträge:** Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="1e120-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="1e120-173">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="1e120-174">**Soll:** Variable Zahlung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="1e120-175">**Haben:** Kreditorenzahlung/Leasingzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="1e120-176">Zurückgestellter Mietaufwand für Anlage (Verbindlichkeit)</span><span class="sxs-lookup"><span data-stu-id="1e120-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="1e120-177">Das Konto ist mit der Forderung des zurückgestellten Mietaufwands oder der Verbindlichkeit aus einem Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand verbunden.</span><span class="sxs-lookup"><span data-stu-id="1e120-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="1e120-178">Dieses Konto wird belastet, wenn eine Rechnung gegen ein Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand gebucht wird, wenn der Mietzahlungsbetrag den linearen Mietaufwand des Zeitraums übersteigt.</span><span class="sxs-lookup"><span data-stu-id="1e120-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="1e120-179">Es wird gutgeschrieben, wenn die Mietzahlung unter dem linearen Mietaufwand des Zeitraums liegt.</span><span class="sxs-lookup"><span data-stu-id="1e120-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="1e120-180">**Beispieljournaleinträge:** Mietzahlung (Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand)</span><span class="sxs-lookup"><span data-stu-id="1e120-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="1e120-181">**Soll:** Mietkosten XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="1e120-182">**Haben:** Zurückgestellter Mietaufwand für Verbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="1e120-183">**Haben:** Kreditorenzahlung/Leasingzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="1e120-184">Mietvertragsausgaben</span><span class="sxs-lookup"><span data-stu-id="1e120-184">Lease expense</span></span>

<span data-ttu-id="1e120-185">Das Konto ist mit dem Mietaufwand verbunden, wenn der Mietvertrag als Mietvertrag mit Behandlung von zurückgestellem Mietaufwand eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="1e120-186">Dieses Konto wird belastet, wenn eine Rechnung gegen ein Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="1e120-187">**Beispieljournaleinträge:** Mietzahlung (Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand)</span><span class="sxs-lookup"><span data-stu-id="1e120-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="1e120-188">**Soll:** Mietkosten XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="1e120-189">**Haben:** Zurückgestellter Mietaufwand für Verbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="1e120-190">**Haben:** Kreditorenzahlung/Leasingzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="1e120-191">Aufwand der dauerhaften Wertminderung</span><span class="sxs-lookup"><span data-stu-id="1e120-191">Impairment expense</span></span>

<span data-ttu-id="1e120-192">Das Konto wird gebucht, wenn ein Mietvertrag wertgemindert ist.</span><span class="sxs-lookup"><span data-stu-id="1e120-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="1e120-193">Dieses Konto wird belastet, während das Konto für das Nutzungsrecht am Leasingobjekt direkt gutgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="1e120-194">**Beispieljournaleinträge:** Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="1e120-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="1e120-195">**Soll:** Aufwand der dauerhaften Wertminderung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="1e120-196">**Haben:** Nutzungsrecht am Leasingobjekt XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="1e120-197">Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="1e120-197">Lease payment</span></span>

<span data-ttu-id="1e120-198">Das Konto wird gegen gebucht, wenn der **An Kreditor bezahlen**-Parameter ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="1e120-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="1e120-199">Dieses Konto wird anstelle des Kreditors gutgeschrieben, wenn der Parameter deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1e120-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="1e120-200">**Beispieljournaleinträge:** Mietzahlung</span><span class="sxs-lookup"><span data-stu-id="1e120-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="1e120-201">**Soll:** Leasingverbindlichkeit XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="1e120-202">**Haben:** Mietzahlung XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="1e120-203">Buchungen des Ausgabentyps</span><span class="sxs-lookup"><span data-stu-id="1e120-203">Expense type postings</span></span>

<span data-ttu-id="1e120-204">Das für jede Ausgabenart ausgewählte Konto wird belastet, wenn eine Zahlung für diese Ausgabenart generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="1e120-205">Zum Beispiel wird das Konto, das für die Kostenart **Versicherung** angegeben ist, immer dann belastet, wenn eine Rechnung oder ein Zahlungsjournaleintrag aus dem Plan für Nebenkosten beim Leasing bei Versicherungskosten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1e120-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="1e120-206">**Beispieljournaleinträge:** Versicherungszahlung</span><span class="sxs-lookup"><span data-stu-id="1e120-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="1e120-207">**Soll:** Versicherungskostenartkonto XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="1e120-208">**Haben:** Gegenkonto XXX</span><span class="sxs-lookup"><span data-stu-id="1e120-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="1e120-209">Das Gegenkonto wird auf Mietvertragsebene in den Zeilen für den Zahlungsplan für die Nebenkosten beim Leasing ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="1e120-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="1e120-210">Dieses Gegenkonto kann dem Kreditor oder einem Sachkonto zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="1e120-210">This offset account can associated with the vendor, or with a ledger account.</span></span>
