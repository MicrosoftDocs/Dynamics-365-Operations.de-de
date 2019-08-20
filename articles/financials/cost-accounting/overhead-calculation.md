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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841488"
---
# <a name="overhead-calculation"></a><span data-ttu-id="8fd3b-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fd3b-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="8fd3b-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="8fd3b-105">Term definition</span></span>
---------------

<span data-ttu-id="8fd3b-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="8fd3b-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="8fd3b-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="8fd3b-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="8fd3b-109">Miete</span><span class="sxs-lookup"><span data-stu-id="8fd3b-109">Rent</span></span>
-   <span data-ttu-id="8fd3b-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-110">Electricity</span></span>
-   <span data-ttu-id="8fd3b-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="8fd3b-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="8fd3b-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="8fd3b-112">Overhead calculation overview</span></span>
<span data-ttu-id="8fd3b-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="8fd3b-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="8fd3b-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="8fd3b-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="8fd3b-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="8fd3b-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="8fd3b-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="8fd3b-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="8fd3b-119">Version type</span></span>
-   <span data-ttu-id="8fd3b-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="8fd3b-120">Date and time</span></span>
-   <span data-ttu-id="8fd3b-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="8fd3b-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="8fd3b-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="8fd3b-122">Fiscal year</span></span>
-   <span data-ttu-id="8fd3b-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="8fd3b-123">Fiscal period</span></span>

<span data-ttu-id="8fd3b-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="8fd3b-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="8fd3b-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="8fd3b-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="8fd3b-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="8fd3b-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="8fd3b-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="8fd3b-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="8fd3b-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="8fd3b-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="8fd3b-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="8fd3b-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="8fd3b-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="8fd3b-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="8fd3b-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="8fd3b-140">Main account</span></span></th>
<th><span data-ttu-id="8fd3b-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-143">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-143">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-144">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-145">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-145">10001</span></span></td>
<td><span data-ttu-id="8fd3b-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-146">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="8fd3b-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="8fd3b-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="8fd3b-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="8fd3b-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="8fd3b-151">Define the cost behavior rule</span></span>

<span data-ttu-id="8fd3b-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="8fd3b-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="8fd3b-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="8fd3b-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="8fd3b-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="8fd3b-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="8fd3b-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="8fd3b-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="8fd3b-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="8fd3b-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="8fd3b-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-160">Journal</span></span></th>
<th><span data-ttu-id="8fd3b-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="8fd3b-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8fd3b-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="8fd3b-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8fd3b-163">Version</span><span class="sxs-lookup"><span data-stu-id="8fd3b-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-164">00001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-164">00001</span></span></td>
<td><span data-ttu-id="8fd3b-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="8fd3b-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="8fd3b-166">Fiscal</span></span></td>
<td><span data-ttu-id="8fd3b-167">2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-167">2017</span></span></td>
<td><span data-ttu-id="8fd3b-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-168">Period 1</span></span></td>
<td><span data-ttu-id="8fd3b-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8fd3b-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-173">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-174">Cost behavior</span></span></th>
<th><span data-ttu-id="8fd3b-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-177">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-177">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-178">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-179">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-179">10001</span></span></td>
<td><span data-ttu-id="8fd3b-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-180">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="8fd3b-181">Unclassified</span></span></td>
<td><span data-ttu-id="8fd3b-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8fd3b-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="8fd3b-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-185">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-186">Cost behavior</span></span></th>
<th><span data-ttu-id="8fd3b-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-187">Amount</span></span></th>
<th><span data-ttu-id="8fd3b-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-189">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-189">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-190">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-191">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-191">10001</span></span></td>
<td><span data-ttu-id="8fd3b-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-192">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="8fd3b-193">Unclassified</span></span></td>
<td><span data-ttu-id="8fd3b-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-194">10,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-196">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-196">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-197">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-198">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-198">10001</span></span></td>
<td><span data-ttu-id="8fd3b-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-199">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="8fd3b-200">Unclassified</span></span></td>
<td><span data-ttu-id="8fd3b-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-201">-10,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-203">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-203">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-204">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-205">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-205">10001</span></span></td>
<td><span data-ttu-id="8fd3b-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-206">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-207">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-208">1,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-210">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-210">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-211">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-212">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-212">10001</span></span></td>
<td><span data-ttu-id="8fd3b-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-213">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-214">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-215">9,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="8fd3b-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="8fd3b-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="8fd3b-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="8fd3b-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="8fd3b-221">Define the cost distribution rule</span></span>

