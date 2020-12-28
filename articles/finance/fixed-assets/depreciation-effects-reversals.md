---
title: Abschreibungseffekte bei Rückbuchungen
description: Dieser Artikel behandelt mögliche Auswirkung beim Stornieren einer Anlagentransaktion.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443460"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="c80e6-103">Abschreibungseffekte bei Rückbuchungen</span><span class="sxs-lookup"><span data-stu-id="c80e6-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c80e6-104">Dieser Artikel behandelt mögliche Auswirkung beim Stornieren einer Anlagentransaktion.</span><span class="sxs-lookup"><span data-stu-id="c80e6-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="c80e6-105">Anlagenbuchungen können storniert werden. Gleiches gilt für die Buchungen, die einer Anlage zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c80e6-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="c80e6-106">Darüber hinaus besteht die Möglichkeit zum Widerrufen stornierter Buchungen.</span><span class="sxs-lookup"><span data-stu-id="c80e6-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="c80e6-107">Sie können eine Buchung stornieren oder widerrufen, bei der es sich nicht um den Posten handelt, der zuletzt in das Wertmodell oder in das Abschreibungsbuch der Anlage gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="c80e6-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="c80e6-108">Prüfen Sie in diesem Fall zunächst, ob nach der zu stornierenden Buchungen bereits Abschreibungsbuchungen erfolgt sind.</span><span class="sxs-lookup"><span data-stu-id="c80e6-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="c80e6-109">Dieser Schritt ist erforderlich, da Abschreibungen beim Stornieren einer Buchung nicht neu berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="c80e6-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="c80e6-110">Aus diesem Grund ist die Abschreibung nach einer Stornierung häufig zu hoch oder zu niedrig bewertet, was in den entsprechenden Beispielen veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="c80e6-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="c80e6-111">Wenn eine Meldung mit dem Hinweis angezeigt wird, dass keine Neuberechnung der Abschreibung stattfindet, setzen Sie den Stornovorgang nicht fort, um eine korrekte Abschreibung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="c80e6-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="c80e6-112">Stornieren Sie stattdessen zunächst die Abschreibungsbuchung, die nach der zu stornierenden Buchung erfolgt ist, und setzen Sie dann den eigentlichen Stornovorgang fort.</span><span class="sxs-lookup"><span data-stu-id="c80e6-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="c80e6-113">Sie erhalten keinen Hinweis zur Neuberechnung der Abschreibung, und die Stornierung kann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c80e6-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="c80e6-114">In den folgenden Beispielen werden die Berechnungen veranschaulicht, die ausgeführt werden, wenn der Vorgang ungeachtet der Warnmeldung und ohne vorherige Stornierung der Abschreibungsbuchungen fortgesetzt wird:</span><span class="sxs-lookup"><span data-stu-id="c80e6-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="c80e6-115">Beispiel 1: Zu hohe Bewertung der Abschreibung</span><span class="sxs-lookup"><span data-stu-id="c80e6-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="c80e6-116">Eine Anlage ist mit einer Nutzungsdauer von fünf Jahren und mit einer linearen Abschreibung (60 Abschreibungsperioden) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c80e6-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="c80e6-117">In diesem Beispiel ergibt sich eine zu hohe Bewertung der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="c80e6-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="c80e6-118">Anlagenbuchungshistorie</span><span class="sxs-lookup"><span data-stu-id="c80e6-118">Asset transaction history</span></span>

