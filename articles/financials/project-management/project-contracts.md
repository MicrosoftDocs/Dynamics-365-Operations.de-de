---
title: "Projektverträge"
description: "Dieses Thema bietet Beispiele für Projektverträge, die Sie für verschiedene Arten von Projekten und Finanzierungsquellen erstellen können, und wie Sie in Microsoft Dynamics 365 for Finance and Operations Verträge verwalten und Rechnungen für Projektdebitoren erstellen können."
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c0f0fcec64ce03c6e1d877fb1c8d004bb416bd95
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="project-contracts"></a><span data-ttu-id="04abf-103">Projektverträge</span><span class="sxs-lookup"><span data-stu-id="04abf-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04abf-104">Dieser Artikel bietet Beispiele für Projektverträge, die Sie für verschieden Arten von Projekten und Finanzierungsquellen erstellen können, und zeigt, wie Sie in Microsoft Dynamics 365 for Finance and Operations Verträge verwalten und Rechnungen für Projektdebitoren erstellen können.</span><span class="sxs-lookup"><span data-stu-id="04abf-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="04abf-105">Der für einen Projektvertrag erstellte Projekttyp definiert die Methode, nach der das Projekt den Debitoren in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="04abf-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="04abf-106">Ein Projektvertrag und das zugehörige Projekt können geändert werden, der Projekttyp jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="04abf-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="04abf-107">Mithilfe eines Projektvertrags können ein oder mehrere Projekte gleichzeitig fakturiert werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="04abf-108">Durch einen Projektvertrag wird zudem sichergestellt, dass für die einzelnen Unterprojekte in einer Projektstruktur die gleiche Rechnungsstellungsprozedur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04abf-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="04abf-109">Jedes Projekt, das fakturiert wird, muss einem Projektvertrag zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="04abf-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="04abf-110">Einstellungen für einen Projektvertrag gelten für alle Projekte und Unterprojekte, die dem Projektvertrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="04abf-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="04abf-111">In einem Projektvertrag können eine oder mehrere Finanzierungsquellen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="04abf-112">Dadurch können Sie die Fakturierung auf mehrere Geldgeber aufteilen, Finanzierungslimits einrichten, damit Finanzierungsquellen nicht mehr als ein angegebener Betrag berechnet wird, und Finanzierungsregeln für die Berechnung von Ausgaben konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="04abf-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="04abf-113">Finanzierung von Projektverträgen</span><span class="sxs-lookup"><span data-stu-id="04abf-113">Funding for project contracts</span></span>
<span data-ttu-id="04abf-114">In einigen Projektverträgen ist möglicherweise festgelegt, dass mehrere Parteien für die Finanzierung der Projektkosten verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="04abf-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="04abf-115">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="04abf-115">Here are some examples:</span></span>

