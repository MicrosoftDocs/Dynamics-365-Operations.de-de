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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208846"
---
# <a name="overhead-calculation"></a><span data-ttu-id="562d7-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="562d7-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="562d7-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="562d7-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="562d7-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="562d7-105">Term definition</span></span>
---------------

<span data-ttu-id="562d7-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="562d7-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="562d7-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="562d7-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="562d7-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="562d7-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="562d7-109">Miete</span><span class="sxs-lookup"><span data-stu-id="562d7-109">Rent</span></span>
-   <span data-ttu-id="562d7-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-110">Electricity</span></span>
-   <span data-ttu-id="562d7-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="562d7-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="562d7-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="562d7-112">Overhead calculation overview</span></span>
<span data-ttu-id="562d7-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="562d7-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="562d7-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="562d7-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="562d7-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="562d7-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="562d7-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="562d7-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="562d7-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="562d7-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="562d7-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="562d7-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="562d7-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="562d7-119">Version type</span></span>
-   <span data-ttu-id="562d7-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="562d7-120">Date and time</span></span>
-   <span data-ttu-id="562d7-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="562d7-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="562d7-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="562d7-122">Fiscal year</span></span>
-   <span data-ttu-id="562d7-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="562d7-123">Fiscal period</span></span>

<span data-ttu-id="562d7-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="562d7-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="562d7-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="562d7-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="562d7-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="562d7-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="562d7-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="562d7-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="562d7-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="562d7-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="562d7-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="562d7-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="562d7-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="562d7-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="562d7-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="562d7-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="562d7-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="562d7-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="562d7-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="562d7-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="562d7-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="562d7-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="562d7-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="562d7-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="562d7-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="562d7-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="562d7-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="562d7-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="562d7-140">Main account</span></span></th>
<th><span data-ttu-id="562d7-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="562d7-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="562d7-143">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-143">CC099</span></span></td>
<td><span data-ttu-id="562d7-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-144">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-145">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-145">10001</span></span></td>
<td><span data-ttu-id="562d7-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-146">Electricity</span></span></td>
<td><span data-ttu-id="562d7-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="562d7-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="562d7-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="562d7-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="562d7-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="562d7-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="562d7-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="562d7-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="562d7-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="562d7-151">Define the cost behavior rule</span></span>

<span data-ttu-id="562d7-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="562d7-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="562d7-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="562d7-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="562d7-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="562d7-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="562d7-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="562d7-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="562d7-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="562d7-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="562d7-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="562d7-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="562d7-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="562d7-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="562d7-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="562d7-160">Journal</span></span></th>
<th><span data-ttu-id="562d7-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="562d7-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="562d7-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="562d7-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="562d7-163">Version</span><span class="sxs-lookup"><span data-stu-id="562d7-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-164">00001</span><span class="sxs-lookup"><span data-stu-id="562d7-164">00001</span></span></td>
<td><span data-ttu-id="562d7-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="562d7-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="562d7-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="562d7-166">Fiscal</span></span></td>
<td><span data-ttu-id="562d7-167">2017</span><span class="sxs-lookup"><span data-stu-id="562d7-167">2017</span></span></td>
<td><span data-ttu-id="562d7-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="562d7-168">Period 1</span></span></td>
<td><span data-ttu-id="562d7-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="562d7-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="562d7-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="562d7-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-173">Cost element</span></span></th>
<th><span data-ttu-id="562d7-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-174">Cost behavior</span></span></th>
<th><span data-ttu-id="562d7-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="562d7-177">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-177">CC099</span></span></td>
<td><span data-ttu-id="562d7-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-178">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-179">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-179">10001</span></span></td>
<td><span data-ttu-id="562d7-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-180">Electricity</span></span></td>
<td><span data-ttu-id="562d7-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="562d7-181">Unclassified</span></span></td>
<td><span data-ttu-id="562d7-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="562d7-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="562d7-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="562d7-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-185">Cost element</span></span></th>
<th><span data-ttu-id="562d7-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-186">Cost behavior</span></span></th>
<th><span data-ttu-id="562d7-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-187">Amount</span></span></th>
<th><span data-ttu-id="562d7-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-189">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-189">CC099</span></span></td>
<td><span data-ttu-id="562d7-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-190">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-191">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-191">10001</span></span></td>
<td><span data-ttu-id="562d7-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-192">Electricity</span></span></td>
<td><span data-ttu-id="562d7-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="562d7-193">Unclassified</span></span></td>
<td><span data-ttu-id="562d7-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="562d7-194">10,000.00</span></span></td>
<td><span data-ttu-id="562d7-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-196">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-196">CC099</span></span></td>
<td><span data-ttu-id="562d7-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-197">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-198">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-198">10001</span></span></td>
<td><span data-ttu-id="562d7-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-199">Electricity</span></span></td>
<td><span data-ttu-id="562d7-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="562d7-200">Unclassified</span></span></td>
<td><span data-ttu-id="562d7-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-201">-10,000.00</span></span></td>
<td><span data-ttu-id="562d7-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-203">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-203">CC099</span></span></td>
<td><span data-ttu-id="562d7-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-204">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-205">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-205">10001</span></span></td>
<td><span data-ttu-id="562d7-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-206">Electricity</span></span></td>
<td><span data-ttu-id="562d7-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-207">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="562d7-208">1,000.00</span></span></td>
<td><span data-ttu-id="562d7-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-210">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-210">CC099</span></span></td>
<td><span data-ttu-id="562d7-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-211">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-212">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-212">10001</span></span></td>
<td><span data-ttu-id="562d7-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-213">Electricity</span></span></td>
<td><span data-ttu-id="562d7-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-214">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="562d7-215">9,000.00</span></span></td>
<td><span data-ttu-id="562d7-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="562d7-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="562d7-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="562d7-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="562d7-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="562d7-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="562d7-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="562d7-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="562d7-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="562d7-221">Define the cost distribution rule</span></span>

