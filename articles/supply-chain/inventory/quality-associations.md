---
title: Qualitätszuordnungen
description: Dieses Thema beschreibt, wie Sie Qualitätsprüfungsaufträge in Microsoft Dynamics 365 Supply Chain Management verwenden können, um automatisch Qualitätsprüfungsaufträge zu generieren, die mit Ihren Verkaufs-, Einkaufs- und Produktionsprozessen zusammenhängen.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956666"
---
# <a name="quality-associations"></a><span data-ttu-id="a38c3-103">Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="a38c3-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a38c3-104">Dieses Thema beschreibt, wie Sie Qualitätsprüfungsaufträge in Microsoft Dynamics 365 Supply Chain Management verwenden können, um automatisch Qualitätsprüfungsaufträge zu generieren, die mit Ihren Verkaufs-, Einkaufs- und Produktionsprozessen zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="a38c3-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="a38c3-105">Eine Qualitätszuordnung definiert alle folgenden Informationen für einen erzeugten Qualitätsprüfungsauftrag:</span><span class="sxs-lookup"><span data-stu-id="a38c3-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="a38c3-106">Das Buchungsereignis</span><span class="sxs-lookup"><span data-stu-id="a38c3-106">The transaction event</span></span>
- <span data-ttu-id="a38c3-107">Die Tests, die für die Artikel ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a38c3-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="a38c3-108">Die akzeptable Qualitätsstufe (AQL)</span><span class="sxs-lookup"><span data-stu-id="a38c3-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="a38c3-109">Den Musteraufnahmeplan</span><span class="sxs-lookup"><span data-stu-id="a38c3-109">The sampling plan</span></span>

<span data-ttu-id="a38c3-110">Sie müssen eine Qualitätszuordnung für jede Variante in einem Geschäftsprozess definieren, die eine automatische Generierung eines Qualitätsprüfungsauftrags erfordert.</span><span class="sxs-lookup"><span data-stu-id="a38c3-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="a38c3-111">So kann ein Qualitätsprüfungsauftrag beispielsweise in Geschäftsprozessen für Bestellungen, Quarantäneaufträge, Aufträge und Produktionsaufträge generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="a38c3-112">Arbeiten mit Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="a38c3-112">Working with quality associations</span></span>

