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
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770803"
---
# <a name="overhead-calculation"></a><span data-ttu-id="5a0f6-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a0f6-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="5a0f6-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="5a0f6-105">Term definition</span></span>
---------------

<span data-ttu-id="5a0f6-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5a0f6-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5a0f6-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="5a0f6-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5a0f6-109">Miete</span><span class="sxs-lookup"><span data-stu-id="5a0f6-109">Rent</span></span>
-   <span data-ttu-id="5a0f6-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-110">Electricity</span></span>
-   <span data-ttu-id="5a0f6-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="5a0f6-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5a0f6-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="5a0f6-112">Overhead calculation overview</span></span>
<span data-ttu-id="5a0f6-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5a0f6-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5a0f6-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5a0f6-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5a0f6-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5a0f6-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="5a0f6-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5a0f6-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="5a0f6-119">Version type</span></span>
-   <span data-ttu-id="5a0f6-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="5a0f6-120">Date and time</span></span>
-   <span data-ttu-id="5a0f6-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="5a0f6-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5a0f6-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="5a0f6-122">Fiscal year</span></span>
-   <span data-ttu-id="5a0f6-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="5a0f6-123">Fiscal period</span></span>

<span data-ttu-id="5a0f6-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5a0f6-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5a0f6-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5a0f6-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5a0f6-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5a0f6-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5a0f6-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5a0f6-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5a0f6-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="5a0f6-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5a0f6-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5a0f6-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5a0f6-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5a0f6-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5a0f6-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="5a0f6-140">Main account</span></span></th>
<th><span data-ttu-id="5a0f6-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-143">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-144">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-145">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-145">10001</span></span></td>
<td><span data-ttu-id="5a0f6-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-146">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5a0f6-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5a0f6-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5a0f6-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5a0f6-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="5a0f6-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5a0f6-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5a0f6-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5a0f6-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5a0f6-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="5a0f6-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5a0f6-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5a0f6-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="5a0f6-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5a0f6-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="5a0f6-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5a0f6-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-160">Journal</span></span></th>
<th><span data-ttu-id="5a0f6-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="5a0f6-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5a0f6-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5a0f6-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5a0f6-163">Version</span><span class="sxs-lookup"><span data-stu-id="5a0f6-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-164">00001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-164">00001</span></span></td>
<td><span data-ttu-id="5a0f6-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5a0f6-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5a0f6-166">Fiscal</span></span></td>
<td><span data-ttu-id="5a0f6-167">2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-167">2017</span></span></td>
<td><span data-ttu-id="5a0f6-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-168">Period 1</span></span></td>
<td><span data-ttu-id="5a0f6-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5a0f6-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-173">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5a0f6-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-177">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-178">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-179">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-179">10001</span></span></td>
<td><span data-ttu-id="5a0f6-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-180">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="5a0f6-181">Unclassified</span></span></td>
<td><span data-ttu-id="5a0f6-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5a0f6-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="5a0f6-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-185">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5a0f6-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-187">Amount</span></span></th>
<th><span data-ttu-id="5a0f6-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-189">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-190">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-191">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-191">10001</span></span></td>
<td><span data-ttu-id="5a0f6-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-192">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="5a0f6-193">Unclassified</span></span></td>
<td><span data-ttu-id="5a0f6-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-194">10,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-196">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-197">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-198">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-198">10001</span></span></td>
<td><span data-ttu-id="5a0f6-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-199">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="5a0f6-200">Unclassified</span></span></td>
<td><span data-ttu-id="5a0f6-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-203">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-204">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-205">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-205">10001</span></span></td>
<td><span data-ttu-id="5a0f6-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-206">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-208">1,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-210">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-211">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-212">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-212">10001</span></span></td>
<td><span data-ttu-id="5a0f6-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-213">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-214">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-215">9,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5a0f6-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5a0f6-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5a0f6-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5a0f6-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="5a0f6-221">Define the cost distribution rule</span></span>

