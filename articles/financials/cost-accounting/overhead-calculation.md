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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "335116"
---
# <a name="overhead-calculation"></a><span data-ttu-id="ccada-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="ccada-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccada-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ccada-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="ccada-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="ccada-105">Term definition</span></span>
---------------

<span data-ttu-id="ccada-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="ccada-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="ccada-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="ccada-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="ccada-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="ccada-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="ccada-109">Miete</span><span class="sxs-lookup"><span data-stu-id="ccada-109">Rent</span></span>
-   <span data-ttu-id="ccada-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-110">Electricity</span></span>
-   <span data-ttu-id="ccada-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="ccada-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="ccada-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="ccada-112">Overhead calculation overview</span></span>
<span data-ttu-id="ccada-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccada-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="ccada-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="ccada-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="ccada-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="ccada-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="ccada-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="ccada-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="ccada-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccada-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="ccada-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="ccada-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="ccada-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="ccada-119">Version type</span></span>
-   <span data-ttu-id="ccada-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="ccada-120">Date and time</span></span>
-   <span data-ttu-id="ccada-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="ccada-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="ccada-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="ccada-122">Fiscal year</span></span>
-   <span data-ttu-id="ccada-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="ccada-123">Fiscal period</span></span>

<span data-ttu-id="ccada-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccada-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="ccada-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="ccada-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="ccada-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ccada-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="ccada-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="ccada-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="ccada-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="ccada-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="ccada-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="ccada-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="ccada-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="ccada-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="ccada-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="ccada-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="ccada-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="ccada-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="ccada-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="ccada-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="ccada-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ccada-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="ccada-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ccada-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="ccada-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="ccada-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="ccada-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ccada-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="ccada-140">Main account</span></span></th>
<th><span data-ttu-id="ccada-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="ccada-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="ccada-143">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-143">CC099</span></span></td>
<td><span data-ttu-id="ccada-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-144">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-145">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-145">10001</span></span></td>
<td><span data-ttu-id="ccada-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-146">Electricity</span></span></td>
<td><span data-ttu-id="ccada-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ccada-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="ccada-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="ccada-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="ccada-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="ccada-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="ccada-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="ccada-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="ccada-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="ccada-151">Define the cost behavior rule</span></span>

<span data-ttu-id="ccada-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="ccada-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="ccada-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="ccada-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="ccada-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="ccada-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="ccada-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="ccada-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="ccada-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="ccada-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="ccada-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="ccada-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="ccada-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="ccada-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ccada-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ccada-160">Journal</span></span></th>
<th><span data-ttu-id="ccada-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="ccada-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ccada-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ccada-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ccada-163">Version</span><span class="sxs-lookup"><span data-stu-id="ccada-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-164">00001</span><span class="sxs-lookup"><span data-stu-id="ccada-164">00001</span></span></td>
<td><span data-ttu-id="ccada-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="ccada-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="ccada-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="ccada-166">Fiscal</span></span></td>
<td><span data-ttu-id="ccada-167">2017</span><span class="sxs-lookup"><span data-stu-id="ccada-167">2017</span></span></td>
<td><span data-ttu-id="ccada-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ccada-168">Period 1</span></span></td>
<td><span data-ttu-id="ccada-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ccada-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ccada-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="ccada-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-173">Cost element</span></span></th>
<th><span data-ttu-id="ccada-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-174">Cost behavior</span></span></th>
<th><span data-ttu-id="ccada-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="ccada-177">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-177">CC099</span></span></td>
<td><span data-ttu-id="ccada-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-178">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-179">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-179">10001</span></span></td>
<td><span data-ttu-id="ccada-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-180">Electricity</span></span></td>
<td><span data-ttu-id="ccada-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="ccada-181">Unclassified</span></span></td>
<td><span data-ttu-id="ccada-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ccada-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ccada-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ccada-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-185">Cost element</span></span></th>
<th><span data-ttu-id="ccada-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-186">Cost behavior</span></span></th>
<th><span data-ttu-id="ccada-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-187">Amount</span></span></th>
<th><span data-ttu-id="ccada-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-189">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-189">CC099</span></span></td>
<td><span data-ttu-id="ccada-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-190">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-191">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-191">10001</span></span></td>
<td><span data-ttu-id="ccada-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-192">Electricity</span></span></td>
<td><span data-ttu-id="ccada-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="ccada-193">Unclassified</span></span></td>
<td><span data-ttu-id="ccada-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ccada-194">10,000.00</span></span></td>
<td><span data-ttu-id="ccada-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-196">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-196">CC099</span></span></td>
<td><span data-ttu-id="ccada-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-197">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-198">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-198">10001</span></span></td>
<td><span data-ttu-id="ccada-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-199">Electricity</span></span></td>
<td><span data-ttu-id="ccada-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="ccada-200">Unclassified</span></span></td>
<td><span data-ttu-id="ccada-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-201">-10,000.00</span></span></td>
<td><span data-ttu-id="ccada-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-203">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-203">CC099</span></span></td>
<td><span data-ttu-id="ccada-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-204">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-205">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-205">10001</span></span></td>
<td><span data-ttu-id="ccada-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-206">Electricity</span></span></td>
<td><span data-ttu-id="ccada-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-207">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ccada-208">1,000.00</span></span></td>
<td><span data-ttu-id="ccada-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-210">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-210">CC099</span></span></td>
<td><span data-ttu-id="ccada-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-211">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-212">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-212">10001</span></span></td>
<td><span data-ttu-id="ccada-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-213">Electricity</span></span></td>
<td><span data-ttu-id="ccada-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-214">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ccada-215">9,000.00</span></span></td>
<td><span data-ttu-id="ccada-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ccada-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="ccada-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="ccada-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="ccada-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="ccada-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="ccada-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="ccada-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="ccada-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="ccada-221">Define the cost distribution rule</span></span>