<span data-ttu-id="562d7-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="562d7-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="562d7-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="562d7-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="562d7-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="562d7-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="562d7-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="562d7-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="562d7-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="562d7-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="562d7-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="562d7-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-228">Cost object</span></span></th>
<th><span data-ttu-id="562d7-229">KWH</span><span class="sxs-lookup"><span data-stu-id="562d7-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-230">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-230">CC001</span></span></td>
<td><span data-ttu-id="562d7-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-231">HR</span></span></td>
<td><span data-ttu-id="562d7-232">1.000</span><span class="sxs-lookup"><span data-stu-id="562d7-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-233">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-233">CC002</span></span></td>
<td><span data-ttu-id="562d7-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-234">Finance</span></span></td>
<td><span data-ttu-id="562d7-235">6.000</span><span class="sxs-lookup"><span data-stu-id="562d7-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-236">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-236">CC003</span></span></td>
<td><span data-ttu-id="562d7-237">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-237">Assembly</span></span></td>
<td><span data-ttu-id="562d7-238">0</span><span class="sxs-lookup"><span data-stu-id="562d7-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="562d7-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-240">Cost object</span></span></th>
<th><span data-ttu-id="562d7-241">Größe</span><span class="sxs-lookup"><span data-stu-id="562d7-241">Magnitude</span></span></th>
<th><span data-ttu-id="562d7-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="562d7-242">Allocation factor</span></span></th>
<th><span data-ttu-id="562d7-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-244">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-244">CC001</span></span></td>
<td><span data-ttu-id="562d7-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-245">HR</span></span></td>
<td><span data-ttu-id="562d7-246">1.000</span><span class="sxs-lookup"><span data-stu-id="562d7-246">1,000</span></span></td>
<td><span data-ttu-id="562d7-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="562d7-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="562d7-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-249">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-249">CC002</span></span></td>
<td><span data-ttu-id="562d7-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-250">Finance</span></span></td>
<td><span data-ttu-id="562d7-251">6.000</span><span class="sxs-lookup"><span data-stu-id="562d7-251">6,000</span></span></td>
<td><span data-ttu-id="562d7-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="562d7-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="562d7-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-254">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-254">CC003</span></span></td>
<td><span data-ttu-id="562d7-255">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-255">Assembly</span></span></td>
<td><span data-ttu-id="562d7-256">0</span><span class="sxs-lookup"><span data-stu-id="562d7-256">0</span></span></td>
<td><span data-ttu-id="562d7-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="562d7-258">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="562d7-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="562d7-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: (Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="562d7-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-261">Cost object</span></span></th>
<th><span data-ttu-id="562d7-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="562d7-262">Formula</span></span></th>
<th><span data-ttu-id="562d7-263">Größe</span><span class="sxs-lookup"><span data-stu-id="562d7-263">Magnitude</span></span></th>
<th><span data-ttu-id="562d7-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="562d7-264">Allocation factor</span></span></th>
<th><span data-ttu-id="562d7-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-266">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-266">CC001</span></span></td>
<td><span data-ttu-id="562d7-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-267">HR</span></span></td>
<td><span data-ttu-id="562d7-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="562d7-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="562d7-269">1</span><span class="sxs-lookup"><span data-stu-id="562d7-269">1</span></span></td>
<td><span data-ttu-id="562d7-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="562d7-271">500,00</span><span class="sxs-lookup"><span data-stu-id="562d7-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-272">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-272">CC002</span></span></td>
<td><span data-ttu-id="562d7-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-273">Finance</span></span></td>
<td><span data-ttu-id="562d7-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="562d7-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="562d7-275">1</span><span class="sxs-lookup"><span data-stu-id="562d7-275">1</span></span></td>
<td><span data-ttu-id="562d7-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="562d7-277">500,00</span><span class="sxs-lookup"><span data-stu-id="562d7-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-278">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-278">CC003</span></span></td>
<td><span data-ttu-id="562d7-279">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-279">Assembly</span></span></td>
<td><span data-ttu-id="562d7-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="562d7-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="562d7-281">0</span><span class="sxs-lookup"><span data-stu-id="562d7-281">0</span></span></td>
<td><span data-ttu-id="562d7-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="562d7-283">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="562d7-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="562d7-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="562d7-285">Journal</span></span></th>
<th><span data-ttu-id="562d7-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="562d7-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="562d7-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="562d7-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="562d7-288">Version</span><span class="sxs-lookup"><span data-stu-id="562d7-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-289">00002</span><span class="sxs-lookup"><span data-stu-id="562d7-289">00002</span></span></td>
<td><span data-ttu-id="562d7-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="562d7-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="562d7-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="562d7-291">Fiscal</span></span></td>
<td><span data-ttu-id="562d7-292">2017</span><span class="sxs-lookup"><span data-stu-id="562d7-292">2017</span></span></td>
<td><span data-ttu-id="562d7-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="562d7-293">Period 1</span></span></td>
<td><span data-ttu-id="562d7-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="562d7-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="562d7-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="562d7-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-298">Cost element</span></span></th>
<th><span data-ttu-id="562d7-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-299">Cost behavior</span></span></th>
<th><span data-ttu-id="562d7-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-302">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-302">CC099</span></span></td>
<td><span data-ttu-id="562d7-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-303">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-304">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-304">10001</span></span></td>
<td><span data-ttu-id="562d7-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-305">Electricity</span></span></td>
<td><span data-ttu-id="562d7-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-306">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="562d7-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-309">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-309">CC099</span></span></td>
<td><span data-ttu-id="562d7-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-310">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-311">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-311">10001</span></span></td>
<td><span data-ttu-id="562d7-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-312">Electricity</span></span></td>
<td><span data-ttu-id="562d7-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-313">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="562d7-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="562d7-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="562d7-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-317">Cost element</span></span></th>
<th><span data-ttu-id="562d7-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-318">Cost behavior</span></span></th>
<th><span data-ttu-id="562d7-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-319">Amount</span></span></th>
<th><span data-ttu-id="562d7-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-321">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-321">CC099</span></span></td>
<td><span data-ttu-id="562d7-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-322">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-323">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-323">10001</span></span></td>
<td><span data-ttu-id="562d7-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-324">Electricity</span></span></td>
<td><span data-ttu-id="562d7-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-325">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="562d7-326">-1,000.00</span></span></td>
<td><span data-ttu-id="562d7-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-328">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-328">CC001</span></span></td>
<td><span data-ttu-id="562d7-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-329">HR</span></span></td>
<td><span data-ttu-id="562d7-330">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-330">10001</span></span></td>
<td><span data-ttu-id="562d7-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-331">Electricity</span></span></td>
<td><span data-ttu-id="562d7-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-332">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-333">500,00</span><span class="sxs-lookup"><span data-stu-id="562d7-333">500.00</span></span></td>
<td><span data-ttu-id="562d7-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-335">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-335">CC002</span></span></td>
<td><span data-ttu-id="562d7-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-336">Finance</span></span></td>
<td><span data-ttu-id="562d7-337">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-337">10001</span></span></td>
<td><span data-ttu-id="562d7-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-338">Electricity</span></span></td>
<td><span data-ttu-id="562d7-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-339">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-340">500,00</span><span class="sxs-lookup"><span data-stu-id="562d7-340">500.00</span></span></td>
<td><span data-ttu-id="562d7-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-342">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-342">CC099</span></span></td>
<td><span data-ttu-id="562d7-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="562d7-343">Default cost center</span></span></td>
<td><span data-ttu-id="562d7-344">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-344">10001</span></span></td>
<td><span data-ttu-id="562d7-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-345">Electricity</span></span></td>
<td><span data-ttu-id="562d7-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-346">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="562d7-347">-9,000.00</span></span></td>
<td><span data-ttu-id="562d7-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-349">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-349">CC001</span></span></td>
<td><span data-ttu-id="562d7-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-350">HR</span></span></td>
<td><span data-ttu-id="562d7-351">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-351">10001</span></span></td>
<td><span data-ttu-id="562d7-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-352">Electricity</span></span></td>
<td><span data-ttu-id="562d7-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-353">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="562d7-354">1,285.71</span></span></td>
<td><span data-ttu-id="562d7-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-356">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-356">CC002</span></span></td>
<td><span data-ttu-id="562d7-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-357">Finance</span></span></td>
<td><span data-ttu-id="562d7-358">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-358">10001</span></span></td>
<td><span data-ttu-id="562d7-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-359">Electricity</span></span></td>
<td><span data-ttu-id="562d7-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-360">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="562d7-361">7,714.29</span></span></td>
<td><span data-ttu-id="562d7-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="562d7-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="562d7-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="562d7-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="562d7-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="562d7-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="562d7-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="562d7-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="562d7-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="562d7-367">Define the overhead rate</span></span>

