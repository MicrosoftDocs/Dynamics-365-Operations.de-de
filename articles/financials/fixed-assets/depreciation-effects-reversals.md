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
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840600"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="6a1fe-103">Abschreibungseffekte bei Rückbuchungen</span><span class="sxs-lookup"><span data-stu-id="6a1fe-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a1fe-104">Dieser Artikel behandelt mögliche Auswirkung beim Stornieren einer Anlagentransaktion.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="6a1fe-105">Anlagenbuchungen können storniert werden. Gleiches gilt für die Buchungen, die einer Anlage zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="6a1fe-106">Darüber hinaus besteht die Möglichkeit zum Widerrufen stornierter Buchungen.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="6a1fe-107">Sie können eine Buchung stornieren oder widerrufen, bei der es sich nicht um den Posten handelt, der zuletzt in das Wertmodell oder in das Abschreibungsbuch der Anlage gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="6a1fe-108">Prüfen Sie in diesem Fall zunächst, ob nach der zu stornierenden Buchungen bereits Abschreibungsbuchungen erfolgt sind.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="6a1fe-109">Dieser Schritt ist erforderlich, da Abschreibungen beim Stornieren einer Buchung nicht neu berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="6a1fe-110">Aus diesem Grund ist die Abschreibung nach einer Stornierung häufig zu hoch oder zu niedrig bewertet, was in den entsprechenden Beispielen veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="6a1fe-111">Wenn eine Meldung mit dem Hinweis angezeigt wird, dass keine Neuberechnung der Abschreibung stattfindet, setzen Sie den Stornovorgang nicht fort, um eine korrekte Abschreibung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="6a1fe-112">Stornieren Sie stattdessen zunächst die Abschreibungsbuchung, die nach der zu stornierenden Buchung erfolgt ist, und setzen Sie dann den eigentlichen Stornovorgang fort.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="6a1fe-113">Sie erhalten keinen Hinweis zur Neuberechnung der Abschreibung, und die Stornierung kann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="6a1fe-114">In den folgenden Beispielen werden die Berechnungen veranschaulicht, die ausgeführt werden, wenn der Vorgang ungeachtet der Warnmeldung und ohne vorherige Stornierung der Abschreibungsbuchungen fortgesetzt wird:</span><span class="sxs-lookup"><span data-stu-id="6a1fe-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="6a1fe-115">Beispiel 1: Zu hohe Bewertung der Abschreibung</span><span class="sxs-lookup"><span data-stu-id="6a1fe-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="6a1fe-116">Eine Anlage ist mit einer Nutzungsdauer von fünf Jahren und mit einer linearen Abschreibung (60 Abschreibungsperioden) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6a1fe-117">In diesem Beispiel ergibt sich eine zu hohe Bewertung der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6a1fe-118">Anlagenbuchungshistorie</span><span class="sxs-lookup"><span data-stu-id="6a1fe-118">Asset transaction history</span></span>

| <span data-ttu-id="6a1fe-119">Datum</span><span class="sxs-lookup"><span data-stu-id="6a1fe-119">Date</span></span>       | <span data-ttu-id="6a1fe-120">Buchungstyp</span><span class="sxs-lookup"><span data-stu-id="6a1fe-120">Transaction type</span></span>                                                          | <span data-ttu-id="6a1fe-121">Betrag</span><span class="sxs-lookup"><span data-stu-id="6a1fe-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6a1fe-122">1. Januar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-122">January 1</span></span>  | <span data-ttu-id="6a1fe-123">Anschaffung</span><span class="sxs-lookup"><span data-stu-id="6a1fe-123">Acquisition</span></span>                                                               | <span data-ttu-id="6a1fe-124">59.000,00</span><span class="sxs-lookup"><span data-stu-id="6a1fe-124">59,000.00</span></span>                                 |
| <span data-ttu-id="6a1fe-125">1. Januar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-125">January 1</span></span>  | <span data-ttu-id="6a1fe-126">Anschaffungsänderung</span><span class="sxs-lookup"><span data-stu-id="6a1fe-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="6a1fe-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6a1fe-127">1,000.00</span></span>                                  |
| <span data-ttu-id="6a1fe-128">31. Januar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-128">January 31</span></span> | <span data-ttu-id="6a1fe-129">Abschreibung (unter Verwendung eines Vorschlags für eine Abschreibungsperiode)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6a1fe-130">1.000,00; Berechnung: Buchwert (59.000 + 1.000) / Anzahl der verbleibenden Abschreibungsperioden (60)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6a1fe-131">Storno</span><span class="sxs-lookup"><span data-stu-id="6a1fe-131">Reversal action</span></span>

| <span data-ttu-id="6a1fe-132">Datum</span><span class="sxs-lookup"><span data-stu-id="6a1fe-132">Date</span></span>      | <span data-ttu-id="6a1fe-133">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="6a1fe-133">Transaction type</span></span>                | <span data-ttu-id="6a1fe-134">Betrag</span><span class="sxs-lookup"><span data-stu-id="6a1fe-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="6a1fe-135">1. Januar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-135">January 1</span></span> | <span data-ttu-id="6a1fe-136">Storno der Anschaffungsänderung</span><span class="sxs-lookup"><span data-stu-id="6a1fe-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="6a1fe-137">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="6a1fe-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6a1fe-138">Abschreibungseffekt</span><span class="sxs-lookup"><span data-stu-id="6a1fe-138">Depreciation effect</span></span>