<span data-ttu-id="5a0f6-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5a0f6-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5a0f6-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5a0f6-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5a0f6-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5a0f6-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-228">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-229">KWH</span><span class="sxs-lookup"><span data-stu-id="5a0f6-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-230">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-230">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-231">HR</span></span></td>
<td><span data-ttu-id="5a0f6-232">1.000</span><span class="sxs-lookup"><span data-stu-id="5a0f6-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-233">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-233">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-234">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-235">6.000</span><span class="sxs-lookup"><span data-stu-id="5a0f6-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-236">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-236">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-237">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-237">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-238">0</span><span class="sxs-lookup"><span data-stu-id="5a0f6-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-240">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-241">Größe</span><span class="sxs-lookup"><span data-stu-id="5a0f6-241">Magnitude</span></span></th>
<th><span data-ttu-id="5a0f6-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5a0f6-242">Allocation factor</span></span></th>
<th><span data-ttu-id="5a0f6-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-244">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-244">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-245">HR</span></span></td>
<td><span data-ttu-id="5a0f6-246">1.000</span><span class="sxs-lookup"><span data-stu-id="5a0f6-246">1,000</span></span></td>
<td><span data-ttu-id="5a0f6-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-249">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-249">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-250">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-251">6.000</span><span class="sxs-lookup"><span data-stu-id="5a0f6-251">6,000</span></span></td>
<td><span data-ttu-id="5a0f6-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5a0f6-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-254">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-254">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-255">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-255">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-256">0</span><span class="sxs-lookup"><span data-stu-id="5a0f6-256">0</span></span></td>
<td><span data-ttu-id="5a0f6-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-258">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5a0f6-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-261">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-262">Formula</span></span></th>
<th><span data-ttu-id="5a0f6-263">Größe</span><span class="sxs-lookup"><span data-stu-id="5a0f6-263">Magnitude</span></span></th>
<th><span data-ttu-id="5a0f6-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5a0f6-264">Allocation factor</span></span></th>
<th><span data-ttu-id="5a0f6-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-266">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-266">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-267">HR</span></span></td>
<td><span data-ttu-id="5a0f6-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5a0f6-269">1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-269">1</span></span></td>
<td><span data-ttu-id="5a0f6-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-271">500,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-272">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-272">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-273">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5a0f6-275">1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-275">1</span></span></td>
<td><span data-ttu-id="5a0f6-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-277">500,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-278">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-278">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-279">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-279">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5a0f6-281">0</span><span class="sxs-lookup"><span data-stu-id="5a0f6-281">0</span></span></td>
<td><span data-ttu-id="5a0f6-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5a0f6-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-285">Journal</span></span></th>
<th><span data-ttu-id="5a0f6-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="5a0f6-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5a0f6-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5a0f6-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5a0f6-288">Version</span><span class="sxs-lookup"><span data-stu-id="5a0f6-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-289">00002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-289">00002</span></span></td>
<td><span data-ttu-id="5a0f6-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5a0f6-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5a0f6-291">Fiscal</span></span></td>
<td><span data-ttu-id="5a0f6-292">2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-292">2017</span></span></td>
<td><span data-ttu-id="5a0f6-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-293">Period 1</span></span></td>
<td><span data-ttu-id="5a0f6-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5a0f6-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-298">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-299">Cost behavior</span></span></th>
<th><span data-ttu-id="5a0f6-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-302">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-302">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-303">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-304">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-304">10001</span></span></td>
<td><span data-ttu-id="5a0f6-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-305">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-306">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-309">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-309">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-310">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-311">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-311">10001</span></span></td>
<td><span data-ttu-id="5a0f6-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-312">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-313">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5a0f6-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="5a0f6-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-317">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-318">Cost behavior</span></span></th>
<th><span data-ttu-id="5a0f6-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-319">Amount</span></span></th>
<th><span data-ttu-id="5a0f6-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-321">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-321">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-322">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-323">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-323">10001</span></span></td>
<td><span data-ttu-id="5a0f6-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-324">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-325">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-326">-1,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-328">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-328">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-329">HR</span></span></td>
<td><span data-ttu-id="5a0f6-330">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-330">10001</span></span></td>
<td><span data-ttu-id="5a0f6-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-331">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-332">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-333">500,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-333">500.00</span></span></td>
<td><span data-ttu-id="5a0f6-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-335">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-335">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-336">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-337">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-337">10001</span></span></td>
<td><span data-ttu-id="5a0f6-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-338">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-339">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-340">500,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-340">500.00</span></span></td>
<td><span data-ttu-id="5a0f6-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-342">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-342">CC099</span></span></td>
<td><span data-ttu-id="5a0f6-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="5a0f6-343">Default cost center</span></span></td>
<td><span data-ttu-id="5a0f6-344">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-344">10001</span></span></td>
<td><span data-ttu-id="5a0f6-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-345">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-346">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-347">-9,000.00</span></span></td>
<td><span data-ttu-id="5a0f6-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-349">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-349">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-350">HR</span></span></td>
<td><span data-ttu-id="5a0f6-351">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-351">10001</span></span></td>
<td><span data-ttu-id="5a0f6-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-352">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-353">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-354">1,285.71</span></span></td>
<td><span data-ttu-id="5a0f6-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-356">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-356">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-357">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-358">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-358">10001</span></span></td>
<td><span data-ttu-id="5a0f6-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-359">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-360">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5a0f6-361">7,714.29</span></span></td>
<td><span data-ttu-id="5a0f6-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5a0f6-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5a0f6-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5a0f6-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5a0f6-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="5a0f6-367">Define the overhead rate</span></span>

