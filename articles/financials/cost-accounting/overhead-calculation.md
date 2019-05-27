---
title: Gemeinkostenberechnung
description: In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544054"
---
# <a name="overhead-calculation"></a><span data-ttu-id="64e41-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="64e41-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64e41-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="64e41-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="64e41-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="64e41-105">Term definition</span></span>
---------------

<span data-ttu-id="64e41-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="64e41-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="64e41-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="64e41-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="64e41-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="64e41-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="64e41-109">Miete</span><span class="sxs-lookup"><span data-stu-id="64e41-109">Rent</span></span>
-   <span data-ttu-id="64e41-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-110">Electricity</span></span>
-   <span data-ttu-id="64e41-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="64e41-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="64e41-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="64e41-112">Overhead calculation overview</span></span>
<span data-ttu-id="64e41-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64e41-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="64e41-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="64e41-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="64e41-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="64e41-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="64e41-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="64e41-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="64e41-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64e41-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="64e41-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="64e41-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="64e41-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="64e41-119">Version type</span></span>
-   <span data-ttu-id="64e41-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="64e41-120">Date and time</span></span>
-   <span data-ttu-id="64e41-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="64e41-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="64e41-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="64e41-122">Fiscal year</span></span>
-   <span data-ttu-id="64e41-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="64e41-123">Fiscal period</span></span>

<span data-ttu-id="64e41-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64e41-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="64e41-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="64e41-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="64e41-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="64e41-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="64e41-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="64e41-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="64e41-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="64e41-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="64e41-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="64e41-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="64e41-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="64e41-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="64e41-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="64e41-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="64e41-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="64e41-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="64e41-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="64e41-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="64e41-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="64e41-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="64e41-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="64e41-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="64e41-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="64e41-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="64e41-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="64e41-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="64e41-140">Main account</span></span></th>
<th><span data-ttu-id="64e41-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="64e41-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="64e41-143">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-143">CC099</span></span></td>
<td><span data-ttu-id="64e41-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-144">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-145">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-145">10001</span></span></td>
<td><span data-ttu-id="64e41-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-146">Electricity</span></span></td>
<td><span data-ttu-id="64e41-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="64e41-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="64e41-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="64e41-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="64e41-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="64e41-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="64e41-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="64e41-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="64e41-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="64e41-151">Define the cost behavior rule</span></span>

<span data-ttu-id="64e41-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="64e41-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="64e41-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="64e41-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="64e41-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="64e41-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="64e41-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="64e41-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="64e41-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="64e41-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="64e41-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="64e41-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="64e41-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="64e41-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="64e41-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="64e41-160">Journal</span></span></th>
<th><span data-ttu-id="64e41-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="64e41-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="64e41-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="64e41-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="64e41-163">Version</span><span class="sxs-lookup"><span data-stu-id="64e41-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-164">00001</span><span class="sxs-lookup"><span data-stu-id="64e41-164">00001</span></span></td>
<td><span data-ttu-id="64e41-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="64e41-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="64e41-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="64e41-166">Fiscal</span></span></td>
<td><span data-ttu-id="64e41-167">2017</span><span class="sxs-lookup"><span data-stu-id="64e41-167">2017</span></span></td>
<td><span data-ttu-id="64e41-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="64e41-168">Period 1</span></span></td>
<td><span data-ttu-id="64e41-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="64e41-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="64e41-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="64e41-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-173">Cost element</span></span></th>
<th><span data-ttu-id="64e41-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-174">Cost behavior</span></span></th>
<th><span data-ttu-id="64e41-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="64e41-177">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-177">CC099</span></span></td>
<td><span data-ttu-id="64e41-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-178">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-179">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-179">10001</span></span></td>
<td><span data-ttu-id="64e41-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-180">Electricity</span></span></td>
<td><span data-ttu-id="64e41-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="64e41-181">Unclassified</span></span></td>
<td><span data-ttu-id="64e41-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="64e41-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="64e41-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="64e41-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-185">Cost element</span></span></th>
<th><span data-ttu-id="64e41-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-186">Cost behavior</span></span></th>
<th><span data-ttu-id="64e41-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-187">Amount</span></span></th>
<th><span data-ttu-id="64e41-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-189">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-189">CC099</span></span></td>
<td><span data-ttu-id="64e41-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-190">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-191">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-191">10001</span></span></td>
<td><span data-ttu-id="64e41-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-192">Electricity</span></span></td>
<td><span data-ttu-id="64e41-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="64e41-193">Unclassified</span></span></td>
<td><span data-ttu-id="64e41-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="64e41-194">10,000.00</span></span></td>
<td><span data-ttu-id="64e41-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-196">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-196">CC099</span></span></td>
<td><span data-ttu-id="64e41-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-197">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-198">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-198">10001</span></span></td>
<td><span data-ttu-id="64e41-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-199">Electricity</span></span></td>
<td><span data-ttu-id="64e41-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="64e41-200">Unclassified</span></span></td>
<td><span data-ttu-id="64e41-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-201">-10,000.00</span></span></td>
<td><span data-ttu-id="64e41-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-203">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-203">CC099</span></span></td>
<td><span data-ttu-id="64e41-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-204">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-205">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-205">10001</span></span></td>
<td><span data-ttu-id="64e41-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-206">Electricity</span></span></td>
<td><span data-ttu-id="64e41-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-207">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="64e41-208">1,000.00</span></span></td>
<td><span data-ttu-id="64e41-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-210">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-210">CC099</span></span></td>
<td><span data-ttu-id="64e41-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-211">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-212">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-212">10001</span></span></td>
<td><span data-ttu-id="64e41-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-213">Electricity</span></span></td>
<td><span data-ttu-id="64e41-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-214">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="64e41-215">9,000.00</span></span></td>
<td><span data-ttu-id="64e41-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="64e41-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="64e41-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="64e41-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="64e41-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="64e41-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="64e41-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="64e41-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="64e41-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="64e41-221">Define the cost distribution rule</span></span>