<span data-ttu-id="ccada-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="ccada-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="ccada-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="ccada-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="ccada-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ccada-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="ccada-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="ccada-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="ccada-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="ccada-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="ccada-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ccada-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-228">Cost object</span></span></th>
<th><span data-ttu-id="ccada-229">KWH</span><span class="sxs-lookup"><span data-stu-id="ccada-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-230">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-230">CC001</span></span></td>
<td><span data-ttu-id="ccada-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-231">HR</span></span></td>
<td><span data-ttu-id="ccada-232">1.000</span><span class="sxs-lookup"><span data-stu-id="ccada-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-233">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-233">CC002</span></span></td>
<td><span data-ttu-id="ccada-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-234">Finance</span></span></td>
<td><span data-ttu-id="ccada-235">6.000</span><span class="sxs-lookup"><span data-stu-id="ccada-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-236">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-236">CC003</span></span></td>
<td><span data-ttu-id="ccada-237">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-237">Assembly</span></span></td>
<td><span data-ttu-id="ccada-238">0</span><span class="sxs-lookup"><span data-stu-id="ccada-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccada-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-240">Cost object</span></span></th>
<th><span data-ttu-id="ccada-241">Größe</span><span class="sxs-lookup"><span data-stu-id="ccada-241">Magnitude</span></span></th>
<th><span data-ttu-id="ccada-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ccada-242">Allocation factor</span></span></th>
<th><span data-ttu-id="ccada-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-244">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-244">CC001</span></span></td>
<td><span data-ttu-id="ccada-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-245">HR</span></span></td>
<td><span data-ttu-id="ccada-246">1.000</span><span class="sxs-lookup"><span data-stu-id="ccada-246">1,000</span></span></td>
<td><span data-ttu-id="ccada-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ccada-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ccada-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-249">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-249">CC002</span></span></td>
<td><span data-ttu-id="ccada-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-250">Finance</span></span></td>
<td><span data-ttu-id="ccada-251">6.000</span><span class="sxs-lookup"><span data-stu-id="ccada-251">6,000</span></span></td>
<td><span data-ttu-id="ccada-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ccada-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ccada-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-254">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-254">CC003</span></span></td>
<td><span data-ttu-id="ccada-255">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-255">Assembly</span></span></td>
<td><span data-ttu-id="ccada-256">0</span><span class="sxs-lookup"><span data-stu-id="ccada-256">0</span></span></td>
<td><span data-ttu-id="ccada-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ccada-258">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="ccada-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="ccada-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccada-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-261">Cost object</span></span></th>
<th><span data-ttu-id="ccada-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="ccada-262">Formula</span></span></th>
<th><span data-ttu-id="ccada-263">Größe</span><span class="sxs-lookup"><span data-stu-id="ccada-263">Magnitude</span></span></th>
<th><span data-ttu-id="ccada-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ccada-264">Allocation factor</span></span></th>
<th><span data-ttu-id="ccada-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-266">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-266">CC001</span></span></td>
<td><span data-ttu-id="ccada-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-267">HR</span></span></td>
<td><span data-ttu-id="ccada-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="ccada-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ccada-269">1</span><span class="sxs-lookup"><span data-stu-id="ccada-269">1</span></span></td>
<td><span data-ttu-id="ccada-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ccada-271">500,00</span><span class="sxs-lookup"><span data-stu-id="ccada-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-272">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-272">CC002</span></span></td>
<td><span data-ttu-id="ccada-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-273">Finance</span></span></td>
<td><span data-ttu-id="ccada-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="ccada-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ccada-275">1</span><span class="sxs-lookup"><span data-stu-id="ccada-275">1</span></span></td>
<td><span data-ttu-id="ccada-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ccada-277">500,00</span><span class="sxs-lookup"><span data-stu-id="ccada-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-278">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-278">CC003</span></span></td>
<td><span data-ttu-id="ccada-279">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-279">Assembly</span></span></td>
<td><span data-ttu-id="ccada-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="ccada-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ccada-281">0</span><span class="sxs-lookup"><span data-stu-id="ccada-281">0</span></span></td>
<td><span data-ttu-id="ccada-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ccada-283">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ccada-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ccada-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ccada-285">Journal</span></span></th>
<th><span data-ttu-id="ccada-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="ccada-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ccada-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ccada-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ccada-288">Version</span><span class="sxs-lookup"><span data-stu-id="ccada-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-289">00002</span><span class="sxs-lookup"><span data-stu-id="ccada-289">00002</span></span></td>
<td><span data-ttu-id="ccada-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="ccada-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="ccada-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="ccada-291">Fiscal</span></span></td>
<td><span data-ttu-id="ccada-292">2017</span><span class="sxs-lookup"><span data-stu-id="ccada-292">2017</span></span></td>
<td><span data-ttu-id="ccada-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ccada-293">Period 1</span></span></td>
<td><span data-ttu-id="ccada-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ccada-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ccada-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="ccada-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-298">Cost element</span></span></th>
<th><span data-ttu-id="ccada-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-299">Cost behavior</span></span></th>
<th><span data-ttu-id="ccada-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-302">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-302">CC099</span></span></td>
<td><span data-ttu-id="ccada-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-303">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-304">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-304">10001</span></span></td>
<td><span data-ttu-id="ccada-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-305">Electricity</span></span></td>
<td><span data-ttu-id="ccada-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-306">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ccada-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-309">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-309">CC099</span></span></td>
<td><span data-ttu-id="ccada-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-310">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-311">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-311">10001</span></span></td>
<td><span data-ttu-id="ccada-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-312">Electricity</span></span></td>
<td><span data-ttu-id="ccada-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-313">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ccada-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ccada-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ccada-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-317">Cost element</span></span></th>
<th><span data-ttu-id="ccada-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-318">Cost behavior</span></span></th>
<th><span data-ttu-id="ccada-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-319">Amount</span></span></th>
<th><span data-ttu-id="ccada-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-321">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-321">CC099</span></span></td>
<td><span data-ttu-id="ccada-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-322">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-323">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-323">10001</span></span></td>
<td><span data-ttu-id="ccada-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-324">Electricity</span></span></td>
<td><span data-ttu-id="ccada-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-325">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ccada-326">-1,000.00</span></span></td>
<td><span data-ttu-id="ccada-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-328">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-328">CC001</span></span></td>
<td><span data-ttu-id="ccada-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-329">HR</span></span></td>
<td><span data-ttu-id="ccada-330">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-330">10001</span></span></td>
<td><span data-ttu-id="ccada-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-331">Electricity</span></span></td>
<td><span data-ttu-id="ccada-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-332">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-333">500,00</span><span class="sxs-lookup"><span data-stu-id="ccada-333">500.00</span></span></td>
<td><span data-ttu-id="ccada-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-335">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-335">CC002</span></span></td>
<td><span data-ttu-id="ccada-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-336">Finance</span></span></td>
<td><span data-ttu-id="ccada-337">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-337">10001</span></span></td>
<td><span data-ttu-id="ccada-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-338">Electricity</span></span></td>
<td><span data-ttu-id="ccada-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-339">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-340">500,00</span><span class="sxs-lookup"><span data-stu-id="ccada-340">500.00</span></span></td>
<td><span data-ttu-id="ccada-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-342">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-342">CC099</span></span></td>
<td><span data-ttu-id="ccada-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ccada-343">Default cost center</span></span></td>
<td><span data-ttu-id="ccada-344">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-344">10001</span></span></td>
<td><span data-ttu-id="ccada-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-345">Electricity</span></span></td>
<td><span data-ttu-id="ccada-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-346">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="ccada-347">-9,000.00</span></span></td>
<td><span data-ttu-id="ccada-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-349">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-349">CC001</span></span></td>
<td><span data-ttu-id="ccada-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-350">HR</span></span></td>
<td><span data-ttu-id="ccada-351">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-351">10001</span></span></td>
<td><span data-ttu-id="ccada-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-352">Electricity</span></span></td>
<td><span data-ttu-id="ccada-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-353">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ccada-354">1,285.71</span></span></td>
<td><span data-ttu-id="ccada-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-356">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-356">CC002</span></span></td>
<td><span data-ttu-id="ccada-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-357">Finance</span></span></td>
<td><span data-ttu-id="ccada-358">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-358">10001</span></span></td>
<td><span data-ttu-id="ccada-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-359">Electricity</span></span></td>
<td><span data-ttu-id="ccada-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-360">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ccada-361">7,714.29</span></span></td>
<td><span data-ttu-id="ccada-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ccada-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="ccada-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="ccada-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="ccada-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="ccada-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="ccada-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="ccada-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="ccada-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="ccada-367">Define the overhead rate</span></span>

