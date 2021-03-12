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
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 711ce21d0e522a737e6307e7de1889c8badd5ce0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005226"
---
# <a name="quality-management-overview"></a><span data-ttu-id="a9417-103">Qualitätsmanagement-Übersicht</span><span class="sxs-lookup"><span data-stu-id="a9417-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9417-104">In diesem Thema wird beschrieben, wie Sie das Qualitätsmanagement in Dynamics 365 Supply Chain Management verwenden können, um die Produktqualität innerhalb der Lieferkette zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a9417-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="a9417-105">Das Qualitätsmanagement kann Ihnen dabei helfen, Abfertigungszeiten zu fehlerhaften Produkten zu verwalten (unabhängig vom Ursprung).</span><span class="sxs-lookup"><span data-stu-id="a9417-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="a9417-106">Da Diagnosetypen mit der Korrekturberichterstellung verknüpft sind, kann Supply Chain Management Aufgaben planen, um Probleme zu korrigieren und zu verhindern, dass sie erneut auftreten.</span><span class="sxs-lookup"><span data-stu-id="a9417-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="a9417-107">Zusätzlich zu den Funktionen für die Verwaltung des Qualitätsmangels, umfasst das Qualitätsmanagement Funktionen für die Nachverfolgung von Problemen nach Problemtyp (auch interne Probleme) und zur Kennzeichnung von Lösungen als kurzzeitig oder langfristig.</span><span class="sxs-lookup"><span data-stu-id="a9417-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="a9417-108">Die Statistiken zu Key Performance Indicators (KPIs) geben Einblick in den Verlauf von vorherigen Qualitätsmangelprobleme sowie zu Lösungen zu deren Korrektur.</span><span class="sxs-lookup"><span data-stu-id="a9417-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="a9417-109">Sie können Verlaufsdaten verwenden, um die Effizienz vorheriger Qualitätsmaßnahmen zu prüfen und geeignete Maßnahmen für die Zukunft zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a9417-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="a9417-110">Wenn Sie eine Qualitätszuordnung festlegen, kann Supply Chain Management Qualitätsprüfungsaufträge für verschiedene Geschäftsprozesse, Ereignisse und Bedingungen generieren.</span><span class="sxs-lookup"><span data-stu-id="a9417-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="a9417-111">Die Qualitätszuordnung kann einen bestimmten Artikel, eine bestimmte Artikelgruppe oder alle Artikel enthalten.</span><span class="sxs-lookup"><span data-stu-id="a9417-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="a9417-112">Beispiele für die Nutzung des Qualitätsmanagements</span><span class="sxs-lookup"><span data-stu-id="a9417-112">Examples of the use of quality management</span></span>
<span data-ttu-id="a9417-113">Das Qualitätsmanagement ist flexibel und kann auf unterschiedliche Weise implementiert werden um die Bedingungen bestimmter Lieferkettenarbeitsgangstufen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a9417-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="a9417-114">Die folgenden Beispiele zeigen die mögliche Verwendung dieser Funktionen:</span><span class="sxs-lookup"><span data-stu-id="a9417-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="a9417-115">Starten Sie automatisch einen Qualitätskontrollenprozess, basierend auf vordefinierten Kriterien (nach Lagerortregistrierung einer Bestellung von einem bestimmten Kreditor).</span><span class="sxs-lookup"><span data-stu-id="a9417-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="a9417-116">Sperren Sie einen Bestand während der Prüfung, um die Verwendung eines genehmigten Bestands zu unterbinden (vollständige Sperrung von Bestellungsmengen).</span><span class="sxs-lookup"><span data-stu-id="a9417-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="a9417-117">Verwenden Sie die Artikelmusteraufnahme als Teil einer Qualitätszuordnung, um die Menge des aktuellen physischen Bestands zu definieren, der geprüft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a9417-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="a9417-118">Die Musteraufnahme kann auf festen Mengen, einem Prozentsatz oder einem vollständigen Kennzeichen basieren.</span><span class="sxs-lookup"><span data-stu-id="a9417-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="a9417-119">Die Funktion _Qualitätsmanagement für Lagerortprozesse_ erweitert die Möglichkeiten des Qualitätsmanagements.</span><span class="sxs-lookup"><span data-stu-id="a9417-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="a9417-120">Wenn Sie diese Funktion verwenden, lesen Sie [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md), um Beispiele dafür zu erhalten, wie Qualitätsmanagement funktioniert, wenn es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a9417-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="a9417-121">Erstellen Sie Qualitätsaufträge für Teilbelege.</span><span class="sxs-lookup"><span data-stu-id="a9417-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="a9417-122">Um einen Qualitätsauftrag zu erstellen, der auf der für einen Auftrag physisch erhaltenen Menge basiert, müssen Sie das Kontrollkästchen **Pro aktualisierter Menge** auf dem Formular **Artikelmusteraufnahme** markieren.</span><span class="sxs-lookup"><span data-stu-id="a9417-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="a9417-123">Erstellen Sie Testtypen, die Minimum-, Maximum- und Zielprüfwerte enthalten, und führen Sie Qualitativ-gegen-quantitative-Tests mit vordefinierten Prüfergebnissen aus.</span><span class="sxs-lookup"><span data-stu-id="a9417-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="a9417-124">Legen Sie ein akzeptables Qualitätsniveau (AQL) fest, um die Qualitätsmessungstoleranz zu steuern.</span><span class="sxs-lookup"><span data-stu-id="a9417-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="a9417-125">Geben Sie die Ressourcen an, die ein Inspektionsarbeitsgang erfordert (z. B. ein Testbereich und Testinstrumente).</span><span class="sxs-lookup"><span data-stu-id="a9417-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="a9417-126">Arbeiten mit Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="a9417-126">Working with quality associations</span></span>
<span data-ttu-id="a9417-127">Der Geschäftsprozess, der eine Qualitätszuordnung verwendet, kann sich auf verschiedene Quelldokumente beziehen (z. B. Bestellungen, Aufträge oder Produktionsaufträge).</span><span class="sxs-lookup"><span data-stu-id="a9417-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="a9417-128">Jeder Qualitätszuordnungsdatensatz definiert den Testsatz, das akzeptable Qualitätsniveau (AQL) und den Musteraufnahmeplan, der für die Qualitätsprüfungsaufträge gilt, die generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="a9417-129">Sie müssen einen Qualitätszuordnungsdatensatz für jede Variante in einem Geschäftsprozess definieren.</span><span class="sxs-lookup"><span data-stu-id="a9417-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="a9417-130">So können Sie beispielsweise eine Qualitätszuordnung einrichten, die einen Qualitätsprüfungsauftrag generiert, wenn ein Produktzugang für Bestellungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a9417-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="a9417-131">Je nach Einrichtung des Ausführungsplans, kann der auslösende Prozess auch gesperrt werden während es einen offenen Qualitätsprüfungsauftrag gibt. Oder die folgenden Prozesse (z. B. das Fakturieren von Bestellungen) können gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="a9417-132">**Hinweis:** Solange es offene Qualitätsprüfungsaufträge gibt, werden Bestandsmengen automatisch für die Ausgabe gesperrt.</span><span class="sxs-lookup"><span data-stu-id="a9417-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="a9417-133">Je nach den **Vollständige Sperrung**-Einstellungen auf der **Artikelmusteraufnahmen**-Seite, ist die Menge entweder die Menge im Qualitätsprüfungsauftrag oder die Menge in der Quelldokumentposition.</span><span class="sxs-lookup"><span data-stu-id="a9417-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="a9417-134">Für einen angegebenen Geschäftsprozess identifiziert Datensatz für Qualitätszuordnungen das Ereignis und Bedingungen, für die ein Qualitätsprüfungsauftrag generiert wird.</span><span class="sxs-lookup"><span data-stu-id="a9417-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="a9417-135">Die Bedingungen können entweder für einen Standort oder für eine juristische Person spezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="a9417-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="a9417-136">Ein Qualitätsprüfungsauftrag mit Zerstörungstests kann nur ausgeführt werden, wenn am Lager Artikel für das Ereignis vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a9417-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="a9417-137">In den folgenden Beispielen wird die Konfiguration eines Qualitätszuordnungsdatensatzes für die Varianten der einzelnen Geschäftsprozesse erläutert.</span><span class="sxs-lookup"><span data-stu-id="a9417-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="a9417-138">Für jedes Beispiel sind zudem in der folgenden Tabelle die Ereignisse und Bedingungen zusammengefasst, die durch einen Qualitätszuordnungsdatensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="a9417-139">Referenztyp</span><span class="sxs-lookup"><span data-stu-id="a9417-139">Reference type</span></span></th>
<th><span data-ttu-id="a9417-140">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="a9417-140">Event type</span></span></th>
<th><span data-ttu-id="a9417-141">Ausführung</span><span class="sxs-lookup"><span data-stu-id="a9417-141">Execution</span></span></th>
<th><span data-ttu-id="a9417-142">Ereignissperrung</span><span class="sxs-lookup"><span data-stu-id="a9417-142">Event blocking</span></span></th>
<th><span data-ttu-id="a9417-143">Dokumentreferenz</span><span class="sxs-lookup"><span data-stu-id="a9417-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="a9417-144">Bestand</span><span class="sxs-lookup"><span data-stu-id="a9417-144">Inventory</span></span></td>
<td><span data-ttu-id="a9417-145">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a9417-145">Not applicable</span></span></td>
<td><span data-ttu-id="a9417-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a9417-146">Not applicable</span></span></td>
<td><span data-ttu-id="a9417-147">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-147">None</span></span></td>
<td><span data-ttu-id="a9417-148">Alle</span><span class="sxs-lookup"><span data-stu-id="a9417-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="a9417-149">Verk.</span><span class="sxs-lookup"><span data-stu-id="a9417-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="a9417-150">Entnahmeprozess wurde geplant</span><span class="sxs-lookup"><span data-stu-id="a9417-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="a9417-151">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-151">Before</span></span></td>
<td><span data-ttu-id="a9417-152">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="a9417-153">Spezifische Kennung, Gruppe oder Alle.</span><span class="sxs-lookup"><span data-stu-id="a9417-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-154">Entnahmeprozess</span><span class="sxs-lookup"><span data-stu-id="a9417-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-155">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="a9417-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-156">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a9417-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9417-157">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="a9417-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-158">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-158">Before</span></span></td>
<td><span data-ttu-id="a9417-159">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-160">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="a9417-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-161">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a9417-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="a9417-162">Einkauf</span><span class="sxs-lookup"><span data-stu-id="a9417-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="a9417-163">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="a9417-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="a9417-164">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-164">Before</span></span></td>
<td><span data-ttu-id="a9417-165">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-166">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="a9417-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-167">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a9417-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-168">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a9417-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9417-169">Nach</span><span class="sxs-lookup"><span data-stu-id="a9417-169">After</span></span></td>
<td><span data-ttu-id="a9417-170">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-171">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a9417-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-172">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a9417-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9417-173">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="a9417-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-174">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a9417-174">Not applicable</span></span></td>
<td><span data-ttu-id="a9417-175">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-176">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a9417-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-177">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a9417-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a9417-178">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a9417-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-179">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-179">Before</span></span></td>
<td><span data-ttu-id="a9417-180">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-181">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a9417-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-182">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a9417-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a9417-183">Nach</span><span class="sxs-lookup"><span data-stu-id="a9417-183">After</span></span></td>
<td><span data-ttu-id="a9417-184">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-185">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a9417-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="a9417-186">Produktion</span><span class="sxs-lookup"><span data-stu-id="a9417-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-187">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="a9417-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-188">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a9417-188">Not applicable</span></span></td>
<td><span data-ttu-id="a9417-189">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="a9417-190">Alle</span><span class="sxs-lookup"><span data-stu-id="a9417-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-191">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a9417-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-192">Beenden</span><span class="sxs-lookup"><span data-stu-id="a9417-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a9417-193">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a9417-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-194">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-194">Before</span></span></td>
<td><span data-ttu-id="a9417-195">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-196">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a9417-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-197">Beenden</span><span class="sxs-lookup"><span data-stu-id="a9417-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a9417-198">Nach</span><span class="sxs-lookup"><span data-stu-id="a9417-198">After</span></span></td>
<td><span data-ttu-id="a9417-199">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-200">Beenden</span><span class="sxs-lookup"><span data-stu-id="a9417-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a9417-201">Quarantäne</span><span class="sxs-lookup"><span data-stu-id="a9417-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-202">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a9417-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="a9417-203">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-203">Before</span></span></td>
<td><span data-ttu-id="a9417-204">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a9417-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-205">Beenden</span><span class="sxs-lookup"><span data-stu-id="a9417-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-206">Nach</span><span class="sxs-lookup"><span data-stu-id="a9417-206">After</span></span></td>
<td><span data-ttu-id="a9417-207">Beenden</span><span class="sxs-lookup"><span data-stu-id="a9417-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-208">Beenden</span><span class="sxs-lookup"><span data-stu-id="a9417-208">End</span></span></td>
<td><span data-ttu-id="a9417-209">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-209">Before</span></span></td>
<td><span data-ttu-id="a9417-210">Beenden</span><span class="sxs-lookup"><span data-stu-id="a9417-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9417-211">Arbeitsplan-Arbeitsgang</span><span class="sxs-lookup"><span data-stu-id="a9417-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-212">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a9417-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="a9417-213">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-213">Before</span></span></td>
<td><span data-ttu-id="a9417-214">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-215">Bestimmte Kennung, Gruppe oder Alle und Ressourcenspezifisch, Gruppe oder Alle</span><span class="sxs-lookup"><span data-stu-id="a9417-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-216">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a9417-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-217">Nach</span><span class="sxs-lookup"><span data-stu-id="a9417-217">After</span></span></td>
<td><span data-ttu-id="a9417-218">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9417-219">Kuppelprodukt - Produktion</span><span class="sxs-lookup"><span data-stu-id="a9417-219">Co-product production</span></span></td>
<td><span data-ttu-id="a9417-220">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="a9417-220">Registration</span></span></td>
<td><span data-ttu-id="a9417-221">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a9417-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-222">Keine</span><span class="sxs-lookup"><span data-stu-id="a9417-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="a9417-223">Alle</span><span class="sxs-lookup"><span data-stu-id="a9417-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a9417-224">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a9417-224">Report as finished</span></span></td>
<td><span data-ttu-id="a9417-225">Vor</span><span class="sxs-lookup"><span data-stu-id="a9417-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-226">Nach</span><span class="sxs-lookup"><span data-stu-id="a9417-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a9417-227">Die folgende Tabelle enthält weitere Informationen darüber, wie Qualitätsprüfungsaufträge für bestimmte Arten von Prozessen generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a9417-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="a9417-228">Prozesstypen</span><span class="sxs-lookup"><span data-stu-id="a9417-228">Type of process</span></span></th>
<th><span data-ttu-id="a9417-229">Wenn Qualitätsprüfungsaufträge automatisch generiert werden können</span><span class="sxs-lookup"><span data-stu-id="a9417-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="a9417-230">Wenn Qualitätsprüfungsaufträge generiert werden können, wenn Zerstörungstest erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="a9417-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="a9417-231">Bedingungsinformationen</span><span class="sxs-lookup"><span data-stu-id="a9417-231">Condition information</span></span></th>
<th><span data-ttu-id="a9417-232">Manuelle Generierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="a9417-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="a9417-233">Bestellung</span><span class="sxs-lookup"><span data-stu-id="a9417-233">Purchase order</span></span></td>
<td><span data-ttu-id="a9417-234">Bevor oder nachdem eine Zugangsliste oder ein Produktzugang für das erhaltene Material gebucht wird</span><span class="sxs-lookup"><span data-stu-id="a9417-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="a9417-235">Nachdem der Produktzugang für das Material, das erhalten wurde, gebucht wurde, da das Material für Zerstörungstest verfügbar sein muss</span><span class="sxs-lookup"><span data-stu-id="a9417-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="a9417-236">Die Anforderung für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Kreditor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="a9417-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a9417-237">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Bestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9417-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-238">Quarantäneauftrag</span><span class="sxs-lookup"><span data-stu-id="a9417-238">Quarantine order</span></span></td>
<td><span data-ttu-id="a9417-239">Bevor oder nachdem der Quarantäneauftrag als fertig oder abgeschlossen gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="a9417-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="a9417-240">Qualitätsprüfungsaufträge, die Zerstörungstests erfordern, können nicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="a9417-241">Es wird angenommen, dass die Quarantäneaufträge-Funktionen die Disposition des Materials verarbeiten, das zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="a9417-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="a9417-242">Die Anforderung für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Kreditor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="a9417-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a9417-243">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Quarantänebestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9417-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-244">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a9417-244">Sales order</span></span></td>
<td><span data-ttu-id="a9417-245">Vor eine geplanter Entnahmevorgang oder eine Lieferscheinaktualisierung für die zu liefernden Artikel</span><span class="sxs-lookup"><span data-stu-id="a9417-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="a9417-246">Bei einem beliebigen Schritt</span><span class="sxs-lookup"><span data-stu-id="a9417-246">At any step</span></span></td>
<td><span data-ttu-id="a9417-247">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Debitor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="a9417-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a9417-248">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Auftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9417-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-249">Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="a9417-249">Production order</span></span></td>
<td><span data-ttu-id="a9417-250">Bevor oder nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="a9417-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="a9417-251">Nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="a9417-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="a9417-252">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, Debitor oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="a9417-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a9417-253">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Produktionsauftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9417-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-254">Produktionsauftrag, der über einen Arbeitsplan-Arbeitsgang verfügt</span><span class="sxs-lookup"><span data-stu-id="a9417-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="a9417-255">Bevor oder nachdem der für einen Arbeitsgang abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="a9417-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="a9417-256">Nachdem die Meldung für den letzten Arbeitsgang abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="a9417-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="a9417-257">Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, eine betriebliche Ressource oder auf eine Kombination aus diesen Bedingungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="a9417-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a9417-258">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Arbeitsplan-Arbeitsgang bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9417-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9417-259">Bestand</span><span class="sxs-lookup"><span data-stu-id="a9417-259">Inventory</span></span></td>
<td><span data-ttu-id="a9417-260">Ein Qualitätsprüfungsauftrag kann nicht für eine Buchung in einer Lagererfassung oder für Umlagerungsauftragsbuchungen automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9417-261">Ein Qualitätsprüfungsauftrag muss für die Lagermenge eines Artikels manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="a9417-262">Physischer Lagerbestand ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9417-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="a9417-263">Automatische Generierung von Qualitätsprüfungsaufträgen – Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9417-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="a9417-264">Einkauf</span><span class="sxs-lookup"><span data-stu-id="a9417-264">Purchasing</span></span>

