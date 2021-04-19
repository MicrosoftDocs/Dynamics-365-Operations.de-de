---
title: Gemeinkostenberechnung
description: In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822902"
---
# <a name="overhead-calculation"></a><span data-ttu-id="c0fb5-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0fb5-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c0fb5-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="c0fb5-105">Term definition</span></span>
---------------

<span data-ttu-id="c0fb5-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c0fb5-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c0fb5-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="c0fb5-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c0fb5-109">Miete</span><span class="sxs-lookup"><span data-stu-id="c0fb5-109">Rent</span></span>
-   <span data-ttu-id="c0fb5-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-110">Electricity</span></span>
-   <span data-ttu-id="c0fb5-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="c0fb5-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c0fb5-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="c0fb5-112">Overhead calculation overview</span></span>
<span data-ttu-id="c0fb5-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c0fb5-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c0fb5-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c0fb5-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c0fb5-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c0fb5-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="c0fb5-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c0fb5-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="c0fb5-119">Version type</span></span>
-   <span data-ttu-id="c0fb5-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="c0fb5-120">Date and time</span></span>
-   <span data-ttu-id="c0fb5-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="c0fb5-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c0fb5-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="c0fb5-122">Fiscal year</span></span>
-   <span data-ttu-id="c0fb5-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="c0fb5-123">Fiscal period</span></span>

<span data-ttu-id="c0fb5-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c0fb5-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c0fb5-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c0fb5-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c0fb5-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c0fb5-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c0fb5-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c0fb5-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c0fb5-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="c0fb5-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c0fb5-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c0fb5-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c0fb5-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c0fb5-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c0fb5-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="c0fb5-140">Main account</span></span></th>
<th><span data-ttu-id="c0fb5-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-143">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-144">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-145">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-145">10001</span></span></td>
<td><span data-ttu-id="c0fb5-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-146">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c0fb5-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c0fb5-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c0fb5-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c0fb5-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="c0fb5-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c0fb5-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c0fb5-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c0fb5-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c0fb5-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="c0fb5-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c0fb5-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c0fb5-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="c0fb5-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c0fb5-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="c0fb5-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c0fb5-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-160">Journal</span></span></th>
<th><span data-ttu-id="c0fb5-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c0fb5-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0fb5-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c0fb5-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0fb5-163">Version</span><span class="sxs-lookup"><span data-stu-id="c0fb5-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-164">00001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-164">00001</span></span></td>
<td><span data-ttu-id="c0fb5-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c0fb5-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c0fb5-166">Fiscal</span></span></td>
<td><span data-ttu-id="c0fb5-167">2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-167">2017</span></span></td>
<td><span data-ttu-id="c0fb5-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-168">Period 1</span></span></td>
<td><span data-ttu-id="c0fb5-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0fb5-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-173">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c0fb5-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-177">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-178">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-179">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-179">10001</span></span></td>
<td><span data-ttu-id="c0fb5-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-180">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c0fb5-181">Unclassified</span></span></td>
<td><span data-ttu-id="c0fb5-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0fb5-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c0fb5-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-185">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c0fb5-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-187">Amount</span></span></th>
<th><span data-ttu-id="c0fb5-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-189">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-190">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-191">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-191">10001</span></span></td>
<td><span data-ttu-id="c0fb5-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-192">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c0fb5-193">Unclassified</span></span></td>
<td><span data-ttu-id="c0fb5-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-194">10,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-196">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-197">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-198">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-198">10001</span></span></td>
<td><span data-ttu-id="c0fb5-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-199">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c0fb5-200">Unclassified</span></span></td>
<td><span data-ttu-id="c0fb5-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-203">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-204">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-205">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-205">10001</span></span></td>
<td><span data-ttu-id="c0fb5-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-206">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-208">1,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-210">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-211">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-212">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-212">10001</span></span></td>
<td><span data-ttu-id="c0fb5-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-213">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-214">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-215">9,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c0fb5-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c0fb5-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c0fb5-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c0fb5-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="c0fb5-221">Define the cost distribution rule</span></span>