<span data-ttu-id="64e41-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="64e41-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="64e41-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="64e41-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="64e41-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="64e41-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="64e41-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="64e41-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="64e41-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="64e41-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="64e41-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64e41-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-228">Cost object</span></span></th>
<th><span data-ttu-id="64e41-229">KWH</span><span class="sxs-lookup"><span data-stu-id="64e41-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-230">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-230">CC001</span></span></td>
<td><span data-ttu-id="64e41-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-231">HR</span></span></td>
<td><span data-ttu-id="64e41-232">1.000</span><span class="sxs-lookup"><span data-stu-id="64e41-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-233">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-233">CC002</span></span></td>
<td><span data-ttu-id="64e41-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-234">Finance</span></span></td>
<td><span data-ttu-id="64e41-235">6.000</span><span class="sxs-lookup"><span data-stu-id="64e41-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-236">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-236">CC003</span></span></td>
<td><span data-ttu-id="64e41-237">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-237">Assembly</span></span></td>
<td><span data-ttu-id="64e41-238">0</span><span class="sxs-lookup"><span data-stu-id="64e41-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="64e41-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-240">Cost object</span></span></th>
<th><span data-ttu-id="64e41-241">Größe</span><span class="sxs-lookup"><span data-stu-id="64e41-241">Magnitude</span></span></th>
<th><span data-ttu-id="64e41-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="64e41-242">Allocation factor</span></span></th>
<th><span data-ttu-id="64e41-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-244">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-244">CC001</span></span></td>
<td><span data-ttu-id="64e41-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-245">HR</span></span></td>
<td><span data-ttu-id="64e41-246">1.000</span><span class="sxs-lookup"><span data-stu-id="64e41-246">1,000</span></span></td>
<td><span data-ttu-id="64e41-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="64e41-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="64e41-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-249">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-249">CC002</span></span></td>
<td><span data-ttu-id="64e41-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-250">Finance</span></span></td>
<td><span data-ttu-id="64e41-251">6.000</span><span class="sxs-lookup"><span data-stu-id="64e41-251">6,000</span></span></td>
<td><span data-ttu-id="64e41-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="64e41-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="64e41-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-254">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-254">CC003</span></span></td>
<td><span data-ttu-id="64e41-255">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-255">Assembly</span></span></td>
<td><span data-ttu-id="64e41-256">0</span><span class="sxs-lookup"><span data-stu-id="64e41-256">0</span></span></td>
<td><span data-ttu-id="64e41-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="64e41-258">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="64e41-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="64e41-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="64e41-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-261">Cost object</span></span></th>
<th><span data-ttu-id="64e41-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="64e41-262">Formula</span></span></th>
<th><span data-ttu-id="64e41-263">Größe</span><span class="sxs-lookup"><span data-stu-id="64e41-263">Magnitude</span></span></th>
<th><span data-ttu-id="64e41-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="64e41-264">Allocation factor</span></span></th>
<th><span data-ttu-id="64e41-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-266">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-266">CC001</span></span></td>
<td><span data-ttu-id="64e41-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-267">HR</span></span></td>
<td><span data-ttu-id="64e41-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="64e41-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="64e41-269">1</span><span class="sxs-lookup"><span data-stu-id="64e41-269">1</span></span></td>
<td><span data-ttu-id="64e41-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="64e41-271">500,00</span><span class="sxs-lookup"><span data-stu-id="64e41-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-272">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-272">CC002</span></span></td>
<td><span data-ttu-id="64e41-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-273">Finance</span></span></td>
<td><span data-ttu-id="64e41-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="64e41-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="64e41-275">1</span><span class="sxs-lookup"><span data-stu-id="64e41-275">1</span></span></td>
<td><span data-ttu-id="64e41-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="64e41-277">500,00</span><span class="sxs-lookup"><span data-stu-id="64e41-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-278">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-278">CC003</span></span></td>
<td><span data-ttu-id="64e41-279">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-279">Assembly</span></span></td>
<td><span data-ttu-id="64e41-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="64e41-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="64e41-281">0</span><span class="sxs-lookup"><span data-stu-id="64e41-281">0</span></span></td>
<td><span data-ttu-id="64e41-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="64e41-283">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="64e41-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="64e41-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="64e41-285">Journal</span></span></th>
<th><span data-ttu-id="64e41-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="64e41-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="64e41-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="64e41-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="64e41-288">Version</span><span class="sxs-lookup"><span data-stu-id="64e41-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-289">00002</span><span class="sxs-lookup"><span data-stu-id="64e41-289">00002</span></span></td>
<td><span data-ttu-id="64e41-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="64e41-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="64e41-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="64e41-291">Fiscal</span></span></td>
<td><span data-ttu-id="64e41-292">2017</span><span class="sxs-lookup"><span data-stu-id="64e41-292">2017</span></span></td>
<td><span data-ttu-id="64e41-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="64e41-293">Period 1</span></span></td>
<td><span data-ttu-id="64e41-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="64e41-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="64e41-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="64e41-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-298">Cost element</span></span></th>
<th><span data-ttu-id="64e41-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-299">Cost behavior</span></span></th>
<th><span data-ttu-id="64e41-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-302">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-302">CC099</span></span></td>
<td><span data-ttu-id="64e41-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-303">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-304">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-304">10001</span></span></td>
<td><span data-ttu-id="64e41-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-305">Electricity</span></span></td>
<td><span data-ttu-id="64e41-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-306">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="64e41-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-309">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-309">CC099</span></span></td>
<td><span data-ttu-id="64e41-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-310">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-311">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-311">10001</span></span></td>
<td><span data-ttu-id="64e41-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-312">Electricity</span></span></td>
<td><span data-ttu-id="64e41-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-313">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="64e41-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="64e41-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="64e41-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-317">Cost element</span></span></th>
<th><span data-ttu-id="64e41-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-318">Cost behavior</span></span></th>
<th><span data-ttu-id="64e41-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-319">Amount</span></span></th>
<th><span data-ttu-id="64e41-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-321">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-321">CC099</span></span></td>
<td><span data-ttu-id="64e41-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-322">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-323">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-323">10001</span></span></td>
<td><span data-ttu-id="64e41-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-324">Electricity</span></span></td>
<td><span data-ttu-id="64e41-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-325">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="64e41-326">-1,000.00</span></span></td>
<td><span data-ttu-id="64e41-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-328">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-328">CC001</span></span></td>
<td><span data-ttu-id="64e41-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-329">HR</span></span></td>
<td><span data-ttu-id="64e41-330">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-330">10001</span></span></td>
<td><span data-ttu-id="64e41-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-331">Electricity</span></span></td>
<td><span data-ttu-id="64e41-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-332">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-333">500,00</span><span class="sxs-lookup"><span data-stu-id="64e41-333">500.00</span></span></td>
<td><span data-ttu-id="64e41-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-335">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-335">CC002</span></span></td>
<td><span data-ttu-id="64e41-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-336">Finance</span></span></td>
<td><span data-ttu-id="64e41-337">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-337">10001</span></span></td>
<td><span data-ttu-id="64e41-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-338">Electricity</span></span></td>
<td><span data-ttu-id="64e41-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-339">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-340">500,00</span><span class="sxs-lookup"><span data-stu-id="64e41-340">500.00</span></span></td>
<td><span data-ttu-id="64e41-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-342">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-342">CC099</span></span></td>
<td><span data-ttu-id="64e41-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="64e41-343">Default cost center</span></span></td>
<td><span data-ttu-id="64e41-344">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-344">10001</span></span></td>
<td><span data-ttu-id="64e41-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-345">Electricity</span></span></td>
<td><span data-ttu-id="64e41-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-346">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="64e41-347">-9,000.00</span></span></td>
<td><span data-ttu-id="64e41-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-349">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-349">CC001</span></span></td>
<td><span data-ttu-id="64e41-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-350">HR</span></span></td>
<td><span data-ttu-id="64e41-351">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-351">10001</span></span></td>
<td><span data-ttu-id="64e41-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-352">Electricity</span></span></td>
<td><span data-ttu-id="64e41-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-353">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="64e41-354">1,285.71</span></span></td>
<td><span data-ttu-id="64e41-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-356">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-356">CC002</span></span></td>
<td><span data-ttu-id="64e41-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-357">Finance</span></span></td>
<td><span data-ttu-id="64e41-358">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-358">10001</span></span></td>
<td><span data-ttu-id="64e41-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-359">Electricity</span></span></td>
<td><span data-ttu-id="64e41-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-360">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="64e41-361">7,714.29</span></span></td>
<td><span data-ttu-id="64e41-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="64e41-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="64e41-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="64e41-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="64e41-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="64e41-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="64e41-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="64e41-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="64e41-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="64e41-367">Define the overhead rate</span></span>

