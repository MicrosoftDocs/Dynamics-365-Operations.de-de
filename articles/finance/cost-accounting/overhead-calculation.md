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
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443685"
---
# <a name="overhead-calculation"></a><span data-ttu-id="c2cd6-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2cd6-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c2cd6-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="c2cd6-105">Term definition</span></span>
---------------

<span data-ttu-id="c2cd6-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c2cd6-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c2cd6-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="c2cd6-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c2cd6-109">Miete</span><span class="sxs-lookup"><span data-stu-id="c2cd6-109">Rent</span></span>
-   <span data-ttu-id="c2cd6-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-110">Electricity</span></span>
-   <span data-ttu-id="c2cd6-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="c2cd6-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c2cd6-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="c2cd6-112">Overhead calculation overview</span></span>
<span data-ttu-id="c2cd6-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c2cd6-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c2cd6-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c2cd6-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c2cd6-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c2cd6-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="c2cd6-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c2cd6-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="c2cd6-119">Version type</span></span>
-   <span data-ttu-id="c2cd6-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="c2cd6-120">Date and time</span></span>
-   <span data-ttu-id="c2cd6-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="c2cd6-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c2cd6-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="c2cd6-122">Fiscal year</span></span>
-   <span data-ttu-id="c2cd6-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="c2cd6-123">Fiscal period</span></span>

<span data-ttu-id="c2cd6-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c2cd6-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c2cd6-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c2cd6-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c2cd6-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c2cd6-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c2cd6-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c2cd6-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c2cd6-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="c2cd6-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c2cd6-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c2cd6-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c2cd6-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c2cd6-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c2cd6-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="c2cd6-140">Main account</span></span></th>
<th><span data-ttu-id="c2cd6-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-143">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-144">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-145">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-145">10001</span></span></td>
<td><span data-ttu-id="c2cd6-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-146">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c2cd6-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c2cd6-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c2cd6-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c2cd6-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="c2cd6-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c2cd6-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c2cd6-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c2cd6-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c2cd6-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="c2cd6-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c2cd6-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c2cd6-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="c2cd6-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c2cd6-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="c2cd6-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c2cd6-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-160">Journal</span></span></th>
<th><span data-ttu-id="c2cd6-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c2cd6-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c2cd6-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c2cd6-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c2cd6-163">Version</span><span class="sxs-lookup"><span data-stu-id="c2cd6-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-164">00001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-164">00001</span></span></td>
<td><span data-ttu-id="c2cd6-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c2cd6-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c2cd6-166">Fiscal</span></span></td>
<td><span data-ttu-id="c2cd6-167">2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-167">2017</span></span></td>
<td><span data-ttu-id="c2cd6-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-168">Period 1</span></span></td>
<td><span data-ttu-id="c2cd6-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c2cd6-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-173">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c2cd6-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-177">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-178">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-179">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-179">10001</span></span></td>
<td><span data-ttu-id="c2cd6-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-180">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c2cd6-181">Unclassified</span></span></td>
<td><span data-ttu-id="c2cd6-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c2cd6-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c2cd6-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-185">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c2cd6-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-187">Amount</span></span></th>
<th><span data-ttu-id="c2cd6-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-189">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-190">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-191">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-191">10001</span></span></td>
<td><span data-ttu-id="c2cd6-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-192">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c2cd6-193">Unclassified</span></span></td>
<td><span data-ttu-id="c2cd6-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-194">10,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-196">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-197">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-198">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-198">10001</span></span></td>
<td><span data-ttu-id="c2cd6-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-199">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c2cd6-200">Unclassified</span></span></td>
<td><span data-ttu-id="c2cd6-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-203">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-204">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-205">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-205">10001</span></span></td>
<td><span data-ttu-id="c2cd6-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-206">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-208">1,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-210">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-211">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-212">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-212">10001</span></span></td>
<td><span data-ttu-id="c2cd6-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-213">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-214">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-215">9,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c2cd6-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c2cd6-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c2cd6-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c2cd6-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="c2cd6-221">Define the cost distribution rule</span></span>