<span data-ttu-id="8fd3b-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="8fd3b-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="8fd3b-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="8fd3b-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="8fd3b-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="8fd3b-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-228">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-229">KWH</span><span class="sxs-lookup"><span data-stu-id="8fd3b-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-230">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-230">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-231">HR</span></span></td>
<td><span data-ttu-id="8fd3b-232">1.000</span><span class="sxs-lookup"><span data-stu-id="8fd3b-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-233">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-233">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-234">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-235">6.000</span><span class="sxs-lookup"><span data-stu-id="8fd3b-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-236">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-236">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-237">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-237">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-238">0</span><span class="sxs-lookup"><span data-stu-id="8fd3b-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-240">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-241">Größe</span><span class="sxs-lookup"><span data-stu-id="8fd3b-241">Magnitude</span></span></th>
<th><span data-ttu-id="8fd3b-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="8fd3b-242">Allocation factor</span></span></th>
<th><span data-ttu-id="8fd3b-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-244">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-244">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-245">HR</span></span></td>
<td><span data-ttu-id="8fd3b-246">1.000</span><span class="sxs-lookup"><span data-stu-id="8fd3b-246">1,000</span></span></td>
<td><span data-ttu-id="8fd3b-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-249">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-249">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-250">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-251">6.000</span><span class="sxs-lookup"><span data-stu-id="8fd3b-251">6,000</span></span></td>
<td><span data-ttu-id="8fd3b-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8fd3b-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-254">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-254">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-255">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-255">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-256">0</span><span class="sxs-lookup"><span data-stu-id="8fd3b-256">0</span></span></td>
<td><span data-ttu-id="8fd3b-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-258">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="8fd3b-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-261">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-262">Formula</span></span></th>
<th><span data-ttu-id="8fd3b-263">Größe</span><span class="sxs-lookup"><span data-stu-id="8fd3b-263">Magnitude</span></span></th>
<th><span data-ttu-id="8fd3b-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="8fd3b-264">Allocation factor</span></span></th>
<th><span data-ttu-id="8fd3b-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-266">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-266">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-267">HR</span></span></td>
<td><span data-ttu-id="8fd3b-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8fd3b-269">1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-269">1</span></span></td>
<td><span data-ttu-id="8fd3b-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-271">500,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-272">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-272">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-273">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8fd3b-275">1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-275">1</span></span></td>
<td><span data-ttu-id="8fd3b-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-277">500,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-278">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-278">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-279">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-279">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8fd3b-281">0</span><span class="sxs-lookup"><span data-stu-id="8fd3b-281">0</span></span></td>
<td><span data-ttu-id="8fd3b-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-283">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8fd3b-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-285">Journal</span></span></th>
<th><span data-ttu-id="8fd3b-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="8fd3b-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8fd3b-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="8fd3b-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8fd3b-288">Version</span><span class="sxs-lookup"><span data-stu-id="8fd3b-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-289">00002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-289">00002</span></span></td>
<td><span data-ttu-id="8fd3b-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="8fd3b-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="8fd3b-291">Fiscal</span></span></td>
<td><span data-ttu-id="8fd3b-292">2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-292">2017</span></span></td>
<td><span data-ttu-id="8fd3b-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-293">Period 1</span></span></td>
<td><span data-ttu-id="8fd3b-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8fd3b-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-298">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-299">Cost behavior</span></span></th>
<th><span data-ttu-id="8fd3b-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-302">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-302">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-303">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-304">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-304">10001</span></span></td>
<td><span data-ttu-id="8fd3b-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-305">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-306">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-309">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-309">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-310">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-311">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-311">10001</span></span></td>
<td><span data-ttu-id="8fd3b-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-312">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-313">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8fd3b-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="8fd3b-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-317">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-318">Cost behavior</span></span></th>
<th><span data-ttu-id="8fd3b-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-319">Amount</span></span></th>
<th><span data-ttu-id="8fd3b-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-321">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-321">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-322">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-323">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-323">10001</span></span></td>
<td><span data-ttu-id="8fd3b-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-324">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-325">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-326">-1,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-328">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-328">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-329">HR</span></span></td>
<td><span data-ttu-id="8fd3b-330">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-330">10001</span></span></td>
<td><span data-ttu-id="8fd3b-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-331">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-332">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-333">500,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-333">500.00</span></span></td>
<td><span data-ttu-id="8fd3b-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-335">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-335">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-336">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-337">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-337">10001</span></span></td>
<td><span data-ttu-id="8fd3b-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-338">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-339">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-340">500,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-340">500.00</span></span></td>
<td><span data-ttu-id="8fd3b-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-342">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-342">CC099</span></span></td>
<td><span data-ttu-id="8fd3b-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="8fd3b-343">Default cost center</span></span></td>
<td><span data-ttu-id="8fd3b-344">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-344">10001</span></span></td>
<td><span data-ttu-id="8fd3b-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-345">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-346">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-347">-9,000.00</span></span></td>
<td><span data-ttu-id="8fd3b-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-349">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-349">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-350">HR</span></span></td>
<td><span data-ttu-id="8fd3b-351">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-351">10001</span></span></td>
<td><span data-ttu-id="8fd3b-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-352">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-353">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-354">1,285.71</span></span></td>
<td><span data-ttu-id="8fd3b-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-356">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-356">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-357">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-358">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-358">10001</span></span></td>
<td><span data-ttu-id="8fd3b-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-359">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-360">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8fd3b-361">7,714.29</span></span></td>
<td><span data-ttu-id="8fd3b-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="8fd3b-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="8fd3b-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="8fd3b-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="8fd3b-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="8fd3b-367">Define the overhead rate</span></span>

