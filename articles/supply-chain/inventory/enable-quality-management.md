---
title: Qualitätsmanagement-Übersicht
description: In diesem Thema wird beschrieben, wie Sie das Qualitätsmanagement in Dynamics 365 Supply Chain Management verwenden können, um die Produktqualität innerhalb der Lieferkette zu verbessern.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba38f9c43fed81768155a27dda88a4bfb4a7828e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653555"
---
# <a name="quality-management-overview"></a><span data-ttu-id="32b29-103">Qualitätsmanagement-Übersicht</span><span class="sxs-lookup"><span data-stu-id="32b29-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32b29-104">In diesem Thema wird beschrieben, wie Sie das Qualitätsmanagement in Dynamics 365 Supply Chain Management verwenden können, um die Produktqualität innerhalb der Lieferkette zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="32b29-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="32b29-105">Das Qualitätsmanagement kann Ihnen dabei helfen, Abfertigungszeiten zu fehlerhaften Produkten zu verwalten (unabhängig vom Ursprung).</span><span class="sxs-lookup"><span data-stu-id="32b29-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="32b29-106">Da Diagnosetypen mit der Korrekturberichterstellung verknüpft sind, kann Supply Chain Management Aufgaben planen, um Probleme zu korrigieren und zu verhindern, dass sie erneut auftreten.</span><span class="sxs-lookup"><span data-stu-id="32b29-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="32b29-107">Zusätzlich zu den Funktionen für die Verwaltung des Qualitätsmangels, umfasst das Qualitätsmanagement Funktionen für die Nachverfolgung von Problemen nach Problemtyp (auch interne Probleme) und zur Kennzeichnung von Lösungen als kurzzeitig oder langfristig.</span><span class="sxs-lookup"><span data-stu-id="32b29-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="32b29-108">Die Statistiken zu Key Performance Indicators (KPIs) geben Einblick in den Verlauf von vorherigen Qualitätsmangelprobleme sowie zu Lösungen zu deren Korrektur.</span><span class="sxs-lookup"><span data-stu-id="32b29-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="32b29-109">Sie können Verlaufsdaten verwenden, um die Effizienz vorheriger Qualitätsmaßnahmen zu prüfen und geeignete Maßnahmen für die Zukunft zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="32b29-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="32b29-110">Wenn Sie eine Qualitätszuordnung festlegen, kann Supply Chain Management Qualitätsprüfungsaufträge für verschiedene Geschäftsprozesse, Ereignisse und Bedingungen generieren.</span><span class="sxs-lookup"><span data-stu-id="32b29-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="32b29-111">Die Qualitätszuordnung kann einen bestimmten Artikel, eine bestimmte Artikelgruppe oder alle Artikel enthalten.</span><span class="sxs-lookup"><span data-stu-id="32b29-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="32b29-112">Beispiele für die Nutzung des Qualitätsmanagements</span><span class="sxs-lookup"><span data-stu-id="32b29-112">Examples of the use of quality management</span></span>
<span data-ttu-id="32b29-113">Das Qualitätsmanagement ist flexibel und kann auf unterschiedliche Weise implementiert werden um die Bedingungen bestimmter Lieferkettenarbeitsgangstufen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="32b29-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="32b29-114">Die folgenden Beispiele zeigen die mögliche Verwendung dieser Funktionen:</span><span class="sxs-lookup"><span data-stu-id="32b29-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="32b29-115">Starten Sie automatisch einen Qualitätskontrollenprozess, basierend auf vordefinierten Kriterien (nach Lagerortregistrierung einer Bestellung von einem bestimmten Kreditor).</span><span class="sxs-lookup"><span data-stu-id="32b29-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="32b29-116">Sperren Sie einen Bestand während der Prüfung, um die Verwendung eines genehmigten Bestands zu unterbinden (vollständige Sperrung von Bestellungsmengen).</span><span class="sxs-lookup"><span data-stu-id="32b29-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="32b29-117">Verwenden Sie die Artikelmusteraufnahme als Teil einer Qualitätszuordnung, um die Menge des aktuellen physischen Bestands zu definieren, der geprüft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="32b29-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="32b29-118">Die Musteraufnahme kann auf festen Mengen oder einem Prozentsatz basieren.</span><span class="sxs-lookup"><span data-stu-id="32b29-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="32b29-119">Erstellen Sie Qualitätsaufträge für Teilbelege.</span><span class="sxs-lookup"><span data-stu-id="32b29-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="32b29-120">Um einen Qualitätsauftrag zu erstellen, der auf der für einen Auftrag physisch erhaltenen Menge basiert, müssen Sie das Kontrollkästchen **Pro aktualisierter Menge** auf dem Formular **Artikelmusteraufnahme** markieren.</span><span class="sxs-lookup"><span data-stu-id="32b29-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="32b29-121">Erstellen Sie Testtypen, die Minimum-, Maximum- und Zielprüfwerte enthalten, und führen Sie Qualitativ-gegen-quantitative-Tests mit vordefinierten Prüfergebnissen aus.</span><span class="sxs-lookup"><span data-stu-id="32b29-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="32b29-122">Legen Sie ein akzeptables Qualitätsniveau (AQL) fest, um die Qualitätsmessungstoleranz zu steuern.</span><span class="sxs-lookup"><span data-stu-id="32b29-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="32b29-123">Geben Sie die Ressourcen an, die ein Inspektionsarbeitsgang erfordert (z. B. ein Testbereich und Testinstrumente).</span><span class="sxs-lookup"><span data-stu-id="32b29-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="32b29-124">Arbeiten mit Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="32b29-124">Working with quality associations</span></span>
<span data-ttu-id="32b29-125">Der Geschäftsprozess, der eine Qualitätszuordnung verwendet, kann sich auf verschiedene Quelldokumente beziehen (z. B. Bestellungen, Aufträge oder Produktionsaufträge).</span><span class="sxs-lookup"><span data-stu-id="32b29-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="32b29-126">Jeder Qualitätszuordnungsdatensatz definiert den Testsatz, das akzeptable Qualitätsniveau (AQL) und den Musteraufnahmeplan, der für die Qualitätsprüfungsaufträge gilt, die generiert werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="32b29-127">Sie müssen einen Qualitätszuordnungsdatensatz für jede Variante in einem Geschäftsprozess definieren.</span><span class="sxs-lookup"><span data-stu-id="32b29-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="32b29-128">So können Sie beispielsweise eine Qualitätszuordnung einrichten, die einen Qualitätsprüfungsauftrag generiert, wenn ein Produktzugang für Bestellungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="32b29-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="32b29-129">Je nach Einrichtung des Ausführungsplans, kann der auslösende Prozess auch gesperrt werden während es einen offenen Qualitätsprüfungsauftrag gibt. Oder die folgenden Prozesse (z. B. das Fakturieren von Bestellungen) können gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="32b29-130">**Hinweis:** Solange es offene Qualitätsprüfungsaufträge gibt, werden Bestandsmengen automatisch für die Ausgabe gesperrt.</span><span class="sxs-lookup"><span data-stu-id="32b29-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="32b29-131">Je nach den **Vollständige Sperrung**-Einstellungen auf der **Artikelmusteraufnahmen**-Seite, ist die Menge entweder die Menge im Qualitätsprüfungsauftrag oder die Menge in der Quelldokumentposition.</span><span class="sxs-lookup"><span data-stu-id="32b29-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="32b29-132">Für einen angegebenen Geschäftsprozess identifiziert Datensatz für Qualitätszuordnungen das Ereignis und Bedingungen, für die ein Qualitätsprüfungsauftrag generiert wird.</span><span class="sxs-lookup"><span data-stu-id="32b29-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="32b29-133">Die Bedingungen können entweder für einen Standort oder für eine juristische Person spezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="32b29-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="32b29-134">Ein Qualitätsprüfungsauftrag mit Zerstörungstests kann nur ausgeführt werden, wenn am Lager Artikel für das Ereignis vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="32b29-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="32b29-135">In den folgenden Beispielen wird die Konfiguration eines Qualitätszuordnungsdatensatzes für die Varianten der einzelnen Geschäftsprozesse erläutert.</span><span class="sxs-lookup"><span data-stu-id="32b29-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="32b29-136">Für jedes Beispiel sind zudem in der folgenden Tabelle die Ereignisse und Bedingungen zusammengefasst, die durch einen Qualitätszuordnungsdatensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="32b29-137">Referenztyp</span><span class="sxs-lookup"><span data-stu-id="32b29-137">Reference type</span></span></th>
<th><span data-ttu-id="32b29-138">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="32b29-138">Event type</span></span></th>
<th><span data-ttu-id="32b29-139">Ausführung</span><span class="sxs-lookup"><span data-stu-id="32b29-139">Execution</span></span></th>
<th><span data-ttu-id="32b29-140">Ereignissperrung</span><span class="sxs-lookup"><span data-stu-id="32b29-140">Event blocking</span></span></th>
<th><span data-ttu-id="32b29-141">Dokumentreferenz</span><span class="sxs-lookup"><span data-stu-id="32b29-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="32b29-142">Bestand</span><span class="sxs-lookup"><span data-stu-id="32b29-142">Inventory</span></span></td>
<td><span data-ttu-id="32b29-143">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="32b29-143">Not applicable</span></span></td>
<td><span data-ttu-id="32b29-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="32b29-144">Not applicable</span></span></td>
<td><span data-ttu-id="32b29-145">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-145">None</span></span></td>
<td><span data-ttu-id="32b29-146">Alle</span><span class="sxs-lookup"><span data-stu-id="32b29-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="32b29-147">Verk.</span><span class="sxs-lookup"><span data-stu-id="32b29-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="32b29-148">Entnahmeprozess wurde geplant</span><span class="sxs-lookup"><span data-stu-id="32b29-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="32b29-149">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-149">Before</span></span></td>
<td><span data-ttu-id="32b29-150">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="32b29-151">Spezifische Kennung, Gruppe oder Alle.</span><span class="sxs-lookup"><span data-stu-id="32b29-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-152">Entnahmeprozess</span><span class="sxs-lookup"><span data-stu-id="32b29-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-153">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="32b29-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-154">Rechnung</span><span class="sxs-lookup"><span data-stu-id="32b29-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="32b29-155">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="32b29-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-156">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-156">Before</span></span></td>
<td><span data-ttu-id="32b29-157">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-158">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="32b29-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-159">Rechnung</span><span class="sxs-lookup"><span data-stu-id="32b29-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="32b29-160">Einkauf</span><span class="sxs-lookup"><span data-stu-id="32b29-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="32b29-161">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="32b29-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="32b29-162">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-162">Before</span></span></td>
<td><span data-ttu-id="32b29-163">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-164">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="32b29-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-165">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="32b29-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-166">Rechnung</span><span class="sxs-lookup"><span data-stu-id="32b29-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="32b29-167">Nach</span><span class="sxs-lookup"><span data-stu-id="32b29-167">After</span></span></td>
<td><span data-ttu-id="32b29-168">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-169">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="32b29-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-170">Rechnung</span><span class="sxs-lookup"><span data-stu-id="32b29-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="32b29-171">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="32b29-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-172">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="32b29-172">Not applicable</span></span></td>
<td><span data-ttu-id="32b29-173">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-174">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="32b29-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-175">Rechnung</span><span class="sxs-lookup"><span data-stu-id="32b29-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="32b29-176">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="32b29-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-177">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-177">Before</span></span></td>
<td><span data-ttu-id="32b29-178">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-179">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="32b29-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-180">Rechnung</span><span class="sxs-lookup"><span data-stu-id="32b29-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="32b29-181">Nach</span><span class="sxs-lookup"><span data-stu-id="32b29-181">After</span></span></td>
<td><span data-ttu-id="32b29-182">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-183">Rechnung</span><span class="sxs-lookup"><span data-stu-id="32b29-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="32b29-184">Produktion</span><span class="sxs-lookup"><span data-stu-id="32b29-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-185">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="32b29-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-186">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="32b29-186">Not applicable</span></span></td>
<td><span data-ttu-id="32b29-187">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="32b29-188">Alle</span><span class="sxs-lookup"><span data-stu-id="32b29-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-189">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="32b29-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-190">Beenden</span><span class="sxs-lookup"><span data-stu-id="32b29-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="32b29-191">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="32b29-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-192">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-192">Before</span></span></td>
<td><span data-ttu-id="32b29-193">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-194">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="32b29-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-195">Beenden</span><span class="sxs-lookup"><span data-stu-id="32b29-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="32b29-196">Nach</span><span class="sxs-lookup"><span data-stu-id="32b29-196">After</span></span></td>
<td><span data-ttu-id="32b29-197">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-198">Beenden</span><span class="sxs-lookup"><span data-stu-id="32b29-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="32b29-199">Quarantäne</span><span class="sxs-lookup"><span data-stu-id="32b29-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-200">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="32b29-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="32b29-201">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-201">Before</span></span></td>
<td><span data-ttu-id="32b29-202">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="32b29-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-203">Beenden</span><span class="sxs-lookup"><span data-stu-id="32b29-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-204">Nach</span><span class="sxs-lookup"><span data-stu-id="32b29-204">After</span></span></td>
<td><span data-ttu-id="32b29-205">Beenden</span><span class="sxs-lookup"><span data-stu-id="32b29-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-206">Beenden</span><span class="sxs-lookup"><span data-stu-id="32b29-206">End</span></span></td>
<td><span data-ttu-id="32b29-207">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-207">Before</span></span></td>
<td><span data-ttu-id="32b29-208">Beenden</span><span class="sxs-lookup"><span data-stu-id="32b29-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="32b29-209">Arbeitsplan-Arbeitsgang</span><span class="sxs-lookup"><span data-stu-id="32b29-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-210">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="32b29-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="32b29-211">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-211">Before</span></span></td>
<td><span data-ttu-id="32b29-212">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-213">Bestimmte Kennung, Gruppe oder Alle und Ressourcenspezifisch, Gruppe oder Alle</span><span class="sxs-lookup"><span data-stu-id="32b29-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-214">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="32b29-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-215">Nach</span><span class="sxs-lookup"><span data-stu-id="32b29-215">After</span></span></td>
<td><span data-ttu-id="32b29-216">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="32b29-217">Kuppelprodukt - Produktion</span><span class="sxs-lookup"><span data-stu-id="32b29-217">Co-product production</span></span></td>
<td><span data-ttu-id="32b29-218">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="32b29-218">Registration</span></span></td>
<td><span data-ttu-id="32b29-219">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="32b29-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-220">Keine</span><span class="sxs-lookup"><span data-stu-id="32b29-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="32b29-221">Alle</span><span class="sxs-lookup"><span data-stu-id="32b29-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="32b29-222">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="32b29-222">Report as finished</span></span></td>
<td><span data-ttu-id="32b29-223">Vor</span><span class="sxs-lookup"><span data-stu-id="32b29-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-224">Nach</span><span class="sxs-lookup"><span data-stu-id="32b29-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="32b29-225">Die folgende Tabelle enthält weitere Informationen darüber, wie Qualitätsprüfungsaufträge für bestimmte Arten von Prozessen generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="32b29-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="32b29-226">Prozesstypen</span><span class="sxs-lookup"><span data-stu-id="32b29-226">Type of process</span></span></th>
<th><span data-ttu-id="32b29-227">Wenn Qualitätsprüfungsaufträge automatisch generiert werden können</span><span class="sxs-lookup"><span data-stu-id="32b29-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="32b29-228">Wenn Qualitätsprüfungsaufträge generiert werden können, wenn Zerstörungstest erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="32b29-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="32b29-229">Bedingungsinformationen</span><span class="sxs-lookup"><span data-stu-id="32b29-229">Condition information</span></span></th>
<th><span data-ttu-id="32b29-230">Manuelle Generierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="32b29-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="32b29-231">Bestellung</span><span class="sxs-lookup"><span data-stu-id="32b29-231">Purchase order</span></span></td>
<td><span data-ttu-id="32b29-232">Bevor oder nachdem eine Zugangsliste oder ein Produktzugang für das erhaltene Material gebucht wird</span><span class="sxs-lookup"><span data-stu-id="32b29-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="32b29-233">Nachdem der Produktzugang für das Material, das erhalten wurde, gebucht wurde, da das Material für Zerstörungstest verfügbar sein muss</span><span class="sxs-lookup"><span data-stu-id="32b29-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="32b29-234">Die Anforderung für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Kreditor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="32b29-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="32b29-235">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Bestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="32b29-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-236">Quarantäneauftrag</span><span class="sxs-lookup"><span data-stu-id="32b29-236">Quarantine order</span></span></td>
<td><span data-ttu-id="32b29-237">Bevor oder nachdem der Quarantäneauftrag als fertig oder abgeschlossen gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="32b29-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="32b29-238">Qualitätsprüfungsaufträge, die Zerstörungstests erfordern, können nicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="32b29-239">Es wird angenommen, dass die Quarantäneaufträge-Funktionen die Disposition des Materials verarbeiten, das zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="32b29-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="32b29-240">Die Anforderung für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Kreditor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="32b29-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="32b29-241">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Quarantänebestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="32b29-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-242">Auftrag</span><span class="sxs-lookup"><span data-stu-id="32b29-242">Sales order</span></span></td>
<td><span data-ttu-id="32b29-243">Vor eine geplanter Entnahmevorgang oder eine Lieferscheinaktualisierung für die zu liefernden Artikel</span><span class="sxs-lookup"><span data-stu-id="32b29-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="32b29-244">Bei einem beliebigen Schritt</span><span class="sxs-lookup"><span data-stu-id="32b29-244">At any step</span></span></td>
<td><span data-ttu-id="32b29-245">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Debitor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="32b29-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="32b29-246">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Auftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="32b29-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-247">Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="32b29-247">Production order</span></span></td>
<td><span data-ttu-id="32b29-248">Bevor oder nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="32b29-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="32b29-249">Nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="32b29-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="32b29-250">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, Debitor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="32b29-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="32b29-251">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Produktionsauftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="32b29-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-252">Produktionsauftrag, der über einen Arbeitsplan-Arbeitsgang verfügt</span><span class="sxs-lookup"><span data-stu-id="32b29-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="32b29-253">Bevor oder nachdem der für einen Arbeitsgang abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="32b29-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="32b29-254">Nachdem die Meldung für den letzten Arbeitsgang abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="32b29-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="32b29-255">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, eine betriebliche Ressource oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="32b29-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="32b29-256">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Arbeitsplan-Arbeitsgang bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="32b29-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32b29-257">Bestand</span><span class="sxs-lookup"><span data-stu-id="32b29-257">Inventory</span></span></td>
<td><span data-ttu-id="32b29-258">Ein Qualitätsprüfungsauftrag kann nicht für eine Buchung in einer Lagererfassung oder für Umlagerungsauftragsbuchungen automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="32b29-259">Ein Qualitätsprüfungsauftrag muss für die Lagermenge eines Artikels manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="32b29-260">Physischer Lagerbestand ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32b29-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="32b29-261">Automatische Generierung von Qualitätsprüfungsaufträgen – Beispiele</span><span class="sxs-lookup"><span data-stu-id="32b29-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="32b29-262">Einkauf</span><span class="sxs-lookup"><span data-stu-id="32b29-262">Purchasing</span></span>

