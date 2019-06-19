---
title: Kostenkonfiguration für die verteilte Auftragsverwaltung (DOM)
description: Dieses Thema behandelt die Kostenkonfiguration für die Funktion zur verteilten Auftragsverwaltung (DOM) in Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80e7a033467c3d94d55f06daa05f99bd27e19a29
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606778"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="ed18e-103">Kostenkonfiguration für die verteilte Auftragsverwaltung (DOM)</span><span class="sxs-lookup"><span data-stu-id="ed18e-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed18e-104">Um den optimalen Standort zur Erledigung von Aufträgen zu ermitteln, berücksichtigen Organisationen mehrere Kostenkomponenten.</span><span class="sxs-lookup"><span data-stu-id="ed18e-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="ed18e-105">Dazu gehören unter anderem Kosten für Versand, Bearbeitung und Verpackung.</span><span class="sxs-lookup"><span data-stu-id="ed18e-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="ed18e-106">Anhand einer berechneten Kombination dieser Kosten wird der Erfüllungslagerplatz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ed18e-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="ed18e-107">Bei der Verbesserung der Zuweisung von Aufträgen zu Erfüllungslagerplätzen durch die erste Iteration der verteilten Auftragsverwaltung (DOM) in Microsoft Dynamics 365 for Retail wurde nur die Entfernung als Faktor berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ed18e-107">When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="ed18e-108">Auch wenn diese ggf. mit Kosten korreliert, ist sie nicht mit Kosten identisch.</span><span class="sxs-lookup"><span data-stu-id="ed18e-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="ed18e-109">So kann ein Übernachtversand über dieselbe Entfernung mehr als ein Drei- oder Sieben-Tage-Versand kosten.</span><span class="sxs-lookup"><span data-stu-id="ed18e-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="ed18e-110">Mit der Funktion zur Kostenkonfiguration können Einzelhändler zusätzliche Kostenkomponenten anlegen und konfigurieren, die zur Ermittlung des besten Standortes zur Erfüllung von Auftragspositionen berechnet und berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="ed18e-111">Sind Kostenkomponenten konfiguriert, verwendet der DOM-Solver bei der Ermittlung des besten Erfüllungslagerplatzes nur diese Kostendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="ed18e-112">Die Entfernungskomponente wird nicht als Kosten berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ed18e-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="ed18e-113">Sind keine Kostenkomponenten konfiguriert, verwendet der DOM-Solver bei der Ermittlung des besten Erfüllungslagerplatzes die Entfernungskomponente als Kosten.</span><span class="sxs-lookup"><span data-stu-id="ed18e-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="ed18e-114">Kostenkomponenten einrichten</span><span class="sxs-lookup"><span data-stu-id="ed18e-114">Set up cost components</span></span>

<span data-ttu-id="ed18e-115">In System können zwei maßgebliche Kostenkomponenten festgelegt werden: **Versand** und **Sonstiges**.</span><span class="sxs-lookup"><span data-stu-id="ed18e-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="ed18e-116">Wie in der folgenden Tabelle dargestellt, unterstützen beide Typen von Kostenkomponenten mehrere Berechnungsgrundlagen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ed18e-117">Typ der Kostenkomponente</span><span class="sxs-lookup"><span data-stu-id="ed18e-117">Cost component type</span></span></th>
<th><span data-ttu-id="ed18e-118">Berechnungsbasis</span><span class="sxs-lookup"><span data-stu-id="ed18e-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ed18e-119">Versand</span><span class="sxs-lookup"><span data-stu-id="ed18e-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ed18e-120">Einfach</span><span class="sxs-lookup"><span data-stu-id="ed18e-120">Simple</span></span></li>
<li><span data-ttu-id="ed18e-121">Mehrstufig</span><span class="sxs-lookup"><span data-stu-id="ed18e-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ed18e-122">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="ed18e-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ed18e-123">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed18e-123">Sales order</span></span></li>
<li><span data-ttu-id="ed18e-124">Verkaufsposition</span><span class="sxs-lookup"><span data-stu-id="ed18e-124">Sales line</span></span></li>
<li><span data-ttu-id="ed18e-125">Ort</span><span class="sxs-lookup"><span data-stu-id="ed18e-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="ed18e-126">Kostenkomponententyp „Versand“</span><span class="sxs-lookup"><span data-stu-id="ed18e-126">Shipping cost component type</span></span>

