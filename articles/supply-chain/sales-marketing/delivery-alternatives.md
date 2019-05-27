---
title: Alternative Lieferung
description: Auftragsabnehmer können die Lieferungsalternativenseite verwenden, um alternative Auftragserfüllungsoptionen zu ermitteln.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 1fbf8f08322c954a482777abcf041ff0b9d8fb77
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555861"
---
# <a name="delivery-alternatives"></a><span data-ttu-id="c37a1-103">Alternative Lieferung</span><span class="sxs-lookup"><span data-stu-id="c37a1-103">Delivery alternatives</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c37a1-104">Auftragsabnehmer können die **Lieferungsalternativenseite** verwenden, um alternative Auftragserfüllungsoptionen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c37a1-104">Sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="c37a1-105">Die neute Seite **Alternative Lieferung** gibt ein besserer Überblick über alle alternativen Optionen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-105">The **Delivery alternatives** page layout gives an overview of all alternative options.</span></span> <span data-ttu-id="c37a1-106">Die Personen, die den Auftrag entgegennehmen können auch hinter das aktuelle Unternehmen blicken, um mehr über die Erfüllungsverkaufschancen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="c37a1-106">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="c37a1-107">Sie können nun Intercompany-Verkaufschancen und Verkaufschancen von externen Kreditoren anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-107">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="c37a1-108">Mithilfe der Funktion nach Lieferdatum sortieren, können Auftragsabnehmer eine intelligente Liste der Lieferalternativen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-108">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="c37a1-109">Außerdem helfen Parameter, die vorgeschlagenen Lieferungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c37a1-109">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="c37a1-110">Da die Transportzeit die Lieferdaten beeinflussen kann, können Auftragsabnehmer die verschiedenen Transportmöglichkeiten ansehen, die Spediteure anbieten.</span><span class="sxs-lookup"><span data-stu-id="c37a1-110">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="c37a1-111">Da Detailinformationen zu jedem Vorschlag angezeigt werden, können Auftragsannehmer informierte Entscheidungen direkt über die Seite **Lieferalternativen durch Anzeigen** machen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-111">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="c37a1-112">Öffnen Sie die Lieferungsalternativeseite</span><span class="sxs-lookup"><span data-stu-id="c37a1-112">Open the Delivery alternatives page</span></span>
<span data-ttu-id="c37a1-113">Sie können die Seite **Alternative Lieferung** aus der Auftragsposition öffnen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-113">You can open the **Delivery alternatives** page from the sales order line.</span></span>

1.  <span data-ttu-id="c37a1-114">Klicken Sie auf **Produkte und Lieferung** &gt; **Lieferalternativen**.</span><span class="sxs-lookup"><span data-stu-id="c37a1-114">Click **Products and supply** &gt; **Delivery alternatives**.</span></span>
2.  <span data-ttu-id="c37a1-115">Klicken Sie auf &gt; **Positionsdetails** **Lieferung** &gt; **Lieferalternativen.**</span><span class="sxs-lookup"><span data-stu-id="c37a1-115">Click **Line details** &gt; **Delivery** &gt; **Delivery alternatives.**</span></span>

<span data-ttu-id="c37a1-116">Sie können auch die Seite **Lieferalternativen** über den Arbeitsbereich **Abfrage Auftragsverarbeitung und -abfrage**. Klicken Sie dann auf **Bestellungen und Favoriten** &gt; **Verzögerte Auftragspositionen** &gt; **Lieferalternativen** **Hinweis:** Sie können die Seite **Lieferalternativen** nur öffnen, wenn beide Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="c37a1-116">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then clicking **Orders and favorites** &gt; **Delayed order lines** &gt; **Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

