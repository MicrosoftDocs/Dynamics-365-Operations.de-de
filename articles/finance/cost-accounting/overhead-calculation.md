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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759471"
---
# <a name="overhead-calculation"></a><span data-ttu-id="451c1-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="451c1-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="451c1-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="451c1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="451c1-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="451c1-105">Term definition</span></span>
---------------

<span data-ttu-id="451c1-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="451c1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="451c1-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="451c1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="451c1-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="451c1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="451c1-109">Miete</span><span class="sxs-lookup"><span data-stu-id="451c1-109">Rent</span></span>
-   <span data-ttu-id="451c1-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-110">Electricity</span></span>
-   <span data-ttu-id="451c1-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="451c1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="451c1-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="451c1-112">Overhead calculation overview</span></span>
<span data-ttu-id="451c1-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="451c1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="451c1-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="451c1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="451c1-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="451c1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="451c1-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="451c1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="451c1-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="451c1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="451c1-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="451c1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="451c1-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="451c1-119">Version type</span></span>
-   <span data-ttu-id="451c1-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="451c1-120">Date and time</span></span>
-   <span data-ttu-id="451c1-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="451c1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="451c1-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="451c1-122">Fiscal year</span></span>
-   <span data-ttu-id="451c1-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="451c1-123">Fiscal period</span></span>

<span data-ttu-id="451c1-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="451c1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="451c1-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="451c1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="451c1-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="451c1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="451c1-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="451c1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="451c1-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="451c1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="451c1-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="451c1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="451c1-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="451c1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="451c1-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="451c1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="451c1-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="451c1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="451c1-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="451c1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="451c1-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="451c1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="451c1-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="451c1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="451c1-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="451c1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="451c1-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="451c1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="451c1-140">Main account</span></span></th>
<th><span data-ttu-id="451c1-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="451c1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="451c1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-143">CC099</span></span></td>
<td><span data-ttu-id="451c1-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-144">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-145">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-145">10001</span></span></td>
<td><span data-ttu-id="451c1-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-146">Electricity</span></span></td>
<td><span data-ttu-id="451c1-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="451c1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="451c1-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="451c1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="451c1-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="451c1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="451c1-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="451c1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="451c1-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="451c1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="451c1-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="451c1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="451c1-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="451c1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="451c1-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="451c1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="451c1-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="451c1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="451c1-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="451c1-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="451c1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="451c1-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="451c1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="451c1-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="451c1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="451c1-160">Journal</span></span></th>
<th><span data-ttu-id="451c1-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="451c1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="451c1-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="451c1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="451c1-163">Version</span><span class="sxs-lookup"><span data-stu-id="451c1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-164">00001</span><span class="sxs-lookup"><span data-stu-id="451c1-164">00001</span></span></td>
<td><span data-ttu-id="451c1-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="451c1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="451c1-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="451c1-166">Fiscal</span></span></td>
<td><span data-ttu-id="451c1-167">2017</span><span class="sxs-lookup"><span data-stu-id="451c1-167">2017</span></span></td>
<td><span data-ttu-id="451c1-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="451c1-168">Period 1</span></span></td>
<td><span data-ttu-id="451c1-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="451c1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="451c1-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="451c1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-173">Cost element</span></span></th>
<th><span data-ttu-id="451c1-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="451c1-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="451c1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-177">CC099</span></span></td>
<td><span data-ttu-id="451c1-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-178">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-179">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-179">10001</span></span></td>
<td><span data-ttu-id="451c1-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-180">Electricity</span></span></td>
<td><span data-ttu-id="451c1-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="451c1-181">Unclassified</span></span></td>
<td><span data-ttu-id="451c1-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="451c1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="451c1-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="451c1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-185">Cost element</span></span></th>
<th><span data-ttu-id="451c1-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="451c1-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-187">Amount</span></span></th>
<th><span data-ttu-id="451c1-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-189">CC099</span></span></td>
<td><span data-ttu-id="451c1-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-190">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-191">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-191">10001</span></span></td>
<td><span data-ttu-id="451c1-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-192">Electricity</span></span></td>
<td><span data-ttu-id="451c1-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="451c1-193">Unclassified</span></span></td>
<td><span data-ttu-id="451c1-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="451c1-194">10,000.00</span></span></td>
<td><span data-ttu-id="451c1-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-196">CC099</span></span></td>
<td><span data-ttu-id="451c1-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-197">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-198">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-198">10001</span></span></td>
<td><span data-ttu-id="451c1-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-199">Electricity</span></span></td>
<td><span data-ttu-id="451c1-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="451c1-200">Unclassified</span></span></td>
<td><span data-ttu-id="451c1-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="451c1-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-203">CC099</span></span></td>
<td><span data-ttu-id="451c1-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-204">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-205">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-205">10001</span></span></td>
<td><span data-ttu-id="451c1-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-206">Electricity</span></span></td>
<td><span data-ttu-id="451c1-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="451c1-208">1,000.00</span></span></td>
<td><span data-ttu-id="451c1-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-210">CC099</span></span></td>
<td><span data-ttu-id="451c1-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-211">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-212">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-212">10001</span></span></td>
<td><span data-ttu-id="451c1-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-213">Electricity</span></span></td>
<td><span data-ttu-id="451c1-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-214">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="451c1-215">9,000.00</span></span></td>
<td><span data-ttu-id="451c1-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="451c1-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="451c1-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="451c1-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="451c1-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="451c1-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="451c1-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="451c1-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="451c1-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="451c1-221">Define the cost distribution rule</span></span>