<span data-ttu-id="a9417-265">Im Einkauf, wenn Sie das Feld **Ereignistyp** auf **Produktzugang** und das **Ausführung**-Feld auf **Später** auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="a9417-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="a9417-266">Wenn die Option **Pro aktualisierter Menge** auf **Ja** festgelegt wird, wird ein Qualitätsprüfungsauftrag für jeden Zugang für den Auftrag anhand der Eingangsmenge und Einstellungen in der Artikelmusteraufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="a9417-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="a9417-267">Wenn eine Menge für den Auftrag eingeht, werden neue Qualitätsprüfungsaufträge auf Grundlage der neuen Eingangsmenge generiert.</span><span class="sxs-lookup"><span data-stu-id="a9417-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="a9417-268">Wenn die Option **Pro aktualisierter Menge** auf **Nein** festgelegt wird, wird ein Qualitätsprüfungsauftrag für den ersten Zugang für den Auftrag anhand der Eingangsmenge generiert.</span><span class="sxs-lookup"><span data-stu-id="a9417-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="a9417-269">Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9417-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="a9417-270">Qualitätsprüfungsaufträge werden nicht für nachfolgende Zugänge für den Auftrag generiert.</span><span class="sxs-lookup"><span data-stu-id="a9417-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="a9417-271">Produktion</span><span class="sxs-lookup"><span data-stu-id="a9417-271">Production</span></span>