-   <span data-ttu-id="c37a1-117">Alle zwingenden Verkaufspositionsinformationen sind ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c37a1-117">All mandatory sales line information is filled in.</span></span>
-   <span data-ttu-id="c37a1-118">Das Feld **Lieferdatumskontrolle** ist auf einen anderen Wert als **None** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c37a1-118">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="c37a1-119">Methoden für die Lieferdatumskontrolle</span><span class="sxs-lookup"><span data-stu-id="c37a1-119">Delivery date control methods</span></span>
<span data-ttu-id="c37a1-120">Die Lieferdatumsteuermethode bestimmt, wie das System Versanddatum einrichtet, wie Lieferalternativen berechnet und welche Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c37a1-120">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="c37a1-121">Beachten Sie, dass die Lieferdatumskontrolle Kalender in Erwägung ziehen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-121">Note that delivery data control takes calendars into consideration.</span></span> <span data-ttu-id="c37a1-122">Daher können die folgenden Kalender das vorgeschlagene Empfangsdatum betreffen: Kalender, der dem Lagerort zugeordnet ist, Transportkalender, Kreditorenkalender und Kundenkalender.</span><span class="sxs-lookup"><span data-stu-id="c37a1-122">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="c37a1-123">Die folgende Tabelle beschreibt jede Methode zur Lieferdatumskontrolle.</span><span class="sxs-lookup"><span data-stu-id="c37a1-123">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c37a1-124"><strong>Methode</strong></span><span class="sxs-lookup"><span data-stu-id="c37a1-124"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="c37a1-125"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="c37a1-125"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37a1-126"><strong>Keines</strong></span><span class="sxs-lookup"><span data-stu-id="c37a1-126"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="c37a1-127">Lieferalternativen für Verkaufspositionen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c37a1-127">Delivery alternatives for sales lines aren&#39;t supported.</span></span> <span data-ttu-id="c37a1-128">Diese Option deaktiviert die Lieferdatensteuerung.</span><span class="sxs-lookup"><span data-stu-id="c37a1-128">This option turns off delivery data control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37a1-129"><strong>Verkaufslieferzeit</strong></span><span class="sxs-lookup"><span data-stu-id="c37a1-129"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="c37a1-130">Lieferalternativen werden basierend auf vordefinierten die Verkaufslieferzeit berechnet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-130">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="c37a1-131">Die Transporttage werden aufgrund der Lieferart berechnet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-131">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="c37a1-132">Lieferalternativen umfassen Lagerorte, die verfügbaren Lagerbestand haben und Angebots-/Nachfrageaufträge.</span><span class="sxs-lookup"><span data-stu-id="c37a1-132">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37a1-133"><strong>VfZ</strong></span><span class="sxs-lookup"><span data-stu-id="c37a1-133"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="c37a1-134">Lieferalternativen werden auf Basis der Logik der verfügbaren Zusagen (VfZ) berechnet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-134">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="c37a1-135">Die aktuelle Verfügbarkeit und die erwartete zukünftige Verfügbarkeit werden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c37a1-135">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="c37a1-136">Die Transporttage werden aufgrund der Lieferart berechnet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-136">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="c37a1-137">Lieferalternativen umfassen Lagerorte, die verfügbaren Lagerbestand haben und Angebots-/Nachfrageaufträge.</span><span class="sxs-lookup"><span data-stu-id="c37a1-137">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37a1-138"><strong>VfZ + Sicherheitszuschlag</strong></span><span class="sxs-lookup"><span data-stu-id="c37a1-138"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="c37a1-139">Lieferalternativen werden wie bei der VfZ-Methode berechnet aber der Sicherheitszuschlag ist in der Berechnung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c37a1-139">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37a1-140"><strong>CTP</strong></span><span class="sxs-lookup"><span data-stu-id="c37a1-140"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="c37a1-141">Lieferalternativen werden auf Basis der Logik der verfügbaren Zusagen (CTP) berechnet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-141">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="c37a1-142">Mrp-Auflösung wird verwendet, um die Verfügbarkeit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-142">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="c37a1-143">Beachten Sie, dass mindestens das CTP Lieferdatum die Verkaufslieferzeit ausgleicht.</span><span class="sxs-lookup"><span data-stu-id="c37a1-143">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="c37a1-144">Die Transporttage werden aufgrund der Lieferart berechnet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-144">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="c37a1-145">Lieferalternativen umfassen auch für die folgenden Lagerorte:</span><span class="sxs-lookup"><span data-stu-id="c37a1-145">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="c37a1-146">Aktueller Lagerort</span><span class="sxs-lookup"><span data-stu-id="c37a1-146">Current warehouse</span></span></li>
<li><span data-ttu-id="c37a1-147">Standardlagerort</span><span class="sxs-lookup"><span data-stu-id="c37a1-147">Default warehouse</span></span></li>
<li><span data-ttu-id="c37a1-148">Alle Lagerorte, die verfügbaren Lagerbestand haben</span><span class="sxs-lookup"><span data-stu-id="c37a1-148">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="c37a1-149">Alle Lagerorte, die Lieferaufträge haben</span><span class="sxs-lookup"><span data-stu-id="c37a1-149">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="c37a1-150">Alle Lagerorte, die eine aktive Stücklisten (BOM)- Versionen haben</span><span class="sxs-lookup"><span data-stu-id="c37a1-150">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="c37a1-151">Hier werden Informationen zu Lieferalternativen angezeigt</span><span class="sxs-lookup"><span data-stu-id="c37a1-151">View information about delivery alternatives</span></span>
<span data-ttu-id="c37a1-152">Dieser Abschnitt beschreibt die Informationen zu den Lieferalternativen, die auf jeder Registerkarte auf der Seite **Lieferalternativen** verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c37a1-152">This section describes the information about delivery alternatives that is available on each tab of the **Delivery alternatives** page.</span></span>