<span data-ttu-id="c2cd6-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c2cd6-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c2cd6-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c2cd6-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c2cd6-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c2cd6-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-228">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-229">KWH</span><span class="sxs-lookup"><span data-stu-id="c2cd6-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-230">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-230">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-231">HR</span></span></td>
<td><span data-ttu-id="c2cd6-232">1.000</span><span class="sxs-lookup"><span data-stu-id="c2cd6-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-233">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-233">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-234">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-235">6.000</span><span class="sxs-lookup"><span data-stu-id="c2cd6-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-236">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-236">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-237">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-237">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-238">0</span><span class="sxs-lookup"><span data-stu-id="c2cd6-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-240">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-241">Größe</span><span class="sxs-lookup"><span data-stu-id="c2cd6-241">Magnitude</span></span></th>
<th><span data-ttu-id="c2cd6-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c2cd6-242">Allocation factor</span></span></th>
<th><span data-ttu-id="c2cd6-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-244">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-244">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-245">HR</span></span></td>
<td><span data-ttu-id="c2cd6-246">1.000</span><span class="sxs-lookup"><span data-stu-id="c2cd6-246">1,000</span></span></td>
<td><span data-ttu-id="c2cd6-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-249">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-249">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-250">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-251">6.000</span><span class="sxs-lookup"><span data-stu-id="c2cd6-251">6,000</span></span></td>
<td><span data-ttu-id="c2cd6-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c2cd6-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-254">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-254">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-255">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-255">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-256">0</span><span class="sxs-lookup"><span data-stu-id="c2cd6-256">0</span></span></td>
<td><span data-ttu-id="c2cd6-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-258">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c2cd6-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: (Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-261">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-262">Formula</span></span></th>
<th><span data-ttu-id="c2cd6-263">Größe</span><span class="sxs-lookup"><span data-stu-id="c2cd6-263">Magnitude</span></span></th>
<th><span data-ttu-id="c2cd6-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c2cd6-264">Allocation factor</span></span></th>
<th><span data-ttu-id="c2cd6-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-266">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-266">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-267">HR</span></span></td>
<td><span data-ttu-id="c2cd6-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c2cd6-269">1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-269">1</span></span></td>
<td><span data-ttu-id="c2cd6-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-271">500,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-272">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-272">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-273">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c2cd6-275">1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-275">1</span></span></td>
<td><span data-ttu-id="c2cd6-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-277">500,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-278">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-278">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-279">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-279">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c2cd6-281">0</span><span class="sxs-lookup"><span data-stu-id="c2cd6-281">0</span></span></td>
<td><span data-ttu-id="c2cd6-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c2cd6-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-285">Journal</span></span></th>
<th><span data-ttu-id="c2cd6-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c2cd6-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c2cd6-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c2cd6-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c2cd6-288">Version</span><span class="sxs-lookup"><span data-stu-id="c2cd6-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-289">00002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-289">00002</span></span></td>
<td><span data-ttu-id="c2cd6-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c2cd6-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c2cd6-291">Fiscal</span></span></td>
<td><span data-ttu-id="c2cd6-292">2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-292">2017</span></span></td>
<td><span data-ttu-id="c2cd6-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-293">Period 1</span></span></td>
<td><span data-ttu-id="c2cd6-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c2cd6-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-298">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-299">Cost behavior</span></span></th>
<th><span data-ttu-id="c2cd6-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-302">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-302">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-303">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-304">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-304">10001</span></span></td>
<td><span data-ttu-id="c2cd6-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-305">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-306">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-309">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-309">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-310">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-311">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-311">10001</span></span></td>
<td><span data-ttu-id="c2cd6-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-312">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-313">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c2cd6-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c2cd6-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-317">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-318">Cost behavior</span></span></th>
<th><span data-ttu-id="c2cd6-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-319">Amount</span></span></th>
<th><span data-ttu-id="c2cd6-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-321">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-321">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-322">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-323">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-323">10001</span></span></td>
<td><span data-ttu-id="c2cd6-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-324">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-325">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-326">-1,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-328">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-328">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-329">HR</span></span></td>
<td><span data-ttu-id="c2cd6-330">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-330">10001</span></span></td>
<td><span data-ttu-id="c2cd6-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-331">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-332">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-333">500,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-333">500.00</span></span></td>
<td><span data-ttu-id="c2cd6-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-335">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-335">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-336">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-337">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-337">10001</span></span></td>
<td><span data-ttu-id="c2cd6-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-338">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-339">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-340">500,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-340">500.00</span></span></td>
<td><span data-ttu-id="c2cd6-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-342">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-342">CC099</span></span></td>
<td><span data-ttu-id="c2cd6-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c2cd6-343">Default cost center</span></span></td>
<td><span data-ttu-id="c2cd6-344">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-344">10001</span></span></td>
<td><span data-ttu-id="c2cd6-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-345">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-346">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-347">-9,000.00</span></span></td>
<td><span data-ttu-id="c2cd6-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-349">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-349">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-350">HR</span></span></td>
<td><span data-ttu-id="c2cd6-351">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-351">10001</span></span></td>
<td><span data-ttu-id="c2cd6-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-352">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-353">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-354">1,285.71</span></span></td>
<td><span data-ttu-id="c2cd6-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-356">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-356">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-357">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-358">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-358">10001</span></span></td>
<td><span data-ttu-id="c2cd6-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-359">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-360">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c2cd6-361">7,714.29</span></span></td>
<td><span data-ttu-id="c2cd6-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c2cd6-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c2cd6-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c2cd6-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c2cd6-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="c2cd6-367">Define the overhead rate</span></span>

<span data-ttu-id="c2cd6-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c2cd6-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-370">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="c2cd6-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-372">Proj 1</span></span></td>
<td><span data-ttu-id="c2cd6-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-373">Project 1</span></span></td>
<td><span data-ttu-id="c2cd6-374">3</span><span class="sxs-lookup"><span data-stu-id="c2cd6-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-375">Proj 2</span></span></td>
<td><span data-ttu-id="c2cd6-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-376">Project 2</span></span></td>
<td><span data-ttu-id="c2cd6-377">1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-379">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-380">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-381">Cost behavior</span></span></th>
<th><span data-ttu-id="c2cd6-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-382">Units</span></span></th>
<th><span data-ttu-id="c2cd6-383">Satz</span><span class="sxs-lookup"><span data-stu-id="c2cd6-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-384">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-384">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-385">HR</span></span></td>
<td><span data-ttu-id="c2cd6-386">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-386">10001</span></span></td>
<td><span data-ttu-id="c2cd6-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-387">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-388">1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-388">1</span></span></td>
<td><span data-ttu-id="c2cd6-389">10</span><span class="sxs-lookup"><span data-stu-id="c2cd6-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-391">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-392">Größe</span><span class="sxs-lookup"><span data-stu-id="c2cd6-392">Magnitude</span></span></th>
<th><span data-ttu-id="c2cd6-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-393">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c2cd6-394">Allocation factor</span></span></th>
<th><span data-ttu-id="c2cd6-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-396">Proj 1</span></span></td>
<td><span data-ttu-id="c2cd6-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-397">Project 1</span></span></td>
<td><span data-ttu-id="c2cd6-398">3</span><span class="sxs-lookup"><span data-stu-id="c2cd6-398">3</span></span></td>
<td><span data-ttu-id="c2cd6-399">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-399">10001</span></span></td>
<td><span data-ttu-id="c2cd6-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c2cd6-401">30,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-402">Proj 2</span></span></td>
<td><span data-ttu-id="c2cd6-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-403">Project 2</span></span></td>
<td><span data-ttu-id="c2cd6-404">1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-404">1</span></span></td>
<td><span data-ttu-id="c2cd6-405">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-405">10001</span></span></td>
<td><span data-ttu-id="c2cd6-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c2cd6-407">10,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c2cd6-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-409">Journal</span></span></th>
<th><span data-ttu-id="c2cd6-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c2cd6-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c2cd6-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c2cd6-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c2cd6-412">Version</span><span class="sxs-lookup"><span data-stu-id="c2cd6-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-413">00003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-413">00003</span></span></td>
<td><span data-ttu-id="c2cd6-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c2cd6-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c2cd6-415">Fiscal</span></span></td>
<td><span data-ttu-id="c2cd6-416">2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-416">2017</span></span></td>
<td><span data-ttu-id="c2cd6-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-417">Period 1</span></span></td>
<td><span data-ttu-id="c2cd6-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c2cd6-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-421">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-422">Größe</span><span class="sxs-lookup"><span data-stu-id="c2cd6-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-424">Proj 1</span></span></td>
<td><span data-ttu-id="c2cd6-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c2cd6-426">3,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-428">Proj 2</span></span></td>
<td><span data-ttu-id="c2cd6-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c2cd6-430">1,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c2cd6-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c2cd6-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-433">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-434">Cost behavior</span></span></th>
<th><span data-ttu-id="c2cd6-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-435">Amount</span></span></th>
<th><span data-ttu-id="c2cd6-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-437">CC0001</span></span></td>
<td><span data-ttu-id="c2cd6-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-438">HR</span></span></td>
<td><span data-ttu-id="c2cd6-439">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-439">10001</span></span></td>
<td><span data-ttu-id="c2cd6-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-440">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-441">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-442">-30.00</span></span></td>
<td><span data-ttu-id="c2cd6-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-444">Proj 1</span></span></td>
<td><span data-ttu-id="c2cd6-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c2cd6-446">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-446">10001</span></span></td>
<td><span data-ttu-id="c2cd6-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-447">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-448">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-449">30,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-449">30.00</span></span></td>
<td><span data-ttu-id="c2cd6-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-451">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-451">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-452">HR</span></span></td>
<td><span data-ttu-id="c2cd6-453">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-453">10001</span></span></td>
<td><span data-ttu-id="c2cd6-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-454">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-455">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-456">-10.00</span></span></td>
<td><span data-ttu-id="c2cd6-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-458">Proj 2</span></span></td>
<td><span data-ttu-id="c2cd6-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c2cd6-460">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-460">10001</span></span></td>
<td><span data-ttu-id="c2cd6-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-461">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-462">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-463">10.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-463">10.00</span></span></td>
<td><span data-ttu-id="c2cd6-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c2cd6-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c2cd6-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c2cd6-468">Finance unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="c2cd6-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c2cd6-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c2cd6-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c2cd6-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c2cd6-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c2cd6-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c2cd6-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="c2cd6-475">Define the cost allocation</span></span>

<span data-ttu-id="c2cd6-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c2cd6-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c2cd6-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-479">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="c2cd6-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-481">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-481">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-482">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-483">35</span><span class="sxs-lookup"><span data-stu-id="c2cd6-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-484">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-484">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-485">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-485">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-486">55</span><span class="sxs-lookup"><span data-stu-id="c2cd6-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-487">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-487">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-488">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-489">10</span><span class="sxs-lookup"><span data-stu-id="c2cd6-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c2cd6-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-492">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="c2cd6-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-494">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-494">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-495">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-495">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-496">65</span><span class="sxs-lookup"><span data-stu-id="c2cd6-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-497">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-497">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-498">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-499">35</span><span class="sxs-lookup"><span data-stu-id="c2cd6-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c2cd6-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-502">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-504">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-505">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-506">60</span><span class="sxs-lookup"><span data-stu-id="c2cd6-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-507">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-508">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-509">20</span><span class="sxs-lookup"><span data-stu-id="c2cd6-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c2cd6-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-512">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-514">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-515">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-516">80</span><span class="sxs-lookup"><span data-stu-id="c2cd6-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-517">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-518">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-519">15</span><span class="sxs-lookup"><span data-stu-id="c2cd6-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c2cd6-520">Statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, können von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c2cd6-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="c2cd6-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-523">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-524">Größe</span><span class="sxs-lookup"><span data-stu-id="c2cd6-524">Magnitude</span></span></th>
<th><span data-ttu-id="c2cd6-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c2cd6-525">Allocation factor</span></span></th>
<th><span data-ttu-id="c2cd6-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-526">Amount</span></span></th>
<th><span data-ttu-id="c2cd6-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-528">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-528">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-529">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-530">35</span><span class="sxs-lookup"><span data-stu-id="c2cd6-530">35</span></span></td>
<td><span data-ttu-id="c2cd6-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c2cd6-532">175.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-532">175.00</span></span></td>
<td><span data-ttu-id="c2cd6-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-534">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-534">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-535">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-535">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-536">55</span><span class="sxs-lookup"><span data-stu-id="c2cd6-536">55</span></span></td>
<td><span data-ttu-id="c2cd6-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c2cd6-538">275.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-538">275.00</span></span></td>
<td><span data-ttu-id="c2cd6-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-540">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-540">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-541">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-542">10</span><span class="sxs-lookup"><span data-stu-id="c2cd6-542">10</span></span></td>
<td><span data-ttu-id="c2cd6-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c2cd6-544">50,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-544">50.00</span></span></td>
<td><span data-ttu-id="c2cd6-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-546">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-546">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-547">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-548">35</span><span class="sxs-lookup"><span data-stu-id="c2cd6-548">35</span></span></td>
<td><span data-ttu-id="c2cd6-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c2cd6-550">436.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-550">436.00</span></span></td>
<td><span data-ttu-id="c2cd6-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-552">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-552">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-553">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-553">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-554">55</span><span class="sxs-lookup"><span data-stu-id="c2cd6-554">55</span></span></td>
<td><span data-ttu-id="c2cd6-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c2cd6-556">685.14</span><span class="sxs-lookup"><span data-stu-id="c2cd6-556">685.14</span></span></td>
<td><span data-ttu-id="c2cd6-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-558">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-558">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-559">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-560">10</span><span class="sxs-lookup"><span data-stu-id="c2cd6-560">10</span></span></td>
<td><span data-ttu-id="c2cd6-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c2cd6-562">124.57</span><span class="sxs-lookup"><span data-stu-id="c2cd6-562">124.57</span></span></td>
<td><span data-ttu-id="c2cd6-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-565">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-566">Größe</span><span class="sxs-lookup"><span data-stu-id="c2cd6-566">Magnitude</span></span></th>
<th><span data-ttu-id="c2cd6-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c2cd6-567">Allocation factor</span></span></th>
<th><span data-ttu-id="c2cd6-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-568">Amount</span></span></th>
<th><span data-ttu-id="c2cd6-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-570">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-570">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-571">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-571">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-572">65</span><span class="sxs-lookup"><span data-stu-id="c2cd6-572">65</span></span></td>
<td><span data-ttu-id="c2cd6-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c2cd6-574">438.75</span><span class="sxs-lookup"><span data-stu-id="c2cd6-574">438.75</span></span></td>
<td><span data-ttu-id="c2cd6-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-576">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-576">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-577">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-578">35</span><span class="sxs-lookup"><span data-stu-id="c2cd6-578">35</span></span></td>
<td><span data-ttu-id="c2cd6-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c2cd6-580">236.25</span><span class="sxs-lookup"><span data-stu-id="c2cd6-580">236.25</span></span></td>
<td><span data-ttu-id="c2cd6-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-582">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-582">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-583">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-583">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-584">65</span><span class="sxs-lookup"><span data-stu-id="c2cd6-584">65</span></span></td>
<td><span data-ttu-id="c2cd6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c2cd6-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c2cd6-586">5,297.69</span></span></td>
<td><span data-ttu-id="c2cd6-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-588">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-588">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-589">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-590">35</span><span class="sxs-lookup"><span data-stu-id="c2cd6-590">35</span></span></td>
<td><span data-ttu-id="c2cd6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c2cd6-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c2cd6-592">2,852.60</span></span></td>
<td><span data-ttu-id="c2cd6-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-595">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-596">Größe</span><span class="sxs-lookup"><span data-stu-id="c2cd6-596">Magnitude</span></span></th>
<th><span data-ttu-id="c2cd6-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c2cd6-597">Allocation factor</span></span></th>
<th><span data-ttu-id="c2cd6-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-598">Amount</span></span></th>
<th><span data-ttu-id="c2cd6-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-600">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-601">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-602">60</span><span class="sxs-lookup"><span data-stu-id="c2cd6-602">60</span></span></td>
<td><span data-ttu-id="c2cd6-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c2cd6-604">535.31</span><span class="sxs-lookup"><span data-stu-id="c2cd6-604">535.31</span></span></td>
<td><span data-ttu-id="c2cd6-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-606">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-607">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-608">20</span><span class="sxs-lookup"><span data-stu-id="c2cd6-608">20</span></span></td>
<td><span data-ttu-id="c2cd6-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c2cd6-610">178.44</span><span class="sxs-lookup"><span data-stu-id="c2cd6-610">178.44</span></span></td>
<td><span data-ttu-id="c2cd6-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-612">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-613">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-614">60</span><span class="sxs-lookup"><span data-stu-id="c2cd6-614">60</span></span></td>
<td><span data-ttu-id="c2cd6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c2cd6-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c2cd6-616">4,487.12</span></span></td>
<td><span data-ttu-id="c2cd6-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-618">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-619">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-620">20</span><span class="sxs-lookup"><span data-stu-id="c2cd6-620">20</span></span></td>
<td><span data-ttu-id="c2cd6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c2cd6-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-622">1,495.71</span></span></td>
<td><span data-ttu-id="c2cd6-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2cd6-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-625">Cost object</span></span></th>
<th><span data-ttu-id="c2cd6-626">Größe</span><span class="sxs-lookup"><span data-stu-id="c2cd6-626">Magnitude</span></span></th>
<th><span data-ttu-id="c2cd6-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c2cd6-627">Allocation factor</span></span></th>
<th><span data-ttu-id="c2cd6-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-628">Amount</span></span></th>
<th><span data-ttu-id="c2cd6-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-630">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-631">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-632">80</span><span class="sxs-lookup"><span data-stu-id="c2cd6-632">80</span></span></td>
<td><span data-ttu-id="c2cd6-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c2cd6-634">241.05</span><span class="sxs-lookup"><span data-stu-id="c2cd6-634">241.05</span></span></td>
<td><span data-ttu-id="c2cd6-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-636">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-637">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-638">15</span><span class="sxs-lookup"><span data-stu-id="c2cd6-638">15</span></span></td>
<td><span data-ttu-id="c2cd6-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c2cd6-640">45.20</span><span class="sxs-lookup"><span data-stu-id="c2cd6-640">45.20</span></span></td>
<td><span data-ttu-id="c2cd6-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-642">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-643">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-644">80</span><span class="sxs-lookup"><span data-stu-id="c2cd6-644">80</span></span></td>
<td><span data-ttu-id="c2cd6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c2cd6-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c2cd6-646">2,507.09</span></span></td>
<td><span data-ttu-id="c2cd6-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-648">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-649">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-650">15</span><span class="sxs-lookup"><span data-stu-id="c2cd6-650">15</span></span></td>
<td><span data-ttu-id="c2cd6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c2cd6-652">470.08</span><span class="sxs-lookup"><span data-stu-id="c2cd6-652">470.08</span></span></td>
<td><span data-ttu-id="c2cd6-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c2cd6-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-655">Journal</span></span></th>
<th><span data-ttu-id="c2cd6-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c2cd6-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c2cd6-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c2cd6-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c2cd6-658">Version</span><span class="sxs-lookup"><span data-stu-id="c2cd6-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-659">00004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-659">00004</span></span></td>
<td><span data-ttu-id="c2cd6-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c2cd6-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c2cd6-661">Fiscal</span></span></td>
<td><span data-ttu-id="c2cd6-662">2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-662">2017</span></span></td>
<td><span data-ttu-id="c2cd6-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-663">Period 1</span></span></td>
<td><span data-ttu-id="c2cd6-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c2cd6-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2cd6-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-668">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-669">Cost behavior</span></span></th>
<th><span data-ttu-id="c2cd6-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-672">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-672">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-673">HR</span></span></td>
<td><span data-ttu-id="c2cd6-674">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-674">10001</span></span></td>
<td><span data-ttu-id="c2cd6-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-675">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-676">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-677">500,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-679">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-679">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-680">HR</span></span></td>
<td><span data-ttu-id="c2cd6-681">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-681">10001</span></span></td>
<td><span data-ttu-id="c2cd6-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-682">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-683">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-686">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-686">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-687">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-688">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-688">10001</span></span></td>
<td><span data-ttu-id="c2cd6-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-689">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-690">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-691">675.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-693">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-693">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-694">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-695">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-695">10001</span></span></td>
<td><span data-ttu-id="c2cd6-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-696">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-697">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c2cd6-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-700">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-700">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-701">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-701">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-702">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-702">10001</span></span></td>
<td><span data-ttu-id="c2cd6-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-703">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-704">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-705">713.75</span><span class="sxs-lookup"><span data-stu-id="c2cd6-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-707">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-707">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-708">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-708">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-709">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-709">10001</span></span></td>
<td><span data-ttu-id="c2cd6-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-710">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-711">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c2cd6-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-714">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-714">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-715">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-716">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-716">10001</span></span></td>
<td><span data-ttu-id="c2cd6-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-717">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-718">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-719">286.25</span><span class="sxs-lookup"><span data-stu-id="c2cd6-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-721">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-721">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-722">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-723">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-723">10001</span></span></td>
<td><span data-ttu-id="c2cd6-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-724">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-725">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c2cd6-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-728">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-729">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-730">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-730">10001</span></span></td>
<td><span data-ttu-id="c2cd6-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-731">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-732">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-733">776.36</span><span class="sxs-lookup"><span data-stu-id="c2cd6-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-735">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-736">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-737">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-737">10001</span></span></td>
<td><span data-ttu-id="c2cd6-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-738">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-739">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c2cd6-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-742">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-743">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-744">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-744">10001</span></span></td>
<td><span data-ttu-id="c2cd6-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-745">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-746">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-747">223.64</span><span class="sxs-lookup"><span data-stu-id="c2cd6-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="c2cd6-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-749">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-750">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-751">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-751">10001</span></span></td>
<td><span data-ttu-id="c2cd6-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-752">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-753">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c2cd6-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c2cd6-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c2cd6-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c2cd6-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c2cd6-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-757">Cost element</span></span></th>
<th><span data-ttu-id="c2cd6-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-758">Cost behavior</span></span></th>
<th><span data-ttu-id="c2cd6-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-759">Amount</span></span></th>
<th><span data-ttu-id="c2cd6-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c2cd6-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2cd6-761">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-761">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-762">HR</span></span></td>
<td><span data-ttu-id="c2cd6-763">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-763">10001</span></span></td>
<td><span data-ttu-id="c2cd6-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-764">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-765">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-766">-500.00</span></span></td>
<td><span data-ttu-id="c2cd6-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-768">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-768">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-769">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-770">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-770">10001</span></span></td>
<td><span data-ttu-id="c2cd6-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-771">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-772">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-773">175.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-773">175.00</span></span></td>
<td><span data-ttu-id="c2cd6-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-775">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-775">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-776">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-776">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-777">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-777">10001</span></span></td>
<td><span data-ttu-id="c2cd6-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-778">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-779">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-780">275.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-780">275.00</span></span></td>
<td><span data-ttu-id="c2cd6-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-782">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-782">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-783">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-784">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-784">10001</span></span></td>
<td><span data-ttu-id="c2cd6-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-785">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-786">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-787">50,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-787">50,00</span></span></td>
<td><span data-ttu-id="c2cd6-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-789">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-789">CC001</span></span></td>
<td><span data-ttu-id="c2cd6-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-790">HR</span></span></td>
<td><span data-ttu-id="c2cd6-791">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-791">10001</span></span></td>
<td><span data-ttu-id="c2cd6-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-792">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-793">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-794">-1,245.71</span></span></td>
<td><span data-ttu-id="c2cd6-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-796">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-796">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-797">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-798">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-798">10001</span></span></td>
<td><span data-ttu-id="c2cd6-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-799">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-800">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-801">436.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-801">436.00</span></span></td>
<td><span data-ttu-id="c2cd6-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-803">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-803">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-804">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-804">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-805">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-805">10001</span></span></td>
<td><span data-ttu-id="c2cd6-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-806">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-807">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-808">685.14</span><span class="sxs-lookup"><span data-stu-id="c2cd6-808">685.14</span></span></td>
<td><span data-ttu-id="c2cd6-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-810">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-810">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-811">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-812">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-812">10001</span></span></td>
<td><span data-ttu-id="c2cd6-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-813">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-814">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-815">124.57</span><span class="sxs-lookup"><span data-stu-id="c2cd6-815">124.57</span></span></td>
<td><span data-ttu-id="c2cd6-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-817">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-817">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-818">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-819">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-819">10001</span></span></td>
<td><span data-ttu-id="c2cd6-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-820">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-821">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-822">-675.00</span></span></td>
<td><span data-ttu-id="c2cd6-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-824">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-824">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-825">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-825">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-826">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-826">10001</span></span></td>
<td><span data-ttu-id="c2cd6-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-827">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-828">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-829">438.75</span><span class="sxs-lookup"><span data-stu-id="c2cd6-829">438.75</span></span></td>
<td><span data-ttu-id="c2cd6-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-831">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-831">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-832">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-833">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-833">10001</span></span></td>
<td><span data-ttu-id="c2cd6-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-834">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-835">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-836">236.25</span><span class="sxs-lookup"><span data-stu-id="c2cd6-836">236.25</span></span></td>
<td><span data-ttu-id="c2cd6-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-838">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-838">CC002</span></span></td>
<td><span data-ttu-id="c2cd6-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2cd6-839">Finance</span></span></td>
<td><span data-ttu-id="c2cd6-840">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-840">10001</span></span></td>
<td><span data-ttu-id="c2cd6-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-841">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-842">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="c2cd6-843">-8,150.29</span></span></td>
<td><span data-ttu-id="c2cd6-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-845">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-845">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-846">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-846">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-847">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-847">10001</span></span></td>
<td><span data-ttu-id="c2cd6-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-848">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-849">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c2cd6-850">5,297.69</span></span></td>
<td><span data-ttu-id="c2cd6-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-852">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-852">CC004</span></span></td>
<td><span data-ttu-id="c2cd6-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-853">Packaging</span></span></td>
<td><span data-ttu-id="c2cd6-854">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-854">10001</span></span></td>
<td><span data-ttu-id="c2cd6-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-855">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-856">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c2cd6-857">2,852.60</span></span></td>
<td><span data-ttu-id="c2cd6-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-859">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-859">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-860">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-860">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-861">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-861">10001</span></span></td>
<td><span data-ttu-id="c2cd6-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-862">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-863">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="c2cd6-864">-713.75</span></span></td>
<td><span data-ttu-id="c2cd6-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-866">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-867">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-868">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-868">10001</span></span></td>
<td><span data-ttu-id="c2cd6-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-869">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-870">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-871">535.31</span><span class="sxs-lookup"><span data-stu-id="c2cd6-871">535.31</span></span></td>
<td><span data-ttu-id="c2cd6-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-873">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-874">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-875">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-875">10001</span></span></td>
<td><span data-ttu-id="c2cd6-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-876">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-877">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-878">178.44</span><span class="sxs-lookup"><span data-stu-id="c2cd6-878">178.44</span></span></td>
<td><span data-ttu-id="c2cd6-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-880">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-880">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-881">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-881">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-882">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-882">10001</span></span></td>
<td><span data-ttu-id="c2cd6-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-883">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-884">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="c2cd6-885">-5,982.83</span></span></td>
<td><span data-ttu-id="c2cd6-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-887">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-888">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-889">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-889">10001</span></span></td>
<td><span data-ttu-id="c2cd6-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-890">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-891">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c2cd6-892">4,487.12</span></span></td>
<td><span data-ttu-id="c2cd6-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-894">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-895">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-896">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-896">10001</span></span></td>
<td><span data-ttu-id="c2cd6-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-897">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-898">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c2cd6-899">1,495.71</span></span></td>
<td><span data-ttu-id="c2cd6-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-901">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-901">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-902">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-902">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-903">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-903">10001</span></span></td>
<td><span data-ttu-id="c2cd6-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-904">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-905">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="c2cd6-906">-286.25</span></span></td>
<td><span data-ttu-id="c2cd6-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-908">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-909">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-910">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-910">10001</span></span></td>
<td><span data-ttu-id="c2cd6-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-911">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-912">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-913">241.05</span><span class="sxs-lookup"><span data-stu-id="c2cd6-913">241.05</span></span></td>
<td><span data-ttu-id="c2cd6-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-915">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-916">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-917">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-917">10001</span></span></td>
<td><span data-ttu-id="c2cd6-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-918">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-919">Fixed cost</span></span></td>
<td><span data-ttu-id="c2cd6-920">45.20</span><span class="sxs-lookup"><span data-stu-id="c2cd6-920">45.20</span></span></td>
<td><span data-ttu-id="c2cd6-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-922">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-922">CC003</span></span></td>
<td><span data-ttu-id="c2cd6-923">Montage</span><span class="sxs-lookup"><span data-stu-id="c2cd6-923">Assembly</span></span></td>
<td><span data-ttu-id="c2cd6-924">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-924">10001</span></span></td>
<td><span data-ttu-id="c2cd6-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-925">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-926">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="c2cd6-927">-2,977.17</span></span></td>
<td><span data-ttu-id="c2cd6-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-929">Prod 1</span></span></td>
<td><span data-ttu-id="c2cd6-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-930">Product 1</span></span></td>
<td><span data-ttu-id="c2cd6-931">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-931">10001</span></span></td>
<td><span data-ttu-id="c2cd6-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-932">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-933">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c2cd6-934">2,507.09</span></span></td>
<td><span data-ttu-id="c2cd6-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2cd6-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-936">Prod 2</span></span></td>
<td><span data-ttu-id="c2cd6-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-937">Product 2</span></span></td>
<td><span data-ttu-id="c2cd6-938">10001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-938">10001</span></span></td>
<td><span data-ttu-id="c2cd6-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-939">Electricity</span></span></td>
<td><span data-ttu-id="c2cd6-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-940">Variable cost</span></span></td>
<td><span data-ttu-id="c2cd6-941">470.08</span><span class="sxs-lookup"><span data-stu-id="c2cd6-941">470.08</span></span></td>
<td><span data-ttu-id="c2cd6-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c2cd6-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c2cd6-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="c2cd6-943">Conclusion</span></span>
<span data-ttu-id="c2cd6-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c2cd6-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c2cd6-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c2cd6-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c2cd6-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c2cd6-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c2cd6-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c2cd6-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="c2cd6-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c2cd6-951">CC099</span><span class="sxs-lookup"><span data-stu-id="c2cd6-951">CC099</span></span></th>
<th><span data-ttu-id="c2cd6-952">CC001</span><span class="sxs-lookup"><span data-stu-id="c2cd6-952">CC001</span></span></th>
<th><span data-ttu-id="c2cd6-953">CC002</span><span class="sxs-lookup"><span data-stu-id="c2cd6-953">CC002</span></span></th>
<th><span data-ttu-id="c2cd6-954">CC003</span><span class="sxs-lookup"><span data-stu-id="c2cd6-954">CC003</span></span></th>
<th><span data-ttu-id="c2cd6-955">CC004</span><span class="sxs-lookup"><span data-stu-id="c2cd6-955">CC004</span></span></th>
<th><span data-ttu-id="c2cd6-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-956">Proj 1</span></span></th>
<th><span data-ttu-id="c2cd6-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-957">Proj 2</span></span></th>
<th><span data-ttu-id="c2cd6-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c2cd6-958">Prod 1</span></span></th>
<th><span data-ttu-id="c2cd6-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c2cd6-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c2cd6-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c2cd6-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c2cd6-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c2cd6-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-971">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c2cd6-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-973">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-974">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-975">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-976">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-977">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-978">776.36</span><span class="sxs-lookup"><span data-stu-id="c2cd6-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-979">223.64</span><span class="sxs-lookup"><span data-stu-id="c2cd6-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c2cd6-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c2cd6-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-982">000</span><span class="sxs-lookup"><span data-stu-id="c2cd6-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-983">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-984">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-985">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-986">0,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-987">30,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-988">10,00</span><span class="sxs-lookup"><span data-stu-id="c2cd6-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c2cd6-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c2cd6-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c2cd6-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c2cd6-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c2cd6-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c2cd6-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c2cd6-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c2cd6-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c2cd6-996">Weitere Informationen finden Sie unter [Kostenrollup-Richtlinie und Zuschlagsberechnung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