<span data-ttu-id="562d7-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="562d7-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="562d7-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="562d7-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-370">Cost object</span></span></th>
<th><span data-ttu-id="562d7-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="562d7-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="562d7-372">Proj 1</span></span></td>
<td><span data-ttu-id="562d7-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-373">Project 1</span></span></td>
<td><span data-ttu-id="562d7-374">3</span><span class="sxs-lookup"><span data-stu-id="562d7-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="562d7-375">Proj 2</span></span></td>
<td><span data-ttu-id="562d7-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-376">Project 2</span></span></td>
<td><span data-ttu-id="562d7-377">1</span><span class="sxs-lookup"><span data-stu-id="562d7-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="562d7-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-379">Cost object</span></span></th>
<th><span data-ttu-id="562d7-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-380">Cost element</span></span></th>
<th><span data-ttu-id="562d7-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-381">Cost behavior</span></span></th>
<th><span data-ttu-id="562d7-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="562d7-382">Units</span></span></th>
<th><span data-ttu-id="562d7-383">Satz</span><span class="sxs-lookup"><span data-stu-id="562d7-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-384">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-384">CC001</span></span></td>
<td><span data-ttu-id="562d7-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-385">HR</span></span></td>
<td><span data-ttu-id="562d7-386">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-386">10001</span></span></td>
<td><span data-ttu-id="562d7-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-387">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-388">1</span><span class="sxs-lookup"><span data-stu-id="562d7-388">1</span></span></td>
<td><span data-ttu-id="562d7-389">10</span><span class="sxs-lookup"><span data-stu-id="562d7-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="562d7-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-391">Cost object</span></span></th>
<th><span data-ttu-id="562d7-392">Größe</span><span class="sxs-lookup"><span data-stu-id="562d7-392">Magnitude</span></span></th>
<th><span data-ttu-id="562d7-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-393">Cost element</span></span></th>
<th><span data-ttu-id="562d7-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="562d7-394">Allocation factor</span></span></th>
<th><span data-ttu-id="562d7-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="562d7-396">Proj 1</span></span></td>
<td><span data-ttu-id="562d7-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-397">Project 1</span></span></td>
<td><span data-ttu-id="562d7-398">3</span><span class="sxs-lookup"><span data-stu-id="562d7-398">3</span></span></td>
<td><span data-ttu-id="562d7-399">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-399">10001</span></span></td>
<td><span data-ttu-id="562d7-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="562d7-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="562d7-401">30,00</span><span class="sxs-lookup"><span data-stu-id="562d7-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="562d7-402">Proj 2</span></span></td>
<td><span data-ttu-id="562d7-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-403">Project 2</span></span></td>
<td><span data-ttu-id="562d7-404">1</span><span class="sxs-lookup"><span data-stu-id="562d7-404">1</span></span></td>
<td><span data-ttu-id="562d7-405">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-405">10001</span></span></td>
<td><span data-ttu-id="562d7-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="562d7-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="562d7-407">10,00</span><span class="sxs-lookup"><span data-stu-id="562d7-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="562d7-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="562d7-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="562d7-409">Journal</span></span></th>
<th><span data-ttu-id="562d7-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="562d7-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="562d7-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="562d7-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="562d7-412">Version</span><span class="sxs-lookup"><span data-stu-id="562d7-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-413">00003</span><span class="sxs-lookup"><span data-stu-id="562d7-413">00003</span></span></td>
<td><span data-ttu-id="562d7-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="562d7-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="562d7-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="562d7-415">Fiscal</span></span></td>
<td><span data-ttu-id="562d7-416">2017</span><span class="sxs-lookup"><span data-stu-id="562d7-416">2017</span></span></td>
<td><span data-ttu-id="562d7-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="562d7-417">Period 1</span></span></td>
<td><span data-ttu-id="562d7-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="562d7-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="562d7-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="562d7-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-421">Cost object</span></span></th>
<th><span data-ttu-id="562d7-422">Größe</span><span class="sxs-lookup"><span data-stu-id="562d7-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="562d7-424">Proj 1</span></span></td>
<td><span data-ttu-id="562d7-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="562d7-426">3,00</span><span class="sxs-lookup"><span data-stu-id="562d7-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="562d7-428">Proj 2</span></span></td>
<td><span data-ttu-id="562d7-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="562d7-430">1,00</span><span class="sxs-lookup"><span data-stu-id="562d7-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="562d7-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="562d7-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-433">Cost element</span></span></th>
<th><span data-ttu-id="562d7-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-434">Cost behavior</span></span></th>
<th><span data-ttu-id="562d7-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-435">Amount</span></span></th>
<th><span data-ttu-id="562d7-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="562d7-437">CC0001</span></span></td>
<td><span data-ttu-id="562d7-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-438">HR</span></span></td>
<td><span data-ttu-id="562d7-439">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-439">10001</span></span></td>
<td><span data-ttu-id="562d7-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-440">Electricity</span></span></td>
<td><span data-ttu-id="562d7-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-441">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="562d7-442">-30.00</span></span></td>
<td><span data-ttu-id="562d7-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="562d7-444">Proj 1</span></span></td>
<td><span data-ttu-id="562d7-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="562d7-446">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-446">10001</span></span></td>
<td><span data-ttu-id="562d7-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-447">Electricity</span></span></td>
<td><span data-ttu-id="562d7-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-448">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-449">30,00</span><span class="sxs-lookup"><span data-stu-id="562d7-449">30.00</span></span></td>
<td><span data-ttu-id="562d7-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-451">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-451">CC001</span></span></td>
<td><span data-ttu-id="562d7-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-452">HR</span></span></td>
<td><span data-ttu-id="562d7-453">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-453">10001</span></span></td>
<td><span data-ttu-id="562d7-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-454">Electricity</span></span></td>
<td><span data-ttu-id="562d7-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-455">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="562d7-456">-10.00</span></span></td>
<td><span data-ttu-id="562d7-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="562d7-458">Proj 2</span></span></td>
<td><span data-ttu-id="562d7-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="562d7-460">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-460">10001</span></span></td>
<td><span data-ttu-id="562d7-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-461">Electricity</span></span></td>
<td><span data-ttu-id="562d7-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-462">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-463">10.00</span><span class="sxs-lookup"><span data-stu-id="562d7-463">10.00</span></span></td>
<td><span data-ttu-id="562d7-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="562d7-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="562d7-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="562d7-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="562d7-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="562d7-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="562d7-468">Finance unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="562d7-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="562d7-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="562d7-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="562d7-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="562d7-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="562d7-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="562d7-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="562d7-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="562d7-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="562d7-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="562d7-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="562d7-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="562d7-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="562d7-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="562d7-475">Define the cost allocation</span></span>