<span data-ttu-id="c0fb5-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c0fb5-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c0fb5-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c0fb5-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c0fb5-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c0fb5-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-228">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-229">KWH</span><span class="sxs-lookup"><span data-stu-id="c0fb5-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-230">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-230">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-231">HR</span></span></td>
<td><span data-ttu-id="c0fb5-232">1.000</span><span class="sxs-lookup"><span data-stu-id="c0fb5-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-233">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-233">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-234">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-235">6.000</span><span class="sxs-lookup"><span data-stu-id="c0fb5-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-236">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-236">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-237">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-237">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-238">0</span><span class="sxs-lookup"><span data-stu-id="c0fb5-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-240">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-241">Größe</span><span class="sxs-lookup"><span data-stu-id="c0fb5-241">Magnitude</span></span></th>
<th><span data-ttu-id="c0fb5-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c0fb5-242">Allocation factor</span></span></th>
<th><span data-ttu-id="c0fb5-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-244">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-244">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-245">HR</span></span></td>
<td><span data-ttu-id="c0fb5-246">1.000</span><span class="sxs-lookup"><span data-stu-id="c0fb5-246">1,000</span></span></td>
<td><span data-ttu-id="c0fb5-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-249">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-249">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-250">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-251">6.000</span><span class="sxs-lookup"><span data-stu-id="c0fb5-251">6,000</span></span></td>
<td><span data-ttu-id="c0fb5-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c0fb5-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-254">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-254">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-255">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-255">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-256">0</span><span class="sxs-lookup"><span data-stu-id="c0fb5-256">0</span></span></td>
<td><span data-ttu-id="c0fb5-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-258">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c0fb5-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: (Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-261">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-262">Formula</span></span></th>
<th><span data-ttu-id="c0fb5-263">Größe</span><span class="sxs-lookup"><span data-stu-id="c0fb5-263">Magnitude</span></span></th>
<th><span data-ttu-id="c0fb5-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c0fb5-264">Allocation factor</span></span></th>
<th><span data-ttu-id="c0fb5-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-266">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-266">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-267">HR</span></span></td>
<td><span data-ttu-id="c0fb5-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0fb5-269">1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-269">1</span></span></td>
<td><span data-ttu-id="c0fb5-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-271">500,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-272">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-272">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-273">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0fb5-275">1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-275">1</span></span></td>
<td><span data-ttu-id="c0fb5-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-277">500,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-278">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-278">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-279">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-279">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0fb5-281">0</span><span class="sxs-lookup"><span data-stu-id="c0fb5-281">0</span></span></td>
<td><span data-ttu-id="c0fb5-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-283">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c0fb5-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-285">Journal</span></span></th>
<th><span data-ttu-id="c0fb5-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c0fb5-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0fb5-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c0fb5-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0fb5-288">Version</span><span class="sxs-lookup"><span data-stu-id="c0fb5-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-289">00002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-289">00002</span></span></td>
<td><span data-ttu-id="c0fb5-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c0fb5-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c0fb5-291">Fiscal</span></span></td>
<td><span data-ttu-id="c0fb5-292">2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-292">2017</span></span></td>
<td><span data-ttu-id="c0fb5-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-293">Period 1</span></span></td>
<td><span data-ttu-id="c0fb5-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0fb5-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-298">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-299">Cost behavior</span></span></th>
<th><span data-ttu-id="c0fb5-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-302">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-302">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-303">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-304">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-304">10001</span></span></td>
<td><span data-ttu-id="c0fb5-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-305">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-306">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-309">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-309">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-310">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-311">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-311">10001</span></span></td>
<td><span data-ttu-id="c0fb5-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-312">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-313">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0fb5-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c0fb5-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-317">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-318">Cost behavior</span></span></th>
<th><span data-ttu-id="c0fb5-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-319">Amount</span></span></th>
<th><span data-ttu-id="c0fb5-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-321">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-321">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-322">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-323">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-323">10001</span></span></td>
<td><span data-ttu-id="c0fb5-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-324">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-325">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-326">-1,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-328">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-328">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-329">HR</span></span></td>
<td><span data-ttu-id="c0fb5-330">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-330">10001</span></span></td>
<td><span data-ttu-id="c0fb5-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-331">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-332">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-333">500,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-333">500.00</span></span></td>
<td><span data-ttu-id="c0fb5-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-335">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-335">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-336">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-337">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-337">10001</span></span></td>
<td><span data-ttu-id="c0fb5-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-338">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-339">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-340">500,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-340">500.00</span></span></td>
<td><span data-ttu-id="c0fb5-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-342">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-342">CC099</span></span></td>
<td><span data-ttu-id="c0fb5-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c0fb5-343">Default cost center</span></span></td>
<td><span data-ttu-id="c0fb5-344">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-344">10001</span></span></td>
<td><span data-ttu-id="c0fb5-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-345">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-346">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-347">-9,000.00</span></span></td>
<td><span data-ttu-id="c0fb5-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-349">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-349">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-350">HR</span></span></td>
<td><span data-ttu-id="c0fb5-351">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-351">10001</span></span></td>
<td><span data-ttu-id="c0fb5-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-352">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-353">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-354">1,285.71</span></span></td>
<td><span data-ttu-id="c0fb5-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-356">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-356">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-357">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-358">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-358">10001</span></span></td>
<td><span data-ttu-id="c0fb5-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-359">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-360">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c0fb5-361">7,714.29</span></span></td>
<td><span data-ttu-id="c0fb5-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c0fb5-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c0fb5-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c0fb5-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c0fb5-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="c0fb5-367">Define the overhead rate</span></span>

<span data-ttu-id="c0fb5-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c0fb5-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-370">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="c0fb5-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-372">Proj 1</span></span></td>
<td><span data-ttu-id="c0fb5-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-373">Project 1</span></span></td>
<td><span data-ttu-id="c0fb5-374">3</span><span class="sxs-lookup"><span data-stu-id="c0fb5-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-375">Proj 2</span></span></td>
<td><span data-ttu-id="c0fb5-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-376">Project 2</span></span></td>
<td><span data-ttu-id="c0fb5-377">1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-379">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-380">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-381">Cost behavior</span></span></th>
<th><span data-ttu-id="c0fb5-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-382">Units</span></span></th>
<th><span data-ttu-id="c0fb5-383">Satz</span><span class="sxs-lookup"><span data-stu-id="c0fb5-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-384">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-384">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-385">HR</span></span></td>
<td><span data-ttu-id="c0fb5-386">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-386">10001</span></span></td>
<td><span data-ttu-id="c0fb5-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-387">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-388">1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-388">1</span></span></td>
<td><span data-ttu-id="c0fb5-389">10</span><span class="sxs-lookup"><span data-stu-id="c0fb5-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-391">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-392">Größe</span><span class="sxs-lookup"><span data-stu-id="c0fb5-392">Magnitude</span></span></th>
<th><span data-ttu-id="c0fb5-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-393">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c0fb5-394">Allocation factor</span></span></th>
<th><span data-ttu-id="c0fb5-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-396">Proj 1</span></span></td>
<td><span data-ttu-id="c0fb5-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-397">Project 1</span></span></td>
<td><span data-ttu-id="c0fb5-398">3</span><span class="sxs-lookup"><span data-stu-id="c0fb5-398">3</span></span></td>
<td><span data-ttu-id="c0fb5-399">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-399">10001</span></span></td>
<td><span data-ttu-id="c0fb5-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c0fb5-401">30,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-402">Proj 2</span></span></td>
<td><span data-ttu-id="c0fb5-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-403">Project 2</span></span></td>
<td><span data-ttu-id="c0fb5-404">1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-404">1</span></span></td>
<td><span data-ttu-id="c0fb5-405">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-405">10001</span></span></td>
<td><span data-ttu-id="c0fb5-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c0fb5-407">10,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c0fb5-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-409">Journal</span></span></th>
<th><span data-ttu-id="c0fb5-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c0fb5-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0fb5-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c0fb5-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0fb5-412">Version</span><span class="sxs-lookup"><span data-stu-id="c0fb5-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-413">00003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-413">00003</span></span></td>
<td><span data-ttu-id="c0fb5-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c0fb5-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c0fb5-415">Fiscal</span></span></td>
<td><span data-ttu-id="c0fb5-416">2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-416">2017</span></span></td>
<td><span data-ttu-id="c0fb5-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-417">Period 1</span></span></td>
<td><span data-ttu-id="c0fb5-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c0fb5-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-421">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-422">Größe</span><span class="sxs-lookup"><span data-stu-id="c0fb5-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-424">Proj 1</span></span></td>
<td><span data-ttu-id="c0fb5-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c0fb5-426">3,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-428">Proj 2</span></span></td>
<td><span data-ttu-id="c0fb5-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c0fb5-430">1,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0fb5-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c0fb5-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-433">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-434">Cost behavior</span></span></th>
<th><span data-ttu-id="c0fb5-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-435">Amount</span></span></th>
<th><span data-ttu-id="c0fb5-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-437">CC0001</span></span></td>
<td><span data-ttu-id="c0fb5-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-438">HR</span></span></td>
<td><span data-ttu-id="c0fb5-439">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-439">10001</span></span></td>
<td><span data-ttu-id="c0fb5-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-440">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-441">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-442">-30.00</span></span></td>
<td><span data-ttu-id="c0fb5-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-444">Proj 1</span></span></td>
<td><span data-ttu-id="c0fb5-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c0fb5-446">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-446">10001</span></span></td>
<td><span data-ttu-id="c0fb5-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-447">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-448">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-449">30,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-449">30.00</span></span></td>
<td><span data-ttu-id="c0fb5-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-451">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-451">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-452">HR</span></span></td>
<td><span data-ttu-id="c0fb5-453">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-453">10001</span></span></td>
<td><span data-ttu-id="c0fb5-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-454">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-455">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-456">-10.00</span></span></td>
<td><span data-ttu-id="c0fb5-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-458">Proj 2</span></span></td>
<td><span data-ttu-id="c0fb5-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c0fb5-460">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-460">10001</span></span></td>
<td><span data-ttu-id="c0fb5-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-461">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-462">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-463">10.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-463">10.00</span></span></td>
<td><span data-ttu-id="c0fb5-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c0fb5-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c0fb5-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c0fb5-468">Finance unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="c0fb5-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c0fb5-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c0fb5-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c0fb5-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c0fb5-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c0fb5-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c0fb5-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="c0fb5-475">Define the cost allocation</span></span>

<span data-ttu-id="c0fb5-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c0fb5-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c0fb5-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-479">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="c0fb5-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-481">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-481">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-482">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-483">35</span><span class="sxs-lookup"><span data-stu-id="c0fb5-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-484">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-484">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-485">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-485">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-486">55</span><span class="sxs-lookup"><span data-stu-id="c0fb5-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-487">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-487">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-488">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-489">10</span><span class="sxs-lookup"><span data-stu-id="c0fb5-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c0fb5-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-492">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="c0fb5-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-494">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-494">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-495">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-495">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-496">65</span><span class="sxs-lookup"><span data-stu-id="c0fb5-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-497">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-497">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-498">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-499">35</span><span class="sxs-lookup"><span data-stu-id="c0fb5-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c0fb5-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-502">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-504">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-505">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-506">60</span><span class="sxs-lookup"><span data-stu-id="c0fb5-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-507">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-508">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-509">20</span><span class="sxs-lookup"><span data-stu-id="c0fb5-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c0fb5-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-512">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-514">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-515">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-516">80</span><span class="sxs-lookup"><span data-stu-id="c0fb5-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-517">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-518">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-519">15</span><span class="sxs-lookup"><span data-stu-id="c0fb5-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c0fb5-520">Statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, können von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c0fb5-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="c0fb5-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-523">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-524">Größe</span><span class="sxs-lookup"><span data-stu-id="c0fb5-524">Magnitude</span></span></th>
<th><span data-ttu-id="c0fb5-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c0fb5-525">Allocation factor</span></span></th>
<th><span data-ttu-id="c0fb5-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-526">Amount</span></span></th>
<th><span data-ttu-id="c0fb5-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-528">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-528">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-529">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-530">35</span><span class="sxs-lookup"><span data-stu-id="c0fb5-530">35</span></span></td>
<td><span data-ttu-id="c0fb5-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0fb5-532">175.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-532">175.00</span></span></td>
<td><span data-ttu-id="c0fb5-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-534">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-534">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-535">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-535">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-536">55</span><span class="sxs-lookup"><span data-stu-id="c0fb5-536">55</span></span></td>
<td><span data-ttu-id="c0fb5-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0fb5-538">275.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-538">275.00</span></span></td>
<td><span data-ttu-id="c0fb5-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-540">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-540">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-541">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-542">10</span><span class="sxs-lookup"><span data-stu-id="c0fb5-542">10</span></span></td>
<td><span data-ttu-id="c0fb5-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0fb5-544">50,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-544">50.00</span></span></td>
<td><span data-ttu-id="c0fb5-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-546">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-546">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-547">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-548">35</span><span class="sxs-lookup"><span data-stu-id="c0fb5-548">35</span></span></td>
<td><span data-ttu-id="c0fb5-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0fb5-550">436.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-550">436.00</span></span></td>
<td><span data-ttu-id="c0fb5-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-552">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-552">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-553">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-553">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-554">55</span><span class="sxs-lookup"><span data-stu-id="c0fb5-554">55</span></span></td>
<td><span data-ttu-id="c0fb5-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0fb5-556">685.14</span><span class="sxs-lookup"><span data-stu-id="c0fb5-556">685.14</span></span></td>
<td><span data-ttu-id="c0fb5-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-558">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-558">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-559">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-560">10</span><span class="sxs-lookup"><span data-stu-id="c0fb5-560">10</span></span></td>
<td><span data-ttu-id="c0fb5-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0fb5-562">124.57</span><span class="sxs-lookup"><span data-stu-id="c0fb5-562">124.57</span></span></td>
<td><span data-ttu-id="c0fb5-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-565">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-566">Größe</span><span class="sxs-lookup"><span data-stu-id="c0fb5-566">Magnitude</span></span></th>
<th><span data-ttu-id="c0fb5-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c0fb5-567">Allocation factor</span></span></th>
<th><span data-ttu-id="c0fb5-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-568">Amount</span></span></th>
<th><span data-ttu-id="c0fb5-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-570">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-570">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-571">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-571">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-572">65</span><span class="sxs-lookup"><span data-stu-id="c0fb5-572">65</span></span></td>
<td><span data-ttu-id="c0fb5-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c0fb5-574">438.75</span><span class="sxs-lookup"><span data-stu-id="c0fb5-574">438.75</span></span></td>
<td><span data-ttu-id="c0fb5-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-576">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-576">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-577">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-578">35</span><span class="sxs-lookup"><span data-stu-id="c0fb5-578">35</span></span></td>
<td><span data-ttu-id="c0fb5-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c0fb5-580">236.25</span><span class="sxs-lookup"><span data-stu-id="c0fb5-580">236.25</span></span></td>
<td><span data-ttu-id="c0fb5-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-582">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-582">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-583">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-583">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-584">65</span><span class="sxs-lookup"><span data-stu-id="c0fb5-584">65</span></span></td>
<td><span data-ttu-id="c0fb5-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c0fb5-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c0fb5-586">5,297.69</span></span></td>
<td><span data-ttu-id="c0fb5-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-588">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-588">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-589">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-590">35</span><span class="sxs-lookup"><span data-stu-id="c0fb5-590">35</span></span></td>
<td><span data-ttu-id="c0fb5-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c0fb5-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c0fb5-592">2,852.60</span></span></td>
<td><span data-ttu-id="c0fb5-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-595">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-596">Größe</span><span class="sxs-lookup"><span data-stu-id="c0fb5-596">Magnitude</span></span></th>
<th><span data-ttu-id="c0fb5-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c0fb5-597">Allocation factor</span></span></th>
<th><span data-ttu-id="c0fb5-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-598">Amount</span></span></th>
<th><span data-ttu-id="c0fb5-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-600">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-601">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-602">60</span><span class="sxs-lookup"><span data-stu-id="c0fb5-602">60</span></span></td>
<td><span data-ttu-id="c0fb5-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c0fb5-604">535.31</span><span class="sxs-lookup"><span data-stu-id="c0fb5-604">535.31</span></span></td>
<td><span data-ttu-id="c0fb5-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-606">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-607">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-608">20</span><span class="sxs-lookup"><span data-stu-id="c0fb5-608">20</span></span></td>
<td><span data-ttu-id="c0fb5-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c0fb5-610">178.44</span><span class="sxs-lookup"><span data-stu-id="c0fb5-610">178.44</span></span></td>
<td><span data-ttu-id="c0fb5-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-612">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-613">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-614">60</span><span class="sxs-lookup"><span data-stu-id="c0fb5-614">60</span></span></td>
<td><span data-ttu-id="c0fb5-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c0fb5-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c0fb5-616">4,487.12</span></span></td>
<td><span data-ttu-id="c0fb5-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-618">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-619">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-620">20</span><span class="sxs-lookup"><span data-stu-id="c0fb5-620">20</span></span></td>
<td><span data-ttu-id="c0fb5-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c0fb5-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-622">1,495.71</span></span></td>
<td><span data-ttu-id="c0fb5-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0fb5-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-625">Cost object</span></span></th>
<th><span data-ttu-id="c0fb5-626">Größe</span><span class="sxs-lookup"><span data-stu-id="c0fb5-626">Magnitude</span></span></th>
<th><span data-ttu-id="c0fb5-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c0fb5-627">Allocation factor</span></span></th>
<th><span data-ttu-id="c0fb5-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-628">Amount</span></span></th>
<th><span data-ttu-id="c0fb5-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-630">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-631">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-632">80</span><span class="sxs-lookup"><span data-stu-id="c0fb5-632">80</span></span></td>
<td><span data-ttu-id="c0fb5-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c0fb5-634">241.05</span><span class="sxs-lookup"><span data-stu-id="c0fb5-634">241.05</span></span></td>
<td><span data-ttu-id="c0fb5-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-636">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-637">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-638">15</span><span class="sxs-lookup"><span data-stu-id="c0fb5-638">15</span></span></td>
<td><span data-ttu-id="c0fb5-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c0fb5-640">45.20</span><span class="sxs-lookup"><span data-stu-id="c0fb5-640">45.20</span></span></td>
<td><span data-ttu-id="c0fb5-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-642">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-643">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-644">80</span><span class="sxs-lookup"><span data-stu-id="c0fb5-644">80</span></span></td>
<td><span data-ttu-id="c0fb5-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c0fb5-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c0fb5-646">2,507.09</span></span></td>
<td><span data-ttu-id="c0fb5-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-648">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-649">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-650">15</span><span class="sxs-lookup"><span data-stu-id="c0fb5-650">15</span></span></td>
<td><span data-ttu-id="c0fb5-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c0fb5-652">470.08</span><span class="sxs-lookup"><span data-stu-id="c0fb5-652">470.08</span></span></td>
<td><span data-ttu-id="c0fb5-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0fb5-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c0fb5-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-655">Journal</span></span></th>
<th><span data-ttu-id="c0fb5-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c0fb5-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0fb5-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c0fb5-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0fb5-658">Version</span><span class="sxs-lookup"><span data-stu-id="c0fb5-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-659">00004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-659">00004</span></span></td>
<td><span data-ttu-id="c0fb5-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c0fb5-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c0fb5-661">Fiscal</span></span></td>
<td><span data-ttu-id="c0fb5-662">2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-662">2017</span></span></td>
<td><span data-ttu-id="c0fb5-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-663">Period 1</span></span></td>
<td><span data-ttu-id="c0fb5-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c0fb5-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0fb5-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-668">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-669">Cost behavior</span></span></th>
<th><span data-ttu-id="c0fb5-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-672">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-672">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-673">HR</span></span></td>
<td><span data-ttu-id="c0fb5-674">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-674">10001</span></span></td>
<td><span data-ttu-id="c0fb5-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-675">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-676">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-677">500,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-679">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-679">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-680">HR</span></span></td>
<td><span data-ttu-id="c0fb5-681">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-681">10001</span></span></td>
<td><span data-ttu-id="c0fb5-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-682">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-683">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-686">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-686">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-687">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-688">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-688">10001</span></span></td>
<td><span data-ttu-id="c0fb5-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-689">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-690">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-691">675.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-693">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-693">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-694">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-695">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-695">10001</span></span></td>
<td><span data-ttu-id="c0fb5-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-696">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-697">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c0fb5-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-700">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-700">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-701">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-701">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-702">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-702">10001</span></span></td>
<td><span data-ttu-id="c0fb5-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-703">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-704">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-705">713.75</span><span class="sxs-lookup"><span data-stu-id="c0fb5-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-707">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-707">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-708">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-708">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-709">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-709">10001</span></span></td>
<td><span data-ttu-id="c0fb5-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-710">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-711">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c0fb5-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-714">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-714">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-715">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-716">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-716">10001</span></span></td>
<td><span data-ttu-id="c0fb5-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-717">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-718">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-719">286.25</span><span class="sxs-lookup"><span data-stu-id="c0fb5-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-721">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-721">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-722">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-723">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-723">10001</span></span></td>
<td><span data-ttu-id="c0fb5-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-724">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-725">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c0fb5-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-728">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-729">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-730">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-730">10001</span></span></td>
<td><span data-ttu-id="c0fb5-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-731">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-732">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-733">776.36</span><span class="sxs-lookup"><span data-stu-id="c0fb5-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-735">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-736">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-737">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-737">10001</span></span></td>
<td><span data-ttu-id="c0fb5-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-738">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-739">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c0fb5-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-742">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-743">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-744">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-744">10001</span></span></td>
<td><span data-ttu-id="c0fb5-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-745">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-746">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-747">223.64</span><span class="sxs-lookup"><span data-stu-id="c0fb5-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0fb5-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-749">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-750">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-751">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-751">10001</span></span></td>
<td><span data-ttu-id="c0fb5-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-752">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-753">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c0fb5-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0fb5-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c0fb5-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0fb5-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0fb5-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-757">Cost element</span></span></th>
<th><span data-ttu-id="c0fb5-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-758">Cost behavior</span></span></th>
<th><span data-ttu-id="c0fb5-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-759">Amount</span></span></th>
<th><span data-ttu-id="c0fb5-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c0fb5-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0fb5-761">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-761">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-762">HR</span></span></td>
<td><span data-ttu-id="c0fb5-763">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-763">10001</span></span></td>
<td><span data-ttu-id="c0fb5-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-764">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-765">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-766">-500.00</span></span></td>
<td><span data-ttu-id="c0fb5-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-768">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-768">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-769">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-770">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-770">10001</span></span></td>
<td><span data-ttu-id="c0fb5-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-771">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-772">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-773">175.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-773">175.00</span></span></td>
<td><span data-ttu-id="c0fb5-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-775">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-775">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-776">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-776">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-777">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-777">10001</span></span></td>
<td><span data-ttu-id="c0fb5-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-778">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-779">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-780">275.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-780">275.00</span></span></td>
<td><span data-ttu-id="c0fb5-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-782">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-782">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-783">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-784">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-784">10001</span></span></td>
<td><span data-ttu-id="c0fb5-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-785">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-786">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-787">50,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-787">50,00</span></span></td>
<td><span data-ttu-id="c0fb5-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-789">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-789">CC001</span></span></td>
<td><span data-ttu-id="c0fb5-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-790">HR</span></span></td>
<td><span data-ttu-id="c0fb5-791">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-791">10001</span></span></td>
<td><span data-ttu-id="c0fb5-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-792">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-793">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-794">-1,245.71</span></span></td>
<td><span data-ttu-id="c0fb5-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-796">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-796">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-797">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-798">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-798">10001</span></span></td>
<td><span data-ttu-id="c0fb5-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-799">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-800">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-801">436.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-801">436.00</span></span></td>
<td><span data-ttu-id="c0fb5-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-803">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-803">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-804">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-804">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-805">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-805">10001</span></span></td>
<td><span data-ttu-id="c0fb5-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-806">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-807">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-808">685.14</span><span class="sxs-lookup"><span data-stu-id="c0fb5-808">685.14</span></span></td>
<td><span data-ttu-id="c0fb5-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-810">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-810">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-811">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-812">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-812">10001</span></span></td>
<td><span data-ttu-id="c0fb5-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-813">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-814">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-815">124.57</span><span class="sxs-lookup"><span data-stu-id="c0fb5-815">124.57</span></span></td>
<td><span data-ttu-id="c0fb5-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-817">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-817">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-818">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-819">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-819">10001</span></span></td>
<td><span data-ttu-id="c0fb5-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-820">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-821">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-822">-675.00</span></span></td>
<td><span data-ttu-id="c0fb5-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-824">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-824">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-825">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-825">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-826">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-826">10001</span></span></td>
<td><span data-ttu-id="c0fb5-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-827">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-828">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-829">438.75</span><span class="sxs-lookup"><span data-stu-id="c0fb5-829">438.75</span></span></td>
<td><span data-ttu-id="c0fb5-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-831">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-831">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-832">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-833">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-833">10001</span></span></td>
<td><span data-ttu-id="c0fb5-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-834">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-835">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-836">236.25</span><span class="sxs-lookup"><span data-stu-id="c0fb5-836">236.25</span></span></td>
<td><span data-ttu-id="c0fb5-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-838">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-838">CC002</span></span></td>
<td><span data-ttu-id="c0fb5-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c0fb5-839">Finance</span></span></td>
<td><span data-ttu-id="c0fb5-840">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-840">10001</span></span></td>
<td><span data-ttu-id="c0fb5-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-841">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-842">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="c0fb5-843">-8,150.29</span></span></td>
<td><span data-ttu-id="c0fb5-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-845">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-845">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-846">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-846">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-847">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-847">10001</span></span></td>
<td><span data-ttu-id="c0fb5-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-848">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-849">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c0fb5-850">5,297.69</span></span></td>
<td><span data-ttu-id="c0fb5-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-852">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-852">CC004</span></span></td>
<td><span data-ttu-id="c0fb5-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-853">Packaging</span></span></td>
<td><span data-ttu-id="c0fb5-854">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-854">10001</span></span></td>
<td><span data-ttu-id="c0fb5-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-855">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-856">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c0fb5-857">2,852.60</span></span></td>
<td><span data-ttu-id="c0fb5-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-859">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-859">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-860">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-860">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-861">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-861">10001</span></span></td>
<td><span data-ttu-id="c0fb5-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-862">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-863">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="c0fb5-864">-713.75</span></span></td>
<td><span data-ttu-id="c0fb5-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-866">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-867">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-868">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-868">10001</span></span></td>
<td><span data-ttu-id="c0fb5-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-869">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-870">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-871">535.31</span><span class="sxs-lookup"><span data-stu-id="c0fb5-871">535.31</span></span></td>
<td><span data-ttu-id="c0fb5-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-873">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-874">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-875">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-875">10001</span></span></td>
<td><span data-ttu-id="c0fb5-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-876">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-877">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-878">178.44</span><span class="sxs-lookup"><span data-stu-id="c0fb5-878">178.44</span></span></td>
<td><span data-ttu-id="c0fb5-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-880">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-880">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-881">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-881">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-882">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-882">10001</span></span></td>
<td><span data-ttu-id="c0fb5-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-883">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-884">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="c0fb5-885">-5,982.83</span></span></td>
<td><span data-ttu-id="c0fb5-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-887">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-888">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-889">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-889">10001</span></span></td>
<td><span data-ttu-id="c0fb5-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-890">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-891">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c0fb5-892">4,487.12</span></span></td>
<td><span data-ttu-id="c0fb5-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-894">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-895">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-896">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-896">10001</span></span></td>
<td><span data-ttu-id="c0fb5-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-897">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-898">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c0fb5-899">1,495.71</span></span></td>
<td><span data-ttu-id="c0fb5-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-901">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-901">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-902">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-902">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-903">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-903">10001</span></span></td>
<td><span data-ttu-id="c0fb5-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-904">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-905">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="c0fb5-906">-286.25</span></span></td>
<td><span data-ttu-id="c0fb5-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-908">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-909">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-910">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-910">10001</span></span></td>
<td><span data-ttu-id="c0fb5-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-911">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-912">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-913">241.05</span><span class="sxs-lookup"><span data-stu-id="c0fb5-913">241.05</span></span></td>
<td><span data-ttu-id="c0fb5-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-915">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-916">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-917">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-917">10001</span></span></td>
<td><span data-ttu-id="c0fb5-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-918">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-919">Fixed cost</span></span></td>
<td><span data-ttu-id="c0fb5-920">45.20</span><span class="sxs-lookup"><span data-stu-id="c0fb5-920">45.20</span></span></td>
<td><span data-ttu-id="c0fb5-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-922">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-922">CC003</span></span></td>
<td><span data-ttu-id="c0fb5-923">Montage</span><span class="sxs-lookup"><span data-stu-id="c0fb5-923">Assembly</span></span></td>
<td><span data-ttu-id="c0fb5-924">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-924">10001</span></span></td>
<td><span data-ttu-id="c0fb5-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-925">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-926">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="c0fb5-927">-2,977.17</span></span></td>
<td><span data-ttu-id="c0fb5-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-929">Prod 1</span></span></td>
<td><span data-ttu-id="c0fb5-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-930">Product 1</span></span></td>
<td><span data-ttu-id="c0fb5-931">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-931">10001</span></span></td>
<td><span data-ttu-id="c0fb5-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-932">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-933">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c0fb5-934">2,507.09</span></span></td>
<td><span data-ttu-id="c0fb5-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0fb5-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-936">Prod 2</span></span></td>
<td><span data-ttu-id="c0fb5-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-937">Product 2</span></span></td>
<td><span data-ttu-id="c0fb5-938">10001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-938">10001</span></span></td>
<td><span data-ttu-id="c0fb5-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-939">Electricity</span></span></td>
<td><span data-ttu-id="c0fb5-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-940">Variable cost</span></span></td>
<td><span data-ttu-id="c0fb5-941">470.08</span><span class="sxs-lookup"><span data-stu-id="c0fb5-941">470.08</span></span></td>
<td><span data-ttu-id="c0fb5-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c0fb5-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c0fb5-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="c0fb5-943">Conclusion</span></span>
<span data-ttu-id="c0fb5-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c0fb5-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c0fb5-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c0fb5-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c0fb5-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c0fb5-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c0fb5-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c0fb5-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="c0fb5-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c0fb5-951">CC099</span><span class="sxs-lookup"><span data-stu-id="c0fb5-951">CC099</span></span></th>
<th><span data-ttu-id="c0fb5-952">CC001</span><span class="sxs-lookup"><span data-stu-id="c0fb5-952">CC001</span></span></th>
<th><span data-ttu-id="c0fb5-953">CC002</span><span class="sxs-lookup"><span data-stu-id="c0fb5-953">CC002</span></span></th>
<th><span data-ttu-id="c0fb5-954">CC003</span><span class="sxs-lookup"><span data-stu-id="c0fb5-954">CC003</span></span></th>
<th><span data-ttu-id="c0fb5-955">CC004</span><span class="sxs-lookup"><span data-stu-id="c0fb5-955">CC004</span></span></th>
<th><span data-ttu-id="c0fb5-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-956">Proj 1</span></span></th>
<th><span data-ttu-id="c0fb5-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-957">Proj 2</span></span></th>
<th><span data-ttu-id="c0fb5-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c0fb5-958">Prod 1</span></span></th>
<th><span data-ttu-id="c0fb5-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c0fb5-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c0fb5-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c0fb5-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c0fb5-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c0fb5-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-971">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c0fb5-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-973">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-974">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-975">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-976">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-977">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-978">776.36</span><span class="sxs-lookup"><span data-stu-id="c0fb5-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-979">223.64</span><span class="sxs-lookup"><span data-stu-id="c0fb5-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c0fb5-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c0fb5-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-982">000</span><span class="sxs-lookup"><span data-stu-id="c0fb5-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-983">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-984">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-985">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-986">0,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-987">30,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-988">10,00</span><span class="sxs-lookup"><span data-stu-id="c0fb5-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c0fb5-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c0fb5-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0fb5-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0fb5-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c0fb5-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c0fb5-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c0fb5-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c0fb5-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="c0fb5-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c0fb5-996">Weitere Informationen finden Sie unter [Kostenrollup-Richtlinie und Zuschlagsberechnung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="c0fb5-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]