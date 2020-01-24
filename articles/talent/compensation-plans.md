---
title: Vergütungspläne
description: Manager Vergütungen und Leistungen können die Vergütungsverwaltung verwenden, um die festen und variablen Vergütungspläne für die Mitarbeiter der Organisation verwalten und verarbeiten.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 8e7e41756c3be73937ef62523ff6bf41536405b0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898849"
---
# <a name="compensation-plans"></a><span data-ttu-id="997de-103">Vergütungspläne</span><span class="sxs-lookup"><span data-stu-id="997de-103">Compensation plans</span></span>

<span data-ttu-id="997de-104">Manager Vergütungen und Leistungen können die Vergütungsverwaltung verwenden, um die festen und variablen Vergütungspläne für die Mitarbeiter der Organisation verwalten und verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="997de-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="997de-105">Einführung</span><span class="sxs-lookup"><span data-stu-id="997de-105">Introduction</span></span>

<span data-ttu-id="997de-106">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="997de-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="997de-107">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="997de-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="997de-108">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="997de-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="997de-109">Die Mitarbeiter können einem oder mehreren Plänen beider Arten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="997de-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="997de-110">Ein Mitarbeiter muss die folgenden Bedingungen erfüllen, um für die Registrierung in einem Vergütungsplan berechtigt zu sein:</span><span class="sxs-lookup"><span data-stu-id="997de-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="997de-111">Der Mitarbeiter muss eine aktive Positionszuweisung haben.</span><span class="sxs-lookup"><span data-stu-id="997de-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="997de-112">Der Mitarbeiter muss den Kriterien entsprechen, die durch Berechtigungsregeln für einen Vergütungsplan definiert werden.</span><span class="sxs-lookup"><span data-stu-id="997de-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="997de-113">Vergütungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="997de-113">Compensation setup</span></span>
<span data-ttu-id="997de-114">Die folgende Tabelle listet Komponenten des Vergütungsprozess auf, die Bestandteile der Vergütungspläne Ihres Unternehmens sein können.</span><span class="sxs-lookup"><span data-stu-id="997de-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="997de-115">Komponente</span><span class="sxs-lookup"><span data-stu-id="997de-115">Component</span></span></th>
<th><span data-ttu-id="997de-116">Weitere Informationen...</span><span class="sxs-lookup"><span data-stu-id="997de-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="997de-117">Aktivitäten bezüglich fester Vergütung</span><span class="sxs-lookup"><span data-stu-id="997de-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="997de-118">Aktivitäten bezüglich fester Vergütung werden aus zwei Gründen eingerichtet:</span><span class="sxs-lookup"><span data-stu-id="997de-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="997de-119">Aktivitäten können die Art der Informationen angeben, die erfasst werden muss, wenn sich die Vergütung eines Mitarbeiters ändert.</span><span class="sxs-lookup"><span data-stu-id="997de-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="997de-120">So können z. B. festlegen, dass der Grund eine Änderung (z. B. eine Beförderung oder Zurückstufung) erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="997de-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="997de-121">Die Aktivitäten werden auf einen Ereignisprozesses angewendet, wenn feste Vergütungspläne berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="997de-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="997de-122">Aktivitäten vom Typ "Vergleich" vergleichen beispielsweise die Bezahlung von Mitarbeitern mit dem Mindestreferenzpunkt für die Stufe des Mitarbeiters und stellen sicher, dass dem Mitarbeiter mindestens das Minimum gezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="997de-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997de-123">Ebenen</span><span class="sxs-lookup"><span data-stu-id="997de-123">Levels</span></span></td>
<td><span data-ttu-id="997de-124">Ebenen werden Stellen zugeordnet, und alle mit der Stelle verknüpften Positionen übernehmen die Stellenreferenz.</span><span class="sxs-lookup"><span data-stu-id="997de-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="997de-125">Sie können eigenständige Ebenen für die drei Arten von Vergütungsplänen erstellen: Abschluss, Bereich und Schritt.</span><span class="sxs-lookup"><span data-stu-id="997de-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997de-126">Matrix für Bereichsauslastung</span><span class="sxs-lookup"><span data-stu-id="997de-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="997de-127">Eine Bereichsauslastungsmatrix unterstützt Sie bei der Verschiebung von Mitarbeitern zum Kontrollpunkt für ihre Stellen.</span><span class="sxs-lookup"><span data-stu-id="997de-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="997de-128">Darüber hinaus kann auch durch die Bereichsauslastung die Fairness des Lohnsatzes innerhalb des Unternehmens kontrolliert werden, ohne dabei die Leistung eines einzelnen Mitarbeiters oder die Leistung des gesamten Unternehmens zugrunde zu legen.</span><span class="sxs-lookup"><span data-stu-id="997de-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="997de-129">So erhalten Mitarbeiter, die in ihrem Bereich geringer bezahlt werden, eine höhere prozentuale Steigerung als Mitarbeiter, die höher im Bereich bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="997de-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="997de-130">Auf diese Weise können Sie Eigenkapitalunterschiede systematisch ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="997de-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="997de-131">Die Bereichsauslastung wird wie folgt berechnet: (Fester Lohnsatz - Bereichs-Minimum) ÷ (Höchstwert des Bereichs - Mindestwert des Bereichs).</span><span class="sxs-lookup"><span data-stu-id="997de-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997de-132">Referenzpunkteinstellungen</span><span class="sxs-lookup"><span data-stu-id="997de-132">Reference point setups</span></span></td>
<td><span data-ttu-id="997de-133">Eine Referenzpunkteinstellung umfasst eine Gruppe von Referenzpunkten, bei denen es sich um Bereiche in einer Lohnsatzmatrix handelt.</span><span class="sxs-lookup"><span data-stu-id="997de-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="997de-134">Jeder Bereich kann einem Lohnsatz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="997de-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="997de-135">Beispielsweise haben Abschlusspläne häufig Referenzpunkte zum Minimum, Mittelwert und Maximum.</span><span class="sxs-lookup"><span data-stu-id="997de-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997de-136">Vergütungsmatrix</span><span class="sxs-lookup"><span data-stu-id="997de-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="997de-137">Eine Vergütungsmatrix ist eine Gruppe von Referenzpunkten und Ebenen, die Sie verwenden, um eine Vergütungsstruktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="997de-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997de-138">Vergütungsstruktur</span><span class="sxs-lookup"><span data-stu-id="997de-138">Compensation structure</span></span></td>
<td><span data-ttu-id="997de-139">Eine Vergütungsstruktur ist eine Vergütungsmatrix, der Lohnsätze mit Referenzpunkten für jede Stufe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="997de-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997de-140">Berechtigungsregeln</span><span class="sxs-lookup"><span data-stu-id="997de-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="997de-141">Berechtigungsregeln werden verwendet, um Mitarbeiter in bestimmten Stellen, Stellenfunktionen, Stellentypen, Abteilungen, Gewerkschaften oder Vergütungsregionen, die durch bestimmte Vergütungspläne abgedeckt werden, zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="997de-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="997de-142">Sie müssen Berechtigungsregeln für Variablen und feste Vergütung erstellen, um Mitarbeiter im Plan zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="997de-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="997de-143">Nachdem Sie die Berechtigungsregeln für einen Vergütungsplan festgelegt haben, können Sie die Stufen des Plans definieren, die für die entsprechenden Stellen gelten sollen.</span><span class="sxs-lookup"><span data-stu-id="997de-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997de-144">Lohnzahlungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="997de-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="997de-145">Lohnzahlungshäufigkeiten werden verwendet, um den Zeitraum zu definieren, für die der Vergütungseinstellungen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="997de-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="997de-146">Beispielsweise hilft Ihnen die Lohnzahlungshäufigkeit zu verstehen, ob der Kompensationsbetrag als jährliches Gehalt oder als Stundenlohn angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="997de-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="997de-147">Zahlungshäufigkeiten werden auch verwendet, um Umrechnungsfaktoren einzurichten, um Vergütung von monatlich, wöchentlich, zweiwöchentlich und stundenbasiert in eine jährliche Lohnzahlungshäufigkeit umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="997de-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997de-148">Ausgleichsregionen</span><span class="sxs-lookup"><span data-stu-id="997de-148">Compensation regions</span></span></td>
<td><span data-ttu-id="997de-149">Vergütungsregionen werden verwendet, um Mitarbeitervergütungen auf Basis des Standorts des Arbeitsplatzes anzugeben.</span><span class="sxs-lookup"><span data-stu-id="997de-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997de-150">Kontrollpunkt</span><span class="sxs-lookup"><span data-stu-id="997de-150">Control point</span></span></td>
<td><span data-ttu-id="997de-151">Der Kontrollpunkt definiert, wie der ideale Lohnsatz für alle Mitarbeiter einer Vergütungsstufe aussieht.</span><span class="sxs-lookup"><span data-stu-id="997de-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="997de-152">Bei bewerteten Planungsstrukturen stellen die Kontrollpunkte üblicherweise die Bereichsmitte dar.</span><span class="sxs-lookup"><span data-stu-id="997de-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="997de-153">Bei flexiblen Strukturen wird nur selten auf Kontrollpunkte zurückgegriffen.</span><span class="sxs-lookup"><span data-stu-id="997de-153">Band structures rarely use control points.</span></span> <span data-ttu-id="997de-154">Sie können den Kontrollpunkt für einen Plan für feste Vergütung im Formular "Pläne für feste Vergütung" angeben.</span><span class="sxs-lookup"><span data-stu-id="997de-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997de-155">Stellenfunktionen</span><span class="sxs-lookup"><span data-stu-id="997de-155">Job functions</span></span></td>
<td><span data-ttu-id="997de-156">Stellenfunktionen werden verwendet, um Vergütungspläne für bestimmte Stellen zu klassifiziert und zu filtern.</span><span class="sxs-lookup"><span data-stu-id="997de-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997de-157">Einzelvorgangstypen</span><span class="sxs-lookup"><span data-stu-id="997de-157">Job types</span></span></td>
<td><span data-ttu-id="997de-158">Stellentypen werden verwendet, um Vergütungspläne für bestimmte Stellen zu klassifiziert und zu filtern.</span><span class="sxs-lookup"><span data-stu-id="997de-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997de-159">Typen für variable Vergütung</span><span class="sxs-lookup"><span data-stu-id="997de-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="997de-160">Die Typen für variable Vergütungen, z. B. eine Aktienprämien oder Bargeldprämien, werden in Plänen für variable Vergütung angewendet.</span><span class="sxs-lookup"><span data-stu-id="997de-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997de-161">Vergütungsraster</span><span class="sxs-lookup"><span data-stu-id="997de-161">Compensation grids</span></span></td>
<td><span data-ttu-id="997de-162">Vergütungsraster enthalten die Vergütungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="997de-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="997de-163">Vergütungsraster können durch mindestens eine Vergütung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="997de-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997de-164">Leistungspläne</span><span class="sxs-lookup"><span data-stu-id="997de-164">Performance plans</span></span></td>
<td><span data-ttu-id="997de-165">Leistungspläne werden verwendet, um Leistung einer Verteilungsmatrix zuzuordnen, um den Plan in einer Strategie für leistungsbezogene Bezahlung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="997de-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997de-166">Leistungsbewertungen</span><span class="sxs-lookup"><span data-stu-id="997de-166">Performance ratings</span></span></td>
<td><span data-ttu-id="997de-167">Leistungsbewertungen werden in Leistungsplänen verwendet, um den Betrag für eine Verdienst- oder eine Leistungsprämie zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="997de-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="997de-168">Prozessereignisse</span><span class="sxs-lookup"><span data-stu-id="997de-168">Process events</span></span>
<span data-ttu-id="997de-169">Ein Prozessereignis kalkuliert Vergütungsinformationen für eine bestimmte Periode für alle Mitarbeiter, die für einen oder mehrere Pläne mit fester oder variabler Vergütung registriert sind.</span><span class="sxs-lookup"><span data-stu-id="997de-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="997de-170">Ein Prozessereignis kann mehrmals zum Testen oder Aktualisieren berechneter Vergütungsergebnisse ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="997de-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="997de-171">Vergütungsereignisse</span><span class="sxs-lookup"><span data-stu-id="997de-171">Compensation events</span></span>
-------------------