| <span data-ttu-id="c80e6-119">Datum</span><span class="sxs-lookup"><span data-stu-id="c80e6-119">Date</span></span>       | <span data-ttu-id="c80e6-120">Buchungstyp</span><span class="sxs-lookup"><span data-stu-id="c80e6-120">Transaction type</span></span>                                                          | <span data-ttu-id="c80e6-121">Betrag</span><span class="sxs-lookup"><span data-stu-id="c80e6-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c80e6-122">1. Januar</span><span class="sxs-lookup"><span data-stu-id="c80e6-122">January 1</span></span>  | <span data-ttu-id="c80e6-123">Anschaffung</span><span class="sxs-lookup"><span data-stu-id="c80e6-123">Acquisition</span></span>                                                               | <span data-ttu-id="c80e6-124">59.000,00</span><span class="sxs-lookup"><span data-stu-id="c80e6-124">59,000.00</span></span>                                 |
| <span data-ttu-id="c80e6-125">1. Januar</span><span class="sxs-lookup"><span data-stu-id="c80e6-125">January 1</span></span>  | <span data-ttu-id="c80e6-126">Anschaffungsänderung</span><span class="sxs-lookup"><span data-stu-id="c80e6-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="c80e6-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c80e6-127">1,000.00</span></span>                                  |
| <span data-ttu-id="c80e6-128">31. Januar</span><span class="sxs-lookup"><span data-stu-id="c80e6-128">January 31</span></span> | <span data-ttu-id="c80e6-129">Abschreibung (unter Verwendung eines Vorschlags für eine Abschreibungsperiode)</span><span class="sxs-lookup"><span data-stu-id="c80e6-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="c80e6-130">1.000,00; Berechnung: Buchwert (59.000 + 1.000) / Anzahl der verbleibenden Abschreibungsperioden (60)</span><span class="sxs-lookup"><span data-stu-id="c80e6-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="c80e6-131">Storno</span><span class="sxs-lookup"><span data-stu-id="c80e6-131">Reversal action</span></span>

| <span data-ttu-id="c80e6-132">Datum</span><span class="sxs-lookup"><span data-stu-id="c80e6-132">Date</span></span>      | <span data-ttu-id="c80e6-133">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="c80e6-133">Transaction type</span></span>                | <span data-ttu-id="c80e6-134">Betrag</span><span class="sxs-lookup"><span data-stu-id="c80e6-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="c80e6-135">1. Januar</span><span class="sxs-lookup"><span data-stu-id="c80e6-135">January 1</span></span> | <span data-ttu-id="c80e6-136">Storno der Anschaffungsänderung</span><span class="sxs-lookup"><span data-stu-id="c80e6-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="c80e6-137">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="c80e6-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="c80e6-138">Abschreibungseffekt</span><span class="sxs-lookup"><span data-stu-id="c80e6-138">Depreciation effect</span></span>

| <span data-ttu-id="c80e6-139">Datum</span><span class="sxs-lookup"><span data-stu-id="c80e6-139">Date</span></span>        | <span data-ttu-id="c80e6-140">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="c80e6-140">Transaction type</span></span>        | <span data-ttu-id="c80e6-141">Betrag</span><span class="sxs-lookup"><span data-stu-id="c80e6-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c80e6-142">28. Februar</span><span class="sxs-lookup"><span data-stu-id="c80e6-142">February 28</span></span> | <span data-ttu-id="c80e6-143">Abschreibung (Vorschlag)</span><span class="sxs-lookup"><span data-stu-id="c80e6-143">Depreciation (proposal)</span></span> | <span data-ttu-id="c80e6-144">983,05; Berechnung: Buchwert (59.000 - 1.000 Abschreibung) / Anzahl der verbleibenden Abschreibungsperioden (59)</span><span class="sxs-lookup"><span data-stu-id="c80e6-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="c80e6-145">Die Abschreibung ist um 16,95 (1.000 - 983,05) zu hoch bewertet.</span><span class="sxs-lookup"><span data-stu-id="c80e6-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="c80e6-146">Beispiel 2: Zu niedrige Bewertung der Abschreibung</span><span class="sxs-lookup"><span data-stu-id="c80e6-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="c80e6-147">Eine Anlage ist mit einer Nutzungsdauer von fünf Jahren und mit einer linearen Abschreibung (60 Abschreibungsperioden) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c80e6-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="c80e6-148">In diesem Beispiel ergibt sich eine zu niedrige Bewertung der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="c80e6-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="c80e6-149">Anlagenbuchungshistorie</span><span class="sxs-lookup"><span data-stu-id="c80e6-149">Asset transaction history</span></span>