<span data-ttu-id="451c1-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="451c1-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="451c1-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="451c1-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="451c1-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="451c1-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="451c1-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="451c1-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="451c1-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="451c1-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="451c1-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="451c1-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-228">Cost object</span></span></th>
<th><span data-ttu-id="451c1-229">KWH</span><span class="sxs-lookup"><span data-stu-id="451c1-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-230">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-230">CC001</span></span></td>
<td><span data-ttu-id="451c1-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-231">HR</span></span></td>
<td><span data-ttu-id="451c1-232">1.000</span><span class="sxs-lookup"><span data-stu-id="451c1-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-233">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-233">CC002</span></span></td>
<td><span data-ttu-id="451c1-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-234">Finance</span></span></td>
<td><span data-ttu-id="451c1-235">6.000</span><span class="sxs-lookup"><span data-stu-id="451c1-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-236">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-236">CC003</span></span></td>
<td><span data-ttu-id="451c1-237">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-237">Assembly</span></span></td>
<td><span data-ttu-id="451c1-238">0</span><span class="sxs-lookup"><span data-stu-id="451c1-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="451c1-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-240">Cost object</span></span></th>
<th><span data-ttu-id="451c1-241">Größe</span><span class="sxs-lookup"><span data-stu-id="451c1-241">Magnitude</span></span></th>
<th><span data-ttu-id="451c1-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="451c1-242">Allocation factor</span></span></th>
<th><span data-ttu-id="451c1-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-244">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-244">CC001</span></span></td>
<td><span data-ttu-id="451c1-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-245">HR</span></span></td>
<td><span data-ttu-id="451c1-246">1.000</span><span class="sxs-lookup"><span data-stu-id="451c1-246">1,000</span></span></td>
<td><span data-ttu-id="451c1-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="451c1-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="451c1-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-249">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-249">CC002</span></span></td>
<td><span data-ttu-id="451c1-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-250">Finance</span></span></td>
<td><span data-ttu-id="451c1-251">6.000</span><span class="sxs-lookup"><span data-stu-id="451c1-251">6,000</span></span></td>
<td><span data-ttu-id="451c1-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="451c1-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="451c1-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-254">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-254">CC003</span></span></td>
<td><span data-ttu-id="451c1-255">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-255">Assembly</span></span></td>
<td><span data-ttu-id="451c1-256">0</span><span class="sxs-lookup"><span data-stu-id="451c1-256">0</span></span></td>
<td><span data-ttu-id="451c1-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="451c1-258">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="451c1-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="451c1-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: (Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="451c1-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-261">Cost object</span></span></th>
<th><span data-ttu-id="451c1-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="451c1-262">Formula</span></span></th>
<th><span data-ttu-id="451c1-263">Größe</span><span class="sxs-lookup"><span data-stu-id="451c1-263">Magnitude</span></span></th>
<th><span data-ttu-id="451c1-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="451c1-264">Allocation factor</span></span></th>
<th><span data-ttu-id="451c1-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-266">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-266">CC001</span></span></td>
<td><span data-ttu-id="451c1-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-267">HR</span></span></td>
<td><span data-ttu-id="451c1-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="451c1-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="451c1-269">1</span><span class="sxs-lookup"><span data-stu-id="451c1-269">1</span></span></td>
<td><span data-ttu-id="451c1-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="451c1-271">500,00</span><span class="sxs-lookup"><span data-stu-id="451c1-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-272">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-272">CC002</span></span></td>
<td><span data-ttu-id="451c1-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-273">Finance</span></span></td>
<td><span data-ttu-id="451c1-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="451c1-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="451c1-275">1</span><span class="sxs-lookup"><span data-stu-id="451c1-275">1</span></span></td>
<td><span data-ttu-id="451c1-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="451c1-277">500,00</span><span class="sxs-lookup"><span data-stu-id="451c1-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-278">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-278">CC003</span></span></td>
<td><span data-ttu-id="451c1-279">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-279">Assembly</span></span></td>
<td><span data-ttu-id="451c1-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="451c1-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="451c1-281">0</span><span class="sxs-lookup"><span data-stu-id="451c1-281">0</span></span></td>
<td><span data-ttu-id="451c1-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="451c1-283">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="451c1-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="451c1-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="451c1-285">Journal</span></span></th>
<th><span data-ttu-id="451c1-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="451c1-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="451c1-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="451c1-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="451c1-288">Version</span><span class="sxs-lookup"><span data-stu-id="451c1-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-289">00002</span><span class="sxs-lookup"><span data-stu-id="451c1-289">00002</span></span></td>
<td><span data-ttu-id="451c1-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="451c1-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="451c1-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="451c1-291">Fiscal</span></span></td>
<td><span data-ttu-id="451c1-292">2017</span><span class="sxs-lookup"><span data-stu-id="451c1-292">2017</span></span></td>
<td><span data-ttu-id="451c1-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="451c1-293">Period 1</span></span></td>
<td><span data-ttu-id="451c1-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="451c1-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="451c1-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="451c1-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-298">Cost element</span></span></th>
<th><span data-ttu-id="451c1-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-299">Cost behavior</span></span></th>
<th><span data-ttu-id="451c1-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-302">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-302">CC099</span></span></td>
<td><span data-ttu-id="451c1-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-303">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-304">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-304">10001</span></span></td>
<td><span data-ttu-id="451c1-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-305">Electricity</span></span></td>
<td><span data-ttu-id="451c1-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-306">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="451c1-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-309">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-309">CC099</span></span></td>
<td><span data-ttu-id="451c1-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-310">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-311">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-311">10001</span></span></td>
<td><span data-ttu-id="451c1-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-312">Electricity</span></span></td>
<td><span data-ttu-id="451c1-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-313">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="451c1-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="451c1-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="451c1-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-317">Cost element</span></span></th>
<th><span data-ttu-id="451c1-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-318">Cost behavior</span></span></th>
<th><span data-ttu-id="451c1-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-319">Amount</span></span></th>
<th><span data-ttu-id="451c1-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-321">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-321">CC099</span></span></td>
<td><span data-ttu-id="451c1-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-322">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-323">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-323">10001</span></span></td>
<td><span data-ttu-id="451c1-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-324">Electricity</span></span></td>
<td><span data-ttu-id="451c1-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-325">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="451c1-326">-1,000.00</span></span></td>
<td><span data-ttu-id="451c1-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-328">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-328">CC001</span></span></td>
<td><span data-ttu-id="451c1-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-329">HR</span></span></td>
<td><span data-ttu-id="451c1-330">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-330">10001</span></span></td>
<td><span data-ttu-id="451c1-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-331">Electricity</span></span></td>
<td><span data-ttu-id="451c1-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-332">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-333">500,00</span><span class="sxs-lookup"><span data-stu-id="451c1-333">500.00</span></span></td>
<td><span data-ttu-id="451c1-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-335">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-335">CC002</span></span></td>
<td><span data-ttu-id="451c1-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-336">Finance</span></span></td>
<td><span data-ttu-id="451c1-337">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-337">10001</span></span></td>
<td><span data-ttu-id="451c1-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-338">Electricity</span></span></td>
<td><span data-ttu-id="451c1-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-339">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-340">500,00</span><span class="sxs-lookup"><span data-stu-id="451c1-340">500.00</span></span></td>
<td><span data-ttu-id="451c1-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-342">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-342">CC099</span></span></td>
<td><span data-ttu-id="451c1-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="451c1-343">Default cost center</span></span></td>
<td><span data-ttu-id="451c1-344">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-344">10001</span></span></td>
<td><span data-ttu-id="451c1-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-345">Electricity</span></span></td>
<td><span data-ttu-id="451c1-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-346">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="451c1-347">-9,000.00</span></span></td>
<td><span data-ttu-id="451c1-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-349">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-349">CC001</span></span></td>
<td><span data-ttu-id="451c1-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-350">HR</span></span></td>
<td><span data-ttu-id="451c1-351">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-351">10001</span></span></td>
<td><span data-ttu-id="451c1-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-352">Electricity</span></span></td>
<td><span data-ttu-id="451c1-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-353">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="451c1-354">1,285.71</span></span></td>
<td><span data-ttu-id="451c1-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-356">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-356">CC002</span></span></td>
<td><span data-ttu-id="451c1-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-357">Finance</span></span></td>
<td><span data-ttu-id="451c1-358">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-358">10001</span></span></td>
<td><span data-ttu-id="451c1-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-359">Electricity</span></span></td>
<td><span data-ttu-id="451c1-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-360">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="451c1-361">7,714.29</span></span></td>
<td><span data-ttu-id="451c1-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="451c1-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="451c1-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="451c1-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="451c1-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="451c1-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="451c1-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="451c1-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="451c1-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="451c1-367">Define the overhead rate</span></span>

