---
title: Qualitätsmanagement-Übersicht
description: In diesem Thema wird beschrieben, wie Sie das Qualitätsmanagement in Dynamics 365 Supply Chain Management verwenden können, um die Produktqualität innerhalb der Lieferkette zu verbessern.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b090450c6b39607f9661667f8063998bbe5ff52
ms.sourcegitcommit: c79062ba89498aa3fe3d86e478d9f32484f5f6dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/03/2020
ms.locfileid: "3224908"
---
# <a name="quality-management-overview"></a><span data-ttu-id="70ab9-103">Qualitätsmanagement-Übersicht</span><span class="sxs-lookup"><span data-stu-id="70ab9-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70ab9-104">In diesem Thema wird beschrieben, wie Sie das Qualitätsmanagement in Dynamics 365 Supply Chain Management verwenden können, um die Produktqualität innerhalb der Lieferkette zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="70ab9-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="70ab9-105">Das Qualitätsmanagement kann Ihnen dabei helfen, Abfertigungszeiten zu fehlerhaften Produkten zu verwalten (unabhängig vom Ursprung).</span><span class="sxs-lookup"><span data-stu-id="70ab9-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="70ab9-106">Da Diagnosetypen mit der Korrekturberichterstellung verknüpft sind, kann Supply Chain Management Aufgaben planen, um Probleme zu korrigieren und zu verhindern, dass sie erneut auftreten.</span><span class="sxs-lookup"><span data-stu-id="70ab9-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="70ab9-107">Zusätzlich zu den Funktionen für die Verwaltung des Qualitätsmangels, umfasst das Qualitätsmanagement Funktionen für die Nachverfolgung von Problemen nach Problemtyp (auch interne Probleme) und zur Kennzeichnung von Lösungen als kurzzeitig oder langfristig.</span><span class="sxs-lookup"><span data-stu-id="70ab9-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="70ab9-108">Die Statistiken zu Key Performance Indicators (KPIs) geben Einblick in den Verlauf von vorherigen Qualitätsmangelprobleme sowie zu Lösungen zu deren Korrektur.</span><span class="sxs-lookup"><span data-stu-id="70ab9-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="70ab9-109">Sie können Verlaufsdaten verwenden, um die Effizienz vorheriger Qualitätsmaßnahmen zu prüfen und geeignete Maßnahmen für die Zukunft zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="70ab9-110">Wenn Sie eine Qualitätszuordnung festlegen, kann Supply Chain Management Qualitätsprüfungsaufträge für verschiedene Geschäftsprozesse, Ereignisse und Bedingungen generieren.</span><span class="sxs-lookup"><span data-stu-id="70ab9-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="70ab9-111">Die Qualitätszuordnung kann einen bestimmten Artikel, eine bestimmte Artikelgruppe oder alle Artikel enthalten.</span><span class="sxs-lookup"><span data-stu-id="70ab9-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="70ab9-112">Beispiele für die Nutzung des Qualitätsmanagements</span><span class="sxs-lookup"><span data-stu-id="70ab9-112">Examples of the use of quality management</span></span>
<span data-ttu-id="70ab9-113">Das Qualitätsmanagement ist flexibel und kann auf unterschiedliche Weise implementiert werden um die Bedingungen bestimmter Lieferkettenarbeitsgangstufen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="70ab9-114">Die folgenden Beispiele zeigen die mögliche Verwendung dieser Funktionen:</span><span class="sxs-lookup"><span data-stu-id="70ab9-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="70ab9-115">Starten Sie automatisch einen Qualitätskontrollenprozess, basierend auf vordefinierten Kriterien (nach Lagerortregistrierung einer Bestellung von einem bestimmten Kreditor).</span><span class="sxs-lookup"><span data-stu-id="70ab9-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="70ab9-116">Sperren Sie einen Bestand während der Prüfung, um die Verwendung eines genehmigten Bestands zu unterbinden (vollständige Sperrung von Bestellungsmengen).</span><span class="sxs-lookup"><span data-stu-id="70ab9-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="70ab9-117">Verwenden Sie die Artikelmusteraufnahme als Teil einer Qualitätszuordnung, um die Menge des aktuellen physischen Bestands zu definieren, der geprüft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="70ab9-118">Die Musteraufnahme kann auf festen Mengen oder einem Prozentsatz basieren.</span><span class="sxs-lookup"><span data-stu-id="70ab9-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="70ab9-119">Erstellen Sie Qualitätsaufträge für Teilbelege.</span><span class="sxs-lookup"><span data-stu-id="70ab9-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="70ab9-120">Um einen Qualitätsauftrag zu erstellen, der auf der für einen Auftrag physisch erhaltenen Menge basiert, müssen Sie das Kontrollkästchen **Pro aktualisierter Menge** auf dem Formular **Artikelmusteraufnahme** markieren.</span><span class="sxs-lookup"><span data-stu-id="70ab9-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="70ab9-121">Erstellen Sie Testtypen, die Minimum-, Maximum- und Zielprüfwerte enthalten, und führen Sie Qualitativ-gegen-quantitative-Tests mit vordefinierten Prüfergebnissen aus.</span><span class="sxs-lookup"><span data-stu-id="70ab9-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="70ab9-122">Legen Sie ein akzeptables Qualitätsniveau (AQL) fest, um die Qualitätsmessungstoleranz zu steuern.</span><span class="sxs-lookup"><span data-stu-id="70ab9-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="70ab9-123">Geben Sie die Ressourcen an, die ein Inspektionsarbeitsgang erfordert (z. B. ein Testbereich und Testinstrumente).</span><span class="sxs-lookup"><span data-stu-id="70ab9-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="70ab9-124">Arbeiten mit Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="70ab9-124">Working with quality associations</span></span>
<span data-ttu-id="70ab9-125">Der Geschäftsprozess, der eine Qualitätszuordnung verwendet, kann sich auf verschiedene Quelldokumente beziehen (z. B. Bestellungen, Aufträge oder Produktionsaufträge).</span><span class="sxs-lookup"><span data-stu-id="70ab9-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="70ab9-126">Jeder Qualitätszuordnungsdatensatz definiert den Testsatz, das akzeptable Qualitätsniveau (AQL) und den Musteraufnahmeplan, der für die Qualitätsprüfungsaufträge gilt, die generiert werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="70ab9-127">Sie müssen einen Qualitätszuordnungsdatensatz für jede Variante in einem Geschäftsprozess definieren.</span><span class="sxs-lookup"><span data-stu-id="70ab9-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="70ab9-128">So können Sie beispielsweise eine Qualitätszuordnung einrichten, die einen Qualitätsprüfungsauftrag generiert, wenn ein Produktzugang für Bestellungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="70ab9-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="70ab9-129">Je nach Einrichtung des Ausführungsplans, kann der auslösende Prozess auch gesperrt werden während es einen offenen Qualitätsprüfungsauftrag gibt. Oder die folgenden Prozesse (z. B. das Fakturieren von Bestellungen) können gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="70ab9-130">**Hinweis:** Solange es offene Qualitätsprüfungsaufträge gibt, werden Bestandsmengen automatisch für die Ausgabe gesperrt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="70ab9-131">Je nach den **Vollständige Sperrung**-Einstellungen auf der **Artikelmusteraufnahmen**-Seite, ist die Menge entweder die Menge im Qualitätsprüfungsauftrag oder die Menge in der Quelldokumentposition.</span><span class="sxs-lookup"><span data-stu-id="70ab9-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="70ab9-132">Für einen angegebenen Geschäftsprozess identifiziert Datensatz für Qualitätszuordnungen das Ereignis und Bedingungen, für die ein Qualitätsprüfungsauftrag generiert wird.</span><span class="sxs-lookup"><span data-stu-id="70ab9-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="70ab9-133">Die Bedingungen können entweder für einen Standort oder für eine juristische Person spezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="70ab9-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="70ab9-134">Ein Qualitätsprüfungsauftrag mit Zerstörungstests kann nur ausgeführt werden, wenn am Lager Artikel für das Ereignis vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="70ab9-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="70ab9-135">In den folgenden Beispielen wird die Konfiguration eines Qualitätszuordnungsdatensatzes für die Varianten der einzelnen Geschäftsprozesse erläutert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="70ab9-136">Für jedes Beispiel sind zudem in der folgenden Tabelle die Ereignisse und Bedingungen zusammengefasst, die durch einen Qualitätszuordnungsdatensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="70ab9-137">Referenztyp</span><span class="sxs-lookup"><span data-stu-id="70ab9-137">Reference type</span></span></th>
<th><span data-ttu-id="70ab9-138">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="70ab9-138">Event type</span></span></th>
<th><span data-ttu-id="70ab9-139">Ausführung</span><span class="sxs-lookup"><span data-stu-id="70ab9-139">Execution</span></span></th>
<th><span data-ttu-id="70ab9-140">Ereignissperrung</span><span class="sxs-lookup"><span data-stu-id="70ab9-140">Event blocking</span></span></th>
<th><span data-ttu-id="70ab9-141">Dokumentreferenz</span><span class="sxs-lookup"><span data-stu-id="70ab9-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="70ab9-142">Bestand</span><span class="sxs-lookup"><span data-stu-id="70ab9-142">Inventory</span></span></td>
<td><span data-ttu-id="70ab9-143">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="70ab9-143">Not applicable</span></span></td>
<td><span data-ttu-id="70ab9-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="70ab9-144">Not applicable</span></span></td>
<td><span data-ttu-id="70ab9-145">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-145">None</span></span></td>
<td><span data-ttu-id="70ab9-146">Alle</span><span class="sxs-lookup"><span data-stu-id="70ab9-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="70ab9-147">Verk.</span><span class="sxs-lookup"><span data-stu-id="70ab9-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="70ab9-148">Entnahmeprozess wurde geplant</span><span class="sxs-lookup"><span data-stu-id="70ab9-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="70ab9-149">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-149">Before</span></span></td>
<td><span data-ttu-id="70ab9-150">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="70ab9-151">Spezifische Kennung, Gruppe oder Alle.</span><span class="sxs-lookup"><span data-stu-id="70ab9-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-152">Entnahmeprozess</span><span class="sxs-lookup"><span data-stu-id="70ab9-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-153">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="70ab9-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-154">Rechnung</span><span class="sxs-lookup"><span data-stu-id="70ab9-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="70ab9-155">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="70ab9-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-156">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-156">Before</span></span></td>
<td><span data-ttu-id="70ab9-157">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-158">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="70ab9-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-159">Rechnung</span><span class="sxs-lookup"><span data-stu-id="70ab9-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="70ab9-160">Einkauf</span><span class="sxs-lookup"><span data-stu-id="70ab9-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="70ab9-161">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="70ab9-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="70ab9-162">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-162">Before</span></span></td>
<td><span data-ttu-id="70ab9-163">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-164">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="70ab9-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-165">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="70ab9-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-166">Rechnung</span><span class="sxs-lookup"><span data-stu-id="70ab9-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="70ab9-167">Nach</span><span class="sxs-lookup"><span data-stu-id="70ab9-167">After</span></span></td>
<td><span data-ttu-id="70ab9-168">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-169">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="70ab9-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-170">Rechnung</span><span class="sxs-lookup"><span data-stu-id="70ab9-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="70ab9-171">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="70ab9-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-172">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="70ab9-172">Not applicable</span></span></td>
<td><span data-ttu-id="70ab9-173">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-174">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="70ab9-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-175">Rechnung</span><span class="sxs-lookup"><span data-stu-id="70ab9-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="70ab9-176">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="70ab9-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-177">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-177">Before</span></span></td>
<td><span data-ttu-id="70ab9-178">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-179">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="70ab9-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-180">Rechnung</span><span class="sxs-lookup"><span data-stu-id="70ab9-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="70ab9-181">Nach</span><span class="sxs-lookup"><span data-stu-id="70ab9-181">After</span></span></td>
<td><span data-ttu-id="70ab9-182">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-183">Rechnung</span><span class="sxs-lookup"><span data-stu-id="70ab9-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="70ab9-184">Produktion</span><span class="sxs-lookup"><span data-stu-id="70ab9-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-185">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="70ab9-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-186">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="70ab9-186">Not applicable</span></span></td>
<td><span data-ttu-id="70ab9-187">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="70ab9-188">Alle</span><span class="sxs-lookup"><span data-stu-id="70ab9-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-189">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="70ab9-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-190">Beenden</span><span class="sxs-lookup"><span data-stu-id="70ab9-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="70ab9-191">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="70ab9-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-192">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-192">Before</span></span></td>
<td><span data-ttu-id="70ab9-193">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-194">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="70ab9-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-195">Beenden</span><span class="sxs-lookup"><span data-stu-id="70ab9-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="70ab9-196">Nach</span><span class="sxs-lookup"><span data-stu-id="70ab9-196">After</span></span></td>
<td><span data-ttu-id="70ab9-197">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-198">Beenden</span><span class="sxs-lookup"><span data-stu-id="70ab9-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="70ab9-199">Quarantäne</span><span class="sxs-lookup"><span data-stu-id="70ab9-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-200">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="70ab9-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="70ab9-201">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-201">Before</span></span></td>
<td><span data-ttu-id="70ab9-202">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="70ab9-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-203">Beenden</span><span class="sxs-lookup"><span data-stu-id="70ab9-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-204">Nach</span><span class="sxs-lookup"><span data-stu-id="70ab9-204">After</span></span></td>
<td><span data-ttu-id="70ab9-205">Beenden</span><span class="sxs-lookup"><span data-stu-id="70ab9-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-206">Beenden</span><span class="sxs-lookup"><span data-stu-id="70ab9-206">End</span></span></td>
<td><span data-ttu-id="70ab9-207">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-207">Before</span></span></td>
<td><span data-ttu-id="70ab9-208">Beenden</span><span class="sxs-lookup"><span data-stu-id="70ab9-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="70ab9-209">Arbeitsplan-Arbeitsgang</span><span class="sxs-lookup"><span data-stu-id="70ab9-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-210">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="70ab9-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="70ab9-211">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-211">Before</span></span></td>
<td><span data-ttu-id="70ab9-212">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-213">Bestimmte Kennung, Gruppe oder Alle und Ressourcenspezifisch, Gruppe oder Alle</span><span class="sxs-lookup"><span data-stu-id="70ab9-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-214">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="70ab9-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-215">Nach</span><span class="sxs-lookup"><span data-stu-id="70ab9-215">After</span></span></td>
<td><span data-ttu-id="70ab9-216">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="70ab9-217">Kuppelprodukt - Produktion</span><span class="sxs-lookup"><span data-stu-id="70ab9-217">Co-product production</span></span></td>
<td><span data-ttu-id="70ab9-218">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="70ab9-218">Registration</span></span></td>
<td><span data-ttu-id="70ab9-219">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="70ab9-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-220">Keine</span><span class="sxs-lookup"><span data-stu-id="70ab9-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="70ab9-221">Alle</span><span class="sxs-lookup"><span data-stu-id="70ab9-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="70ab9-222">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="70ab9-222">Report as finished</span></span></td>
<td><span data-ttu-id="70ab9-223">Vor</span><span class="sxs-lookup"><span data-stu-id="70ab9-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-224">Nach</span><span class="sxs-lookup"><span data-stu-id="70ab9-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="70ab9-225">Die folgende Tabelle enthält weitere Informationen darüber, wie Qualitätsprüfungsaufträge für bestimmte Arten von Prozessen generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="70ab9-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="70ab9-226">Prozesstypen</span><span class="sxs-lookup"><span data-stu-id="70ab9-226">Type of process</span></span></th>
<th><span data-ttu-id="70ab9-227">Wenn Qualitätsprüfungsaufträge automatisch generiert werden können</span><span class="sxs-lookup"><span data-stu-id="70ab9-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="70ab9-228">Wenn Qualitätsprüfungsaufträge generiert werden können, wenn Zerstörungstest erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="70ab9-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="70ab9-229">Bedingungsinformationen</span><span class="sxs-lookup"><span data-stu-id="70ab9-229">Condition information</span></span></th>
<th><span data-ttu-id="70ab9-230">Manuelle Generierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="70ab9-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="70ab9-231">Bestellung</span><span class="sxs-lookup"><span data-stu-id="70ab9-231">Purchase order</span></span></td>
<td><span data-ttu-id="70ab9-232">Bevor oder nachdem eine Zugangsliste oder ein Produktzugang für das erhaltene Material gebucht wird</span><span class="sxs-lookup"><span data-stu-id="70ab9-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="70ab9-233">Nachdem der Produktzugang für das Material, das erhalten wurde, gebucht wurde, da das Material für Zerstörungstest verfügbar sein muss</span><span class="sxs-lookup"><span data-stu-id="70ab9-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="70ab9-234">Die Anforderung für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Kreditor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="70ab9-235">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Bestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-236">Quarantäneauftrag</span><span class="sxs-lookup"><span data-stu-id="70ab9-236">Quarantine order</span></span></td>
<td><span data-ttu-id="70ab9-237">Bevor oder nachdem der Quarantäneauftrag als fertig oder abgeschlossen gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="70ab9-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="70ab9-238">Qualitätsprüfungsaufträge, die Zerstörungstests erfordern, können nicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="70ab9-239">Es wird angenommen, dass die Quarantäneaufträge-Funktionen die Disposition des Materials verarbeiten, das zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="70ab9-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="70ab9-240">Die Anforderung für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Kreditor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="70ab9-241">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Quarantänebestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-242">Auftrag</span><span class="sxs-lookup"><span data-stu-id="70ab9-242">Sales order</span></span></td>
<td><span data-ttu-id="70ab9-243">Vor eine geplanter Entnahmevorgang oder eine Lieferscheinaktualisierung für die zu liefernden Artikel</span><span class="sxs-lookup"><span data-stu-id="70ab9-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="70ab9-244">Bei einem beliebigen Schritt</span><span class="sxs-lookup"><span data-stu-id="70ab9-244">At any step</span></span></td>
<td><span data-ttu-id="70ab9-245">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Debitor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="70ab9-246">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Auftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-247">Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="70ab9-247">Production order</span></span></td>
<td><span data-ttu-id="70ab9-248">Bevor oder nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="70ab9-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="70ab9-249">Nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="70ab9-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="70ab9-250">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, Debitor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="70ab9-251">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Produktionsauftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-252">Produktionsauftrag, der über einen Arbeitsplan-Arbeitsgang verfügt</span><span class="sxs-lookup"><span data-stu-id="70ab9-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="70ab9-253">Bevor oder nachdem der für einen Arbeitsgang abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="70ab9-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="70ab9-254">Nachdem die Meldung für den letzten Arbeitsgang abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="70ab9-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="70ab9-255">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, eine betriebliche Ressource oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="70ab9-256">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Arbeitsplan-Arbeitsgang bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-257">Bestand</span><span class="sxs-lookup"><span data-stu-id="70ab9-257">Inventory</span></span></td>
<td><span data-ttu-id="70ab9-258">Ein Qualitätsprüfungsauftrag kann nicht für eine Buchung in einer Lagererfassung oder für Umlagerungsauftragsbuchungen automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="70ab9-259">Ein Qualitätsprüfungsauftrag muss für die Lagermenge eines Artikels manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="70ab9-260">Physischer Lagerbestand ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="70ab9-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="70ab9-261">Automatische Generierung von Qualitätsprüfungsaufträgen – Beispiele</span><span class="sxs-lookup"><span data-stu-id="70ab9-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="70ab9-262">Einkauf</span><span class="sxs-lookup"><span data-stu-id="70ab9-262">Purchasing</span></span>