<span data-ttu-id="5a0f6-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5a0f6-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-370">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="5a0f6-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-372">Proj 1</span></span></td>
<td><span data-ttu-id="5a0f6-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-373">Project 1</span></span></td>
<td><span data-ttu-id="5a0f6-374">3</span><span class="sxs-lookup"><span data-stu-id="5a0f6-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-375">Proj 2</span></span></td>
<td><span data-ttu-id="5a0f6-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-376">Project 2</span></span></td>
<td><span data-ttu-id="5a0f6-377">1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-379">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-380">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-381">Cost behavior</span></span></th>
<th><span data-ttu-id="5a0f6-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-382">Units</span></span></th>
<th><span data-ttu-id="5a0f6-383">Satz</span><span class="sxs-lookup"><span data-stu-id="5a0f6-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-384">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-384">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-385">HR</span></span></td>
<td><span data-ttu-id="5a0f6-386">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-386">10001</span></span></td>
<td><span data-ttu-id="5a0f6-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-387">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-388">1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-388">1</span></span></td>
<td><span data-ttu-id="5a0f6-389">10</span><span class="sxs-lookup"><span data-stu-id="5a0f6-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-391">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-392">Größe</span><span class="sxs-lookup"><span data-stu-id="5a0f6-392">Magnitude</span></span></th>
<th><span data-ttu-id="5a0f6-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-393">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5a0f6-394">Allocation factor</span></span></th>
<th><span data-ttu-id="5a0f6-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-396">Proj 1</span></span></td>
<td><span data-ttu-id="5a0f6-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-397">Project 1</span></span></td>
<td><span data-ttu-id="5a0f6-398">3</span><span class="sxs-lookup"><span data-stu-id="5a0f6-398">3</span></span></td>
<td><span data-ttu-id="5a0f6-399">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-399">10001</span></span></td>
<td><span data-ttu-id="5a0f6-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5a0f6-401">30,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-402">Proj 2</span></span></td>
<td><span data-ttu-id="5a0f6-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-403">Project 2</span></span></td>
<td><span data-ttu-id="5a0f6-404">1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-404">1</span></span></td>
<td><span data-ttu-id="5a0f6-405">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-405">10001</span></span></td>
<td><span data-ttu-id="5a0f6-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5a0f6-407">10,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5a0f6-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-409">Journal</span></span></th>
<th><span data-ttu-id="5a0f6-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="5a0f6-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5a0f6-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5a0f6-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5a0f6-412">Version</span><span class="sxs-lookup"><span data-stu-id="5a0f6-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-413">00003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-413">00003</span></span></td>
<td><span data-ttu-id="5a0f6-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5a0f6-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5a0f6-415">Fiscal</span></span></td>
<td><span data-ttu-id="5a0f6-416">2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-416">2017</span></span></td>
<td><span data-ttu-id="5a0f6-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-417">Period 1</span></span></td>
<td><span data-ttu-id="5a0f6-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5a0f6-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-421">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-422">Größe</span><span class="sxs-lookup"><span data-stu-id="5a0f6-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-424">Proj 1</span></span></td>
<td><span data-ttu-id="5a0f6-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5a0f6-426">3,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-428">Proj 2</span></span></td>
<td><span data-ttu-id="5a0f6-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5a0f6-430">1,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5a0f6-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="5a0f6-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-433">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-434">Cost behavior</span></span></th>
<th><span data-ttu-id="5a0f6-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-435">Amount</span></span></th>
<th><span data-ttu-id="5a0f6-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-437">CC0001</span></span></td>
<td><span data-ttu-id="5a0f6-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-438">HR</span></span></td>
<td><span data-ttu-id="5a0f6-439">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-439">10001</span></span></td>
<td><span data-ttu-id="5a0f6-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-440">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-441">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-442">-30.00</span></span></td>
<td><span data-ttu-id="5a0f6-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-444">Proj 1</span></span></td>
<td><span data-ttu-id="5a0f6-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5a0f6-446">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-446">10001</span></span></td>
<td><span data-ttu-id="5a0f6-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-447">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-448">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-449">30,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-449">30.00</span></span></td>
<td><span data-ttu-id="5a0f6-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-451">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-451">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-452">HR</span></span></td>
<td><span data-ttu-id="5a0f6-453">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-453">10001</span></span></td>
<td><span data-ttu-id="5a0f6-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-454">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-455">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-456">-10.00</span></span></td>
<td><span data-ttu-id="5a0f6-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-458">Proj 2</span></span></td>
<td><span data-ttu-id="5a0f6-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5a0f6-460">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-460">10001</span></span></td>
<td><span data-ttu-id="5a0f6-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-461">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-462">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-463">10.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-463">10.00</span></span></td>
<td><span data-ttu-id="5a0f6-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5a0f6-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5a0f6-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5a0f6-468">Finance unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="5a0f6-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5a0f6-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5a0f6-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5a0f6-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5a0f6-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5a0f6-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5a0f6-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="5a0f6-475">Define the cost allocation</span></span>