<span data-ttu-id="451c1-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="451c1-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="451c1-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="451c1-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-370">Cost object</span></span></th>
<th><span data-ttu-id="451c1-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="451c1-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="451c1-372">Proj 1</span></span></td>
<td><span data-ttu-id="451c1-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-373">Project 1</span></span></td>
<td><span data-ttu-id="451c1-374">3</span><span class="sxs-lookup"><span data-stu-id="451c1-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="451c1-375">Proj 2</span></span></td>
<td><span data-ttu-id="451c1-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-376">Project 2</span></span></td>
<td><span data-ttu-id="451c1-377">1</span><span class="sxs-lookup"><span data-stu-id="451c1-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="451c1-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-379">Cost object</span></span></th>
<th><span data-ttu-id="451c1-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-380">Cost element</span></span></th>
<th><span data-ttu-id="451c1-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-381">Cost behavior</span></span></th>
<th><span data-ttu-id="451c1-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="451c1-382">Units</span></span></th>
<th><span data-ttu-id="451c1-383">Satz</span><span class="sxs-lookup"><span data-stu-id="451c1-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-384">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-384">CC001</span></span></td>
<td><span data-ttu-id="451c1-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-385">HR</span></span></td>
<td><span data-ttu-id="451c1-386">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-386">10001</span></span></td>
<td><span data-ttu-id="451c1-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-387">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-388">1</span><span class="sxs-lookup"><span data-stu-id="451c1-388">1</span></span></td>
<td><span data-ttu-id="451c1-389">10</span><span class="sxs-lookup"><span data-stu-id="451c1-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="451c1-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-391">Cost object</span></span></th>
<th><span data-ttu-id="451c1-392">Größe</span><span class="sxs-lookup"><span data-stu-id="451c1-392">Magnitude</span></span></th>
<th><span data-ttu-id="451c1-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-393">Cost element</span></span></th>
<th><span data-ttu-id="451c1-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="451c1-394">Allocation factor</span></span></th>
<th><span data-ttu-id="451c1-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="451c1-396">Proj 1</span></span></td>
<td><span data-ttu-id="451c1-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-397">Project 1</span></span></td>
<td><span data-ttu-id="451c1-398">3</span><span class="sxs-lookup"><span data-stu-id="451c1-398">3</span></span></td>
<td><span data-ttu-id="451c1-399">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-399">10001</span></span></td>
<td><span data-ttu-id="451c1-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="451c1-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="451c1-401">30,00</span><span class="sxs-lookup"><span data-stu-id="451c1-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="451c1-402">Proj 2</span></span></td>
<td><span data-ttu-id="451c1-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-403">Project 2</span></span></td>
<td><span data-ttu-id="451c1-404">1</span><span class="sxs-lookup"><span data-stu-id="451c1-404">1</span></span></td>
<td><span data-ttu-id="451c1-405">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-405">10001</span></span></td>
<td><span data-ttu-id="451c1-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="451c1-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="451c1-407">10,00</span><span class="sxs-lookup"><span data-stu-id="451c1-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="451c1-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="451c1-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="451c1-409">Journal</span></span></th>
<th><span data-ttu-id="451c1-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="451c1-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="451c1-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="451c1-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="451c1-412">Version</span><span class="sxs-lookup"><span data-stu-id="451c1-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-413">00003</span><span class="sxs-lookup"><span data-stu-id="451c1-413">00003</span></span></td>
<td><span data-ttu-id="451c1-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="451c1-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="451c1-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="451c1-415">Fiscal</span></span></td>
<td><span data-ttu-id="451c1-416">2017</span><span class="sxs-lookup"><span data-stu-id="451c1-416">2017</span></span></td>
<td><span data-ttu-id="451c1-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="451c1-417">Period 1</span></span></td>
<td><span data-ttu-id="451c1-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="451c1-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="451c1-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="451c1-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-421">Cost object</span></span></th>
<th><span data-ttu-id="451c1-422">Größe</span><span class="sxs-lookup"><span data-stu-id="451c1-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="451c1-424">Proj 1</span></span></td>
<td><span data-ttu-id="451c1-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="451c1-426">3,00</span><span class="sxs-lookup"><span data-stu-id="451c1-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="451c1-428">Proj 2</span></span></td>
<td><span data-ttu-id="451c1-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="451c1-430">1,00</span><span class="sxs-lookup"><span data-stu-id="451c1-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="451c1-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="451c1-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-433">Cost element</span></span></th>
<th><span data-ttu-id="451c1-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-434">Cost behavior</span></span></th>
<th><span data-ttu-id="451c1-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-435">Amount</span></span></th>
<th><span data-ttu-id="451c1-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="451c1-437">CC0001</span></span></td>
<td><span data-ttu-id="451c1-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-438">HR</span></span></td>
<td><span data-ttu-id="451c1-439">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-439">10001</span></span></td>
<td><span data-ttu-id="451c1-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-440">Electricity</span></span></td>
<td><span data-ttu-id="451c1-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-441">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="451c1-442">-30.00</span></span></td>
<td><span data-ttu-id="451c1-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="451c1-444">Proj 1</span></span></td>
<td><span data-ttu-id="451c1-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="451c1-446">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-446">10001</span></span></td>
<td><span data-ttu-id="451c1-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-447">Electricity</span></span></td>
<td><span data-ttu-id="451c1-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-448">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-449">30,00</span><span class="sxs-lookup"><span data-stu-id="451c1-449">30.00</span></span></td>
<td><span data-ttu-id="451c1-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-451">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-451">CC001</span></span></td>
<td><span data-ttu-id="451c1-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-452">HR</span></span></td>
<td><span data-ttu-id="451c1-453">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-453">10001</span></span></td>
<td><span data-ttu-id="451c1-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-454">Electricity</span></span></td>
<td><span data-ttu-id="451c1-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-455">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="451c1-456">-10.00</span></span></td>
<td><span data-ttu-id="451c1-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="451c1-458">Proj 2</span></span></td>
<td><span data-ttu-id="451c1-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="451c1-460">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-460">10001</span></span></td>
<td><span data-ttu-id="451c1-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-461">Electricity</span></span></td>
<td><span data-ttu-id="451c1-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-462">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-463">10.00</span><span class="sxs-lookup"><span data-stu-id="451c1-463">10.00</span></span></td>
<td><span data-ttu-id="451c1-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="451c1-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="451c1-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="451c1-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="451c1-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="451c1-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="451c1-468">Finance unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="451c1-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="451c1-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="451c1-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="451c1-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="451c1-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="451c1-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="451c1-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="451c1-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="451c1-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="451c1-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="451c1-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="451c1-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="451c1-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="451c1-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="451c1-475">Define the cost allocation</span></span>

