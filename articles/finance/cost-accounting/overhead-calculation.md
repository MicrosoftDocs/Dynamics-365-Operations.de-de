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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177923"
---
# <a name="overhead-calculation"></a><span data-ttu-id="ee0c9-103">Gemeinkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee0c9-104">In diesem Thema werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="ee0c9-105">Begriffsdefinition</span><span class="sxs-lookup"><span data-stu-id="ee0c9-105">Term definition</span></span>
---------------

<span data-ttu-id="ee0c9-106">Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="ee0c9-107">Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="ee0c9-108">Hier sind einige Beispiele für Gemeinkosten:</span><span class="sxs-lookup"><span data-stu-id="ee0c9-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="ee0c9-109">Miete</span><span class="sxs-lookup"><span data-stu-id="ee0c9-109">Rent</span></span>
-   <span data-ttu-id="ee0c9-110">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-110">Electricity</span></span>
-   <span data-ttu-id="ee0c9-111">Verwaltungsgehälter</span><span class="sxs-lookup"><span data-stu-id="ee0c9-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="ee0c9-112">Gemeinkostenberechnung, Übersicht</span><span class="sxs-lookup"><span data-stu-id="ee0c9-112">Overhead calculation overview</span></span>
<span data-ttu-id="ee0c9-113">Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="ee0c9-114">Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="ee0c9-115">Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="ee0c9-116">Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="ee0c9-117">Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="ee0c9-118">Die eindeutige Version-Kennung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="ee0c9-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="ee0c9-119">Versionstyp</span><span class="sxs-lookup"><span data-stu-id="ee0c9-119">Version type</span></span>
-   <span data-ttu-id="ee0c9-120">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="ee0c9-120">Date and time</span></span>
-   <span data-ttu-id="ee0c9-121">Kostenrechnungssachkonto</span><span class="sxs-lookup"><span data-stu-id="ee0c9-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="ee0c9-122">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="ee0c9-122">Fiscal year</span></span>
-   <span data-ttu-id="ee0c9-123">Finanzzeitraum</span><span class="sxs-lookup"><span data-stu-id="ee0c9-123">Fiscal period</span></span>

