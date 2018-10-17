---
title: Gemeinkostenberechnung
description: "In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: de-de
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="c9b78-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="c9b78-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9b78-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c9b78-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c9b78-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="c9b78-105">Term definition</span></span>
---------------

<span data-ttu-id="c9b78-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="c9b78-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c9b78-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="c9b78-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c9b78-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="c9b78-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c9b78-109">Miete</span><span class="sxs-lookup"><span data-stu-id="c9b78-109">Rent</span></span>
-   <span data-ttu-id="c9b78-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-110">Electricity</span></span>
-   <span data-ttu-id="c9b78-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="c9b78-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c9b78-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="c9b78-112">Overhead calculation overview</span></span>
<span data-ttu-id="c9b78-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9b78-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c9b78-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c9b78-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="c9b78-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c9b78-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="c9b78-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c9b78-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9b78-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c9b78-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="c9b78-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c9b78-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="c9b78-119">Version type</span></span>
-   <span data-ttu-id="c9b78-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="c9b78-120">Date and time</span></span>
-   <span data-ttu-id="c9b78-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="c9b78-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c9b78-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="c9b78-122">Fiscal year</span></span>
-   <span data-ttu-id="c9b78-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="c9b78-123">Fiscal period</span></span>

<span data-ttu-id="c9b78-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9b78-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c9b78-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c9b78-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c9b78-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c9b78-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="c9b78-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c9b78-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="c9b78-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c9b78-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="c9b78-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c9b78-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="c9b78-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c9b78-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c9b78-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c9b78-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="c9b78-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c9b78-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="c9b78-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c9b78-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c9b78-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c9b78-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c9b78-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="c9b78-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c9b78-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="c9b78-140">Main account</span></span></th>
<th><span data-ttu-id="c9b78-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="c9b78-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c9b78-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-143">CC099</span></span></td>
<td><span data-ttu-id="c9b78-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-144">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-145">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-145">10001</span></span></td>
<td><span data-ttu-id="c9b78-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-146">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c9b78-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="c9b78-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c9b78-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="c9b78-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c9b78-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="c9b78-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c9b78-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="c9b78-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c9b78-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="c9b78-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c9b78-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="c9b78-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c9b78-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="c9b78-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c9b78-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="c9b78-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c9b78-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c9b78-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="c9b78-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c9b78-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="c9b78-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c9b78-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c9b78-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c9b78-160">Journal</span></span></th>
<th><span data-ttu-id="c9b78-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c9b78-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c9b78-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c9b78-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c9b78-163">Version</span><span class="sxs-lookup"><span data-stu-id="c9b78-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-164">00001</span><span class="sxs-lookup"><span data-stu-id="c9b78-164">00001</span></span></td>
<td><span data-ttu-id="c9b78-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="c9b78-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c9b78-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c9b78-166">Fiscal</span></span></td>
<td><span data-ttu-id="c9b78-167">2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-167">2017</span></span></td>
<td><span data-ttu-id="c9b78-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-168">Period 1</span></span></td>
<td><span data-ttu-id="c9b78-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c9b78-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c9b78-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-173">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c9b78-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c9b78-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-177">CC099</span></span></td>
<td><span data-ttu-id="c9b78-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-178">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-179">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-179">10001</span></span></td>
<td><span data-ttu-id="c9b78-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-180">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c9b78-181">Unclassified</span></span></td>
<td><span data-ttu-id="c9b78-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c9b78-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c9b78-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-185">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c9b78-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-187">Amount</span></span></th>
<th><span data-ttu-id="c9b78-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-189">CC099</span></span></td>
<td><span data-ttu-id="c9b78-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-190">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-191">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-191">10001</span></span></td>
<td><span data-ttu-id="c9b78-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-192">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c9b78-193">Unclassified</span></span></td>
<td><span data-ttu-id="c9b78-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-194">10,000.00</span></span></td>
<td><span data-ttu-id="c9b78-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-196">CC099</span></span></td>
<td><span data-ttu-id="c9b78-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-197">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-198">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-198">10001</span></span></td>
<td><span data-ttu-id="c9b78-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-199">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c9b78-200">Unclassified</span></span></td>
<td><span data-ttu-id="c9b78-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c9b78-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-203">CC099</span></span></td>
<td><span data-ttu-id="c9b78-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-204">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-205">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-205">10001</span></span></td>
<td><span data-ttu-id="c9b78-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-206">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-208">1,000.00</span></span></td>
<td><span data-ttu-id="c9b78-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-210">CC099</span></span></td>
<td><span data-ttu-id="c9b78-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-211">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-212">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-212">10001</span></span></td>
<td><span data-ttu-id="c9b78-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-213">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-214">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-215">9,000.00</span></span></td>
<td><span data-ttu-id="c9b78-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c9b78-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c9b78-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="c9b78-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c9b78-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c9b78-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="c9b78-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c9b78-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="c9b78-221">Define the cost distribution rule</span></span>