### <a name="products"></a><span data-ttu-id="c37a1-153">Produkte</span><span class="sxs-lookup"><span data-stu-id="c37a1-153">Products</span></span>

<span data-ttu-id="c37a1-154">Diese Registerkarte zeigt eine Zusammenfassung des Produkts und Details der aktuellen Auftragsposition.</span><span class="sxs-lookup"><span data-stu-id="c37a1-154">This tab shows a summary of the product and details of the current sales line.</span></span>

### <a name="delivery-alternatives"></a><span data-ttu-id="c37a1-155">Alternative Lieferung</span><span class="sxs-lookup"><span data-stu-id="c37a1-155">Delivery alternatives</span></span>

<span data-ttu-id="c37a1-156">Diese Registerkarte ist eine Liste von Lieferalternativen , die nach Empfangsdatum sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="c37a1-156">This tab shows a list of delivery alternatives that is sorted by receipt data.</span></span> <span data-ttu-id="c37a1-157">Über der Liste können Sie auswählen, welche Optionen basierend auf den Vorschlägen, ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c37a1-157">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="c37a1-158">Sie können auch die Lieferart auswählen, die die Transporttage bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c37a1-158">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="c37a1-159">Die folgenden Optionen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="c37a1-159">The following options are available:</span></span>

-   <span data-ttu-id="c37a1-160">**Schließen Sie andere Produktvarianten ein** - Diese Option ist auch für Produkte verfügbar, die Produktvarianten haben.</span><span class="sxs-lookup"><span data-stu-id="c37a1-160">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="c37a1-161">Er umfasst Lieferalternativen für weitere Varianten des Produkts.</span><span class="sxs-lookup"><span data-stu-id="c37a1-161">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="c37a1-162">Diese Option ist nicht für CTP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c37a1-162">This option isn't available for CTP.</span></span>
-   <span data-ttu-id="c37a1-163">**Schließen Sie Teilmenge ein** -, Standardmäßig sind nur Vorschläge verfügbar, die die gesamte Menge der Verkaufsposition einschließen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-163">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="c37a1-164">Wählen Sie diese Option, um Vorschläge einzubeziehen, die der Auftragsposition nur teilweise entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-164">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="c37a1-165">Diese Option ist hilfreich, wenn der Debitor ein früheres Lieferdatum anfordert und Teillieferung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c37a1-165">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
-   <span data-ttu-id="c37a1-166">**Schließen Sie ein späteres Datum** -, Standardmäßig werden nur Anforderungen berücksichtigt, die besser sind (früher) als das aktuelle Datum in der Verkaufsposition.</span><span class="sxs-lookup"><span data-stu-id="c37a1-166">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="c37a1-167">Wählen Sie diese Option aus, um spätere Daten einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-167">Select this option to include later dates.</span></span> <span data-ttu-id="c37a1-168">Diese Option kann in den folgenden Situationen hilfreich sein, in dem Parameter nicht das Datum Priorität haben.</span><span class="sxs-lookup"><span data-stu-id="c37a1-168">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="c37a1-169">So werden beispielsweise ein Kreditor oder ein bestimmter Lagerort bevorzugt werden.</span><span class="sxs-lookup"><span data-stu-id="c37a1-169">For example, a specific vendor or warehouse might be preferred.</span></span>
-   <span data-ttu-id="c37a1-170">**Lieferart** - Wählen den bevorzugten Liefermodus, um Kosten und Transportzeiten zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="c37a1-170">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="c37a1-171">Sie finden die Auswirkungen sofort in den vorgeschlagenen Lieferalternativen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-171">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="c37a1-172">Daher ist es einfach, die Alternativen zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-172">Therefore, it's easy to compare the alternatives.</span></span>
-   <span data-ttu-id="c37a1-173">**Beschaffung einschließen** Wenn Beschaffung aktiviert ist, schließen die vorgeschlagenen Lieferalternativen Optionen ein, die sowohl Optionen für externe Kreditoren und andere Unternehmen in der Unternehmensgruppe (Intercompany) ein.</span><span class="sxs-lookup"><span data-stu-id="c37a1-173">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="c37a1-174">Die Option **Beschaffung einschließen** wird für die VfZ-Kalkulation und die Lieferdatumssteuerung VfZ + Sicherheitszuschlag unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c37a1-174">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="c37a1-175">Beschaffungsoptionen vom Standardlieferanten für das Produkt und alle genehmigten Lieferanten für das Produkt sind eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-175">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
-   <span data-ttu-id="c37a1-176">Bei externen Kreditoren basiert die Berechnung auf Grundlage der Lieferzeit.</span><span class="sxs-lookup"><span data-stu-id="c37a1-176">For external vendors, the calculation is based on the purchase lead time.</span></span>
-   <span data-ttu-id="c37a1-177">Für Intercompany berücksichtigt die Berechung, was vom Beschaffungsunternehmen verfügbar ist, basierend auf der Lieferdatumskontrolle im Beschaffungsunternehmen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-177">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
-   <span data-ttu-id="c37a1-178">**Liefertyp** (Nur relevant für Beschaffung)</span><span class="sxs-lookup"><span data-stu-id="c37a1-178">**Delivery type** (Relevant for procurement)</span></span>
    -   <span data-ttu-id="c37a1-179">**Bestand** - Produkte werden vom Beschaffungslagerort zum Standort/Lagerort in der Verkaufsposition versendet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-179">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="c37a1-180">Sie werden dann von diesem Lagerort an den Kunden versendet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-180">They are then shipped from that warehouse to the customer.</span></span>
    -   <span data-ttu-id="c37a1-181">**Direktlieferung** - Produkte werden direkt vom Beschaffungslagerort an den Kunden versendet.</span><span class="sxs-lookup"><span data-stu-id="c37a1-181">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="availability-information"></a><span data-ttu-id="c37a1-182">Verfügbarkeitsinformationen</span><span class="sxs-lookup"><span data-stu-id="c37a1-182">Availability information</span></span>