<span data-ttu-id="32b29-263">Im Einkauf, wenn Sie das Feld **Ereignistyp** auf **Produktzugang** und das **Ausführung**-Feld auf **Später** auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="32b29-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="32b29-264">Wenn die Option **Pro aktualisierter Menge** auf **Ja** festgelegt wird, wird ein Qualitätsprüfungsauftrag für jeden Zugang für den Auftrag anhand der Eingangsmenge und Einstellungen in der Artikelmusteraufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="32b29-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="32b29-265">Wenn eine Menge für den Auftrag eingeht, werden neue Qualitätsprüfungsaufträge auf Grundlage der neuen Eingangsmenge generiert.</span><span class="sxs-lookup"><span data-stu-id="32b29-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="32b29-266">Wenn die Option **Pro aktualisierter Menge** auf **Nein** festgelegt wird, wird ein Qualitätsprüfungsauftrag für den ersten Zugang für den Auftrag anhand der Eingangsmenge generiert.</span><span class="sxs-lookup"><span data-stu-id="32b29-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="32b29-267">Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="32b29-268">Qualitätsprüfungsaufträge werden nicht für nachfolgende Zugänge für den Auftrag generiert.</span><span class="sxs-lookup"><span data-stu-id="32b29-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="32b29-269">Qualitätsspezifikation</span><span class="sxs-lookup"><span data-stu-id="32b29-269">Quality specification</span></span></th>
<th><span data-ttu-id="32b29-270">Pro aktualisierter Menge</span><span class="sxs-lookup"><span data-stu-id="32b29-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="32b29-271">Pro Rückverfolgungsangabe</span><span class="sxs-lookup"><span data-stu-id="32b29-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="32b29-272">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="32b29-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="32b29-273">Prozentsatz: 10 %</span><span class="sxs-lookup"><span data-stu-id="32b29-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="32b29-274">Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="32b29-275">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-275">Batch number: No</span></span></p>
<p><span data-ttu-id="32b29-276">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="32b29-277">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="32b29-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="32b29-278">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="32b29-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="32b29-279">Qualitätsprüfungsauftrag Nr. 1 für 3 (10 % von 30)</span><span class="sxs-lookup"><span data-stu-id="32b29-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-280">Fertigmeldung für 70</span><span class="sxs-lookup"><span data-stu-id="32b29-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="32b29-281">Qualitätsprüfungsauftrag Nr. 2 für 7 (10 % verbleibenden Auftragsmenge, die in diesem Fall 70 entspricht)</span><span class="sxs-lookup"><span data-stu-id="32b29-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="32b29-282">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="32b29-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="32b29-283">Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-283">No</span></span></td>
<td>
<p><span data-ttu-id="32b29-284">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-284">Batch number: No</span></span></p>
<p><span data-ttu-id="32b29-285">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="32b29-286">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="32b29-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="32b29-287">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="32b29-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="32b29-288">Qualitätsprüfungsauftrag Nr. 1 wird für 1 erstellt (für die erste als fertig gemeldete Menge, die den festen Wert „1“ hat).</span><span class="sxs-lookup"><span data-stu-id="32b29-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="32b29-289">Es werden keine weiteren Qualitätsprüfungsaufträge für die Restmenge erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-290">Fertigmeldung für 10</span><span class="sxs-lookup"><span data-stu-id="32b29-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="32b29-291">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-292">Fertigmeldung für 60</span><span class="sxs-lookup"><span data-stu-id="32b29-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="32b29-293">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="32b29-294">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="32b29-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="32b29-295">Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="32b29-296">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="32b29-297">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="32b29-298">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="32b29-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="32b29-299">Fertigmeldung für 3</span><span class="sxs-lookup"><span data-stu-id="32b29-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="32b29-300">Qualitätsprüfungsauftrag Nr. 1 für 1 von Charge Nr. b1, Serie Nr. s1</span><span class="sxs-lookup"><span data-stu-id="32b29-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="32b29-301">Qualitätsprüfungsauftrag Nr. 2 für 1 von Charge Nr. b2, Serie Nr. s2</span><span class="sxs-lookup"><span data-stu-id="32b29-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="32b29-302">Qualitätsprüfungsauftrag Nr. 3 für 1 von Charge Nr. b3, Serie Nr. s3</span><span class="sxs-lookup"><span data-stu-id="32b29-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-303">Fertigmeldung für 2</span><span class="sxs-lookup"><span data-stu-id="32b29-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="32b29-304">Qualitätsprüfungsauftrag Nr. 4 für 1 von Charge Nr. b4, Serie Nr. s4</span><span class="sxs-lookup"><span data-stu-id="32b29-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="32b29-305">Qualitätsprüfungsauftrag Nr. 5 für 1 von Charge Nr. b5, Serie Nr. s5</span><span class="sxs-lookup"><span data-stu-id="32b29-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="32b29-306"><strong>Hinweis:</strong> Die Charge kann wiederverwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="32b29-307">Feste Menge: 2</span><span class="sxs-lookup"><span data-stu-id="32b29-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="32b29-308">Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-308">No</span></span></td>
<td>
<p><span data-ttu-id="32b29-309">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="32b29-310">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="32b29-311">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="32b29-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="32b29-312">Fertigmeldung für 4</span><span class="sxs-lookup"><span data-stu-id="32b29-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="32b29-313">Qualitätsprüfungsauftrag Nr. 1 für 1 von Charge Nr. b1, Serie Nr. s1.</span><span class="sxs-lookup"><span data-stu-id="32b29-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="32b29-314">Qualitätsprüfungsauftrag Nr. 2 für 1 von Charge Nr. b2, Serie Nr. s2.</span><span class="sxs-lookup"><span data-stu-id="32b29-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="32b29-315">Qualitätsprüfungsauftrag Nr. 3 für 1 von Charge Nr. b3, Serie Nr. s3.</span><span class="sxs-lookup"><span data-stu-id="32b29-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="32b29-316">Qualitätsprüfungsauftrag Nr. 4 für 1 von Charge Nr. b4, Serie Nr. s4.</span><span class="sxs-lookup"><span data-stu-id="32b29-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="32b29-317">Es werden keine weiteren Qualitätsprüfungsaufträge für die Restmenge erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-318">Fertigmeldung für 6</span><span class="sxs-lookup"><span data-stu-id="32b29-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="32b29-319">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="32b29-320">Produktion</span><span class="sxs-lookup"><span data-stu-id="32b29-320">Production</span></span>