<span data-ttu-id="562d7-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="562d7-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="562d7-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="562d7-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="562d7-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="562d7-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-479">Cost object</span></span></th>
<th><span data-ttu-id="562d7-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="562d7-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-481">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-481">CC002</span></span></td>
<td><span data-ttu-id="562d7-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-482">Finance</span></span></td>
<td><span data-ttu-id="562d7-483">35</span><span class="sxs-lookup"><span data-stu-id="562d7-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-484">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-484">CC003</span></span></td>
<td><span data-ttu-id="562d7-485">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-485">Assembly</span></span></td>
<td><span data-ttu-id="562d7-486">55</span><span class="sxs-lookup"><span data-stu-id="562d7-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-487">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-487">CC004</span></span></td>
<td><span data-ttu-id="562d7-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-488">Packaging</span></span></td>
<td><span data-ttu-id="562d7-489">10</span><span class="sxs-lookup"><span data-stu-id="562d7-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="562d7-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="562d7-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="562d7-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-492">Cost object</span></span></th>
<th><span data-ttu-id="562d7-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="562d7-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-494">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-494">CC003</span></span></td>
<td><span data-ttu-id="562d7-495">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-495">Assembly</span></span></td>
<td><span data-ttu-id="562d7-496">65</span><span class="sxs-lookup"><span data-stu-id="562d7-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-497">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-497">CC004</span></span></td>
<td><span data-ttu-id="562d7-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-498">Packaging</span></span></td>
<td><span data-ttu-id="562d7-499">35</span><span class="sxs-lookup"><span data-stu-id="562d7-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="562d7-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="562d7-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="562d7-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-502">Cost object</span></span></th>
<th><span data-ttu-id="562d7-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="562d7-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-504">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-505">Product 1</span></span></td>
<td><span data-ttu-id="562d7-506">60</span><span class="sxs-lookup"><span data-stu-id="562d7-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-507">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-508">Product 2</span></span></td>
<td><span data-ttu-id="562d7-509">20</span><span class="sxs-lookup"><span data-stu-id="562d7-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="562d7-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="562d7-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="562d7-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-512">Cost object</span></span></th>
<th><span data-ttu-id="562d7-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="562d7-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-514">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-515">Product 1</span></span></td>
<td><span data-ttu-id="562d7-516">80</span><span class="sxs-lookup"><span data-stu-id="562d7-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-517">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-518">Product 2</span></span></td>
<td><span data-ttu-id="562d7-519">15</span><span class="sxs-lookup"><span data-stu-id="562d7-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="562d7-520">Statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, können von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="562d7-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="562d7-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="562d7-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="562d7-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="562d7-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-523">Cost object</span></span></th>
<th><span data-ttu-id="562d7-524">Größe</span><span class="sxs-lookup"><span data-stu-id="562d7-524">Magnitude</span></span></th>
<th><span data-ttu-id="562d7-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="562d7-525">Allocation factor</span></span></th>
<th><span data-ttu-id="562d7-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-526">Amount</span></span></th>
<th><span data-ttu-id="562d7-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-528">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-528">CC002</span></span></td>
<td><span data-ttu-id="562d7-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-529">Finance</span></span></td>
<td><span data-ttu-id="562d7-530">35</span><span class="sxs-lookup"><span data-stu-id="562d7-530">35</span></span></td>
<td><span data-ttu-id="562d7-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="562d7-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="562d7-532">175.00</span><span class="sxs-lookup"><span data-stu-id="562d7-532">175.00</span></span></td>
<td><span data-ttu-id="562d7-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-534">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-534">CC003</span></span></td>
<td><span data-ttu-id="562d7-535">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-535">Assembly</span></span></td>
<td><span data-ttu-id="562d7-536">55</span><span class="sxs-lookup"><span data-stu-id="562d7-536">55</span></span></td>
<td><span data-ttu-id="562d7-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="562d7-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="562d7-538">275.00</span><span class="sxs-lookup"><span data-stu-id="562d7-538">275.00</span></span></td>
<td><span data-ttu-id="562d7-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-540">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-540">CC004</span></span></td>
<td><span data-ttu-id="562d7-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-541">Packaging</span></span></td>
<td><span data-ttu-id="562d7-542">10</span><span class="sxs-lookup"><span data-stu-id="562d7-542">10</span></span></td>
<td><span data-ttu-id="562d7-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="562d7-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="562d7-544">50,00</span><span class="sxs-lookup"><span data-stu-id="562d7-544">50.00</span></span></td>
<td><span data-ttu-id="562d7-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-546">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-546">CC002</span></span></td>
<td><span data-ttu-id="562d7-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-547">Finance</span></span></td>
<td><span data-ttu-id="562d7-548">35</span><span class="sxs-lookup"><span data-stu-id="562d7-548">35</span></span></td>
<td><span data-ttu-id="562d7-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="562d7-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="562d7-550">436.00</span><span class="sxs-lookup"><span data-stu-id="562d7-550">436.00</span></span></td>
<td><span data-ttu-id="562d7-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-552">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-552">CC003</span></span></td>
<td><span data-ttu-id="562d7-553">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-553">Assembly</span></span></td>
<td><span data-ttu-id="562d7-554">55</span><span class="sxs-lookup"><span data-stu-id="562d7-554">55</span></span></td>
<td><span data-ttu-id="562d7-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="562d7-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="562d7-556">685.14</span><span class="sxs-lookup"><span data-stu-id="562d7-556">685.14</span></span></td>
<td><span data-ttu-id="562d7-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-558">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-558">CC004</span></span></td>
<td><span data-ttu-id="562d7-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-559">Packaging</span></span></td>
<td><span data-ttu-id="562d7-560">10</span><span class="sxs-lookup"><span data-stu-id="562d7-560">10</span></span></td>
<td><span data-ttu-id="562d7-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="562d7-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="562d7-562">124.57</span><span class="sxs-lookup"><span data-stu-id="562d7-562">124.57</span></span></td>
<td><span data-ttu-id="562d7-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="562d7-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-565">Cost object</span></span></th>
<th><span data-ttu-id="562d7-566">Größe</span><span class="sxs-lookup"><span data-stu-id="562d7-566">Magnitude</span></span></th>
<th><span data-ttu-id="562d7-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="562d7-567">Allocation factor</span></span></th>
<th><span data-ttu-id="562d7-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-568">Amount</span></span></th>
<th><span data-ttu-id="562d7-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-570">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-570">CC003</span></span></td>
<td><span data-ttu-id="562d7-571">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-571">Assembly</span></span></td>
<td><span data-ttu-id="562d7-572">65</span><span class="sxs-lookup"><span data-stu-id="562d7-572">65</span></span></td>
<td><span data-ttu-id="562d7-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="562d7-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="562d7-574">438.75</span><span class="sxs-lookup"><span data-stu-id="562d7-574">438.75</span></span></td>
<td><span data-ttu-id="562d7-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-576">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-576">CC004</span></span></td>
<td><span data-ttu-id="562d7-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-577">Packaging</span></span></td>
<td><span data-ttu-id="562d7-578">35</span><span class="sxs-lookup"><span data-stu-id="562d7-578">35</span></span></td>
<td><span data-ttu-id="562d7-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="562d7-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="562d7-580">236.25</span><span class="sxs-lookup"><span data-stu-id="562d7-580">236.25</span></span></td>
<td><span data-ttu-id="562d7-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-582">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-582">CC003</span></span></td>
<td><span data-ttu-id="562d7-583">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-583">Assembly</span></span></td>
<td><span data-ttu-id="562d7-584">65</span><span class="sxs-lookup"><span data-stu-id="562d7-584">65</span></span></td>
<td><span data-ttu-id="562d7-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="562d7-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="562d7-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="562d7-586">5,297.69</span></span></td>
<td><span data-ttu-id="562d7-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-588">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-588">CC004</span></span></td>
<td><span data-ttu-id="562d7-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-589">Packaging</span></span></td>
<td><span data-ttu-id="562d7-590">35</span><span class="sxs-lookup"><span data-stu-id="562d7-590">35</span></span></td>
<td><span data-ttu-id="562d7-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="562d7-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="562d7-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="562d7-592">2,852.60</span></span></td>
<td><span data-ttu-id="562d7-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="562d7-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-595">Cost object</span></span></th>
<th><span data-ttu-id="562d7-596">Größe</span><span class="sxs-lookup"><span data-stu-id="562d7-596">Magnitude</span></span></th>
<th><span data-ttu-id="562d7-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="562d7-597">Allocation factor</span></span></th>
<th><span data-ttu-id="562d7-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-598">Amount</span></span></th>
<th><span data-ttu-id="562d7-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-600">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-601">Product 1</span></span></td>
<td><span data-ttu-id="562d7-602">60</span><span class="sxs-lookup"><span data-stu-id="562d7-602">60</span></span></td>
<td><span data-ttu-id="562d7-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="562d7-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="562d7-604">535.31</span><span class="sxs-lookup"><span data-stu-id="562d7-604">535.31</span></span></td>
<td><span data-ttu-id="562d7-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-606">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-607">Product 2</span></span></td>
<td><span data-ttu-id="562d7-608">20</span><span class="sxs-lookup"><span data-stu-id="562d7-608">20</span></span></td>
<td><span data-ttu-id="562d7-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="562d7-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="562d7-610">178.44</span><span class="sxs-lookup"><span data-stu-id="562d7-610">178.44</span></span></td>
<td><span data-ttu-id="562d7-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-612">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-613">Product 1</span></span></td>
<td><span data-ttu-id="562d7-614">60</span><span class="sxs-lookup"><span data-stu-id="562d7-614">60</span></span></td>
<td><span data-ttu-id="562d7-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="562d7-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="562d7-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="562d7-616">4,487.12</span></span></td>
<td><span data-ttu-id="562d7-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-618">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-619">Product 2</span></span></td>
<td><span data-ttu-id="562d7-620">20</span><span class="sxs-lookup"><span data-stu-id="562d7-620">20</span></span></td>
<td><span data-ttu-id="562d7-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="562d7-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="562d7-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="562d7-622">1,495.71</span></span></td>
<td><span data-ttu-id="562d7-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="562d7-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="562d7-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-625">Cost object</span></span></th>
<th><span data-ttu-id="562d7-626">Größe</span><span class="sxs-lookup"><span data-stu-id="562d7-626">Magnitude</span></span></th>
<th><span data-ttu-id="562d7-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="562d7-627">Allocation factor</span></span></th>
<th><span data-ttu-id="562d7-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-628">Amount</span></span></th>
<th><span data-ttu-id="562d7-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-630">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-631">Product 1</span></span></td>
<td><span data-ttu-id="562d7-632">80</span><span class="sxs-lookup"><span data-stu-id="562d7-632">80</span></span></td>
<td><span data-ttu-id="562d7-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="562d7-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="562d7-634">241.05</span><span class="sxs-lookup"><span data-stu-id="562d7-634">241.05</span></span></td>
<td><span data-ttu-id="562d7-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-636">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-637">Product 2</span></span></td>
<td><span data-ttu-id="562d7-638">15</span><span class="sxs-lookup"><span data-stu-id="562d7-638">15</span></span></td>
<td><span data-ttu-id="562d7-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="562d7-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="562d7-640">45.20</span><span class="sxs-lookup"><span data-stu-id="562d7-640">45.20</span></span></td>
<td><span data-ttu-id="562d7-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-642">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-643">Product 1</span></span></td>
<td><span data-ttu-id="562d7-644">80</span><span class="sxs-lookup"><span data-stu-id="562d7-644">80</span></span></td>
<td><span data-ttu-id="562d7-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="562d7-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="562d7-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="562d7-646">2,507.09</span></span></td>
<td><span data-ttu-id="562d7-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-648">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-649">Product 2</span></span></td>
<td><span data-ttu-id="562d7-650">15</span><span class="sxs-lookup"><span data-stu-id="562d7-650">15</span></span></td>
<td><span data-ttu-id="562d7-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="562d7-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="562d7-652">470.08</span><span class="sxs-lookup"><span data-stu-id="562d7-652">470.08</span></span></td>
<td><span data-ttu-id="562d7-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="562d7-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="562d7-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="562d7-655">Journal</span></span></th>
<th><span data-ttu-id="562d7-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="562d7-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="562d7-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="562d7-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="562d7-658">Version</span><span class="sxs-lookup"><span data-stu-id="562d7-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-659">00004</span><span class="sxs-lookup"><span data-stu-id="562d7-659">00004</span></span></td>
<td><span data-ttu-id="562d7-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="562d7-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="562d7-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="562d7-661">Fiscal</span></span></td>
<td><span data-ttu-id="562d7-662">2017</span><span class="sxs-lookup"><span data-stu-id="562d7-662">2017</span></span></td>
<td><span data-ttu-id="562d7-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="562d7-663">Period 1</span></span></td>
<td><span data-ttu-id="562d7-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="562d7-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="562d7-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="562d7-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562d7-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-668">Cost element</span></span></th>
<th><span data-ttu-id="562d7-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-669">Cost behavior</span></span></th>
<th><span data-ttu-id="562d7-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-672">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-672">CC001</span></span></td>
<td><span data-ttu-id="562d7-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-673">HR</span></span></td>
<td><span data-ttu-id="562d7-674">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-674">10001</span></span></td>
<td><span data-ttu-id="562d7-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-675">Electricity</span></span></td>
<td><span data-ttu-id="562d7-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-676">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-677">500,00</span><span class="sxs-lookup"><span data-stu-id="562d7-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-679">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-679">CC001</span></span></td>
<td><span data-ttu-id="562d7-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-680">HR</span></span></td>
<td><span data-ttu-id="562d7-681">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-681">10001</span></span></td>
<td><span data-ttu-id="562d7-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-682">Electricity</span></span></td>
<td><span data-ttu-id="562d7-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-683">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="562d7-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-686">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-686">CC002</span></span></td>
<td><span data-ttu-id="562d7-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-687">Finance</span></span></td>
<td><span data-ttu-id="562d7-688">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-688">10001</span></span></td>
<td><span data-ttu-id="562d7-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-689">Electricity</span></span></td>
<td><span data-ttu-id="562d7-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-690">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-691">675.00</span><span class="sxs-lookup"><span data-stu-id="562d7-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-693">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-693">CC002</span></span></td>
<td><span data-ttu-id="562d7-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-694">Finance</span></span></td>
<td><span data-ttu-id="562d7-695">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-695">10001</span></span></td>
<td><span data-ttu-id="562d7-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-696">Electricity</span></span></td>
<td><span data-ttu-id="562d7-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-697">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="562d7-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-700">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-700">CC003</span></span></td>
<td><span data-ttu-id="562d7-701">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-701">Assembly</span></span></td>
<td><span data-ttu-id="562d7-702">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-702">10001</span></span></td>
<td><span data-ttu-id="562d7-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-703">Electricity</span></span></td>
<td><span data-ttu-id="562d7-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-704">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-705">713.75</span><span class="sxs-lookup"><span data-stu-id="562d7-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-707">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-707">CC003</span></span></td>
<td><span data-ttu-id="562d7-708">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-708">Assembly</span></span></td>
<td><span data-ttu-id="562d7-709">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-709">10001</span></span></td>
<td><span data-ttu-id="562d7-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-710">Electricity</span></span></td>
<td><span data-ttu-id="562d7-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-711">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="562d7-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-714">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-714">CC003</span></span></td>
<td><span data-ttu-id="562d7-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-715">Packaging</span></span></td>
<td><span data-ttu-id="562d7-716">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-716">10001</span></span></td>
<td><span data-ttu-id="562d7-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-717">Electricity</span></span></td>
<td><span data-ttu-id="562d7-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-718">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-719">286.25</span><span class="sxs-lookup"><span data-stu-id="562d7-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-721">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-721">CC003</span></span></td>
<td><span data-ttu-id="562d7-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-722">Packaging</span></span></td>
<td><span data-ttu-id="562d7-723">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-723">10001</span></span></td>
<td><span data-ttu-id="562d7-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-724">Electricity</span></span></td>
<td><span data-ttu-id="562d7-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-725">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="562d7-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-728">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-729">Product 1</span></span></td>
<td><span data-ttu-id="562d7-730">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-730">10001</span></span></td>
<td><span data-ttu-id="562d7-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-731">Electricity</span></span></td>
<td><span data-ttu-id="562d7-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-732">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-733">776.36</span><span class="sxs-lookup"><span data-stu-id="562d7-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-735">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-736">Product 1</span></span></td>
<td><span data-ttu-id="562d7-737">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-737">10001</span></span></td>
<td><span data-ttu-id="562d7-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-738">Electricity</span></span></td>
<td><span data-ttu-id="562d7-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-739">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="562d7-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-742">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-743">Product 1</span></span></td>
<td><span data-ttu-id="562d7-744">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-744">10001</span></span></td>
<td><span data-ttu-id="562d7-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-745">Electricity</span></span></td>
<td><span data-ttu-id="562d7-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-746">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-747">223.64</span><span class="sxs-lookup"><span data-stu-id="562d7-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="562d7-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-749">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-750">Product 1</span></span></td>
<td><span data-ttu-id="562d7-751">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-751">10001</span></span></td>
<td><span data-ttu-id="562d7-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-752">Electricity</span></span></td>
<td><span data-ttu-id="562d7-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-753">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="562d7-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="562d7-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="562d7-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="562d7-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="562d7-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-757">Cost element</span></span></th>
<th><span data-ttu-id="562d7-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="562d7-758">Cost behavior</span></span></th>
<th><span data-ttu-id="562d7-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="562d7-759">Amount</span></span></th>
<th><span data-ttu-id="562d7-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="562d7-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562d7-761">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-761">CC001</span></span></td>
<td><span data-ttu-id="562d7-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-762">HR</span></span></td>
<td><span data-ttu-id="562d7-763">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-763">10001</span></span></td>
<td><span data-ttu-id="562d7-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-764">Electricity</span></span></td>
<td><span data-ttu-id="562d7-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-765">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="562d7-766">-500.00</span></span></td>
<td><span data-ttu-id="562d7-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-768">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-768">CC002</span></span></td>
<td><span data-ttu-id="562d7-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-769">Finance</span></span></td>
<td><span data-ttu-id="562d7-770">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-770">10001</span></span></td>
<td><span data-ttu-id="562d7-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-771">Electricity</span></span></td>
<td><span data-ttu-id="562d7-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-772">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-773">175.00</span><span class="sxs-lookup"><span data-stu-id="562d7-773">175.00</span></span></td>
<td><span data-ttu-id="562d7-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-775">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-775">CC003</span></span></td>
<td><span data-ttu-id="562d7-776">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-776">Assembly</span></span></td>
<td><span data-ttu-id="562d7-777">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-777">10001</span></span></td>
<td><span data-ttu-id="562d7-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-778">Electricity</span></span></td>
<td><span data-ttu-id="562d7-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-779">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-780">275.00</span><span class="sxs-lookup"><span data-stu-id="562d7-780">275.00</span></span></td>
<td><span data-ttu-id="562d7-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-782">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-782">CC004</span></span></td>
<td><span data-ttu-id="562d7-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-783">Packaging</span></span></td>
<td><span data-ttu-id="562d7-784">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-784">10001</span></span></td>
<td><span data-ttu-id="562d7-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-785">Electricity</span></span></td>
<td><span data-ttu-id="562d7-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-786">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-787">50,00</span><span class="sxs-lookup"><span data-stu-id="562d7-787">50,00</span></span></td>
<td><span data-ttu-id="562d7-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-789">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-789">CC001</span></span></td>
<td><span data-ttu-id="562d7-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="562d7-790">HR</span></span></td>
<td><span data-ttu-id="562d7-791">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-791">10001</span></span></td>
<td><span data-ttu-id="562d7-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-792">Electricity</span></span></td>
<td><span data-ttu-id="562d7-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-793">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="562d7-794">-1,245.71</span></span></td>
<td><span data-ttu-id="562d7-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-796">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-796">CC002</span></span></td>
<td><span data-ttu-id="562d7-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-797">Finance</span></span></td>
<td><span data-ttu-id="562d7-798">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-798">10001</span></span></td>
<td><span data-ttu-id="562d7-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-799">Electricity</span></span></td>
<td><span data-ttu-id="562d7-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-800">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-801">436.00</span><span class="sxs-lookup"><span data-stu-id="562d7-801">436.00</span></span></td>
<td><span data-ttu-id="562d7-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-803">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-803">CC003</span></span></td>
<td><span data-ttu-id="562d7-804">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-804">Assembly</span></span></td>
<td><span data-ttu-id="562d7-805">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-805">10001</span></span></td>
<td><span data-ttu-id="562d7-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-806">Electricity</span></span></td>
<td><span data-ttu-id="562d7-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-807">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-808">685.14</span><span class="sxs-lookup"><span data-stu-id="562d7-808">685.14</span></span></td>
<td><span data-ttu-id="562d7-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-810">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-810">CC004</span></span></td>
<td><span data-ttu-id="562d7-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-811">Packaging</span></span></td>
<td><span data-ttu-id="562d7-812">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-812">10001</span></span></td>
<td><span data-ttu-id="562d7-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-813">Electricity</span></span></td>
<td><span data-ttu-id="562d7-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-814">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-815">124.57</span><span class="sxs-lookup"><span data-stu-id="562d7-815">124.57</span></span></td>
<td><span data-ttu-id="562d7-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-817">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-817">CC002</span></span></td>
<td><span data-ttu-id="562d7-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-818">Finance</span></span></td>
<td><span data-ttu-id="562d7-819">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-819">10001</span></span></td>
<td><span data-ttu-id="562d7-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-820">Electricity</span></span></td>
<td><span data-ttu-id="562d7-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-821">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="562d7-822">-675.00</span></span></td>
<td><span data-ttu-id="562d7-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-824">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-824">CC003</span></span></td>
<td><span data-ttu-id="562d7-825">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-825">Assembly</span></span></td>
<td><span data-ttu-id="562d7-826">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-826">10001</span></span></td>
<td><span data-ttu-id="562d7-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-827">Electricity</span></span></td>
<td><span data-ttu-id="562d7-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-828">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-829">438.75</span><span class="sxs-lookup"><span data-stu-id="562d7-829">438.75</span></span></td>
<td><span data-ttu-id="562d7-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-831">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-831">CC004</span></span></td>
<td><span data-ttu-id="562d7-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-832">Packaging</span></span></td>
<td><span data-ttu-id="562d7-833">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-833">10001</span></span></td>
<td><span data-ttu-id="562d7-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-834">Electricity</span></span></td>
<td><span data-ttu-id="562d7-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-835">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-836">236.25</span><span class="sxs-lookup"><span data-stu-id="562d7-836">236.25</span></span></td>
<td><span data-ttu-id="562d7-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-838">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-838">CC002</span></span></td>
<td><span data-ttu-id="562d7-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="562d7-839">Finance</span></span></td>
<td><span data-ttu-id="562d7-840">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-840">10001</span></span></td>
<td><span data-ttu-id="562d7-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-841">Electricity</span></span></td>
<td><span data-ttu-id="562d7-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-842">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="562d7-843">-8,150.29</span></span></td>
<td><span data-ttu-id="562d7-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-845">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-845">CC003</span></span></td>
<td><span data-ttu-id="562d7-846">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-846">Assembly</span></span></td>
<td><span data-ttu-id="562d7-847">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-847">10001</span></span></td>
<td><span data-ttu-id="562d7-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-848">Electricity</span></span></td>
<td><span data-ttu-id="562d7-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-849">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="562d7-850">5,297.69</span></span></td>
<td><span data-ttu-id="562d7-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-852">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-852">CC004</span></span></td>
<td><span data-ttu-id="562d7-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="562d7-853">Packaging</span></span></td>
<td><span data-ttu-id="562d7-854">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-854">10001</span></span></td>
<td><span data-ttu-id="562d7-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-855">Electricity</span></span></td>
<td><span data-ttu-id="562d7-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-856">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="562d7-857">2,852.60</span></span></td>
<td><span data-ttu-id="562d7-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-859">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-859">CC003</span></span></td>
<td><span data-ttu-id="562d7-860">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-860">Assembly</span></span></td>
<td><span data-ttu-id="562d7-861">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-861">10001</span></span></td>
<td><span data-ttu-id="562d7-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-862">Electricity</span></span></td>
<td><span data-ttu-id="562d7-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-863">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="562d7-864">-713.75</span></span></td>
<td><span data-ttu-id="562d7-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-866">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-867">Product 1</span></span></td>
<td><span data-ttu-id="562d7-868">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-868">10001</span></span></td>
<td><span data-ttu-id="562d7-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-869">Electricity</span></span></td>
<td><span data-ttu-id="562d7-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-870">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-871">535.31</span><span class="sxs-lookup"><span data-stu-id="562d7-871">535.31</span></span></td>
<td><span data-ttu-id="562d7-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-873">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-874">Product 2</span></span></td>
<td><span data-ttu-id="562d7-875">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-875">10001</span></span></td>
<td><span data-ttu-id="562d7-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-876">Electricity</span></span></td>
<td><span data-ttu-id="562d7-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-877">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-878">178.44</span><span class="sxs-lookup"><span data-stu-id="562d7-878">178.44</span></span></td>
<td><span data-ttu-id="562d7-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-880">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-880">CC003</span></span></td>
<td><span data-ttu-id="562d7-881">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-881">Assembly</span></span></td>
<td><span data-ttu-id="562d7-882">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-882">10001</span></span></td>
<td><span data-ttu-id="562d7-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-883">Electricity</span></span></td>
<td><span data-ttu-id="562d7-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-884">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="562d7-885">-5,982.83</span></span></td>
<td><span data-ttu-id="562d7-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-887">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-888">Product 1</span></span></td>
<td><span data-ttu-id="562d7-889">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-889">10001</span></span></td>
<td><span data-ttu-id="562d7-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-890">Electricity</span></span></td>
<td><span data-ttu-id="562d7-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-891">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="562d7-892">4,487.12</span></span></td>
<td><span data-ttu-id="562d7-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-894">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-895">Product 2</span></span></td>
<td><span data-ttu-id="562d7-896">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-896">10001</span></span></td>
<td><span data-ttu-id="562d7-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-897">Electricity</span></span></td>
<td><span data-ttu-id="562d7-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-898">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="562d7-899">1,495.71</span></span></td>
<td><span data-ttu-id="562d7-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-901">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-901">CC003</span></span></td>
<td><span data-ttu-id="562d7-902">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-902">Assembly</span></span></td>
<td><span data-ttu-id="562d7-903">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-903">10001</span></span></td>
<td><span data-ttu-id="562d7-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-904">Electricity</span></span></td>
<td><span data-ttu-id="562d7-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-905">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="562d7-906">-286.25</span></span></td>
<td><span data-ttu-id="562d7-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-908">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-909">Product 1</span></span></td>
<td><span data-ttu-id="562d7-910">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-910">10001</span></span></td>
<td><span data-ttu-id="562d7-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-911">Electricity</span></span></td>
<td><span data-ttu-id="562d7-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-912">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-913">241.05</span><span class="sxs-lookup"><span data-stu-id="562d7-913">241.05</span></span></td>
<td><span data-ttu-id="562d7-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-915">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-916">Product 2</span></span></td>
<td><span data-ttu-id="562d7-917">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-917">10001</span></span></td>
<td><span data-ttu-id="562d7-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-918">Electricity</span></span></td>
<td><span data-ttu-id="562d7-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-919">Fixed cost</span></span></td>
<td><span data-ttu-id="562d7-920">45.20</span><span class="sxs-lookup"><span data-stu-id="562d7-920">45.20</span></span></td>
<td><span data-ttu-id="562d7-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-922">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-922">CC003</span></span></td>
<td><span data-ttu-id="562d7-923">Montage</span><span class="sxs-lookup"><span data-stu-id="562d7-923">Assembly</span></span></td>
<td><span data-ttu-id="562d7-924">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-924">10001</span></span></td>
<td><span data-ttu-id="562d7-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-925">Electricity</span></span></td>
<td><span data-ttu-id="562d7-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-926">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="562d7-927">-2,977.17</span></span></td>
<td><span data-ttu-id="562d7-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-929">Prod 1</span></span></td>
<td><span data-ttu-id="562d7-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="562d7-930">Product 1</span></span></td>
<td><span data-ttu-id="562d7-931">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-931">10001</span></span></td>
<td><span data-ttu-id="562d7-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-932">Electricity</span></span></td>
<td><span data-ttu-id="562d7-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-933">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="562d7-934">2,507.09</span></span></td>
<td><span data-ttu-id="562d7-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562d7-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-936">Prod 2</span></span></td>
<td><span data-ttu-id="562d7-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="562d7-937">Product 2</span></span></td>
<td><span data-ttu-id="562d7-938">10001</span><span class="sxs-lookup"><span data-stu-id="562d7-938">10001</span></span></td>
<td><span data-ttu-id="562d7-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-939">Electricity</span></span></td>
<td><span data-ttu-id="562d7-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-940">Variable cost</span></span></td>
<td><span data-ttu-id="562d7-941">470.08</span><span class="sxs-lookup"><span data-stu-id="562d7-941">470.08</span></span></td>
<td><span data-ttu-id="562d7-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="562d7-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="562d7-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="562d7-943">Conclusion</span></span>
<span data-ttu-id="562d7-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="562d7-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="562d7-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="562d7-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="562d7-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="562d7-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="562d7-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="562d7-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="562d7-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="562d7-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="562d7-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="562d7-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="562d7-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="562d7-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="562d7-951">CC099</span><span class="sxs-lookup"><span data-stu-id="562d7-951">CC099</span></span></th>
<th><span data-ttu-id="562d7-952">CC001</span><span class="sxs-lookup"><span data-stu-id="562d7-952">CC001</span></span></th>
<th><span data-ttu-id="562d7-953">CC002</span><span class="sxs-lookup"><span data-stu-id="562d7-953">CC002</span></span></th>
<th><span data-ttu-id="562d7-954">CC003</span><span class="sxs-lookup"><span data-stu-id="562d7-954">CC003</span></span></th>
<th><span data-ttu-id="562d7-955">CC004</span><span class="sxs-lookup"><span data-stu-id="562d7-955">CC004</span></span></th>
<th><span data-ttu-id="562d7-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="562d7-956">Proj 1</span></span></th>
<th><span data-ttu-id="562d7-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="562d7-957">Proj 2</span></span></th>
<th><span data-ttu-id="562d7-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="562d7-958">Prod 1</span></span></th>
<th><span data-ttu-id="562d7-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="562d7-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="562d7-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="562d7-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="562d7-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="562d7-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="562d7-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-971">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="562d7-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="562d7-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-973">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-974">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-975">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-976">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-977">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="562d7-978">776.36</span><span class="sxs-lookup"><span data-stu-id="562d7-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-979">223.64</span><span class="sxs-lookup"><span data-stu-id="562d7-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="562d7-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="562d7-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-982">000</span><span class="sxs-lookup"><span data-stu-id="562d7-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-983">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-984">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-985">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-986">0,00</span><span class="sxs-lookup"><span data-stu-id="562d7-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-987">30,00</span><span class="sxs-lookup"><span data-stu-id="562d7-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-988">10,00</span><span class="sxs-lookup"><span data-stu-id="562d7-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="562d7-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="562d7-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="562d7-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="562d7-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="562d7-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="562d7-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="562d7-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="562d7-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="562d7-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="562d7-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="562d7-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="562d7-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="562d7-996">Weitere Informationen finden Sie unter [Kostenrollup-Richtlinie und Zuschlagsberechnung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="562d7-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]