<span data-ttu-id="5a0f6-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5a0f6-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5a0f6-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-479">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="5a0f6-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-481">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-481">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-482">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-483">35</span><span class="sxs-lookup"><span data-stu-id="5a0f6-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-484">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-484">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-485">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-485">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-486">55</span><span class="sxs-lookup"><span data-stu-id="5a0f6-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-487">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-487">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-488">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-489">10</span><span class="sxs-lookup"><span data-stu-id="5a0f6-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5a0f6-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-492">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="5a0f6-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-494">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-494">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-495">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-495">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-496">65</span><span class="sxs-lookup"><span data-stu-id="5a0f6-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-497">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-497">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-498">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-499">35</span><span class="sxs-lookup"><span data-stu-id="5a0f6-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5a0f6-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-502">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-504">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-505">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-506">60</span><span class="sxs-lookup"><span data-stu-id="5a0f6-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-507">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-508">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-509">20</span><span class="sxs-lookup"><span data-stu-id="5a0f6-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5a0f6-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-512">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-514">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-515">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-516">80</span><span class="sxs-lookup"><span data-stu-id="5a0f6-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-517">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-518">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-519">15</span><span class="sxs-lookup"><span data-stu-id="5a0f6-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5a0f6-520">Statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, können von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5a0f6-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="5a0f6-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-523">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-524">Größe</span><span class="sxs-lookup"><span data-stu-id="5a0f6-524">Magnitude</span></span></th>
<th><span data-ttu-id="5a0f6-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5a0f6-525">Allocation factor</span></span></th>
<th><span data-ttu-id="5a0f6-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-526">Amount</span></span></th>
<th><span data-ttu-id="5a0f6-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-528">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-528">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-529">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-530">35</span><span class="sxs-lookup"><span data-stu-id="5a0f6-530">35</span></span></td>
<td><span data-ttu-id="5a0f6-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5a0f6-532">175.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-532">175.00</span></span></td>
<td><span data-ttu-id="5a0f6-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-534">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-534">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-535">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-535">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-536">55</span><span class="sxs-lookup"><span data-stu-id="5a0f6-536">55</span></span></td>
<td><span data-ttu-id="5a0f6-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5a0f6-538">275.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-538">275.00</span></span></td>
<td><span data-ttu-id="5a0f6-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-540">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-540">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-541">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-542">10</span><span class="sxs-lookup"><span data-stu-id="5a0f6-542">10</span></span></td>
<td><span data-ttu-id="5a0f6-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5a0f6-544">50,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-544">50.00</span></span></td>
<td><span data-ttu-id="5a0f6-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-546">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-546">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-547">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-548">35</span><span class="sxs-lookup"><span data-stu-id="5a0f6-548">35</span></span></td>
<td><span data-ttu-id="5a0f6-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5a0f6-550">436.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-550">436.00</span></span></td>
<td><span data-ttu-id="5a0f6-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-552">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-552">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-553">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-553">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-554">55</span><span class="sxs-lookup"><span data-stu-id="5a0f6-554">55</span></span></td>
<td><span data-ttu-id="5a0f6-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5a0f6-556">685.14</span><span class="sxs-lookup"><span data-stu-id="5a0f6-556">685.14</span></span></td>
<td><span data-ttu-id="5a0f6-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-558">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-558">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-559">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-560">10</span><span class="sxs-lookup"><span data-stu-id="5a0f6-560">10</span></span></td>
<td><span data-ttu-id="5a0f6-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5a0f6-562">124.57</span><span class="sxs-lookup"><span data-stu-id="5a0f6-562">124.57</span></span></td>
<td><span data-ttu-id="5a0f6-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-565">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-566">Größe</span><span class="sxs-lookup"><span data-stu-id="5a0f6-566">Magnitude</span></span></th>
<th><span data-ttu-id="5a0f6-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5a0f6-567">Allocation factor</span></span></th>
<th><span data-ttu-id="5a0f6-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-568">Amount</span></span></th>
<th><span data-ttu-id="5a0f6-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-570">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-570">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-571">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-571">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-572">65</span><span class="sxs-lookup"><span data-stu-id="5a0f6-572">65</span></span></td>
<td><span data-ttu-id="5a0f6-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5a0f6-574">438.75</span><span class="sxs-lookup"><span data-stu-id="5a0f6-574">438.75</span></span></td>
<td><span data-ttu-id="5a0f6-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-576">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-576">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-577">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-578">35</span><span class="sxs-lookup"><span data-stu-id="5a0f6-578">35</span></span></td>
<td><span data-ttu-id="5a0f6-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5a0f6-580">236.25</span><span class="sxs-lookup"><span data-stu-id="5a0f6-580">236.25</span></span></td>
<td><span data-ttu-id="5a0f6-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-582">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-582">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-583">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-583">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-584">65</span><span class="sxs-lookup"><span data-stu-id="5a0f6-584">65</span></span></td>
<td><span data-ttu-id="5a0f6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5a0f6-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5a0f6-586">5,297.69</span></span></td>
<td><span data-ttu-id="5a0f6-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-588">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-588">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-589">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-590">35</span><span class="sxs-lookup"><span data-stu-id="5a0f6-590">35</span></span></td>
<td><span data-ttu-id="5a0f6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5a0f6-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5a0f6-592">2,852.60</span></span></td>
<td><span data-ttu-id="5a0f6-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-595">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-596">Größe</span><span class="sxs-lookup"><span data-stu-id="5a0f6-596">Magnitude</span></span></th>
<th><span data-ttu-id="5a0f6-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5a0f6-597">Allocation factor</span></span></th>
<th><span data-ttu-id="5a0f6-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-598">Amount</span></span></th>
<th><span data-ttu-id="5a0f6-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-600">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-601">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-602">60</span><span class="sxs-lookup"><span data-stu-id="5a0f6-602">60</span></span></td>
<td><span data-ttu-id="5a0f6-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5a0f6-604">535.31</span><span class="sxs-lookup"><span data-stu-id="5a0f6-604">535.31</span></span></td>
<td><span data-ttu-id="5a0f6-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-606">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-607">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-608">20</span><span class="sxs-lookup"><span data-stu-id="5a0f6-608">20</span></span></td>
<td><span data-ttu-id="5a0f6-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5a0f6-610">178.44</span><span class="sxs-lookup"><span data-stu-id="5a0f6-610">178.44</span></span></td>
<td><span data-ttu-id="5a0f6-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-612">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-613">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-614">60</span><span class="sxs-lookup"><span data-stu-id="5a0f6-614">60</span></span></td>
<td><span data-ttu-id="5a0f6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5a0f6-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5a0f6-616">4,487.12</span></span></td>
<td><span data-ttu-id="5a0f6-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-618">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-619">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-620">20</span><span class="sxs-lookup"><span data-stu-id="5a0f6-620">20</span></span></td>
<td><span data-ttu-id="5a0f6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5a0f6-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-622">1,495.71</span></span></td>
<td><span data-ttu-id="5a0f6-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a0f6-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-625">Cost object</span></span></th>
<th><span data-ttu-id="5a0f6-626">Größe</span><span class="sxs-lookup"><span data-stu-id="5a0f6-626">Magnitude</span></span></th>
<th><span data-ttu-id="5a0f6-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="5a0f6-627">Allocation factor</span></span></th>
<th><span data-ttu-id="5a0f6-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-628">Amount</span></span></th>
<th><span data-ttu-id="5a0f6-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-630">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-631">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-632">80</span><span class="sxs-lookup"><span data-stu-id="5a0f6-632">80</span></span></td>
<td><span data-ttu-id="5a0f6-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5a0f6-634">241.05</span><span class="sxs-lookup"><span data-stu-id="5a0f6-634">241.05</span></span></td>
<td><span data-ttu-id="5a0f6-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-636">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-637">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-638">15</span><span class="sxs-lookup"><span data-stu-id="5a0f6-638">15</span></span></td>
<td><span data-ttu-id="5a0f6-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5a0f6-640">45.20</span><span class="sxs-lookup"><span data-stu-id="5a0f6-640">45.20</span></span></td>
<td><span data-ttu-id="5a0f6-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-642">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-643">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-644">80</span><span class="sxs-lookup"><span data-stu-id="5a0f6-644">80</span></span></td>
<td><span data-ttu-id="5a0f6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5a0f6-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5a0f6-646">2,507.09</span></span></td>
<td><span data-ttu-id="5a0f6-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-648">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-649">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-650">15</span><span class="sxs-lookup"><span data-stu-id="5a0f6-650">15</span></span></td>
<td><span data-ttu-id="5a0f6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5a0f6-652">470.08</span><span class="sxs-lookup"><span data-stu-id="5a0f6-652">470.08</span></span></td>
<td><span data-ttu-id="5a0f6-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5a0f6-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="5a0f6-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-655">Journal</span></span></th>
<th><span data-ttu-id="5a0f6-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="5a0f6-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5a0f6-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5a0f6-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5a0f6-658">Version</span><span class="sxs-lookup"><span data-stu-id="5a0f6-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-659">00004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-659">00004</span></span></td>
<td><span data-ttu-id="5a0f6-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5a0f6-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="5a0f6-661">Fiscal</span></span></td>
<td><span data-ttu-id="5a0f6-662">2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-662">2017</span></span></td>
<td><span data-ttu-id="5a0f6-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-663">Period 1</span></span></td>
<td><span data-ttu-id="5a0f6-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5a0f6-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5a0f6-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-668">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-669">Cost behavior</span></span></th>
<th><span data-ttu-id="5a0f6-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-672">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-672">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-673">HR</span></span></td>
<td><span data-ttu-id="5a0f6-674">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-674">10001</span></span></td>
<td><span data-ttu-id="5a0f6-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-675">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-676">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-677">500,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-679">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-679">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-680">HR</span></span></td>
<td><span data-ttu-id="5a0f6-681">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-681">10001</span></span></td>
<td><span data-ttu-id="5a0f6-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-682">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-683">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-686">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-686">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-687">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-688">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-688">10001</span></span></td>
<td><span data-ttu-id="5a0f6-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-689">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-690">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-691">675.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-693">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-693">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-694">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-695">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-695">10001</span></span></td>
<td><span data-ttu-id="5a0f6-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-696">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-697">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5a0f6-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-700">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-700">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-701">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-701">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-702">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-702">10001</span></span></td>
<td><span data-ttu-id="5a0f6-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-703">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-704">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-705">713.75</span><span class="sxs-lookup"><span data-stu-id="5a0f6-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-707">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-707">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-708">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-708">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-709">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-709">10001</span></span></td>
<td><span data-ttu-id="5a0f6-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-710">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-711">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5a0f6-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-714">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-714">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-715">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-716">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-716">10001</span></span></td>
<td><span data-ttu-id="5a0f6-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-717">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-718">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-719">286.25</span><span class="sxs-lookup"><span data-stu-id="5a0f6-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-721">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-721">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-722">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-723">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-723">10001</span></span></td>
<td><span data-ttu-id="5a0f6-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-724">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-725">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5a0f6-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-728">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-729">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-730">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-730">10001</span></span></td>
<td><span data-ttu-id="5a0f6-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-731">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-732">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-733">776.36</span><span class="sxs-lookup"><span data-stu-id="5a0f6-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-735">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-736">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-737">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-737">10001</span></span></td>
<td><span data-ttu-id="5a0f6-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-738">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-739">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5a0f6-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-742">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-743">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-744">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-744">10001</span></span></td>
<td><span data-ttu-id="5a0f6-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-745">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-746">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-747">223.64</span><span class="sxs-lookup"><span data-stu-id="5a0f6-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="5a0f6-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-749">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-750">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-751">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-751">10001</span></span></td>
<td><span data-ttu-id="5a0f6-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-752">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-753">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5a0f6-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5a0f6-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="5a0f6-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5a0f6-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5a0f6-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-757">Cost element</span></span></th>
<th><span data-ttu-id="5a0f6-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-758">Cost behavior</span></span></th>
<th><span data-ttu-id="5a0f6-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-759">Amount</span></span></th>
<th><span data-ttu-id="5a0f6-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="5a0f6-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5a0f6-761">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-761">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-762">HR</span></span></td>
<td><span data-ttu-id="5a0f6-763">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-763">10001</span></span></td>
<td><span data-ttu-id="5a0f6-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-764">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-765">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-766">-500.00</span></span></td>
<td><span data-ttu-id="5a0f6-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-768">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-768">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-769">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-770">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-770">10001</span></span></td>
<td><span data-ttu-id="5a0f6-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-771">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-772">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-773">175.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-773">175.00</span></span></td>
<td><span data-ttu-id="5a0f6-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-775">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-775">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-776">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-776">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-777">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-777">10001</span></span></td>
<td><span data-ttu-id="5a0f6-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-778">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-779">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-780">275.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-780">275.00</span></span></td>
<td><span data-ttu-id="5a0f6-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-782">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-782">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-783">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-784">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-784">10001</span></span></td>
<td><span data-ttu-id="5a0f6-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-785">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-786">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-787">50,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-787">50,00</span></span></td>
<td><span data-ttu-id="5a0f6-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-789">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-789">CC001</span></span></td>
<td><span data-ttu-id="5a0f6-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-790">HR</span></span></td>
<td><span data-ttu-id="5a0f6-791">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-791">10001</span></span></td>
<td><span data-ttu-id="5a0f6-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-792">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-793">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-794">-1,245.71</span></span></td>
<td><span data-ttu-id="5a0f6-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-796">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-796">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-797">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-798">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-798">10001</span></span></td>
<td><span data-ttu-id="5a0f6-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-799">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-800">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-801">436.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-801">436.00</span></span></td>
<td><span data-ttu-id="5a0f6-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-803">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-803">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-804">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-804">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-805">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-805">10001</span></span></td>
<td><span data-ttu-id="5a0f6-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-806">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-807">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-808">685.14</span><span class="sxs-lookup"><span data-stu-id="5a0f6-808">685.14</span></span></td>
<td><span data-ttu-id="5a0f6-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-810">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-810">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-811">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-812">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-812">10001</span></span></td>
<td><span data-ttu-id="5a0f6-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-813">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-814">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-815">124.57</span><span class="sxs-lookup"><span data-stu-id="5a0f6-815">124.57</span></span></td>
<td><span data-ttu-id="5a0f6-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-817">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-817">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-818">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-819">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-819">10001</span></span></td>
<td><span data-ttu-id="5a0f6-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-820">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-821">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-822">-675.00</span></span></td>
<td><span data-ttu-id="5a0f6-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-824">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-824">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-825">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-825">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-826">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-826">10001</span></span></td>
<td><span data-ttu-id="5a0f6-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-827">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-828">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-829">438.75</span><span class="sxs-lookup"><span data-stu-id="5a0f6-829">438.75</span></span></td>
<td><span data-ttu-id="5a0f6-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-831">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-831">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-832">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-833">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-833">10001</span></span></td>
<td><span data-ttu-id="5a0f6-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-834">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-835">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-836">236.25</span><span class="sxs-lookup"><span data-stu-id="5a0f6-836">236.25</span></span></td>
<td><span data-ttu-id="5a0f6-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-838">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-838">CC002</span></span></td>
<td><span data-ttu-id="5a0f6-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5a0f6-839">Finance</span></span></td>
<td><span data-ttu-id="5a0f6-840">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-840">10001</span></span></td>
<td><span data-ttu-id="5a0f6-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-841">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-842">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="5a0f6-843">-8,150.29</span></span></td>
<td><span data-ttu-id="5a0f6-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-845">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-845">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-846">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-846">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-847">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-847">10001</span></span></td>
<td><span data-ttu-id="5a0f6-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-848">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-849">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5a0f6-850">5,297.69</span></span></td>
<td><span data-ttu-id="5a0f6-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-852">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-852">CC004</span></span></td>
<td><span data-ttu-id="5a0f6-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-853">Packaging</span></span></td>
<td><span data-ttu-id="5a0f6-854">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-854">10001</span></span></td>
<td><span data-ttu-id="5a0f6-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-855">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-856">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5a0f6-857">2,852.60</span></span></td>
<td><span data-ttu-id="5a0f6-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-859">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-859">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-860">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-860">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-861">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-861">10001</span></span></td>
<td><span data-ttu-id="5a0f6-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-862">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-863">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="5a0f6-864">-713.75</span></span></td>
<td><span data-ttu-id="5a0f6-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-866">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-867">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-868">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-868">10001</span></span></td>
<td><span data-ttu-id="5a0f6-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-869">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-870">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-871">535.31</span><span class="sxs-lookup"><span data-stu-id="5a0f6-871">535.31</span></span></td>
<td><span data-ttu-id="5a0f6-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-873">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-874">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-875">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-875">10001</span></span></td>
<td><span data-ttu-id="5a0f6-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-876">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-877">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-878">178.44</span><span class="sxs-lookup"><span data-stu-id="5a0f6-878">178.44</span></span></td>
<td><span data-ttu-id="5a0f6-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-880">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-880">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-881">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-881">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-882">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-882">10001</span></span></td>
<td><span data-ttu-id="5a0f6-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-883">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-884">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="5a0f6-885">-5,982.83</span></span></td>
<td><span data-ttu-id="5a0f6-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-887">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-888">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-889">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-889">10001</span></span></td>
<td><span data-ttu-id="5a0f6-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-890">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-891">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5a0f6-892">4,487.12</span></span></td>
<td><span data-ttu-id="5a0f6-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-894">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-895">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-896">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-896">10001</span></span></td>
<td><span data-ttu-id="5a0f6-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-897">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-898">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5a0f6-899">1,495.71</span></span></td>
<td><span data-ttu-id="5a0f6-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-901">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-901">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-902">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-902">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-903">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-903">10001</span></span></td>
<td><span data-ttu-id="5a0f6-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-904">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-905">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="5a0f6-906">-286.25</span></span></td>
<td><span data-ttu-id="5a0f6-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-908">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-909">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-910">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-910">10001</span></span></td>
<td><span data-ttu-id="5a0f6-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-911">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-912">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-913">241.05</span><span class="sxs-lookup"><span data-stu-id="5a0f6-913">241.05</span></span></td>
<td><span data-ttu-id="5a0f6-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-915">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-916">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-917">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-917">10001</span></span></td>
<td><span data-ttu-id="5a0f6-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-918">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-919">Fixed cost</span></span></td>
<td><span data-ttu-id="5a0f6-920">45.20</span><span class="sxs-lookup"><span data-stu-id="5a0f6-920">45.20</span></span></td>
<td><span data-ttu-id="5a0f6-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-922">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-922">CC003</span></span></td>
<td><span data-ttu-id="5a0f6-923">Montage</span><span class="sxs-lookup"><span data-stu-id="5a0f6-923">Assembly</span></span></td>
<td><span data-ttu-id="5a0f6-924">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-924">10001</span></span></td>
<td><span data-ttu-id="5a0f6-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-925">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-926">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="5a0f6-927">-2,977.17</span></span></td>
<td><span data-ttu-id="5a0f6-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-929">Prod 1</span></span></td>
<td><span data-ttu-id="5a0f6-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-930">Product 1</span></span></td>
<td><span data-ttu-id="5a0f6-931">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-931">10001</span></span></td>
<td><span data-ttu-id="5a0f6-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-932">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-933">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5a0f6-934">2,507.09</span></span></td>
<td><span data-ttu-id="5a0f6-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5a0f6-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-936">Prod 2</span></span></td>
<td><span data-ttu-id="5a0f6-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-937">Product 2</span></span></td>
<td><span data-ttu-id="5a0f6-938">10001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-938">10001</span></span></td>
<td><span data-ttu-id="5a0f6-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-939">Electricity</span></span></td>
<td><span data-ttu-id="5a0f6-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-940">Variable cost</span></span></td>
<td><span data-ttu-id="5a0f6-941">470.08</span><span class="sxs-lookup"><span data-stu-id="5a0f6-941">470.08</span></span></td>
<td><span data-ttu-id="5a0f6-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="5a0f6-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5a0f6-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="5a0f6-943">Conclusion</span></span>
<span data-ttu-id="5a0f6-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5a0f6-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5a0f6-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5a0f6-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5a0f6-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="5a0f6-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5a0f6-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5a0f6-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="5a0f6-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5a0f6-951">CC099</span><span class="sxs-lookup"><span data-stu-id="5a0f6-951">CC099</span></span></th>
<th><span data-ttu-id="5a0f6-952">CC001</span><span class="sxs-lookup"><span data-stu-id="5a0f6-952">CC001</span></span></th>
<th><span data-ttu-id="5a0f6-953">CC002</span><span class="sxs-lookup"><span data-stu-id="5a0f6-953">CC002</span></span></th>
<th><span data-ttu-id="5a0f6-954">CC003</span><span class="sxs-lookup"><span data-stu-id="5a0f6-954">CC003</span></span></th>
<th><span data-ttu-id="5a0f6-955">CC004</span><span class="sxs-lookup"><span data-stu-id="5a0f6-955">CC004</span></span></th>
<th><span data-ttu-id="5a0f6-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-956">Proj 1</span></span></th>
<th><span data-ttu-id="5a0f6-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-957">Proj 2</span></span></th>
<th><span data-ttu-id="5a0f6-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="5a0f6-958">Prod 1</span></span></th>
<th><span data-ttu-id="5a0f6-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="5a0f6-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5a0f6-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="5a0f6-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5a0f6-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="5a0f6-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-971">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5a0f6-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-973">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-974">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-975">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-976">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-977">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-978">776.36</span><span class="sxs-lookup"><span data-stu-id="5a0f6-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-979">223.64</span><span class="sxs-lookup"><span data-stu-id="5a0f6-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5a0f6-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="5a0f6-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-982">000</span><span class="sxs-lookup"><span data-stu-id="5a0f6-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-983">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-984">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-985">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-986">0,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-987">30,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-988">10,00</span><span class="sxs-lookup"><span data-stu-id="5a0f6-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5a0f6-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5a0f6-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5a0f6-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5a0f6-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5a0f6-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5a0f6-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5a0f6-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5a0f6-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="5a0f6-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5a0f6-996">Weitere Informationen finden Sie unter [Kostenrollup-Richtlinie und Zuschlagsberechnung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="5a0f6-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