<span data-ttu-id="32b29-321">In der Produktion, wenn Sie das Feld **Ereignistyp** auf **Fertigmeldung** und das **Ausführung**-Feld auf **Später** auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="32b29-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="32b29-322">Wenn die Option **Pro aktualisierter Menge** auf **Ja** festgelegt wird, wird ein Qualitätsprüfungsauftrag auf der Basis einer jeden fertiggestellten Menge und der Einstellungen in der Artikelmusteraufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="32b29-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="32b29-323">Wenn eine Menge für den Produktionsauftrag als fertig gemeldet wird, werden neue Qualitätsprüfungsaufträge auf Grundlage der neuen fertiggestellten Menge generiert.</span><span class="sxs-lookup"><span data-stu-id="32b29-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="32b29-324">Diese Generierungslogik ist mit dem Einkauf konsistent.</span><span class="sxs-lookup"><span data-stu-id="32b29-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="32b29-325">Wenn die Option **Pro aktualisierter Menge** auf **Nein** festgelegt wird, wird ein Qualitätsprüfungsauftrag das erste Mal, wenn eine Menge als fertig gemeldet wird, anhand der fertiggestellten Menge generiert.</span><span class="sxs-lookup"><span data-stu-id="32b29-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="32b29-326">Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen der Artikelmusteraufnahme erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="32b29-327">Qualitätsprüfungsaufträge werden nicht für nachfolgende fertiggestellte Mengen generiert.</span><span class="sxs-lookup"><span data-stu-id="32b29-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="32b29-328">Qualitätsspezifikation</span><span class="sxs-lookup"><span data-stu-id="32b29-328">Quality specification</span></span></th>
<th><span data-ttu-id="32b29-329">Pro aktualisierter Menge</span><span class="sxs-lookup"><span data-stu-id="32b29-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="32b29-330">Pro Rückverfolgungsangabe</span><span class="sxs-lookup"><span data-stu-id="32b29-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="32b29-331">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="32b29-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="32b29-332">Prozentsatz: 10 %</span><span class="sxs-lookup"><span data-stu-id="32b29-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="32b29-333">Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="32b29-334">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-334">Batch number: No</span></span></p>
<p><span data-ttu-id="32b29-335">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="32b29-336">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="32b29-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="32b29-337">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="32b29-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="32b29-338">Qualitätsprüfungsauftrag Nr. 1 für 3 (10 % von 30)</span><span class="sxs-lookup"><span data-stu-id="32b29-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-339">Fertigmeldung für 70</span><span class="sxs-lookup"><span data-stu-id="32b29-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="32b29-340">Qualitätsprüfungsauftrag Nr. 2 für 7 (10 % verbleibenden Auftragsmenge, die in diesem Fall 70 entspricht)</span><span class="sxs-lookup"><span data-stu-id="32b29-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="32b29-341">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="32b29-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="32b29-342">Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-342">No</span></span></td>
<td>
<p><span data-ttu-id="32b29-343">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-343">Batch number: No</span></span></p>
<p><span data-ttu-id="32b29-344">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="32b29-345">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="32b29-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="32b29-346">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="32b29-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="32b29-347">Qualitätsprüfungsauftrag Nr. 1 für 1 (für die erste als fertig gemeldete Menge, die den festen Wert „1“ hat)</span><span class="sxs-lookup"><span data-stu-id="32b29-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="32b29-348">Qualitätsprüfungsauftrag Nr. 2 für 1 (für die verbleibende Menge, die immer noch den festen Wert „1“ hat)</span><span class="sxs-lookup"><span data-stu-id="32b29-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-349">Fertigmeldung für 10</span><span class="sxs-lookup"><span data-stu-id="32b29-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="32b29-350">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-351">Fertigmeldung für 60</span><span class="sxs-lookup"><span data-stu-id="32b29-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="32b29-352">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="32b29-353">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="32b29-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="32b29-354">Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="32b29-355">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="32b29-356">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="32b29-357">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="32b29-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="32b29-358">Fertigmeldung für 3: 1 für Nr. b1, Nr. s1; 1 für Nr. b2, Nr. s2; und 1 für Nr. b3, Nr. s3</span><span class="sxs-lookup"><span data-stu-id="32b29-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="32b29-359">Qualitätsprüfungsauftrag Nr. 1 für 1 von Charge Nr. b1, Serie Nr. s1</span><span class="sxs-lookup"><span data-stu-id="32b29-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="32b29-360">Qualitätsprüfungsauftrag Nr. 2 für 1 von Charge Nr. b2, Serie Nr. s2</span><span class="sxs-lookup"><span data-stu-id="32b29-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="32b29-361">Qualitätsprüfungsauftrag Nr. 3 für 1 von Charge Nr. b3, Serie Nr. s3</span><span class="sxs-lookup"><span data-stu-id="32b29-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-362">Fertigmeldung für 2: 1 für Nr. b4, Nr. s4; und 1 für Nr. b5, Nr. s5</span><span class="sxs-lookup"><span data-stu-id="32b29-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="32b29-363">Qualitätsprüfungsauftrag Nr. 4 für 1 von Charge Nr. b4, Serie Nr. s4</span><span class="sxs-lookup"><span data-stu-id="32b29-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="32b29-364">Qualitätsprüfungsauftrag Nr. 5 für 1 von Charge Nr. b5, Serie Nr. s5</span><span class="sxs-lookup"><span data-stu-id="32b29-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="32b29-365"><strong>Hinweis:</strong> Die Charge kann wiederverwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="32b29-366">Feste Menge: 2</span><span class="sxs-lookup"><span data-stu-id="32b29-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="32b29-367">Nein</span><span class="sxs-lookup"><span data-stu-id="32b29-367">No</span></span></td>
<td>
<p><span data-ttu-id="32b29-368">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="32b29-369">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="32b29-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="32b29-370">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="32b29-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="32b29-371">Fertigmeldung für 4: 1 für Nr. b1, Nr. s1; 1 für Nr. b2, Nr. s2; 1 für Nr. b3, Nr. s3; und 1 für Nr. b4, Nr. s4</span><span class="sxs-lookup"><span data-stu-id="32b29-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="32b29-372">Qualitätsprüfungsauftrag Nr. 1 für 1 von Charge Nr. b1, Serie Nr. s1</span><span class="sxs-lookup"><span data-stu-id="32b29-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="32b29-373">Qualitätsprüfungsauftrag Nr. 2 für 1 von Charge Nr. b2, Serie Nr. s2</span><span class="sxs-lookup"><span data-stu-id="32b29-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="32b29-374">Qualitätsprüfungsauftrag Nr. 3 für 1 von Charge Nr. b3, Serie Nr. s3</span><span class="sxs-lookup"><span data-stu-id="32b29-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="32b29-375">Qualitätsprüfungsauftrag Nr. 4 für 1 von Charge Nr. b4, Serie Nr. s4</span><span class="sxs-lookup"><span data-stu-id="32b29-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="32b29-376">Qualitätsprüfungsauftrag Nr. 5 für 2, ohne Verweis auf eine Charge und Seriennummer</span><span class="sxs-lookup"><span data-stu-id="32b29-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="32b29-377">Fertigmeldung für 6: 1 für Nr. b5, Nr. s5; 1 für Nr. b6, Nr. s6; 1 für Nr. b7, Nr. s7; 1 für Nr. b8, Nr. s8; 1 für Nr. b9, Nr. s9; und 1 für Nr. b10, Nr. s10</span><span class="sxs-lookup"><span data-stu-id="32b29-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="32b29-378">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="32b29-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="32b29-379">Qualitätsmanagementseiten</span><span class="sxs-lookup"><span data-stu-id="32b29-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32b29-380">Seite</span><span class="sxs-lookup"><span data-stu-id="32b29-380">Page</span></span></th>
<th><span data-ttu-id="32b29-381">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32b29-381">Description</span></span></th>
<th><span data-ttu-id="32b29-382">Beispiel</span><span class="sxs-lookup"><span data-stu-id="32b29-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="32b29-383">Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="32b29-383">Quality associations</span></span></td>
<td><span data-ttu-id="32b29-384">Siehe vorherige Abschnitte dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="32b29-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="32b29-385">Eine Qualitätszuordnung definiert alle folgenden Informationen für einen erzeugten Qualitätsprüfungsauftrag:</span><span class="sxs-lookup"><span data-stu-id="32b29-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="32b29-386">Das Buchungsereignis</span><span class="sxs-lookup"><span data-stu-id="32b29-386">The transaction event</span></span></li>
<li><span data-ttu-id="32b29-387">Die Tests, die für die Artikel ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="32b29-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="32b29-388">Das akzeptable Qualitätsniveau</span><span class="sxs-lookup"><span data-stu-id="32b29-388">The AQL</span></span></li>
<li><span data-ttu-id="32b29-389">Den Musteraufnahmeplan</span><span class="sxs-lookup"><span data-stu-id="32b29-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="32b29-390">Sie müssen eine Qualitätszuordnung für jede Variante in einem Geschäftsprozess definieren, die eine automatische Generierung eines Qualitätsprüfungsauftrags erfordert.</span><span class="sxs-lookup"><span data-stu-id="32b29-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="32b29-391">So kann ein Qualitätsprüfungsauftrag beispielsweise in Geschäftsprozessen für Bestellungen, Quarantäneaufträge, Aufträge und Produktionsaufträge generiert werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32b29-392">Tests</span><span class="sxs-lookup"><span data-stu-id="32b29-392">Tests</span></span></td>
<td><span data-ttu-id="32b29-393">Mithilfe dieser Seite können Sie die einzelnen Tests definieren und anzeigen, mit denen ermittelt wird, ob Ihre Produkte den Qualitätsangaben entsprechen.</span><span class="sxs-lookup"><span data-stu-id="32b29-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="32b29-394">Einzelne Tests können einer Testgruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="32b29-395">In diesem Fall werden auch testspezifische Informationen (beispielsweise die zulässigen Messwerte) angegeben.</span><span class="sxs-lookup"><span data-stu-id="32b29-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="32b29-396">Messwerte kommen bei Mengentests, Testvariablen bei Qualitätstests zum Einsatz.</span><span class="sxs-lookup"><span data-stu-id="32b29-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="32b29-397">Ein Mengentest besitzt den Testtyp <strong>Ganzzahl</strong> oder <strong>Bruchteil</strong> sowie eine Angabe für die Maßeinheit.</span><span class="sxs-lookup"><span data-stu-id="32b29-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="32b29-398">Qualitätsangaben und Testergebnisse werden in Zahlen ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="32b29-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="32b29-399">Für einen Qualitätstest wird der Testtyp <strong>Option</strong> verwendet.</span><span class="sxs-lookup"><span data-stu-id="32b29-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="32b29-400">Qualitative Tests erfordern zusätzliche Informationen über die zu messende Variable und die zugehörigen Optionen.</span><span class="sxs-lookup"><span data-stu-id="32b29-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="32b29-401">Qualitätsangaben und Testergebnisse werden gemäß einem Ergebnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="32b29-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="32b29-402">Ein Produktionsunternehmen führt zwei Tests für eingekauftes Material durch: einen Mengentest für die Materialqualität und einen Qualitätstest für Verpackungsschäden.</span><span class="sxs-lookup"><span data-stu-id="32b29-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="32b29-403">Für den Qualitätstest werden weitere Informationen definiert, um die Testvariable (beschädigte Verpackung) und die Ergebnisse zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="32b29-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="32b29-404">Auf der Seite <strong>Testgruppen</strong> werden die beiden Tests einer Testgruppe zugeordnet und die testspezifischen Informationen angegeben.</span><span class="sxs-lookup"><span data-stu-id="32b29-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="32b29-405">Die Testgruppe wird einem Qualitätsprüfungsauftrag zugeordnet, sodass das Unternehmen einen Bericht über die Testergebnisse für die beiden Tests erhält.</span><span class="sxs-lookup"><span data-stu-id="32b29-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32b29-406">Testgruppen</span><span class="sxs-lookup"><span data-stu-id="32b29-406">Test groups</span></span></td>
<td><span data-ttu-id="32b29-407">Mithilfe dieser Seite können Sie Testgruppen und die einzelnen Tests einrichten, bearbeiten und anzeigen, die einer Testgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="32b29-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="32b29-408">Im oberen Bereich werden Testgruppen, im unteren Bereich die Tests angezeigt, die einer ausgewählten Testgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="32b29-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="32b29-409">Sie ordnen einer Testgruppe mehrere Richtlinien zu, z. B. einen Musteraufnahmeplan, eine akzeptables Qualitätsniveau und die Anforderungen für Zerstörungstests.</span><span class="sxs-lookup"><span data-stu-id="32b29-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="32b29-410">Wenn Sie einer Testgruppe einen einzelnen Test zuweisen, können Sie zusätzliche Informationen definieren (z. B. die Sequenz, Dokumente und Prüfdaten).</span><span class="sxs-lookup"><span data-stu-id="32b29-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="32b29-411">Bei einem Mengentest zählen zu den zu definierenden Informationen auch die akzeptablen Messwerte.</span><span class="sxs-lookup"><span data-stu-id="32b29-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="32b29-412">Bei einem Qualitätstest zählen hierzu auch die Testvariable und das Standardergebnis.</span><span class="sxs-lookup"><span data-stu-id="32b29-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="32b29-413">Die einem Qualitätsprüfungsauftrag zugeordnete Testgruppe definiert die Tests, die für den angegebenen Artikel ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="32b29-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="32b29-414">Tests für die Qualitätsprüfung können jedoch hinzugefügt, geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="32b29-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="32b29-415">Testergebnisse werden für jeden Test im Qualitätsprüfungsauftrag gemeldet.</span><span class="sxs-lookup"><span data-stu-id="32b29-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="32b29-416">Ein Produktionsunternehmen definiert eine Testgruppe für jede Abweichung von den Qualitätsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="32b29-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="32b29-417">In den verschiedenen Testgruppen sind Unterschiede in den Musteraufnahmeplänen, die zusammen auszuführenden Tests, das akzeptable Qualitätsniveau und andere Faktoren enthalten.</span><span class="sxs-lookup"><span data-stu-id="32b29-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="32b29-418">Bei Mengentests sind zudem Unterschiede hinsichtlich der akzeptablen Messwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="32b29-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="32b29-419">Um die Qualitätsrichtlinien durchzusetzen weißt das Unternehmen jeder Regel eine Testgruppe zum automatischen Erstellen von Qualitätsprüfungsaufträgen zu (im Formular <strong>Qualitätszuordnungen</strong>) und weißt eine Testgruppe zu den manuell erstellten Qualitätsprüfungsaufträgen zu.</span><span class="sxs-lookup"><span data-stu-id="32b29-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32b29-420">Artikelqualitätsgruppen</span><span class="sxs-lookup"><span data-stu-id="32b29-420">Item quality groups</span></span></td>
<td><span data-ttu-id="32b29-421">Mithilfe dieser Seite können Sie die Artikel, die einer Qualitätsgruppe zugewiesen sind, oder die Qualitätsgruppen, die einem Artikel zugewiesen sind, einrichten, bearbeiten und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="32b29-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="32b29-422">Eine Qualitätsgruppe gibt Aufschluss über allgemeine Testanforderungen für Artikel.</span><span class="sxs-lookup"><span data-stu-id="32b29-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="32b29-423">Nachdem Sie die Testanforderungen auf der Seite <strong>Testgruppen</strong> definiert haben, können die Regeln für die automatische Generierung von Qualitätsprüfungsaufträgen definieren.</span><span class="sxs-lookup"><span data-stu-id="32b29-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="32b29-424">Um den Vorgang zu vereinfachen, definieren Sie keine Regeln für einzelne Artikel.</span><span class="sxs-lookup"><span data-stu-id="32b29-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="32b29-425">Stattdessen definieren Sie Regeln für eine Qualitätsgruppe, indem Sie die Seite <strong>Qualitätszuordnungen</strong> verwenden.</span><span class="sxs-lookup"><span data-stu-id="32b29-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="32b29-426">Sie können auch die Seite <strong>Artikelqualitätsgruppen</strong> für eine ausgewählte Qualitätsgruppe verwenden, um dieser Gruppe geeignete Artikel zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="32b29-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="32b29-427">Sie können auch die Seite <strong>Artikelqualitätsgruppen</strong> für eine ausgewählte Qualitätsgruppe verwenden, um dieser dem Artikel passende Qualitätsgruppen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="32b29-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="32b29-428">Ein Produktionsunternehmen erwirbt verschiedene Rohstoffe, bei denen die gleichen Testanforderungen zur Prüfung eingehender Waren gelten.</span><span class="sxs-lookup"><span data-stu-id="32b29-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="32b29-429">Das Unternehmen definiert eine Qualitätsgruppe und weist die zugehörigen Artikelnummern der Rohstoffe der Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="32b29-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="32b29-430">Später erwirbt das Unternehmen einen neuen Rohstofftyp, für den die gleichen Testanforderungen gelten.</span><span class="sxs-lookup"><span data-stu-id="32b29-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="32b29-431">Anstatt neue Testanforderungen für den neuen Rohstoff einzurichten, fügt das Unternehmen die Artikelnummer neuen Materials der vorhandenen Qualitätsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="32b29-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="32b29-432">Das gleiche Produktionsunternehmen produziert auch Artikel, für die die gleichen Produktionstestanforderungen gelten, und liefert Artikel mit den gleichen Anforderungen für die Durchführung von Tests vor der Lieferung.</span><span class="sxs-lookup"><span data-stu-id="32b29-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="32b29-433">Das Unternehmen definiert zwei zusätzliche Qualitätsgruppen und weist dann jeder Qualitätsgruppe die entsprechenden Artikelnummern zu.</span><span class="sxs-lookup"><span data-stu-id="32b29-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32b29-434">Testvariablen</span><span class="sxs-lookup"><span data-stu-id="32b29-434">Test variables</span></span></td>
<td><span data-ttu-id="32b29-435">Mit dieser Seite können Sie das die Variablen definieren und anzeigen, die Qualitätstests zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="32b29-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="32b29-436">Für jede Variable definieren Sie Ergebnisaufzählungen, die die möglichen Optionen darstellen.</span><span class="sxs-lookup"><span data-stu-id="32b29-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="32b29-437">Sie definieren Tests auf der <strong>Tests</strong>-Seite.</span><span class="sxs-lookup"><span data-stu-id="32b29-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="32b29-438">Bei Mengentests müssen Sie den Testtyp auf <strong>Option</strong> festlegen.</span><span class="sxs-lookup"><span data-stu-id="32b29-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="32b29-439">Verwenden Sie die Seite <strong>Testgruppen</strong>, um einem einzelnen Test eine Testvariable zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="32b29-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="32b29-440">Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="32b29-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="32b29-441">Diese Abnahmeprüfung besitzt mehrere Variablen.</span><span class="sxs-lookup"><span data-stu-id="32b29-441">This inspection test has several variables.</span></span> <span data-ttu-id="32b29-442">Eine Variable ist der Geschmack, wobei die möglichen Ergebnisse "gut" oder "schlecht" lauten.</span><span class="sxs-lookup"><span data-stu-id="32b29-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="32b29-443">Eine zweite Variable ist die Farbe, bei der die möglichen Ergebnisse "zu dunkel", "zu hell" und "in Ordnung" sind.</span><span class="sxs-lookup"><span data-stu-id="32b29-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32b29-444">Ergebnisse für Testvariable</span><span class="sxs-lookup"><span data-stu-id="32b29-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="32b29-445">Mithilfe dieser Seite werden die möglichen Testergebnisse für eine Testvariable geändert, die einem Qualitätstest zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="32b29-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="32b29-446">Für jedes Ergebnis weisen Sie entweder den Status <strong>Erfolgreich</strong> oder <strong>Fehlgeschlagen</strong> zu.</span><span class="sxs-lookup"><span data-stu-id="32b29-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="32b29-447">Definieren Sie eine Variable und die Ergebnisse für jeden Qualitätstest, der auf der Seite <strong>Tests</strong> definiert ist.</span><span class="sxs-lookup"><span data-stu-id="32b29-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="32b29-448">(Für Qualitätstests, wird der Testtyp auf der Seite <strong>Option</strong> auf <strong>Tests</strong>) gesetzt. Verwenden Sie die Seite <strong>Testgruppen</strong>, um eine Testvariable und ein Standardergebnis einzelnem Qualitätstest zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="32b29-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="32b29-449">Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="32b29-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="32b29-450">Diese Abnahmeprüfung besitzt mehrere Variablen.</span><span class="sxs-lookup"><span data-stu-id="32b29-450">This inspection test has of several variables.</span></span> <span data-ttu-id="32b29-451">Eine Variable ist der Geschmack, wobei die möglichen Ergebnisse "gut" oder "schlecht" lauten.</span><span class="sxs-lookup"><span data-stu-id="32b29-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="32b29-452">Eine zweite Variable ist die Farbe, bei der die möglichen Ergebnisse "zu dunkel", "zu hell" und "in Ordnung" sind.</span><span class="sxs-lookup"><span data-stu-id="32b29-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="32b29-453">Für jedes Ergebnis wird der Status <strong>Erfolgreich</strong> oder <strong>Fehlgeschlagen</strong> festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32b29-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="32b29-454">Während der Abnahmeprüfung für jede Variable meldet der Inspektor das Testergebnis, indem er eines der Ergebnisse auswählt.</span><span class="sxs-lookup"><span data-stu-id="32b29-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="32b29-455">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="32b29-455">Additional resources</span></span>
--------

[<span data-ttu-id="32b29-456">Qualitätsmanagementprozesse</span><span class="sxs-lookup"><span data-stu-id="32b29-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="32b29-457">Verwaltung von Qualitätsmängeln aktivieren</span><span class="sxs-lookup"><span data-stu-id="32b29-457">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
