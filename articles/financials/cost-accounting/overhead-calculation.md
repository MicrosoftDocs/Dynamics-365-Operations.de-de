---
title: Gemeinkostenberechnung
description: "In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="5aa56-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="5aa56-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5aa56-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5aa56-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="5aa56-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="5aa56-105">Term definition</span></span>
---------------

<span data-ttu-id="5aa56-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="5aa56-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5aa56-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="5aa56-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5aa56-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="5aa56-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5aa56-109">Miete</span><span class="sxs-lookup"><span data-stu-id="5aa56-109">Rent</span></span>
-   <span data-ttu-id="5aa56-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-110">Electricity</span></span>
-   <span data-ttu-id="5aa56-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="5aa56-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5aa56-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="5aa56-112">Overhead calculation overview</span></span>
<span data-ttu-id="5aa56-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5aa56-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5aa56-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5aa56-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="5aa56-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5aa56-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="5aa56-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5aa56-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5aa56-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5aa56-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="5aa56-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5aa56-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="5aa56-119">Version type</span></span>
-   <span data-ttu-id="5aa56-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="5aa56-120">Date and time</span></span>
-   <span data-ttu-id="5aa56-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="5aa56-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5aa56-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="5aa56-122">Fiscal year</span></span>
-   <span data-ttu-id="5aa56-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="5aa56-123">Fiscal period</span></span>

<span data-ttu-id="5aa56-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5aa56-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5aa56-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5aa56-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5aa56-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5aa56-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="5aa56-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5aa56-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="5aa56-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5aa56-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="5aa56-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5aa56-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="5aa56-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5aa56-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5aa56-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5aa56-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="5aa56-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5aa56-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="5aa56-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5aa56-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5aa56-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5aa56-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5aa56-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="5aa56-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5aa56-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="5aa56-140">Main account</span></span></th>
<th><span data-ttu-id="5aa56-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="5aa56-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5aa56-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-143">CC099</span></span></td>
<td><span data-ttu-id="5aa56-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-144">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-145">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-145">10001</span></span></td>
<td><span data-ttu-id="5aa56-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-146">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5aa56-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="5aa56-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5aa56-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="5aa56-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5aa56-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="5aa56-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5aa56-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="5aa56-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5aa56-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="5aa56-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5aa56-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="5aa56-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5aa56-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="5aa56-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5aa56-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="5aa56-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5aa56-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5aa56-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="5aa56-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5aa56-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="5aa56-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5aa56-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5aa56-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5aa56-160">Journal</span></span></th>
<th><span data-ttu-id="5aa56-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="5aa56-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5aa56-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5aa56-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5aa56-163">Version</span><span class="sxs-lookup"><span data-stu-id="5aa56-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-164">00001</span><span class="sxs-lookup"><span data-stu-id="5aa56-164">00001</span></span></td>
<td><span data-ttu-id="5aa56-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="5aa56-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5aa56-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5aa56-166">Fiscal</span></span></td>
<td><span data-ttu-id="5aa56-167">2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-167">2017</span></span></td>
<td><span data-ttu-id="5aa56-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-168">Period 1</span></span></td>
<td><span data-ttu-id="5aa56-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5aa56-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="5aa56-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-173">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5aa56-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5aa56-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-177">CC099</span></span></td>
<td><span data-ttu-id="5aa56-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-178">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-179">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-179">10001</span></span></td>
<td><span data-ttu-id="5aa56-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-180">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="5aa56-181">Unclassified</span></span></td>
<td><span data-ttu-id="5aa56-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5aa56-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="5aa56-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-185">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5aa56-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-187">Amount</span></span></th>
<th><span data-ttu-id="5aa56-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-189">CC099</span></span></td>
<td><span data-ttu-id="5aa56-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-190">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-191">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-191">10001</span></span></td>
<td><span data-ttu-id="5aa56-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-192">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="5aa56-193">Unclassified</span></span></td>
<td><span data-ttu-id="5aa56-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-194">10,000.00</span></span></td>
<td><span data-ttu-id="5aa56-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-196">CC099</span></span></td>
<td><span data-ttu-id="5aa56-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-197">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-198">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-198">10001</span></span></td>
<td><span data-ttu-id="5aa56-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-199">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="5aa56-200">Unclassified</span></span></td>
<td><span data-ttu-id="5aa56-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5aa56-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-203">CC099</span></span></td>
<td><span data-ttu-id="5aa56-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-204">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-205">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-205">10001</span></span></td>
<td><span data-ttu-id="5aa56-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-206">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-208">1,000.00</span></span></td>
<td><span data-ttu-id="5aa56-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-210">CC099</span></span></td>
<td><span data-ttu-id="5aa56-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-211">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-212">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-212">10001</span></span></td>
<td><span data-ttu-id="5aa56-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-213">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-214">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-215">9,000.00</span></span></td>
<td><span data-ttu-id="5aa56-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-217">Detaillierte Informationen zum Kostenverhalten finden Sie in der Richtlinie Kostenverhalten.</span><span class="sxs-lookup"><span data-stu-id="5aa56-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="5aa56-218">(Beachten Sie, dass dieses Thema noch nicht abgedeckt ist, aber bald verfügbar sein wird.)</span><span class="sxs-lookup"><span data-stu-id="5aa56-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5aa56-219">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="5aa56-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5aa56-220">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5aa56-221">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="5aa56-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5aa56-222">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="5aa56-222">Define the cost distribution rule</span></span>

