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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f56feac74dfe78b740342688a908d001614cffd0
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="1d8ca-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-103">Overhead calculation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1d8ca-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="1d8ca-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="1d8ca-105">Term definition</span></span>
---------------

<span data-ttu-id="1d8ca-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="1d8ca-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="1d8ca-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="1d8ca-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="1d8ca-109">Miete</span><span class="sxs-lookup"><span data-stu-id="1d8ca-109">Rent</span></span>
-   <span data-ttu-id="1d8ca-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-110">Electricity</span></span>
-   <span data-ttu-id="1d8ca-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="1d8ca-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="1d8ca-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="1d8ca-112">Overhead calculation overview</span></span>
<span data-ttu-id="1d8ca-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="1d8ca-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="1d8ca-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="1d8ca-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="1d8ca-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="1d8ca-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="1d8ca-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="1d8ca-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="1d8ca-119">Version type</span></span>
-   <span data-ttu-id="1d8ca-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="1d8ca-120">Date and time</span></span>
-   <span data-ttu-id="1d8ca-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="1d8ca-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="1d8ca-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="1d8ca-122">Fiscal year</span></span>
-   <span data-ttu-id="1d8ca-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="1d8ca-123">Fiscal period</span></span>

<span data-ttu-id="1d8ca-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="1d8ca-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="1d8ca-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="1d8ca-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="1d8ca-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="1d8ca-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="1d8ca-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="1d8ca-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="1d8ca-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="1d8ca-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="1d8ca-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="1d8ca-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="1d8ca-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="1d8ca-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="1d8ca-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="1d8ca-140">Main account</span></span></th>
<th><span data-ttu-id="1d8ca-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-143">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-143">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-144">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-145">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-145">10001</span></span></td>
<td><span data-ttu-id="1d8ca-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-146">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="1d8ca-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="1d8ca-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="1d8ca-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="1d8ca-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="1d8ca-151">Define the cost behavior rule</span></span>

<span data-ttu-id="1d8ca-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="1d8ca-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="1d8ca-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="1d8ca-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="1d8ca-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="1d8ca-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="1d8ca-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="1d8ca-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="1d8ca-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="1d8ca-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="1d8ca-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="1d8ca-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-160">Journal</span></span></th>
<th><span data-ttu-id="1d8ca-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="1d8ca-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1d8ca-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1d8ca-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1d8ca-163">Version</span><span class="sxs-lookup"><span data-stu-id="1d8ca-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-164">00001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-164">00001</span></span></td>
<td><span data-ttu-id="1d8ca-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="1d8ca-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="1d8ca-166">Fiscal</span></span></td>
<td><span data-ttu-id="1d8ca-167">2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-167">2017</span></span></td>
<td><span data-ttu-id="1d8ca-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-168">Period 1</span></span></td>
<td><span data-ttu-id="1d8ca-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1d8ca-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-173">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-174">Cost behavior</span></span></th>
<th><span data-ttu-id="1d8ca-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-177">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-177">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-178">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-179">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-179">10001</span></span></td>
<td><span data-ttu-id="1d8ca-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-180">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="1d8ca-181">Unclassified</span></span></td>
<td><span data-ttu-id="1d8ca-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1d8ca-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="1d8ca-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-185">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-186">Cost behavior</span></span></th>
<th><span data-ttu-id="1d8ca-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-187">Amount</span></span></th>
<th><span data-ttu-id="1d8ca-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-189">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-189">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-190">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-191">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-191">10001</span></span></td>
<td><span data-ttu-id="1d8ca-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-192">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="1d8ca-193">Unclassified</span></span></td>
<td><span data-ttu-id="1d8ca-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-194">10,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-196">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-196">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-197">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-198">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-198">10001</span></span></td>
<td><span data-ttu-id="1d8ca-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-199">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="1d8ca-200">Unclassified</span></span></td>
<td><span data-ttu-id="1d8ca-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-201">-10,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-203">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-203">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-204">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-205">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-205">10001</span></span></td>
<td><span data-ttu-id="1d8ca-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-206">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-207">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-208">1,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-210">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-210">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-211">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-212">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-212">10001</span></span></td>
<td><span data-ttu-id="1d8ca-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-213">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-214">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-215">9,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-217">Detaillierte Informationen zum Kostenverhalten finden Sie in der Richtlinie Kostenverhalten.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="1d8ca-218">(Beachten Sie, dass dieses Thema noch nicht abgedeckt ist, aber bald verfügbar sein wird.)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="1d8ca-219">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="1d8ca-220">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="1d8ca-221">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="1d8ca-222">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="1d8ca-222">Define the cost distribution rule</span></span>