<span data-ttu-id="451c1-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="451c1-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="451c1-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="451c1-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="451c1-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="451c1-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-479">Cost object</span></span></th>
<th><span data-ttu-id="451c1-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="451c1-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-481">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-481">CC002</span></span></td>
<td><span data-ttu-id="451c1-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-482">Finance</span></span></td>
<td><span data-ttu-id="451c1-483">35</span><span class="sxs-lookup"><span data-stu-id="451c1-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-484">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-484">CC003</span></span></td>
<td><span data-ttu-id="451c1-485">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-485">Assembly</span></span></td>
<td><span data-ttu-id="451c1-486">55</span><span class="sxs-lookup"><span data-stu-id="451c1-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-487">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-487">CC004</span></span></td>
<td><span data-ttu-id="451c1-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-488">Packaging</span></span></td>
<td><span data-ttu-id="451c1-489">10</span><span class="sxs-lookup"><span data-stu-id="451c1-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="451c1-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="451c1-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="451c1-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-492">Cost object</span></span></th>
<th><span data-ttu-id="451c1-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="451c1-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-494">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-494">CC003</span></span></td>
<td><span data-ttu-id="451c1-495">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-495">Assembly</span></span></td>
<td><span data-ttu-id="451c1-496">65</span><span class="sxs-lookup"><span data-stu-id="451c1-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-497">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-497">CC004</span></span></td>
<td><span data-ttu-id="451c1-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-498">Packaging</span></span></td>
<td><span data-ttu-id="451c1-499">35</span><span class="sxs-lookup"><span data-stu-id="451c1-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="451c1-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="451c1-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="451c1-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-502">Cost object</span></span></th>
<th><span data-ttu-id="451c1-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="451c1-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-504">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-505">Product 1</span></span></td>
<td><span data-ttu-id="451c1-506">60</span><span class="sxs-lookup"><span data-stu-id="451c1-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-507">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-508">Product 2</span></span></td>
<td><span data-ttu-id="451c1-509">20</span><span class="sxs-lookup"><span data-stu-id="451c1-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="451c1-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="451c1-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="451c1-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-512">Cost object</span></span></th>
<th><span data-ttu-id="451c1-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="451c1-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-514">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-515">Product 1</span></span></td>
<td><span data-ttu-id="451c1-516">80</span><span class="sxs-lookup"><span data-stu-id="451c1-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-517">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-518">Product 2</span></span></td>
<td><span data-ttu-id="451c1-519">15</span><span class="sxs-lookup"><span data-stu-id="451c1-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="451c1-520">Statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, können von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="451c1-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="451c1-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="451c1-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="451c1-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="451c1-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-523">Cost object</span></span></th>
<th><span data-ttu-id="451c1-524">Größe</span><span class="sxs-lookup"><span data-stu-id="451c1-524">Magnitude</span></span></th>
<th><span data-ttu-id="451c1-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="451c1-525">Allocation factor</span></span></th>
<th><span data-ttu-id="451c1-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-526">Amount</span></span></th>
<th><span data-ttu-id="451c1-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-528">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-528">CC002</span></span></td>
<td><span data-ttu-id="451c1-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-529">Finance</span></span></td>
<td><span data-ttu-id="451c1-530">35</span><span class="sxs-lookup"><span data-stu-id="451c1-530">35</span></span></td>
<td><span data-ttu-id="451c1-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="451c1-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="451c1-532">175.00</span><span class="sxs-lookup"><span data-stu-id="451c1-532">175.00</span></span></td>
<td><span data-ttu-id="451c1-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-534">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-534">CC003</span></span></td>
<td><span data-ttu-id="451c1-535">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-535">Assembly</span></span></td>
<td><span data-ttu-id="451c1-536">55</span><span class="sxs-lookup"><span data-stu-id="451c1-536">55</span></span></td>
<td><span data-ttu-id="451c1-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="451c1-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="451c1-538">275.00</span><span class="sxs-lookup"><span data-stu-id="451c1-538">275.00</span></span></td>
<td><span data-ttu-id="451c1-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-540">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-540">CC004</span></span></td>
<td><span data-ttu-id="451c1-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-541">Packaging</span></span></td>
<td><span data-ttu-id="451c1-542">10</span><span class="sxs-lookup"><span data-stu-id="451c1-542">10</span></span></td>
<td><span data-ttu-id="451c1-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="451c1-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="451c1-544">50,00</span><span class="sxs-lookup"><span data-stu-id="451c1-544">50.00</span></span></td>
<td><span data-ttu-id="451c1-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-546">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-546">CC002</span></span></td>
<td><span data-ttu-id="451c1-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-547">Finance</span></span></td>
<td><span data-ttu-id="451c1-548">35</span><span class="sxs-lookup"><span data-stu-id="451c1-548">35</span></span></td>
<td><span data-ttu-id="451c1-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="451c1-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="451c1-550">436.00</span><span class="sxs-lookup"><span data-stu-id="451c1-550">436.00</span></span></td>
<td><span data-ttu-id="451c1-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-552">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-552">CC003</span></span></td>
<td><span data-ttu-id="451c1-553">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-553">Assembly</span></span></td>
<td><span data-ttu-id="451c1-554">55</span><span class="sxs-lookup"><span data-stu-id="451c1-554">55</span></span></td>
<td><span data-ttu-id="451c1-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="451c1-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="451c1-556">685.14</span><span class="sxs-lookup"><span data-stu-id="451c1-556">685.14</span></span></td>
<td><span data-ttu-id="451c1-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-558">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-558">CC004</span></span></td>
<td><span data-ttu-id="451c1-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-559">Packaging</span></span></td>
<td><span data-ttu-id="451c1-560">10</span><span class="sxs-lookup"><span data-stu-id="451c1-560">10</span></span></td>
<td><span data-ttu-id="451c1-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="451c1-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="451c1-562">124.57</span><span class="sxs-lookup"><span data-stu-id="451c1-562">124.57</span></span></td>
<td><span data-ttu-id="451c1-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="451c1-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-565">Cost object</span></span></th>
<th><span data-ttu-id="451c1-566">Größe</span><span class="sxs-lookup"><span data-stu-id="451c1-566">Magnitude</span></span></th>
<th><span data-ttu-id="451c1-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="451c1-567">Allocation factor</span></span></th>
<th><span data-ttu-id="451c1-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-568">Amount</span></span></th>
<th><span data-ttu-id="451c1-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-570">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-570">CC003</span></span></td>
<td><span data-ttu-id="451c1-571">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-571">Assembly</span></span></td>
<td><span data-ttu-id="451c1-572">65</span><span class="sxs-lookup"><span data-stu-id="451c1-572">65</span></span></td>
<td><span data-ttu-id="451c1-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="451c1-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="451c1-574">438.75</span><span class="sxs-lookup"><span data-stu-id="451c1-574">438.75</span></span></td>
<td><span data-ttu-id="451c1-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-576">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-576">CC004</span></span></td>
<td><span data-ttu-id="451c1-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-577">Packaging</span></span></td>
<td><span data-ttu-id="451c1-578">35</span><span class="sxs-lookup"><span data-stu-id="451c1-578">35</span></span></td>
<td><span data-ttu-id="451c1-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="451c1-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="451c1-580">236.25</span><span class="sxs-lookup"><span data-stu-id="451c1-580">236.25</span></span></td>
<td><span data-ttu-id="451c1-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-582">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-582">CC003</span></span></td>
<td><span data-ttu-id="451c1-583">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-583">Assembly</span></span></td>
<td><span data-ttu-id="451c1-584">65</span><span class="sxs-lookup"><span data-stu-id="451c1-584">65</span></span></td>
<td><span data-ttu-id="451c1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="451c1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="451c1-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="451c1-586">5,297.69</span></span></td>
<td><span data-ttu-id="451c1-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-588">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-588">CC004</span></span></td>
<td><span data-ttu-id="451c1-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-589">Packaging</span></span></td>
<td><span data-ttu-id="451c1-590">35</span><span class="sxs-lookup"><span data-stu-id="451c1-590">35</span></span></td>
<td><span data-ttu-id="451c1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="451c1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="451c1-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="451c1-592">2,852.60</span></span></td>
<td><span data-ttu-id="451c1-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="451c1-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-595">Cost object</span></span></th>
<th><span data-ttu-id="451c1-596">Größe</span><span class="sxs-lookup"><span data-stu-id="451c1-596">Magnitude</span></span></th>
<th><span data-ttu-id="451c1-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="451c1-597">Allocation factor</span></span></th>
<th><span data-ttu-id="451c1-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-598">Amount</span></span></th>
<th><span data-ttu-id="451c1-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-600">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-601">Product 1</span></span></td>
<td><span data-ttu-id="451c1-602">60</span><span class="sxs-lookup"><span data-stu-id="451c1-602">60</span></span></td>
<td><span data-ttu-id="451c1-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="451c1-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="451c1-604">535.31</span><span class="sxs-lookup"><span data-stu-id="451c1-604">535.31</span></span></td>
<td><span data-ttu-id="451c1-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-606">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-607">Product 2</span></span></td>
<td><span data-ttu-id="451c1-608">20</span><span class="sxs-lookup"><span data-stu-id="451c1-608">20</span></span></td>
<td><span data-ttu-id="451c1-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="451c1-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="451c1-610">178.44</span><span class="sxs-lookup"><span data-stu-id="451c1-610">178.44</span></span></td>
<td><span data-ttu-id="451c1-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-612">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-613">Product 1</span></span></td>
<td><span data-ttu-id="451c1-614">60</span><span class="sxs-lookup"><span data-stu-id="451c1-614">60</span></span></td>
<td><span data-ttu-id="451c1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="451c1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="451c1-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="451c1-616">4,487.12</span></span></td>
<td><span data-ttu-id="451c1-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-618">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-619">Product 2</span></span></td>
<td><span data-ttu-id="451c1-620">20</span><span class="sxs-lookup"><span data-stu-id="451c1-620">20</span></span></td>
<td><span data-ttu-id="451c1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="451c1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="451c1-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="451c1-622">1,495.71</span></span></td>
<td><span data-ttu-id="451c1-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="451c1-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="451c1-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-625">Cost object</span></span></th>
<th><span data-ttu-id="451c1-626">Größe</span><span class="sxs-lookup"><span data-stu-id="451c1-626">Magnitude</span></span></th>
<th><span data-ttu-id="451c1-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="451c1-627">Allocation factor</span></span></th>
<th><span data-ttu-id="451c1-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-628">Amount</span></span></th>
<th><span data-ttu-id="451c1-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-630">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-631">Product 1</span></span></td>
<td><span data-ttu-id="451c1-632">80</span><span class="sxs-lookup"><span data-stu-id="451c1-632">80</span></span></td>
<td><span data-ttu-id="451c1-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="451c1-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="451c1-634">241.05</span><span class="sxs-lookup"><span data-stu-id="451c1-634">241.05</span></span></td>
<td><span data-ttu-id="451c1-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-636">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-637">Product 2</span></span></td>
<td><span data-ttu-id="451c1-638">15</span><span class="sxs-lookup"><span data-stu-id="451c1-638">15</span></span></td>
<td><span data-ttu-id="451c1-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="451c1-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="451c1-640">45.20</span><span class="sxs-lookup"><span data-stu-id="451c1-640">45.20</span></span></td>
<td><span data-ttu-id="451c1-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-642">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-643">Product 1</span></span></td>
<td><span data-ttu-id="451c1-644">80</span><span class="sxs-lookup"><span data-stu-id="451c1-644">80</span></span></td>
<td><span data-ttu-id="451c1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="451c1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="451c1-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="451c1-646">2,507.09</span></span></td>
<td><span data-ttu-id="451c1-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-648">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-649">Product 2</span></span></td>
<td><span data-ttu-id="451c1-650">15</span><span class="sxs-lookup"><span data-stu-id="451c1-650">15</span></span></td>
<td><span data-ttu-id="451c1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="451c1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="451c1-652">470.08</span><span class="sxs-lookup"><span data-stu-id="451c1-652">470.08</span></span></td>
<td><span data-ttu-id="451c1-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="451c1-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="451c1-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="451c1-655">Journal</span></span></th>
<th><span data-ttu-id="451c1-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="451c1-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="451c1-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="451c1-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="451c1-658">Version</span><span class="sxs-lookup"><span data-stu-id="451c1-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-659">00004</span><span class="sxs-lookup"><span data-stu-id="451c1-659">00004</span></span></td>
<td><span data-ttu-id="451c1-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="451c1-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="451c1-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="451c1-661">Fiscal</span></span></td>
<td><span data-ttu-id="451c1-662">2017</span><span class="sxs-lookup"><span data-stu-id="451c1-662">2017</span></span></td>
<td><span data-ttu-id="451c1-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="451c1-663">Period 1</span></span></td>
<td><span data-ttu-id="451c1-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="451c1-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="451c1-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="451c1-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="451c1-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-668">Cost element</span></span></th>
<th><span data-ttu-id="451c1-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-669">Cost behavior</span></span></th>
<th><span data-ttu-id="451c1-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-672">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-672">CC001</span></span></td>
<td><span data-ttu-id="451c1-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-673">HR</span></span></td>
<td><span data-ttu-id="451c1-674">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-674">10001</span></span></td>
<td><span data-ttu-id="451c1-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-675">Electricity</span></span></td>
<td><span data-ttu-id="451c1-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-676">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-677">500,00</span><span class="sxs-lookup"><span data-stu-id="451c1-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-679">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-679">CC001</span></span></td>
<td><span data-ttu-id="451c1-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-680">HR</span></span></td>
<td><span data-ttu-id="451c1-681">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-681">10001</span></span></td>
<td><span data-ttu-id="451c1-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-682">Electricity</span></span></td>
<td><span data-ttu-id="451c1-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-683">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="451c1-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-686">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-686">CC002</span></span></td>
<td><span data-ttu-id="451c1-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-687">Finance</span></span></td>
<td><span data-ttu-id="451c1-688">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-688">10001</span></span></td>
<td><span data-ttu-id="451c1-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-689">Electricity</span></span></td>
<td><span data-ttu-id="451c1-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-690">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-691">675.00</span><span class="sxs-lookup"><span data-stu-id="451c1-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-693">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-693">CC002</span></span></td>
<td><span data-ttu-id="451c1-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-694">Finance</span></span></td>
<td><span data-ttu-id="451c1-695">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-695">10001</span></span></td>
<td><span data-ttu-id="451c1-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-696">Electricity</span></span></td>
<td><span data-ttu-id="451c1-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-697">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="451c1-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-700">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-700">CC003</span></span></td>
<td><span data-ttu-id="451c1-701">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-701">Assembly</span></span></td>
<td><span data-ttu-id="451c1-702">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-702">10001</span></span></td>
<td><span data-ttu-id="451c1-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-703">Electricity</span></span></td>
<td><span data-ttu-id="451c1-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-704">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-705">713.75</span><span class="sxs-lookup"><span data-stu-id="451c1-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-707">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-707">CC003</span></span></td>
<td><span data-ttu-id="451c1-708">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-708">Assembly</span></span></td>
<td><span data-ttu-id="451c1-709">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-709">10001</span></span></td>
<td><span data-ttu-id="451c1-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-710">Electricity</span></span></td>
<td><span data-ttu-id="451c1-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-711">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="451c1-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-714">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-714">CC003</span></span></td>
<td><span data-ttu-id="451c1-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-715">Packaging</span></span></td>
<td><span data-ttu-id="451c1-716">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-716">10001</span></span></td>
<td><span data-ttu-id="451c1-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-717">Electricity</span></span></td>
<td><span data-ttu-id="451c1-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-718">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-719">286.25</span><span class="sxs-lookup"><span data-stu-id="451c1-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-721">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-721">CC003</span></span></td>
<td><span data-ttu-id="451c1-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-722">Packaging</span></span></td>
<td><span data-ttu-id="451c1-723">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-723">10001</span></span></td>
<td><span data-ttu-id="451c1-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-724">Electricity</span></span></td>
<td><span data-ttu-id="451c1-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-725">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="451c1-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-728">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-729">Product 1</span></span></td>
<td><span data-ttu-id="451c1-730">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-730">10001</span></span></td>
<td><span data-ttu-id="451c1-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-731">Electricity</span></span></td>
<td><span data-ttu-id="451c1-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-732">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-733">776.36</span><span class="sxs-lookup"><span data-stu-id="451c1-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-735">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-736">Product 1</span></span></td>
<td><span data-ttu-id="451c1-737">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-737">10001</span></span></td>
<td><span data-ttu-id="451c1-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-738">Electricity</span></span></td>
<td><span data-ttu-id="451c1-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-739">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="451c1-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-742">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-743">Product 1</span></span></td>
<td><span data-ttu-id="451c1-744">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-744">10001</span></span></td>
<td><span data-ttu-id="451c1-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-745">Electricity</span></span></td>
<td><span data-ttu-id="451c1-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-746">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-747">223.64</span><span class="sxs-lookup"><span data-stu-id="451c1-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="451c1-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-749">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-750">Product 1</span></span></td>
<td><span data-ttu-id="451c1-751">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-751">10001</span></span></td>
<td><span data-ttu-id="451c1-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-752">Electricity</span></span></td>
<td><span data-ttu-id="451c1-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-753">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="451c1-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="451c1-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="451c1-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="451c1-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="451c1-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-757">Cost element</span></span></th>
<th><span data-ttu-id="451c1-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="451c1-758">Cost behavior</span></span></th>
<th><span data-ttu-id="451c1-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="451c1-759">Amount</span></span></th>
<th><span data-ttu-id="451c1-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="451c1-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="451c1-761">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-761">CC001</span></span></td>
<td><span data-ttu-id="451c1-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-762">HR</span></span></td>
<td><span data-ttu-id="451c1-763">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-763">10001</span></span></td>
<td><span data-ttu-id="451c1-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-764">Electricity</span></span></td>
<td><span data-ttu-id="451c1-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-765">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="451c1-766">-500.00</span></span></td>
<td><span data-ttu-id="451c1-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-768">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-768">CC002</span></span></td>
<td><span data-ttu-id="451c1-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-769">Finance</span></span></td>
<td><span data-ttu-id="451c1-770">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-770">10001</span></span></td>
<td><span data-ttu-id="451c1-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-771">Electricity</span></span></td>
<td><span data-ttu-id="451c1-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-772">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-773">175.00</span><span class="sxs-lookup"><span data-stu-id="451c1-773">175.00</span></span></td>
<td><span data-ttu-id="451c1-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-775">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-775">CC003</span></span></td>
<td><span data-ttu-id="451c1-776">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-776">Assembly</span></span></td>
<td><span data-ttu-id="451c1-777">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-777">10001</span></span></td>
<td><span data-ttu-id="451c1-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-778">Electricity</span></span></td>
<td><span data-ttu-id="451c1-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-779">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-780">275.00</span><span class="sxs-lookup"><span data-stu-id="451c1-780">275.00</span></span></td>
<td><span data-ttu-id="451c1-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-782">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-782">CC004</span></span></td>
<td><span data-ttu-id="451c1-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-783">Packaging</span></span></td>
<td><span data-ttu-id="451c1-784">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-784">10001</span></span></td>
<td><span data-ttu-id="451c1-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-785">Electricity</span></span></td>
<td><span data-ttu-id="451c1-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-786">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-787">50,00</span><span class="sxs-lookup"><span data-stu-id="451c1-787">50,00</span></span></td>
<td><span data-ttu-id="451c1-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-789">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-789">CC001</span></span></td>
<td><span data-ttu-id="451c1-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="451c1-790">HR</span></span></td>
<td><span data-ttu-id="451c1-791">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-791">10001</span></span></td>
<td><span data-ttu-id="451c1-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-792">Electricity</span></span></td>
<td><span data-ttu-id="451c1-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-793">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="451c1-794">-1,245.71</span></span></td>
<td><span data-ttu-id="451c1-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-796">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-796">CC002</span></span></td>
<td><span data-ttu-id="451c1-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-797">Finance</span></span></td>
<td><span data-ttu-id="451c1-798">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-798">10001</span></span></td>
<td><span data-ttu-id="451c1-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-799">Electricity</span></span></td>
<td><span data-ttu-id="451c1-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-800">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-801">436.00</span><span class="sxs-lookup"><span data-stu-id="451c1-801">436.00</span></span></td>
<td><span data-ttu-id="451c1-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-803">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-803">CC003</span></span></td>
<td><span data-ttu-id="451c1-804">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-804">Assembly</span></span></td>
<td><span data-ttu-id="451c1-805">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-805">10001</span></span></td>
<td><span data-ttu-id="451c1-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-806">Electricity</span></span></td>
<td><span data-ttu-id="451c1-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-807">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-808">685.14</span><span class="sxs-lookup"><span data-stu-id="451c1-808">685.14</span></span></td>
<td><span data-ttu-id="451c1-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-810">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-810">CC004</span></span></td>
<td><span data-ttu-id="451c1-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-811">Packaging</span></span></td>
<td><span data-ttu-id="451c1-812">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-812">10001</span></span></td>
<td><span data-ttu-id="451c1-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-813">Electricity</span></span></td>
<td><span data-ttu-id="451c1-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-814">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-815">124.57</span><span class="sxs-lookup"><span data-stu-id="451c1-815">124.57</span></span></td>
<td><span data-ttu-id="451c1-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-817">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-817">CC002</span></span></td>
<td><span data-ttu-id="451c1-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-818">Finance</span></span></td>
<td><span data-ttu-id="451c1-819">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-819">10001</span></span></td>
<td><span data-ttu-id="451c1-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-820">Electricity</span></span></td>
<td><span data-ttu-id="451c1-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-821">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="451c1-822">-675.00</span></span></td>
<td><span data-ttu-id="451c1-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-824">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-824">CC003</span></span></td>
<td><span data-ttu-id="451c1-825">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-825">Assembly</span></span></td>
<td><span data-ttu-id="451c1-826">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-826">10001</span></span></td>
<td><span data-ttu-id="451c1-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-827">Electricity</span></span></td>
<td><span data-ttu-id="451c1-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-828">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-829">438.75</span><span class="sxs-lookup"><span data-stu-id="451c1-829">438.75</span></span></td>
<td><span data-ttu-id="451c1-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-831">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-831">CC004</span></span></td>
<td><span data-ttu-id="451c1-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-832">Packaging</span></span></td>
<td><span data-ttu-id="451c1-833">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-833">10001</span></span></td>
<td><span data-ttu-id="451c1-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-834">Electricity</span></span></td>
<td><span data-ttu-id="451c1-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-835">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-836">236.25</span><span class="sxs-lookup"><span data-stu-id="451c1-836">236.25</span></span></td>
<td><span data-ttu-id="451c1-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-838">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-838">CC002</span></span></td>
<td><span data-ttu-id="451c1-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="451c1-839">Finance</span></span></td>
<td><span data-ttu-id="451c1-840">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-840">10001</span></span></td>
<td><span data-ttu-id="451c1-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-841">Electricity</span></span></td>
<td><span data-ttu-id="451c1-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-842">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="451c1-843">-8,150.29</span></span></td>
<td><span data-ttu-id="451c1-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-845">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-845">CC003</span></span></td>
<td><span data-ttu-id="451c1-846">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-846">Assembly</span></span></td>
<td><span data-ttu-id="451c1-847">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-847">10001</span></span></td>
<td><span data-ttu-id="451c1-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-848">Electricity</span></span></td>
<td><span data-ttu-id="451c1-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-849">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="451c1-850">5,297.69</span></span></td>
<td><span data-ttu-id="451c1-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-852">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-852">CC004</span></span></td>
<td><span data-ttu-id="451c1-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="451c1-853">Packaging</span></span></td>
<td><span data-ttu-id="451c1-854">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-854">10001</span></span></td>
<td><span data-ttu-id="451c1-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-855">Electricity</span></span></td>
<td><span data-ttu-id="451c1-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-856">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="451c1-857">2,852.60</span></span></td>
<td><span data-ttu-id="451c1-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-859">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-859">CC003</span></span></td>
<td><span data-ttu-id="451c1-860">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-860">Assembly</span></span></td>
<td><span data-ttu-id="451c1-861">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-861">10001</span></span></td>
<td><span data-ttu-id="451c1-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-862">Electricity</span></span></td>
<td><span data-ttu-id="451c1-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-863">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="451c1-864">-713.75</span></span></td>
<td><span data-ttu-id="451c1-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-866">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-867">Product 1</span></span></td>
<td><span data-ttu-id="451c1-868">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-868">10001</span></span></td>
<td><span data-ttu-id="451c1-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-869">Electricity</span></span></td>
<td><span data-ttu-id="451c1-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-870">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-871">535.31</span><span class="sxs-lookup"><span data-stu-id="451c1-871">535.31</span></span></td>
<td><span data-ttu-id="451c1-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-873">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-874">Product 2</span></span></td>
<td><span data-ttu-id="451c1-875">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-875">10001</span></span></td>
<td><span data-ttu-id="451c1-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-876">Electricity</span></span></td>
<td><span data-ttu-id="451c1-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-877">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-878">178.44</span><span class="sxs-lookup"><span data-stu-id="451c1-878">178.44</span></span></td>
<td><span data-ttu-id="451c1-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-880">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-880">CC003</span></span></td>
<td><span data-ttu-id="451c1-881">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-881">Assembly</span></span></td>
<td><span data-ttu-id="451c1-882">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-882">10001</span></span></td>
<td><span data-ttu-id="451c1-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-883">Electricity</span></span></td>
<td><span data-ttu-id="451c1-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-884">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="451c1-885">-5,982.83</span></span></td>
<td><span data-ttu-id="451c1-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-887">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-888">Product 1</span></span></td>
<td><span data-ttu-id="451c1-889">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-889">10001</span></span></td>
<td><span data-ttu-id="451c1-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-890">Electricity</span></span></td>
<td><span data-ttu-id="451c1-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-891">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="451c1-892">4,487.12</span></span></td>
<td><span data-ttu-id="451c1-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-894">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-895">Product 2</span></span></td>
<td><span data-ttu-id="451c1-896">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-896">10001</span></span></td>
<td><span data-ttu-id="451c1-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-897">Electricity</span></span></td>
<td><span data-ttu-id="451c1-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-898">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="451c1-899">1,495.71</span></span></td>
<td><span data-ttu-id="451c1-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-901">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-901">CC003</span></span></td>
<td><span data-ttu-id="451c1-902">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-902">Assembly</span></span></td>
<td><span data-ttu-id="451c1-903">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-903">10001</span></span></td>
<td><span data-ttu-id="451c1-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-904">Electricity</span></span></td>
<td><span data-ttu-id="451c1-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-905">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="451c1-906">-286.25</span></span></td>
<td><span data-ttu-id="451c1-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-908">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-909">Product 1</span></span></td>
<td><span data-ttu-id="451c1-910">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-910">10001</span></span></td>
<td><span data-ttu-id="451c1-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-911">Electricity</span></span></td>
<td><span data-ttu-id="451c1-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-912">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-913">241.05</span><span class="sxs-lookup"><span data-stu-id="451c1-913">241.05</span></span></td>
<td><span data-ttu-id="451c1-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-915">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-916">Product 2</span></span></td>
<td><span data-ttu-id="451c1-917">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-917">10001</span></span></td>
<td><span data-ttu-id="451c1-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-918">Electricity</span></span></td>
<td><span data-ttu-id="451c1-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-919">Fixed cost</span></span></td>
<td><span data-ttu-id="451c1-920">45.20</span><span class="sxs-lookup"><span data-stu-id="451c1-920">45.20</span></span></td>
<td><span data-ttu-id="451c1-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-922">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-922">CC003</span></span></td>
<td><span data-ttu-id="451c1-923">Montage</span><span class="sxs-lookup"><span data-stu-id="451c1-923">Assembly</span></span></td>
<td><span data-ttu-id="451c1-924">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-924">10001</span></span></td>
<td><span data-ttu-id="451c1-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-925">Electricity</span></span></td>
<td><span data-ttu-id="451c1-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-926">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="451c1-927">-2,977.17</span></span></td>
<td><span data-ttu-id="451c1-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-929">Prod 1</span></span></td>
<td><span data-ttu-id="451c1-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="451c1-930">Product 1</span></span></td>
<td><span data-ttu-id="451c1-931">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-931">10001</span></span></td>
<td><span data-ttu-id="451c1-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-932">Electricity</span></span></td>
<td><span data-ttu-id="451c1-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-933">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="451c1-934">2,507.09</span></span></td>
<td><span data-ttu-id="451c1-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="451c1-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-936">Prod 2</span></span></td>
<td><span data-ttu-id="451c1-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="451c1-937">Product 2</span></span></td>
<td><span data-ttu-id="451c1-938">10001</span><span class="sxs-lookup"><span data-stu-id="451c1-938">10001</span></span></td>
<td><span data-ttu-id="451c1-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-939">Electricity</span></span></td>
<td><span data-ttu-id="451c1-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-940">Variable cost</span></span></td>
<td><span data-ttu-id="451c1-941">470.08</span><span class="sxs-lookup"><span data-stu-id="451c1-941">470.08</span></span></td>
<td><span data-ttu-id="451c1-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="451c1-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="451c1-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="451c1-943">Conclusion</span></span>
<span data-ttu-id="451c1-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="451c1-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="451c1-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="451c1-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="451c1-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="451c1-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="451c1-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="451c1-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="451c1-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="451c1-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="451c1-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="451c1-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="451c1-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="451c1-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="451c1-951">CC099</span><span class="sxs-lookup"><span data-stu-id="451c1-951">CC099</span></span></th>
<th><span data-ttu-id="451c1-952">CC001</span><span class="sxs-lookup"><span data-stu-id="451c1-952">CC001</span></span></th>
<th><span data-ttu-id="451c1-953">CC002</span><span class="sxs-lookup"><span data-stu-id="451c1-953">CC002</span></span></th>
<th><span data-ttu-id="451c1-954">CC003</span><span class="sxs-lookup"><span data-stu-id="451c1-954">CC003</span></span></th>
<th><span data-ttu-id="451c1-955">CC004</span><span class="sxs-lookup"><span data-stu-id="451c1-955">CC004</span></span></th>
<th><span data-ttu-id="451c1-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="451c1-956">Proj 1</span></span></th>
<th><span data-ttu-id="451c1-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="451c1-957">Proj 2</span></span></th>
<th><span data-ttu-id="451c1-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="451c1-958">Prod 1</span></span></th>
<th><span data-ttu-id="451c1-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="451c1-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="451c1-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="451c1-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="451c1-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="451c1-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="451c1-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-971">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="451c1-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="451c1-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-973">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-974">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-975">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-976">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-977">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="451c1-978">776.36</span><span class="sxs-lookup"><span data-stu-id="451c1-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-979">223.64</span><span class="sxs-lookup"><span data-stu-id="451c1-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="451c1-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="451c1-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-982">000</span><span class="sxs-lookup"><span data-stu-id="451c1-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-983">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-984">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-985">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-986">0,00</span><span class="sxs-lookup"><span data-stu-id="451c1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-987">30,00</span><span class="sxs-lookup"><span data-stu-id="451c1-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-988">10,00</span><span class="sxs-lookup"><span data-stu-id="451c1-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="451c1-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="451c1-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="451c1-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="451c1-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="451c1-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="451c1-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="451c1-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="451c1-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="451c1-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="451c1-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="451c1-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="451c1-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="451c1-996">Weitere Informationen finden Sie unter [Kostenrollup-Richtlinie und Zuschlagsberechnung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="451c1-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