<span data-ttu-id="64e41-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="64e41-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="64e41-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="64e41-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-370">Cost object</span></span></th>
<th><span data-ttu-id="64e41-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="64e41-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="64e41-372">Proj 1</span></span></td>
<td><span data-ttu-id="64e41-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-373">Project 1</span></span></td>
<td><span data-ttu-id="64e41-374">3</span><span class="sxs-lookup"><span data-stu-id="64e41-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="64e41-375">Proj 2</span></span></td>
<td><span data-ttu-id="64e41-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-376">Project 2</span></span></td>
<td><span data-ttu-id="64e41-377">1</span><span class="sxs-lookup"><span data-stu-id="64e41-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="64e41-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-379">Cost object</span></span></th>
<th><span data-ttu-id="64e41-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-380">Cost element</span></span></th>
<th><span data-ttu-id="64e41-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-381">Cost behavior</span></span></th>
<th><span data-ttu-id="64e41-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="64e41-382">Units</span></span></th>
<th><span data-ttu-id="64e41-383">Satz</span><span class="sxs-lookup"><span data-stu-id="64e41-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-384">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-384">CC001</span></span></td>
<td><span data-ttu-id="64e41-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-385">HR</span></span></td>
<td><span data-ttu-id="64e41-386">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-386">10001</span></span></td>
<td><span data-ttu-id="64e41-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-387">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-388">1</span><span class="sxs-lookup"><span data-stu-id="64e41-388">1</span></span></td>
<td><span data-ttu-id="64e41-389">10</span><span class="sxs-lookup"><span data-stu-id="64e41-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="64e41-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-391">Cost object</span></span></th>
<th><span data-ttu-id="64e41-392">Größe</span><span class="sxs-lookup"><span data-stu-id="64e41-392">Magnitude</span></span></th>
<th><span data-ttu-id="64e41-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-393">Cost element</span></span></th>
<th><span data-ttu-id="64e41-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="64e41-394">Allocation factor</span></span></th>
<th><span data-ttu-id="64e41-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="64e41-396">Proj 1</span></span></td>
<td><span data-ttu-id="64e41-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-397">Project 1</span></span></td>
<td><span data-ttu-id="64e41-398">3</span><span class="sxs-lookup"><span data-stu-id="64e41-398">3</span></span></td>
<td><span data-ttu-id="64e41-399">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-399">10001</span></span></td>
<td><span data-ttu-id="64e41-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="64e41-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="64e41-401">30,00</span><span class="sxs-lookup"><span data-stu-id="64e41-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="64e41-402">Proj 2</span></span></td>
<td><span data-ttu-id="64e41-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-403">Project 2</span></span></td>
<td><span data-ttu-id="64e41-404">1</span><span class="sxs-lookup"><span data-stu-id="64e41-404">1</span></span></td>
<td><span data-ttu-id="64e41-405">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-405">10001</span></span></td>
<td><span data-ttu-id="64e41-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="64e41-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="64e41-407">10,00</span><span class="sxs-lookup"><span data-stu-id="64e41-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="64e41-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="64e41-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="64e41-409">Journal</span></span></th>
<th><span data-ttu-id="64e41-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="64e41-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="64e41-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="64e41-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="64e41-412">Version</span><span class="sxs-lookup"><span data-stu-id="64e41-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-413">00003</span><span class="sxs-lookup"><span data-stu-id="64e41-413">00003</span></span></td>
<td><span data-ttu-id="64e41-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="64e41-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="64e41-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="64e41-415">Fiscal</span></span></td>
<td><span data-ttu-id="64e41-416">2017</span><span class="sxs-lookup"><span data-stu-id="64e41-416">2017</span></span></td>
<td><span data-ttu-id="64e41-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="64e41-417">Period 1</span></span></td>
<td><span data-ttu-id="64e41-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="64e41-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="64e41-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="64e41-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-421">Cost object</span></span></th>
<th><span data-ttu-id="64e41-422">Größe</span><span class="sxs-lookup"><span data-stu-id="64e41-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="64e41-424">Proj 1</span></span></td>
<td><span data-ttu-id="64e41-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="64e41-426">3,00</span><span class="sxs-lookup"><span data-stu-id="64e41-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="64e41-428">Proj 2</span></span></td>
<td><span data-ttu-id="64e41-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="64e41-430">1,00</span><span class="sxs-lookup"><span data-stu-id="64e41-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="64e41-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="64e41-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-433">Cost element</span></span></th>
<th><span data-ttu-id="64e41-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-434">Cost behavior</span></span></th>
<th><span data-ttu-id="64e41-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-435">Amount</span></span></th>
<th><span data-ttu-id="64e41-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="64e41-437">CC0001</span></span></td>
<td><span data-ttu-id="64e41-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-438">HR</span></span></td>
<td><span data-ttu-id="64e41-439">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-439">10001</span></span></td>
<td><span data-ttu-id="64e41-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-440">Electricity</span></span></td>
<td><span data-ttu-id="64e41-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-441">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="64e41-442">-30.00</span></span></td>
<td><span data-ttu-id="64e41-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="64e41-444">Proj 1</span></span></td>
<td><span data-ttu-id="64e41-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="64e41-446">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-446">10001</span></span></td>
<td><span data-ttu-id="64e41-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-447">Electricity</span></span></td>
<td><span data-ttu-id="64e41-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-448">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-449">30,00</span><span class="sxs-lookup"><span data-stu-id="64e41-449">30.00</span></span></td>
<td><span data-ttu-id="64e41-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-451">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-451">CC001</span></span></td>
<td><span data-ttu-id="64e41-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-452">HR</span></span></td>
<td><span data-ttu-id="64e41-453">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-453">10001</span></span></td>
<td><span data-ttu-id="64e41-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-454">Electricity</span></span></td>
<td><span data-ttu-id="64e41-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-455">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="64e41-456">-10.00</span></span></td>
<td><span data-ttu-id="64e41-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="64e41-458">Proj 2</span></span></td>
<td><span data-ttu-id="64e41-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="64e41-460">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-460">10001</span></span></td>
<td><span data-ttu-id="64e41-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-461">Electricity</span></span></td>
<td><span data-ttu-id="64e41-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-462">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-463">10.00</span><span class="sxs-lookup"><span data-stu-id="64e41-463">10.00</span></span></td>
<td><span data-ttu-id="64e41-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="64e41-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="64e41-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="64e41-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="64e41-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="64e41-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="64e41-468">Finance and Operations unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="64e41-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="64e41-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="64e41-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="64e41-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64e41-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="64e41-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="64e41-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="64e41-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64e41-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="64e41-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="64e41-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="64e41-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="64e41-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="64e41-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="64e41-475">Define the cost allocation</span></span>