-   <span data-ttu-id="04abf-116">Ein großer Debitor, der mehrere Divisionen hat, fordert die Finanzierung eines Projekts nach Divisionen an.</span><span class="sxs-lookup"><span data-stu-id="04abf-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="04abf-117">Ihre Unternehmen teilt die Kosten eines umfangreichen Projekts mit einer externen Organisation.</span><span class="sxs-lookup"><span data-stu-id="04abf-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="04abf-118">Ein Straßenprojekt wird durch zwei Gemeinden finanziert.</span><span class="sxs-lookup"><span data-stu-id="04abf-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="04abf-119">Ein Brückenprojekt wird durch einen staatlicher Zuschuss und von einem Privatunternehmen finanziert.</span><span class="sxs-lookup"><span data-stu-id="04abf-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="04abf-120">In Finance and Operations können Sie die Rechnungsstellung für eine Transaktion oder ein gesamtes Projekt unter mehreren Debitoren, Zuschüssen oder Organisationen aufteilen.</span><span class="sxs-lookup"><span data-stu-id="04abf-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="04abf-121">In Projekten mit mehreren Finanzierern werden alle Parteien, die zur Finanzierung eines erweiterten Finanzierungsprojekts beitragen, als Finanzierungsquellen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="04abf-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="04abf-122">Nachdem ein Debitor, eine Organisation oder ein Zuschuss als Finanzierungsquelle definiert wurde, kann diese einer oder mehreren Finanzierungsregeln zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="04abf-123">Finanzierungsregeln enthalten die Kriterien, nach denen Zuordnungen verschiedener Finanzierungsquellen für ein Projekt vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="04abf-124">Da gelagerte Artikel, z. B. in Bestellanforderungen und Bestellungen, nicht geteilt werden können, kann der Kostenbetrag nicht auf mehrere Finanzierungsquellen zum Zeitpunkt der Verteilung aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="04abf-125">Der Finanzierungsquellenwert bleibt folglich null, bis der Lagerbestand gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="04abf-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="04abf-126">Wenn der Lagerabgang gebucht wird, wird der Kostenbetrag in Übereinstimmung mit den Kontoverteilungsregeln für das Projekt verteilt.</span><span class="sxs-lookup"><span data-stu-id="04abf-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="04abf-127">Nachfolgend finden Sie einige Schritte, die Sie ausführen können, um die Fakturierung auf mehrere Finanzierungsquellen aufzuteilen:</span><span class="sxs-lookup"><span data-stu-id="04abf-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="04abf-128">Geben Sie an, dass für alle Buchungen zu einem Projekt dieselbe Verkaufswährung im Projektvertrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="04abf-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="04abf-129">Richten Sie Finanzierungslimits ein, sodass eine Finanzierungsquelle für ein Projekt nicht höher als mit dem angegebenen Betrag fakturiert wird.</span><span class="sxs-lookup"><span data-stu-id="04abf-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="04abf-130">Konfigurieren Sie Finanzierungsregeln und Finanzierungslimits für die einzelnen Arbeitskräfte, Artikel, Kategorien, Kategoriengruppen und Bankbuchungsarten (oder für die Buchungsarten insgesamt).</span><span class="sxs-lookup"><span data-stu-id="04abf-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="04abf-131">Wählen Sie ein optionales Start- und Enddatum für den Zeitraum, für den die jeweilige Finanzierungsregel gültig ist.</span><span class="sxs-lookup"><span data-stu-id="04abf-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="04abf-132">Geben Sie den Prozentsatz an, mit dem jede Finanzierungsquelle beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="04abf-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="04abf-133">Geben Sie die Finanzierungsquelle an, der Rundungsdifferenzen aus den Berechnungen der Finanzierungszuordnung zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04abf-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="04abf-134">Richten Sie Regeln ein, die festlegen, wie Projektkosten für externe Debitoren fakturiert und wie sie internen Organisationen zugerechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04abf-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="04abf-135">Erfassen Sie Buchungen in einem gesperrten Finanzierungskonto, bis eine zusätzliche Finanzierung bereitsteht oder bis die Kosten intern übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="04abf-136">Zur Bestimmung der Steuergruppe, die einer Buchung zugewiesen werden soll, wird das Projekt nach einer Steuergruppenzuweisung durchsucht.</span><span class="sxs-lookup"><span data-stu-id="04abf-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="04abf-137">Wurde auf Projektebene keine Steuergruppenzuweisung vorgenommen, wird nach dem Projektvertrag gesucht.</span><span class="sxs-lookup"><span data-stu-id="04abf-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="04abf-138">Beispiel: Mehrere Finanzierungsquellen (einfach)</span><span class="sxs-lookup"><span data-stu-id="04abf-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="04abf-139">Die folgende Tabelle enthält Szenarien für die Verwaltung der Finanzierungszuteilung mir mehreren Finanzierungsquellen.</span><span class="sxs-lookup"><span data-stu-id="04abf-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="04abf-140">Diese Szenarien basieren auf den folgenden Annahmen:</span><span class="sxs-lookup"><span data-stu-id="04abf-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="04abf-141">Die Prioritätseinstellungen werden in die Zuweisung von Geldmitteln einbezogen, bevor andere Finanzierungsregelkriterien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="04abf-142">Kein Datumsbereich ist angegeben worden, um die Periode zu definieren, in der die Finanzierungsregel gültig ist.</span><span class="sxs-lookup"><span data-stu-id="04abf-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04abf-143"><strong>Szenario</strong></span><span class="sxs-lookup"><span data-stu-id="04abf-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="04abf-144"><strong>Finanzierungsquelle </strong></span><span class="sxs-lookup"><span data-stu-id="04abf-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="04abf-145"><strong>Zuteilung in Prozent </strong></span><span class="sxs-lookup"><span data-stu-id="04abf-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="04abf-146"><strong>Zuweisungspriorität </strong></span><span class="sxs-lookup"><span data-stu-id="04abf-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04abf-147">Sie möchten einer Finanzierungsquelle Kosten zuweisen, bis die Mittel erschöpft sind, dann einer zweiten Finanzierungsquelle Kosten zuweisen, bis die Mittel erschöpft sind, und die verbleibenden Kosten schließlich einer dritten Finanzierungsquelle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="04abf-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="04abf-148">Finanzierungsquelle 1</span><span class="sxs-lookup"><span data-stu-id="04abf-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="04abf-149">Finanzierungsquelle 2</span><span class="sxs-lookup"><span data-stu-id="04abf-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="04abf-150">Finanzierungsquelle 3</span><span class="sxs-lookup"><span data-stu-id="04abf-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04abf-151">100 %</span><span class="sxs-lookup"><span data-stu-id="04abf-151">100%</span></span></li>
<li><span data-ttu-id="04abf-152">100 %</span><span class="sxs-lookup"><span data-stu-id="04abf-152">100%</span></span></li>
<li><span data-ttu-id="04abf-153">100 %</span><span class="sxs-lookup"><span data-stu-id="04abf-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04abf-154">1</span><span class="sxs-lookup"><span data-stu-id="04abf-154">1</span></span></li>
<li><span data-ttu-id="04abf-155">2</span><span class="sxs-lookup"><span data-stu-id="04abf-155">2</span></span></li>
<li><span data-ttu-id="04abf-156">3</span><span class="sxs-lookup"><span data-stu-id="04abf-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04abf-157">Sie möchten 75 Prozent der Kosten einer Finanzierungsquelle und 25 Prozent der Kosten einer zweiten Finanzierungsquelle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="04abf-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="04abf-158">Wenn eine dieser Finanzierungsquellen erschöpft ist, möchten Sie die verbleibenden Kosten aus einer dritten Finanzierungsquelle decken.</span><span class="sxs-lookup"><span data-stu-id="04abf-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="04abf-159">Finanzierungsquelle 1</span><span class="sxs-lookup"><span data-stu-id="04abf-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="04abf-160">Finanzierungsquelle 2</span><span class="sxs-lookup"><span data-stu-id="04abf-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="04abf-161">Finanzierungsquelle 3</span><span class="sxs-lookup"><span data-stu-id="04abf-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04abf-162">75 %</span><span class="sxs-lookup"><span data-stu-id="04abf-162">75%</span></span></li>
<li><span data-ttu-id="04abf-163">25 %</span><span class="sxs-lookup"><span data-stu-id="04abf-163">25%</span></span></li>
<li><span data-ttu-id="04abf-164">100 %</span><span class="sxs-lookup"><span data-stu-id="04abf-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04abf-165">1</span><span class="sxs-lookup"><span data-stu-id="04abf-165">1</span></span></li>
<li><span data-ttu-id="04abf-166">1</span><span class="sxs-lookup"><span data-stu-id="04abf-166">1</span></span></li>
<li><span data-ttu-id="04abf-167">2</span><span class="sxs-lookup"><span data-stu-id="04abf-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04abf-168">Sie möchten 75 Prozent der Kosten einer Finanzierungsquelle und 25 Prozent der Kosten einer zweiten Finanzierungsquelle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="04abf-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="04abf-169">Wenn eine der beiden Finanzierungsquellen erschöpft ist, möchten Sie die verbleibenden Kosten zwischen einer dritten und vierten Finanzierungsquelle aufteilen.</span><span class="sxs-lookup"><span data-stu-id="04abf-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="04abf-170">Finanzierungsquelle 1</span><span class="sxs-lookup"><span data-stu-id="04abf-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="04abf-171">Finanzierungsquelle 2</span><span class="sxs-lookup"><span data-stu-id="04abf-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="04abf-172">Finanzierungsquelle 3</span><span class="sxs-lookup"><span data-stu-id="04abf-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="04abf-173">Finanzierungsquelle 4</span><span class="sxs-lookup"><span data-stu-id="04abf-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04abf-174">75 %</span><span class="sxs-lookup"><span data-stu-id="04abf-174">75%</span></span></li>
<li><span data-ttu-id="04abf-175">25 %</span><span class="sxs-lookup"><span data-stu-id="04abf-175">25%</span></span></li>
<li><span data-ttu-id="04abf-176">50 %</span><span class="sxs-lookup"><span data-stu-id="04abf-176">50%</span></span></li>
<li><span data-ttu-id="04abf-177">50 %</span><span class="sxs-lookup"><span data-stu-id="04abf-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04abf-178">1</span><span class="sxs-lookup"><span data-stu-id="04abf-178">1</span></span></li>
<li><span data-ttu-id="04abf-179">1</span><span class="sxs-lookup"><span data-stu-id="04abf-179">1</span></span></li>
<li><span data-ttu-id="04abf-180">2</span><span class="sxs-lookup"><span data-stu-id="04abf-180">2</span></span></li>
<li><span data-ttu-id="04abf-181">2</span><span class="sxs-lookup"><span data-stu-id="04abf-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04abf-182">Sie möchten die ersten 25 Prozent der Kosten einer Finanzierungsquelle und den Rest der zweiten Finanzierungsquelle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="04abf-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="04abf-183">Finanzierungsquelle 1</span><span class="sxs-lookup"><span data-stu-id="04abf-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="04abf-184">Finanzierungsquelle 2</span><span class="sxs-lookup"><span data-stu-id="04abf-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04abf-185">25 %</span><span class="sxs-lookup"><span data-stu-id="04abf-185">25%</span></span></li>
<li><span data-ttu-id="04abf-186">100 %</span><span class="sxs-lookup"><span data-stu-id="04abf-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04abf-187">1</span><span class="sxs-lookup"><span data-stu-id="04abf-187">1</span></span></li>
<li><span data-ttu-id="04abf-188">2</span><span class="sxs-lookup"><span data-stu-id="04abf-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="04abf-189">Beispiel Mehrere Finanzierungsquellen (komplex)</span><span class="sxs-lookup"><span data-stu-id="04abf-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="04abf-190">Sie haben drei Finanzierungsquellen, und Sie möchten sie in der folgenden Reihenfolge verwenden:</span><span class="sxs-lookup"><span data-stu-id="04abf-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="04abf-191">Verwenden Sie Finanzierungsquelle 2 und Finanzierungsquelle 3 zu gleichen Teilen, bis Finanzierungsquelle 2 erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="04abf-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="04abf-192">Fahren Sie mit der Nutzung von Finanzierungsquelle 3 fort, bis sie erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="04abf-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="04abf-193">Verwenden Sie Finanzierungsquelle 1, nachdem Finanzierungsquelle 3 erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="04abf-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="04abf-194">Um dies zu erreichen, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="04abf-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="04abf-195">Richten Sie Finanzierungslimits für Finanzierungsquelle 2 und Finanzierungsquelle 3 für die entsprechenden Beträge ein.</span><span class="sxs-lookup"><span data-stu-id="04abf-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="04abf-196">Erstellen Sie die folgenden Finanzierungsregeln:</span><span class="sxs-lookup"><span data-stu-id="04abf-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="04abf-197">Regel 1 (Priorität 1): Weisen Sie 50 Prozent der Buchungen der Finanzierungsquelle 2 und 50 Prozent der Buchungen der Finanzierungsquelle 3 zu.</span><span class="sxs-lookup"><span data-stu-id="04abf-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="04abf-198">Regel 2 (Priorität 2): Weisen Sie 100 Prozent der Buchungen der Finanzierungsquelle 3 zu.</span><span class="sxs-lookup"><span data-stu-id="04abf-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="04abf-199">Regel 3 (Priorität 3): Weisen Sie 100 Prozent der Buchungen der Finanzierungsquelle 1 zu.</span><span class="sxs-lookup"><span data-stu-id="04abf-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="04abf-200">Diese Einstellung funktioniert, da bei Buchungen alle Regeln und Grenzwerte auf ihre Relevanz für die aktuell auszuführende Buchung geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="04abf-201">Wenn keine Regeln oder Grenzwerte für die Buchung gelten, trifft die Regel Alle Buchungen zu.</span><span class="sxs-lookup"><span data-stu-id="04abf-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="04abf-202">Die Regel "Alle Buchungen" gilt für alle Buchungen.</span><span class="sxs-lookup"><span data-stu-id="04abf-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="04abf-203">Wenn das System eine Regel findet, die einer bestimmten Buchung entspricht, wird der Prozentsatz zunächst nach dieser Regel zugewiesen, aber erst angewendet, nachdem die restlichen Grenzwerte geprüft werden, die eingerichtet worden sind.</span><span class="sxs-lookup"><span data-stu-id="04abf-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="04abf-204">Wenn ein Grenzwert erreicht wurde und die Mittel einer Finanzierungsquelle erschöpft sind, wird die dem Finanzierungsgrenzwert zugeordnete Finanzierungsregel ignoriert und die nächste Regel gesucht, die anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="04abf-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="04abf-205">In einigen Fällen kann nur ein Teil der Buchung anhand einer Regel zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="04abf-206">Dies kann der Fall sein, wenn ein Grenzwert beim Zuweisen der Buchung erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="04abf-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="04abf-207">In diesem Fall wird nur ein bestimmter Betrag gemäß der Regel zugewiesen, beispielsweise jeder Finanzierungsquelle 50 Prozent.</span><span class="sxs-lookup"><span data-stu-id="04abf-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="04abf-208">Dies ist gewöhnlich bei Regel 1 der Fall (weiter oben in diesem Abschnitt beschrieben).</span><span class="sxs-lookup"><span data-stu-id="04abf-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="04abf-209">Der Rest wird gemäß der nachfolgenden Regel in der Sequenz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="04abf-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="04abf-210">In der folgenden Tabelle wird dieses Szenario detaillierter überprüft.</span><span class="sxs-lookup"><span data-stu-id="04abf-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04abf-211"><strong>Fokus </strong></span><span class="sxs-lookup"><span data-stu-id="04abf-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="04abf-212"><strong>Detailinformationen </strong></span><span class="sxs-lookup"><span data-stu-id="04abf-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04abf-213">Finanzierungsregeln</span><span class="sxs-lookup"><span data-stu-id="04abf-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="04abf-214">Regel 1 (Priorität 1): Alle Buchungen.</span><span class="sxs-lookup"><span data-stu-id="04abf-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="04abf-215">Finanzierungsquelle 2 50% und Finanzierungsquelle 3 50% zuweisen.</span><span class="sxs-lookup"><span data-stu-id="04abf-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="04abf-216">Regel 2 (Priorität 2): Alle Buchungen.</span><span class="sxs-lookup"><span data-stu-id="04abf-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="04abf-217">Finanzierungsquelle 3 100% zuweisen.</span><span class="sxs-lookup"><span data-stu-id="04abf-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="04abf-218">Regel 3 (Priorität 2): Alle Buchungen.</span><span class="sxs-lookup"><span data-stu-id="04abf-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="04abf-219">Finanzierungsquelle 1 100% zuweisen.</span><span class="sxs-lookup"><span data-stu-id="04abf-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04abf-220">Finanzierungslimits</span><span class="sxs-lookup"><span data-stu-id="04abf-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="04abf-221">Grenzwert für Finanzierungsquelle 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="04abf-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="04abf-222">Grenzwert für Finanzierungsquelle 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="04abf-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="04abf-223">Grenzwert für Finanzierungsquelle 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="04abf-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04abf-224">Buchung 1</span><span class="sxs-lookup"><span data-stu-id="04abf-224">Transaction 1</span></span></td>
<td><span data-ttu-id="04abf-225"><strong>Buchungsbetrag:</strong> 100,00<strong>Finanzierung:</strong> Die Buchung wurde nur gemäß Regel 1 bezahlt, da die Buchung vollständig bezahlt ist, nachdem Regel 1 angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="04abf-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="04abf-226">Die Buchung wird zu gleichen Teilen von Finanzierungsquelle 2 und Finanzierungsquelle 3 finanziert.</span><span class="sxs-lookup"><span data-stu-id="04abf-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="04abf-227">Finanzierungsquelle 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="04abf-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="04abf-228">Finanzierungsquelle 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="04abf-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04abf-229">Buchung 2</span><span class="sxs-lookup"><span data-stu-id="04abf-229">Transaction 2</span></span></td>
<td><span data-ttu-id="04abf-230"><strong>Buchungsbetrag:</strong> 5.000,00<strong>Finanzierung:</strong> Die Zahlung der Buchung gemäß allen drei Regeln.</span><span class="sxs-lookup"><span data-stu-id="04abf-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="04abf-231"><strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="04abf-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="04abf-232">Finanzierungsquelle 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="04abf-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="04abf-233">Finanzierungsquelle 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="04abf-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="04abf-234">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="04abf-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="04abf-235">Finanzierungsquelle 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="04abf-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="04abf-236">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="04abf-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="04abf-237">Finanzierungsquelle 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="04abf-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04abf-238">Gesamtbeträge, die auf die einzelnen Finanzierungsquellen verteilt werden</span><span class="sxs-lookup"><span data-stu-id="04abf-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="04abf-239">Finanzierungsquelle 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="04abf-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="04abf-240">Finanzierungsquelle 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="04abf-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="04abf-241">Finanzierungsquelle 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="04abf-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="04abf-242">Abrechnungsregeln</span><span class="sxs-lookup"><span data-stu-id="04abf-242">Billing rules</span></span>
<span data-ttu-id="04abf-243">Wenn Sie mit einem Debitor einen Projektvertrag aushandeln, legen Sie fest, wie und wann dem Debitor Rechnungen für Arbeit an einem Projekt ausgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="04abf-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="04abf-244">Nachdem Sie den Projektvertrag und das Projekt eingerichtet haben, können Sie Fakturierungsregeln für das Projekt einrichten.</span><span class="sxs-lookup"><span data-stu-id="04abf-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="04abf-245">Fakturierungsregeln basieren auf den Projektbedingungen, die im Projektvertrag angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="04abf-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="04abf-246">Die Fakturierungsregeln, die erstellt werden können, hängen von den Bedingungen im Projektvertrag und dem der Fakturierungsregel zugeordneten Projekttyp ab, z. B. Termin und Material, Festpreis oder Meilenstein.</span><span class="sxs-lookup"><span data-stu-id="04abf-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="04abf-247">Sie können mehrere Fakturierungsregeln für einen Projektvertrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="04abf-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="04abf-248">Sie können eine Fakturierungsregel auch mehreren Projekten zuweisen, die dem gleichen Projektvertrag zugeordnet sind und ähnliche Rechnungsstellungsbedingungen haben.</span><span class="sxs-lookup"><span data-stu-id="04abf-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="04abf-249">Sie können folgende Arten von Fakturierungsregeln einrichten:</span><span class="sxs-lookup"><span data-stu-id="04abf-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="04abf-250">**Liefereinheit** – Rechnungsstellung an einen Debitor, wenn Sie eine Liefereinheit abschließen.</span><span class="sxs-lookup"><span data-stu-id="04abf-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="04abf-251">Sie definieren die Liefereinheiten im Vertrag.</span><span class="sxs-lookup"><span data-stu-id="04abf-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="04abf-252">**Fortschritt** – Rechnungsstellung an einen Debitor erfolgt beim Abschluss eines angegebenen Prozentsatzes des Projekts.</span><span class="sxs-lookup"><span data-stu-id="04abf-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="04abf-253">Sie können eine Fakturierungsregel einrichten, um den Prozentsatz der abgeschlossenen Arbeit automatisch zu berechnen, oder Sie können den abgeschlossenen Prozentsatz der Arbeit und des Betrags manuell berechnen, der dem Debitor in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="04abf-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="04abf-254">**Meilenstein** – Der vollständige Betrag für einen Meilenstein wird dem Debitor beim Erreichen eines Projektmeilensteins in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="04abf-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="04abf-255">**Gebühr** – Es erfolgt die Rechnungsstellung an den Debitor hinsichtlich der Dienstleistungen und einer Verwaltungsgebühr (normalerweise ein Prozentsatz der Dienstleistungskosten).</span><span class="sxs-lookup"><span data-stu-id="04abf-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="04abf-256">**Nach Aufwand** – Berechnen Sie einem Debitor eine Rechnung die Stunden und Materialien für ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="04abf-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="04abf-257">Für alle Typen von Fakturierungsregeln können Sie einen einzubehaltenden Prozentsatz angeben, der von einer Debitorenrechnung abzuziehen ist, bis ein Projekt eine vereinbarte Phase erreicht.</span><span class="sxs-lookup"><span data-stu-id="04abf-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="04abf-258">Der Zahlungseinbehaltungsprozentsatz wird im Projektvertrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="04abf-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="04abf-259">Der Betrag wird an berechnet und abgezogen vom Gesamtwert der Positionen in einer Debitorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="04abf-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="04abf-260">Für **Zeit und Aufwand** und **Fortschritt**-Fakturierungsregeln können Sie fakturierbare Kategorien zuweisen.</span><span class="sxs-lookup"><span data-stu-id="04abf-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="04abf-261">Fakturierbare Kategorien geben die Buchungen an, die in die Debitorenrechnungen eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04abf-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="04abf-262">Wenn eine Rechnung für den Debitor ausgestellt werden kann, wird der für das Projekt in Rechnung zu stellende Betrag auf Grundlage der Fakturierungsregeln berechnet, und es wird ein Vorschlag für eine Projektrechnung generiert.</span><span class="sxs-lookup"><span data-stu-id="04abf-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="04abf-263">In den folgenden Abschnitten finden Sie Beispiele, die zeigen, wie eine Fakturierungsregel für ein Projekt eingerichtet und verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="04abf-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="04abf-264">Beispiel: Erstellen einer Fakturierungsregel auf Grundlage der Anzahl gelieferter Einheiten</span><span class="sxs-lookup"><span data-stu-id="04abf-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="04abf-265">Ihre Organisation vereinbart, insgesamt fünf Schulungssitzungen für die Mitarbeiter eines Debitors mit Kosten von 10.000 Euro pro Schulung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="04abf-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="04abf-266">Sie stellen bei Abschluss jeder Schulungssitzung eine Rechnung an den Debitor aus.</span><span class="sxs-lookup"><span data-stu-id="04abf-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="04abf-267">Bei der Einrichtung der Fakturierungsregeln für den Vertrag verwenden Sie die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="04abf-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="04abf-268">Die Liefereinheit ist eine Schulungssitzung.</span><span class="sxs-lookup"><span data-stu-id="04abf-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="04abf-269">Der Preis je Einheit beträgt 10.000 Euro pro Schulungssitzung.</span><span class="sxs-lookup"><span data-stu-id="04abf-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="04abf-270">Die Gesamtanzahl von Einheiten ist fünf Schulungssitzungen.</span><span class="sxs-lookup"><span data-stu-id="04abf-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="04abf-271">Wenn Sie eine Schulungssitzung abgeschlossen haben, können Sie eine Rechnung über 10.000 Euro für die erste gelieferte Einheit erstellen und die Rechnung an den Debitor senden.</span><span class="sxs-lookup"><span data-stu-id="04abf-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="04abf-272">Beispiel: Erstellen einer Fakturierungsregel auf Grundlage eines angegebenen Prozentsatzes der Projektfertigstellung (manuelle Berechnung)</span><span class="sxs-lookup"><span data-stu-id="04abf-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="04abf-273">Ihre Organisation, eine Softwareberatungsfirma, vereinbart mit einem Debitor, einen Teil eines Produkts zu entwickeln, das der Debitor entwickelt.</span><span class="sxs-lookup"><span data-stu-id="04abf-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="04abf-274">Ihre Organisation sagt zu, den Softwarecode über einen Zeitraum von sechs Monaten zu liefern.</span><span class="sxs-lookup"><span data-stu-id="04abf-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="04abf-275">Der Debitor erklärt sich einverstanden, Ihrer Organisation insgesamt 100.000 Euro für die Arbeit zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="04abf-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="04abf-276">Sie erstellen eine Fakturierungsregel, um dem Debitor auf Grundlage eines Prozentsatzes, zu dem die Arbeit am Projekt gemäß Vertrag abgeschlossen wurde, eine Rechnung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="04abf-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="04abf-277">Am Ende des ersten Monats ermitteln Sie in einer Besprechung mit dem Debitor den abgeschlossenen Prozentsatz der Arbeit.</span><span class="sxs-lookup"><span data-stu-id="04abf-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="04abf-278">Nach einer Prüfung des Projekts durch Sie und den Debitor entscheiden Sie, dass 15 % des Projekts abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="04abf-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="04abf-279">Sie erstellen eine Rechnung in Höhe von 15.000 Euro (15 % von 100.000 Euro) und senden sie an den Debitor.</span><span class="sxs-lookup"><span data-stu-id="04abf-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="04abf-280">Beispiel: Erstellen einer Fakturierungsregel auf Grundlage eines angegebenen Prozentsatzes der Projektfertigstellung (automatische Berechnung)</span><span class="sxs-lookup"><span data-stu-id="04abf-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="04abf-281">Ihre Organisation, eine Softwareentwicklungsfirma, entwickelt ein Lohnbuchhaltungspaket für einen Debitor für 30.000 Euro.</span><span class="sxs-lookup"><span data-stu-id="04abf-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="04abf-282">Der Debitor erklärt sich einverstanden, Ihre Organisation basierend auf dem abgeschlossenen Prozentsatz der Arbeit zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="04abf-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="04abf-283">Ihre Vorkalkulation der Projektkosten beläuft sich auf 20.000 Euro.</span><span class="sxs-lookup"><span data-stu-id="04abf-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="04abf-284">Die im Abrechnungsprozess zu verwendenden Arbeitskategorien sind im Projektvertrag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04abf-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="04abf-285">Sie richten Fakturierungsregeln ein, durch die die Rechnungsbeträge für den abgeschlossenen Prozentsatz der Arbeit für jede Kategorie automatisch berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="04abf-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="04abf-286">Sie richten ein Budget für jede Kategorie ein:</span><span class="sxs-lookup"><span data-stu-id="04abf-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="04abf-287">**Entwicklung** – Kosten von 15.000 Euro und Umsatzerlös von 20.000 Euro</span><span class="sxs-lookup"><span data-stu-id="04abf-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="04abf-288">**Installation** – Kosten von 5.000 Euro und Umsatzerlös von 10.000 Euro.</span><span class="sxs-lookup"><span data-stu-id="04abf-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="04abf-289">Bei der ersten Rechnungsstellung an den Debitor wird der Rechnungsbetrag automatisch anhand der folgenden Informationen berechnet:</span><span class="sxs-lookup"><span data-stu-id="04abf-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="04abf-290">Nach einem Monat sendet die Arbeitskraft bei dem Projekt einen Arbeitszeitnachweis für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="04abf-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="04abf-291">Die Kosten für die Arbeitsstunden der Arbeitskraft belaufen sich auf 5.000 Euro für Entwicklung und 1.000 Euro für Installation.</span><span class="sxs-lookup"><span data-stu-id="04abf-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="04abf-292">Die Entwicklungsarbeit ist zu 33 Prozent abgeschlossen (5.000 Euro tatsächliche Kosten/15.000 Euro Budgetkosten), und die Installationsarbeit ist zu 20 Prozent abgeschlossen (1.000 Euro tatsächliche Kosten/5.000 Euro Budgetkosten).</span><span class="sxs-lookup"><span data-stu-id="04abf-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="04abf-293">Der Rechnungsbetrag von 8.667 wird automatisch berechnet (33 Prozent von 20.000 plus 20 Prozent von 10.000).</span><span class="sxs-lookup"><span data-stu-id="04abf-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="04abf-294">Sie erstellen eine Rechnung in Höhe von 8.667 Euro und senden sie an den Debitor.</span><span class="sxs-lookup"><span data-stu-id="04abf-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="04abf-295">Beispiel: Erstellen einer Fakturierungsregel auf Grundlage vereinbarter Meilensteine</span><span class="sxs-lookup"><span data-stu-id="04abf-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="04abf-296">Ihre Organisation, eine Unternehmensberatungsfirma, führt eine Marktforschung für ein Produkt durch, das der Debitor zu verkaufen plant.</span><span class="sxs-lookup"><span data-stu-id="04abf-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="04abf-297">Der Debitor erklärt sich einverstanden, Ihre Dienstleistungen ab März für einen Zeitraum von drei Monaten in Anspruch zu nehmen und Ihrer Organisation 50.000 Euro zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="04abf-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="04abf-298">Das Projekt umfasst drei Meilensteine:</span><span class="sxs-lookup"><span data-stu-id="04abf-298">The project has three milestones:</span></span>