<span data-ttu-id="1d8ca-223">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="1d8ca-224">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="1d8ca-225">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="1d8ca-226">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="1d8ca-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="1d8ca-227">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="1d8ca-228">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-229">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-229">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-230">KWH</span><span class="sxs-lookup"><span data-stu-id="1d8ca-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-231">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-231">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-232">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-232">HR</span></span></td>
<td><span data-ttu-id="1d8ca-233">1.000</span><span class="sxs-lookup"><span data-stu-id="1d8ca-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-234">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-234">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-235">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-235">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-236">6.000</span><span class="sxs-lookup"><span data-stu-id="1d8ca-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-237">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-237">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-238">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-238">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-239">0</span><span class="sxs-lookup"><span data-stu-id="1d8ca-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-240">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-241">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-241">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-242">Größe</span><span class="sxs-lookup"><span data-stu-id="1d8ca-242">Magnitude</span></span></th>
<th><span data-ttu-id="1d8ca-243">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="1d8ca-243">Allocation factor</span></span></th>
<th><span data-ttu-id="1d8ca-244">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-245">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-245">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-246">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-246">HR</span></span></td>
<td><span data-ttu-id="1d8ca-247">1.000</span><span class="sxs-lookup"><span data-stu-id="1d8ca-247">1,000</span></span></td>
<td><span data-ttu-id="1d8ca-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-250">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-250">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-251">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-251">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-252">6.000</span><span class="sxs-lookup"><span data-stu-id="1d8ca-252">6,000</span></span></td>
<td><span data-ttu-id="1d8ca-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="1d8ca-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-255">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-255">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-256">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-256">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-257">0</span><span class="sxs-lookup"><span data-stu-id="1d8ca-257">0</span></span></td>
<td><span data-ttu-id="1d8ca-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-259">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-260">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="1d8ca-261">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-262">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-262">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-263">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-263">Formula</span></span></th>
<th><span data-ttu-id="1d8ca-264">Größe</span><span class="sxs-lookup"><span data-stu-id="1d8ca-264">Magnitude</span></span></th>
<th><span data-ttu-id="1d8ca-265">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="1d8ca-265">Allocation factor</span></span></th>
<th><span data-ttu-id="1d8ca-266">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-267">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-267">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-268">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-268">HR</span></span></td>
<td><span data-ttu-id="1d8ca-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1d8ca-270">1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-270">1</span></span></td>
<td><span data-ttu-id="1d8ca-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-272">500,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-273">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-273">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-274">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-274">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1d8ca-276">1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-276">1</span></span></td>
<td><span data-ttu-id="1d8ca-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-278">500,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-279">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-279">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-280">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-280">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1d8ca-282">0</span><span class="sxs-lookup"><span data-stu-id="1d8ca-282">0</span></span></td>
<td><span data-ttu-id="1d8ca-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-284">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="1d8ca-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-286">Erfassung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-286">Journal</span></span></th>
<th><span data-ttu-id="1d8ca-287">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="1d8ca-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1d8ca-288">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1d8ca-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1d8ca-289">Version</span><span class="sxs-lookup"><span data-stu-id="1d8ca-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-290">00002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-290">00002</span></span></td>
<td><span data-ttu-id="1d8ca-291">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="1d8ca-292">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="1d8ca-292">Fiscal</span></span></td>
<td><span data-ttu-id="1d8ca-293">2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-293">2017</span></span></td>
<td><span data-ttu-id="1d8ca-294">Periode 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-294">Period 1</span></span></td>
<td><span data-ttu-id="1d8ca-295">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1d8ca-296">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-297">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-298">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-299">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-299">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-300">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-300">Cost behavior</span></span></th>
<th><span data-ttu-id="1d8ca-301">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-302">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-303">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-303">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-304">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-304">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-305">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-305">10001</span></span></td>
<td><span data-ttu-id="1d8ca-306">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-306">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-307">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-307">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-309">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-310">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-310">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-311">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-311">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-312">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-312">10001</span></span></td>
<td><span data-ttu-id="1d8ca-313">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-313">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-314">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-314">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-315">9.000,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1d8ca-316">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="1d8ca-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-317">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-318">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-318">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-319">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-319">Cost behavior</span></span></th>
<th><span data-ttu-id="1d8ca-320">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-320">Amount</span></span></th>
<th><span data-ttu-id="1d8ca-321">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-322">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-322">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-323">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-323">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-324">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-324">10001</span></span></td>
<td><span data-ttu-id="1d8ca-325">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-325">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-326">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-326">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-327">-1,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-328">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-329">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-329">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-330">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-330">HR</span></span></td>
<td><span data-ttu-id="1d8ca-331">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-331">10001</span></span></td>
<td><span data-ttu-id="1d8ca-332">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-332">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-333">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-333">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-334">500,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-334">500.00</span></span></td>
<td><span data-ttu-id="1d8ca-335">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-336">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-336">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-337">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-337">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-338">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-338">10001</span></span></td>
<td><span data-ttu-id="1d8ca-339">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-339">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-340">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-340">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-341">500,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-341">500.00</span></span></td>
<td><span data-ttu-id="1d8ca-342">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-343">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-343">CC099</span></span></td>
<td><span data-ttu-id="1d8ca-344">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="1d8ca-344">Default cost center</span></span></td>
<td><span data-ttu-id="1d8ca-345">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-345">10001</span></span></td>
<td><span data-ttu-id="1d8ca-346">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-346">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-347">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-347">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-348">-9,000.00</span></span></td>
<td><span data-ttu-id="1d8ca-349">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-350">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-350">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-351">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-351">HR</span></span></td>
<td><span data-ttu-id="1d8ca-352">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-352">10001</span></span></td>
<td><span data-ttu-id="1d8ca-353">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-353">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-354">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-354">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-355">1,285.71</span></span></td>
<td><span data-ttu-id="1d8ca-356">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-357">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-357">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-358">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-358">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-359">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-359">10001</span></span></td>
<td><span data-ttu-id="1d8ca-360">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-360">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-361">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-361">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="1d8ca-362">7,714.29</span></span></td>
<td><span data-ttu-id="1d8ca-363">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-364">Detaillierte Informationen zur Verrechnungsgrundlage und der Kostenaufteilung finden Sie unter Richtlinie zur Verrechnungsgrundlage und der Kostenbasis.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="1d8ca-365">(Beachten Sie, dass dieses Thema noch nicht abgedeckt ist, aber bald verfügbar sein wird.)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="1d8ca-366">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="1d8ca-367">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="1d8ca-368">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="1d8ca-369">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="1d8ca-369">Define the overhead rate</span></span>