<span data-ttu-id="8fd3b-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="8fd3b-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-370">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="8fd3b-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-372">Proj 1</span></span></td>
<td><span data-ttu-id="8fd3b-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-373">Project 1</span></span></td>
<td><span data-ttu-id="8fd3b-374">3</span><span class="sxs-lookup"><span data-stu-id="8fd3b-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-375">Proj 2</span></span></td>
<td><span data-ttu-id="8fd3b-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-376">Project 2</span></span></td>
<td><span data-ttu-id="8fd3b-377">1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-379">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-380">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-381">Cost behavior</span></span></th>
<th><span data-ttu-id="8fd3b-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-382">Units</span></span></th>
<th><span data-ttu-id="8fd3b-383">Satz</span><span class="sxs-lookup"><span data-stu-id="8fd3b-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-384">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-384">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-385">HR</span></span></td>
<td><span data-ttu-id="8fd3b-386">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-386">10001</span></span></td>
<td><span data-ttu-id="8fd3b-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-387">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-388">1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-388">1</span></span></td>
<td><span data-ttu-id="8fd3b-389">10</span><span class="sxs-lookup"><span data-stu-id="8fd3b-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-391">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-392">Größe</span><span class="sxs-lookup"><span data-stu-id="8fd3b-392">Magnitude</span></span></th>
<th><span data-ttu-id="8fd3b-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-393">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="8fd3b-394">Allocation factor</span></span></th>
<th><span data-ttu-id="8fd3b-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-396">Proj 1</span></span></td>
<td><span data-ttu-id="8fd3b-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-397">Project 1</span></span></td>
<td><span data-ttu-id="8fd3b-398">3</span><span class="sxs-lookup"><span data-stu-id="8fd3b-398">3</span></span></td>
<td><span data-ttu-id="8fd3b-399">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-399">10001</span></span></td>
<td><span data-ttu-id="8fd3b-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8fd3b-401">30,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-402">Proj 2</span></span></td>
<td><span data-ttu-id="8fd3b-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-403">Project 2</span></span></td>
<td><span data-ttu-id="8fd3b-404">1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-404">1</span></span></td>
<td><span data-ttu-id="8fd3b-405">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-405">10001</span></span></td>
<td><span data-ttu-id="8fd3b-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8fd3b-407">10,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8fd3b-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-409">Journal</span></span></th>
<th><span data-ttu-id="8fd3b-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="8fd3b-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8fd3b-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="8fd3b-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8fd3b-412">Version</span><span class="sxs-lookup"><span data-stu-id="8fd3b-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-413">00003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-413">00003</span></span></td>
<td><span data-ttu-id="8fd3b-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="8fd3b-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="8fd3b-415">Fiscal</span></span></td>
<td><span data-ttu-id="8fd3b-416">2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-416">2017</span></span></td>
<td><span data-ttu-id="8fd3b-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-417">Period 1</span></span></td>
<td><span data-ttu-id="8fd3b-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="8fd3b-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-421">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-422">Größe</span><span class="sxs-lookup"><span data-stu-id="8fd3b-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-424">Proj 1</span></span></td>
<td><span data-ttu-id="8fd3b-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8fd3b-426">3,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-428">Proj 2</span></span></td>
<td><span data-ttu-id="8fd3b-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8fd3b-430">1,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8fd3b-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="8fd3b-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-433">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-434">Cost behavior</span></span></th>
<th><span data-ttu-id="8fd3b-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-435">Amount</span></span></th>
<th><span data-ttu-id="8fd3b-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-437">CC0001</span></span></td>
<td><span data-ttu-id="8fd3b-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-438">HR</span></span></td>
<td><span data-ttu-id="8fd3b-439">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-439">10001</span></span></td>
<td><span data-ttu-id="8fd3b-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-440">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-441">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-442">-30.00</span></span></td>
<td><span data-ttu-id="8fd3b-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-444">Proj 1</span></span></td>
<td><span data-ttu-id="8fd3b-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8fd3b-446">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-446">10001</span></span></td>
<td><span data-ttu-id="8fd3b-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-447">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-448">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-449">30,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-449">30.00</span></span></td>
<td><span data-ttu-id="8fd3b-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-451">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-451">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-452">HR</span></span></td>
<td><span data-ttu-id="8fd3b-453">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-453">10001</span></span></td>
<td><span data-ttu-id="8fd3b-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-454">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-455">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-456">-10.00</span></span></td>
<td><span data-ttu-id="8fd3b-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-458">Proj 2</span></span></td>
<td><span data-ttu-id="8fd3b-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8fd3b-460">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-460">10001</span></span></td>
<td><span data-ttu-id="8fd3b-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-461">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-462">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-463">10.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-463">10.00</span></span></td>
<td><span data-ttu-id="8fd3b-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="8fd3b-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="8fd3b-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="8fd3b-468">Finance and Operations unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="8fd3b-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="8fd3b-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="8fd3b-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="8fd3b-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="8fd3b-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="8fd3b-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="8fd3b-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="8fd3b-475">Define the cost allocation</span></span>