<span data-ttu-id="a9417-272">In der Produktion, wenn Sie das Feld **Ereignistyp** auf **Fertigmeldung** und das **Ausführung**-Feld auf **Später** auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="a9417-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="a9417-273">Wenn die Option **Pro aktualisierter Menge** auf **Ja** festgelegt wird, wird ein Qualitätsprüfungsauftrag auf der Basis einer jeden fertiggestellten Menge und der Einstellungen in der Artikelmusteraufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="a9417-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="a9417-274">Wenn eine Menge für den Produktionsauftrag als fertig gemeldet wird, werden neue Qualitätsprüfungsaufträge auf Grundlage der neuen fertiggestellten Menge generiert.</span><span class="sxs-lookup"><span data-stu-id="a9417-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="a9417-275">Diese Generierungslogik ist mit dem Einkauf konsistent.</span><span class="sxs-lookup"><span data-stu-id="a9417-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="a9417-276">Wenn die Option **Pro aktualisierter Menge** auf **Nein** festgelegt wird, wird ein Qualitätsprüfungsauftrag das erste Mal, wenn eine Menge als fertig gemeldet wird, anhand der fertiggestellten Menge generiert.</span><span class="sxs-lookup"><span data-stu-id="a9417-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="a9417-277">Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen der Artikelmusteraufnahme erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9417-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="a9417-278">Qualitätsprüfungsaufträge werden nicht für nachfolgende fertiggestellte Mengen generiert.</span><span class="sxs-lookup"><span data-stu-id="a9417-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="a9417-279">Qualitätsspezifikation</span><span class="sxs-lookup"><span data-stu-id="a9417-279">Quality specification</span></span></th>
<th><span data-ttu-id="a9417-280">Pro aktualisierter Menge</span><span class="sxs-lookup"><span data-stu-id="a9417-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="a9417-281">Pro Rückverfolgungsangabe</span><span class="sxs-lookup"><span data-stu-id="a9417-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="a9417-282">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a9417-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="a9417-283">Prozentsatz: 10 %</span><span class="sxs-lookup"><span data-stu-id="a9417-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="a9417-284">Ja</span><span class="sxs-lookup"><span data-stu-id="a9417-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="a9417-285">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="a9417-285">Batch number: No</span></span></p>
<p><span data-ttu-id="a9417-286">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="a9417-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="a9417-287">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="a9417-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="a9417-288">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="a9417-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="a9417-289">Qualitätsprüfungsauftrag Nr. 1 für 3 (10 % von 30)</span><span class="sxs-lookup"><span data-stu-id="a9417-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a9417-290">Fertigmeldung für 70</span><span class="sxs-lookup"><span data-stu-id="a9417-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="a9417-291">Qualitätsprüfungsauftrag Nr. 2 für 7 (10 % verbleibenden Auftragsmenge, die in diesem Fall 70 entspricht)</span><span class="sxs-lookup"><span data-stu-id="a9417-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="a9417-292">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="a9417-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="a9417-293">Nein</span><span class="sxs-lookup"><span data-stu-id="a9417-293">No</span></span></td>
<td>
<p><span data-ttu-id="a9417-294">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="a9417-294">Batch number: No</span></span></p>
<p><span data-ttu-id="a9417-295">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="a9417-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="a9417-296">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="a9417-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="a9417-297">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="a9417-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="a9417-298">Qualitätsprüfungsauftrag Nr. 1 für 1 (für die erste als fertig gemeldete Menge, die den festen Wert „1“ hat)</span><span class="sxs-lookup"><span data-stu-id="a9417-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="a9417-299">Qualitätsprüfungsauftrag Nr. 2 für 1 (für die verbleibende Menge, die immer noch den festen Wert „1“ hat)</span><span class="sxs-lookup"><span data-stu-id="a9417-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a9417-300">Fertigmeldung für 10</span><span class="sxs-lookup"><span data-stu-id="a9417-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="a9417-301">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9417-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a9417-302">Fertigmeldung für 60</span><span class="sxs-lookup"><span data-stu-id="a9417-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="a9417-303">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9417-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="a9417-304">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="a9417-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="a9417-305">Ja</span><span class="sxs-lookup"><span data-stu-id="a9417-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="a9417-306">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="a9417-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="a9417-307">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="a9417-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="a9417-308">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="a9417-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="a9417-309">Fertigmeldung für 3: 1 für Nr. b1, Nr. s1; 1 für Nr. b2, Nr. s2; und 1 für Nr. b3, Nr. s3</span><span class="sxs-lookup"><span data-stu-id="a9417-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="a9417-310">Qualitätsprüfungsauftrag Nr. 1 für 1 von Charge Nr. b1, Serie Nr. s1</span><span class="sxs-lookup"><span data-stu-id="a9417-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="a9417-311">Qualitätsprüfungsauftrag Nr. 2 für 1 von Charge Nr. b2, Serie Nr. s2</span><span class="sxs-lookup"><span data-stu-id="a9417-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="a9417-312">Qualitätsprüfungsauftrag Nr. 3 für 1 von Charge Nr. b3, Serie Nr. s3</span><span class="sxs-lookup"><span data-stu-id="a9417-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a9417-313">Fertigmeldung für 2: 1 für Nr. b4, Nr. s4; und 1 für Nr. b5, Nr. s5</span><span class="sxs-lookup"><span data-stu-id="a9417-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="a9417-314">Qualitätsprüfungsauftrag Nr. 4 für 1 von Charge Nr. b4, Serie Nr. s4</span><span class="sxs-lookup"><span data-stu-id="a9417-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="a9417-315">Qualitätsprüfungsauftrag Nr. 5 für 1 von Charge Nr. b5, Serie Nr. s5</span><span class="sxs-lookup"><span data-stu-id="a9417-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="a9417-316"><strong>Hinweis:</strong> Die Charge kann wiederverwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a9417-317">Feste Menge: 2</span><span class="sxs-lookup"><span data-stu-id="a9417-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="a9417-318">Nein</span><span class="sxs-lookup"><span data-stu-id="a9417-318">No</span></span></td>
<td>
<p><span data-ttu-id="a9417-319">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="a9417-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="a9417-320">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="a9417-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="a9417-321">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="a9417-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="a9417-322">Fertigmeldung für 4: 1 für Nr. b1, Nr. s1; 1 für Nr. b2, Nr. s2; 1 für Nr. b3, Nr. s3; und 1 für Nr. b4, Nr. s4</span><span class="sxs-lookup"><span data-stu-id="a9417-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="a9417-323">Qualitätsprüfungsauftrag Nr. 1 für 1 von Charge Nr. b1, Serie Nr. s1</span><span class="sxs-lookup"><span data-stu-id="a9417-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="a9417-324">Qualitätsprüfungsauftrag Nr. 2 für 1 von Charge Nr. b2, Serie Nr. s2</span><span class="sxs-lookup"><span data-stu-id="a9417-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="a9417-325">Qualitätsprüfungsauftrag Nr. 3 für 1 von Charge Nr. b3, Serie Nr. s3</span><span class="sxs-lookup"><span data-stu-id="a9417-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="a9417-326">Qualitätsprüfungsauftrag Nr. 4 für 1 von Charge Nr. b4, Serie Nr. s4</span><span class="sxs-lookup"><span data-stu-id="a9417-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="a9417-327">Qualitätsprüfungsauftrag Nr. 5 für 2, ohne Verweis auf eine Charge und Seriennummer</span><span class="sxs-lookup"><span data-stu-id="a9417-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a9417-328">Fertigmeldung für 6: 1 für Nr. b5, Nr. s5; 1 für Nr. b6, Nr. s6; 1 für Nr. b7, Nr. s7; 1 für Nr. b8, Nr. s8; 1 für Nr. b9, Nr. s9; und 1 für Nr. b10, Nr. s10</span><span class="sxs-lookup"><span data-stu-id="a9417-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="a9417-329">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9417-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a9417-330">Die Funktion *Qualitätsmanagement für Lagerortprozesse* fügt Funktionen zur Verarbeitung von Qualitätsaufträgen für die Produktion hinzu, wenn der **Ereignistyp** auf *Fertigmeldung* und **Ausführung** auf *Nach* eingestellt ist, und die Einkäufe mit **Ereignistyp** sind auf *Registrierung* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a9417-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="a9417-331">Weitere Informationen finden Sie unter [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="a9417-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="a9417-332">Qualitätsmanagementseiten</span><span class="sxs-lookup"><span data-stu-id="a9417-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9417-333">Seite</span><span class="sxs-lookup"><span data-stu-id="a9417-333">Page</span></span></th>
<th><span data-ttu-id="a9417-334">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9417-334">Description</span></span></th>
<th><span data-ttu-id="a9417-335">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9417-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9417-336">Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="a9417-336">Quality associations</span></span></td>
<td><span data-ttu-id="a9417-337">Siehe vorherige Abschnitte dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="a9417-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="a9417-338">Eine Qualitätszuordnung definiert alle folgenden Informationen für einen erzeugten Qualitätsprüfungsauftrag:</span><span class="sxs-lookup"><span data-stu-id="a9417-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="a9417-339">Das Buchungsereignis</span><span class="sxs-lookup"><span data-stu-id="a9417-339">The transaction event</span></span></li>
<li><span data-ttu-id="a9417-340">Die Tests, die für die Artikel ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a9417-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="a9417-341">Das akzeptable Qualitätsniveau</span><span class="sxs-lookup"><span data-stu-id="a9417-341">The AQL</span></span></li>
<li><span data-ttu-id="a9417-342">Den Musteraufnahmeplan</span><span class="sxs-lookup"><span data-stu-id="a9417-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="a9417-343">Sie müssen eine Qualitätszuordnung für jede Variante in einem Geschäftsprozess definieren, die eine automatische Generierung eines Qualitätsprüfungsauftrags erfordert.</span><span class="sxs-lookup"><span data-stu-id="a9417-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="a9417-344">So kann ein Qualitätsprüfungsauftrag beispielsweise in Geschäftsprozessen für Bestellungen, Quarantäneaufträge, Aufträge und Produktionsaufträge generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9417-345">Tests</span><span class="sxs-lookup"><span data-stu-id="a9417-345">Tests</span></span></td>
<td><span data-ttu-id="a9417-346">Mithilfe dieser Seite können Sie die einzelnen Tests definieren und anzeigen, mit denen ermittelt wird, ob Ihre Produkte den Qualitätsangaben entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a9417-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="a9417-347">Einzelne Tests können einer Testgruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="a9417-348">In diesem Fall werden auch testspezifische Informationen (beispielsweise die zulässigen Messwerte) angegeben.</span><span class="sxs-lookup"><span data-stu-id="a9417-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="a9417-349">Messwerte kommen bei Mengentests, Testvariablen bei Qualitätstests zum Einsatz.</span><span class="sxs-lookup"><span data-stu-id="a9417-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="a9417-350">Ein Mengentest besitzt den Testtyp <strong>Ganzzahl</strong> oder <strong>Bruchteil</strong> sowie eine Angabe für die Maßeinheit.</span><span class="sxs-lookup"><span data-stu-id="a9417-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="a9417-351">Qualitätsangaben und Testergebnisse werden in Zahlen ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="a9417-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="a9417-352">Für einen Qualitätstest wird der Testtyp <strong>Option</strong> verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9417-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="a9417-353">Qualitative Tests erfordern zusätzliche Informationen über die zu messende Variable und die zugehörigen Optionen.</span><span class="sxs-lookup"><span data-stu-id="a9417-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="a9417-354">Qualitätsangaben und Testergebnisse werden gemäß einem Ergebnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="a9417-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="a9417-355">Ein Produktionsunternehmen führt zwei Tests für eingekauftes Material durch: einen Mengentest für die Materialqualität und einen Qualitätstest für Verpackungsschäden.</span><span class="sxs-lookup"><span data-stu-id="a9417-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="a9417-356">Für den Qualitätstest werden weitere Informationen definiert, um die Testvariable (beschädigte Verpackung) und die Ergebnisse zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a9417-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="a9417-357">Auf der Seite <strong>Testgruppen</strong> werden die beiden Tests einer Testgruppe zugeordnet und die testspezifischen Informationen angegeben.</span><span class="sxs-lookup"><span data-stu-id="a9417-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="a9417-358">Die Testgruppe wird einem Qualitätsprüfungsauftrag zugeordnet, sodass das Unternehmen einen Bericht über die Testergebnisse für die beiden Tests erhält.</span><span class="sxs-lookup"><span data-stu-id="a9417-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9417-359">Testgruppen</span><span class="sxs-lookup"><span data-stu-id="a9417-359">Test groups</span></span></td>
<td><span data-ttu-id="a9417-360">Mithilfe dieser Seite können Sie Testgruppen und die einzelnen Tests einrichten, bearbeiten und anzeigen, die einer Testgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a9417-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="a9417-361">Im oberen Bereich werden Testgruppen, im unteren Bereich die Tests angezeigt, die einer ausgewählten Testgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a9417-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="a9417-362">Sie ordnen einer Testgruppe mehrere Richtlinien zu, z. B. einen Musteraufnahmeplan, eine akzeptables Qualitätsniveau und die Anforderungen für Zerstörungstests.</span><span class="sxs-lookup"><span data-stu-id="a9417-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="a9417-363">Wenn Sie einer Testgruppe einen einzelnen Test zuweisen, können Sie zusätzliche Informationen definieren (z. B. die Sequenz, Dokumente und Prüfdaten).</span><span class="sxs-lookup"><span data-stu-id="a9417-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="a9417-364">Bei einem Mengentest zählen zu den zu definierenden Informationen auch die akzeptablen Messwerte.</span><span class="sxs-lookup"><span data-stu-id="a9417-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="a9417-365">Bei einem Qualitätstest zählen hierzu auch die Testvariable und das Standardergebnis.</span><span class="sxs-lookup"><span data-stu-id="a9417-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="a9417-366">Die einem Qualitätsprüfungsauftrag zugeordnete Testgruppe definiert die Tests, die für den angegebenen Artikel ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a9417-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="a9417-367">Tests für die Qualitätsprüfung können jedoch hinzugefügt, geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a9417-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="a9417-368">Testergebnisse werden für jeden Test im Qualitätsprüfungsauftrag gemeldet.</span><span class="sxs-lookup"><span data-stu-id="a9417-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="a9417-369">Ein Produktionsunternehmen definiert eine Testgruppe für jede Abweichung von den Qualitätsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="a9417-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="a9417-370">In den verschiedenen Testgruppen sind Unterschiede in den Musteraufnahmeplänen, die zusammen auszuführenden Tests, das akzeptable Qualitätsniveau und andere Faktoren enthalten.</span><span class="sxs-lookup"><span data-stu-id="a9417-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="a9417-371">Bei Mengentests sind zudem Unterschiede hinsichtlich der akzeptablen Messwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="a9417-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="a9417-372">Um die Qualitätsrichtlinien durchzusetzen weißt das Unternehmen jeder Regel eine Testgruppe zum automatischen Erstellen von Qualitätsprüfungsaufträgen zu (im Formular <strong>Qualitätszuordnungen</strong>) und weißt eine Testgruppe zu den manuell erstellten Qualitätsprüfungsaufträgen zu.</span><span class="sxs-lookup"><span data-stu-id="a9417-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9417-373">Artikelqualitätsgruppen</span><span class="sxs-lookup"><span data-stu-id="a9417-373">Item quality groups</span></span></td>
<td><span data-ttu-id="a9417-374">Mithilfe dieser Seite können Sie die Artikel, die einer Qualitätsgruppe zugewiesen sind, oder die Qualitätsgruppen, die einem Artikel zugewiesen sind, einrichten, bearbeiten und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a9417-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="a9417-375">Eine Qualitätsgruppe gibt Aufschluss über allgemeine Testanforderungen für Artikel.</span><span class="sxs-lookup"><span data-stu-id="a9417-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="a9417-376">Nachdem Sie die Testanforderungen auf der Seite <strong>Testgruppen</strong> definiert haben, können die Regeln für die automatische Generierung von Qualitätsprüfungsaufträgen definieren.</span><span class="sxs-lookup"><span data-stu-id="a9417-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="a9417-377">Um den Vorgang zu vereinfachen, definieren Sie keine Regeln für einzelne Artikel.</span><span class="sxs-lookup"><span data-stu-id="a9417-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="a9417-378">Stattdessen definieren Sie Regeln für eine Qualitätsgruppe, indem Sie die Seite <strong>Qualitätszuordnungen</strong> verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9417-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="a9417-379">Sie können auch die Seite <strong>Artikelqualitätsgruppen</strong> für eine ausgewählte Qualitätsgruppe verwenden, um dieser Gruppe geeignete Artikel zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a9417-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="a9417-380">Sie können auch die Seite <strong>Artikelqualitätsgruppen</strong> für eine ausgewählte Qualitätsgruppe verwenden, um dieser dem Artikel passende Qualitätsgruppen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a9417-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="a9417-381">Ein Produktionsunternehmen erwirbt verschiedene Rohstoffe, bei denen die gleichen Testanforderungen zur Prüfung eingehender Waren gelten.</span><span class="sxs-lookup"><span data-stu-id="a9417-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="a9417-382">Das Unternehmen definiert eine Qualitätsgruppe und weist die zugehörigen Artikelnummern der Rohstoffe der Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="a9417-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="a9417-383">Später erwirbt das Unternehmen einen neuen Rohstofftyp, für den die gleichen Testanforderungen gelten.</span><span class="sxs-lookup"><span data-stu-id="a9417-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="a9417-384">Anstatt neue Testanforderungen für den neuen Rohstoff einzurichten, fügt das Unternehmen die Artikelnummer neuen Materials der vorhandenen Qualitätsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="a9417-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="a9417-385">Das gleiche Produktionsunternehmen produziert auch Artikel, für die die gleichen Produktionstestanforderungen gelten, und liefert Artikel mit den gleichen Anforderungen für die Durchführung von Tests vor der Lieferung.</span><span class="sxs-lookup"><span data-stu-id="a9417-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="a9417-386">Das Unternehmen definiert zwei zusätzliche Qualitätsgruppen und weist dann jeder Qualitätsgruppe die entsprechenden Artikelnummern zu.</span><span class="sxs-lookup"><span data-stu-id="a9417-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9417-387">Testvariablen</span><span class="sxs-lookup"><span data-stu-id="a9417-387">Test variables</span></span></td>
<td><span data-ttu-id="a9417-388">Mit dieser Seite können Sie das die Variablen definieren und anzeigen, die Qualitätstests zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a9417-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="a9417-389">Für jede Variable definieren Sie Ergebnisaufzählungen, die die möglichen Optionen darstellen.</span><span class="sxs-lookup"><span data-stu-id="a9417-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="a9417-390">Sie definieren Tests auf der <strong>Tests</strong>-Seite.</span><span class="sxs-lookup"><span data-stu-id="a9417-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="a9417-391">Bei Mengentests müssen Sie den Testtyp auf <strong>Option</strong> festlegen.</span><span class="sxs-lookup"><span data-stu-id="a9417-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="a9417-392">Verwenden Sie die Seite <strong>Testgruppen</strong>, um einem einzelnen Test eine Testvariable zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a9417-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="a9417-393">Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="a9417-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="a9417-394">Diese Abnahmeprüfung besitzt mehrere Variablen.</span><span class="sxs-lookup"><span data-stu-id="a9417-394">This inspection test has several variables.</span></span> <span data-ttu-id="a9417-395">Eine Variable ist der Geschmack, wobei die möglichen Ergebnisse "gut" oder "schlecht" lauten.</span><span class="sxs-lookup"><span data-stu-id="a9417-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="a9417-396">Eine zweite Variable ist die Farbe, bei der die möglichen Ergebnisse "zu dunkel", "zu hell" und "in Ordnung" sind.</span><span class="sxs-lookup"><span data-stu-id="a9417-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9417-397">Ergebnisse für Testvariable</span><span class="sxs-lookup"><span data-stu-id="a9417-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="a9417-398">Mithilfe dieser Seite werden die möglichen Testergebnisse für eine Testvariable geändert, die einem Qualitätstest zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a9417-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="a9417-399">Für jedes Ergebnis weisen Sie entweder den Status <strong>Erfolgreich</strong> oder <strong>Fehlgeschlagen</strong> zu.</span><span class="sxs-lookup"><span data-stu-id="a9417-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="a9417-400">Definieren Sie eine Variable und die Ergebnisse für jeden Qualitätstest, der auf der Seite <strong>Tests</strong> definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a9417-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="a9417-401">(Für Qualitätstests, wird der Testtyp auf der Seite <strong>Option</strong> auf <strong>Tests</strong>) gesetzt. Verwenden Sie die Seite <strong>Testgruppen</strong>, um eine Testvariable und ein Standardergebnis einzelnem Qualitätstest zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a9417-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="a9417-402">Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="a9417-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="a9417-403">Diese Abnahmeprüfung besitzt mehrere Variablen.</span><span class="sxs-lookup"><span data-stu-id="a9417-403">This inspection test has of several variables.</span></span> <span data-ttu-id="a9417-404">Eine Variable ist der Geschmack, wobei die möglichen Ergebnisse "gut" oder "schlecht" lauten.</span><span class="sxs-lookup"><span data-stu-id="a9417-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="a9417-405">Eine zweite Variable ist die Farbe, bei der die möglichen Ergebnisse "zu dunkel", "zu hell" und "in Ordnung" sind.</span><span class="sxs-lookup"><span data-stu-id="a9417-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="a9417-406">Für jedes Ergebnis wird der Status <strong>Erfolgreich</strong> oder <strong>Fehlgeschlagen</strong> festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a9417-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="a9417-407">Während der Abnahmeprüfung für jede Variable meldet der Inspektor das Testergebnis, indem er eines der Ergebnisse auswählt.</span><span class="sxs-lookup"><span data-stu-id="a9417-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="a9417-408">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a9417-408">Additional resources</span></span>
--------

[<span data-ttu-id="a9417-409">Qualitätsmanagementprozesse</span><span class="sxs-lookup"><span data-stu-id="a9417-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="a9417-410">Qualitätsmangelverwaltung</span><span class="sxs-lookup"><span data-stu-id="a9417-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="a9417-411">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="a9417-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