<span data-ttu-id="5aa56-223">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="5aa56-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5aa56-224">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="5aa56-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5aa56-225">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5aa56-226">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="5aa56-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5aa56-227">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="5aa56-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5aa56-228">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5aa56-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-229">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-229">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-230">KWH</span><span class="sxs-lookup"><span data-stu-id="5aa56-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-231">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-231">CC001</span></span></td>
<td><span data-ttu-id="5aa56-232">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-232">HR</span></span></td>
<td><span data-ttu-id="5aa56-233">1.000</span><span class="sxs-lookup"><span data-stu-id="5aa56-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-234">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-234">CC002</span></span></td>
<td><span data-ttu-id="5aa56-235">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-235">Finance</span></span></td>
<td><span data-ttu-id="5aa56-236">6.000</span><span class="sxs-lookup"><span data-stu-id="5aa56-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-237">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-237">CC003</span></span></td>
<td><span data-ttu-id="5aa56-238">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-238">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-239">0</span><span class="sxs-lookup"><span data-stu-id="5aa56-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-240">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5aa56-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-241">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-241">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-242">Größe</span><span class="sxs-lookup"><span data-stu-id="5aa56-242">Magnitude</span></span></th>
<th><span data-ttu-id="5aa56-243">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5aa56-243">Allocation factor</span></span></th>
<th><span data-ttu-id="5aa56-244">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-245">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-245">CC001</span></span></td>
<td><span data-ttu-id="5aa56-246">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-246">HR</span></span></td>
<td><span data-ttu-id="5aa56-247">1.000</span><span class="sxs-lookup"><span data-stu-id="5aa56-247">1,000</span></span></td>
<td><span data-ttu-id="5aa56-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5aa56-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-250">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-250">CC002</span></span></td>
<td><span data-ttu-id="5aa56-251">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-251">Finance</span></span></td>
<td><span data-ttu-id="5aa56-252">6.000</span><span class="sxs-lookup"><span data-stu-id="5aa56-252">6,000</span></span></td>
<td><span data-ttu-id="5aa56-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5aa56-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5aa56-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-255">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-255">CC003</span></span></td>
<td><span data-ttu-id="5aa56-256">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-256">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-257">0</span><span class="sxs-lookup"><span data-stu-id="5aa56-257">0</span></span></td>
<td><span data-ttu-id="5aa56-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5aa56-259">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-260">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="5aa56-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5aa56-261">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5aa56-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-262">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-262">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-263">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="5aa56-263">Formula</span></span></th>
<th><span data-ttu-id="5aa56-264">Größe</span><span class="sxs-lookup"><span data-stu-id="5aa56-264">Magnitude</span></span></th>
<th><span data-ttu-id="5aa56-265">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5aa56-265">Allocation factor</span></span></th>
<th><span data-ttu-id="5aa56-266">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-267">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-267">CC001</span></span></td>
<td><span data-ttu-id="5aa56-268">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-268">HR</span></span></td>
<td><span data-ttu-id="5aa56-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5aa56-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5aa56-270">1</span><span class="sxs-lookup"><span data-stu-id="5aa56-270">1</span></span></td>
<td><span data-ttu-id="5aa56-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5aa56-272">500,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-273">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-273">CC002</span></span></td>
<td><span data-ttu-id="5aa56-274">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-274">Finance</span></span></td>
<td><span data-ttu-id="5aa56-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5aa56-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5aa56-276">1</span><span class="sxs-lookup"><span data-stu-id="5aa56-276">1</span></span></td>
<td><span data-ttu-id="5aa56-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5aa56-278">500,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-279">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-279">CC003</span></span></td>
<td><span data-ttu-id="5aa56-280">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-280">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5aa56-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5aa56-282">0</span><span class="sxs-lookup"><span data-stu-id="5aa56-282">0</span></span></td>
<td><span data-ttu-id="5aa56-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5aa56-284">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5aa56-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5aa56-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-286">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5aa56-286">Journal</span></span></th>
<th><span data-ttu-id="5aa56-287">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="5aa56-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5aa56-288">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5aa56-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5aa56-289">Version</span><span class="sxs-lookup"><span data-stu-id="5aa56-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-290">00002</span><span class="sxs-lookup"><span data-stu-id="5aa56-290">00002</span></span></td>
<td><span data-ttu-id="5aa56-291">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="5aa56-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5aa56-292">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5aa56-292">Fiscal</span></span></td>
<td><span data-ttu-id="5aa56-293">2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-293">2017</span></span></td>
<td><span data-ttu-id="5aa56-294">Periode 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-294">Period 1</span></span></td>
<td><span data-ttu-id="5aa56-295">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5aa56-296">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="5aa56-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-297">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-298">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-299">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-299">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-300">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-300">Cost behavior</span></span></th>
<th><span data-ttu-id="5aa56-301">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-302">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-303">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-303">CC099</span></span></td>
<td><span data-ttu-id="5aa56-304">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-304">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-305">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-305">10001</span></span></td>
<td><span data-ttu-id="5aa56-306">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-306">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-307">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-307">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-309">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-310">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-310">CC099</span></span></td>
<td><span data-ttu-id="5aa56-311">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-311">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-312">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-312">10001</span></span></td>
<td><span data-ttu-id="5aa56-313">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-313">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-314">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-314">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-315">9.000,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5aa56-316">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="5aa56-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-317">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-318">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-318">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-319">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-319">Cost behavior</span></span></th>
<th><span data-ttu-id="5aa56-320">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-320">Amount</span></span></th>
<th><span data-ttu-id="5aa56-321">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-322">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-322">CC099</span></span></td>
<td><span data-ttu-id="5aa56-323">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-323">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-324">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-324">10001</span></span></td>
<td><span data-ttu-id="5aa56-325">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-325">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-326">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-326">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-327">-1,000.00</span></span></td>
<td><span data-ttu-id="5aa56-328">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-329">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-329">CC001</span></span></td>
<td><span data-ttu-id="5aa56-330">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-330">HR</span></span></td>
<td><span data-ttu-id="5aa56-331">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-331">10001</span></span></td>
<td><span data-ttu-id="5aa56-332">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-332">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-333">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-333">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-334">500,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-334">500.00</span></span></td>
<td><span data-ttu-id="5aa56-335">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-336">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-336">CC002</span></span></td>
<td><span data-ttu-id="5aa56-337">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-337">Finance</span></span></td>
<td><span data-ttu-id="5aa56-338">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-338">10001</span></span></td>
<td><span data-ttu-id="5aa56-339">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-339">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-340">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-340">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-341">500,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-341">500.00</span></span></td>
<td><span data-ttu-id="5aa56-342">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-343">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-343">CC099</span></span></td>
<td><span data-ttu-id="5aa56-344">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5aa56-344">Default cost center</span></span></td>
<td><span data-ttu-id="5aa56-345">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-345">10001</span></span></td>
<td><span data-ttu-id="5aa56-346">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-346">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-347">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-347">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-348">-9,000.00</span></span></td>
<td><span data-ttu-id="5aa56-349">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-350">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-350">CC001</span></span></td>
<td><span data-ttu-id="5aa56-351">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-351">HR</span></span></td>
<td><span data-ttu-id="5aa56-352">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-352">10001</span></span></td>
<td><span data-ttu-id="5aa56-353">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-353">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-354">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-354">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-355">1,285.71</span></span></td>
<td><span data-ttu-id="5aa56-356">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-357">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-357">CC002</span></span></td>
<td><span data-ttu-id="5aa56-358">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-358">Finance</span></span></td>
<td><span data-ttu-id="5aa56-359">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-359">10001</span></span></td>
<td><span data-ttu-id="5aa56-360">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-360">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-361">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-361">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5aa56-362">7,714.29</span></span></td>
<td><span data-ttu-id="5aa56-363">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-364">Detaillierte Informationen zur Verrechnungsgrundlage und der Kostenaufteilung finden Sie unter Richtlinie zur Verrechnungsgrundlage und der Kostenbasis.</span><span class="sxs-lookup"><span data-stu-id="5aa56-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="5aa56-365">(Beachten Sie, dass dieses Thema noch nicht abgedeckt ist, aber bald verfügbar sein wird.)</span><span class="sxs-lookup"><span data-stu-id="5aa56-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5aa56-366">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="5aa56-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5aa56-367">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="5aa56-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5aa56-368">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="5aa56-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5aa56-369">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="5aa56-369">Define the overhead rate</span></span>