<span data-ttu-id="70ab9-263">Im Einkauf, wenn Sie das Feld **Ereignistyp** auf **Produktzugang** und das **Ausführung**-Feld auf **Später** auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="70ab9-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="70ab9-264">Wenn die Option **Pro aktualisierter Menge** auf **Ja** festgelegt wird, wird ein Qualitätsprüfungsauftrag für jeden Zugang für den Auftrag anhand der Eingangsmenge und Einstellungen in der Artikelmusteraufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="70ab9-265">Wenn eine Menge für den Auftrag eingeht, werden neue Qualitätsprüfungsaufträge auf Grundlage der neuen Eingangsmenge generiert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="70ab9-266">Wenn die Option **Pro aktualisierter Menge** auf **Nein** festgelegt wird, wird ein Qualitätsprüfungsauftrag für den ersten Zugang für den Auftrag anhand der Eingangsmenge generiert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="70ab9-267">Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="70ab9-268">Qualitätsprüfungsaufträge werden nicht für nachfolgende Zugänge für den Auftrag generiert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="70ab9-269">Produktion</span><span class="sxs-lookup"><span data-stu-id="70ab9-269">Production</span></span>

<span data-ttu-id="70ab9-270">In der Produktion, wenn Sie das Feld **Ereignistyp** auf **Fertigmeldung** und das **Ausführung**-Feld auf **Später** auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="70ab9-270">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="70ab9-271">Wenn die Option **Pro aktualisierter Menge** auf **Ja** festgelegt wird, wird ein Qualitätsprüfungsauftrag auf der Basis einer jeden fertiggestellten Menge und der Einstellungen in der Artikelmusteraufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-271">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="70ab9-272">Wenn eine Menge für den Produktionsauftrag als fertig gemeldet wird, werden neue Qualitätsprüfungsaufträge auf Grundlage der neuen fertiggestellten Menge generiert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-272">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="70ab9-273">Diese Generierungslogik ist mit dem Einkauf konsistent.</span><span class="sxs-lookup"><span data-stu-id="70ab9-273">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="70ab9-274">Wenn die Option **Pro aktualisierter Menge** auf **Nein** festgelegt wird, wird ein Qualitätsprüfungsauftrag das erste Mal, wenn eine Menge als fertig gemeldet wird, anhand der fertiggestellten Menge generiert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-274">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="70ab9-275">Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen der Artikelmusteraufnahme erstellt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-275">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="70ab9-276">Qualitätsprüfungsaufträge werden nicht für nachfolgende fertiggestellte Mengen generiert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-276">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="70ab9-277">Qualitätsspezifikation</span><span class="sxs-lookup"><span data-stu-id="70ab9-277">Quality specification</span></span></th>
<th><span data-ttu-id="70ab9-278">Pro aktualisierter Menge</span><span class="sxs-lookup"><span data-stu-id="70ab9-278">Per updated quantity</span></span></th>
<th><span data-ttu-id="70ab9-279">Pro Rückverfolgungsangabe</span><span class="sxs-lookup"><span data-stu-id="70ab9-279">Per tracking dimension</span></span></th>
<th><span data-ttu-id="70ab9-280">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="70ab9-280">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="70ab9-281">Prozentsatz: 10 %</span><span class="sxs-lookup"><span data-stu-id="70ab9-281">Percentage: 10%</span></span></td>
<td><span data-ttu-id="70ab9-282">Ja</span><span class="sxs-lookup"><span data-stu-id="70ab9-282">Yes</span></span></td>
<td>
<p><span data-ttu-id="70ab9-283">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="70ab9-283">Batch number: No</span></span></p>
<p><span data-ttu-id="70ab9-284">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="70ab9-284">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="70ab9-285">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="70ab9-285">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="70ab9-286">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="70ab9-286">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="70ab9-287">Qualitätsprüfungsauftrag Nr. 1 für 3 (10 % von 30)</span><span class="sxs-lookup"><span data-stu-id="70ab9-287">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="70ab9-288">Fertigmeldung für 70</span><span class="sxs-lookup"><span data-stu-id="70ab9-288">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="70ab9-289">Qualitätsprüfungsauftrag Nr. 2 für 7 (10 % verbleibenden Auftragsmenge, die in diesem Fall 70 entspricht)</span><span class="sxs-lookup"><span data-stu-id="70ab9-289">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-290">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="70ab9-290">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="70ab9-291">Nein</span><span class="sxs-lookup"><span data-stu-id="70ab9-291">No</span></span></td>
<td>
<p><span data-ttu-id="70ab9-292">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="70ab9-292">Batch number: No</span></span></p>
<p><span data-ttu-id="70ab9-293">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="70ab9-293">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="70ab9-294">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="70ab9-294">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="70ab9-295">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="70ab9-295">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="70ab9-296">Qualitätsprüfungsauftrag Nr. 1 für 1 (für die erste als fertig gemeldete Menge, die den festen Wert „1“ hat)</span><span class="sxs-lookup"><span data-stu-id="70ab9-296">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="70ab9-297">Qualitätsprüfungsauftrag Nr. 2 für 1 (für die verbleibende Menge, die immer noch den festen Wert „1“ hat)</span><span class="sxs-lookup"><span data-stu-id="70ab9-297">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="70ab9-298">Fertigmeldung für 10</span><span class="sxs-lookup"><span data-stu-id="70ab9-298">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="70ab9-299">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-299">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="70ab9-300">Fertigmeldung für 60</span><span class="sxs-lookup"><span data-stu-id="70ab9-300">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="70ab9-301">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-301">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-302">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="70ab9-302">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="70ab9-303">Ja</span><span class="sxs-lookup"><span data-stu-id="70ab9-303">Yes</span></span></td>
<td>
<p><span data-ttu-id="70ab9-304">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="70ab9-304">Batch number: Yes</span></span></p>
<p><span data-ttu-id="70ab9-305">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="70ab9-305">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="70ab9-306">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="70ab9-306">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="70ab9-307">Fertigmeldung für 3: 1 für Nr. b1, Nr. s1; 1 für Nr. b2, Nr. s2; und 1 für Nr. b3, Nr. s3</span><span class="sxs-lookup"><span data-stu-id="70ab9-307">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="70ab9-308">Qualitätsprüfungsauftrag Nr. 1 für 1 von Charge Nr. b1, Serie Nr. s1</span><span class="sxs-lookup"><span data-stu-id="70ab9-308">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="70ab9-309">Qualitätsprüfungsauftrag Nr. 2 für 1 von Charge Nr. b2, Serie Nr. s2</span><span class="sxs-lookup"><span data-stu-id="70ab9-309">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="70ab9-310">Qualitätsprüfungsauftrag Nr. 3 für 1 von Charge Nr. b3, Serie Nr. s3</span><span class="sxs-lookup"><span data-stu-id="70ab9-310">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="70ab9-311">Fertigmeldung für 2: 1 für Nr. b4, Nr. s4; und 1 für Nr. b5, Nr. s5</span><span class="sxs-lookup"><span data-stu-id="70ab9-311">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="70ab9-312">Qualitätsprüfungsauftrag Nr. 4 für 1 von Charge Nr. b4, Serie Nr. s4</span><span class="sxs-lookup"><span data-stu-id="70ab9-312">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="70ab9-313">Qualitätsprüfungsauftrag Nr. 5 für 1 von Charge Nr. b5, Serie Nr. s5</span><span class="sxs-lookup"><span data-stu-id="70ab9-313">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="70ab9-314"><strong>Hinweis:</strong> Die Charge kann wiederverwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-314"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="70ab9-315">Feste Menge: 2</span><span class="sxs-lookup"><span data-stu-id="70ab9-315">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="70ab9-316">Nein</span><span class="sxs-lookup"><span data-stu-id="70ab9-316">No</span></span></td>
<td>
<p><span data-ttu-id="70ab9-317">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="70ab9-317">Batch number: Yes</span></span></p>
<p><span data-ttu-id="70ab9-318">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="70ab9-318">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="70ab9-319">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="70ab9-319">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="70ab9-320">Fertigmeldung für 4: 1 für Nr. b1, Nr. s1; 1 für Nr. b2, Nr. s2; 1 für Nr. b3, Nr. s3; und 1 für Nr. b4, Nr. s4</span><span class="sxs-lookup"><span data-stu-id="70ab9-320">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="70ab9-321">Qualitätsprüfungsauftrag Nr. 1 für 1 von Charge Nr. b1, Serie Nr. s1</span><span class="sxs-lookup"><span data-stu-id="70ab9-321">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="70ab9-322">Qualitätsprüfungsauftrag Nr. 2 für 1 von Charge Nr. b2, Serie Nr. s2</span><span class="sxs-lookup"><span data-stu-id="70ab9-322">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="70ab9-323">Qualitätsprüfungsauftrag Nr. 3 für 1 von Charge Nr. b3, Serie Nr. s3</span><span class="sxs-lookup"><span data-stu-id="70ab9-323">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="70ab9-324">Qualitätsprüfungsauftrag Nr. 4 für 1 von Charge Nr. b4, Serie Nr. s4</span><span class="sxs-lookup"><span data-stu-id="70ab9-324">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="70ab9-325">Qualitätsprüfungsauftrag Nr. 5 für 2, ohne Verweis auf eine Charge und Seriennummer</span><span class="sxs-lookup"><span data-stu-id="70ab9-325">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="70ab9-326">Fertigmeldung für 6: 1 für Nr. b5, Nr. s5; 1 für Nr. b6, Nr. s6; 1 für Nr. b7, Nr. s7; 1 für Nr. b8, Nr. s8; 1 für Nr. b9, Nr. s9; und 1 für Nr. b10, Nr. s10</span><span class="sxs-lookup"><span data-stu-id="70ab9-326">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="70ab9-327">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-327">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="70ab9-328">Qualitätsmanagementseiten</span><span class="sxs-lookup"><span data-stu-id="70ab9-328">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70ab9-329">Seite</span><span class="sxs-lookup"><span data-stu-id="70ab9-329">Page</span></span></th>
<th><span data-ttu-id="70ab9-330">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70ab9-330">Description</span></span></th>
<th><span data-ttu-id="70ab9-331">Beispiel</span><span class="sxs-lookup"><span data-stu-id="70ab9-331">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70ab9-332">Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="70ab9-332">Quality associations</span></span></td>
<td><span data-ttu-id="70ab9-333">Siehe vorherige Abschnitte dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="70ab9-333">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="70ab9-334">Eine Qualitätszuordnung definiert alle folgenden Informationen für einen erzeugten Qualitätsprüfungsauftrag:</span><span class="sxs-lookup"><span data-stu-id="70ab9-334">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="70ab9-335">Das Buchungsereignis</span><span class="sxs-lookup"><span data-stu-id="70ab9-335">The transaction event</span></span></li>
<li><span data-ttu-id="70ab9-336">Die Tests, die für die Artikel ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-336">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="70ab9-337">Das akzeptable Qualitätsniveau</span><span class="sxs-lookup"><span data-stu-id="70ab9-337">The AQL</span></span></li>
<li><span data-ttu-id="70ab9-338">Den Musteraufnahmeplan</span><span class="sxs-lookup"><span data-stu-id="70ab9-338">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="70ab9-339">Sie müssen eine Qualitätszuordnung für jede Variante in einem Geschäftsprozess definieren, die eine automatische Generierung eines Qualitätsprüfungsauftrags erfordert.</span><span class="sxs-lookup"><span data-stu-id="70ab9-339">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="70ab9-340">So kann ein Qualitätsprüfungsauftrag beispielsweise in Geschäftsprozessen für Bestellungen, Quarantäneaufträge, Aufträge und Produktionsaufträge generiert werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-340">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70ab9-341">Tests</span><span class="sxs-lookup"><span data-stu-id="70ab9-341">Tests</span></span></td>
<td><span data-ttu-id="70ab9-342">Mithilfe dieser Seite können Sie die einzelnen Tests definieren und anzeigen, mit denen ermittelt wird, ob Ihre Produkte den Qualitätsangaben entsprechen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-342">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="70ab9-343">Einzelne Tests können einer Testgruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-343">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="70ab9-344">In diesem Fall werden auch testspezifische Informationen (beispielsweise die zulässigen Messwerte) angegeben.</span><span class="sxs-lookup"><span data-stu-id="70ab9-344">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="70ab9-345">Messwerte kommen bei Mengentests, Testvariablen bei Qualitätstests zum Einsatz.</span><span class="sxs-lookup"><span data-stu-id="70ab9-345">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="70ab9-346">Ein Mengentest besitzt den Testtyp <strong>Ganzzahl</strong> oder <strong>Bruchteil</strong> sowie eine Angabe für die Maßeinheit.</span><span class="sxs-lookup"><span data-stu-id="70ab9-346">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="70ab9-347">Qualitätsangaben und Testergebnisse werden in Zahlen ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-347">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="70ab9-348">Für einen Qualitätstest wird der Testtyp <strong>Option</strong> verwendet.</span><span class="sxs-lookup"><span data-stu-id="70ab9-348">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="70ab9-349">Qualitative Tests erfordern zusätzliche Informationen über die zu messende Variable und die zugehörigen Optionen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-349">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="70ab9-350">Qualitätsangaben und Testergebnisse werden gemäß einem Ergebnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-350">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="70ab9-351">Ein Produktionsunternehmen führt zwei Tests für eingekauftes Material durch: einen Mengentest für die Materialqualität und einen Qualitätstest für Verpackungsschäden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-351">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="70ab9-352">Für den Qualitätstest werden weitere Informationen definiert, um die Testvariable (beschädigte Verpackung) und die Ergebnisse zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-352">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="70ab9-353">Auf der Seite <strong>Testgruppen</strong> werden die beiden Tests einer Testgruppe zugeordnet und die testspezifischen Informationen angegeben.</span><span class="sxs-lookup"><span data-stu-id="70ab9-353">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="70ab9-354">Die Testgruppe wird einem Qualitätsprüfungsauftrag zugeordnet, sodass das Unternehmen einen Bericht über die Testergebnisse für die beiden Tests erhält.</span><span class="sxs-lookup"><span data-stu-id="70ab9-354">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70ab9-355">Testgruppen</span><span class="sxs-lookup"><span data-stu-id="70ab9-355">Test groups</span></span></td>
<td><span data-ttu-id="70ab9-356">Mithilfe dieser Seite können Sie Testgruppen und die einzelnen Tests einrichten, bearbeiten und anzeigen, die einer Testgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="70ab9-356">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="70ab9-357">Im oberen Bereich werden Testgruppen, im unteren Bereich die Tests angezeigt, die einer ausgewählten Testgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="70ab9-357">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="70ab9-358">Sie ordnen einer Testgruppe mehrere Richtlinien zu, z. B. einen Musteraufnahmeplan, eine akzeptables Qualitätsniveau und die Anforderungen für Zerstörungstests.</span><span class="sxs-lookup"><span data-stu-id="70ab9-358">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="70ab9-359">Wenn Sie einer Testgruppe einen einzelnen Test zuweisen, können Sie zusätzliche Informationen definieren (z. B. die Sequenz, Dokumente und Prüfdaten).</span><span class="sxs-lookup"><span data-stu-id="70ab9-359">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="70ab9-360">Bei einem Mengentest zählen zu den zu definierenden Informationen auch die akzeptablen Messwerte.</span><span class="sxs-lookup"><span data-stu-id="70ab9-360">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="70ab9-361">Bei einem Qualitätstest zählen hierzu auch die Testvariable und das Standardergebnis.</span><span class="sxs-lookup"><span data-stu-id="70ab9-361">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="70ab9-362">Die einem Qualitätsprüfungsauftrag zugeordnete Testgruppe definiert die Tests, die für den angegebenen Artikel ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-362">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="70ab9-363">Tests für die Qualitätsprüfung können jedoch hinzugefügt, geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-363">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="70ab9-364">Testergebnisse werden für jeden Test im Qualitätsprüfungsauftrag gemeldet.</span><span class="sxs-lookup"><span data-stu-id="70ab9-364">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="70ab9-365">Ein Produktionsunternehmen definiert eine Testgruppe für jede Abweichung von den Qualitätsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="70ab9-365">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="70ab9-366">In den verschiedenen Testgruppen sind Unterschiede in den Musteraufnahmeplänen, die zusammen auszuführenden Tests, das akzeptable Qualitätsniveau und andere Faktoren enthalten.</span><span class="sxs-lookup"><span data-stu-id="70ab9-366">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="70ab9-367">Bei Mengentests sind zudem Unterschiede hinsichtlich der akzeptablen Messwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="70ab9-367">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="70ab9-368">Um die Qualitätsrichtlinien durchzusetzen weißt das Unternehmen jeder Regel eine Testgruppe zum automatischen Erstellen von Qualitätsprüfungsaufträgen zu (im Formular <strong>Qualitätszuordnungen</strong>) und weißt eine Testgruppe zu den manuell erstellten Qualitätsprüfungsaufträgen zu.</span><span class="sxs-lookup"><span data-stu-id="70ab9-368">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70ab9-369">Artikelqualitätsgruppen</span><span class="sxs-lookup"><span data-stu-id="70ab9-369">Item quality groups</span></span></td>
<td><span data-ttu-id="70ab9-370">Mithilfe dieser Seite können Sie die Artikel, die einer Qualitätsgruppe zugewiesen sind, oder die Qualitätsgruppen, die einem Artikel zugewiesen sind, einrichten, bearbeiten und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-370">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="70ab9-371">Eine Qualitätsgruppe gibt Aufschluss über allgemeine Testanforderungen für Artikel.</span><span class="sxs-lookup"><span data-stu-id="70ab9-371">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="70ab9-372">Nachdem Sie die Testanforderungen auf der Seite <strong>Testgruppen</strong> definiert haben, können die Regeln für die automatische Generierung von Qualitätsprüfungsaufträgen definieren.</span><span class="sxs-lookup"><span data-stu-id="70ab9-372">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="70ab9-373">Um den Vorgang zu vereinfachen, definieren Sie keine Regeln für einzelne Artikel.</span><span class="sxs-lookup"><span data-stu-id="70ab9-373">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="70ab9-374">Stattdessen definieren Sie Regeln für eine Qualitätsgruppe, indem Sie die Seite <strong>Qualitätszuordnungen</strong> verwenden.</span><span class="sxs-lookup"><span data-stu-id="70ab9-374">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="70ab9-375">Sie können auch die Seite <strong>Artikelqualitätsgruppen</strong> für eine ausgewählte Qualitätsgruppe verwenden, um dieser Gruppe geeignete Artikel zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-375">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="70ab9-376">Sie können auch die Seite <strong>Artikelqualitätsgruppen</strong> für eine ausgewählte Qualitätsgruppe verwenden, um dieser dem Artikel passende Qualitätsgruppen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-376">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="70ab9-377">Ein Produktionsunternehmen erwirbt verschiedene Rohstoffe, bei denen die gleichen Testanforderungen zur Prüfung eingehender Waren gelten.</span><span class="sxs-lookup"><span data-stu-id="70ab9-377">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="70ab9-378">Das Unternehmen definiert eine Qualitätsgruppe und weist die zugehörigen Artikelnummern der Rohstoffe der Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="70ab9-378">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="70ab9-379">Später erwirbt das Unternehmen einen neuen Rohstofftyp, für den die gleichen Testanforderungen gelten.</span><span class="sxs-lookup"><span data-stu-id="70ab9-379">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="70ab9-380">Anstatt neue Testanforderungen für den neuen Rohstoff einzurichten, fügt das Unternehmen die Artikelnummer neuen Materials der vorhandenen Qualitätsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="70ab9-380">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="70ab9-381">Das gleiche Produktionsunternehmen produziert auch Artikel, für die die gleichen Produktionstestanforderungen gelten, und liefert Artikel mit den gleichen Anforderungen für die Durchführung von Tests vor der Lieferung.</span><span class="sxs-lookup"><span data-stu-id="70ab9-381">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="70ab9-382">Das Unternehmen definiert zwei zusätzliche Qualitätsgruppen und weist dann jeder Qualitätsgruppe die entsprechenden Artikelnummern zu.</span><span class="sxs-lookup"><span data-stu-id="70ab9-382">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70ab9-383">Testvariablen</span><span class="sxs-lookup"><span data-stu-id="70ab9-383">Test variables</span></span></td>
<td><span data-ttu-id="70ab9-384">Mit dieser Seite können Sie das die Variablen definieren und anzeigen, die Qualitätstests zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="70ab9-384">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="70ab9-385">Für jede Variable definieren Sie Ergebnisaufzählungen, die die möglichen Optionen darstellen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-385">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="70ab9-386">Sie definieren Tests auf der <strong>Tests</strong>-Seite.</span><span class="sxs-lookup"><span data-stu-id="70ab9-386">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="70ab9-387">Bei Mengentests müssen Sie den Testtyp auf <strong>Option</strong> festlegen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-387">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="70ab9-388">Verwenden Sie die Seite <strong>Testgruppen</strong>, um einem einzelnen Test eine Testvariable zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-388">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="70ab9-389">Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="70ab9-389">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="70ab9-390">Diese Abnahmeprüfung besitzt mehrere Variablen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-390">This inspection test has several variables.</span></span> <span data-ttu-id="70ab9-391">Eine Variable ist der Geschmack, wobei die möglichen Ergebnisse "gut" oder "schlecht" lauten.</span><span class="sxs-lookup"><span data-stu-id="70ab9-391">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="70ab9-392">Eine zweite Variable ist die Farbe, bei der die möglichen Ergebnisse "zu dunkel", "zu hell" und "in Ordnung" sind.</span><span class="sxs-lookup"><span data-stu-id="70ab9-392">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70ab9-393">Ergebnisse für Testvariable</span><span class="sxs-lookup"><span data-stu-id="70ab9-393">Test variable outcomes</span></span></td>
<td><span data-ttu-id="70ab9-394">Mithilfe dieser Seite werden die möglichen Testergebnisse für eine Testvariable geändert, die einem Qualitätstest zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="70ab9-394">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="70ab9-395">Für jedes Ergebnis weisen Sie entweder den Status <strong>Erfolgreich</strong> oder <strong>Fehlgeschlagen</strong> zu.</span><span class="sxs-lookup"><span data-stu-id="70ab9-395">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="70ab9-396">Definieren Sie eine Variable und die Ergebnisse für jeden Qualitätstest, der auf der Seite <strong>Tests</strong> definiert ist.</span><span class="sxs-lookup"><span data-stu-id="70ab9-396">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="70ab9-397">(Für Qualitätstests, wird der Testtyp auf der Seite <strong>Option</strong> auf <strong>Tests</strong>) gesetzt. Verwenden Sie die Seite <strong>Testgruppen</strong>, um eine Testvariable und ein Standardergebnis einzelnem Qualitätstest zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-397">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="70ab9-398">Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="70ab9-398">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="70ab9-399">Diese Abnahmeprüfung besitzt mehrere Variablen.</span><span class="sxs-lookup"><span data-stu-id="70ab9-399">This inspection test has of several variables.</span></span> <span data-ttu-id="70ab9-400">Eine Variable ist der Geschmack, wobei die möglichen Ergebnisse "gut" oder "schlecht" lauten.</span><span class="sxs-lookup"><span data-stu-id="70ab9-400">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="70ab9-401">Eine zweite Variable ist die Farbe, bei der die möglichen Ergebnisse "zu dunkel", "zu hell" und "in Ordnung" sind.</span><span class="sxs-lookup"><span data-stu-id="70ab9-401">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="70ab9-402">Für jedes Ergebnis wird der Status <strong>Erfolgreich</strong> oder <strong>Fehlgeschlagen</strong> festgelegt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-402">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="70ab9-403">Während der Abnahmeprüfung für jede Variable meldet der Inspektor das Testergebnis, indem er eines der Ergebnisse auswählt.</span><span class="sxs-lookup"><span data-stu-id="70ab9-403">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="70ab9-404">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="70ab9-404">Additional resources</span></span>
--------

[<span data-ttu-id="70ab9-405">Qualitätsmanagementprozesse</span><span class="sxs-lookup"><span data-stu-id="70ab9-405">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="70ab9-406">Qualitätsmangelverwaltung</span><span class="sxs-lookup"><span data-stu-id="70ab9-406">Nonconformance management</span></span>](enable-nonconformance-management.md)