<span data-ttu-id="997de-172">Jedes Mal, wenn ein Prozessereignis ausgeführt wird, wird ein Kompensationsereignis erstellt.</span><span class="sxs-lookup"><span data-stu-id="997de-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="997de-173">Kompensationsereignisse enthalten die Ergebnisse des Kompensationsprozesses für jeden Mitarbeiter, das in diesen Prozessereignis enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="997de-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="997de-174">Wenn die Berechnungen korrekt sind, können Sie das Prozessereignis laden, um die Vergütungsdatensätze für die Mitarbeiter zu aktualisieren, die vom Prozessereignis betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="997de-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="997de-175">Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="997de-175">Recommendations</span></span>
<span data-ttu-id="997de-176">Nachdem Sie ein Prozessereignis ausgeführt haben, können Sie Anpassungen an Lohnsteigerung oder Prämienbetrag eines Mitarbeiters basierend auf den berechneten Richtlinien des Prozessereignisses empfehlen.</span><span class="sxs-lookup"><span data-stu-id="997de-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="997de-177">Um Empfehlungen für Mitarbeiter zu machen, müssen Sie Empfehlungen aktivieren, wenn Sie Vergütungspläne einrichten oder das Prozessereignis erstellen.</span><span class="sxs-lookup"><span data-stu-id="997de-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>