<span data-ttu-id="ed18e-127">In diesem Abschnitt wird beschrieben, wie die einzelnen Kombinationen des Kostenkomponententyps **Versand** und eine Berechnungsgrundlage für Versandkosten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="ed18e-128">Ferner wird erläutert, wie der DOM-Solver die einzelnen Kombinationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed18e-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="ed18e-129">Kostenkomponententyp = Versand und Berechnungsgrundlage = Einfach</span><span class="sxs-lookup"><span data-stu-id="ed18e-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="ed18e-130">Wird eine Kombination aus dem Kostenkomponententyp **Versand** und der Berechnungsgrundlage **Einfach** verwendet, beruhen die Versandkosten einer Lieferart entweder auf einer Kostenpauschale oder auf der Entfernung.</span><span class="sxs-lookup"><span data-stu-id="ed18e-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="ed18e-131">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="ed18e-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ed18e-132">**Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ed18e-133">**Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ed18e-134">**Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</span><span class="sxs-lookup"><span data-stu-id="ed18e-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ed18e-135">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</span><span class="sxs-lookup"><span data-stu-id="ed18e-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ed18e-136">**Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ed18e-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ed18e-137">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ed18e-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ed18e-138">**Unternehmen**: Geben Sie die juristische Person an, für die Kostenfaktor konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ed18e-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="ed18e-139">Alle Positionen der Berechnungskriterien müssen sich auf dieselbe juristische Person beziehen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="ed18e-140">**Lieferarten**: Geben Sie die Lieferarten an, für die die Kosten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="ed18e-141">**Berechnungstyp**: Geben Sie an, wie die Kosten für die einzelnen Lieferarten berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="ed18e-142">Es werden zwei Berechnungsarten unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ed18e-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="ed18e-143">**Fest**: Für die Lieferart wird eine Pauschale verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed18e-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="ed18e-144">Bei Auswahl dieser Berechnungsart bestimmt das Feld **Kosten** die Kostenpauschale.</span><span class="sxs-lookup"><span data-stu-id="ed18e-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="ed18e-145">**Pro Entfernungseinheit**: Die Kosten für die Lieferart werden berechnet, indem der im Feld **Kosten** angegebene Wert mit der Entfernung zwischen Lieferadresse und Standorten multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ed18e-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="ed18e-146">**Kosten**: Geben Sie den Wert an, der im Zusammenhang mit dem Feld **Berechnungstyp** verwendet wird, um die Kosten für eine Lieferart zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="ed18e-147">Kostenkomponententyp = Versand und Berechnungsgrundlage = Mehrstufig</span><span class="sxs-lookup"><span data-stu-id="ed18e-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="ed18e-148">Wird eine Kombination aus dem Kostenkomponententyp **Versand** und der Berechnungsgrundlage **Mehrstufig** verwendet, beruhen die Versandkosten einer Lieferart entweder auf einer Kostenpauschale oder auf der Entfernung.</span><span class="sxs-lookup"><span data-stu-id="ed18e-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="ed18e-149">Allerdings beruht die Entfernung bei dieser Kombination auf einer mehrstufigen Entfernungsskala.</span><span class="sxs-lookup"><span data-stu-id="ed18e-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="ed18e-150">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="ed18e-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ed18e-151">**Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ed18e-152">**Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ed18e-153">**Standardkosten**: Geben Sie die Kosten an, die für eine Lieferart verwendet werden sollen, wenn die Entfernung zwischen der Lieferadresse und dem Standort nicht in eine der mehrstufigen Entfernungen der Lieferart fällt.</span><span class="sxs-lookup"><span data-stu-id="ed18e-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="ed18e-154">**Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</span><span class="sxs-lookup"><span data-stu-id="ed18e-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ed18e-155">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</span><span class="sxs-lookup"><span data-stu-id="ed18e-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ed18e-156">**Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ed18e-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ed18e-157">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ed18e-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ed18e-158">**Unternehmen**: Geben Sie die juristische Person an, für die Kostenfaktor konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ed18e-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="ed18e-159">Alle Positionen der Berechnungskriterien müssen sich auf dieselbe juristische Person beziehen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="ed18e-160">**Lieferarten**: Geben Sie die Lieferarten an, für die die Kosten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="ed18e-161">**Entfernungstyp**: Geben Sie an, ob die mehrstufige Entfernungsdefinition Luftlinie oder Straßenentfernung ist.</span><span class="sxs-lookup"><span data-stu-id="ed18e-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="ed18e-162">**Entfernungseinheiten**: Geben Sie die Einheit an, in der die Entfernung gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="ed18e-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="ed18e-163">**Entfernung von**: Geben Sie den Startpunkt der mehrstufigen Entfernung an.</span><span class="sxs-lookup"><span data-stu-id="ed18e-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="ed18e-164">**Entfernung bis**: Geben Sie den Zielpunkt der mehrstufigen Entfernung an.</span><span class="sxs-lookup"><span data-stu-id="ed18e-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="ed18e-165">**Berechnungstyp**: Geben Sie an, wie die Kosten für die einzelnen Lieferarten und die mehrstufige Entfernung berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="ed18e-166">Es werden zwei Berechnungsarten unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ed18e-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="ed18e-167">**Fest**: Für die Lieferart wird eine Pauschale verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed18e-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="ed18e-168">Bei Auswahl dieser Berechnungsart bestimmt das Feld **Kosten** die Kostenpauschale.</span><span class="sxs-lookup"><span data-stu-id="ed18e-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="ed18e-169">**Pro Entfernungseinheit**: Die Kosten für die Lieferart und die mehrstufige Entfernung werden berechnet, indem der im Feld **Kosten** angegebene Wert mit der Entfernung zwischen Lieferadresse und Standorten multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ed18e-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="ed18e-170">**Kosten**: Geben Sie den Wert an, der im Zusammenhang mit dem Feld **Berechnungstyp** verwendet wird, um die Kosten für eine Lieferart zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="ed18e-171">Bei Angaben mehrstufiger Entfernungen prüft das System, ob Entfernungen fehlen oder überlappen.</span><span class="sxs-lookup"><span data-stu-id="ed18e-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="ed18e-172">Der für eine Lieferart verwendete Entfernungstyp muss für alle mehrstufigen Entfernungen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="ed18e-173">Kostenkomponententyp „Sonstiges“</span><span class="sxs-lookup"><span data-stu-id="ed18e-173">Other cost component type</span></span>