<span data-ttu-id="a38c3-113">Der Geschäftsprozess, der eine Qualitätszuordnung verwendet, kann sich auf verschiedene Quelldokumente beziehen (z. B. Bestellungen, Aufträge oder Produktionsaufträge).</span><span class="sxs-lookup"><span data-stu-id="a38c3-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="a38c3-114">Jeder Qualitätszuordnungsdatensatz definiert den Testsatz, das akzeptable Qualitätsniveau (AQL) und den Musteraufnahmeplan, der für die Qualitätsprüfungsaufträge gilt, die generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="a38c3-115">Sie müssen einen Qualitätszuordnungsdatensatz für jede Variante in einem Geschäftsprozess definieren.</span><span class="sxs-lookup"><span data-stu-id="a38c3-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="a38c3-116">So können Sie beispielsweise eine Qualitätszuordnung einrichten, die einen Qualitätsprüfungsauftrag generiert, wenn ein Produktzugang für Bestellungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a38c3-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="a38c3-117">Je nach Einrichten des Ausführungsplans kann der auslösende Prozess selbst blockiert werden, während ein offener Qualitätsprüfungsauftrag vorliegt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="a38c3-118">Alternativ können nachfolgende Prozesse, wie z.B. die Rechnungsstellung für den Kauf, blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="a38c3-119">Solange es offene Qualitätsprüfungsaufträge gibt, werden Bestandsmengen automatisch für die Ausgabe gesperrt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="a38c3-120">Abhängig von der Einstellung des Felds **Vollsperrung** auf der Seite **Artikelmusteraufnahme** ist die Menge entweder die Menge auf dem Qualitätsprüfungsauftrag oder die Menge auf der Quelldokumentzeile.</span><span class="sxs-lookup"><span data-stu-id="a38c3-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="a38c3-121">Weitere Informationen finden Sie unter [Qualitätsmanagement Artikelmusteraufnahme](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="a38c3-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="a38c3-122">Für einen bestimmten Geschäftsprozess identifiziert der Datensatz für die Qualitätszuordnung das Ereignis und die Bedingungen, für die ein Qualitätsprüfungsauftrag erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="a38c3-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="a38c3-123">Die Bedingungen können entweder für einen Standort oder für eine juristische Person spezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="a38c3-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="a38c3-124">Ein Qualitätsprüfungsauftrag mit Zerstörungstests kann nur ausgeführt werden, wenn am Lager Artikel für das Ereignis vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a38c3-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="a38c3-125">Um mit Qualitätsverbänden zu arbeiten, gehen Sie zu **Bestandsmanagement \> Einrichten \> Qualitätskontrolle \> Qualitätsverbände**.</span><span class="sxs-lookup"><span data-stu-id="a38c3-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="a38c3-126">Die folgenden Beispiele zeigen, wie ein Datensatz für die Qualitätszuordnung für die Variationen in jedem Geschäftsprozess definiert wird.</span><span class="sxs-lookup"><span data-stu-id="a38c3-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="a38c3-127">Für jedes Beispiel sind zudem in der folgenden Tabelle die Ereignisse und Bedingungen zusammengefasst, die durch einen Qualitätszuordnungsdatensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a38c3-128">Referenztyp</span><span class="sxs-lookup"><span data-stu-id="a38c3-128">Reference type</span></span></th>
<th><span data-ttu-id="a38c3-129">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="a38c3-129">Event type</span></span></th>
<th><span data-ttu-id="a38c3-130">Ausführung</span><span class="sxs-lookup"><span data-stu-id="a38c3-130">Execution</span></span></th>
<th><span data-ttu-id="a38c3-131">Ereignissperrung</span><span class="sxs-lookup"><span data-stu-id="a38c3-131">Event blocking</span></span></th>
<th><span data-ttu-id="a38c3-132">Dokumentreferenz</span><span class="sxs-lookup"><span data-stu-id="a38c3-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a38c3-133">Bestand</span><span class="sxs-lookup"><span data-stu-id="a38c3-133">Inventory</span></span></td>
<td><span data-ttu-id="a38c3-134">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a38c3-134">Not applicable</span></span></td>
<td><span data-ttu-id="a38c3-135">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a38c3-135">Not applicable</span></span></td>
<td><span data-ttu-id="a38c3-136">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-136">None</span></span></td>
<td><span data-ttu-id="a38c3-137">Alle</span><span class="sxs-lookup"><span data-stu-id="a38c3-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="a38c3-138">Verk.</span><span class="sxs-lookup"><span data-stu-id="a38c3-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="a38c3-139">Entnahmeprozess wurde geplant</span><span class="sxs-lookup"><span data-stu-id="a38c3-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="a38c3-140">Vor</span><span class="sxs-lookup"><span data-stu-id="a38c3-140">Before</span></span></td>
<td><span data-ttu-id="a38c3-141">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="a38c3-142">Spezifische Kennung, Gruppe oder Alle.</span><span class="sxs-lookup"><span data-stu-id="a38c3-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-143">Entnahmeprozess</span><span class="sxs-lookup"><span data-stu-id="a38c3-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-144">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="a38c3-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-145">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a38c3-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a38c3-146">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="a38c3-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-147">Vor</span><span class="sxs-lookup"><span data-stu-id="a38c3-147">Before</span></span></td>
<td><span data-ttu-id="a38c3-148">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-149">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="a38c3-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-150">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a38c3-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="a38c3-151">Einkauf</span><span class="sxs-lookup"><span data-stu-id="a38c3-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="a38c3-152">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="a38c3-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="a38c3-153">Vor</span><span class="sxs-lookup"><span data-stu-id="a38c3-153">Before</span></span></td>
<td><span data-ttu-id="a38c3-154">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-155">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="a38c3-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-156">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a38c3-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-157">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a38c3-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a38c3-158">Nach</span><span class="sxs-lookup"><span data-stu-id="a38c3-158">After</span></span></td>
<td><span data-ttu-id="a38c3-159">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-160">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a38c3-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-161">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a38c3-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a38c3-162">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="a38c3-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-163">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a38c3-163">Not applicable</span></span></td>
<td><span data-ttu-id="a38c3-164">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-165">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a38c3-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-166">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a38c3-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a38c3-167">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a38c3-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-168">Vor</span><span class="sxs-lookup"><span data-stu-id="a38c3-168">Before</span></span></td>
<td><span data-ttu-id="a38c3-169">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-170">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="a38c3-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-171">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a38c3-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a38c3-172">Nach</span><span class="sxs-lookup"><span data-stu-id="a38c3-172">After</span></span></td>
<td><span data-ttu-id="a38c3-173">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-174">Rechnung</span><span class="sxs-lookup"><span data-stu-id="a38c3-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="a38c3-175">Produktion</span><span class="sxs-lookup"><span data-stu-id="a38c3-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-176">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="a38c3-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-177">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a38c3-177">Not applicable</span></span></td>
<td><span data-ttu-id="a38c3-178">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="a38c3-179">Alle</span><span class="sxs-lookup"><span data-stu-id="a38c3-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-180">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a38c3-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-181">Beenden</span><span class="sxs-lookup"><span data-stu-id="a38c3-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a38c3-182">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a38c3-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-183">Vor</span><span class="sxs-lookup"><span data-stu-id="a38c3-183">Before</span></span></td>
<td><span data-ttu-id="a38c3-184">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-185">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a38c3-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-186">Beenden</span><span class="sxs-lookup"><span data-stu-id="a38c3-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a38c3-187">Nach</span><span class="sxs-lookup"><span data-stu-id="a38c3-187">After</span></span></td>
<td><span data-ttu-id="a38c3-188">Keine</span><span class="sxs-lookup"><span data-stu-id="a38c3-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-189">Beenden</span><span class="sxs-lookup"><span data-stu-id="a38c3-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a38c3-190">Quarantäne</span><span class="sxs-lookup"><span data-stu-id="a38c3-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-191">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a38c3-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="a38c3-192">Vor</span><span class="sxs-lookup"><span data-stu-id="a38c3-192">Before</span></span></td>
<td><span data-ttu-id="a38c3-193">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a38c3-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-194">Beenden</span><span class="sxs-lookup"><span data-stu-id="a38c3-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-195">Nach</span><span class="sxs-lookup"><span data-stu-id="a38c3-195">After</span></span></td>
<td><span data-ttu-id="a38c3-196">Beenden</span><span class="sxs-lookup"><span data-stu-id="a38c3-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-197">Beenden</span><span class="sxs-lookup"><span data-stu-id="a38c3-197">End</span></span></td>
<td><span data-ttu-id="a38c3-198">Vor</span><span class="sxs-lookup"><span data-stu-id="a38c3-198">Before</span></span></td>
<td><span data-ttu-id="a38c3-199">Beenden</span><span class="sxs-lookup"><span data-stu-id="a38c3-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a38c3-200">Arbeitsplan-Arbeitsgang</span><span class="sxs-lookup"><span data-stu-id="a38c3-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-201">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a38c3-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="a38c3-202">Vorher</span><span class="sxs-lookup"><span data-stu-id="a38c3-202">Before</span></span></td>
<td><span data-ttu-id="a38c3-203">Keines</span><span class="sxs-lookup"><span data-stu-id="a38c3-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-204">Spezifische ID, Gruppe oder Alle und spezifische Ressource, Gruppe oder Alle</span><span class="sxs-lookup"><span data-stu-id="a38c3-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-205">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a38c3-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-206">Später</span><span class="sxs-lookup"><span data-stu-id="a38c3-206">After</span></span></td>
<td><span data-ttu-id="a38c3-207">Keines</span><span class="sxs-lookup"><span data-stu-id="a38c3-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a38c3-208">Kuppelprodukt - Produktion</span><span class="sxs-lookup"><span data-stu-id="a38c3-208">Co-product production</span></span></td>
<td><span data-ttu-id="a38c3-209">Umsatzsteuernummer</span><span class="sxs-lookup"><span data-stu-id="a38c3-209">Registration</span></span></td>
<td><span data-ttu-id="a38c3-210">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a38c3-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-211">Keines</span><span class="sxs-lookup"><span data-stu-id="a38c3-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="a38c3-212">Alle</span><span class="sxs-lookup"><span data-stu-id="a38c3-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a38c3-213">Fertigmeldung</span><span class="sxs-lookup"><span data-stu-id="a38c3-213">Report as finished</span></span></td>
<td><span data-ttu-id="a38c3-214">Vorher</span><span class="sxs-lookup"><span data-stu-id="a38c3-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-215">Später</span><span class="sxs-lookup"><span data-stu-id="a38c3-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a38c3-216">Die Funktion *Qualitätsmanagement für Lagerorte* fügt Funktionalitäten für die Verarbeitung von Qualitätsprüfungsaufträgen für die Produktion hinzu, bei denen das Feld **Ereignistyp** auf *Bericht als fertig* und das Feld **Ausführung** auf *Nach* festgelegt ist, und für den Kauf, bei dem das Feld **Ereignistyp** auf *Registrierung* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a38c3-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="a38c3-217">Weitere Informationen finden Sie unter [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="a38c3-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="a38c3-218">Die folgende Tabelle enthält weitere Informationen darüber, wie Qualitätsprüfungsaufträge für bestimmte Arten von Prozessen generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a38c3-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="a38c3-219">Prozesstypen</span><span class="sxs-lookup"><span data-stu-id="a38c3-219">Type of process</span></span></th>
<th><span data-ttu-id="a38c3-220">Wenn Qualitätsprüfungsaufträge automatisch generiert werden können</span><span class="sxs-lookup"><span data-stu-id="a38c3-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="a38c3-221">Wenn Qualitätsprüfungsaufträge generiert werden können, wenn Zerstörungstest erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="a38c3-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="a38c3-222">Bedingungsinformationen</span><span class="sxs-lookup"><span data-stu-id="a38c3-222">Condition information</span></span></th>
<th><span data-ttu-id="a38c3-223">Manuelle Generierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="a38c3-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a38c3-224">Bestellung</span><span class="sxs-lookup"><span data-stu-id="a38c3-224">Purchase order</span></span></td>
<td><span data-ttu-id="a38c3-225">Bevor oder nachdem eine Zugangsliste oder ein Produktzugang für das erhaltene Material gebucht wird</span><span class="sxs-lookup"><span data-stu-id="a38c3-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="a38c3-226">Nachdem der Produktzugang für das Material, das erhalten wurde, gebucht wurde, da das Material für Zerstörungstest verfügbar sein muss</span><span class="sxs-lookup"><span data-stu-id="a38c3-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="a38c3-227">Der Bedarf für einen Qualitätsprüfungsauftrag kann einen bestimmten Betrieb, ein Element oder einen Kreditor oder eine Kombination dieser Bedingungen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="a38c3-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a38c3-228">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Bestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-229">Quarantäneauftrag</span><span class="sxs-lookup"><span data-stu-id="a38c3-229">Quarantine order</span></span></td>
<td><span data-ttu-id="a38c3-230">Bevor oder nachdem der Quarantäneauftrag als fertig oder abgeschlossen gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="a38c3-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="a38c3-231">Qualitätsprüfungsaufträge, die zerstörende Tests erfordern, können nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="a38c3-232">Es wird davon ausgegangen, dass die Funktionalität des Quarantäneauftrags die Disposition des zerstörten Materials übernimmt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="a38c3-233">Der Bedarf für einen Qualitätsprüfungsauftrag kann einen bestimmten Betrieb, ein Element oder einen Kreditor oder eine Kombination dieser Bedingungen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="a38c3-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a38c3-234">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Quarantänebestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-235">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a38c3-235">Sales order</span></span></td>
<td><span data-ttu-id="a38c3-236">Vor eine geplanter Entnahmevorgang oder eine Lieferscheinaktualisierung für die zu liefernden Artikel</span><span class="sxs-lookup"><span data-stu-id="a38c3-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="a38c3-237">Bei einem beliebigen Schritt</span><span class="sxs-lookup"><span data-stu-id="a38c3-237">At any step</span></span></td>
<td><span data-ttu-id="a38c3-238">Die Anforderung für einen Qualitätsprüfungsauftrag kann einen bestimmten Standort, ein Element oder einen Debitor oder eine Kombination dieser Bedingungen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="a38c3-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a38c3-239">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Auftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-240">Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="a38c3-240">Production order</span></span></td>
<td><span data-ttu-id="a38c3-241">Bevor oder nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="a38c3-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="a38c3-242">Nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="a38c3-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="a38c3-243">Die Anforderung für einen Qualitätsprüfungsauftrag kann einen bestimmten Betrieb oder ein Element oder eine Kombination dieser Bedingungen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="a38c3-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a38c3-244">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Produktionsauftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-245">Produktionsauftrag, der über einen Arbeitsplan-Arbeitsgang verfügt</span><span class="sxs-lookup"><span data-stu-id="a38c3-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="a38c3-246">Bevor oder nachdem der für einen Arbeitsgang abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="a38c3-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="a38c3-247">Nachdem die Meldung für den letzten Arbeitsgang abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="a38c3-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="a38c3-248">Die Anforderung für einen Qualitätsprüfungsauftrag kann einen bestimmten Standort, ein Element oder eine Vorgangsressource oder eine Kombination dieser Bedingungen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="a38c3-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a38c3-249">Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Arbeitsplan-Arbeitsgang bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-250">Bestand</span><span class="sxs-lookup"><span data-stu-id="a38c3-250">Inventory</span></span></td>
<td><span data-ttu-id="a38c3-251">Ein Qualitätsprüfungsauftrag kann nicht automatisch für eine Transaktion in einer Bestandserfassung oder für Umlagerungserfassungstransaktionen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a38c3-252">Ein Qualitätsprüfungsauftrag muss manuell für die Bestandsmenge eines Elements erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="a38c3-253">Physischer Lagerbestand ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a38c3-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="a38c3-254">Beispiele zur automatischen Generierung von Qualitätsprüfungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="a38c3-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="a38c3-255">Einkaufen</span><span class="sxs-lookup"><span data-stu-id="a38c3-255">Purchasing</span></span>

<span data-ttu-id="a38c3-256">Im Einkauf, wenn Sie das Feld **Ereignistyp** auf *Produktzugang* und das **Ausführung**-Feld auf *Später* auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="a38c3-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="a38c3-257">Wenn die Option **Pro aktualisierter Menge** auf *Ja* festgelegt wird, wird ein Qualitätsprüfungsauftrag für jeden Zugang für den Auftrag anhand der Eingangsmenge und Einstellungen in der Artikelmusteraufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="a38c3-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="a38c3-258">Wenn eine Menge für den Auftrag eingeht, werden neue Qualitätsprüfungsaufträge auf Grundlage der neuen Eingangsmenge generiert.</span><span class="sxs-lookup"><span data-stu-id="a38c3-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="a38c3-259">Wenn die Option **Pro aktualisierter Menge** auf *Nein* festgelegt wird, wird ein Qualitätsprüfungsauftrag für den ersten Zugang für den Auftrag anhand der Eingangsmenge generiert.</span><span class="sxs-lookup"><span data-stu-id="a38c3-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="a38c3-260">Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="a38c3-261">Qualitätsprüfungsaufträge werden nicht für nachfolgende Zugänge für den Auftrag generiert.</span><span class="sxs-lookup"><span data-stu-id="a38c3-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="a38c3-262">Produktion</span><span class="sxs-lookup"><span data-stu-id="a38c3-262">Production</span></span>

<span data-ttu-id="a38c3-263">In der Produktion, wenn Sie das Feld **Ereignistyp** auf *Fertigmeldung* und das **Ausführung**-Feld auf *Später* auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="a38c3-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="a38c3-264">Wenn die Option **Pro aktualisierter Menge** auf *Ja* festgelegt wird, wird ein Qualitätsprüfungsauftrag auf der Basis einer jeden fertiggestellten Menge und der Einstellungen in der Artikelmusteraufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="a38c3-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="a38c3-265">Jedes Mal, wenn eine Menge als fertiggestellt gegen den Produktionsauftrag gemeldet wird, werden neue Qualitätsprüfungsaufträge basierend auf der neu fertiggestellten Menge erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="a38c3-266">Diese Generierungslogik ist mit dem Einkauf konsistent.</span><span class="sxs-lookup"><span data-stu-id="a38c3-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="a38c3-267">Wenn die Option **Pro aktualisierter Menge** auf *Nein* festgelegt wird, wird ein Qualitätsprüfungsauftrag das erste Mal, wenn eine Menge als fertig gemeldet wird, anhand der fertiggestellten Menge generiert.</span><span class="sxs-lookup"><span data-stu-id="a38c3-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="a38c3-268">Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen der Artikelmusteraufnahme erstellt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="a38c3-269">Qualitätsprüfungsaufträge werden nicht für nachfolgende fertiggestellte Mengen generiert.</span><span class="sxs-lookup"><span data-stu-id="a38c3-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a38c3-270">Qualitätsspezifikation</span><span class="sxs-lookup"><span data-stu-id="a38c3-270">Quality specification</span></span></th>
<th><span data-ttu-id="a38c3-271">Pro aktualisierter Menge</span><span class="sxs-lookup"><span data-stu-id="a38c3-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="a38c3-272">Pro Rückverfolgungsangabe</span><span class="sxs-lookup"><span data-stu-id="a38c3-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="a38c3-273">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a38c3-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a38c3-274">Prozentsatz: 10 %</span><span class="sxs-lookup"><span data-stu-id="a38c3-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="a38c3-275">Ja</span><span class="sxs-lookup"><span data-stu-id="a38c3-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="a38c3-276">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="a38c3-276">Batch number: No</span></span></p>
<p><span data-ttu-id="a38c3-277">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="a38c3-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="a38c3-278">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="a38c3-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="a38c3-279">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="a38c3-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="a38c3-280">Qualitätsprüfungsauftrag 1 zu 3 (10% von 30)</span><span class="sxs-lookup"><span data-stu-id="a38c3-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a38c3-281">Fertigmeldung für 70</span><span class="sxs-lookup"><span data-stu-id="a38c3-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="a38c3-282">Qualitätsprüfungsauftrag 2 zu 7 (10% der verbleibenden Auftragsmenge, die in diesem Fall 70 beträgt)</span><span class="sxs-lookup"><span data-stu-id="a38c3-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-283">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="a38c3-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="a38c3-284">Nr.</span><span class="sxs-lookup"><span data-stu-id="a38c3-284">No</span></span></td>
<td>
<p><span data-ttu-id="a38c3-285">Chargennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="a38c3-285">Batch number: No</span></span></p>
<p><span data-ttu-id="a38c3-286">Seriennummer: Nein</span><span class="sxs-lookup"><span data-stu-id="a38c3-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="a38c3-287">Auftragsmenge: 100</span><span class="sxs-lookup"><span data-stu-id="a38c3-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="a38c3-288">Fertigmeldung für 30</span><span class="sxs-lookup"><span data-stu-id="a38c3-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="a38c3-289">Qualitätsprüfungsauftrag 1 zu 1 (für die erste als fertig gemeldete Menge, die einen festen Wert von 1 hat)</span><span class="sxs-lookup"><span data-stu-id="a38c3-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="a38c3-290">Qualitätsprüfungsauftrag 2 für 1 (für die Restmenge, die immer noch den festen Wert 1 hat)</span><span class="sxs-lookup"><span data-stu-id="a38c3-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a38c3-291">Fertigmeldung für 10</span><span class="sxs-lookup"><span data-stu-id="a38c3-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="a38c3-292">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a38c3-293">Fertigmeldung für 60</span><span class="sxs-lookup"><span data-stu-id="a38c3-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="a38c3-294">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-295">Feste Menge: 1</span><span class="sxs-lookup"><span data-stu-id="a38c3-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="a38c3-296">Ja</span><span class="sxs-lookup"><span data-stu-id="a38c3-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="a38c3-297">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="a38c3-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="a38c3-298">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="a38c3-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="a38c3-299">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="a38c3-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="a38c3-300">Fertigmeldung für 3: 1 für Batch-Nummer b1, Seriennummer s1; 1 für Batch-Nummer b2, Seriennummer s2; und 1 für Batch-Nummer b3, Seriennummer s3</span><span class="sxs-lookup"><span data-stu-id="a38c3-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="a38c3-301">Qualitätsprüfungsauftrag 1 zu 1 von Batch-Nummer b1, Seriennummer s1</span><span class="sxs-lookup"><span data-stu-id="a38c3-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="a38c3-302">Qualitätsprüfungsauftrag 2 für 1 von Batch-Nummer b2, Seriennummer s2</span><span class="sxs-lookup"><span data-stu-id="a38c3-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="a38c3-303">Qualitätsprüfungsauftrag 3 für 1 der Batchnummer b3, Seriennummer s3</span><span class="sxs-lookup"><span data-stu-id="a38c3-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a38c3-304">Bericht als fertig für 2: 1 für Batch-Nummer b4, Seriennummer s4; und 1 für Batch-Nummer b5, Seriennummer s5</span><span class="sxs-lookup"><span data-stu-id="a38c3-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="a38c3-305">Qualitätsprüfungsauftrag 4 für 1 der Batchnummer b4, Seriennummer s4</span><span class="sxs-lookup"><span data-stu-id="a38c3-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="a38c3-306">Qualitätsprüfungsauftrag 5 für 1 der Batchnummer b5, Seriennummer s5</span><span class="sxs-lookup"><span data-stu-id="a38c3-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="a38c3-307"><strong>Hinweis:</strong> Die Charge kann wiederverwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a38c3-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a38c3-308">Feste Menge: 2</span><span class="sxs-lookup"><span data-stu-id="a38c3-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="a38c3-309">Nr.</span><span class="sxs-lookup"><span data-stu-id="a38c3-309">No</span></span></td>
<td>
<p><span data-ttu-id="a38c3-310">Chargennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="a38c3-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="a38c3-311">Seriennummer: Ja</span><span class="sxs-lookup"><span data-stu-id="a38c3-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="a38c3-312">Auftragsmenge: 10</span><span class="sxs-lookup"><span data-stu-id="a38c3-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="a38c3-313">Fertigmeldung für 4: 1 für Batchnummer b1, Seriennummer s1; 1 für Batchnummer b2, Seriennummer s2; 1 für Batchnummer b3, Seriennummer s3; und 1 für Batchnummer b4, Seriennummer s4</span><span class="sxs-lookup"><span data-stu-id="a38c3-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="a38c3-314">Qualitätsprüfungsauftrag 1 zu 1 von Batch-Nummer b1, Seriennummer s1</span><span class="sxs-lookup"><span data-stu-id="a38c3-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="a38c3-315">Qualitätsprüfungsauftrag 2 für 1 von Batch-Nummer b2, Seriennummer s2</span><span class="sxs-lookup"><span data-stu-id="a38c3-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="a38c3-316">Qualitätsprüfungsauftrag 3 für 1 der Batchnummer b3, Seriennummer s3</span><span class="sxs-lookup"><span data-stu-id="a38c3-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="a38c3-317">Qualitätsprüfungsauftrag 4 für 1 der Batchnummer b4, Seriennummer s4</span><span class="sxs-lookup"><span data-stu-id="a38c3-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="a38c3-318">Qualitätsprüfungsauftrag 5 zu 2, ohne Bezug auf eine Batch-Nummer und eine Seriennummer</span><span class="sxs-lookup"><span data-stu-id="a38c3-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="a38c3-319">Bericht als beendet für 6: 1 für Batch-Nummer b5, Seriennummer s5; 1 für Batch-Nummer b6, Seriennummer s6; 1 für Batch-Nummer b7, Seriennummer s7; 1 für Batch-Nummer b8, Seriennummer s8; 1 für Batch-Nummer b9, Seriennummer s9; und 1 für Batch-Nummer b10, Seriennummer s10</span><span class="sxs-lookup"><span data-stu-id="a38c3-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="a38c3-320">Es werden keine Qualitätsprüfungsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="a38c3-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="a38c3-321">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a38c3-321">Additional resources</span></span>

- [<span data-ttu-id="a38c3-322">Qualitätsmanagementprozesse</span><span class="sxs-lookup"><span data-stu-id="a38c3-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="a38c3-323">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="a38c3-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="a38c3-324">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="a38c3-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