<span data-ttu-id="1d8ca-370">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="1d8ca-371">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-372">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-372">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-373">Stunden</span><span class="sxs-lookup"><span data-stu-id="1d8ca-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-374">Proj 1</span></span></td>
<td><span data-ttu-id="1d8ca-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-375">Project 1</span></span></td>
<td><span data-ttu-id="1d8ca-376">3</span><span class="sxs-lookup"><span data-stu-id="1d8ca-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-377">Proj 2</span></span></td>
<td><span data-ttu-id="1d8ca-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-378">Project 2</span></span></td>
<td><span data-ttu-id="1d8ca-379">1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-380">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-381">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-381">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-382">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-382">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-383">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-383">Cost behavior</span></span></th>
<th><span data-ttu-id="1d8ca-384">Einheiten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-384">Units</span></span></th>
<th><span data-ttu-id="1d8ca-385">Satz</span><span class="sxs-lookup"><span data-stu-id="1d8ca-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-386">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-386">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-387">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-387">HR</span></span></td>
<td><span data-ttu-id="1d8ca-388">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-388">10001</span></span></td>
<td><span data-ttu-id="1d8ca-389">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-389">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-390">1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-390">1</span></span></td>
<td><span data-ttu-id="1d8ca-391">10</span><span class="sxs-lookup"><span data-stu-id="1d8ca-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-392">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-393">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-393">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-394">Größe</span><span class="sxs-lookup"><span data-stu-id="1d8ca-394">Magnitude</span></span></th>
<th><span data-ttu-id="1d8ca-395">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-395">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-396">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="1d8ca-396">Allocation factor</span></span></th>
<th><span data-ttu-id="1d8ca-397">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-398">Proj 1</span></span></td>
<td><span data-ttu-id="1d8ca-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-399">Project 1</span></span></td>
<td><span data-ttu-id="1d8ca-400">3</span><span class="sxs-lookup"><span data-stu-id="1d8ca-400">3</span></span></td>
<td><span data-ttu-id="1d8ca-401">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-401">10001</span></span></td>
<td><span data-ttu-id="1d8ca-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="1d8ca-403">30,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-404">Proj 2</span></span></td>
<td><span data-ttu-id="1d8ca-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-405">Project 2</span></span></td>
<td><span data-ttu-id="1d8ca-406">1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-406">1</span></span></td>
<td><span data-ttu-id="1d8ca-407">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-407">10001</span></span></td>
<td><span data-ttu-id="1d8ca-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="1d8ca-409">10,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="1d8ca-410">Erfassung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-411">Erfassung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-411">Journal</span></span></th>
<th><span data-ttu-id="1d8ca-412">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="1d8ca-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1d8ca-413">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1d8ca-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1d8ca-414">Version</span><span class="sxs-lookup"><span data-stu-id="1d8ca-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-415">00003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-415">00003</span></span></td>
<td><span data-ttu-id="1d8ca-416">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="1d8ca-417">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="1d8ca-417">Fiscal</span></span></td>
<td><span data-ttu-id="1d8ca-418">2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-418">2017</span></span></td>
<td><span data-ttu-id="1d8ca-419">Periode 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-419">Period 1</span></span></td>
<td><span data-ttu-id="1d8ca-420">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="1d8ca-421">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-422">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-423">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-423">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-424">Größe</span><span class="sxs-lookup"><span data-stu-id="1d8ca-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-425">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-426">Proj 1</span></span></td>
<td><span data-ttu-id="1d8ca-427">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="1d8ca-428">3,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-429">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-430">Proj 2</span></span></td>
<td><span data-ttu-id="1d8ca-431">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="1d8ca-432">1,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1d8ca-433">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="1d8ca-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-434">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-435">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-435">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-436">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-436">Cost behavior</span></span></th>
<th><span data-ttu-id="1d8ca-437">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-437">Amount</span></span></th>
<th><span data-ttu-id="1d8ca-438">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-439">CC0001</span></span></td>
<td><span data-ttu-id="1d8ca-440">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-440">HR</span></span></td>
<td><span data-ttu-id="1d8ca-441">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-441">10001</span></span></td>
<td><span data-ttu-id="1d8ca-442">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-442">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-443">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-443">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-444">-30.00</span></span></td>
<td><span data-ttu-id="1d8ca-445">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-446">Proj 1</span></span></td>
<td><span data-ttu-id="1d8ca-447">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="1d8ca-448">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-448">10001</span></span></td>
<td><span data-ttu-id="1d8ca-449">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-449">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-450">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-450">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-451">30,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-451">30.00</span></span></td>
<td><span data-ttu-id="1d8ca-452">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-453">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-453">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-454">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-454">HR</span></span></td>
<td><span data-ttu-id="1d8ca-455">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-455">10001</span></span></td>
<td><span data-ttu-id="1d8ca-456">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-456">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-457">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-457">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-458">-10.00</span></span></td>
<td><span data-ttu-id="1d8ca-459">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-460">Proj 2</span></span></td>
<td><span data-ttu-id="1d8ca-461">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="1d8ca-462">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-462">10001</span></span></td>
<td><span data-ttu-id="1d8ca-463">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-463">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-464">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-464">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-465">10,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-465">10.00</span></span></td>
<td><span data-ttu-id="1d8ca-466">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-467">Detaillierte Informationen zur Richtlinie über Gemeinkostensätze finden Sie in der Richtlinie Gemeinkostensatz und Zuweisungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="1d8ca-468">(Beachten Sie, dass dieses Thema noch nicht abgedeckt ist, aber bald verfügbar sein wird.)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="1d8ca-469">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="1d8ca-470">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="1d8ca-471">Finance and Operations unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="1d8ca-472">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="1d8ca-473">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="1d8ca-474">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="1d8ca-475">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="1d8ca-476">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="1d8ca-477">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="1d8ca-478">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="1d8ca-478">Define the cost allocation</span></span>