-   <span data-ttu-id="04abf-299">Meilenstein 1: Sammeln von Verbraucherdaten – 31. März</span><span class="sxs-lookup"><span data-stu-id="04abf-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="04abf-300">Meilenstein 2: Analyse der Verbraucherdaten – 30. April</span><span class="sxs-lookup"><span data-stu-id="04abf-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="04abf-301">Meilenstein 3: Präsentation eines Realisierbarkeitsplans für das Produkt – 31. Mai</span><span class="sxs-lookup"><span data-stu-id="04abf-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="04abf-302">Der Debitor erklärt sich einverstanden, Ihrer Organisation 10.000 Euro für den ersten Meilenstein und jeweils 20.000 Euro für den zweiten und dritten Meilenstein zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="04abf-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="04abf-303">Beim Einrichten des Projektvertrags vereinbaren Sie, basierend auf den abgeschlossenen Meilensteinen Rechnungen an den Debitor auszustellen.</span><span class="sxs-lookup"><span data-stu-id="04abf-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="04abf-304">Zum Einrichten der Fakturierungsregel führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="04abf-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="04abf-305">Definieren Sie die Projektmeilensteine.</span><span class="sxs-lookup"><span data-stu-id="04abf-305">Define the project milestones.</span></span>
-   <span data-ttu-id="04abf-306">Definieren Sie den Betrag, der dem Debitor beim Erreichen des Projektmeilensteins in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="04abf-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="04abf-307">Nach Abschluss des ersten Meilensteins am 31. März markieren Sie diesen als abgeschlossen und erstellen eine Rechnung über 10.000 Euro und senden sie an den Debitor.</span><span class="sxs-lookup"><span data-stu-id="04abf-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="04abf-308">Sie können eine Rechnung für einen Meilenstein erst erstellen, wenn Sie den Meilenstein als abgeschlossen markiert haben.</span><span class="sxs-lookup"><span data-stu-id="04abf-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="04abf-309">Beispiel: Erstellen einer Fakturierungsregel auf Grundlage von Dienstleistungen und einer Verwaltungsgebühr</span><span class="sxs-lookup"><span data-stu-id="04abf-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="04abf-310">Ihre Organisation führt Managementberatungen durch. Sie führt eine Marktforschung zur Bewertung der Realisierbarkeit eines beim Debitor in der Entwicklung befindlichen Produkts durch.</span><span class="sxs-lookup"><span data-stu-id="04abf-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="04abf-311">Die Vereinbarungen legen fest, die Dienstleistungen Ihrer drei besten Unternehmensberater für die Marktforschung auf Aufwandsbasis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="04abf-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="04abf-312">Der Debitor stimmt zu, einen Stundensatz von 100 Euro und eine zusätzliche Verwaltungsgebühr von 10 Prozent für die anfallenden Beratungsstunden für das Projekt zu zahlen.</span><span class="sxs-lookup"><span data-stu-id="04abf-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="04abf-313">Beim Einrichten des Projektvertrags erstellen Sie eine Fakturierungsregel, mit der eine Verwaltungsgebühr von 10 Prozent zu den berechneten Beratungsstunden für das Projekt addiert wird.</span><span class="sxs-lookup"><span data-stu-id="04abf-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="04abf-314">Wenn Sie eine Rechnung für den Debitor erstellen, wird dem Debitor zusätzlich zu den Kosten der Beratungsstunden eine Verwaltungsgebühr von 10 Prozent in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="04abf-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="04abf-315">Wenn die drei Berater z. B. insgesamt 200 Stunden am Projekt gearbeitet haben, wird anhand der folgenden Berechnung eine Rechnung in Höhe von 22.000 Euro erstellt:</span><span class="sxs-lookup"><span data-stu-id="04abf-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="04abf-316">200 Stunden zu 100 Euro pro Stunde = 20.000 Euro</span><span class="sxs-lookup"><span data-stu-id="04abf-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="04abf-317">10-Prozent-Bearbeitungsgebühr = 2.000</span><span class="sxs-lookup"><span data-stu-id="04abf-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="04abf-318">Gesamter Rechnungsbetrag = 22.000</span><span class="sxs-lookup"><span data-stu-id="04abf-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="04abf-319">Wenn Gebühren für einen Debitor steuerpflichtig sind und Sie eine Mehrwertsteuergruppe im Projektvertrag auswählen, wird die Mehrwertsteuergruppe automatisch in eine Fakturierungsregel für Gebühren eingegeben.</span><span class="sxs-lookup"><span data-stu-id="04abf-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="04abf-320">Beispiel: Erstellen einer Fakturierungsregel für die Aufwandskosten</span><span class="sxs-lookup"><span data-stu-id="04abf-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="04abf-321">Ihre Organisation führt Softwareberatungen durch, und hat mit dem Debitor vereinbart, fünf technische Berater für ein Softwareentwicklungsprojekt die nächsten sechs Monate bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="04abf-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="04abf-322">Der Debitor erklärt sich damit einverstanden, einen Betrag von 150 Euro für jede Beratungsstunde und die Kosten für das Büromaterial zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="04abf-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="04abf-323">Ihre Organisation sendet am Ende jedes Monats eine Rechnung an den Debitor.</span><span class="sxs-lookup"><span data-stu-id="04abf-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="04abf-324">Beim Einrichten des Projektvertrags können Sie zustimmen, den Debitor monatlich für den Aufwand für das Projekt zu fakturieren.</span><span class="sxs-lookup"><span data-stu-id="04abf-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="04abf-325">Sie erstellen eine Fakturierungsregel die die folgenden Informationen beinhaltet:</span><span class="sxs-lookup"><span data-stu-id="04abf-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="04abf-326">Die Vertragsdauer beträgt sechs Monate.</span><span class="sxs-lookup"><span data-stu-id="04abf-326">The contract period is six months.</span></span>
-   <span data-ttu-id="04abf-327">Die Beratungsdauer wird mit einem Satz von 150 Euro pro Stunde berechnet.</span><span class="sxs-lookup"><span data-stu-id="04abf-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="04abf-328">Büromaterial wird zu Anschaffungskosten in Rechnung gestellt. Dabei darf die Summe für das Projekt maximal 10.000 Euro betragen.</span><span class="sxs-lookup"><span data-stu-id="04abf-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="04abf-329">Während des Projekts erstellen Sie am Ende jedes Kalendermonats eine Debitorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="04abf-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="04abf-330">Im ersten Monat wurden von den Beratern insgesamt 800 Stunden im Projekt erfasst.</span><span class="sxs-lookup"><span data-stu-id="04abf-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="04abf-331">Die Kosten für das Büromaterial, die für das Projekt berechnet werden, betragen 2.000 Euro.</span><span class="sxs-lookup"><span data-stu-id="04abf-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="04abf-332">Am Ende des Monats erstellen Sie eine Rechnung über 122.000, berechnet als 800 Stunden zu 150 pro Stunde plus 2.000 für Büromaterial.</span><span class="sxs-lookup"><span data-stu-id="04abf-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