<span data-ttu-id="c9b78-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="c9b78-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c9b78-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="c9b78-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c9b78-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c9b78-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="c9b78-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c9b78-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="c9b78-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c9b78-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9b78-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-228">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-229">KWH</span><span class="sxs-lookup"><span data-stu-id="c9b78-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-230">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-230">CC001</span></span></td>
<td><span data-ttu-id="c9b78-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-231">HR</span></span></td>
<td><span data-ttu-id="c9b78-232">1.000</span><span class="sxs-lookup"><span data-stu-id="c9b78-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-233">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-233">CC002</span></span></td>
<td><span data-ttu-id="c9b78-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-234">Finance</span></span></td>
<td><span data-ttu-id="c9b78-235">6.000</span><span class="sxs-lookup"><span data-stu-id="c9b78-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-236">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-236">CC003</span></span></td>
<td><span data-ttu-id="c9b78-237">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-237">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-238">0</span><span class="sxs-lookup"><span data-stu-id="c9b78-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9b78-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-240">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-241">Größe</span><span class="sxs-lookup"><span data-stu-id="c9b78-241">Magnitude</span></span></th>
<th><span data-ttu-id="c9b78-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c9b78-242">Allocation factor</span></span></th>
<th><span data-ttu-id="c9b78-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-244">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-244">CC001</span></span></td>
<td><span data-ttu-id="c9b78-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-245">HR</span></span></td>
<td><span data-ttu-id="c9b78-246">1.000</span><span class="sxs-lookup"><span data-stu-id="c9b78-246">1,000</span></span></td>
<td><span data-ttu-id="c9b78-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c9b78-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-249">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-249">CC002</span></span></td>
<td><span data-ttu-id="c9b78-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-250">Finance</span></span></td>
<td><span data-ttu-id="c9b78-251">6.000</span><span class="sxs-lookup"><span data-stu-id="c9b78-251">6,000</span></span></td>
<td><span data-ttu-id="c9b78-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c9b78-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c9b78-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-254">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-254">CC003</span></span></td>
<td><span data-ttu-id="c9b78-255">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-255">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-256">0</span><span class="sxs-lookup"><span data-stu-id="c9b78-256">0</span></span></td>
<td><span data-ttu-id="c9b78-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c9b78-258">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="c9b78-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c9b78-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9b78-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-261">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="c9b78-262">Formula</span></span></th>
<th><span data-ttu-id="c9b78-263">Größe</span><span class="sxs-lookup"><span data-stu-id="c9b78-263">Magnitude</span></span></th>
<th><span data-ttu-id="c9b78-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c9b78-264">Allocation factor</span></span></th>
<th><span data-ttu-id="c9b78-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-266">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-266">CC001</span></span></td>
<td><span data-ttu-id="c9b78-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-267">HR</span></span></td>
<td><span data-ttu-id="c9b78-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c9b78-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c9b78-269">1</span><span class="sxs-lookup"><span data-stu-id="c9b78-269">1</span></span></td>
<td><span data-ttu-id="c9b78-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c9b78-271">500,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-272">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-272">CC002</span></span></td>
<td><span data-ttu-id="c9b78-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-273">Finance</span></span></td>
<td><span data-ttu-id="c9b78-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c9b78-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c9b78-275">1</span><span class="sxs-lookup"><span data-stu-id="c9b78-275">1</span></span></td>
<td><span data-ttu-id="c9b78-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c9b78-277">500,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-278">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-278">CC003</span></span></td>
<td><span data-ttu-id="c9b78-279">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-279">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c9b78-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c9b78-281">0</span><span class="sxs-lookup"><span data-stu-id="c9b78-281">0</span></span></td>
<td><span data-ttu-id="c9b78-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c9b78-283">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c9b78-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c9b78-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c9b78-285">Journal</span></span></th>
<th><span data-ttu-id="c9b78-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c9b78-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c9b78-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c9b78-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c9b78-288">Version</span><span class="sxs-lookup"><span data-stu-id="c9b78-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-289">00002</span><span class="sxs-lookup"><span data-stu-id="c9b78-289">00002</span></span></td>
<td><span data-ttu-id="c9b78-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="c9b78-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c9b78-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c9b78-291">Fiscal</span></span></td>
<td><span data-ttu-id="c9b78-292">2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-292">2017</span></span></td>
<td><span data-ttu-id="c9b78-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-293">Period 1</span></span></td>
<td><span data-ttu-id="c9b78-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c9b78-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c9b78-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-298">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-299">Cost behavior</span></span></th>
<th><span data-ttu-id="c9b78-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-302">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-302">CC099</span></span></td>
<td><span data-ttu-id="c9b78-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-303">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-304">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-304">10001</span></span></td>
<td><span data-ttu-id="c9b78-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-305">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-306">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-309">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-309">CC099</span></span></td>
<td><span data-ttu-id="c9b78-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-310">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-311">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-311">10001</span></span></td>
<td><span data-ttu-id="c9b78-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-312">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-313">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c9b78-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c9b78-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-317">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-318">Cost behavior</span></span></th>
<th><span data-ttu-id="c9b78-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-319">Amount</span></span></th>
<th><span data-ttu-id="c9b78-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-321">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-321">CC099</span></span></td>
<td><span data-ttu-id="c9b78-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-322">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-323">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-323">10001</span></span></td>
<td><span data-ttu-id="c9b78-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-324">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-325">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-326">-1,000.00</span></span></td>
<td><span data-ttu-id="c9b78-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-328">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-328">CC001</span></span></td>
<td><span data-ttu-id="c9b78-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-329">HR</span></span></td>
<td><span data-ttu-id="c9b78-330">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-330">10001</span></span></td>
<td><span data-ttu-id="c9b78-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-331">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-332">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-333">500,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-333">500.00</span></span></td>
<td><span data-ttu-id="c9b78-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-335">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-335">CC002</span></span></td>
<td><span data-ttu-id="c9b78-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-336">Finance</span></span></td>
<td><span data-ttu-id="c9b78-337">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-337">10001</span></span></td>
<td><span data-ttu-id="c9b78-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-338">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-339">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-340">500,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-340">500.00</span></span></td>
<td><span data-ttu-id="c9b78-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-342">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-342">CC099</span></span></td>
<td><span data-ttu-id="c9b78-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="c9b78-343">Default cost center</span></span></td>
<td><span data-ttu-id="c9b78-344">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-344">10001</span></span></td>
<td><span data-ttu-id="c9b78-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-345">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-346">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-347">-9,000.00</span></span></td>
<td><span data-ttu-id="c9b78-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-349">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-349">CC001</span></span></td>
<td><span data-ttu-id="c9b78-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-350">HR</span></span></td>
<td><span data-ttu-id="c9b78-351">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-351">10001</span></span></td>
<td><span data-ttu-id="c9b78-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-352">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-353">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-354">1,285.71</span></span></td>
<td><span data-ttu-id="c9b78-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-356">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-356">CC002</span></span></td>
<td><span data-ttu-id="c9b78-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-357">Finance</span></span></td>
<td><span data-ttu-id="c9b78-358">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-358">10001</span></span></td>
<td><span data-ttu-id="c9b78-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-359">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-360">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c9b78-361">7,714.29</span></span></td>
<td><span data-ttu-id="c9b78-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c9b78-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c9b78-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="c9b78-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c9b78-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="c9b78-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c9b78-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="c9b78-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c9b78-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="c9b78-367">Define the overhead rate</span></span>