<span data-ttu-id="8fd3b-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="8fd3b-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="8fd3b-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-479">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="8fd3b-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-481">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-481">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-482">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-483">35</span><span class="sxs-lookup"><span data-stu-id="8fd3b-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-484">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-484">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-485">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-485">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-486">55</span><span class="sxs-lookup"><span data-stu-id="8fd3b-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-487">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-487">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-488">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-489">10</span><span class="sxs-lookup"><span data-stu-id="8fd3b-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="8fd3b-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-492">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="8fd3b-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-494">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-494">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-495">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-495">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-496">65</span><span class="sxs-lookup"><span data-stu-id="8fd3b-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-497">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-497">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-498">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-499">35</span><span class="sxs-lookup"><span data-stu-id="8fd3b-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="8fd3b-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-502">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-504">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-505">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-506">60</span><span class="sxs-lookup"><span data-stu-id="8fd3b-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-507">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-508">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-509">20</span><span class="sxs-lookup"><span data-stu-id="8fd3b-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="8fd3b-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-512">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-514">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-515">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-516">80</span><span class="sxs-lookup"><span data-stu-id="8fd3b-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-517">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-518">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-519">September</span><span class="sxs-lookup"><span data-stu-id="8fd3b-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8fd3b-520">In Finance and Operations können statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="8fd3b-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="8fd3b-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-523">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-524">Größe</span><span class="sxs-lookup"><span data-stu-id="8fd3b-524">Magnitude</span></span></th>
<th><span data-ttu-id="8fd3b-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="8fd3b-525">Allocation factor</span></span></th>
<th><span data-ttu-id="8fd3b-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-526">Amount</span></span></th>
<th><span data-ttu-id="8fd3b-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-528">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-528">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-529">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-530">35</span><span class="sxs-lookup"><span data-stu-id="8fd3b-530">35</span></span></td>
<td><span data-ttu-id="8fd3b-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8fd3b-532">175.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-532">175.00</span></span></td>
<td><span data-ttu-id="8fd3b-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-534">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-534">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-535">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-535">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-536">55</span><span class="sxs-lookup"><span data-stu-id="8fd3b-536">55</span></span></td>
<td><span data-ttu-id="8fd3b-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8fd3b-538">275.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-538">275.00</span></span></td>
<td><span data-ttu-id="8fd3b-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-540">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-540">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-541">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-542">10</span><span class="sxs-lookup"><span data-stu-id="8fd3b-542">10</span></span></td>
<td><span data-ttu-id="8fd3b-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8fd3b-544">50,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-544">50.00</span></span></td>
<td><span data-ttu-id="8fd3b-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-546">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-546">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-547">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-548">35</span><span class="sxs-lookup"><span data-stu-id="8fd3b-548">35</span></span></td>
<td><span data-ttu-id="8fd3b-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8fd3b-550">436.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-550">436.00</span></span></td>
<td><span data-ttu-id="8fd3b-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-552">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-552">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-553">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-553">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-554">55</span><span class="sxs-lookup"><span data-stu-id="8fd3b-554">55</span></span></td>
<td><span data-ttu-id="8fd3b-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8fd3b-556">685.14</span><span class="sxs-lookup"><span data-stu-id="8fd3b-556">685.14</span></span></td>
<td><span data-ttu-id="8fd3b-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-558">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-558">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-559">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-560">10</span><span class="sxs-lookup"><span data-stu-id="8fd3b-560">10</span></span></td>
<td><span data-ttu-id="8fd3b-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8fd3b-562">124.57</span><span class="sxs-lookup"><span data-stu-id="8fd3b-562">124.57</span></span></td>
<td><span data-ttu-id="8fd3b-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-565">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-566">Größe</span><span class="sxs-lookup"><span data-stu-id="8fd3b-566">Magnitude</span></span></th>
<th><span data-ttu-id="8fd3b-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="8fd3b-567">Allocation factor</span></span></th>
<th><span data-ttu-id="8fd3b-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-568">Amount</span></span></th>
<th><span data-ttu-id="8fd3b-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-570">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-570">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-571">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-571">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-572">65</span><span class="sxs-lookup"><span data-stu-id="8fd3b-572">65</span></span></td>
<td><span data-ttu-id="8fd3b-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8fd3b-574">438.75</span><span class="sxs-lookup"><span data-stu-id="8fd3b-574">438.75</span></span></td>
<td><span data-ttu-id="8fd3b-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-576">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-576">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-577">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-578">35</span><span class="sxs-lookup"><span data-stu-id="8fd3b-578">35</span></span></td>
<td><span data-ttu-id="8fd3b-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8fd3b-580">236.25</span><span class="sxs-lookup"><span data-stu-id="8fd3b-580">236.25</span></span></td>
<td><span data-ttu-id="8fd3b-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-582">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-582">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-583">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-583">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-584">65</span><span class="sxs-lookup"><span data-stu-id="8fd3b-584">65</span></span></td>
<td><span data-ttu-id="8fd3b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8fd3b-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8fd3b-586">5,297.69</span></span></td>
<td><span data-ttu-id="8fd3b-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-588">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-588">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-589">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-590">35</span><span class="sxs-lookup"><span data-stu-id="8fd3b-590">35</span></span></td>
<td><span data-ttu-id="8fd3b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8fd3b-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8fd3b-592">2,852.60</span></span></td>
<td><span data-ttu-id="8fd3b-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-595">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-596">Größe</span><span class="sxs-lookup"><span data-stu-id="8fd3b-596">Magnitude</span></span></th>
<th><span data-ttu-id="8fd3b-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="8fd3b-597">Allocation factor</span></span></th>
<th><span data-ttu-id="8fd3b-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-598">Amount</span></span></th>
<th><span data-ttu-id="8fd3b-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-600">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-601">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-602">60</span><span class="sxs-lookup"><span data-stu-id="8fd3b-602">60</span></span></td>
<td><span data-ttu-id="8fd3b-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8fd3b-604">535.31</span><span class="sxs-lookup"><span data-stu-id="8fd3b-604">535.31</span></span></td>
<td><span data-ttu-id="8fd3b-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-606">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-607">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-608">20</span><span class="sxs-lookup"><span data-stu-id="8fd3b-608">20</span></span></td>
<td><span data-ttu-id="8fd3b-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8fd3b-610">178.44</span><span class="sxs-lookup"><span data-stu-id="8fd3b-610">178.44</span></span></td>
<td><span data-ttu-id="8fd3b-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-612">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-613">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-614">60</span><span class="sxs-lookup"><span data-stu-id="8fd3b-614">60</span></span></td>
<td><span data-ttu-id="8fd3b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8fd3b-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8fd3b-616">4,487.12</span></span></td>
<td><span data-ttu-id="8fd3b-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-618">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-619">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-620">20</span><span class="sxs-lookup"><span data-stu-id="8fd3b-620">20</span></span></td>
<td><span data-ttu-id="8fd3b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8fd3b-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-622">1,495.71</span></span></td>
<td><span data-ttu-id="8fd3b-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8fd3b-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-625">Cost object</span></span></th>
<th><span data-ttu-id="8fd3b-626">Größe</span><span class="sxs-lookup"><span data-stu-id="8fd3b-626">Magnitude</span></span></th>
<th><span data-ttu-id="8fd3b-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="8fd3b-627">Allocation factor</span></span></th>
<th><span data-ttu-id="8fd3b-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-628">Amount</span></span></th>
<th><span data-ttu-id="8fd3b-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-630">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-631">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-632">80</span><span class="sxs-lookup"><span data-stu-id="8fd3b-632">80</span></span></td>
<td><span data-ttu-id="8fd3b-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8fd3b-634">241.05</span><span class="sxs-lookup"><span data-stu-id="8fd3b-634">241.05</span></span></td>
<td><span data-ttu-id="8fd3b-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-636">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-637">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-638">15</span><span class="sxs-lookup"><span data-stu-id="8fd3b-638">15</span></span></td>
<td><span data-ttu-id="8fd3b-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8fd3b-640">45.20</span><span class="sxs-lookup"><span data-stu-id="8fd3b-640">45.20</span></span></td>
<td><span data-ttu-id="8fd3b-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-642">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-643">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-644">80</span><span class="sxs-lookup"><span data-stu-id="8fd3b-644">80</span></span></td>
<td><span data-ttu-id="8fd3b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8fd3b-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8fd3b-646">2,507.09</span></span></td>
<td><span data-ttu-id="8fd3b-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-648">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-649">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-650">15</span><span class="sxs-lookup"><span data-stu-id="8fd3b-650">15</span></span></td>
<td><span data-ttu-id="8fd3b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8fd3b-652">470.08</span><span class="sxs-lookup"><span data-stu-id="8fd3b-652">470.08</span></span></td>
<td><span data-ttu-id="8fd3b-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8fd3b-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-655">Journal</span></span></th>
<th><span data-ttu-id="8fd3b-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="8fd3b-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8fd3b-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="8fd3b-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8fd3b-658">Version</span><span class="sxs-lookup"><span data-stu-id="8fd3b-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-659">00004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-659">00004</span></span></td>
<td><span data-ttu-id="8fd3b-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="8fd3b-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="8fd3b-661">Fiscal</span></span></td>
<td><span data-ttu-id="8fd3b-662">2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-662">2017</span></span></td>
<td><span data-ttu-id="8fd3b-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-663">Period 1</span></span></td>
<td><span data-ttu-id="8fd3b-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="8fd3b-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8fd3b-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-668">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-669">Cost behavior</span></span></th>
<th><span data-ttu-id="8fd3b-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-672">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-672">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-673">HR</span></span></td>
<td><span data-ttu-id="8fd3b-674">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-674">10001</span></span></td>
<td><span data-ttu-id="8fd3b-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-675">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-676">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-677">500,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-679">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-679">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-680">HR</span></span></td>
<td><span data-ttu-id="8fd3b-681">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-681">10001</span></span></td>
<td><span data-ttu-id="8fd3b-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-682">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-683">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-686">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-686">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-687">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-688">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-688">10001</span></span></td>
<td><span data-ttu-id="8fd3b-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-689">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-690">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-691">675.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-693">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-693">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-694">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-695">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-695">10001</span></span></td>
<td><span data-ttu-id="8fd3b-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-696">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-697">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="8fd3b-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-700">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-700">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-701">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-701">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-702">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-702">10001</span></span></td>
<td><span data-ttu-id="8fd3b-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-703">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-704">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-705">713.75</span><span class="sxs-lookup"><span data-stu-id="8fd3b-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-707">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-707">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-708">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-708">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-709">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-709">10001</span></span></td>
<td><span data-ttu-id="8fd3b-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-710">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-711">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="8fd3b-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-714">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-714">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-715">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-716">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-716">10001</span></span></td>
<td><span data-ttu-id="8fd3b-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-717">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-718">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-719">286.25</span><span class="sxs-lookup"><span data-stu-id="8fd3b-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-721">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-721">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-722">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-723">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-723">10001</span></span></td>
<td><span data-ttu-id="8fd3b-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-724">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-725">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="8fd3b-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-728">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-729">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-730">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-730">10001</span></span></td>
<td><span data-ttu-id="8fd3b-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-731">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-732">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-733">776.36</span><span class="sxs-lookup"><span data-stu-id="8fd3b-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-735">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-736">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-737">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-737">10001</span></span></td>
<td><span data-ttu-id="8fd3b-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-738">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-739">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8fd3b-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-742">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-743">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-744">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-744">10001</span></span></td>
<td><span data-ttu-id="8fd3b-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-745">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-746">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-747">223.64</span><span class="sxs-lookup"><span data-stu-id="8fd3b-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="8fd3b-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-749">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-750">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-751">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-751">10001</span></span></td>
<td><span data-ttu-id="8fd3b-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-752">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-753">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8fd3b-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8fd3b-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="8fd3b-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8fd3b-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8fd3b-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-757">Cost element</span></span></th>
<th><span data-ttu-id="8fd3b-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-758">Cost behavior</span></span></th>
<th><span data-ttu-id="8fd3b-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-759">Amount</span></span></th>
<th><span data-ttu-id="8fd3b-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="8fd3b-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8fd3b-761">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-761">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-762">HR</span></span></td>
<td><span data-ttu-id="8fd3b-763">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-763">10001</span></span></td>
<td><span data-ttu-id="8fd3b-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-764">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-765">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-766">-500.00</span></span></td>
<td><span data-ttu-id="8fd3b-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-768">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-768">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-769">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-770">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-770">10001</span></span></td>
<td><span data-ttu-id="8fd3b-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-771">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-772">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-773">175.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-773">175.00</span></span></td>
<td><span data-ttu-id="8fd3b-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-775">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-775">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-776">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-776">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-777">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-777">10001</span></span></td>
<td><span data-ttu-id="8fd3b-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-778">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-779">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-780">275.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-780">275.00</span></span></td>
<td><span data-ttu-id="8fd3b-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-782">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-782">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-783">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-784">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-784">10001</span></span></td>
<td><span data-ttu-id="8fd3b-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-785">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-786">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-787">50,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-787">50,00</span></span></td>
<td><span data-ttu-id="8fd3b-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-789">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-789">CC001</span></span></td>
<td><span data-ttu-id="8fd3b-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-790">HR</span></span></td>
<td><span data-ttu-id="8fd3b-791">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-791">10001</span></span></td>
<td><span data-ttu-id="8fd3b-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-792">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-793">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-794">-1,245.71</span></span></td>
<td><span data-ttu-id="8fd3b-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-796">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-796">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-797">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-798">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-798">10001</span></span></td>
<td><span data-ttu-id="8fd3b-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-799">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-800">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-801">436.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-801">436.00</span></span></td>
<td><span data-ttu-id="8fd3b-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-803">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-803">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-804">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-804">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-805">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-805">10001</span></span></td>
<td><span data-ttu-id="8fd3b-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-806">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-807">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-808">685.14</span><span class="sxs-lookup"><span data-stu-id="8fd3b-808">685.14</span></span></td>
<td><span data-ttu-id="8fd3b-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-810">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-810">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-811">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-812">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-812">10001</span></span></td>
<td><span data-ttu-id="8fd3b-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-813">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-814">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-815">124.57</span><span class="sxs-lookup"><span data-stu-id="8fd3b-815">124.57</span></span></td>
<td><span data-ttu-id="8fd3b-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-817">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-817">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-818">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-819">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-819">10001</span></span></td>
<td><span data-ttu-id="8fd3b-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-820">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-821">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-822">-675.00</span></span></td>
<td><span data-ttu-id="8fd3b-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-824">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-824">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-825">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-825">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-826">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-826">10001</span></span></td>
<td><span data-ttu-id="8fd3b-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-827">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-828">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-829">438.75</span><span class="sxs-lookup"><span data-stu-id="8fd3b-829">438.75</span></span></td>
<td><span data-ttu-id="8fd3b-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-831">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-831">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-832">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-833">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-833">10001</span></span></td>
<td><span data-ttu-id="8fd3b-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-834">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-835">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-836">236.25</span><span class="sxs-lookup"><span data-stu-id="8fd3b-836">236.25</span></span></td>
<td><span data-ttu-id="8fd3b-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-838">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-838">CC002</span></span></td>
<td><span data-ttu-id="8fd3b-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8fd3b-839">Finance</span></span></td>
<td><span data-ttu-id="8fd3b-840">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-840">10001</span></span></td>
<td><span data-ttu-id="8fd3b-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-841">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-842">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="8fd3b-843">-8,150.29</span></span></td>
<td><span data-ttu-id="8fd3b-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-845">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-845">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-846">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-846">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-847">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-847">10001</span></span></td>
<td><span data-ttu-id="8fd3b-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-848">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-849">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8fd3b-850">5,297.69</span></span></td>
<td><span data-ttu-id="8fd3b-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-852">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-852">CC004</span></span></td>
<td><span data-ttu-id="8fd3b-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-853">Packaging</span></span></td>
<td><span data-ttu-id="8fd3b-854">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-854">10001</span></span></td>
<td><span data-ttu-id="8fd3b-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-855">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-856">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8fd3b-857">2,852.60</span></span></td>
<td><span data-ttu-id="8fd3b-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-859">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-859">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-860">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-860">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-861">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-861">10001</span></span></td>
<td><span data-ttu-id="8fd3b-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-862">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-863">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="8fd3b-864">-713.75</span></span></td>
<td><span data-ttu-id="8fd3b-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-866">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-867">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-868">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-868">10001</span></span></td>
<td><span data-ttu-id="8fd3b-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-869">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-870">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-871">535.31</span><span class="sxs-lookup"><span data-stu-id="8fd3b-871">535.31</span></span></td>
<td><span data-ttu-id="8fd3b-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-873">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-874">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-875">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-875">10001</span></span></td>
<td><span data-ttu-id="8fd3b-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-876">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-877">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-878">178.44</span><span class="sxs-lookup"><span data-stu-id="8fd3b-878">178.44</span></span></td>
<td><span data-ttu-id="8fd3b-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-880">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-880">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-881">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-881">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-882">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-882">10001</span></span></td>
<td><span data-ttu-id="8fd3b-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-883">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-884">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="8fd3b-885">-5,982.83</span></span></td>
<td><span data-ttu-id="8fd3b-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-887">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-888">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-889">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-889">10001</span></span></td>
<td><span data-ttu-id="8fd3b-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-890">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-891">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8fd3b-892">4,487.12</span></span></td>
<td><span data-ttu-id="8fd3b-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-894">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-895">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-896">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-896">10001</span></span></td>
<td><span data-ttu-id="8fd3b-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-897">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-898">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8fd3b-899">1,495.71</span></span></td>
<td><span data-ttu-id="8fd3b-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-901">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-901">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-902">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-902">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-903">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-903">10001</span></span></td>
<td><span data-ttu-id="8fd3b-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-904">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-905">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="8fd3b-906">-286.25</span></span></td>
<td><span data-ttu-id="8fd3b-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-908">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-909">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-910">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-910">10001</span></span></td>
<td><span data-ttu-id="8fd3b-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-911">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-912">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-913">241.05</span><span class="sxs-lookup"><span data-stu-id="8fd3b-913">241.05</span></span></td>
<td><span data-ttu-id="8fd3b-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-915">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-916">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-917">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-917">10001</span></span></td>
<td><span data-ttu-id="8fd3b-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-918">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-919">Fixed cost</span></span></td>
<td><span data-ttu-id="8fd3b-920">45.20</span><span class="sxs-lookup"><span data-stu-id="8fd3b-920">45.20</span></span></td>
<td><span data-ttu-id="8fd3b-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-922">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-922">CC003</span></span></td>
<td><span data-ttu-id="8fd3b-923">Montage</span><span class="sxs-lookup"><span data-stu-id="8fd3b-923">Assembly</span></span></td>
<td><span data-ttu-id="8fd3b-924">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-924">10001</span></span></td>
<td><span data-ttu-id="8fd3b-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-925">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-926">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="8fd3b-927">-2,977.17</span></span></td>
<td><span data-ttu-id="8fd3b-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-929">Prod 1</span></span></td>
<td><span data-ttu-id="8fd3b-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-930">Product 1</span></span></td>
<td><span data-ttu-id="8fd3b-931">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-931">10001</span></span></td>
<td><span data-ttu-id="8fd3b-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-932">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-933">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8fd3b-934">2,507.09</span></span></td>
<td><span data-ttu-id="8fd3b-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8fd3b-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-936">Prod 2</span></span></td>
<td><span data-ttu-id="8fd3b-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-937">Product 2</span></span></td>
<td><span data-ttu-id="8fd3b-938">10001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-938">10001</span></span></td>
<td><span data-ttu-id="8fd3b-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-939">Electricity</span></span></td>
<td><span data-ttu-id="8fd3b-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-940">Variable cost</span></span></td>
<td><span data-ttu-id="8fd3b-941">470.08</span><span class="sxs-lookup"><span data-stu-id="8fd3b-941">470.08</span></span></td>
<td><span data-ttu-id="8fd3b-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="8fd3b-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="8fd3b-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="8fd3b-943">Conclusion</span></span>
<span data-ttu-id="8fd3b-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="8fd3b-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="8fd3b-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="8fd3b-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="8fd3b-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="8fd3b-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="8fd3b-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="8fd3b-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8fd3b-951">CC099</span><span class="sxs-lookup"><span data-stu-id="8fd3b-951">CC099</span></span></th>
<th><span data-ttu-id="8fd3b-952">CC001</span><span class="sxs-lookup"><span data-stu-id="8fd3b-952">CC001</span></span></th>
<th><span data-ttu-id="8fd3b-953">CC002</span><span class="sxs-lookup"><span data-stu-id="8fd3b-953">CC002</span></span></th>
<th><span data-ttu-id="8fd3b-954">CC003</span><span class="sxs-lookup"><span data-stu-id="8fd3b-954">CC003</span></span></th>
<th><span data-ttu-id="8fd3b-955">CC004</span><span class="sxs-lookup"><span data-stu-id="8fd3b-955">CC004</span></span></th>
<th><span data-ttu-id="8fd3b-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-956">Proj 1</span></span></th>
<th><span data-ttu-id="8fd3b-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-957">Proj 2</span></span></th>
<th><span data-ttu-id="8fd3b-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="8fd3b-958">Prod 1</span></span></th>
<th><span data-ttu-id="8fd3b-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="8fd3b-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="8fd3b-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="8fd3b-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="8fd3b-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="8fd3b-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-971">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="8fd3b-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-973">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-974">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-975">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-976">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-977">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-978">776.36</span><span class="sxs-lookup"><span data-stu-id="8fd3b-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-979">223.64</span><span class="sxs-lookup"><span data-stu-id="8fd3b-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="8fd3b-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="8fd3b-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-982">000</span><span class="sxs-lookup"><span data-stu-id="8fd3b-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-983">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-984">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-985">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-986">0,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-987">30,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-988">10,00</span><span class="sxs-lookup"><span data-stu-id="8fd3b-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8fd3b-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8fd3b-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8fd3b-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8fd3b-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8fd3b-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="8fd3b-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="8fd3b-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="8fd3b-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="8fd3b-996">Weitere Informationen hierzu finden Sie unter [Kostenzusammenfassung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