| <span data-ttu-id="6a1fe-139">Datum</span><span class="sxs-lookup"><span data-stu-id="6a1fe-139">Date</span></span>        | <span data-ttu-id="6a1fe-140">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="6a1fe-140">Transaction type</span></span>        | <span data-ttu-id="6a1fe-141">Betrag</span><span class="sxs-lookup"><span data-stu-id="6a1fe-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1fe-142">28. Februar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-142">February 28</span></span> | <span data-ttu-id="6a1fe-143">Abschreibung (Vorschlag)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-143">Depreciation (proposal)</span></span> | <span data-ttu-id="6a1fe-144">983,05; Berechnung: Buchwert (59.000 - 1.000 Abschreibung) / Anzahl der verbleibenden Abschreibungsperioden (59)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6a1fe-145">Die Abschreibung ist um 16,95 (1.000 - 983,05) zu hoch bewertet.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="6a1fe-146">Beispiel 2: Zu niedrige Bewertung der Abschreibung</span><span class="sxs-lookup"><span data-stu-id="6a1fe-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="6a1fe-147">Eine Anlage ist mit einer Nutzungsdauer von fünf Jahren und mit einer linearen Abschreibung (60 Abschreibungsperioden) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6a1fe-148">In diesem Beispiel ergibt sich eine zu niedrige Bewertung der Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6a1fe-149">Anlagenbuchungshistorie</span><span class="sxs-lookup"><span data-stu-id="6a1fe-149">Asset transaction history</span></span>

| <span data-ttu-id="6a1fe-150">Datum</span><span class="sxs-lookup"><span data-stu-id="6a1fe-150">Date</span></span>       | <span data-ttu-id="6a1fe-151">Buchungsart</span><span class="sxs-lookup"><span data-stu-id="6a1fe-151">Transaction type</span></span>                                                          | <span data-ttu-id="6a1fe-152">Betrag</span><span class="sxs-lookup"><span data-stu-id="6a1fe-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="6a1fe-153">1. Januar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-153">January 1</span></span>  | <span data-ttu-id="6a1fe-154">Anschaffung</span><span class="sxs-lookup"><span data-stu-id="6a1fe-154">Acquisition</span></span>                                                               | <span data-ttu-id="6a1fe-155">59.000,00</span><span class="sxs-lookup"><span data-stu-id="6a1fe-155">59,000.00</span></span>                                   |
| <span data-ttu-id="6a1fe-156">1. Januar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-156">January 1</span></span>  | <span data-ttu-id="6a1fe-157">Regulierung vom Typ "Niedrigerbewertung"</span><span class="sxs-lookup"><span data-stu-id="6a1fe-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="6a1fe-158">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6a1fe-158">1,000.00</span></span>                                    |
| <span data-ttu-id="6a1fe-159">31. Januar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-159">January 31</span></span> | <span data-ttu-id="6a1fe-160">Abschreibung (unter Verwendung eines Vorschlags für eine Abschreibungsperiode)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6a1fe-161">966,67; Berechnung: Buchwert (59.000 – 1.000) / Anzahl der verbleibenden Abschreibungsperioden (60)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6a1fe-162">Storno</span><span class="sxs-lookup"><span data-stu-id="6a1fe-162">Reversal action</span></span>

| <span data-ttu-id="6a1fe-163">Datum</span><span class="sxs-lookup"><span data-stu-id="6a1fe-163">Date</span></span>      | <span data-ttu-id="6a1fe-164">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="6a1fe-164">Transaction type</span></span>               | <span data-ttu-id="6a1fe-165">Betrag</span><span class="sxs-lookup"><span data-stu-id="6a1fe-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="6a1fe-166">1. Januar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-166">January 1</span></span> | <span data-ttu-id="6a1fe-167">Storno der Regulierung vom Typ "Niedrigerbewertung"</span><span class="sxs-lookup"><span data-stu-id="6a1fe-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="6a1fe-168">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="6a1fe-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6a1fe-169">Abschreibungseffekt</span><span class="sxs-lookup"><span data-stu-id="6a1fe-169">Depreciation effect</span></span>

| <span data-ttu-id="6a1fe-170">Datum</span><span class="sxs-lookup"><span data-stu-id="6a1fe-170">Date</span></span>        | <span data-ttu-id="6a1fe-171">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="6a1fe-171">Transaction type</span></span>        | <span data-ttu-id="6a1fe-172">Betrag</span><span class="sxs-lookup"><span data-stu-id="6a1fe-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1fe-173">28. Februar</span><span class="sxs-lookup"><span data-stu-id="6a1fe-173">February 28</span></span> | <span data-ttu-id="6a1fe-174">Abschreibung (Vorschlag)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-174">Depreciation (proposal)</span></span> | <span data-ttu-id="6a1fe-175">983,62; Berechnung: Buchwert (59.000 - 966,67 Abschreibung) / Anzahl der verbleibenden Abschreibungsperioden (59)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6a1fe-176">Die Abschreibung ist um 16,95 (983,62 - 966,67) zu niedrig bewertet.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="6a1fe-177">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a1fe-177">Additional resources</span></span>
--------

[<span data-ttu-id="6a1fe-178">Anlagenabschreibung</span><span class="sxs-lookup"><span data-stu-id="6a1fe-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