| <span data-ttu-id="c80e6-150">Datum</span><span class="sxs-lookup"><span data-stu-id="c80e6-150">Date</span></span>       | <span data-ttu-id="c80e6-151">Buchungsart</span><span class="sxs-lookup"><span data-stu-id="c80e6-151">Transaction type</span></span>                                                          | <span data-ttu-id="c80e6-152">Betrag</span><span class="sxs-lookup"><span data-stu-id="c80e6-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="c80e6-153">1. Januar</span><span class="sxs-lookup"><span data-stu-id="c80e6-153">January 1</span></span>  | <span data-ttu-id="c80e6-154">Anschaffung</span><span class="sxs-lookup"><span data-stu-id="c80e6-154">Acquisition</span></span>                                                               | <span data-ttu-id="c80e6-155">59.000,00</span><span class="sxs-lookup"><span data-stu-id="c80e6-155">59,000.00</span></span>                                   |
| <span data-ttu-id="c80e6-156">1. Januar</span><span class="sxs-lookup"><span data-stu-id="c80e6-156">January 1</span></span>  | <span data-ttu-id="c80e6-157">Regulierung vom Typ "Niedrigerbewertung"</span><span class="sxs-lookup"><span data-stu-id="c80e6-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="c80e6-158">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c80e6-158">1,000.00</span></span>                                    |
| <span data-ttu-id="c80e6-159">31. Januar</span><span class="sxs-lookup"><span data-stu-id="c80e6-159">January 31</span></span> | <span data-ttu-id="c80e6-160">Abschreibung (unter Verwendung eines Vorschlags für eine Abschreibungsperiode)</span><span class="sxs-lookup"><span data-stu-id="c80e6-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="c80e6-161">966,67; Berechnung: Buchwert (59.000 – 1.000) / Anzahl der verbleibenden Abschreibungsperioden (60)</span><span class="sxs-lookup"><span data-stu-id="c80e6-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="c80e6-162">Storno</span><span class="sxs-lookup"><span data-stu-id="c80e6-162">Reversal action</span></span>

| <span data-ttu-id="c80e6-163">Datum</span><span class="sxs-lookup"><span data-stu-id="c80e6-163">Date</span></span>      | <span data-ttu-id="c80e6-164">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="c80e6-164">Transaction type</span></span>               | <span data-ttu-id="c80e6-165">Betrag</span><span class="sxs-lookup"><span data-stu-id="c80e6-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="c80e6-166">1. Januar</span><span class="sxs-lookup"><span data-stu-id="c80e6-166">January 1</span></span> | <span data-ttu-id="c80e6-167">Storno der Regulierung vom Typ "Niedrigerbewertung"</span><span class="sxs-lookup"><span data-stu-id="c80e6-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="c80e6-168">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="c80e6-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="c80e6-169">Abschreibungseffekt</span><span class="sxs-lookup"><span data-stu-id="c80e6-169">Depreciation effect</span></span>

| <span data-ttu-id="c80e6-170">Datum</span><span class="sxs-lookup"><span data-stu-id="c80e6-170">Date</span></span>        | <span data-ttu-id="c80e6-171">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="c80e6-171">Transaction type</span></span>        | <span data-ttu-id="c80e6-172">Betrag</span><span class="sxs-lookup"><span data-stu-id="c80e6-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c80e6-173">28. Februar</span><span class="sxs-lookup"><span data-stu-id="c80e6-173">February 28</span></span> | <span data-ttu-id="c80e6-174">Abschreibung (Vorschlag)</span><span class="sxs-lookup"><span data-stu-id="c80e6-174">Depreciation (proposal)</span></span> | <span data-ttu-id="c80e6-175">983,62; Berechnung: Buchwert (59.000 - 966,67 Abschreibung) / Anzahl der verbleibenden Abschreibungsperioden (59)</span><span class="sxs-lookup"><span data-stu-id="c80e6-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="c80e6-176">Die Abschreibung ist um 16,95 (983,62 - 966,67) zu niedrig bewertet.</span><span class="sxs-lookup"><span data-stu-id="c80e6-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="c80e6-177">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c80e6-177">Additional resources</span></span>
--------

[<span data-ttu-id="c80e6-178">Anlagenabschreibung</span><span class="sxs-lookup"><span data-stu-id="c80e6-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