<span data-ttu-id="ee0c9-124">Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="ee0c9-125">Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="ee0c9-126">Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="ee0c9-127">In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="ee0c9-128">Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="ee0c9-129">Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="ee0c9-130">Deshalb ist die Nachweisbarkeit immer gegeben.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="ee0c9-131">[![Gemeinkostenberechnung](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="ee0c9-132">Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu</span><span class="sxs-lookup"><span data-stu-id="ee0c9-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="ee0c9-133">In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="ee0c9-134">Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="ee0c9-135">In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="ee0c9-136">Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="ee0c9-137">Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-138">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-139">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-140">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="ee0c9-140">Main account</span></span></th>
<th><span data-ttu-id="ee0c9-141">Betrag in Buchhaltungswährung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-142">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-143">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-143">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-144">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-144">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-145">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-145">10001</span></span></td>
<td><span data-ttu-id="ee0c9-146">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-146">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="ee0c9-148">Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="ee0c9-149">Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="ee0c9-150">Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als  **Fixkosten** oder **Variable Kosten** neu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="ee0c9-151">Definieren Sie die Kostenverhaltensregel</span><span class="sxs-lookup"><span data-stu-id="ee0c9-151">Define the cost behavior rule</span></span>

<span data-ttu-id="ee0c9-152">Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="ee0c9-153">Elektrizitätsrechnungen entsprechen oftmals dieser Definition.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="ee0c9-154">Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="ee0c9-155">Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:</span><span class="sxs-lookup"><span data-stu-id="ee0c9-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="ee0c9-156">Fester Betrag 1,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="ee0c9-157">0 &lt;= 1,000.00 = Fest</span><span class="sxs-lookup"><span data-stu-id="ee0c9-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="ee0c9-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="ee0c9-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="ee0c9-159">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-160">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-160">Journal</span></span></th>
<th><span data-ttu-id="ee0c9-161">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="ee0c9-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ee0c9-162">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ee0c9-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ee0c9-163">Version</span><span class="sxs-lookup"><span data-stu-id="ee0c9-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-164">00001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-164">00001</span></span></td>
<td><span data-ttu-id="ee0c9-165">Erfassung der Kostenverhaltensberechnung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="ee0c9-166">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="ee0c9-166">Fiscal</span></span></td>
<td><span data-ttu-id="ee0c9-167">2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-167">2017</span></span></td>
<td><span data-ttu-id="ee0c9-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-168">Period 1</span></span></td>
<td><span data-ttu-id="ee0c9-169">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ee0c9-170">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-171">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-172">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-173">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-174">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-174">Cost behavior</span></span></th>
<th><span data-ttu-id="ee0c9-175">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-176">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-177">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-177">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-178">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-178">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-179">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-179">10001</span></span></td>
<td><span data-ttu-id="ee0c9-180">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-180">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-181">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="ee0c9-181">Unclassified</span></span></td>
<td><span data-ttu-id="ee0c9-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ee0c9-183">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ee0c9-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-184">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-185">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-186">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-186">Cost behavior</span></span></th>
<th><span data-ttu-id="ee0c9-187">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-187">Amount</span></span></th>
<th><span data-ttu-id="ee0c9-188">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-189">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-189">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-190">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-190">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-191">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-191">10001</span></span></td>
<td><span data-ttu-id="ee0c9-192">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-192">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-193">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="ee0c9-193">Unclassified</span></span></td>
<td><span data-ttu-id="ee0c9-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-194">10,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-195">3. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-196">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-196">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-197">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-197">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-198">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-198">10001</span></span></td>
<td><span data-ttu-id="ee0c9-199">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-199">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-200">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="ee0c9-200">Unclassified</span></span></td>
<td><span data-ttu-id="ee0c9-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-201">-10,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-202">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-203">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-203">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-204">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-204">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-205">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-205">10001</span></span></td>
<td><span data-ttu-id="ee0c9-206">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-206">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-207">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-207">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-208">1,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-209">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-210">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-210">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-211">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-211">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-212">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-212">10001</span></span></td>
<td><span data-ttu-id="ee0c9-213">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-213">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-214">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-214">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-215">9,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-216">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-217">Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="ee0c9-218">Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="ee0c9-219">Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="ee0c9-220">Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="ee0c9-221">Definieren Sie die Kostenaufteilungsregel</span><span class="sxs-lookup"><span data-stu-id="ee0c9-221">Define the cost distribution rule</span></span>

<span data-ttu-id="ee0c9-222">In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="ee0c9-223">In der Kostenrechnung ist dieser Ansatz nicht genau genug.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="ee0c9-224">Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="ee0c9-225">Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="ee0c9-226">Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="ee0c9-227">Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-228">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-228">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-229">KWH</span><span class="sxs-lookup"><span data-stu-id="ee0c9-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-230">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-230">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-231">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-231">HR</span></span></td>
<td><span data-ttu-id="ee0c9-232">1.000</span><span class="sxs-lookup"><span data-stu-id="ee0c9-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-233">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-233">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-234">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-234">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-235">6.000</span><span class="sxs-lookup"><span data-stu-id="ee0c9-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-236">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-236">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-237">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-237">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-238">0</span><span class="sxs-lookup"><span data-stu-id="ee0c9-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-239">Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-240">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-240">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-241">Größe</span><span class="sxs-lookup"><span data-stu-id="ee0c9-241">Magnitude</span></span></th>
<th><span data-ttu-id="ee0c9-242">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ee0c9-242">Allocation factor</span></span></th>
<th><span data-ttu-id="ee0c9-243">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-244">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-244">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-245">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-245">HR</span></span></td>
<td><span data-ttu-id="ee0c9-246">1.000</span><span class="sxs-lookup"><span data-stu-id="ee0c9-246">1,000</span></span></td>
<td><span data-ttu-id="ee0c9-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-249">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-249">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-250">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-250">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-251">6.000</span><span class="sxs-lookup"><span data-stu-id="ee0c9-251">6,000</span></span></td>
<td><span data-ttu-id="ee0c9-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ee0c9-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-254">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-254">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-255">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-255">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-256">0</span><span class="sxs-lookup"><span data-stu-id="ee0c9-256">0</span></span></td>
<td><span data-ttu-id="ee0c9-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-258">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-259">Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="ee0c9-260">Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: Elektrizität &gt;0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-261">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-261">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-262">Berechnungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-262">Formula</span></span></th>
<th><span data-ttu-id="ee0c9-263">Größe</span><span class="sxs-lookup"><span data-stu-id="ee0c9-263">Magnitude</span></span></th>
<th><span data-ttu-id="ee0c9-264">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ee0c9-264">Allocation factor</span></span></th>
<th><span data-ttu-id="ee0c9-265">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-266">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-266">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-267">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-267">HR</span></span></td>
<td><span data-ttu-id="ee0c9-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ee0c9-269">1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-269">1</span></span></td>
<td><span data-ttu-id="ee0c9-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-271">500,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-272">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-272">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-273">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-273">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ee0c9-275">1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-275">1</span></span></td>
<td><span data-ttu-id="ee0c9-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-277">500,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-278">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-278">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-279">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-279">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ee0c9-281">0</span><span class="sxs-lookup"><span data-stu-id="ee0c9-281">0</span></span></td>
<td><span data-ttu-id="ee0c9-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-283">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ee0c9-284">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-285">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-285">Journal</span></span></th>
<th><span data-ttu-id="ee0c9-286">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="ee0c9-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ee0c9-287">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ee0c9-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ee0c9-288">Version</span><span class="sxs-lookup"><span data-stu-id="ee0c9-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-289">00002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-289">00002</span></span></td>
<td><span data-ttu-id="ee0c9-290">Berechnung der Kostenverteilung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="ee0c9-291">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="ee0c9-291">Fiscal</span></span></td>
<td><span data-ttu-id="ee0c9-292">2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-292">2017</span></span></td>
<td><span data-ttu-id="ee0c9-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-293">Period 1</span></span></td>
<td><span data-ttu-id="ee0c9-294">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ee0c9-295">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-296">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-297">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-298">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-299">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-299">Cost behavior</span></span></th>
<th><span data-ttu-id="ee0c9-300">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-301">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-302">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-302">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-303">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-303">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-304">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-304">10001</span></span></td>
<td><span data-ttu-id="ee0c9-305">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-305">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-306">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-306">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-308">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-309">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-309">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-310">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-310">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-311">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-311">10001</span></span></td>
<td><span data-ttu-id="ee0c9-312">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-312">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-313">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-313">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ee0c9-315">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ee0c9-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-316">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-317">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-318">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-318">Cost behavior</span></span></th>
<th><span data-ttu-id="ee0c9-319">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-319">Amount</span></span></th>
<th><span data-ttu-id="ee0c9-320">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-321">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-321">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-322">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-322">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-323">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-323">10001</span></span></td>
<td><span data-ttu-id="ee0c9-324">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-324">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-325">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-325">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-326">-1,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-327">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-328">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-328">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-329">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-329">HR</span></span></td>
<td><span data-ttu-id="ee0c9-330">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-330">10001</span></span></td>
<td><span data-ttu-id="ee0c9-331">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-331">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-332">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-332">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-333">500,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-333">500.00</span></span></td>
<td><span data-ttu-id="ee0c9-334">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-335">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-335">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-336">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-336">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-337">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-337">10001</span></span></td>
<td><span data-ttu-id="ee0c9-338">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-338">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-339">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-339">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-340">500,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-340">500.00</span></span></td>
<td><span data-ttu-id="ee0c9-341">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-342">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-342">CC099</span></span></td>
<td><span data-ttu-id="ee0c9-343">Standardmäßige Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="ee0c9-343">Default cost center</span></span></td>
<td><span data-ttu-id="ee0c9-344">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-344">10001</span></span></td>
<td><span data-ttu-id="ee0c9-345">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-345">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-346">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-346">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-347">-9,000.00</span></span></td>
<td><span data-ttu-id="ee0c9-348">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-349">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-349">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-350">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-350">HR</span></span></td>
<td><span data-ttu-id="ee0c9-351">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-351">10001</span></span></td>
<td><span data-ttu-id="ee0c9-352">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-352">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-353">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-353">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-354">1,285.71</span></span></td>
<td><span data-ttu-id="ee0c9-355">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-356">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-356">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-357">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-357">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-358">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-358">10001</span></span></td>
<td><span data-ttu-id="ee0c9-359">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-359">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-360">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-360">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ee0c9-361">7,714.29</span></span></td>
<td><span data-ttu-id="ee0c9-362">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-363">Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="ee0c9-364">Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="ee0c9-365">Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="ee0c9-366">Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="ee0c9-367">Definieren Sie den Gemeinkostensatz</span><span class="sxs-lookup"><span data-stu-id="ee0c9-367">Define the overhead rate</span></span>

<span data-ttu-id="ee0c9-368">Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="ee0c9-369">Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-370">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-370">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-371">Stunden</span><span class="sxs-lookup"><span data-stu-id="ee0c9-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-372">Proj 1</span></span></td>
<td><span data-ttu-id="ee0c9-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-373">Project 1</span></span></td>
<td><span data-ttu-id="ee0c9-374">3</span><span class="sxs-lookup"><span data-stu-id="ee0c9-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-375">Proj 2</span></span></td>
<td><span data-ttu-id="ee0c9-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-376">Project 2</span></span></td>
<td><span data-ttu-id="ee0c9-377">1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-378">Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-379">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-379">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-380">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-381">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-381">Cost behavior</span></span></th>
<th><span data-ttu-id="ee0c9-382">Einheiten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-382">Units</span></span></th>
<th><span data-ttu-id="ee0c9-383">Satz</span><span class="sxs-lookup"><span data-stu-id="ee0c9-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-384">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-384">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-385">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-385">HR</span></span></td>
<td><span data-ttu-id="ee0c9-386">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-386">10001</span></span></td>
<td><span data-ttu-id="ee0c9-387">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-387">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-388">1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-388">1</span></span></td>
<td><span data-ttu-id="ee0c9-389">10</span><span class="sxs-lookup"><span data-stu-id="ee0c9-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-390">Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-391">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-391">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-392">Größe</span><span class="sxs-lookup"><span data-stu-id="ee0c9-392">Magnitude</span></span></th>
<th><span data-ttu-id="ee0c9-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-393">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-394">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ee0c9-394">Allocation factor</span></span></th>
<th><span data-ttu-id="ee0c9-395">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-396">Proj 1</span></span></td>
<td><span data-ttu-id="ee0c9-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-397">Project 1</span></span></td>
<td><span data-ttu-id="ee0c9-398">3</span><span class="sxs-lookup"><span data-stu-id="ee0c9-398">3</span></span></td>
<td><span data-ttu-id="ee0c9-399">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-399">10001</span></span></td>
<td><span data-ttu-id="ee0c9-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ee0c9-401">30,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-402">Proj 2</span></span></td>
<td><span data-ttu-id="ee0c9-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-403">Project 2</span></span></td>
<td><span data-ttu-id="ee0c9-404">1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-404">1</span></span></td>
<td><span data-ttu-id="ee0c9-405">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-405">10001</span></span></td>
<td><span data-ttu-id="ee0c9-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ee0c9-407">10,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ee0c9-408">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-409">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-409">Journal</span></span></th>
<th><span data-ttu-id="ee0c9-410">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="ee0c9-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ee0c9-411">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ee0c9-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ee0c9-412">Version</span><span class="sxs-lookup"><span data-stu-id="ee0c9-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-413">00003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-413">00003</span></span></td>
<td><span data-ttu-id="ee0c9-414">Erfassung der Gemeinkostensatzberechnung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="ee0c9-415">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="ee0c9-415">Fiscal</span></span></td>
<td><span data-ttu-id="ee0c9-416">2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-416">2017</span></span></td>
<td><span data-ttu-id="ee0c9-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-417">Period 1</span></span></td>
<td><span data-ttu-id="ee0c9-418">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="ee0c9-419">Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-420">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-421">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-421">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-422">Größe</span><span class="sxs-lookup"><span data-stu-id="ee0c9-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-423">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-424">Proj 1</span></span></td>
<td><span data-ttu-id="ee0c9-425">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ee0c9-426">3,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-427">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-428">Proj 2</span></span></td>
<td><span data-ttu-id="ee0c9-429">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ee0c9-430">1,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ee0c9-431">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ee0c9-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-432">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-433">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-434">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-434">Cost behavior</span></span></th>
<th><span data-ttu-id="ee0c9-435">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-435">Amount</span></span></th>
<th><span data-ttu-id="ee0c9-436">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-437">CC0001</span></span></td>
<td><span data-ttu-id="ee0c9-438">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-438">HR</span></span></td>
<td><span data-ttu-id="ee0c9-439">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-439">10001</span></span></td>
<td><span data-ttu-id="ee0c9-440">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-440">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-441">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-441">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-442">-30.00</span></span></td>
<td><span data-ttu-id="ee0c9-443">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-444">Proj 1</span></span></td>
<td><span data-ttu-id="ee0c9-445">Internes Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ee0c9-446">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-446">10001</span></span></td>
<td><span data-ttu-id="ee0c9-447">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-447">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-448">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-448">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-449">30,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-449">30.00</span></span></td>
<td><span data-ttu-id="ee0c9-450">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-451">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-451">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-452">HR</span></span></td>
<td><span data-ttu-id="ee0c9-453">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-453">10001</span></span></td>
<td><span data-ttu-id="ee0c9-454">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-454">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-455">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-455">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-456">-10.00</span></span></td>
<td><span data-ttu-id="ee0c9-457">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-458">Proj 2</span></span></td>
<td><span data-ttu-id="ee0c9-459">Internes Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ee0c9-460">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-460">10001</span></span></td>
<td><span data-ttu-id="ee0c9-461">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-461">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-462">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-462">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-463">10.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-463">10.00</span></span></td>
<td><span data-ttu-id="ee0c9-464">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-465">Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="ee0c9-466">Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="ee0c9-467">Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="ee0c9-468">Finance unterstützt die gegenseitige Zuordnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="ee0c9-469">In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="ee0c9-470">Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="ee0c9-471">Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="ee0c9-472">Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="ee0c9-473">Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="ee0c9-474">[![Reziproke Methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="ee0c9-475">Kostenzuteilung definieren</span><span class="sxs-lookup"><span data-stu-id="ee0c9-475">Define the cost allocation</span></span>

<span data-ttu-id="ee0c9-476">Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="ee0c9-477">Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="ee0c9-478">Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-479">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-479">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-480">HR-Dienste</span><span class="sxs-lookup"><span data-stu-id="ee0c9-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-481">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-481">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-482">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-482">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-483">35</span><span class="sxs-lookup"><span data-stu-id="ee0c9-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-484">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-484">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-485">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-485">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-486">55</span><span class="sxs-lookup"><span data-stu-id="ee0c9-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-487">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-487">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-488">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-488">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-489">10</span><span class="sxs-lookup"><span data-stu-id="ee0c9-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-490">Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="ee0c9-491">Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-492">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-492">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-493">Finanzdienste</span><span class="sxs-lookup"><span data-stu-id="ee0c9-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-494">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-494">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-495">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-495">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-496">65</span><span class="sxs-lookup"><span data-stu-id="ee0c9-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-497">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-497">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-498">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-498">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-499">35</span><span class="sxs-lookup"><span data-stu-id="ee0c9-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-500">Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="ee0c9-501">Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-502">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-502">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-503">Montage-Services (Stunden)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-504">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-504">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-505">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-506">60</span><span class="sxs-lookup"><span data-stu-id="ee0c9-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-507">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-507">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-508">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-509">20</span><span class="sxs-lookup"><span data-stu-id="ee0c9-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-510">Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="ee0c9-511">Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-512">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-512">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-513">Packdienste (Stunden)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-514">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-514">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-515">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-516">80</span><span class="sxs-lookup"><span data-stu-id="ee0c9-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-517">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-517">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-518">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-519">15</span><span class="sxs-lookup"><span data-stu-id="ee0c9-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ee0c9-520">Statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, können von den Quelldaten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="ee0c9-521">Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="ee0c9-522">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-523">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-523">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-524">Größe</span><span class="sxs-lookup"><span data-stu-id="ee0c9-524">Magnitude</span></span></th>
<th><span data-ttu-id="ee0c9-525">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ee0c9-525">Allocation factor</span></span></th>
<th><span data-ttu-id="ee0c9-526">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-526">Amount</span></span></th>
<th><span data-ttu-id="ee0c9-527">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-528">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-528">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-529">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-529">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-530">35</span><span class="sxs-lookup"><span data-stu-id="ee0c9-530">35</span></span></td>
<td><span data-ttu-id="ee0c9-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ee0c9-532">175.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-532">175.00</span></span></td>
<td><span data-ttu-id="ee0c9-533">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-534">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-534">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-535">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-535">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-536">55</span><span class="sxs-lookup"><span data-stu-id="ee0c9-536">55</span></span></td>
<td><span data-ttu-id="ee0c9-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ee0c9-538">275.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-538">275.00</span></span></td>
<td><span data-ttu-id="ee0c9-539">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-540">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-540">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-541">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-541">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-542">10</span><span class="sxs-lookup"><span data-stu-id="ee0c9-542">10</span></span></td>
<td><span data-ttu-id="ee0c9-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ee0c9-544">50,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-544">50.00</span></span></td>
<td><span data-ttu-id="ee0c9-545">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-546">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-546">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-547">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-547">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-548">35</span><span class="sxs-lookup"><span data-stu-id="ee0c9-548">35</span></span></td>
<td><span data-ttu-id="ee0c9-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ee0c9-550">436.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-550">436.00</span></span></td>
<td><span data-ttu-id="ee0c9-551">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-552">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-552">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-553">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-553">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-554">55</span><span class="sxs-lookup"><span data-stu-id="ee0c9-554">55</span></span></td>
<td><span data-ttu-id="ee0c9-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ee0c9-556">685.14</span><span class="sxs-lookup"><span data-stu-id="ee0c9-556">685.14</span></span></td>
<td><span data-ttu-id="ee0c9-557">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-558">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-558">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-559">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-559">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-560">10</span><span class="sxs-lookup"><span data-stu-id="ee0c9-560">10</span></span></td>
<td><span data-ttu-id="ee0c9-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ee0c9-562">124.57</span><span class="sxs-lookup"><span data-stu-id="ee0c9-562">124.57</span></span></td>
<td><span data-ttu-id="ee0c9-563">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-564">Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-565">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-565">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-566">Größe</span><span class="sxs-lookup"><span data-stu-id="ee0c9-566">Magnitude</span></span></th>
<th><span data-ttu-id="ee0c9-567">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ee0c9-567">Allocation factor</span></span></th>
<th><span data-ttu-id="ee0c9-568">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-568">Amount</span></span></th>
<th><span data-ttu-id="ee0c9-569">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-570">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-570">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-571">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-571">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-572">65</span><span class="sxs-lookup"><span data-stu-id="ee0c9-572">65</span></span></td>
<td><span data-ttu-id="ee0c9-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ee0c9-574">438.75</span><span class="sxs-lookup"><span data-stu-id="ee0c9-574">438.75</span></span></td>
<td><span data-ttu-id="ee0c9-575">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-576">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-576">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-577">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-577">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-578">35</span><span class="sxs-lookup"><span data-stu-id="ee0c9-578">35</span></span></td>
<td><span data-ttu-id="ee0c9-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ee0c9-580">236.25</span><span class="sxs-lookup"><span data-stu-id="ee0c9-580">236.25</span></span></td>
<td><span data-ttu-id="ee0c9-581">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-582">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-582">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-583">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-583">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-584">65</span><span class="sxs-lookup"><span data-stu-id="ee0c9-584">65</span></span></td>
<td><span data-ttu-id="ee0c9-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ee0c9-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ee0c9-586">5,297.69</span></span></td>
<td><span data-ttu-id="ee0c9-587">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-588">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-588">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-589">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-589">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-590">35</span><span class="sxs-lookup"><span data-stu-id="ee0c9-590">35</span></span></td>
<td><span data-ttu-id="ee0c9-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ee0c9-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ee0c9-592">2,852.60</span></span></td>
<td><span data-ttu-id="ee0c9-593">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-594">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-595">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-595">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-596">Größe</span><span class="sxs-lookup"><span data-stu-id="ee0c9-596">Magnitude</span></span></th>
<th><span data-ttu-id="ee0c9-597">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ee0c9-597">Allocation factor</span></span></th>
<th><span data-ttu-id="ee0c9-598">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-598">Amount</span></span></th>
<th><span data-ttu-id="ee0c9-599">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-600">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-600">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-601">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-602">60</span><span class="sxs-lookup"><span data-stu-id="ee0c9-602">60</span></span></td>
<td><span data-ttu-id="ee0c9-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ee0c9-604">535.31</span><span class="sxs-lookup"><span data-stu-id="ee0c9-604">535.31</span></span></td>
<td><span data-ttu-id="ee0c9-605">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-606">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-606">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-607">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-608">20</span><span class="sxs-lookup"><span data-stu-id="ee0c9-608">20</span></span></td>
<td><span data-ttu-id="ee0c9-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ee0c9-610">178.44</span><span class="sxs-lookup"><span data-stu-id="ee0c9-610">178.44</span></span></td>
<td><span data-ttu-id="ee0c9-611">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-612">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-612">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-613">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-614">60</span><span class="sxs-lookup"><span data-stu-id="ee0c9-614">60</span></span></td>
<td><span data-ttu-id="ee0c9-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ee0c9-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ee0c9-616">4,487.12</span></span></td>
<td><span data-ttu-id="ee0c9-617">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-618">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-618">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-619">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-620">20</span><span class="sxs-lookup"><span data-stu-id="ee0c9-620">20</span></span></td>
<td><span data-ttu-id="ee0c9-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ee0c9-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-622">1,495.71</span></span></td>
<td><span data-ttu-id="ee0c9-623">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee0c9-624">Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-625">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-625">Cost object</span></span></th>
<th><span data-ttu-id="ee0c9-626">Größe</span><span class="sxs-lookup"><span data-stu-id="ee0c9-626">Magnitude</span></span></th>
<th><span data-ttu-id="ee0c9-627">Zuweisungsfaktor</span><span class="sxs-lookup"><span data-stu-id="ee0c9-627">Allocation factor</span></span></th>
<th><span data-ttu-id="ee0c9-628">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-628">Amount</span></span></th>
<th><span data-ttu-id="ee0c9-629">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-630">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-630">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-631">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-632">80</span><span class="sxs-lookup"><span data-stu-id="ee0c9-632">80</span></span></td>
<td><span data-ttu-id="ee0c9-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ee0c9-634">241.05</span><span class="sxs-lookup"><span data-stu-id="ee0c9-634">241.05</span></span></td>
<td><span data-ttu-id="ee0c9-635">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-636">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-636">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-637">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-638">15</span><span class="sxs-lookup"><span data-stu-id="ee0c9-638">15</span></span></td>
<td><span data-ttu-id="ee0c9-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ee0c9-640">45.20</span><span class="sxs-lookup"><span data-stu-id="ee0c9-640">45.20</span></span></td>
<td><span data-ttu-id="ee0c9-641">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-642">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-642">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-643">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-644">80</span><span class="sxs-lookup"><span data-stu-id="ee0c9-644">80</span></span></td>
<td><span data-ttu-id="ee0c9-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ee0c9-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ee0c9-646">2,507.09</span></span></td>
<td><span data-ttu-id="ee0c9-647">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-648">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-648">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-649">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-650">15</span><span class="sxs-lookup"><span data-stu-id="ee0c9-650">15</span></span></td>
<td><span data-ttu-id="ee0c9-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ee0c9-652">470.08</span><span class="sxs-lookup"><span data-stu-id="ee0c9-652">470.08</span></span></td>
<td><span data-ttu-id="ee0c9-653">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ee0c9-654">Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)</span><span class="sxs-lookup"><span data-stu-id="ee0c9-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-655">Erfassung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-655">Journal</span></span></th>
<th><span data-ttu-id="ee0c9-656">Journaltyp</span><span class="sxs-lookup"><span data-stu-id="ee0c9-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ee0c9-657">Steuerkalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ee0c9-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ee0c9-658">Version</span><span class="sxs-lookup"><span data-stu-id="ee0c9-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-659">00004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-659">00004</span></span></td>
<td><span data-ttu-id="ee0c9-660">Kostenzuteilungserfassung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="ee0c9-661">Steuerlich</span><span class="sxs-lookup"><span data-stu-id="ee0c9-661">Fiscal</span></span></td>
<td><span data-ttu-id="ee0c9-662">2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-662">2017</span></span></td>
<td><span data-ttu-id="ee0c9-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-663">Period 1</span></span></td>
<td><span data-ttu-id="ee0c9-664">Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="ee0c9-665">Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ee0c9-666">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-667">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-668">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-669">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-669">Cost behavior</span></span></th>
<th><span data-ttu-id="ee0c9-670">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-671">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-672">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-672">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-673">HR</span></span></td>
<td><span data-ttu-id="ee0c9-674">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-674">10001</span></span></td>
<td><span data-ttu-id="ee0c9-675">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-675">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-676">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-676">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-677">500,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-678">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-679">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-679">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-680">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-680">HR</span></span></td>
<td><span data-ttu-id="ee0c9-681">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-681">10001</span></span></td>
<td><span data-ttu-id="ee0c9-682">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-682">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-683">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-683">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-685">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-686">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-686">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-687">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-687">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-688">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-688">10001</span></span></td>
<td><span data-ttu-id="ee0c9-689">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-689">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-690">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-690">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-691">675.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-692">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-693">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-693">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-694">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-694">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-695">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-695">10001</span></span></td>
<td><span data-ttu-id="ee0c9-696">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-696">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-697">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-697">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="ee0c9-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-699">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-700">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-700">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-701">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-701">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-702">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-702">10001</span></span></td>
<td><span data-ttu-id="ee0c9-703">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-703">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-704">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-704">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-705">713.75</span><span class="sxs-lookup"><span data-stu-id="ee0c9-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-706">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-707">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-707">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-708">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-708">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-709">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-709">10001</span></span></td>
<td><span data-ttu-id="ee0c9-710">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-710">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-711">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-711">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="ee0c9-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-713">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-714">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-714">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-715">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-715">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-716">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-716">10001</span></span></td>
<td><span data-ttu-id="ee0c9-717">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-717">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-718">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-718">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-719">286.25</span><span class="sxs-lookup"><span data-stu-id="ee0c9-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-720">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-721">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-721">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-722">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-722">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-723">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-723">10001</span></span></td>
<td><span data-ttu-id="ee0c9-724">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-724">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-725">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-725">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="ee0c9-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-727">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-728">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-728">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-729">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-730">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-730">10001</span></span></td>
<td><span data-ttu-id="ee0c9-731">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-731">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-732">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-732">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-733">776.36</span><span class="sxs-lookup"><span data-stu-id="ee0c9-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-734">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-735">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-735">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-736">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-737">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-737">10001</span></span></td>
<td><span data-ttu-id="ee0c9-738">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-738">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-739">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-739">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ee0c9-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-741">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-742">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-742">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-743">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-744">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-744">10001</span></span></td>
<td><span data-ttu-id="ee0c9-745">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-745">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-746">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-746">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-747">223.64</span><span class="sxs-lookup"><span data-stu-id="ee0c9-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-748">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="ee0c9-749">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-749">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-750">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-751">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-751">10001</span></span></td>
<td><span data-ttu-id="ee0c9-752">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-752">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-753">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-753">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ee0c9-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ee0c9-755">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ee0c9-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ee0c9-756">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ee0c9-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-757">Cost element</span></span></th>
<th><span data-ttu-id="ee0c9-758">Kostenverhalten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-758">Cost behavior</span></span></th>
<th><span data-ttu-id="ee0c9-759">Betrag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-759">Amount</span></span></th>
<th><span data-ttu-id="ee0c9-760">Abschlussstichtag</span><span class="sxs-lookup"><span data-stu-id="ee0c9-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee0c9-761">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-761">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-762">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-762">HR</span></span></td>
<td><span data-ttu-id="ee0c9-763">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-763">10001</span></span></td>
<td><span data-ttu-id="ee0c9-764">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-764">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-765">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-765">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-766">-500.00</span></span></td>
<td><span data-ttu-id="ee0c9-767">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-768">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-768">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-769">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-769">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-770">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-770">10001</span></span></td>
<td><span data-ttu-id="ee0c9-771">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-771">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-772">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-772">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-773">175.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-773">175.00</span></span></td>
<td><span data-ttu-id="ee0c9-774">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-775">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-775">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-776">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-776">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-777">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-777">10001</span></span></td>
<td><span data-ttu-id="ee0c9-778">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-778">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-779">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-779">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-780">275.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-780">275.00</span></span></td>
<td><span data-ttu-id="ee0c9-781">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-782">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-782">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-783">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-783">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-784">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-784">10001</span></span></td>
<td><span data-ttu-id="ee0c9-785">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-785">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-786">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-786">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-787">50,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-787">50,00</span></span></td>
<td><span data-ttu-id="ee0c9-788">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-789">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-789">CC001</span></span></td>
<td><span data-ttu-id="ee0c9-790">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-790">HR</span></span></td>
<td><span data-ttu-id="ee0c9-791">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-791">10001</span></span></td>
<td><span data-ttu-id="ee0c9-792">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-792">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-793">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-793">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-794">-1,245.71</span></span></td>
<td><span data-ttu-id="ee0c9-795">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-796">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-796">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-797">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-797">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-798">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-798">10001</span></span></td>
<td><span data-ttu-id="ee0c9-799">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-799">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-800">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-800">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-801">436.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-801">436.00</span></span></td>
<td><span data-ttu-id="ee0c9-802">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-803">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-803">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-804">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-804">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-805">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-805">10001</span></span></td>
<td><span data-ttu-id="ee0c9-806">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-806">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-807">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-807">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-808">685.14</span><span class="sxs-lookup"><span data-stu-id="ee0c9-808">685.14</span></span></td>
<td><span data-ttu-id="ee0c9-809">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-810">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-810">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-811">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-811">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-812">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-812">10001</span></span></td>
<td><span data-ttu-id="ee0c9-813">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-813">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-814">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-814">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-815">124.57</span><span class="sxs-lookup"><span data-stu-id="ee0c9-815">124.57</span></span></td>
<td><span data-ttu-id="ee0c9-816">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-817">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-817">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-818">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-818">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-819">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-819">10001</span></span></td>
<td><span data-ttu-id="ee0c9-820">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-820">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-821">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-821">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-822">-675.00</span></span></td>
<td><span data-ttu-id="ee0c9-823">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-824">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-824">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-825">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-825">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-826">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-826">10001</span></span></td>
<td><span data-ttu-id="ee0c9-827">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-827">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-828">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-828">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-829">438.75</span><span class="sxs-lookup"><span data-stu-id="ee0c9-829">438.75</span></span></td>
<td><span data-ttu-id="ee0c9-830">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-831">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-831">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-832">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-832">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-833">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-833">10001</span></span></td>
<td><span data-ttu-id="ee0c9-834">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-834">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-835">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-835">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-836">236.25</span><span class="sxs-lookup"><span data-stu-id="ee0c9-836">236.25</span></span></td>
<td><span data-ttu-id="ee0c9-837">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-838">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-838">CC002</span></span></td>
<td><span data-ttu-id="ee0c9-839">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ee0c9-839">Finance</span></span></td>
<td><span data-ttu-id="ee0c9-840">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-840">10001</span></span></td>
<td><span data-ttu-id="ee0c9-841">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-841">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-842">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-842">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="ee0c9-843">-8,150.29</span></span></td>
<td><span data-ttu-id="ee0c9-844">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-845">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-845">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-846">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-846">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-847">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-847">10001</span></span></td>
<td><span data-ttu-id="ee0c9-848">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-848">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-849">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-849">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ee0c9-850">5,297.69</span></span></td>
<td><span data-ttu-id="ee0c9-851">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-852">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-852">CC004</span></span></td>
<td><span data-ttu-id="ee0c9-853">Verpackung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-853">Packaging</span></span></td>
<td><span data-ttu-id="ee0c9-854">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-854">10001</span></span></td>
<td><span data-ttu-id="ee0c9-855">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-855">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-856">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-856">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ee0c9-857">2,852.60</span></span></td>
<td><span data-ttu-id="ee0c9-858">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-859">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-859">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-860">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-860">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-861">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-861">10001</span></span></td>
<td><span data-ttu-id="ee0c9-862">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-862">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-863">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-863">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="ee0c9-864">-713.75</span></span></td>
<td><span data-ttu-id="ee0c9-865">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-866">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-866">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-867">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-868">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-868">10001</span></span></td>
<td><span data-ttu-id="ee0c9-869">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-869">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-870">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-870">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-871">535.31</span><span class="sxs-lookup"><span data-stu-id="ee0c9-871">535.31</span></span></td>
<td><span data-ttu-id="ee0c9-872">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-873">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-873">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-874">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-875">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-875">10001</span></span></td>
<td><span data-ttu-id="ee0c9-876">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-876">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-877">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-877">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-878">178.44</span><span class="sxs-lookup"><span data-stu-id="ee0c9-878">178.44</span></span></td>
<td><span data-ttu-id="ee0c9-879">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-880">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-880">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-881">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-881">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-882">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-882">10001</span></span></td>
<td><span data-ttu-id="ee0c9-883">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-883">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-884">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-884">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="ee0c9-885">-5,982.83</span></span></td>
<td><span data-ttu-id="ee0c9-886">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-887">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-887">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-888">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-889">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-889">10001</span></span></td>
<td><span data-ttu-id="ee0c9-890">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-890">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-891">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-891">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ee0c9-892">4,487.12</span></span></td>
<td><span data-ttu-id="ee0c9-893">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-894">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-894">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-895">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-896">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-896">10001</span></span></td>
<td><span data-ttu-id="ee0c9-897">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-897">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-898">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-898">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ee0c9-899">1,495.71</span></span></td>
<td><span data-ttu-id="ee0c9-900">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-901">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-901">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-902">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-902">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-903">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-903">10001</span></span></td>
<td><span data-ttu-id="ee0c9-904">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-904">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-905">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-905">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="ee0c9-906">-286.25</span></span></td>
<td><span data-ttu-id="ee0c9-907">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-908">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-908">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-909">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-910">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-910">10001</span></span></td>
<td><span data-ttu-id="ee0c9-911">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-911">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-912">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-912">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-913">241.05</span><span class="sxs-lookup"><span data-stu-id="ee0c9-913">241.05</span></span></td>
<td><span data-ttu-id="ee0c9-914">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-915">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-915">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-916">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-917">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-917">10001</span></span></td>
<td><span data-ttu-id="ee0c9-918">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-918">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-919">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-919">Fixed cost</span></span></td>
<td><span data-ttu-id="ee0c9-920">45.20</span><span class="sxs-lookup"><span data-stu-id="ee0c9-920">45.20</span></span></td>
<td><span data-ttu-id="ee0c9-921">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-922">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-922">CC003</span></span></td>
<td><span data-ttu-id="ee0c9-923">Montage</span><span class="sxs-lookup"><span data-stu-id="ee0c9-923">Assembly</span></span></td>
<td><span data-ttu-id="ee0c9-924">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-924">10001</span></span></td>
<td><span data-ttu-id="ee0c9-925">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-925">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-926">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-926">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="ee0c9-927">-2,977.17</span></span></td>
<td><span data-ttu-id="ee0c9-928">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-929">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-929">Prod 1</span></span></td>
<td><span data-ttu-id="ee0c9-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-930">Product 1</span></span></td>
<td><span data-ttu-id="ee0c9-931">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-931">10001</span></span></td>
<td><span data-ttu-id="ee0c9-932">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-932">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-933">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-933">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ee0c9-934">2,507.09</span></span></td>
<td><span data-ttu-id="ee0c9-935">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee0c9-936">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-936">Prod 2</span></span></td>
<td><span data-ttu-id="ee0c9-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-937">Product 2</span></span></td>
<td><span data-ttu-id="ee0c9-938">10001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-938">10001</span></span></td>
<td><span data-ttu-id="ee0c9-939">Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-939">Electricity</span></span></td>
<td><span data-ttu-id="ee0c9-940">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-940">Variable cost</span></span></td>
<td><span data-ttu-id="ee0c9-941">470.08</span><span class="sxs-lookup"><span data-stu-id="ee0c9-941">470.08</span></span></td>
<td><span data-ttu-id="ee0c9-942">31. Januar 2017</span><span class="sxs-lookup"><span data-stu-id="ee0c9-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="ee0c9-943">Schlussfolgerung</span><span class="sxs-lookup"><span data-stu-id="ee0c9-943">Conclusion</span></span>
<span data-ttu-id="ee0c9-944">In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="ee0c9-945">Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="ee0c9-946">In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="ee0c9-947">Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="ee0c9-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ee0c9-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="ee0c9-949">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="ee0c9-950">Gesamt</span><span class="sxs-lookup"><span data-stu-id="ee0c9-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ee0c9-951">CC099</span><span class="sxs-lookup"><span data-stu-id="ee0c9-951">CC099</span></span></th>
<th><span data-ttu-id="ee0c9-952">CC001</span><span class="sxs-lookup"><span data-stu-id="ee0c9-952">CC001</span></span></th>
<th><span data-ttu-id="ee0c9-953">CC002</span><span class="sxs-lookup"><span data-stu-id="ee0c9-953">CC002</span></span></th>
<th><span data-ttu-id="ee0c9-954">CC003</span><span class="sxs-lookup"><span data-stu-id="ee0c9-954">CC003</span></span></th>
<th><span data-ttu-id="ee0c9-955">CC004</span><span class="sxs-lookup"><span data-stu-id="ee0c9-955">CC004</span></span></th>
<th><span data-ttu-id="ee0c9-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-956">Proj 1</span></span></th>
<th><span data-ttu-id="ee0c9-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-957">Proj 2</span></span></th>
<th><span data-ttu-id="ee0c9-958">Produktion 1</span><span class="sxs-lookup"><span data-stu-id="ee0c9-958">Prod 1</span></span></th>
<th><span data-ttu-id="ee0c9-959">Produktion 2</span><span class="sxs-lookup"><span data-stu-id="ee0c9-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="ee0c9-960">100'1 Elektrizität</span><span class="sxs-lookup"><span data-stu-id="ee0c9-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="ee0c9-970">Nicht klassifiziert</span><span class="sxs-lookup"><span data-stu-id="ee0c9-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-971">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="ee0c9-972">Fixkosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-973">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-974">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-975">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-976">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-977">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-978">776.36</span><span class="sxs-lookup"><span data-stu-id="ee0c9-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-979">223.64</span><span class="sxs-lookup"><span data-stu-id="ee0c9-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="ee0c9-981">Variable Kosten</span><span class="sxs-lookup"><span data-stu-id="ee0c9-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-982">000</span><span class="sxs-lookup"><span data-stu-id="ee0c9-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-983">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-984">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-985">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-986">0,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-987">30,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-988">10,00</span><span class="sxs-lookup"><span data-stu-id="ee0c9-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ee0c9-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ee0c9-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ee0c9-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ee0c9-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ee0c9-992">Dieses Thema veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="ee0c9-993">Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="ee0c9-994">Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="ee0c9-995">Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="ee0c9-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="ee0c9-996">Weitere Informationen hierzu finden Sie unter [Kostenzusammenfassung](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="ee0c9-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