<span data-ttu-id="c9b78-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="c9b78-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c9b78-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-370">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="c9b78-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-372">Proj 1</span></span></td>
<td><span data-ttu-id="c9b78-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-373">Project 1</span></span></td>
<td><span data-ttu-id="c9b78-374">3</span><span class="sxs-lookup"><span data-stu-id="c9b78-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-375">Proj 2</span></span></td>
<td><span data-ttu-id="c9b78-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-376">Project 2</span></span></td>
<td><span data-ttu-id="c9b78-377">1</span><span class="sxs-lookup"><span data-stu-id="c9b78-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="c9b78-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-379">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-380">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-381">Cost behavior</span></span></th>
<th><span data-ttu-id="c9b78-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="c9b78-382">Units</span></span></th>
<th><span data-ttu-id="c9b78-383">Satz</span><span class="sxs-lookup"><span data-stu-id="c9b78-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-384">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-384">CC001</span></span></td>
<td><span data-ttu-id="c9b78-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-385">HR</span></span></td>
<td><span data-ttu-id="c9b78-386">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-386">10001</span></span></td>
<td><span data-ttu-id="c9b78-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-387">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-388">1</span><span class="sxs-lookup"><span data-stu-id="c9b78-388">1</span></span></td>
<td><span data-ttu-id="c9b78-389">10</span><span class="sxs-lookup"><span data-stu-id="c9b78-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-391">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-392">Größe</span><span class="sxs-lookup"><span data-stu-id="c9b78-392">Magnitude</span></span></th>
<th><span data-ttu-id="c9b78-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-393">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c9b78-394">Allocation factor</span></span></th>
<th><span data-ttu-id="c9b78-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-396">Proj 1</span></span></td>
<td><span data-ttu-id="c9b78-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-397">Project 1</span></span></td>
<td><span data-ttu-id="c9b78-398">3</span><span class="sxs-lookup"><span data-stu-id="c9b78-398">3</span></span></td>
<td><span data-ttu-id="c9b78-399">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-399">10001</span></span></td>
<td><span data-ttu-id="c9b78-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c9b78-401">30,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-402">Proj 2</span></span></td>
<td><span data-ttu-id="c9b78-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-403">Project 2</span></span></td>
<td><span data-ttu-id="c9b78-404">1</span><span class="sxs-lookup"><span data-stu-id="c9b78-404">1</span></span></td>
<td><span data-ttu-id="c9b78-405">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-405">10001</span></span></td>
<td><span data-ttu-id="c9b78-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c9b78-407">10,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c9b78-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c9b78-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c9b78-409">Journal</span></span></th>
<th><span data-ttu-id="c9b78-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c9b78-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c9b78-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c9b78-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c9b78-412">Version</span><span class="sxs-lookup"><span data-stu-id="c9b78-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-413">00003</span><span class="sxs-lookup"><span data-stu-id="c9b78-413">00003</span></span></td>
<td><span data-ttu-id="c9b78-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="c9b78-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c9b78-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c9b78-415">Fiscal</span></span></td>
<td><span data-ttu-id="c9b78-416">2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-416">2017</span></span></td>
<td><span data-ttu-id="c9b78-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-417">Period 1</span></span></td>
<td><span data-ttu-id="c9b78-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c9b78-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="c9b78-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-421">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-422">Größe</span><span class="sxs-lookup"><span data-stu-id="c9b78-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-424">Proj 1</span></span></td>
<td><span data-ttu-id="c9b78-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c9b78-426">3,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-428">Proj 2</span></span></td>
<td><span data-ttu-id="c9b78-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c9b78-430">1,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c9b78-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c9b78-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-433">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-434">Cost behavior</span></span></th>
<th><span data-ttu-id="c9b78-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-435">Amount</span></span></th>
<th><span data-ttu-id="c9b78-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="c9b78-437">CC0001</span></span></td>
<td><span data-ttu-id="c9b78-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-438">HR</span></span></td>
<td><span data-ttu-id="c9b78-439">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-439">10001</span></span></td>
<td><span data-ttu-id="c9b78-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-440">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-441">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-442">-30.00</span></span></td>
<td><span data-ttu-id="c9b78-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-444">Proj 1</span></span></td>
<td><span data-ttu-id="c9b78-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c9b78-446">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-446">10001</span></span></td>
<td><span data-ttu-id="c9b78-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-447">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-448">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-449">30,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-449">30.00</span></span></td>
<td><span data-ttu-id="c9b78-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-451">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-451">CC001</span></span></td>
<td><span data-ttu-id="c9b78-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-452">HR</span></span></td>
<td><span data-ttu-id="c9b78-453">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-453">10001</span></span></td>
<td><span data-ttu-id="c9b78-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-454">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-455">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-456">-10.00</span></span></td>
<td><span data-ttu-id="c9b78-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-458">Proj 2</span></span></td>
<td><span data-ttu-id="c9b78-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c9b78-460">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-460">10001</span></span></td>
<td><span data-ttu-id="c9b78-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-461">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-462">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-463">10.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-463">10.00</span></span></td>
<td><span data-ttu-id="c9b78-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="c9b78-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c9b78-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="c9b78-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c9b78-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9b78-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c9b78-468">Finance and Operations unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="c9b78-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="c9b78-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c9b78-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c9b78-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c9b78-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9b78-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c9b78-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c9b78-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c9b78-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c9b78-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c9b78-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="c9b78-475">Define the cost allocation</span></span>