<span data-ttu-id="64e41-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="64e41-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="64e41-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="64e41-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="64e41-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="64e41-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-479">Cost object</span></span></th>
<th><span data-ttu-id="64e41-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="64e41-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-481">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-481">CC002</span></span></td>
<td><span data-ttu-id="64e41-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-482">Finance</span></span></td>
<td><span data-ttu-id="64e41-483">35</span><span class="sxs-lookup"><span data-stu-id="64e41-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-484">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-484">CC003</span></span></td>
<td><span data-ttu-id="64e41-485">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-485">Assembly</span></span></td>
<td><span data-ttu-id="64e41-486">55</span><span class="sxs-lookup"><span data-stu-id="64e41-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-487">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-487">CC004</span></span></td>
<td><span data-ttu-id="64e41-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-488">Packaging</span></span></td>
<td><span data-ttu-id="64e41-489">10</span><span class="sxs-lookup"><span data-stu-id="64e41-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="64e41-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="64e41-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="64e41-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-492">Cost object</span></span></th>
<th><span data-ttu-id="64e41-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="64e41-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-494">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-494">CC003</span></span></td>
<td><span data-ttu-id="64e41-495">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-495">Assembly</span></span></td>
<td><span data-ttu-id="64e41-496">65</span><span class="sxs-lookup"><span data-stu-id="64e41-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-497">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-497">CC004</span></span></td>
<td><span data-ttu-id="64e41-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-498">Packaging</span></span></td>
<td><span data-ttu-id="64e41-499">35</span><span class="sxs-lookup"><span data-stu-id="64e41-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="64e41-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="64e41-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="64e41-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-502">Cost object</span></span></th>
<th><span data-ttu-id="64e41-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="64e41-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-504">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-505">Product 1</span></span></td>
<td><span data-ttu-id="64e41-506">60</span><span class="sxs-lookup"><span data-stu-id="64e41-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-507">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-508">Product 2</span></span></td>
<td><span data-ttu-id="64e41-509">20</span><span class="sxs-lookup"><span data-stu-id="64e41-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="64e41-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="64e41-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="64e41-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-512">Cost object</span></span></th>
<th><span data-ttu-id="64e41-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="64e41-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-514">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-515">Product 1</span></span></td>
<td><span data-ttu-id="64e41-516">80</span><span class="sxs-lookup"><span data-stu-id="64e41-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-517">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-518">Product 2</span></span></td>
<td><span data-ttu-id="64e41-519">September</span><span class="sxs-lookup"><span data-stu-id="64e41-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="64e41-520">In Finance and Operations können statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="64e41-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="64e41-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="64e41-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="64e41-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="64e41-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-523">Cost object</span></span></th>
<th><span data-ttu-id="64e41-524">Größe</span><span class="sxs-lookup"><span data-stu-id="64e41-524">Magnitude</span></span></th>
<th><span data-ttu-id="64e41-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="64e41-525">Allocation factor</span></span></th>
<th><span data-ttu-id="64e41-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-526">Amount</span></span></th>
<th><span data-ttu-id="64e41-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-528">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-528">CC002</span></span></td>
<td><span data-ttu-id="64e41-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-529">Finance</span></span></td>
<td><span data-ttu-id="64e41-530">35</span><span class="sxs-lookup"><span data-stu-id="64e41-530">35</span></span></td>
<td><span data-ttu-id="64e41-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="64e41-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="64e41-532">175.00</span><span class="sxs-lookup"><span data-stu-id="64e41-532">175.00</span></span></td>
<td><span data-ttu-id="64e41-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-534">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-534">CC003</span></span></td>
<td><span data-ttu-id="64e41-535">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-535">Assembly</span></span></td>
<td><span data-ttu-id="64e41-536">55</span><span class="sxs-lookup"><span data-stu-id="64e41-536">55</span></span></td>
<td><span data-ttu-id="64e41-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="64e41-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="64e41-538">275.00</span><span class="sxs-lookup"><span data-stu-id="64e41-538">275.00</span></span></td>
<td><span data-ttu-id="64e41-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-540">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-540">CC004</span></span></td>
<td><span data-ttu-id="64e41-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-541">Packaging</span></span></td>
<td><span data-ttu-id="64e41-542">10</span><span class="sxs-lookup"><span data-stu-id="64e41-542">10</span></span></td>
<td><span data-ttu-id="64e41-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="64e41-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="64e41-544">50,00</span><span class="sxs-lookup"><span data-stu-id="64e41-544">50.00</span></span></td>
<td><span data-ttu-id="64e41-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-546">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-546">CC002</span></span></td>
<td><span data-ttu-id="64e41-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-547">Finance</span></span></td>
<td><span data-ttu-id="64e41-548">35</span><span class="sxs-lookup"><span data-stu-id="64e41-548">35</span></span></td>
<td><span data-ttu-id="64e41-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="64e41-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="64e41-550">436.00</span><span class="sxs-lookup"><span data-stu-id="64e41-550">436.00</span></span></td>
<td><span data-ttu-id="64e41-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-552">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-552">CC003</span></span></td>
<td><span data-ttu-id="64e41-553">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-553">Assembly</span></span></td>
<td><span data-ttu-id="64e41-554">55</span><span class="sxs-lookup"><span data-stu-id="64e41-554">55</span></span></td>
<td><span data-ttu-id="64e41-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="64e41-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="64e41-556">685.14</span><span class="sxs-lookup"><span data-stu-id="64e41-556">685.14</span></span></td>
<td><span data-ttu-id="64e41-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-558">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-558">CC004</span></span></td>
<td><span data-ttu-id="64e41-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-559">Packaging</span></span></td>
<td><span data-ttu-id="64e41-560">10</span><span class="sxs-lookup"><span data-stu-id="64e41-560">10</span></span></td>
<td><span data-ttu-id="64e41-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="64e41-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="64e41-562">124.57</span><span class="sxs-lookup"><span data-stu-id="64e41-562">124.57</span></span></td>
<td><span data-ttu-id="64e41-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="64e41-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-565">Cost object</span></span></th>
<th><span data-ttu-id="64e41-566">Größe</span><span class="sxs-lookup"><span data-stu-id="64e41-566">Magnitude</span></span></th>
<th><span data-ttu-id="64e41-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="64e41-567">Allocation factor</span></span></th>
<th><span data-ttu-id="64e41-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-568">Amount</span></span></th>
<th><span data-ttu-id="64e41-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-570">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-570">CC003</span></span></td>
<td><span data-ttu-id="64e41-571">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-571">Assembly</span></span></td>
<td><span data-ttu-id="64e41-572">65</span><span class="sxs-lookup"><span data-stu-id="64e41-572">65</span></span></td>
<td><span data-ttu-id="64e41-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="64e41-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="64e41-574">438.75</span><span class="sxs-lookup"><span data-stu-id="64e41-574">438.75</span></span></td>
<td><span data-ttu-id="64e41-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-576">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-576">CC004</span></span></td>
<td><span data-ttu-id="64e41-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-577">Packaging</span></span></td>
<td><span data-ttu-id="64e41-578">35</span><span class="sxs-lookup"><span data-stu-id="64e41-578">35</span></span></td>
<td><span data-ttu-id="64e41-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="64e41-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="64e41-580">236.25</span><span class="sxs-lookup"><span data-stu-id="64e41-580">236.25</span></span></td>
<td><span data-ttu-id="64e41-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-582">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-582">CC003</span></span></td>
<td><span data-ttu-id="64e41-583">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-583">Assembly</span></span></td>
<td><span data-ttu-id="64e41-584">65</span><span class="sxs-lookup"><span data-stu-id="64e41-584">65</span></span></td>
<td><span data-ttu-id="64e41-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="64e41-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="64e41-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="64e41-586">5,297.69</span></span></td>
<td><span data-ttu-id="64e41-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-588">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-588">CC004</span></span></td>
<td><span data-ttu-id="64e41-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-589">Packaging</span></span></td>
<td><span data-ttu-id="64e41-590">35</span><span class="sxs-lookup"><span data-stu-id="64e41-590">35</span></span></td>
<td><span data-ttu-id="64e41-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="64e41-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="64e41-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="64e41-592">2,852.60</span></span></td>
<td><span data-ttu-id="64e41-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="64e41-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-595">Cost object</span></span></th>
<th><span data-ttu-id="64e41-596">Größe</span><span class="sxs-lookup"><span data-stu-id="64e41-596">Magnitude</span></span></th>
<th><span data-ttu-id="64e41-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="64e41-597">Allocation factor</span></span></th>
<th><span data-ttu-id="64e41-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-598">Amount</span></span></th>
<th><span data-ttu-id="64e41-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-600">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-601">Product 1</span></span></td>
<td><span data-ttu-id="64e41-602">60</span><span class="sxs-lookup"><span data-stu-id="64e41-602">60</span></span></td>
<td><span data-ttu-id="64e41-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="64e41-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="64e41-604">535.31</span><span class="sxs-lookup"><span data-stu-id="64e41-604">535.31</span></span></td>
<td><span data-ttu-id="64e41-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-606">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-607">Product 2</span></span></td>
<td><span data-ttu-id="64e41-608">20</span><span class="sxs-lookup"><span data-stu-id="64e41-608">20</span></span></td>
<td><span data-ttu-id="64e41-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="64e41-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="64e41-610">178.44</span><span class="sxs-lookup"><span data-stu-id="64e41-610">178.44</span></span></td>
<td><span data-ttu-id="64e41-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-612">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-613">Product 1</span></span></td>
<td><span data-ttu-id="64e41-614">60</span><span class="sxs-lookup"><span data-stu-id="64e41-614">60</span></span></td>
<td><span data-ttu-id="64e41-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="64e41-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="64e41-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="64e41-616">4,487.12</span></span></td>
<td><span data-ttu-id="64e41-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-618">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-619">Product 2</span></span></td>
<td><span data-ttu-id="64e41-620">20</span><span class="sxs-lookup"><span data-stu-id="64e41-620">20</span></span></td>
<td><span data-ttu-id="64e41-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="64e41-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="64e41-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="64e41-622">1,495.71</span></span></td>
<td><span data-ttu-id="64e41-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64e41-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="64e41-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-625">Cost object</span></span></th>
<th><span data-ttu-id="64e41-626">Größe</span><span class="sxs-lookup"><span data-stu-id="64e41-626">Magnitude</span></span></th>
<th><span data-ttu-id="64e41-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="64e41-627">Allocation factor</span></span></th>
<th><span data-ttu-id="64e41-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-628">Amount</span></span></th>
<th><span data-ttu-id="64e41-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-630">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-631">Product 1</span></span></td>
<td><span data-ttu-id="64e41-632">80</span><span class="sxs-lookup"><span data-stu-id="64e41-632">80</span></span></td>
<td><span data-ttu-id="64e41-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="64e41-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="64e41-634">241.05</span><span class="sxs-lookup"><span data-stu-id="64e41-634">241.05</span></span></td>
<td><span data-ttu-id="64e41-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-636">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-637">Product 2</span></span></td>
<td><span data-ttu-id="64e41-638">15</span><span class="sxs-lookup"><span data-stu-id="64e41-638">15</span></span></td>
<td><span data-ttu-id="64e41-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="64e41-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="64e41-640">45.20</span><span class="sxs-lookup"><span data-stu-id="64e41-640">45.20</span></span></td>
<td><span data-ttu-id="64e41-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-642">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-643">Product 1</span></span></td>
<td><span data-ttu-id="64e41-644">80</span><span class="sxs-lookup"><span data-stu-id="64e41-644">80</span></span></td>
<td><span data-ttu-id="64e41-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="64e41-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="64e41-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="64e41-646">2,507.09</span></span></td>
<td><span data-ttu-id="64e41-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-648">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-649">Product 2</span></span></td>
<td><span data-ttu-id="64e41-650">15</span><span class="sxs-lookup"><span data-stu-id="64e41-650">15</span></span></td>
<td><span data-ttu-id="64e41-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="64e41-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="64e41-652">470.08</span><span class="sxs-lookup"><span data-stu-id="64e41-652">470.08</span></span></td>
<td><span data-ttu-id="64e41-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="64e41-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="64e41-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="64e41-655">Journal</span></span></th>
<th><span data-ttu-id="64e41-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="64e41-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="64e41-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="64e41-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="64e41-658">Version</span><span class="sxs-lookup"><span data-stu-id="64e41-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-659">00004</span><span class="sxs-lookup"><span data-stu-id="64e41-659">00004</span></span></td>
<td><span data-ttu-id="64e41-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="64e41-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="64e41-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="64e41-661">Fiscal</span></span></td>
<td><span data-ttu-id="64e41-662">2017</span><span class="sxs-lookup"><span data-stu-id="64e41-662">2017</span></span></td>
<td><span data-ttu-id="64e41-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="64e41-663">Period 1</span></span></td>
<td><span data-ttu-id="64e41-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="64e41-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="64e41-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="64e41-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64e41-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-668">Cost element</span></span></th>
<th><span data-ttu-id="64e41-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-669">Cost behavior</span></span></th>
<th><span data-ttu-id="64e41-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-672">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-672">CC001</span></span></td>
<td><span data-ttu-id="64e41-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-673">HR</span></span></td>
<td><span data-ttu-id="64e41-674">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-674">10001</span></span></td>
<td><span data-ttu-id="64e41-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-675">Electricity</span></span></td>
<td><span data-ttu-id="64e41-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-676">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-677">500,00</span><span class="sxs-lookup"><span data-stu-id="64e41-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-679">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-679">CC001</span></span></td>
<td><span data-ttu-id="64e41-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-680">HR</span></span></td>
<td><span data-ttu-id="64e41-681">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-681">10001</span></span></td>
<td><span data-ttu-id="64e41-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-682">Electricity</span></span></td>
<td><span data-ttu-id="64e41-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-683">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="64e41-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-686">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-686">CC002</span></span></td>
<td><span data-ttu-id="64e41-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-687">Finance</span></span></td>
<td><span data-ttu-id="64e41-688">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-688">10001</span></span></td>
<td><span data-ttu-id="64e41-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-689">Electricity</span></span></td>
<td><span data-ttu-id="64e41-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-690">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-691">675.00</span><span class="sxs-lookup"><span data-stu-id="64e41-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-693">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-693">CC002</span></span></td>
<td><span data-ttu-id="64e41-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-694">Finance</span></span></td>
<td><span data-ttu-id="64e41-695">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-695">10001</span></span></td>
<td><span data-ttu-id="64e41-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-696">Electricity</span></span></td>
<td><span data-ttu-id="64e41-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-697">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="64e41-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-700">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-700">CC003</span></span></td>
<td><span data-ttu-id="64e41-701">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-701">Assembly</span></span></td>
<td><span data-ttu-id="64e41-702">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-702">10001</span></span></td>
<td><span data-ttu-id="64e41-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-703">Electricity</span></span></td>
<td><span data-ttu-id="64e41-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-704">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-705">713.75</span><span class="sxs-lookup"><span data-stu-id="64e41-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-707">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-707">CC003</span></span></td>
<td><span data-ttu-id="64e41-708">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-708">Assembly</span></span></td>
<td><span data-ttu-id="64e41-709">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-709">10001</span></span></td>
<td><span data-ttu-id="64e41-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-710">Electricity</span></span></td>
<td><span data-ttu-id="64e41-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-711">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="64e41-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-714">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-714">CC003</span></span></td>
<td><span data-ttu-id="64e41-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-715">Packaging</span></span></td>
<td><span data-ttu-id="64e41-716">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-716">10001</span></span></td>
<td><span data-ttu-id="64e41-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-717">Electricity</span></span></td>
<td><span data-ttu-id="64e41-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-718">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-719">286.25</span><span class="sxs-lookup"><span data-stu-id="64e41-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-721">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-721">CC003</span></span></td>
<td><span data-ttu-id="64e41-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-722">Packaging</span></span></td>
<td><span data-ttu-id="64e41-723">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-723">10001</span></span></td>
<td><span data-ttu-id="64e41-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-724">Electricity</span></span></td>
<td><span data-ttu-id="64e41-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-725">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="64e41-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-728">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-729">Product 1</span></span></td>
<td><span data-ttu-id="64e41-730">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-730">10001</span></span></td>
<td><span data-ttu-id="64e41-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-731">Electricity</span></span></td>
<td><span data-ttu-id="64e41-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-732">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-733">776.36</span><span class="sxs-lookup"><span data-stu-id="64e41-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-735">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-736">Product 1</span></span></td>
<td><span data-ttu-id="64e41-737">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-737">10001</span></span></td>
<td><span data-ttu-id="64e41-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-738">Electricity</span></span></td>
<td><span data-ttu-id="64e41-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-739">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="64e41-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-742">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-743">Product 1</span></span></td>
<td><span data-ttu-id="64e41-744">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-744">10001</span></span></td>
<td><span data-ttu-id="64e41-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-745">Electricity</span></span></td>
<td><span data-ttu-id="64e41-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-746">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-747">223.64</span><span class="sxs-lookup"><span data-stu-id="64e41-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="64e41-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-749">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-750">Product 1</span></span></td>
<td><span data-ttu-id="64e41-751">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-751">10001</span></span></td>
<td><span data-ttu-id="64e41-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-752">Electricity</span></span></td>
<td><span data-ttu-id="64e41-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-753">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="64e41-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="64e41-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="64e41-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64e41-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64e41-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-757">Cost element</span></span></th>
<th><span data-ttu-id="64e41-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="64e41-758">Cost behavior</span></span></th>
<th><span data-ttu-id="64e41-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="64e41-759">Amount</span></span></th>
<th><span data-ttu-id="64e41-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="64e41-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64e41-761">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-761">CC001</span></span></td>
<td><span data-ttu-id="64e41-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-762">HR</span></span></td>
<td><span data-ttu-id="64e41-763">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-763">10001</span></span></td>
<td><span data-ttu-id="64e41-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-764">Electricity</span></span></td>
<td><span data-ttu-id="64e41-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-765">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="64e41-766">-500.00</span></span></td>
<td><span data-ttu-id="64e41-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-768">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-768">CC002</span></span></td>
<td><span data-ttu-id="64e41-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-769">Finance</span></span></td>
<td><span data-ttu-id="64e41-770">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-770">10001</span></span></td>
<td><span data-ttu-id="64e41-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-771">Electricity</span></span></td>
<td><span data-ttu-id="64e41-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-772">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-773">175.00</span><span class="sxs-lookup"><span data-stu-id="64e41-773">175.00</span></span></td>
<td><span data-ttu-id="64e41-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-775">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-775">CC003</span></span></td>
<td><span data-ttu-id="64e41-776">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-776">Assembly</span></span></td>
<td><span data-ttu-id="64e41-777">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-777">10001</span></span></td>
<td><span data-ttu-id="64e41-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-778">Electricity</span></span></td>
<td><span data-ttu-id="64e41-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-779">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-780">275.00</span><span class="sxs-lookup"><span data-stu-id="64e41-780">275.00</span></span></td>
<td><span data-ttu-id="64e41-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-782">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-782">CC004</span></span></td>
<td><span data-ttu-id="64e41-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-783">Packaging</span></span></td>
<td><span data-ttu-id="64e41-784">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-784">10001</span></span></td>
<td><span data-ttu-id="64e41-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-785">Electricity</span></span></td>
<td><span data-ttu-id="64e41-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-786">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-787">50,00</span><span class="sxs-lookup"><span data-stu-id="64e41-787">50,00</span></span></td>
<td><span data-ttu-id="64e41-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-789">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-789">CC001</span></span></td>
<td><span data-ttu-id="64e41-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="64e41-790">HR</span></span></td>
<td><span data-ttu-id="64e41-791">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-791">10001</span></span></td>
<td><span data-ttu-id="64e41-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-792">Electricity</span></span></td>
<td><span data-ttu-id="64e41-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-793">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="64e41-794">-1,245.71</span></span></td>
<td><span data-ttu-id="64e41-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-796">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-796">CC002</span></span></td>
<td><span data-ttu-id="64e41-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-797">Finance</span></span></td>
<td><span data-ttu-id="64e41-798">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-798">10001</span></span></td>
<td><span data-ttu-id="64e41-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-799">Electricity</span></span></td>
<td><span data-ttu-id="64e41-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-800">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-801">436.00</span><span class="sxs-lookup"><span data-stu-id="64e41-801">436.00</span></span></td>
<td><span data-ttu-id="64e41-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-803">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-803">CC003</span></span></td>
<td><span data-ttu-id="64e41-804">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-804">Assembly</span></span></td>
<td><span data-ttu-id="64e41-805">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-805">10001</span></span></td>
<td><span data-ttu-id="64e41-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-806">Electricity</span></span></td>
<td><span data-ttu-id="64e41-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-807">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-808">685.14</span><span class="sxs-lookup"><span data-stu-id="64e41-808">685.14</span></span></td>
<td><span data-ttu-id="64e41-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-810">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-810">CC004</span></span></td>
<td><span data-ttu-id="64e41-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-811">Packaging</span></span></td>
<td><span data-ttu-id="64e41-812">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-812">10001</span></span></td>
<td><span data-ttu-id="64e41-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-813">Electricity</span></span></td>
<td><span data-ttu-id="64e41-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-814">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-815">124.57</span><span class="sxs-lookup"><span data-stu-id="64e41-815">124.57</span></span></td>
<td><span data-ttu-id="64e41-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-817">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-817">CC002</span></span></td>
<td><span data-ttu-id="64e41-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-818">Finance</span></span></td>
<td><span data-ttu-id="64e41-819">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-819">10001</span></span></td>
<td><span data-ttu-id="64e41-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-820">Electricity</span></span></td>
<td><span data-ttu-id="64e41-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-821">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="64e41-822">-675.00</span></span></td>
<td><span data-ttu-id="64e41-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-824">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-824">CC003</span></span></td>
<td><span data-ttu-id="64e41-825">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-825">Assembly</span></span></td>
<td><span data-ttu-id="64e41-826">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-826">10001</span></span></td>
<td><span data-ttu-id="64e41-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-827">Electricity</span></span></td>
<td><span data-ttu-id="64e41-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-828">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-829">438.75</span><span class="sxs-lookup"><span data-stu-id="64e41-829">438.75</span></span></td>
<td><span data-ttu-id="64e41-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-831">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-831">CC004</span></span></td>
<td><span data-ttu-id="64e41-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-832">Packaging</span></span></td>
<td><span data-ttu-id="64e41-833">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-833">10001</span></span></td>
<td><span data-ttu-id="64e41-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-834">Electricity</span></span></td>
<td><span data-ttu-id="64e41-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-835">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-836">236.25</span><span class="sxs-lookup"><span data-stu-id="64e41-836">236.25</span></span></td>
<td><span data-ttu-id="64e41-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-838">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-838">CC002</span></span></td>
<td><span data-ttu-id="64e41-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="64e41-839">Finance</span></span></td>
<td><span data-ttu-id="64e41-840">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-840">10001</span></span></td>
<td><span data-ttu-id="64e41-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-841">Electricity</span></span></td>
<td><span data-ttu-id="64e41-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-842">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="64e41-843">-8,150.29</span></span></td>
<td><span data-ttu-id="64e41-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-845">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-845">CC003</span></span></td>
<td><span data-ttu-id="64e41-846">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-846">Assembly</span></span></td>
<td><span data-ttu-id="64e41-847">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-847">10001</span></span></td>
<td><span data-ttu-id="64e41-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-848">Electricity</span></span></td>
<td><span data-ttu-id="64e41-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-849">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="64e41-850">5,297.69</span></span></td>
<td><span data-ttu-id="64e41-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-852">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-852">CC004</span></span></td>
<td><span data-ttu-id="64e41-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="64e41-853">Packaging</span></span></td>
<td><span data-ttu-id="64e41-854">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-854">10001</span></span></td>
<td><span data-ttu-id="64e41-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-855">Electricity</span></span></td>
<td><span data-ttu-id="64e41-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-856">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="64e41-857">2,852.60</span></span></td>
<td><span data-ttu-id="64e41-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-859">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-859">CC003</span></span></td>
<td><span data-ttu-id="64e41-860">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-860">Assembly</span></span></td>
<td><span data-ttu-id="64e41-861">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-861">10001</span></span></td>
<td><span data-ttu-id="64e41-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-862">Electricity</span></span></td>
<td><span data-ttu-id="64e41-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-863">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="64e41-864">-713.75</span></span></td>
<td><span data-ttu-id="64e41-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-866">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-867">Product 1</span></span></td>
<td><span data-ttu-id="64e41-868">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-868">10001</span></span></td>
<td><span data-ttu-id="64e41-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-869">Electricity</span></span></td>
<td><span data-ttu-id="64e41-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-870">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-871">535.31</span><span class="sxs-lookup"><span data-stu-id="64e41-871">535.31</span></span></td>
<td><span data-ttu-id="64e41-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-873">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-874">Product 2</span></span></td>
<td><span data-ttu-id="64e41-875">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-875">10001</span></span></td>
<td><span data-ttu-id="64e41-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-876">Electricity</span></span></td>
<td><span data-ttu-id="64e41-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-877">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-878">178.44</span><span class="sxs-lookup"><span data-stu-id="64e41-878">178.44</span></span></td>
<td><span data-ttu-id="64e41-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-880">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-880">CC003</span></span></td>
<td><span data-ttu-id="64e41-881">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-881">Assembly</span></span></td>
<td><span data-ttu-id="64e41-882">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-882">10001</span></span></td>
<td><span data-ttu-id="64e41-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-883">Electricity</span></span></td>
<td><span data-ttu-id="64e41-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-884">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="64e41-885">-5,982.83</span></span></td>
<td><span data-ttu-id="64e41-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-887">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-888">Product 1</span></span></td>
<td><span data-ttu-id="64e41-889">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-889">10001</span></span></td>
<td><span data-ttu-id="64e41-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-890">Electricity</span></span></td>
<td><span data-ttu-id="64e41-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-891">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="64e41-892">4,487.12</span></span></td>
<td><span data-ttu-id="64e41-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-894">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-895">Product 2</span></span></td>
<td><span data-ttu-id="64e41-896">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-896">10001</span></span></td>
<td><span data-ttu-id="64e41-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-897">Electricity</span></span></td>
<td><span data-ttu-id="64e41-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-898">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="64e41-899">1,495.71</span></span></td>
<td><span data-ttu-id="64e41-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-901">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-901">CC003</span></span></td>
<td><span data-ttu-id="64e41-902">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-902">Assembly</span></span></td>
<td><span data-ttu-id="64e41-903">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-903">10001</span></span></td>
<td><span data-ttu-id="64e41-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-904">Electricity</span></span></td>
<td><span data-ttu-id="64e41-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-905">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="64e41-906">-286.25</span></span></td>
<td><span data-ttu-id="64e41-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-908">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-909">Product 1</span></span></td>
<td><span data-ttu-id="64e41-910">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-910">10001</span></span></td>
<td><span data-ttu-id="64e41-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-911">Electricity</span></span></td>
<td><span data-ttu-id="64e41-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-912">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-913">241.05</span><span class="sxs-lookup"><span data-stu-id="64e41-913">241.05</span></span></td>
<td><span data-ttu-id="64e41-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-915">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-916">Product 2</span></span></td>
<td><span data-ttu-id="64e41-917">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-917">10001</span></span></td>
<td><span data-ttu-id="64e41-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-918">Electricity</span></span></td>
<td><span data-ttu-id="64e41-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-919">Fixed cost</span></span></td>
<td><span data-ttu-id="64e41-920">45.20</span><span class="sxs-lookup"><span data-stu-id="64e41-920">45.20</span></span></td>
<td><span data-ttu-id="64e41-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-922">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-922">CC003</span></span></td>
<td><span data-ttu-id="64e41-923">Montage</span><span class="sxs-lookup"><span data-stu-id="64e41-923">Assembly</span></span></td>
<td><span data-ttu-id="64e41-924">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-924">10001</span></span></td>
<td><span data-ttu-id="64e41-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-925">Electricity</span></span></td>
<td><span data-ttu-id="64e41-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-926">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="64e41-927">-2,977.17</span></span></td>
<td><span data-ttu-id="64e41-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-929">Prod 1</span></span></td>
<td><span data-ttu-id="64e41-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="64e41-930">Product 1</span></span></td>
<td><span data-ttu-id="64e41-931">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-931">10001</span></span></td>
<td><span data-ttu-id="64e41-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-932">Electricity</span></span></td>
<td><span data-ttu-id="64e41-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-933">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="64e41-934">2,507.09</span></span></td>
<td><span data-ttu-id="64e41-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64e41-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-936">Prod 2</span></span></td>
<td><span data-ttu-id="64e41-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="64e41-937">Product 2</span></span></td>
<td><span data-ttu-id="64e41-938">10001</span><span class="sxs-lookup"><span data-stu-id="64e41-938">10001</span></span></td>
<td><span data-ttu-id="64e41-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-939">Electricity</span></span></td>
<td><span data-ttu-id="64e41-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-940">Variable cost</span></span></td>
<td><span data-ttu-id="64e41-941">470.08</span><span class="sxs-lookup"><span data-stu-id="64e41-941">470.08</span></span></td>
<td><span data-ttu-id="64e41-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="64e41-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="64e41-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="64e41-943">Conclusion</span></span>
<span data-ttu-id="64e41-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="64e41-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="64e41-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64e41-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="64e41-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="64e41-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="64e41-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="64e41-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="64e41-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="64e41-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="64e41-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="64e41-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="64e41-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="64e41-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="64e41-951">CC099</span><span class="sxs-lookup"><span data-stu-id="64e41-951">CC099</span></span></th>
<th><span data-ttu-id="64e41-952">CC001</span><span class="sxs-lookup"><span data-stu-id="64e41-952">CC001</span></span></th>
<th><span data-ttu-id="64e41-953">CC002</span><span class="sxs-lookup"><span data-stu-id="64e41-953">CC002</span></span></th>
<th><span data-ttu-id="64e41-954">CC003</span><span class="sxs-lookup"><span data-stu-id="64e41-954">CC003</span></span></th>
<th><span data-ttu-id="64e41-955">CC004</span><span class="sxs-lookup"><span data-stu-id="64e41-955">CC004</span></span></th>
<th><span data-ttu-id="64e41-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="64e41-956">Proj 1</span></span></th>
<th><span data-ttu-id="64e41-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="64e41-957">Proj 2</span></span></th>
<th><span data-ttu-id="64e41-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="64e41-958">Prod 1</span></span></th>
<th><span data-ttu-id="64e41-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="64e41-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="64e41-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="64e41-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="64e41-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="64e41-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="64e41-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-971">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="64e41-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="64e41-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-973">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-974">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-975">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-976">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-977">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="64e41-978">776.36</span><span class="sxs-lookup"><span data-stu-id="64e41-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-979">223.64</span><span class="sxs-lookup"><span data-stu-id="64e41-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="64e41-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="64e41-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-982">000</span><span class="sxs-lookup"><span data-stu-id="64e41-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-983">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-984">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-985">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-986">0,00</span><span class="sxs-lookup"><span data-stu-id="64e41-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-987">30,00</span><span class="sxs-lookup"><span data-stu-id="64e41-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-988">10,00</span><span class="sxs-lookup"><span data-stu-id="64e41-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="64e41-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="64e41-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64e41-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="64e41-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="64e41-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="64e41-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="64e41-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="64e41-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="64e41-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="64e41-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="64e41-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="64e41-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="64e41-996">Weitere Informationen hierzu finden Sie unter [Kostenzusammenfassung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="64e41-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