<span data-ttu-id="c37a1-183">Informationen in dieser Registerkarte beziehen sich auf die Lieferung alternativer ausgewählter Positionen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-183">Information on this tab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="c37a1-184">Die folgenden Informationen werden, je nach spezifischer Lieferdatumskontrolle für die Auftragsposition angezeigt:</span><span class="sxs-lookup"><span data-stu-id="c37a1-184">The following information is shown, depending on the delivery date control for the sales line:</span></span>

-   <span data-ttu-id="c37a1-185">**Verkaufslieferzeit**</span><span class="sxs-lookup"><span data-stu-id="c37a1-185">**Sales lead time**</span></span>
    -   <span data-ttu-id="c37a1-186">**Verfügbar heute** - Zeigt den aktuellen physischen, physisch reservierten und physisch verfügbaren Bestand an.</span><span class="sxs-lookup"><span data-stu-id="c37a1-186">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="c37a1-187">**Parameter** - Zeigt die Bestandeinheit und die Verkaufslieferzeit.</span><span class="sxs-lookup"><span data-stu-id="c37a1-187">**Parameters** - Show the inventory unit and sales lead time.</span></span>

-   <span data-ttu-id="c37a1-188">**VfZ und VfZ + Sicherheitszuschlag für Warenabgang**</span><span class="sxs-lookup"><span data-stu-id="c37a1-188">**ATP and ATP + Issue margin**</span></span>
    -   <span data-ttu-id="c37a1-189">**Verfügbar heute** - Zeigt den aktuellen physischen, physisch reservierten und physisch verfügbaren Bestand an.</span><span class="sxs-lookup"><span data-stu-id="c37a1-189">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="c37a1-190">**Parameter** - Zeigt die Bestandeinheit und die Verkaufslieferzeit.</span><span class="sxs-lookup"><span data-stu-id="c37a1-190">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="c37a1-191">**Künftige Verfügbarkeit** - Zeigt eine grafische Darstellung der aktuellen und künftigen Verfügbarkeit für den ausgewählten Standort und den Lagerort unter **Lieferalternativen**.</span><span class="sxs-lookup"><span data-stu-id="c37a1-191">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="c37a1-192">Sie können auf die Diagrammspalten klicken, um ausführliche Informationen zur künftigen Verfügbarkeit des Produkts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-192">You can click the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="c37a1-193">Der Schieberegler wird eine Liste relevanter Bedarfs- und Angebotaufträge innerhalb des VfZ-Planungszeitraums anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-193">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