<span data-ttu-id="ccada-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="ccada-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="ccada-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ccada-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-370">Cost object</span></span></th>
<th><span data-ttu-id="ccada-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="ccada-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ccada-372">Proj 1</span></span></td>
<td><span data-ttu-id="ccada-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-373">Project 1</span></span></td>
<td><span data-ttu-id="ccada-374">3</span><span class="sxs-lookup"><span data-stu-id="ccada-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ccada-375">Proj 2</span></span></td>
<td><span data-ttu-id="ccada-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-376">Project 2</span></span></td>
<td><span data-ttu-id="ccada-377">1</span><span class="sxs-lookup"><span data-stu-id="ccada-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="ccada-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-379">Cost object</span></span></th>
<th><span data-ttu-id="ccada-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-380">Cost element</span></span></th>
<th><span data-ttu-id="ccada-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-381">Cost behavior</span></span></th>
<th><span data-ttu-id="ccada-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="ccada-382">Units</span></span></th>
<th><span data-ttu-id="ccada-383">Satz</span><span class="sxs-lookup"><span data-stu-id="ccada-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-384">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-384">CC001</span></span></td>
<td><span data-ttu-id="ccada-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-385">HR</span></span></td>
<td><span data-ttu-id="ccada-386">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-386">10001</span></span></td>
<td><span data-ttu-id="ccada-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-387">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-388">1</span><span class="sxs-lookup"><span data-stu-id="ccada-388">1</span></span></td>
<td><span data-ttu-id="ccada-389">10</span><span class="sxs-lookup"><span data-stu-id="ccada-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccada-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-391">Cost object</span></span></th>
<th><span data-ttu-id="ccada-392">Größe</span><span class="sxs-lookup"><span data-stu-id="ccada-392">Magnitude</span></span></th>
<th><span data-ttu-id="ccada-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-393">Cost element</span></span></th>
<th><span data-ttu-id="ccada-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ccada-394">Allocation factor</span></span></th>
<th><span data-ttu-id="ccada-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ccada-396">Proj 1</span></span></td>
<td><span data-ttu-id="ccada-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-397">Project 1</span></span></td>
<td><span data-ttu-id="ccada-398">3</span><span class="sxs-lookup"><span data-stu-id="ccada-398">3</span></span></td>
<td><span data-ttu-id="ccada-399">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-399">10001</span></span></td>
<td><span data-ttu-id="ccada-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="ccada-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ccada-401">30,00</span><span class="sxs-lookup"><span data-stu-id="ccada-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ccada-402">Proj 2</span></span></td>
<td><span data-ttu-id="ccada-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-403">Project 2</span></span></td>
<td><span data-ttu-id="ccada-404">1</span><span class="sxs-lookup"><span data-stu-id="ccada-404">1</span></span></td>
<td><span data-ttu-id="ccada-405">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-405">10001</span></span></td>
<td><span data-ttu-id="ccada-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="ccada-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ccada-407">10,00</span><span class="sxs-lookup"><span data-stu-id="ccada-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ccada-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ccada-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ccada-409">Journal</span></span></th>
<th><span data-ttu-id="ccada-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="ccada-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ccada-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ccada-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ccada-412">Version</span><span class="sxs-lookup"><span data-stu-id="ccada-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-413">00003</span><span class="sxs-lookup"><span data-stu-id="ccada-413">00003</span></span></td>
<td><span data-ttu-id="ccada-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="ccada-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="ccada-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="ccada-415">Fiscal</span></span></td>
<td><span data-ttu-id="ccada-416">2017</span><span class="sxs-lookup"><span data-stu-id="ccada-416">2017</span></span></td>
<td><span data-ttu-id="ccada-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ccada-417">Period 1</span></span></td>
<td><span data-ttu-id="ccada-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ccada-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="ccada-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="ccada-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-421">Cost object</span></span></th>
<th><span data-ttu-id="ccada-422">Größe</span><span class="sxs-lookup"><span data-stu-id="ccada-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ccada-424">Proj 1</span></span></td>
<td><span data-ttu-id="ccada-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ccada-426">3,00</span><span class="sxs-lookup"><span data-stu-id="ccada-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ccada-428">Proj 2</span></span></td>
<td><span data-ttu-id="ccada-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ccada-430">1,00</span><span class="sxs-lookup"><span data-stu-id="ccada-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ccada-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ccada-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-433">Cost element</span></span></th>
<th><span data-ttu-id="ccada-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-434">Cost behavior</span></span></th>
<th><span data-ttu-id="ccada-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-435">Amount</span></span></th>
<th><span data-ttu-id="ccada-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="ccada-437">CC0001</span></span></td>
<td><span data-ttu-id="ccada-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-438">HR</span></span></td>
<td><span data-ttu-id="ccada-439">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-439">10001</span></span></td>
<td><span data-ttu-id="ccada-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-440">Electricity</span></span></td>
<td><span data-ttu-id="ccada-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-441">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="ccada-442">-30.00</span></span></td>
<td><span data-ttu-id="ccada-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ccada-444">Proj 1</span></span></td>
<td><span data-ttu-id="ccada-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ccada-446">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-446">10001</span></span></td>
<td><span data-ttu-id="ccada-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-447">Electricity</span></span></td>
<td><span data-ttu-id="ccada-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-448">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-449">30,00</span><span class="sxs-lookup"><span data-stu-id="ccada-449">30.00</span></span></td>
<td><span data-ttu-id="ccada-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-451">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-451">CC001</span></span></td>
<td><span data-ttu-id="ccada-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-452">HR</span></span></td>
<td><span data-ttu-id="ccada-453">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-453">10001</span></span></td>
<td><span data-ttu-id="ccada-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-454">Electricity</span></span></td>
<td><span data-ttu-id="ccada-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-455">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="ccada-456">-10.00</span></span></td>
<td><span data-ttu-id="ccada-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ccada-458">Proj 2</span></span></td>
<td><span data-ttu-id="ccada-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ccada-460">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-460">10001</span></span></td>
<td><span data-ttu-id="ccada-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-461">Electricity</span></span></td>
<td><span data-ttu-id="ccada-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-462">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-463">10.00</span><span class="sxs-lookup"><span data-stu-id="ccada-463">10.00</span></span></td>
<td><span data-ttu-id="ccada-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="ccada-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="ccada-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="ccada-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="ccada-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccada-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="ccada-468">Finance and Operations unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="ccada-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="ccada-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ccada-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="ccada-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ccada-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="ccada-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ccada-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="ccada-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ccada-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="ccada-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="ccada-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="ccada-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="ccada-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="ccada-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="ccada-475">Define the cost allocation</span></span>