<span data-ttu-id="c9b78-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="c9b78-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c9b78-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c9b78-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c9b78-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-479">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="c9b78-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-481">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-481">CC002</span></span></td>
<td><span data-ttu-id="c9b78-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-482">Finance</span></span></td>
<td><span data-ttu-id="c9b78-483">35</span><span class="sxs-lookup"><span data-stu-id="c9b78-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-484">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-484">CC003</span></span></td>
<td><span data-ttu-id="c9b78-485">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-485">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-486">55</span><span class="sxs-lookup"><span data-stu-id="c9b78-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-487">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-487">CC004</span></span></td>
<td><span data-ttu-id="c9b78-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-488">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-489">10</span><span class="sxs-lookup"><span data-stu-id="c9b78-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c9b78-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c9b78-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-492">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="c9b78-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-494">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-494">CC003</span></span></td>
<td><span data-ttu-id="c9b78-495">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-495">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-496">65</span><span class="sxs-lookup"><span data-stu-id="c9b78-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-497">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-497">CC004</span></span></td>
<td><span data-ttu-id="c9b78-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-498">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-499">35</span><span class="sxs-lookup"><span data-stu-id="c9b78-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c9b78-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c9b78-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-502">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="c9b78-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-504">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-505">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-506">60</span><span class="sxs-lookup"><span data-stu-id="c9b78-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-507">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-508">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-509">20</span><span class="sxs-lookup"><span data-stu-id="c9b78-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="c9b78-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c9b78-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-512">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="c9b78-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-514">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-515">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-516">80</span><span class="sxs-lookup"><span data-stu-id="c9b78-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-517">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-518">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-519">September</span><span class="sxs-lookup"><span data-stu-id="c9b78-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c9b78-520">In Finance and Operations können statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c9b78-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="c9b78-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="c9b78-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c9b78-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-523">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-524">Größe</span><span class="sxs-lookup"><span data-stu-id="c9b78-524">Magnitude</span></span></th>
<th><span data-ttu-id="c9b78-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c9b78-525">Allocation factor</span></span></th>
<th><span data-ttu-id="c9b78-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-526">Amount</span></span></th>
<th><span data-ttu-id="c9b78-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-528">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-528">CC002</span></span></td>
<td><span data-ttu-id="c9b78-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-529">Finance</span></span></td>
<td><span data-ttu-id="c9b78-530">35</span><span class="sxs-lookup"><span data-stu-id="c9b78-530">35</span></span></td>
<td><span data-ttu-id="c9b78-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c9b78-532">175.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-532">175.00</span></span></td>
<td><span data-ttu-id="c9b78-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-534">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-534">CC003</span></span></td>
<td><span data-ttu-id="c9b78-535">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-535">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-536">55</span><span class="sxs-lookup"><span data-stu-id="c9b78-536">55</span></span></td>
<td><span data-ttu-id="c9b78-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c9b78-538">275.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-538">275.00</span></span></td>
<td><span data-ttu-id="c9b78-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-540">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-540">CC004</span></span></td>
<td><span data-ttu-id="c9b78-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-541">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-542">10</span><span class="sxs-lookup"><span data-stu-id="c9b78-542">10</span></span></td>
<td><span data-ttu-id="c9b78-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c9b78-544">50,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-544">50.00</span></span></td>
<td><span data-ttu-id="c9b78-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-546">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-546">CC002</span></span></td>
<td><span data-ttu-id="c9b78-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-547">Finance</span></span></td>
<td><span data-ttu-id="c9b78-548">35</span><span class="sxs-lookup"><span data-stu-id="c9b78-548">35</span></span></td>
<td><span data-ttu-id="c9b78-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c9b78-550">436.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-550">436.00</span></span></td>
<td><span data-ttu-id="c9b78-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-552">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-552">CC003</span></span></td>
<td><span data-ttu-id="c9b78-553">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-553">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-554">55</span><span class="sxs-lookup"><span data-stu-id="c9b78-554">55</span></span></td>
<td><span data-ttu-id="c9b78-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c9b78-556">685.14</span><span class="sxs-lookup"><span data-stu-id="c9b78-556">685.14</span></span></td>
<td><span data-ttu-id="c9b78-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-558">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-558">CC004</span></span></td>
<td><span data-ttu-id="c9b78-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-559">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-560">10</span><span class="sxs-lookup"><span data-stu-id="c9b78-560">10</span></span></td>
<td><span data-ttu-id="c9b78-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c9b78-562">124.57</span><span class="sxs-lookup"><span data-stu-id="c9b78-562">124.57</span></span></td>
<td><span data-ttu-id="c9b78-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c9b78-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-565">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-566">Größe</span><span class="sxs-lookup"><span data-stu-id="c9b78-566">Magnitude</span></span></th>
<th><span data-ttu-id="c9b78-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c9b78-567">Allocation factor</span></span></th>
<th><span data-ttu-id="c9b78-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-568">Amount</span></span></th>
<th><span data-ttu-id="c9b78-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-570">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-570">CC003</span></span></td>
<td><span data-ttu-id="c9b78-571">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-571">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-572">65</span><span class="sxs-lookup"><span data-stu-id="c9b78-572">65</span></span></td>
<td><span data-ttu-id="c9b78-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c9b78-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c9b78-574">438.75</span><span class="sxs-lookup"><span data-stu-id="c9b78-574">438.75</span></span></td>
<td><span data-ttu-id="c9b78-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-576">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-576">CC004</span></span></td>
<td><span data-ttu-id="c9b78-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-577">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-578">35</span><span class="sxs-lookup"><span data-stu-id="c9b78-578">35</span></span></td>
<td><span data-ttu-id="c9b78-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c9b78-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c9b78-580">236.25</span><span class="sxs-lookup"><span data-stu-id="c9b78-580">236.25</span></span></td>
<td><span data-ttu-id="c9b78-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-582">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-582">CC003</span></span></td>
<td><span data-ttu-id="c9b78-583">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-583">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-584">65</span><span class="sxs-lookup"><span data-stu-id="c9b78-584">65</span></span></td>
<td><span data-ttu-id="c9b78-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c9b78-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c9b78-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c9b78-586">5,297.69</span></span></td>
<td><span data-ttu-id="c9b78-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-588">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-588">CC004</span></span></td>
<td><span data-ttu-id="c9b78-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-589">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-590">35</span><span class="sxs-lookup"><span data-stu-id="c9b78-590">35</span></span></td>
<td><span data-ttu-id="c9b78-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c9b78-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c9b78-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c9b78-592">2,852.60</span></span></td>
<td><span data-ttu-id="c9b78-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c9b78-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-595">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-596">Größe</span><span class="sxs-lookup"><span data-stu-id="c9b78-596">Magnitude</span></span></th>
<th><span data-ttu-id="c9b78-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c9b78-597">Allocation factor</span></span></th>
<th><span data-ttu-id="c9b78-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-598">Amount</span></span></th>
<th><span data-ttu-id="c9b78-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-600">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-601">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-602">60</span><span class="sxs-lookup"><span data-stu-id="c9b78-602">60</span></span></td>
<td><span data-ttu-id="c9b78-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c9b78-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c9b78-604">535.31</span><span class="sxs-lookup"><span data-stu-id="c9b78-604">535.31</span></span></td>
<td><span data-ttu-id="c9b78-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-606">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-607">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-608">20</span><span class="sxs-lookup"><span data-stu-id="c9b78-608">20</span></span></td>
<td><span data-ttu-id="c9b78-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c9b78-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c9b78-610">178.44</span><span class="sxs-lookup"><span data-stu-id="c9b78-610">178.44</span></span></td>
<td><span data-ttu-id="c9b78-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-612">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-613">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-614">60</span><span class="sxs-lookup"><span data-stu-id="c9b78-614">60</span></span></td>
<td><span data-ttu-id="c9b78-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c9b78-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c9b78-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c9b78-616">4,487.12</span></span></td>
<td><span data-ttu-id="c9b78-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-618">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-619">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-620">20</span><span class="sxs-lookup"><span data-stu-id="c9b78-620">20</span></span></td>
<td><span data-ttu-id="c9b78-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c9b78-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c9b78-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-622">1,495.71</span></span></td>
<td><span data-ttu-id="c9b78-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9b78-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="c9b78-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-625">Cost object</span></span></th>
<th><span data-ttu-id="c9b78-626">Größe</span><span class="sxs-lookup"><span data-stu-id="c9b78-626">Magnitude</span></span></th>
<th><span data-ttu-id="c9b78-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="c9b78-627">Allocation factor</span></span></th>
<th><span data-ttu-id="c9b78-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-628">Amount</span></span></th>
<th><span data-ttu-id="c9b78-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-630">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-631">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-632">80</span><span class="sxs-lookup"><span data-stu-id="c9b78-632">80</span></span></td>
<td><span data-ttu-id="c9b78-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c9b78-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c9b78-634">241.05</span><span class="sxs-lookup"><span data-stu-id="c9b78-634">241.05</span></span></td>
<td><span data-ttu-id="c9b78-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-636">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-637">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-638">15</span><span class="sxs-lookup"><span data-stu-id="c9b78-638">15</span></span></td>
<td><span data-ttu-id="c9b78-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c9b78-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c9b78-640">45.20</span><span class="sxs-lookup"><span data-stu-id="c9b78-640">45.20</span></span></td>
<td><span data-ttu-id="c9b78-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-642">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-643">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-644">80</span><span class="sxs-lookup"><span data-stu-id="c9b78-644">80</span></span></td>
<td><span data-ttu-id="c9b78-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c9b78-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c9b78-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c9b78-646">2,507.09</span></span></td>
<td><span data-ttu-id="c9b78-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-648">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-649">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-650">15</span><span class="sxs-lookup"><span data-stu-id="c9b78-650">15</span></span></td>
<td><span data-ttu-id="c9b78-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c9b78-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c9b78-652">470.08</span><span class="sxs-lookup"><span data-stu-id="c9b78-652">470.08</span></span></td>
<td><span data-ttu-id="c9b78-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c9b78-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="c9b78-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="c9b78-655">Journal</span></span></th>
<th><span data-ttu-id="c9b78-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="c9b78-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c9b78-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c9b78-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c9b78-658">Version</span><span class="sxs-lookup"><span data-stu-id="c9b78-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-659">00004</span><span class="sxs-lookup"><span data-stu-id="c9b78-659">00004</span></span></td>
<td><span data-ttu-id="c9b78-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="c9b78-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c9b78-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="c9b78-661">Fiscal</span></span></td>
<td><span data-ttu-id="c9b78-662">2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-662">2017</span></span></td>
<td><span data-ttu-id="c9b78-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-663">Period 1</span></span></td>
<td><span data-ttu-id="c9b78-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c9b78-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="c9b78-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9b78-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-668">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-669">Cost behavior</span></span></th>
<th><span data-ttu-id="c9b78-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-672">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-672">CC001</span></span></td>
<td><span data-ttu-id="c9b78-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-673">HR</span></span></td>
<td><span data-ttu-id="c9b78-674">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-674">10001</span></span></td>
<td><span data-ttu-id="c9b78-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-675">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-676">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-677">500,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-679">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-679">CC001</span></span></td>
<td><span data-ttu-id="c9b78-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-680">HR</span></span></td>
<td><span data-ttu-id="c9b78-681">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-681">10001</span></span></td>
<td><span data-ttu-id="c9b78-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-682">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-683">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-686">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-686">CC002</span></span></td>
<td><span data-ttu-id="c9b78-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-687">Finance</span></span></td>
<td><span data-ttu-id="c9b78-688">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-688">10001</span></span></td>
<td><span data-ttu-id="c9b78-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-689">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-690">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-691">675.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-693">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-693">CC002</span></span></td>
<td><span data-ttu-id="c9b78-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-694">Finance</span></span></td>
<td><span data-ttu-id="c9b78-695">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-695">10001</span></span></td>
<td><span data-ttu-id="c9b78-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-696">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-697">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c9b78-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-700">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-700">CC003</span></span></td>
<td><span data-ttu-id="c9b78-701">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-701">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-702">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-702">10001</span></span></td>
<td><span data-ttu-id="c9b78-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-703">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-704">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-705">713.75</span><span class="sxs-lookup"><span data-stu-id="c9b78-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-707">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-707">CC003</span></span></td>
<td><span data-ttu-id="c9b78-708">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-708">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-709">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-709">10001</span></span></td>
<td><span data-ttu-id="c9b78-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-710">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-711">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c9b78-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-714">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-714">CC003</span></span></td>
<td><span data-ttu-id="c9b78-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-715">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-716">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-716">10001</span></span></td>
<td><span data-ttu-id="c9b78-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-717">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-718">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-719">286.25</span><span class="sxs-lookup"><span data-stu-id="c9b78-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-721">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-721">CC003</span></span></td>
<td><span data-ttu-id="c9b78-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-722">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-723">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-723">10001</span></span></td>
<td><span data-ttu-id="c9b78-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-724">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-725">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c9b78-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-728">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-729">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-730">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-730">10001</span></span></td>
<td><span data-ttu-id="c9b78-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-731">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-732">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-733">776.36</span><span class="sxs-lookup"><span data-stu-id="c9b78-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-735">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-736">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-737">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-737">10001</span></span></td>
<td><span data-ttu-id="c9b78-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-738">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-739">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c9b78-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-742">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-743">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-744">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-744">10001</span></span></td>
<td><span data-ttu-id="c9b78-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-745">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-746">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-747">223.64</span><span class="sxs-lookup"><span data-stu-id="c9b78-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9b78-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-749">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-750">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-751">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-751">10001</span></span></td>
<td><span data-ttu-id="c9b78-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-752">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-753">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c9b78-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c9b78-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="c9b78-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9b78-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9b78-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-757">Cost element</span></span></th>
<th><span data-ttu-id="c9b78-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="c9b78-758">Cost behavior</span></span></th>
<th><span data-ttu-id="c9b78-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="c9b78-759">Amount</span></span></th>
<th><span data-ttu-id="c9b78-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="c9b78-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9b78-761">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-761">CC001</span></span></td>
<td><span data-ttu-id="c9b78-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-762">HR</span></span></td>
<td><span data-ttu-id="c9b78-763">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-763">10001</span></span></td>
<td><span data-ttu-id="c9b78-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-764">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-765">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-766">-500.00</span></span></td>
<td><span data-ttu-id="c9b78-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-768">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-768">CC002</span></span></td>
<td><span data-ttu-id="c9b78-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-769">Finance</span></span></td>
<td><span data-ttu-id="c9b78-770">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-770">10001</span></span></td>
<td><span data-ttu-id="c9b78-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-771">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-772">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-773">175.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-773">175.00</span></span></td>
<td><span data-ttu-id="c9b78-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-775">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-775">CC003</span></span></td>
<td><span data-ttu-id="c9b78-776">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-776">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-777">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-777">10001</span></span></td>
<td><span data-ttu-id="c9b78-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-778">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-779">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-780">275.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-780">275.00</span></span></td>
<td><span data-ttu-id="c9b78-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-782">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-782">CC004</span></span></td>
<td><span data-ttu-id="c9b78-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-783">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-784">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-784">10001</span></span></td>
<td><span data-ttu-id="c9b78-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-785">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-786">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-787">50,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-787">50,00</span></span></td>
<td><span data-ttu-id="c9b78-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-789">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-789">CC001</span></span></td>
<td><span data-ttu-id="c9b78-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9b78-790">HR</span></span></td>
<td><span data-ttu-id="c9b78-791">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-791">10001</span></span></td>
<td><span data-ttu-id="c9b78-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-792">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-793">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-794">-1,245.71</span></span></td>
<td><span data-ttu-id="c9b78-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-796">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-796">CC002</span></span></td>
<td><span data-ttu-id="c9b78-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-797">Finance</span></span></td>
<td><span data-ttu-id="c9b78-798">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-798">10001</span></span></td>
<td><span data-ttu-id="c9b78-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-799">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-800">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-801">436.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-801">436.00</span></span></td>
<td><span data-ttu-id="c9b78-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-803">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-803">CC003</span></span></td>
<td><span data-ttu-id="c9b78-804">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-804">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-805">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-805">10001</span></span></td>
<td><span data-ttu-id="c9b78-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-806">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-807">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-808">685.14</span><span class="sxs-lookup"><span data-stu-id="c9b78-808">685.14</span></span></td>
<td><span data-ttu-id="c9b78-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-810">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-810">CC004</span></span></td>
<td><span data-ttu-id="c9b78-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-811">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-812">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-812">10001</span></span></td>
<td><span data-ttu-id="c9b78-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-813">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-814">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-815">124.57</span><span class="sxs-lookup"><span data-stu-id="c9b78-815">124.57</span></span></td>
<td><span data-ttu-id="c9b78-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-817">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-817">CC002</span></span></td>
<td><span data-ttu-id="c9b78-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-818">Finance</span></span></td>
<td><span data-ttu-id="c9b78-819">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-819">10001</span></span></td>
<td><span data-ttu-id="c9b78-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-820">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-821">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="c9b78-822">-675.00</span></span></td>
<td><span data-ttu-id="c9b78-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-824">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-824">CC003</span></span></td>
<td><span data-ttu-id="c9b78-825">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-825">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-826">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-826">10001</span></span></td>
<td><span data-ttu-id="c9b78-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-827">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-828">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-829">438.75</span><span class="sxs-lookup"><span data-stu-id="c9b78-829">438.75</span></span></td>
<td><span data-ttu-id="c9b78-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-831">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-831">CC004</span></span></td>
<td><span data-ttu-id="c9b78-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-832">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-833">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-833">10001</span></span></td>
<td><span data-ttu-id="c9b78-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-834">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-835">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-836">236.25</span><span class="sxs-lookup"><span data-stu-id="c9b78-836">236.25</span></span></td>
<td><span data-ttu-id="c9b78-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-838">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-838">CC002</span></span></td>
<td><span data-ttu-id="c9b78-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c9b78-839">Finance</span></span></td>
<td><span data-ttu-id="c9b78-840">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-840">10001</span></span></td>
<td><span data-ttu-id="c9b78-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-841">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-842">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="c9b78-843">-8,150.29</span></span></td>
<td><span data-ttu-id="c9b78-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-845">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-845">CC003</span></span></td>
<td><span data-ttu-id="c9b78-846">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-846">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-847">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-847">10001</span></span></td>
<td><span data-ttu-id="c9b78-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-848">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-849">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c9b78-850">5,297.69</span></span></td>
<td><span data-ttu-id="c9b78-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-852">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-852">CC004</span></span></td>
<td><span data-ttu-id="c9b78-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="c9b78-853">Packaging</span></span></td>
<td><span data-ttu-id="c9b78-854">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-854">10001</span></span></td>
<td><span data-ttu-id="c9b78-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-855">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-856">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c9b78-857">2,852.60</span></span></td>
<td><span data-ttu-id="c9b78-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-859">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-859">CC003</span></span></td>
<td><span data-ttu-id="c9b78-860">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-860">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-861">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-861">10001</span></span></td>
<td><span data-ttu-id="c9b78-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-862">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-863">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="c9b78-864">-713.75</span></span></td>
<td><span data-ttu-id="c9b78-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-866">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-867">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-868">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-868">10001</span></span></td>
<td><span data-ttu-id="c9b78-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-869">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-870">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-871">535.31</span><span class="sxs-lookup"><span data-stu-id="c9b78-871">535.31</span></span></td>
<td><span data-ttu-id="c9b78-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-873">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-874">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-875">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-875">10001</span></span></td>
<td><span data-ttu-id="c9b78-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-876">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-877">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-878">178.44</span><span class="sxs-lookup"><span data-stu-id="c9b78-878">178.44</span></span></td>
<td><span data-ttu-id="c9b78-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-880">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-880">CC003</span></span></td>
<td><span data-ttu-id="c9b78-881">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-881">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-882">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-882">10001</span></span></td>
<td><span data-ttu-id="c9b78-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-883">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-884">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="c9b78-885">-5,982.83</span></span></td>
<td><span data-ttu-id="c9b78-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-887">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-888">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-889">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-889">10001</span></span></td>
<td><span data-ttu-id="c9b78-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-890">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-891">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c9b78-892">4,487.12</span></span></td>
<td><span data-ttu-id="c9b78-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-894">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-895">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-896">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-896">10001</span></span></td>
<td><span data-ttu-id="c9b78-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-897">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-898">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c9b78-899">1,495.71</span></span></td>
<td><span data-ttu-id="c9b78-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-901">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-901">CC003</span></span></td>
<td><span data-ttu-id="c9b78-902">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-902">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-903">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-903">10001</span></span></td>
<td><span data-ttu-id="c9b78-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-904">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-905">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="c9b78-906">-286.25</span></span></td>
<td><span data-ttu-id="c9b78-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-908">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-909">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-910">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-910">10001</span></span></td>
<td><span data-ttu-id="c9b78-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-911">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-912">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-913">241.05</span><span class="sxs-lookup"><span data-stu-id="c9b78-913">241.05</span></span></td>
<td><span data-ttu-id="c9b78-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-915">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-916">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-917">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-917">10001</span></span></td>
<td><span data-ttu-id="c9b78-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-918">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-919">Fixed cost</span></span></td>
<td><span data-ttu-id="c9b78-920">45.20</span><span class="sxs-lookup"><span data-stu-id="c9b78-920">45.20</span></span></td>
<td><span data-ttu-id="c9b78-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-922">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-922">CC003</span></span></td>
<td><span data-ttu-id="c9b78-923">Montage</span><span class="sxs-lookup"><span data-stu-id="c9b78-923">Assembly</span></span></td>
<td><span data-ttu-id="c9b78-924">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-924">10001</span></span></td>
<td><span data-ttu-id="c9b78-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-925">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-926">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="c9b78-927">-2,977.17</span></span></td>
<td><span data-ttu-id="c9b78-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-929">Prod 1</span></span></td>
<td><span data-ttu-id="c9b78-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-930">Product 1</span></span></td>
<td><span data-ttu-id="c9b78-931">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-931">10001</span></span></td>
<td><span data-ttu-id="c9b78-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-932">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-933">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c9b78-934">2,507.09</span></span></td>
<td><span data-ttu-id="c9b78-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9b78-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-936">Prod 2</span></span></td>
<td><span data-ttu-id="c9b78-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-937">Product 2</span></span></td>
<td><span data-ttu-id="c9b78-938">10001</span><span class="sxs-lookup"><span data-stu-id="c9b78-938">10001</span></span></td>
<td><span data-ttu-id="c9b78-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-939">Electricity</span></span></td>
<td><span data-ttu-id="c9b78-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-940">Variable cost</span></span></td>
<td><span data-ttu-id="c9b78-941">470.08</span><span class="sxs-lookup"><span data-stu-id="c9b78-941">470.08</span></span></td>
<td><span data-ttu-id="c9b78-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="c9b78-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c9b78-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="c9b78-943">Conclusion</span></span>
<span data-ttu-id="c9b78-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c9b78-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c9b78-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c9b78-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9b78-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c9b78-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c9b78-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c9b78-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="c9b78-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c9b78-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9b78-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c9b78-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="c9b78-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c9b78-951">CC099</span><span class="sxs-lookup"><span data-stu-id="c9b78-951">CC099</span></span></th>
<th><span data-ttu-id="c9b78-952">CC001</span><span class="sxs-lookup"><span data-stu-id="c9b78-952">CC001</span></span></th>
<th><span data-ttu-id="c9b78-953">CC002</span><span class="sxs-lookup"><span data-stu-id="c9b78-953">CC002</span></span></th>
<th><span data-ttu-id="c9b78-954">CC003</span><span class="sxs-lookup"><span data-stu-id="c9b78-954">CC003</span></span></th>
<th><span data-ttu-id="c9b78-955">CC004</span><span class="sxs-lookup"><span data-stu-id="c9b78-955">CC004</span></span></th>
<th><span data-ttu-id="c9b78-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-956">Proj 1</span></span></th>
<th><span data-ttu-id="c9b78-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-957">Proj 2</span></span></th>
<th><span data-ttu-id="c9b78-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="c9b78-958">Prod 1</span></span></th>
<th><span data-ttu-id="c9b78-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="c9b78-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c9b78-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="c9b78-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c9b78-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="c9b78-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-971">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c9b78-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-973">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-974">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-975">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-976">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-977">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-978">776.36</span><span class="sxs-lookup"><span data-stu-id="c9b78-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-979">223.64</span><span class="sxs-lookup"><span data-stu-id="c9b78-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c9b78-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="c9b78-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-982">000</span><span class="sxs-lookup"><span data-stu-id="c9b78-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-983">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-984">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-985">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-986">0,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-987">30,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-988">10,00</span><span class="sxs-lookup"><span data-stu-id="c9b78-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c9b78-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c9b78-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9b78-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9b78-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c9b78-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="c9b78-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c9b78-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c9b78-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c9b78-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="c9b78-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c9b78-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="c9b78-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c9b78-996">Weitere Informationen hierzu finden Sie unter [Kostenzusammenfassung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="c9b78-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