-   <span data-ttu-id="c37a1-194">**CTP**</span><span class="sxs-lookup"><span data-stu-id="c37a1-194">**CTP**</span></span>
    -   <span data-ttu-id="c37a1-195">**Verfügbar heute** - Zeigt den aktuellen physischen, physisch reservierten und physisch verfügbaren Bestand an.</span><span class="sxs-lookup"><span data-stu-id="c37a1-195">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="c37a1-196">**Parameter** - Zeigt die Bestandeinheit und die Verkaufslieferzeit.</span><span class="sxs-lookup"><span data-stu-id="c37a1-196">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="c37a1-197">**Auflösung** - Zeigt eine Lieferauflösung der ausgewählten Lieferalternative.</span><span class="sxs-lookup"><span data-stu-id="c37a1-197">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="c37a1-198">Sie können **Einstellungen** verwenden, um die Felder und die Bestanddimensionen zu ändern, die bei der Auflösung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c37a1-198">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="impact-of-selected-alternative"></a><span data-ttu-id="c37a1-199">Auswirkungen der gewählten Alternative</span><span class="sxs-lookup"><span data-stu-id="c37a1-199">Impact of selected alternative</span></span>

<span data-ttu-id="c37a1-200">Diese Registerkarte zeigt die Auswirkungen auf die ausgewählte Lieferungsalternative.</span><span class="sxs-lookup"><span data-stu-id="c37a1-200">This tab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="c37a1-201">Wenn Sie **OK** klicken, wird die Auftragsposition mit den markierten Werte in den Spalten AUSGEWÄHLT aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c37a1-201">If you click **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="c37a1-202">Beachten Sie, dass, wenn die Menge in der ausgewählten Lieferalternative kleiner als die Menge in der Auftragsposition ist, und die Auftragsposition in zwei Positionen aufgeteilt wird: eine Position für die ausgewählte Menge und eine Zeile für die Restmenge.</span><span class="sxs-lookup"><span data-stu-id="c37a1-202">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="c37a1-203">Sie können den Handelszweig auch aktualisieren, damit die Zeitplanpositionen übereinstimmt und die Preiskalkulation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="c37a1-203">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

<a name="additional-resources"></a><span data-ttu-id="c37a1-204">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c37a1-204">Additional resources</span></span>
--------

[<span data-ttu-id="c37a1-205">Lieferterminzusage</span><span class="sxs-lookup"><span data-stu-id="c37a1-205">Order promising</span></span>](delivery-dates-available-promise-calculations.md)