<span data-ttu-id="ed18e-174">In diesem Abschnitt wird beschrieben, wie die einzelnen Kombinationen des Kostenkomponententyps **Sonstiges** und eines weiteren Kostentyps bei nicht versandbezogenen Kosten berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="ed18e-175">Ferner wird erläutert, wie der DOM-Solver die einzelnen Kombinationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed18e-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="ed18e-176">Kostenkomponententyp = Sonstiges und anderer Kostentyp = Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed18e-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="ed18e-177">Eine Kombination aus dem Kostenkomponententyp **Sonstiges** und dem anderen Kostentyp **Auftrag** wird verwendet, um auf Auftragsebene Kosten ohne Versandbezug zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ed18e-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="ed18e-178">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="ed18e-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ed18e-179">**Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ed18e-180">**Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ed18e-181">**Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</span><span class="sxs-lookup"><span data-stu-id="ed18e-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ed18e-182">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</span><span class="sxs-lookup"><span data-stu-id="ed18e-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ed18e-183">**Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ed18e-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ed18e-184">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ed18e-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ed18e-185">**Kosten**: Geben Sie den Wert für nichtversandbezogene Kosten auf Auftragsebene ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="ed18e-186">Kostenkomponententyp = Sonstiges und anderer Kostentyp = Auftragsposition</span><span class="sxs-lookup"><span data-stu-id="ed18e-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="ed18e-187">Eine Kombination aus dem Kostenkomponententyp **Sonstiges** und dem anderen Kostentyp **Auftragsposition** wird verwendet, um auf Auftragspositionsebene Kosten ohne Versandbezug zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ed18e-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="ed18e-188">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="ed18e-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ed18e-189">**Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ed18e-190">**Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ed18e-191">**Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</span><span class="sxs-lookup"><span data-stu-id="ed18e-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ed18e-192">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</span><span class="sxs-lookup"><span data-stu-id="ed18e-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ed18e-193">**Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ed18e-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ed18e-194">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ed18e-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ed18e-195">**Kosten**: Geben Sie den Wert für nichtversandbezogene Kosten auf Auftragspositionsebene ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="ed18e-196">Kostenkomponententyp = Sonstiges und anderer Kostentyp = Standort</span><span class="sxs-lookup"><span data-stu-id="ed18e-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="ed18e-197">Eine Kombination aus dem Kostenkomponententyp **Sonstiges** und dem anderen Kostentyp **Standort** wird verwendet, um für eine Gruppe von Standorten oder für einen einzelnen Standort nichtversandbezogene Kosten zu berechnet.</span><span class="sxs-lookup"><span data-stu-id="ed18e-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="ed18e-198">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="ed18e-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ed18e-199">**Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ed18e-200">**Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.</span><span class="sxs-lookup"><span data-stu-id="ed18e-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ed18e-201">**Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</span><span class="sxs-lookup"><span data-stu-id="ed18e-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ed18e-202">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</span><span class="sxs-lookup"><span data-stu-id="ed18e-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ed18e-203">**Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ed18e-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ed18e-204">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ed18e-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ed18e-205">**Erfüllungsgruppe**: Geben Sie die Gruppe der Standorte an, für die die Kosten ohne Versandbezug definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="ed18e-206">**Erfüllungslagerplatz**: Geben Sie den Ort an, für den die Kosten ohne Versandbezug definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ed18e-207">Bei standortbasierten Berechnungskriterien können keine Erfüllungsgruppe und kein Erfüllungslagerplatz angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="ed18e-208">**Kosten**: Geben Sie den Wert für die Kosten ohne Versandbezug auf Ebene der Erfüllungsgruppe oder auf Ebene des Erfüllungslagerplatzes an.</span><span class="sxs-lookup"><span data-stu-id="ed18e-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed18e-209">Damit diese Kosten bei der DOM berücksichtigt werden, muss der Kostenfaktor im jeweiligen Erfüllungsprofil ergänzt werden.</span><span class="sxs-lookup"><span data-stu-id="ed18e-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