<span data-ttu-id="1d8ca-479">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="1d8ca-480">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="1d8ca-481">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-482">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-482">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-483">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="1d8ca-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-484">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-484">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-485">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-485">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-486">35</span><span class="sxs-lookup"><span data-stu-id="1d8ca-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-487">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-487">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-488">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-488">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-489">55</span><span class="sxs-lookup"><span data-stu-id="1d8ca-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-490">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-490">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-491">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-491">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-492">10</span><span class="sxs-lookup"><span data-stu-id="1d8ca-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-493">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="1d8ca-494">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-495">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-495">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-496">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="1d8ca-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-497">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-497">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-498">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-498">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-499">65</span><span class="sxs-lookup"><span data-stu-id="1d8ca-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-500">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-500">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-501">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-501">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-502">35</span><span class="sxs-lookup"><span data-stu-id="1d8ca-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-503">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="1d8ca-504">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-505">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-505">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-506">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-507">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-507">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-508">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-509">60</span><span class="sxs-lookup"><span data-stu-id="1d8ca-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-510">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-510">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-511">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-512">20</span><span class="sxs-lookup"><span data-stu-id="1d8ca-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-513">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="1d8ca-514">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-515">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-515">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-516">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-517">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-517">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-518">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-519">80</span><span class="sxs-lookup"><span data-stu-id="1d8ca-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-520">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-520">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-521">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-522">15</span><span class="sxs-lookup"><span data-stu-id="1d8ca-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-523">**Hinweis:** In Finance and Operations können statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="1d8ca-524">Ausführliche Informationen zur Anzeige statistischer Kennzahlanbieter, finden Sie in der Anbietervorlage statistischen Kennzahl.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="1d8ca-525">(Hinweis, dieses Thema ist nicht abgeschlossen, aber bald verfügbar) Die folgende Tabelle zeigt das Ergebnis an, wenn der HR-Service als Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten angewendet würde (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="1d8ca-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-526">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-526">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-527">Größe</span><span class="sxs-lookup"><span data-stu-id="1d8ca-527">Magnitude</span></span></th>
<th><span data-ttu-id="1d8ca-528">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="1d8ca-528">Allocation factor</span></span></th>
<th><span data-ttu-id="1d8ca-529">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-529">Amount</span></span></th>
<th><span data-ttu-id="1d8ca-530">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-531">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-531">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-532">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-532">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-533">35</span><span class="sxs-lookup"><span data-stu-id="1d8ca-533">35</span></span></td>
<td><span data-ttu-id="1d8ca-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1d8ca-535">175.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-535">175.00</span></span></td>
<td><span data-ttu-id="1d8ca-536">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-537">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-537">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-538">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-538">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-539">55</span><span class="sxs-lookup"><span data-stu-id="1d8ca-539">55</span></span></td>
<td><span data-ttu-id="1d8ca-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1d8ca-541">275.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-541">275.00</span></span></td>
<td><span data-ttu-id="1d8ca-542">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-543">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-543">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-544">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-544">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-545">10</span><span class="sxs-lookup"><span data-stu-id="1d8ca-545">10</span></span></td>
<td><span data-ttu-id="1d8ca-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1d8ca-547">50,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-547">50.00</span></span></td>
<td><span data-ttu-id="1d8ca-548">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-549">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-549">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-550">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-550">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-551">35</span><span class="sxs-lookup"><span data-stu-id="1d8ca-551">35</span></span></td>
<td><span data-ttu-id="1d8ca-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1d8ca-553">436.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-553">436.00</span></span></td>
<td><span data-ttu-id="1d8ca-554">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-555">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-555">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-556">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-556">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-557">55</span><span class="sxs-lookup"><span data-stu-id="1d8ca-557">55</span></span></td>
<td><span data-ttu-id="1d8ca-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1d8ca-559">685.14</span><span class="sxs-lookup"><span data-stu-id="1d8ca-559">685.14</span></span></td>
<td><span data-ttu-id="1d8ca-560">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-561">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-561">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-562">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-562">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-563">10</span><span class="sxs-lookup"><span data-stu-id="1d8ca-563">10</span></span></td>
<td><span data-ttu-id="1d8ca-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1d8ca-565">124.57</span><span class="sxs-lookup"><span data-stu-id="1d8ca-565">124.57</span></span></td>
<td><span data-ttu-id="1d8ca-566">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-567">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="1d8ca-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-568">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-568">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-569">Größe</span><span class="sxs-lookup"><span data-stu-id="1d8ca-569">Magnitude</span></span></th>
<th><span data-ttu-id="1d8ca-570">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="1d8ca-570">Allocation factor</span></span></th>
<th><span data-ttu-id="1d8ca-571">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-571">Amount</span></span></th>
<th><span data-ttu-id="1d8ca-572">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-573">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-573">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-574">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-574">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-575">65</span><span class="sxs-lookup"><span data-stu-id="1d8ca-575">65</span></span></td>
<td><span data-ttu-id="1d8ca-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="1d8ca-577">438.75</span><span class="sxs-lookup"><span data-stu-id="1d8ca-577">438.75</span></span></td>
<td><span data-ttu-id="1d8ca-578">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-579">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-579">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-580">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-580">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-581">35</span><span class="sxs-lookup"><span data-stu-id="1d8ca-581">35</span></span></td>
<td><span data-ttu-id="1d8ca-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="1d8ca-583">236.25</span><span class="sxs-lookup"><span data-stu-id="1d8ca-583">236.25</span></span></td>
<td><span data-ttu-id="1d8ca-584">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-585">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-585">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-586">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-586">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-587">65</span><span class="sxs-lookup"><span data-stu-id="1d8ca-587">65</span></span></td>
<td><span data-ttu-id="1d8ca-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="1d8ca-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="1d8ca-589">5,297.69</span></span></td>
<td><span data-ttu-id="1d8ca-590">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-591">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-591">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-592">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-592">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-593">35</span><span class="sxs-lookup"><span data-stu-id="1d8ca-593">35</span></span></td>
<td><span data-ttu-id="1d8ca-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="1d8ca-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="1d8ca-595">2,852.60</span></span></td>
<td><span data-ttu-id="1d8ca-596">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-597">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="1d8ca-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-598">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-598">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-599">Größe</span><span class="sxs-lookup"><span data-stu-id="1d8ca-599">Magnitude</span></span></th>
<th><span data-ttu-id="1d8ca-600">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="1d8ca-600">Allocation factor</span></span></th>
<th><span data-ttu-id="1d8ca-601">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-601">Amount</span></span></th>
<th><span data-ttu-id="1d8ca-602">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-603">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-603">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-604">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-605">60</span><span class="sxs-lookup"><span data-stu-id="1d8ca-605">60</span></span></td>
<td><span data-ttu-id="1d8ca-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="1d8ca-607">535.31</span><span class="sxs-lookup"><span data-stu-id="1d8ca-607">535.31</span></span></td>
<td><span data-ttu-id="1d8ca-608">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-609">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-609">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-610">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-611">20</span><span class="sxs-lookup"><span data-stu-id="1d8ca-611">20</span></span></td>
<td><span data-ttu-id="1d8ca-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="1d8ca-613">178.44</span><span class="sxs-lookup"><span data-stu-id="1d8ca-613">178.44</span></span></td>
<td><span data-ttu-id="1d8ca-614">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-615">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-615">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-616">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-617">60</span><span class="sxs-lookup"><span data-stu-id="1d8ca-617">60</span></span></td>
<td><span data-ttu-id="1d8ca-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="1d8ca-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="1d8ca-619">4,487.12</span></span></td>
<td><span data-ttu-id="1d8ca-620">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-621">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-621">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-622">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-623">20</span><span class="sxs-lookup"><span data-stu-id="1d8ca-623">20</span></span></td>
<td><span data-ttu-id="1d8ca-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="1d8ca-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-625">1,495.71</span></span></td>
<td><span data-ttu-id="1d8ca-626">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d8ca-627">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="1d8ca-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-628">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-628">Cost object</span></span></th>
<th><span data-ttu-id="1d8ca-629">Größe</span><span class="sxs-lookup"><span data-stu-id="1d8ca-629">Magnitude</span></span></th>
<th><span data-ttu-id="1d8ca-630">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="1d8ca-630">Allocation factor</span></span></th>
<th><span data-ttu-id="1d8ca-631">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-631">Amount</span></span></th>
<th><span data-ttu-id="1d8ca-632">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-633">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-633">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-634">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-635">80</span><span class="sxs-lookup"><span data-stu-id="1d8ca-635">80</span></span></td>
<td><span data-ttu-id="1d8ca-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="1d8ca-637">241.05</span><span class="sxs-lookup"><span data-stu-id="1d8ca-637">241.05</span></span></td>
<td><span data-ttu-id="1d8ca-638">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-639">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-639">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-640">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-641">15</span><span class="sxs-lookup"><span data-stu-id="1d8ca-641">15</span></span></td>
<td><span data-ttu-id="1d8ca-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="1d8ca-643">45.20</span><span class="sxs-lookup"><span data-stu-id="1d8ca-643">45.20</span></span></td>
<td><span data-ttu-id="1d8ca-644">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-645">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-645">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-646">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-647">80</span><span class="sxs-lookup"><span data-stu-id="1d8ca-647">80</span></span></td>
<td><span data-ttu-id="1d8ca-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="1d8ca-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="1d8ca-649">2,507.09</span></span></td>
<td><span data-ttu-id="1d8ca-650">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-651">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-651">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-652">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-653">15</span><span class="sxs-lookup"><span data-stu-id="1d8ca-653">15</span></span></td>
<td><span data-ttu-id="1d8ca-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="1d8ca-655">470.08</span><span class="sxs-lookup"><span data-stu-id="1d8ca-655">470.08</span></span></td>
<td><span data-ttu-id="1d8ca-656">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1d8ca-657">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-658">Erfassung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-658">Journal</span></span></th>
<th><span data-ttu-id="1d8ca-659">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="1d8ca-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1d8ca-660">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1d8ca-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1d8ca-661">Version</span><span class="sxs-lookup"><span data-stu-id="1d8ca-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-662">00004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-662">00004</span></span></td>
<td><span data-ttu-id="1d8ca-663">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="1d8ca-664">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="1d8ca-664">Fiscal</span></span></td>
<td><span data-ttu-id="1d8ca-665">2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-665">2017</span></span></td>
<td><span data-ttu-id="1d8ca-666">Periode 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-666">Period 1</span></span></td>
<td><span data-ttu-id="1d8ca-667">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="1d8ca-668">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d8ca-669">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-670">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-671">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-671">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-672">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-672">Cost behavior</span></span></th>
<th><span data-ttu-id="1d8ca-673">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-674">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-675">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-675">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-676">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-676">HR</span></span></td>
<td><span data-ttu-id="1d8ca-677">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-677">10001</span></span></td>
<td><span data-ttu-id="1d8ca-678">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-678">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-679">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-679">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-680">500,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-681">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-682">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-682">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-683">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-683">HR</span></span></td>
<td><span data-ttu-id="1d8ca-684">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-684">10001</span></span></td>
<td><span data-ttu-id="1d8ca-685">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-685">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-686">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-686">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-688">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-689">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-689">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-690">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-690">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-691">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-691">10001</span></span></td>
<td><span data-ttu-id="1d8ca-692">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-692">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-693">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-693">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-694">675.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-695">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-696">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-696">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-697">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-697">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-698">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-698">10001</span></span></td>
<td><span data-ttu-id="1d8ca-699">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-699">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-700">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-700">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="1d8ca-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-702">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-703">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-703">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-704">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-704">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-705">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-705">10001</span></span></td>
<td><span data-ttu-id="1d8ca-706">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-706">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-707">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-707">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-708">713.75</span><span class="sxs-lookup"><span data-stu-id="1d8ca-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-709">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-710">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-710">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-711">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-711">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-712">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-712">10001</span></span></td>
<td><span data-ttu-id="1d8ca-713">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-713">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-714">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-714">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="1d8ca-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-716">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-717">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-717">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-718">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-718">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-719">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-719">10001</span></span></td>
<td><span data-ttu-id="1d8ca-720">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-720">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-721">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-721">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-722">286.25</span><span class="sxs-lookup"><span data-stu-id="1d8ca-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-723">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-724">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-724">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-725">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-725">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-726">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-726">10001</span></span></td>
<td><span data-ttu-id="1d8ca-727">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-727">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-728">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-728">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="1d8ca-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-730">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-731">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-731">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-732">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-733">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-733">10001</span></span></td>
<td><span data-ttu-id="1d8ca-734">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-734">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-735">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-735">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-736">776.36</span><span class="sxs-lookup"><span data-stu-id="1d8ca-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-737">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-738">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-738">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-739">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-740">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-740">10001</span></span></td>
<td><span data-ttu-id="1d8ca-741">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-741">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-742">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-742">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="1d8ca-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-744">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-745">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-745">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-746">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-747">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-747">10001</span></span></td>
<td><span data-ttu-id="1d8ca-748">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-748">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-749">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-749">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-750">223.64</span><span class="sxs-lookup"><span data-stu-id="1d8ca-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-751">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="1d8ca-752">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-752">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-753">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-754">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-754">10001</span></span></td>
<td><span data-ttu-id="1d8ca-755">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-755">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-756">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-756">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="1d8ca-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1d8ca-758">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="1d8ca-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1d8ca-759">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1d8ca-760">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-760">Cost element</span></span></th>
<th><span data-ttu-id="1d8ca-761">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-761">Cost behavior</span></span></th>
<th><span data-ttu-id="1d8ca-762">Betrag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-762">Amount</span></span></th>
<th><span data-ttu-id="1d8ca-763">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="1d8ca-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d8ca-764">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-764">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-765">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-765">HR</span></span></td>
<td><span data-ttu-id="1d8ca-766">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-766">10001</span></span></td>
<td><span data-ttu-id="1d8ca-767">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-767">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-768">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-768">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-769">-500.00</span></span></td>
<td><span data-ttu-id="1d8ca-770">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-771">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-771">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-772">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-772">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-773">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-773">10001</span></span></td>
<td><span data-ttu-id="1d8ca-774">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-774">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-775">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-775">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-776">175.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-776">175.00</span></span></td>
<td><span data-ttu-id="1d8ca-777">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-778">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-778">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-779">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-779">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-780">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-780">10001</span></span></td>
<td><span data-ttu-id="1d8ca-781">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-781">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-782">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-782">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-783">275.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-783">275.00</span></span></td>
<td><span data-ttu-id="1d8ca-784">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-785">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-785">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-786">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-786">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-787">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-787">10001</span></span></td>
<td><span data-ttu-id="1d8ca-788">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-788">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-789">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-789">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-790">50,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-790">50,00</span></span></td>
<td><span data-ttu-id="1d8ca-791">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-792">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-792">CC001</span></span></td>
<td><span data-ttu-id="1d8ca-793">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-793">HR</span></span></td>
<td><span data-ttu-id="1d8ca-794">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-794">10001</span></span></td>
<td><span data-ttu-id="1d8ca-795">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-795">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-796">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-796">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-797">-1,245.71</span></span></td>
<td><span data-ttu-id="1d8ca-798">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-799">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-799">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-800">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-800">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-801">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-801">10001</span></span></td>
<td><span data-ttu-id="1d8ca-802">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-802">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-803">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-803">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-804">436.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-804">436.00</span></span></td>
<td><span data-ttu-id="1d8ca-805">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-806">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-806">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-807">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-807">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-808">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-808">10001</span></span></td>
<td><span data-ttu-id="1d8ca-809">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-809">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-810">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-810">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-811">685.14</span><span class="sxs-lookup"><span data-stu-id="1d8ca-811">685.14</span></span></td>
<td><span data-ttu-id="1d8ca-812">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-813">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-813">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-814">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-814">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-815">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-815">10001</span></span></td>
<td><span data-ttu-id="1d8ca-816">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-816">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-817">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-817">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-818">124.57</span><span class="sxs-lookup"><span data-stu-id="1d8ca-818">124.57</span></span></td>
<td><span data-ttu-id="1d8ca-819">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-820">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-820">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-821">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-821">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-822">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-822">10001</span></span></td>
<td><span data-ttu-id="1d8ca-823">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-823">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-824">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-824">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-825">-675.00</span></span></td>
<td><span data-ttu-id="1d8ca-826">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-827">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-827">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-828">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-828">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-829">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-829">10001</span></span></td>
<td><span data-ttu-id="1d8ca-830">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-830">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-831">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-831">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-832">438.75</span><span class="sxs-lookup"><span data-stu-id="1d8ca-832">438.75</span></span></td>
<td><span data-ttu-id="1d8ca-833">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-834">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-834">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-835">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-835">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-836">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-836">10001</span></span></td>
<td><span data-ttu-id="1d8ca-837">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-837">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-838">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-838">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-839">236.25</span><span class="sxs-lookup"><span data-stu-id="1d8ca-839">236.25</span></span></td>
<td><span data-ttu-id="1d8ca-840">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-841">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-841">CC002</span></span></td>
<td><span data-ttu-id="1d8ca-842">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1d8ca-842">Finance</span></span></td>
<td><span data-ttu-id="1d8ca-843">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-843">10001</span></span></td>
<td><span data-ttu-id="1d8ca-844">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-844">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-845">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-845">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="1d8ca-846">-8,150.29</span></span></td>
<td><span data-ttu-id="1d8ca-847">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-848">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-848">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-849">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-849">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-850">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-850">10001</span></span></td>
<td><span data-ttu-id="1d8ca-851">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-851">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-852">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-852">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="1d8ca-853">5,297.69</span></span></td>
<td><span data-ttu-id="1d8ca-854">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-855">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-855">CC004</span></span></td>
<td><span data-ttu-id="1d8ca-856">Verpackung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-856">Packaging</span></span></td>
<td><span data-ttu-id="1d8ca-857">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-857">10001</span></span></td>
<td><span data-ttu-id="1d8ca-858">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-858">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-859">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-859">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="1d8ca-860">2,852.60</span></span></td>
<td><span data-ttu-id="1d8ca-861">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-862">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-862">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-863">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-863">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-864">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-864">10001</span></span></td>
<td><span data-ttu-id="1d8ca-865">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-865">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-866">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-866">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="1d8ca-867">-713.75</span></span></td>
<td><span data-ttu-id="1d8ca-868">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-869">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-869">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-870">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-871">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-871">10001</span></span></td>
<td><span data-ttu-id="1d8ca-872">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-872">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-873">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-873">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-874">535.31</span><span class="sxs-lookup"><span data-stu-id="1d8ca-874">535.31</span></span></td>
<td><span data-ttu-id="1d8ca-875">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-876">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-876">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-877">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-878">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-878">10001</span></span></td>
<td><span data-ttu-id="1d8ca-879">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-879">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-880">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-880">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-881">178.44</span><span class="sxs-lookup"><span data-stu-id="1d8ca-881">178.44</span></span></td>
<td><span data-ttu-id="1d8ca-882">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-883">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-883">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-884">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-884">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-885">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-885">10001</span></span></td>
<td><span data-ttu-id="1d8ca-886">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-886">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-887">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-887">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="1d8ca-888">-5,982.83</span></span></td>
<td><span data-ttu-id="1d8ca-889">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-890">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-890">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-891">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-892">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-892">10001</span></span></td>
<td><span data-ttu-id="1d8ca-893">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-893">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-894">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-894">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="1d8ca-895">4,487.12</span></span></td>
<td><span data-ttu-id="1d8ca-896">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-897">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-897">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-898">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-899">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-899">10001</span></span></td>
<td><span data-ttu-id="1d8ca-900">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-900">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-901">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-901">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="1d8ca-902">1,495.71</span></span></td>
<td><span data-ttu-id="1d8ca-903">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-904">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-904">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-905">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-905">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-906">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-906">10001</span></span></td>
<td><span data-ttu-id="1d8ca-907">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-907">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-908">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-908">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="1d8ca-909">-286.25</span></span></td>
<td><span data-ttu-id="1d8ca-910">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-911">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-911">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-912">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-913">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-913">10001</span></span></td>
<td><span data-ttu-id="1d8ca-914">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-914">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-915">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-915">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-916">241.05</span><span class="sxs-lookup"><span data-stu-id="1d8ca-916">241.05</span></span></td>
<td><span data-ttu-id="1d8ca-917">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-918">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-918">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-919">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-920">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-920">10001</span></span></td>
<td><span data-ttu-id="1d8ca-921">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-921">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-922">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-922">Fixed cost</span></span></td>
<td><span data-ttu-id="1d8ca-923">45.20</span><span class="sxs-lookup"><span data-stu-id="1d8ca-923">45.20</span></span></td>
<td><span data-ttu-id="1d8ca-924">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-925">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-925">CC003</span></span></td>
<td><span data-ttu-id="1d8ca-926">Montage</span><span class="sxs-lookup"><span data-stu-id="1d8ca-926">Assembly</span></span></td>
<td><span data-ttu-id="1d8ca-927">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-927">10001</span></span></td>
<td><span data-ttu-id="1d8ca-928">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-928">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-929">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-929">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="1d8ca-930">-2,977.17</span></span></td>
<td><span data-ttu-id="1d8ca-931">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-932">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-932">Prod 1</span></span></td>
<td><span data-ttu-id="1d8ca-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-933">Product 1</span></span></td>
<td><span data-ttu-id="1d8ca-934">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-934">10001</span></span></td>
<td><span data-ttu-id="1d8ca-935">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-935">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-936">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-936">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="1d8ca-937">2,507.09</span></span></td>
<td><span data-ttu-id="1d8ca-938">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d8ca-939">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-939">Prod 2</span></span></td>
<td><span data-ttu-id="1d8ca-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-940">Product 2</span></span></td>
<td><span data-ttu-id="1d8ca-941">10001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-941">10001</span></span></td>
<td><span data-ttu-id="1d8ca-942">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-942">Electricity</span></span></td>
<td><span data-ttu-id="1d8ca-943">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-943">Variable cost</span></span></td>
<td><span data-ttu-id="1d8ca-944">470.08</span><span class="sxs-lookup"><span data-stu-id="1d8ca-944">470.08</span></span></td>
<td><span data-ttu-id="1d8ca-945">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="1d8ca-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="1d8ca-946">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="1d8ca-946">Conclusion</span></span>
<span data-ttu-id="1d8ca-947">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="1d8ca-948">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="1d8ca-949">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="1d8ca-950">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="1d8ca-951">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1d8ca-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="1d8ca-952">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="1d8ca-953">Gesamt</span><span class="sxs-lookup"><span data-stu-id="1d8ca-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1d8ca-954">CC099</span><span class="sxs-lookup"><span data-stu-id="1d8ca-954">CC099</span></span></th>
<th><span data-ttu-id="1d8ca-955">CC001</span><span class="sxs-lookup"><span data-stu-id="1d8ca-955">CC001</span></span></th>
<th><span data-ttu-id="1d8ca-956">CC002</span><span class="sxs-lookup"><span data-stu-id="1d8ca-956">CC002</span></span></th>
<th><span data-ttu-id="1d8ca-957">CC003</span><span class="sxs-lookup"><span data-stu-id="1d8ca-957">CC003</span></span></th>
<th><span data-ttu-id="1d8ca-958">CC004</span><span class="sxs-lookup"><span data-stu-id="1d8ca-958">CC004</span></span></th>
<th><span data-ttu-id="1d8ca-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-959">Proj 1</span></span></th>
<th><span data-ttu-id="1d8ca-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-960">Proj 2</span></span></th>
<th><span data-ttu-id="1d8ca-961">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="1d8ca-961">Prod 1</span></span></th>
<th><span data-ttu-id="1d8ca-962">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="1d8ca-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="1d8ca-963">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="1d8ca-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="1d8ca-973">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="1d8ca-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-974">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="1d8ca-975">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-976">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-977">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-978">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-979">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-980">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-981">776.36</span><span class="sxs-lookup"><span data-stu-id="1d8ca-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-982">223.64</span><span class="sxs-lookup"><span data-stu-id="1d8ca-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="1d8ca-984">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="1d8ca-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-985">000</span><span class="sxs-lookup"><span data-stu-id="1d8ca-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-986">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-987">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-988">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-989">0,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-990">30,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-991">10,00</span><span class="sxs-lookup"><span data-stu-id="1d8ca-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="1d8ca-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="1d8ca-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1d8ca-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1d8ca-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1d8ca-995">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="1d8ca-996">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="1d8ca-997">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="1d8ca-998">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="1d8ca-999">Für ausführlichere Informationen gehen Sie zur Richtlinie Kostenzusammenfassung.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="1d8ca-1000">(Beachten Sie, dass dieses Thema noch nicht abgedeckt ist, aber bald verfügbar sein wird.)</span><span class="sxs-lookup"><span data-stu-id="1d8ca-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