<span data-ttu-id="5aa56-370">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="5aa56-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5aa56-371">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-372">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-372">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-373">Stunden</span><span class="sxs-lookup"><span data-stu-id="5aa56-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-374">Proj 1</span></span></td>
<td><span data-ttu-id="5aa56-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-375">Project 1</span></span></td>
<td><span data-ttu-id="5aa56-376">3</span><span class="sxs-lookup"><span data-stu-id="5aa56-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-377">Proj 2</span></span></td>
<td><span data-ttu-id="5aa56-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-378">Project 2</span></span></td>
<td><span data-ttu-id="5aa56-379">1</span><span class="sxs-lookup"><span data-stu-id="5aa56-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-380">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="5aa56-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-381">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-381">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-382">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-382">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-383">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-383">Cost behavior</span></span></th>
<th><span data-ttu-id="5aa56-384">Einheiten</span><span class="sxs-lookup"><span data-stu-id="5aa56-384">Units</span></span></th>
<th><span data-ttu-id="5aa56-385">Satz</span><span class="sxs-lookup"><span data-stu-id="5aa56-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-386">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-386">CC001</span></span></td>
<td><span data-ttu-id="5aa56-387">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-387">HR</span></span></td>
<td><span data-ttu-id="5aa56-388">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-388">10001</span></span></td>
<td><span data-ttu-id="5aa56-389">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-389">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-390">1</span><span class="sxs-lookup"><span data-stu-id="5aa56-390">1</span></span></td>
<td><span data-ttu-id="5aa56-391">10</span><span class="sxs-lookup"><span data-stu-id="5aa56-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-392">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-393">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-393">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-394">Größe</span><span class="sxs-lookup"><span data-stu-id="5aa56-394">Magnitude</span></span></th>
<th><span data-ttu-id="5aa56-395">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-395">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-396">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5aa56-396">Allocation factor</span></span></th>
<th><span data-ttu-id="5aa56-397">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-398">Proj 1</span></span></td>
<td><span data-ttu-id="5aa56-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-399">Project 1</span></span></td>
<td><span data-ttu-id="5aa56-400">3</span><span class="sxs-lookup"><span data-stu-id="5aa56-400">3</span></span></td>
<td><span data-ttu-id="5aa56-401">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-401">10001</span></span></td>
<td><span data-ttu-id="5aa56-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5aa56-403">30,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-404">Proj 2</span></span></td>
<td><span data-ttu-id="5aa56-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-405">Project 2</span></span></td>
<td><span data-ttu-id="5aa56-406">1</span><span class="sxs-lookup"><span data-stu-id="5aa56-406">1</span></span></td>
<td><span data-ttu-id="5aa56-407">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-407">10001</span></span></td>
<td><span data-ttu-id="5aa56-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5aa56-409">10,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5aa56-410">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5aa56-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-411">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5aa56-411">Journal</span></span></th>
<th><span data-ttu-id="5aa56-412">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="5aa56-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5aa56-413">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5aa56-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5aa56-414">Version</span><span class="sxs-lookup"><span data-stu-id="5aa56-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-415">00003</span><span class="sxs-lookup"><span data-stu-id="5aa56-415">00003</span></span></td>
<td><span data-ttu-id="5aa56-416">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="5aa56-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5aa56-417">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5aa56-417">Fiscal</span></span></td>
<td><span data-ttu-id="5aa56-418">2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-418">2017</span></span></td>
<td><span data-ttu-id="5aa56-419">Periode 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-419">Period 1</span></span></td>
<td><span data-ttu-id="5aa56-420">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5aa56-421">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="5aa56-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-422">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-423">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-423">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-424">Größe</span><span class="sxs-lookup"><span data-stu-id="5aa56-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-425">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-426">Proj 1</span></span></td>
<td><span data-ttu-id="5aa56-427">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5aa56-428">3,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-429">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-430">Proj 2</span></span></td>
<td><span data-ttu-id="5aa56-431">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5aa56-432">1,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5aa56-433">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="5aa56-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-434">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-435">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-435">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-436">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-436">Cost behavior</span></span></th>
<th><span data-ttu-id="5aa56-437">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-437">Amount</span></span></th>
<th><span data-ttu-id="5aa56-438">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="5aa56-439">CC0001</span></span></td>
<td><span data-ttu-id="5aa56-440">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-440">HR</span></span></td>
<td><span data-ttu-id="5aa56-441">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-441">10001</span></span></td>
<td><span data-ttu-id="5aa56-442">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-442">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-443">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-443">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-444">-30.00</span></span></td>
<td><span data-ttu-id="5aa56-445">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-446">Proj 1</span></span></td>
<td><span data-ttu-id="5aa56-447">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5aa56-448">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-448">10001</span></span></td>
<td><span data-ttu-id="5aa56-449">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-449">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-450">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-450">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-451">30,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-451">30.00</span></span></td>
<td><span data-ttu-id="5aa56-452">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-453">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-453">CC001</span></span></td>
<td><span data-ttu-id="5aa56-454">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-454">HR</span></span></td>
<td><span data-ttu-id="5aa56-455">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-455">10001</span></span></td>
<td><span data-ttu-id="5aa56-456">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-456">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-457">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-457">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-458">-10.00</span></span></td>
<td><span data-ttu-id="5aa56-459">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-460">Proj 2</span></span></td>
<td><span data-ttu-id="5aa56-461">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5aa56-462">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-462">10001</span></span></td>
<td><span data-ttu-id="5aa56-463">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-463">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-464">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-464">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-465">10,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-465">10.00</span></span></td>
<td><span data-ttu-id="5aa56-466">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-467">Detaillierte Informationen zur Richtlinie über Gemeinkostensätze finden Sie in der Richtlinie Gemeinkostensatz und Zuweisungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="5aa56-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="5aa56-468">(Beachten Sie, dass dieses Thema noch nicht abgedeckt ist, aber bald verfügbar sein wird.)</span><span class="sxs-lookup"><span data-stu-id="5aa56-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5aa56-469">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="5aa56-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5aa56-470">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5aa56-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5aa56-471">Finance and Operations unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="5aa56-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="5aa56-472">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5aa56-473">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5aa56-474">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5aa56-475">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5aa56-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5aa56-476">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5aa56-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5aa56-477">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5aa56-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5aa56-478">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="5aa56-478">Define the cost allocation</span></span>