<span data-ttu-id="ccada-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="ccada-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="ccada-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="ccada-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="ccada-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ccada-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-479">Cost object</span></span></th>
<th><span data-ttu-id="ccada-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="ccada-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-481">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-481">CC002</span></span></td>
<td><span data-ttu-id="ccada-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-482">Finance</span></span></td>
<td><span data-ttu-id="ccada-483">35</span><span class="sxs-lookup"><span data-stu-id="ccada-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-484">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-484">CC003</span></span></td>
<td><span data-ttu-id="ccada-485">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-485">Assembly</span></span></td>
<td><span data-ttu-id="ccada-486">55</span><span class="sxs-lookup"><span data-stu-id="ccada-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-487">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-487">CC004</span></span></td>
<td><span data-ttu-id="ccada-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-488">Packaging</span></span></td>
<td><span data-ttu-id="ccada-489">10</span><span class="sxs-lookup"><span data-stu-id="ccada-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="ccada-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="ccada-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ccada-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-492">Cost object</span></span></th>
<th><span data-ttu-id="ccada-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="ccada-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-494">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-494">CC003</span></span></td>
<td><span data-ttu-id="ccada-495">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-495">Assembly</span></span></td>
<td><span data-ttu-id="ccada-496">65</span><span class="sxs-lookup"><span data-stu-id="ccada-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-497">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-497">CC004</span></span></td>
<td><span data-ttu-id="ccada-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-498">Packaging</span></span></td>
<td><span data-ttu-id="ccada-499">35</span><span class="sxs-lookup"><span data-stu-id="ccada-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="ccada-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="ccada-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ccada-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-502">Cost object</span></span></th>
<th><span data-ttu-id="ccada-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="ccada-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-504">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-505">Product 1</span></span></td>
<td><span data-ttu-id="ccada-506">60</span><span class="sxs-lookup"><span data-stu-id="ccada-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-507">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-508">Product 2</span></span></td>
<td><span data-ttu-id="ccada-509">20</span><span class="sxs-lookup"><span data-stu-id="ccada-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="ccada-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="ccada-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ccada-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-512">Cost object</span></span></th>
<th><span data-ttu-id="ccada-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="ccada-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-514">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-515">Product 1</span></span></td>
<td><span data-ttu-id="ccada-516">80</span><span class="sxs-lookup"><span data-stu-id="ccada-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-517">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-518">Product 2</span></span></td>
<td><span data-ttu-id="ccada-519">September</span><span class="sxs-lookup"><span data-stu-id="ccada-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ccada-520">In Finance and Operations können statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ccada-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="ccada-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="ccada-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="ccada-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="ccada-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-523">Cost object</span></span></th>
<th><span data-ttu-id="ccada-524">Größe</span><span class="sxs-lookup"><span data-stu-id="ccada-524">Magnitude</span></span></th>
<th><span data-ttu-id="ccada-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ccada-525">Allocation factor</span></span></th>
<th><span data-ttu-id="ccada-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-526">Amount</span></span></th>
<th><span data-ttu-id="ccada-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-528">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-528">CC002</span></span></td>
<td><span data-ttu-id="ccada-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-529">Finance</span></span></td>
<td><span data-ttu-id="ccada-530">35</span><span class="sxs-lookup"><span data-stu-id="ccada-530">35</span></span></td>
<td><span data-ttu-id="ccada-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="ccada-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ccada-532">175.00</span><span class="sxs-lookup"><span data-stu-id="ccada-532">175.00</span></span></td>
<td><span data-ttu-id="ccada-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-534">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-534">CC003</span></span></td>
<td><span data-ttu-id="ccada-535">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-535">Assembly</span></span></td>
<td><span data-ttu-id="ccada-536">55</span><span class="sxs-lookup"><span data-stu-id="ccada-536">55</span></span></td>
<td><span data-ttu-id="ccada-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="ccada-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ccada-538">275.00</span><span class="sxs-lookup"><span data-stu-id="ccada-538">275.00</span></span></td>
<td><span data-ttu-id="ccada-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-540">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-540">CC004</span></span></td>
<td><span data-ttu-id="ccada-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-541">Packaging</span></span></td>
<td><span data-ttu-id="ccada-542">10</span><span class="sxs-lookup"><span data-stu-id="ccada-542">10</span></span></td>
<td><span data-ttu-id="ccada-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="ccada-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ccada-544">50,00</span><span class="sxs-lookup"><span data-stu-id="ccada-544">50.00</span></span></td>
<td><span data-ttu-id="ccada-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-546">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-546">CC002</span></span></td>
<td><span data-ttu-id="ccada-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-547">Finance</span></span></td>
<td><span data-ttu-id="ccada-548">35</span><span class="sxs-lookup"><span data-stu-id="ccada-548">35</span></span></td>
<td><span data-ttu-id="ccada-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="ccada-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ccada-550">436.00</span><span class="sxs-lookup"><span data-stu-id="ccada-550">436.00</span></span></td>
<td><span data-ttu-id="ccada-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-552">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-552">CC003</span></span></td>
<td><span data-ttu-id="ccada-553">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-553">Assembly</span></span></td>
<td><span data-ttu-id="ccada-554">55</span><span class="sxs-lookup"><span data-stu-id="ccada-554">55</span></span></td>
<td><span data-ttu-id="ccada-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="ccada-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ccada-556">685.14</span><span class="sxs-lookup"><span data-stu-id="ccada-556">685.14</span></span></td>
<td><span data-ttu-id="ccada-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-558">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-558">CC004</span></span></td>
<td><span data-ttu-id="ccada-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-559">Packaging</span></span></td>
<td><span data-ttu-id="ccada-560">10</span><span class="sxs-lookup"><span data-stu-id="ccada-560">10</span></span></td>
<td><span data-ttu-id="ccada-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="ccada-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ccada-562">124.57</span><span class="sxs-lookup"><span data-stu-id="ccada-562">124.57</span></span></td>
<td><span data-ttu-id="ccada-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="ccada-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-565">Cost object</span></span></th>
<th><span data-ttu-id="ccada-566">Größe</span><span class="sxs-lookup"><span data-stu-id="ccada-566">Magnitude</span></span></th>
<th><span data-ttu-id="ccada-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ccada-567">Allocation factor</span></span></th>
<th><span data-ttu-id="ccada-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-568">Amount</span></span></th>
<th><span data-ttu-id="ccada-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-570">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-570">CC003</span></span></td>
<td><span data-ttu-id="ccada-571">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-571">Assembly</span></span></td>
<td><span data-ttu-id="ccada-572">65</span><span class="sxs-lookup"><span data-stu-id="ccada-572">65</span></span></td>
<td><span data-ttu-id="ccada-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="ccada-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ccada-574">438.75</span><span class="sxs-lookup"><span data-stu-id="ccada-574">438.75</span></span></td>
<td><span data-ttu-id="ccada-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-576">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-576">CC004</span></span></td>
<td><span data-ttu-id="ccada-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-577">Packaging</span></span></td>
<td><span data-ttu-id="ccada-578">35</span><span class="sxs-lookup"><span data-stu-id="ccada-578">35</span></span></td>
<td><span data-ttu-id="ccada-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="ccada-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ccada-580">236.25</span><span class="sxs-lookup"><span data-stu-id="ccada-580">236.25</span></span></td>
<td><span data-ttu-id="ccada-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-582">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-582">CC003</span></span></td>
<td><span data-ttu-id="ccada-583">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-583">Assembly</span></span></td>
<td><span data-ttu-id="ccada-584">65</span><span class="sxs-lookup"><span data-stu-id="ccada-584">65</span></span></td>
<td><span data-ttu-id="ccada-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="ccada-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ccada-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ccada-586">5,297.69</span></span></td>
<td><span data-ttu-id="ccada-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-588">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-588">CC004</span></span></td>
<td><span data-ttu-id="ccada-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-589">Packaging</span></span></td>
<td><span data-ttu-id="ccada-590">35</span><span class="sxs-lookup"><span data-stu-id="ccada-590">35</span></span></td>
<td><span data-ttu-id="ccada-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="ccada-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ccada-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ccada-592">2,852.60</span></span></td>
<td><span data-ttu-id="ccada-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="ccada-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-595">Cost object</span></span></th>
<th><span data-ttu-id="ccada-596">Größe</span><span class="sxs-lookup"><span data-stu-id="ccada-596">Magnitude</span></span></th>
<th><span data-ttu-id="ccada-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ccada-597">Allocation factor</span></span></th>
<th><span data-ttu-id="ccada-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-598">Amount</span></span></th>
<th><span data-ttu-id="ccada-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-600">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-601">Product 1</span></span></td>
<td><span data-ttu-id="ccada-602">60</span><span class="sxs-lookup"><span data-stu-id="ccada-602">60</span></span></td>
<td><span data-ttu-id="ccada-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="ccada-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ccada-604">535.31</span><span class="sxs-lookup"><span data-stu-id="ccada-604">535.31</span></span></td>
<td><span data-ttu-id="ccada-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-606">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-607">Product 2</span></span></td>
<td><span data-ttu-id="ccada-608">20</span><span class="sxs-lookup"><span data-stu-id="ccada-608">20</span></span></td>
<td><span data-ttu-id="ccada-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="ccada-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ccada-610">178.44</span><span class="sxs-lookup"><span data-stu-id="ccada-610">178.44</span></span></td>
<td><span data-ttu-id="ccada-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-612">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-613">Product 1</span></span></td>
<td><span data-ttu-id="ccada-614">60</span><span class="sxs-lookup"><span data-stu-id="ccada-614">60</span></span></td>
<td><span data-ttu-id="ccada-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="ccada-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ccada-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ccada-616">4,487.12</span></span></td>
<td><span data-ttu-id="ccada-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-618">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-619">Product 2</span></span></td>
<td><span data-ttu-id="ccada-620">20</span><span class="sxs-lookup"><span data-stu-id="ccada-620">20</span></span></td>
<td><span data-ttu-id="ccada-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="ccada-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ccada-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ccada-622">1,495.71</span></span></td>
<td><span data-ttu-id="ccada-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccada-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="ccada-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-625">Cost object</span></span></th>
<th><span data-ttu-id="ccada-626">Größe</span><span class="sxs-lookup"><span data-stu-id="ccada-626">Magnitude</span></span></th>
<th><span data-ttu-id="ccada-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ccada-627">Allocation factor</span></span></th>
<th><span data-ttu-id="ccada-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-628">Amount</span></span></th>
<th><span data-ttu-id="ccada-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-630">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-631">Product 1</span></span></td>
<td><span data-ttu-id="ccada-632">80</span><span class="sxs-lookup"><span data-stu-id="ccada-632">80</span></span></td>
<td><span data-ttu-id="ccada-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="ccada-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ccada-634">241.05</span><span class="sxs-lookup"><span data-stu-id="ccada-634">241.05</span></span></td>
<td><span data-ttu-id="ccada-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-636">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-637">Product 2</span></span></td>
<td><span data-ttu-id="ccada-638">15</span><span class="sxs-lookup"><span data-stu-id="ccada-638">15</span></span></td>
<td><span data-ttu-id="ccada-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="ccada-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ccada-640">45.20</span><span class="sxs-lookup"><span data-stu-id="ccada-640">45.20</span></span></td>
<td><span data-ttu-id="ccada-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-642">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-643">Product 1</span></span></td>
<td><span data-ttu-id="ccada-644">80</span><span class="sxs-lookup"><span data-stu-id="ccada-644">80</span></span></td>
<td><span data-ttu-id="ccada-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="ccada-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ccada-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ccada-646">2,507.09</span></span></td>
<td><span data-ttu-id="ccada-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-648">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-649">Product 2</span></span></td>
<td><span data-ttu-id="ccada-650">15</span><span class="sxs-lookup"><span data-stu-id="ccada-650">15</span></span></td>
<td><span data-ttu-id="ccada-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="ccada-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ccada-652">470.08</span><span class="sxs-lookup"><span data-stu-id="ccada-652">470.08</span></span></td>
<td><span data-ttu-id="ccada-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ccada-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="ccada-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ccada-655">Journal</span></span></th>
<th><span data-ttu-id="ccada-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="ccada-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ccada-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ccada-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ccada-658">Version</span><span class="sxs-lookup"><span data-stu-id="ccada-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-659">00004</span><span class="sxs-lookup"><span data-stu-id="ccada-659">00004</span></span></td>
<td><span data-ttu-id="ccada-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="ccada-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="ccada-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="ccada-661">Fiscal</span></span></td>
<td><span data-ttu-id="ccada-662">2017</span><span class="sxs-lookup"><span data-stu-id="ccada-662">2017</span></span></td>
<td><span data-ttu-id="ccada-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ccada-663">Period 1</span></span></td>
<td><span data-ttu-id="ccada-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ccada-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="ccada-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="ccada-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ccada-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-668">Cost element</span></span></th>
<th><span data-ttu-id="ccada-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-669">Cost behavior</span></span></th>
<th><span data-ttu-id="ccada-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-672">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-672">CC001</span></span></td>
<td><span data-ttu-id="ccada-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-673">HR</span></span></td>
<td><span data-ttu-id="ccada-674">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-674">10001</span></span></td>
<td><span data-ttu-id="ccada-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-675">Electricity</span></span></td>
<td><span data-ttu-id="ccada-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-676">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-677">500,00</span><span class="sxs-lookup"><span data-stu-id="ccada-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-679">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-679">CC001</span></span></td>
<td><span data-ttu-id="ccada-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-680">HR</span></span></td>
<td><span data-ttu-id="ccada-681">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-681">10001</span></span></td>
<td><span data-ttu-id="ccada-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-682">Electricity</span></span></td>
<td><span data-ttu-id="ccada-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-683">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="ccada-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-686">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-686">CC002</span></span></td>
<td><span data-ttu-id="ccada-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-687">Finance</span></span></td>
<td><span data-ttu-id="ccada-688">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-688">10001</span></span></td>
<td><span data-ttu-id="ccada-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-689">Electricity</span></span></td>
<td><span data-ttu-id="ccada-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-690">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-691">675.00</span><span class="sxs-lookup"><span data-stu-id="ccada-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-693">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-693">CC002</span></span></td>
<td><span data-ttu-id="ccada-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-694">Finance</span></span></td>
<td><span data-ttu-id="ccada-695">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-695">10001</span></span></td>
<td><span data-ttu-id="ccada-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-696">Electricity</span></span></td>
<td><span data-ttu-id="ccada-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-697">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="ccada-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-700">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-700">CC003</span></span></td>
<td><span data-ttu-id="ccada-701">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-701">Assembly</span></span></td>
<td><span data-ttu-id="ccada-702">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-702">10001</span></span></td>
<td><span data-ttu-id="ccada-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-703">Electricity</span></span></td>
<td><span data-ttu-id="ccada-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-704">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-705">713.75</span><span class="sxs-lookup"><span data-stu-id="ccada-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-707">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-707">CC003</span></span></td>
<td><span data-ttu-id="ccada-708">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-708">Assembly</span></span></td>
<td><span data-ttu-id="ccada-709">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-709">10001</span></span></td>
<td><span data-ttu-id="ccada-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-710">Electricity</span></span></td>
<td><span data-ttu-id="ccada-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-711">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="ccada-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-714">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-714">CC003</span></span></td>
<td><span data-ttu-id="ccada-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-715">Packaging</span></span></td>
<td><span data-ttu-id="ccada-716">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-716">10001</span></span></td>
<td><span data-ttu-id="ccada-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-717">Electricity</span></span></td>
<td><span data-ttu-id="ccada-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-718">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-719">286.25</span><span class="sxs-lookup"><span data-stu-id="ccada-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-721">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-721">CC003</span></span></td>
<td><span data-ttu-id="ccada-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-722">Packaging</span></span></td>
<td><span data-ttu-id="ccada-723">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-723">10001</span></span></td>
<td><span data-ttu-id="ccada-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-724">Electricity</span></span></td>
<td><span data-ttu-id="ccada-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-725">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="ccada-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-728">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-729">Product 1</span></span></td>
<td><span data-ttu-id="ccada-730">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-730">10001</span></span></td>
<td><span data-ttu-id="ccada-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-731">Electricity</span></span></td>
<td><span data-ttu-id="ccada-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-732">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-733">776.36</span><span class="sxs-lookup"><span data-stu-id="ccada-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-735">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-736">Product 1</span></span></td>
<td><span data-ttu-id="ccada-737">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-737">10001</span></span></td>
<td><span data-ttu-id="ccada-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-738">Electricity</span></span></td>
<td><span data-ttu-id="ccada-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-739">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ccada-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-742">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-743">Product 1</span></span></td>
<td><span data-ttu-id="ccada-744">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-744">10001</span></span></td>
<td><span data-ttu-id="ccada-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-745">Electricity</span></span></td>
<td><span data-ttu-id="ccada-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-746">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-747">223.64</span><span class="sxs-lookup"><span data-stu-id="ccada-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="ccada-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-749">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-750">Product 1</span></span></td>
<td><span data-ttu-id="ccada-751">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-751">10001</span></span></td>
<td><span data-ttu-id="ccada-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-752">Electricity</span></span></td>
<td><span data-ttu-id="ccada-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-753">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ccada-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ccada-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ccada-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ccada-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ccada-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-757">Cost element</span></span></th>
<th><span data-ttu-id="ccada-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ccada-758">Cost behavior</span></span></th>
<th><span data-ttu-id="ccada-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="ccada-759">Amount</span></span></th>
<th><span data-ttu-id="ccada-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ccada-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccada-761">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-761">CC001</span></span></td>
<td><span data-ttu-id="ccada-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-762">HR</span></span></td>
<td><span data-ttu-id="ccada-763">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-763">10001</span></span></td>
<td><span data-ttu-id="ccada-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-764">Electricity</span></span></td>
<td><span data-ttu-id="ccada-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-765">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="ccada-766">-500.00</span></span></td>
<td><span data-ttu-id="ccada-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-768">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-768">CC002</span></span></td>
<td><span data-ttu-id="ccada-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-769">Finance</span></span></td>
<td><span data-ttu-id="ccada-770">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-770">10001</span></span></td>
<td><span data-ttu-id="ccada-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-771">Electricity</span></span></td>
<td><span data-ttu-id="ccada-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-772">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-773">175.00</span><span class="sxs-lookup"><span data-stu-id="ccada-773">175.00</span></span></td>
<td><span data-ttu-id="ccada-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-775">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-775">CC003</span></span></td>
<td><span data-ttu-id="ccada-776">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-776">Assembly</span></span></td>
<td><span data-ttu-id="ccada-777">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-777">10001</span></span></td>
<td><span data-ttu-id="ccada-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-778">Electricity</span></span></td>
<td><span data-ttu-id="ccada-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-779">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-780">275.00</span><span class="sxs-lookup"><span data-stu-id="ccada-780">275.00</span></span></td>
<td><span data-ttu-id="ccada-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-782">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-782">CC004</span></span></td>
<td><span data-ttu-id="ccada-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-783">Packaging</span></span></td>
<td><span data-ttu-id="ccada-784">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-784">10001</span></span></td>
<td><span data-ttu-id="ccada-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-785">Electricity</span></span></td>
<td><span data-ttu-id="ccada-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-786">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-787">50,00</span><span class="sxs-lookup"><span data-stu-id="ccada-787">50,00</span></span></td>
<td><span data-ttu-id="ccada-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-789">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-789">CC001</span></span></td>
<td><span data-ttu-id="ccada-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ccada-790">HR</span></span></td>
<td><span data-ttu-id="ccada-791">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-791">10001</span></span></td>
<td><span data-ttu-id="ccada-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-792">Electricity</span></span></td>
<td><span data-ttu-id="ccada-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-793">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="ccada-794">-1,245.71</span></span></td>
<td><span data-ttu-id="ccada-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-796">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-796">CC002</span></span></td>
<td><span data-ttu-id="ccada-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-797">Finance</span></span></td>
<td><span data-ttu-id="ccada-798">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-798">10001</span></span></td>
<td><span data-ttu-id="ccada-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-799">Electricity</span></span></td>
<td><span data-ttu-id="ccada-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-800">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-801">436.00</span><span class="sxs-lookup"><span data-stu-id="ccada-801">436.00</span></span></td>
<td><span data-ttu-id="ccada-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-803">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-803">CC003</span></span></td>
<td><span data-ttu-id="ccada-804">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-804">Assembly</span></span></td>
<td><span data-ttu-id="ccada-805">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-805">10001</span></span></td>
<td><span data-ttu-id="ccada-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-806">Electricity</span></span></td>
<td><span data-ttu-id="ccada-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-807">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-808">685.14</span><span class="sxs-lookup"><span data-stu-id="ccada-808">685.14</span></span></td>
<td><span data-ttu-id="ccada-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-810">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-810">CC004</span></span></td>
<td><span data-ttu-id="ccada-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-811">Packaging</span></span></td>
<td><span data-ttu-id="ccada-812">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-812">10001</span></span></td>
<td><span data-ttu-id="ccada-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-813">Electricity</span></span></td>
<td><span data-ttu-id="ccada-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-814">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-815">124.57</span><span class="sxs-lookup"><span data-stu-id="ccada-815">124.57</span></span></td>
<td><span data-ttu-id="ccada-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-817">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-817">CC002</span></span></td>
<td><span data-ttu-id="ccada-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-818">Finance</span></span></td>
<td><span data-ttu-id="ccada-819">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-819">10001</span></span></td>
<td><span data-ttu-id="ccada-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-820">Electricity</span></span></td>
<td><span data-ttu-id="ccada-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-821">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="ccada-822">-675.00</span></span></td>
<td><span data-ttu-id="ccada-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-824">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-824">CC003</span></span></td>
<td><span data-ttu-id="ccada-825">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-825">Assembly</span></span></td>
<td><span data-ttu-id="ccada-826">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-826">10001</span></span></td>
<td><span data-ttu-id="ccada-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-827">Electricity</span></span></td>
<td><span data-ttu-id="ccada-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-828">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-829">438.75</span><span class="sxs-lookup"><span data-stu-id="ccada-829">438.75</span></span></td>
<td><span data-ttu-id="ccada-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-831">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-831">CC004</span></span></td>
<td><span data-ttu-id="ccada-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-832">Packaging</span></span></td>
<td><span data-ttu-id="ccada-833">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-833">10001</span></span></td>
<td><span data-ttu-id="ccada-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-834">Electricity</span></span></td>
<td><span data-ttu-id="ccada-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-835">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-836">236.25</span><span class="sxs-lookup"><span data-stu-id="ccada-836">236.25</span></span></td>
<td><span data-ttu-id="ccada-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-838">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-838">CC002</span></span></td>
<td><span data-ttu-id="ccada-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ccada-839">Finance</span></span></td>
<td><span data-ttu-id="ccada-840">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-840">10001</span></span></td>
<td><span data-ttu-id="ccada-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-841">Electricity</span></span></td>
<td><span data-ttu-id="ccada-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-842">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="ccada-843">-8,150.29</span></span></td>
<td><span data-ttu-id="ccada-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-845">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-845">CC003</span></span></td>
<td><span data-ttu-id="ccada-846">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-846">Assembly</span></span></td>
<td><span data-ttu-id="ccada-847">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-847">10001</span></span></td>
<td><span data-ttu-id="ccada-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-848">Electricity</span></span></td>
<td><span data-ttu-id="ccada-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-849">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ccada-850">5,297.69</span></span></td>
<td><span data-ttu-id="ccada-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-852">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-852">CC004</span></span></td>
<td><span data-ttu-id="ccada-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ccada-853">Packaging</span></span></td>
<td><span data-ttu-id="ccada-854">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-854">10001</span></span></td>
<td><span data-ttu-id="ccada-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-855">Electricity</span></span></td>
<td><span data-ttu-id="ccada-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-856">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ccada-857">2,852.60</span></span></td>
<td><span data-ttu-id="ccada-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-859">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-859">CC003</span></span></td>
<td><span data-ttu-id="ccada-860">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-860">Assembly</span></span></td>
<td><span data-ttu-id="ccada-861">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-861">10001</span></span></td>
<td><span data-ttu-id="ccada-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-862">Electricity</span></span></td>
<td><span data-ttu-id="ccada-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-863">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="ccada-864">-713.75</span></span></td>
<td><span data-ttu-id="ccada-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-866">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-867">Product 1</span></span></td>
<td><span data-ttu-id="ccada-868">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-868">10001</span></span></td>
<td><span data-ttu-id="ccada-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-869">Electricity</span></span></td>
<td><span data-ttu-id="ccada-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-870">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-871">535.31</span><span class="sxs-lookup"><span data-stu-id="ccada-871">535.31</span></span></td>
<td><span data-ttu-id="ccada-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-873">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-874">Product 2</span></span></td>
<td><span data-ttu-id="ccada-875">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-875">10001</span></span></td>
<td><span data-ttu-id="ccada-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-876">Electricity</span></span></td>
<td><span data-ttu-id="ccada-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-877">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-878">178.44</span><span class="sxs-lookup"><span data-stu-id="ccada-878">178.44</span></span></td>
<td><span data-ttu-id="ccada-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-880">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-880">CC003</span></span></td>
<td><span data-ttu-id="ccada-881">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-881">Assembly</span></span></td>
<td><span data-ttu-id="ccada-882">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-882">10001</span></span></td>
<td><span data-ttu-id="ccada-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-883">Electricity</span></span></td>
<td><span data-ttu-id="ccada-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-884">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="ccada-885">-5,982.83</span></span></td>
<td><span data-ttu-id="ccada-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-887">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-888">Product 1</span></span></td>
<td><span data-ttu-id="ccada-889">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-889">10001</span></span></td>
<td><span data-ttu-id="ccada-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-890">Electricity</span></span></td>
<td><span data-ttu-id="ccada-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-891">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ccada-892">4,487.12</span></span></td>
<td><span data-ttu-id="ccada-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-894">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-895">Product 2</span></span></td>
<td><span data-ttu-id="ccada-896">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-896">10001</span></span></td>
<td><span data-ttu-id="ccada-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-897">Electricity</span></span></td>
<td><span data-ttu-id="ccada-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-898">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ccada-899">1,495.71</span></span></td>
<td><span data-ttu-id="ccada-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-901">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-901">CC003</span></span></td>
<td><span data-ttu-id="ccada-902">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-902">Assembly</span></span></td>
<td><span data-ttu-id="ccada-903">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-903">10001</span></span></td>
<td><span data-ttu-id="ccada-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-904">Electricity</span></span></td>
<td><span data-ttu-id="ccada-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-905">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="ccada-906">-286.25</span></span></td>
<td><span data-ttu-id="ccada-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-908">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-909">Product 1</span></span></td>
<td><span data-ttu-id="ccada-910">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-910">10001</span></span></td>
<td><span data-ttu-id="ccada-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-911">Electricity</span></span></td>
<td><span data-ttu-id="ccada-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-912">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-913">241.05</span><span class="sxs-lookup"><span data-stu-id="ccada-913">241.05</span></span></td>
<td><span data-ttu-id="ccada-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-915">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-916">Product 2</span></span></td>
<td><span data-ttu-id="ccada-917">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-917">10001</span></span></td>
<td><span data-ttu-id="ccada-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-918">Electricity</span></span></td>
<td><span data-ttu-id="ccada-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-919">Fixed cost</span></span></td>
<td><span data-ttu-id="ccada-920">45.20</span><span class="sxs-lookup"><span data-stu-id="ccada-920">45.20</span></span></td>
<td><span data-ttu-id="ccada-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-922">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-922">CC003</span></span></td>
<td><span data-ttu-id="ccada-923">Montage</span><span class="sxs-lookup"><span data-stu-id="ccada-923">Assembly</span></span></td>
<td><span data-ttu-id="ccada-924">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-924">10001</span></span></td>
<td><span data-ttu-id="ccada-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-925">Electricity</span></span></td>
<td><span data-ttu-id="ccada-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-926">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="ccada-927">-2,977.17</span></span></td>
<td><span data-ttu-id="ccada-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-929">Prod 1</span></span></td>
<td><span data-ttu-id="ccada-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ccada-930">Product 1</span></span></td>
<td><span data-ttu-id="ccada-931">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-931">10001</span></span></td>
<td><span data-ttu-id="ccada-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-932">Electricity</span></span></td>
<td><span data-ttu-id="ccada-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-933">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ccada-934">2,507.09</span></span></td>
<td><span data-ttu-id="ccada-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccada-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-936">Prod 2</span></span></td>
<td><span data-ttu-id="ccada-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ccada-937">Product 2</span></span></td>
<td><span data-ttu-id="ccada-938">10001</span><span class="sxs-lookup"><span data-stu-id="ccada-938">10001</span></span></td>
<td><span data-ttu-id="ccada-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-939">Electricity</span></span></td>
<td><span data-ttu-id="ccada-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-940">Variable cost</span></span></td>
<td><span data-ttu-id="ccada-941">470.08</span><span class="sxs-lookup"><span data-stu-id="ccada-941">470.08</span></span></td>
<td><span data-ttu-id="ccada-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ccada-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="ccada-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="ccada-943">Conclusion</span></span>
<span data-ttu-id="ccada-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ccada-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="ccada-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ccada-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="ccada-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccada-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="ccada-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ccada-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="ccada-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ccada-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="ccada-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ccada-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="ccada-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="ccada-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ccada-951">CC099</span><span class="sxs-lookup"><span data-stu-id="ccada-951">CC099</span></span></th>
<th><span data-ttu-id="ccada-952">CC001</span><span class="sxs-lookup"><span data-stu-id="ccada-952">CC001</span></span></th>
<th><span data-ttu-id="ccada-953">CC002</span><span class="sxs-lookup"><span data-stu-id="ccada-953">CC002</span></span></th>
<th><span data-ttu-id="ccada-954">CC003</span><span class="sxs-lookup"><span data-stu-id="ccada-954">CC003</span></span></th>
<th><span data-ttu-id="ccada-955">CC004</span><span class="sxs-lookup"><span data-stu-id="ccada-955">CC004</span></span></th>
<th><span data-ttu-id="ccada-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ccada-956">Proj 1</span></span></th>
<th><span data-ttu-id="ccada-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ccada-957">Proj 2</span></span></th>
<th><span data-ttu-id="ccada-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ccada-958">Prod 1</span></span></th>
<th><span data-ttu-id="ccada-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ccada-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="ccada-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ccada-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ccada-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="ccada-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="ccada-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-971">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="ccada-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ccada-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-973">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-974">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-975">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-976">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-977">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ccada-978">776.36</span><span class="sxs-lookup"><span data-stu-id="ccada-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-979">223.64</span><span class="sxs-lookup"><span data-stu-id="ccada-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="ccada-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ccada-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-982">000</span><span class="sxs-lookup"><span data-stu-id="ccada-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-983">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-984">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-985">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-986">0,00</span><span class="sxs-lookup"><span data-stu-id="ccada-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-987">30,00</span><span class="sxs-lookup"><span data-stu-id="ccada-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-988">10,00</span><span class="sxs-lookup"><span data-stu-id="ccada-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ccada-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ccada-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ccada-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ccada-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ccada-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="ccada-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="ccada-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ccada-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="ccada-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="ccada-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="ccada-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="ccada-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="ccada-996">Weitere Informationen hierzu finden Sie unter [Kostenzusammenfassung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="ccada-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