<span data-ttu-id="5aa56-479">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="5aa56-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5aa56-480">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="5aa56-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5aa56-481">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-482">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-482">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-483">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="5aa56-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-484">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-484">CC002</span></span></td>
<td><span data-ttu-id="5aa56-485">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-485">Finance</span></span></td>
<td><span data-ttu-id="5aa56-486">35</span><span class="sxs-lookup"><span data-stu-id="5aa56-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-487">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-487">CC003</span></span></td>
<td><span data-ttu-id="5aa56-488">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-488">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-489">55</span><span class="sxs-lookup"><span data-stu-id="5aa56-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-490">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-490">CC004</span></span></td>
<td><span data-ttu-id="5aa56-491">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-491">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-492">10</span><span class="sxs-lookup"><span data-stu-id="5aa56-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-493">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="5aa56-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5aa56-494">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-495">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-495">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-496">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="5aa56-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-497">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-497">CC003</span></span></td>
<td><span data-ttu-id="5aa56-498">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-498">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-499">65</span><span class="sxs-lookup"><span data-stu-id="5aa56-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-500">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-500">CC004</span></span></td>
<td><span data-ttu-id="5aa56-501">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-501">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-502">35</span><span class="sxs-lookup"><span data-stu-id="5aa56-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-503">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="5aa56-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5aa56-504">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-505">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-505">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-506">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="5aa56-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-507">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-507">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-508">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-509">60</span><span class="sxs-lookup"><span data-stu-id="5aa56-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-510">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-510">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-511">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-512">20</span><span class="sxs-lookup"><span data-stu-id="5aa56-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-513">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="5aa56-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5aa56-514">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-515">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-515">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-516">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="5aa56-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-517">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-517">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-518">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-519">80</span><span class="sxs-lookup"><span data-stu-id="5aa56-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-520">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-520">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-521">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-522">15</span><span class="sxs-lookup"><span data-stu-id="5aa56-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-523">**Hinweis:** In Finance and Operations können statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5aa56-524">Ausführliche Informationen zur Anzeige statistischer Kennzahlanbieter, finden Sie in der Anbietervorlage statistischen Kennzahl.</span><span class="sxs-lookup"><span data-stu-id="5aa56-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="5aa56-525">(Hinweis, dieses Thema ist nicht abgeschlossen, aber bald verfügbar) Die folgende Tabelle zeigt das Ergebnis an, wenn der HR-Service als Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten angewendet würde (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="5aa56-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-526">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-526">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-527">Größe</span><span class="sxs-lookup"><span data-stu-id="5aa56-527">Magnitude</span></span></th>
<th><span data-ttu-id="5aa56-528">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5aa56-528">Allocation factor</span></span></th>
<th><span data-ttu-id="5aa56-529">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-529">Amount</span></span></th>
<th><span data-ttu-id="5aa56-530">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-531">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-531">CC002</span></span></td>
<td><span data-ttu-id="5aa56-532">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-532">Finance</span></span></td>
<td><span data-ttu-id="5aa56-533">35</span><span class="sxs-lookup"><span data-stu-id="5aa56-533">35</span></span></td>
<td><span data-ttu-id="5aa56-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5aa56-535">175.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-535">175.00</span></span></td>
<td><span data-ttu-id="5aa56-536">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-537">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-537">CC003</span></span></td>
<td><span data-ttu-id="5aa56-538">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-538">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-539">55</span><span class="sxs-lookup"><span data-stu-id="5aa56-539">55</span></span></td>
<td><span data-ttu-id="5aa56-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5aa56-541">275.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-541">275.00</span></span></td>
<td><span data-ttu-id="5aa56-542">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-543">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-543">CC004</span></span></td>
<td><span data-ttu-id="5aa56-544">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-544">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-545">10</span><span class="sxs-lookup"><span data-stu-id="5aa56-545">10</span></span></td>
<td><span data-ttu-id="5aa56-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5aa56-547">50,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-547">50.00</span></span></td>
<td><span data-ttu-id="5aa56-548">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-549">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-549">CC002</span></span></td>
<td><span data-ttu-id="5aa56-550">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-550">Finance</span></span></td>
<td><span data-ttu-id="5aa56-551">35</span><span class="sxs-lookup"><span data-stu-id="5aa56-551">35</span></span></td>
<td><span data-ttu-id="5aa56-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5aa56-553">436.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-553">436.00</span></span></td>
<td><span data-ttu-id="5aa56-554">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-555">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-555">CC003</span></span></td>
<td><span data-ttu-id="5aa56-556">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-556">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-557">55</span><span class="sxs-lookup"><span data-stu-id="5aa56-557">55</span></span></td>
<td><span data-ttu-id="5aa56-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5aa56-559">685.14</span><span class="sxs-lookup"><span data-stu-id="5aa56-559">685.14</span></span></td>
<td><span data-ttu-id="5aa56-560">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-561">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-561">CC004</span></span></td>
<td><span data-ttu-id="5aa56-562">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-562">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-563">10</span><span class="sxs-lookup"><span data-stu-id="5aa56-563">10</span></span></td>
<td><span data-ttu-id="5aa56-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5aa56-565">124.57</span><span class="sxs-lookup"><span data-stu-id="5aa56-565">124.57</span></span></td>
<td><span data-ttu-id="5aa56-566">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-567">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="5aa56-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-568">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-568">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-569">Größe</span><span class="sxs-lookup"><span data-stu-id="5aa56-569">Magnitude</span></span></th>
<th><span data-ttu-id="5aa56-570">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5aa56-570">Allocation factor</span></span></th>
<th><span data-ttu-id="5aa56-571">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-571">Amount</span></span></th>
<th><span data-ttu-id="5aa56-572">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-573">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-573">CC003</span></span></td>
<td><span data-ttu-id="5aa56-574">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-574">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-575">65</span><span class="sxs-lookup"><span data-stu-id="5aa56-575">65</span></span></td>
<td><span data-ttu-id="5aa56-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="5aa56-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5aa56-577">438.75</span><span class="sxs-lookup"><span data-stu-id="5aa56-577">438.75</span></span></td>
<td><span data-ttu-id="5aa56-578">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-579">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-579">CC004</span></span></td>
<td><span data-ttu-id="5aa56-580">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-580">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-581">35</span><span class="sxs-lookup"><span data-stu-id="5aa56-581">35</span></span></td>
<td><span data-ttu-id="5aa56-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="5aa56-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5aa56-583">236.25</span><span class="sxs-lookup"><span data-stu-id="5aa56-583">236.25</span></span></td>
<td><span data-ttu-id="5aa56-584">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-585">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-585">CC003</span></span></td>
<td><span data-ttu-id="5aa56-586">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-586">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-587">65</span><span class="sxs-lookup"><span data-stu-id="5aa56-587">65</span></span></td>
<td><span data-ttu-id="5aa56-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="5aa56-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5aa56-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5aa56-589">5,297.69</span></span></td>
<td><span data-ttu-id="5aa56-590">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-591">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-591">CC004</span></span></td>
<td><span data-ttu-id="5aa56-592">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-592">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-593">35</span><span class="sxs-lookup"><span data-stu-id="5aa56-593">35</span></span></td>
<td><span data-ttu-id="5aa56-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="5aa56-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5aa56-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5aa56-595">2,852.60</span></span></td>
<td><span data-ttu-id="5aa56-596">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-597">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="5aa56-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-598">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-598">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-599">Größe</span><span class="sxs-lookup"><span data-stu-id="5aa56-599">Magnitude</span></span></th>
<th><span data-ttu-id="5aa56-600">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5aa56-600">Allocation factor</span></span></th>
<th><span data-ttu-id="5aa56-601">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-601">Amount</span></span></th>
<th><span data-ttu-id="5aa56-602">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-603">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-603">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-604">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-605">60</span><span class="sxs-lookup"><span data-stu-id="5aa56-605">60</span></span></td>
<td><span data-ttu-id="5aa56-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="5aa56-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5aa56-607">535.31</span><span class="sxs-lookup"><span data-stu-id="5aa56-607">535.31</span></span></td>
<td><span data-ttu-id="5aa56-608">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-609">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-609">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-610">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-611">20</span><span class="sxs-lookup"><span data-stu-id="5aa56-611">20</span></span></td>
<td><span data-ttu-id="5aa56-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="5aa56-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5aa56-613">178.44</span><span class="sxs-lookup"><span data-stu-id="5aa56-613">178.44</span></span></td>
<td><span data-ttu-id="5aa56-614">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-615">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-615">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-616">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-617">60</span><span class="sxs-lookup"><span data-stu-id="5aa56-617">60</span></span></td>
<td><span data-ttu-id="5aa56-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="5aa56-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5aa56-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5aa56-619">4,487.12</span></span></td>
<td><span data-ttu-id="5aa56-620">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-621">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-621">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-622">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-623">20</span><span class="sxs-lookup"><span data-stu-id="5aa56-623">20</span></span></td>
<td><span data-ttu-id="5aa56-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="5aa56-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5aa56-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-625">1,495.71</span></span></td>
<td><span data-ttu-id="5aa56-626">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5aa56-627">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="5aa56-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-628">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-628">Cost object</span></span></th>
<th><span data-ttu-id="5aa56-629">Größe</span><span class="sxs-lookup"><span data-stu-id="5aa56-629">Magnitude</span></span></th>
<th><span data-ttu-id="5aa56-630">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5aa56-630">Allocation factor</span></span></th>
<th><span data-ttu-id="5aa56-631">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-631">Amount</span></span></th>
<th><span data-ttu-id="5aa56-632">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-633">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-633">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-634">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-635">80</span><span class="sxs-lookup"><span data-stu-id="5aa56-635">80</span></span></td>
<td><span data-ttu-id="5aa56-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="5aa56-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5aa56-637">241.05</span><span class="sxs-lookup"><span data-stu-id="5aa56-637">241.05</span></span></td>
<td><span data-ttu-id="5aa56-638">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-639">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-639">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-640">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-641">15</span><span class="sxs-lookup"><span data-stu-id="5aa56-641">15</span></span></td>
<td><span data-ttu-id="5aa56-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="5aa56-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5aa56-643">45.20</span><span class="sxs-lookup"><span data-stu-id="5aa56-643">45.20</span></span></td>
<td><span data-ttu-id="5aa56-644">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-645">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-645">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-646">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-647">80</span><span class="sxs-lookup"><span data-stu-id="5aa56-647">80</span></span></td>
<td><span data-ttu-id="5aa56-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="5aa56-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5aa56-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5aa56-649">2,507.09</span></span></td>
<td><span data-ttu-id="5aa56-650">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-651">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-651">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-652">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-653">15</span><span class="sxs-lookup"><span data-stu-id="5aa56-653">15</span></span></td>
<td><span data-ttu-id="5aa56-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="5aa56-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5aa56-655">470.08</span><span class="sxs-lookup"><span data-stu-id="5aa56-655">470.08</span></span></td>
<td><span data-ttu-id="5aa56-656">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5aa56-657">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="5aa56-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-658">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5aa56-658">Journal</span></span></th>
<th><span data-ttu-id="5aa56-659">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="5aa56-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5aa56-660">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5aa56-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5aa56-661">Version</span><span class="sxs-lookup"><span data-stu-id="5aa56-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-662">00004</span><span class="sxs-lookup"><span data-stu-id="5aa56-662">00004</span></span></td>
<td><span data-ttu-id="5aa56-663">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="5aa56-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5aa56-664">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5aa56-664">Fiscal</span></span></td>
<td><span data-ttu-id="5aa56-665">2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-665">2017</span></span></td>
<td><span data-ttu-id="5aa56-666">Periode 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-666">Period 1</span></span></td>
<td><span data-ttu-id="5aa56-667">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5aa56-668">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="5aa56-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5aa56-669">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-670">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-671">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-671">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-672">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-672">Cost behavior</span></span></th>
<th><span data-ttu-id="5aa56-673">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-674">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-675">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-675">CC001</span></span></td>
<td><span data-ttu-id="5aa56-676">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-676">HR</span></span></td>
<td><span data-ttu-id="5aa56-677">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-677">10001</span></span></td>
<td><span data-ttu-id="5aa56-678">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-678">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-679">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-679">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-680">500,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-681">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-682">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-682">CC001</span></span></td>
<td><span data-ttu-id="5aa56-683">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-683">HR</span></span></td>
<td><span data-ttu-id="5aa56-684">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-684">10001</span></span></td>
<td><span data-ttu-id="5aa56-685">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-685">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-686">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-686">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-688">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-689">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-689">CC002</span></span></td>
<td><span data-ttu-id="5aa56-690">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-690">Finance</span></span></td>
<td><span data-ttu-id="5aa56-691">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-691">10001</span></span></td>
<td><span data-ttu-id="5aa56-692">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-692">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-693">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-693">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-694">675.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-695">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-696">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-696">CC002</span></span></td>
<td><span data-ttu-id="5aa56-697">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-697">Finance</span></span></td>
<td><span data-ttu-id="5aa56-698">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-698">10001</span></span></td>
<td><span data-ttu-id="5aa56-699">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-699">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-700">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-700">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5aa56-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-702">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-703">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-703">CC003</span></span></td>
<td><span data-ttu-id="5aa56-704">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-704">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-705">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-705">10001</span></span></td>
<td><span data-ttu-id="5aa56-706">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-706">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-707">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-707">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-708">713.75</span><span class="sxs-lookup"><span data-stu-id="5aa56-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-709">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-710">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-710">CC003</span></span></td>
<td><span data-ttu-id="5aa56-711">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-711">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-712">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-712">10001</span></span></td>
<td><span data-ttu-id="5aa56-713">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-713">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-714">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-714">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5aa56-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-716">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-717">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-717">CC003</span></span></td>
<td><span data-ttu-id="5aa56-718">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-718">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-719">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-719">10001</span></span></td>
<td><span data-ttu-id="5aa56-720">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-720">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-721">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-721">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-722">286.25</span><span class="sxs-lookup"><span data-stu-id="5aa56-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-723">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-724">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-724">CC003</span></span></td>
<td><span data-ttu-id="5aa56-725">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-725">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-726">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-726">10001</span></span></td>
<td><span data-ttu-id="5aa56-727">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-727">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-728">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-728">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5aa56-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-730">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-731">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-731">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-732">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-733">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-733">10001</span></span></td>
<td><span data-ttu-id="5aa56-734">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-734">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-735">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-735">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-736">776.36</span><span class="sxs-lookup"><span data-stu-id="5aa56-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-737">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-738">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-738">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-739">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-740">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-740">10001</span></span></td>
<td><span data-ttu-id="5aa56-741">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-741">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-742">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-742">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5aa56-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-744">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-745">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-745">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-746">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-747">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-747">10001</span></span></td>
<td><span data-ttu-id="5aa56-748">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-748">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-749">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-749">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-750">223.64</span><span class="sxs-lookup"><span data-stu-id="5aa56-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-751">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="5aa56-752">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-752">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-753">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-754">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-754">10001</span></span></td>
<td><span data-ttu-id="5aa56-755">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-755">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-756">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-756">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5aa56-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5aa56-758">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="5aa56-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5aa56-759">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5aa56-760">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-760">Cost element</span></span></th>
<th><span data-ttu-id="5aa56-761">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5aa56-761">Cost behavior</span></span></th>
<th><span data-ttu-id="5aa56-762">Betrag</span><span class="sxs-lookup"><span data-stu-id="5aa56-762">Amount</span></span></th>
<th><span data-ttu-id="5aa56-763">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5aa56-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5aa56-764">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-764">CC001</span></span></td>
<td><span data-ttu-id="5aa56-765">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-765">HR</span></span></td>
<td><span data-ttu-id="5aa56-766">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-766">10001</span></span></td>
<td><span data-ttu-id="5aa56-767">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-767">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-768">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-768">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-769">-500.00</span></span></td>
<td><span data-ttu-id="5aa56-770">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-771">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-771">CC002</span></span></td>
<td><span data-ttu-id="5aa56-772">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-772">Finance</span></span></td>
<td><span data-ttu-id="5aa56-773">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-773">10001</span></span></td>
<td><span data-ttu-id="5aa56-774">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-774">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-775">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-775">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-776">175.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-776">175.00</span></span></td>
<td><span data-ttu-id="5aa56-777">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-778">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-778">CC003</span></span></td>
<td><span data-ttu-id="5aa56-779">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-779">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-780">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-780">10001</span></span></td>
<td><span data-ttu-id="5aa56-781">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-781">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-782">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-782">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-783">275.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-783">275.00</span></span></td>
<td><span data-ttu-id="5aa56-784">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-785">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-785">CC004</span></span></td>
<td><span data-ttu-id="5aa56-786">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-786">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-787">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-787">10001</span></span></td>
<td><span data-ttu-id="5aa56-788">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-788">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-789">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-789">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-790">50,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-790">50,00</span></span></td>
<td><span data-ttu-id="5aa56-791">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-792">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-792">CC001</span></span></td>
<td><span data-ttu-id="5aa56-793">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5aa56-793">HR</span></span></td>
<td><span data-ttu-id="5aa56-794">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-794">10001</span></span></td>
<td><span data-ttu-id="5aa56-795">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-795">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-796">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-796">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-797">-1,245.71</span></span></td>
<td><span data-ttu-id="5aa56-798">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-799">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-799">CC002</span></span></td>
<td><span data-ttu-id="5aa56-800">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-800">Finance</span></span></td>
<td><span data-ttu-id="5aa56-801">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-801">10001</span></span></td>
<td><span data-ttu-id="5aa56-802">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-802">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-803">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-803">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-804">436.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-804">436.00</span></span></td>
<td><span data-ttu-id="5aa56-805">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-806">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-806">CC003</span></span></td>
<td><span data-ttu-id="5aa56-807">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-807">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-808">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-808">10001</span></span></td>
<td><span data-ttu-id="5aa56-809">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-809">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-810">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-810">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-811">685.14</span><span class="sxs-lookup"><span data-stu-id="5aa56-811">685.14</span></span></td>
<td><span data-ttu-id="5aa56-812">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-813">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-813">CC004</span></span></td>
<td><span data-ttu-id="5aa56-814">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-814">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-815">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-815">10001</span></span></td>
<td><span data-ttu-id="5aa56-816">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-816">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-817">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-817">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-818">124.57</span><span class="sxs-lookup"><span data-stu-id="5aa56-818">124.57</span></span></td>
<td><span data-ttu-id="5aa56-819">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-820">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-820">CC002</span></span></td>
<td><span data-ttu-id="5aa56-821">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-821">Finance</span></span></td>
<td><span data-ttu-id="5aa56-822">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-822">10001</span></span></td>
<td><span data-ttu-id="5aa56-823">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-823">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-824">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-824">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="5aa56-825">-675.00</span></span></td>
<td><span data-ttu-id="5aa56-826">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-827">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-827">CC003</span></span></td>
<td><span data-ttu-id="5aa56-828">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-828">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-829">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-829">10001</span></span></td>
<td><span data-ttu-id="5aa56-830">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-830">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-831">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-831">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-832">438.75</span><span class="sxs-lookup"><span data-stu-id="5aa56-832">438.75</span></span></td>
<td><span data-ttu-id="5aa56-833">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-834">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-834">CC004</span></span></td>
<td><span data-ttu-id="5aa56-835">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-835">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-836">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-836">10001</span></span></td>
<td><span data-ttu-id="5aa56-837">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-837">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-838">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-838">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-839">236.25</span><span class="sxs-lookup"><span data-stu-id="5aa56-839">236.25</span></span></td>
<td><span data-ttu-id="5aa56-840">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-841">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-841">CC002</span></span></td>
<td><span data-ttu-id="5aa56-842">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5aa56-842">Finance</span></span></td>
<td><span data-ttu-id="5aa56-843">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-843">10001</span></span></td>
<td><span data-ttu-id="5aa56-844">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-844">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-845">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-845">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="5aa56-846">-8,150.29</span></span></td>
<td><span data-ttu-id="5aa56-847">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-848">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-848">CC003</span></span></td>
<td><span data-ttu-id="5aa56-849">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-849">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-850">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-850">10001</span></span></td>
<td><span data-ttu-id="5aa56-851">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-851">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-852">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-852">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5aa56-853">5,297.69</span></span></td>
<td><span data-ttu-id="5aa56-854">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-855">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-855">CC004</span></span></td>
<td><span data-ttu-id="5aa56-856">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5aa56-856">Packaging</span></span></td>
<td><span data-ttu-id="5aa56-857">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-857">10001</span></span></td>
<td><span data-ttu-id="5aa56-858">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-858">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-859">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-859">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5aa56-860">2,852.60</span></span></td>
<td><span data-ttu-id="5aa56-861">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-862">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-862">CC003</span></span></td>
<td><span data-ttu-id="5aa56-863">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-863">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-864">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-864">10001</span></span></td>
<td><span data-ttu-id="5aa56-865">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-865">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-866">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-866">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="5aa56-867">-713.75</span></span></td>
<td><span data-ttu-id="5aa56-868">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-869">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-869">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-870">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-871">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-871">10001</span></span></td>
<td><span data-ttu-id="5aa56-872">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-872">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-873">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-873">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-874">535.31</span><span class="sxs-lookup"><span data-stu-id="5aa56-874">535.31</span></span></td>
<td><span data-ttu-id="5aa56-875">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-876">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-876">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-877">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-878">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-878">10001</span></span></td>
<td><span data-ttu-id="5aa56-879">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-879">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-880">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-880">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-881">178.44</span><span class="sxs-lookup"><span data-stu-id="5aa56-881">178.44</span></span></td>
<td><span data-ttu-id="5aa56-882">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-883">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-883">CC003</span></span></td>
<td><span data-ttu-id="5aa56-884">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-884">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-885">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-885">10001</span></span></td>
<td><span data-ttu-id="5aa56-886">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-886">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-887">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-887">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="5aa56-888">-5,982.83</span></span></td>
<td><span data-ttu-id="5aa56-889">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-890">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-890">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-891">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-892">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-892">10001</span></span></td>
<td><span data-ttu-id="5aa56-893">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-893">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-894">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-894">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5aa56-895">4,487.12</span></span></td>
<td><span data-ttu-id="5aa56-896">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-897">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-897">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-898">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-899">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-899">10001</span></span></td>
<td><span data-ttu-id="5aa56-900">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-900">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-901">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-901">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5aa56-902">1,495.71</span></span></td>
<td><span data-ttu-id="5aa56-903">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-904">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-904">CC003</span></span></td>
<td><span data-ttu-id="5aa56-905">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-905">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-906">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-906">10001</span></span></td>
<td><span data-ttu-id="5aa56-907">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-907">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-908">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-908">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="5aa56-909">-286.25</span></span></td>
<td><span data-ttu-id="5aa56-910">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-911">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-911">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-912">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-913">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-913">10001</span></span></td>
<td><span data-ttu-id="5aa56-914">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-914">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-915">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-915">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-916">241.05</span><span class="sxs-lookup"><span data-stu-id="5aa56-916">241.05</span></span></td>
<td><span data-ttu-id="5aa56-917">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-918">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-918">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-919">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-920">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-920">10001</span></span></td>
<td><span data-ttu-id="5aa56-921">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-921">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-922">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-922">Fixed cost</span></span></td>
<td><span data-ttu-id="5aa56-923">45.20</span><span class="sxs-lookup"><span data-stu-id="5aa56-923">45.20</span></span></td>
<td><span data-ttu-id="5aa56-924">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-925">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-925">CC003</span></span></td>
<td><span data-ttu-id="5aa56-926">Montage</span><span class="sxs-lookup"><span data-stu-id="5aa56-926">Assembly</span></span></td>
<td><span data-ttu-id="5aa56-927">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-927">10001</span></span></td>
<td><span data-ttu-id="5aa56-928">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-928">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-929">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-929">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="5aa56-930">-2,977.17</span></span></td>
<td><span data-ttu-id="5aa56-931">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-932">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-932">Prod 1</span></span></td>
<td><span data-ttu-id="5aa56-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-933">Product 1</span></span></td>
<td><span data-ttu-id="5aa56-934">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-934">10001</span></span></td>
<td><span data-ttu-id="5aa56-935">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-935">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-936">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-936">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5aa56-937">2,507.09</span></span></td>
<td><span data-ttu-id="5aa56-938">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5aa56-939">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-939">Prod 2</span></span></td>
<td><span data-ttu-id="5aa56-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-940">Product 2</span></span></td>
<td><span data-ttu-id="5aa56-941">10001</span><span class="sxs-lookup"><span data-stu-id="5aa56-941">10001</span></span></td>
<td><span data-ttu-id="5aa56-942">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-942">Electricity</span></span></td>
<td><span data-ttu-id="5aa56-943">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-943">Variable cost</span></span></td>
<td><span data-ttu-id="5aa56-944">470.08</span><span class="sxs-lookup"><span data-stu-id="5aa56-944">470.08</span></span></td>
<td><span data-ttu-id="5aa56-945">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5aa56-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5aa56-946">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="5aa56-946">Conclusion</span></span>
<span data-ttu-id="5aa56-947">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5aa56-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5aa56-948">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5aa56-949">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5aa56-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5aa56-950">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5aa56-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5aa56-951">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5aa56-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5aa56-952">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5aa56-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5aa56-953">Gesamt</span><span class="sxs-lookup"><span data-stu-id="5aa56-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5aa56-954">CC099</span><span class="sxs-lookup"><span data-stu-id="5aa56-954">CC099</span></span></th>
<th><span data-ttu-id="5aa56-955">CC001</span><span class="sxs-lookup"><span data-stu-id="5aa56-955">CC001</span></span></th>
<th><span data-ttu-id="5aa56-956">CC002</span><span class="sxs-lookup"><span data-stu-id="5aa56-956">CC002</span></span></th>
<th><span data-ttu-id="5aa56-957">CC003</span><span class="sxs-lookup"><span data-stu-id="5aa56-957">CC003</span></span></th>
<th><span data-ttu-id="5aa56-958">CC004</span><span class="sxs-lookup"><span data-stu-id="5aa56-958">CC004</span></span></th>
<th><span data-ttu-id="5aa56-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-959">Proj 1</span></span></th>
<th><span data-ttu-id="5aa56-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-960">Proj 2</span></span></th>
<th><span data-ttu-id="5aa56-961">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5aa56-961">Prod 1</span></span></th>
<th><span data-ttu-id="5aa56-962">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5aa56-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5aa56-963">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5aa56-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5aa56-973">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="5aa56-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-974">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5aa56-975">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-976">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-977">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-978">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-979">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-980">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-981">776.36</span><span class="sxs-lookup"><span data-stu-id="5aa56-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-982">223.64</span><span class="sxs-lookup"><span data-stu-id="5aa56-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5aa56-984">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5aa56-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-985">000</span><span class="sxs-lookup"><span data-stu-id="5aa56-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-986">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-987">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-988">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-989">0,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-990">30,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-991">10,00</span><span class="sxs-lookup"><span data-stu-id="5aa56-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5aa56-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5aa56-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5aa56-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5aa56-995">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="5aa56-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5aa56-996">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5aa56-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5aa56-997">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="5aa56-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5aa56-998">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="5aa56-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5aa56-999">Für ausführlichere Informationen gehen Sie zur Richtlinie Kostenzusammenfassung.</span><span class="sxs-lookup"><span data-stu-id="5aa56-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="5aa56-1000">(Beachten Sie, dass dieses Thema noch nicht abgedeckt ist, aber bald verfügbar sein wird.)</span><span class="sxs-lookup"><span data-stu-id="5aa56-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




