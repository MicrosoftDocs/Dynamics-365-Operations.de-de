---
title: Bestandsobjektwerte
description: Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e92c7889b11208c4d2b48eb279a104a7c226f904
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "319131"
---
# <a name="inventory-object-values"></a><span data-ttu-id="8ee65-103">Bestandsobjektwerte</span><span class="sxs-lookup"><span data-stu-id="8ee65-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ee65-104">Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="8ee65-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="8ee65-105">Eine Neuen Funktionen mit der Bezeichnung, **physische Menge** zeigt die Werte eines bestimmten Bestandsobjekts an.</span><span class="sxs-lookup"><span data-stu-id="8ee65-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="8ee65-106">Ein Kostenobjekt stellt die Entitätsebene dar, in der Bestandsbuchhaltung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ee65-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="8ee65-107">Weitere Informationen zu den Kostenobjekten finden Sie unter [Kostenobjekte](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="8ee65-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="8ee65-108">Damit die Werte eines bestimmten Bestandsobjekts anzuzeigen, klicken Sie **Physische Menge** auf der Seite **Kostenträger**.</span><span class="sxs-lookup"><span data-stu-id="8ee65-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="8ee65-109">Hier wird dargestellt, wie der Wert eines Bestandsobjekts berechnet wird:</span><span class="sxs-lookup"><span data-stu-id="8ee65-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="8ee65-110">Bestandsobjekt. Wert = Kostenträger. Durchschnittliche Einheitenkosten × Bestandsobjekt. Menge</span><span class="sxs-lookup"><span data-stu-id="8ee65-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="8ee65-111">Die folgenden Beispiele zeigen, wie die Werte eines Bestandsobjekts und des Kostenträgers berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="8ee65-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="8ee65-112">Zwei Produktzugangsereignisse werden auf Artikel A erfasst:</span><span class="sxs-lookup"><span data-stu-id="8ee65-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="8ee65-113">Produktzugang 1: Menge = 100 PCs, Betrag = 1.000,00 €, Standort = 1, Lagerort =11, Chargennummer</span><span class="sxs-lookup"><span data-stu-id="8ee65-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="8ee65-114">= B1</span><span class="sxs-lookup"><span data-stu-id="8ee65-114">= B1</span></span>
-   <span data-ttu-id="8ee65-115">Produktzugang 2: Menge = 50 PCs, Betrag = 800,00 €, Standort = 1, Lagerort =11, Chargennummer</span><span class="sxs-lookup"><span data-stu-id="8ee65-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="8ee65-116">= B2</span><span class="sxs-lookup"><span data-stu-id="8ee65-116">= B2</span></span>

<span data-ttu-id="8ee65-117">In der folgenden Tabelle wird das Berechnungsergebnis für einen Kostenträger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8ee65-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="8ee65-118">Das Ergebnis sehen Sie auf der Seite **Kostenobjekt**.</span><span class="sxs-lookup"><span data-stu-id="8ee65-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ee65-119">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="8ee65-119">Object type</span></span></th>
<th><span data-ttu-id="8ee65-120">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="8ee65-120">Item number</span></span></th>
<th><span data-ttu-id="8ee65-121">Standort</span><span class="sxs-lookup"><span data-stu-id="8ee65-121">Site</span></span></th>
<th><span data-ttu-id="8ee65-122">Menge</span><span class="sxs-lookup"><span data-stu-id="8ee65-122">Quantity</span></span></th>
<th><span data-ttu-id="8ee65-123">Lagereinheit</span><span class="sxs-lookup"><span data-stu-id="8ee65-123">Inventory unit</span></span></th>
<th><span data-ttu-id="8ee65-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee65-124">Value</span></span></th>
<th><span data-ttu-id="8ee65-125">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="8ee65-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ee65-126">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="8ee65-126">Cost object</span></span></td>
<td><span data-ttu-id="8ee65-127">A:</span><span class="sxs-lookup"><span data-stu-id="8ee65-127">A</span></span></td>
<td><span data-ttu-id="8ee65-128">1</span><span class="sxs-lookup"><span data-stu-id="8ee65-128">1</span></span></td>
<td><span data-ttu-id="8ee65-129">150</span><span class="sxs-lookup"><span data-stu-id="8ee65-129">150</span></span></td>
<td><span data-ttu-id="8ee65-130">Stck.</span><span class="sxs-lookup"><span data-stu-id="8ee65-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="8ee65-131">1800,00 €</span><span class="sxs-lookup"><span data-stu-id="8ee65-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="8ee65-132">12,00 €</span><span class="sxs-lookup"><span data-stu-id="8ee65-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ee65-133">In der folgenden Tabelle wird das Berechnungsergebnis für ein Bestandsobjekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8ee65-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="8ee65-134">Das Ergebnis sehen Sie, wenn Sie auf der Seite **Physische Menge** auf der Seite **Kostenobjekt** klicken.</span><span class="sxs-lookup"><span data-stu-id="8ee65-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ee65-135">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="8ee65-135">Object type</span></span></th>
<th><span data-ttu-id="8ee65-136">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="8ee65-136">Item number</span></span></th>
<th><span data-ttu-id="8ee65-137">Standort</span><span class="sxs-lookup"><span data-stu-id="8ee65-137">Site</span></span></th>
<th><span data-ttu-id="8ee65-138">Lagerort</span><span class="sxs-lookup"><span data-stu-id="8ee65-138">Warehouse</span></span></th>
<th><span data-ttu-id="8ee65-139">Chargennummer</span><span class="sxs-lookup"><span data-stu-id="8ee65-139">Batch No.</span></span></th>
<th><span data-ttu-id="8ee65-140">Menge</span><span class="sxs-lookup"><span data-stu-id="8ee65-140">Quantity</span></span></th>
<th><span data-ttu-id="8ee65-141">Lagereinheit</span><span class="sxs-lookup"><span data-stu-id="8ee65-141">Inventory unit</span></span></th>
<th><span data-ttu-id="8ee65-142">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee65-142">Value</span></span></th>
<th><span data-ttu-id="8ee65-143">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="8ee65-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ee65-144">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="8ee65-144">Inventory object</span></span></td>
<td><span data-ttu-id="8ee65-145">A:</span><span class="sxs-lookup"><span data-stu-id="8ee65-145">A</span></span></td>
<td><span data-ttu-id="8ee65-146">1</span><span class="sxs-lookup"><span data-stu-id="8ee65-146">1</span></span></td>
<td><span data-ttu-id="8ee65-147">11</span><span class="sxs-lookup"><span data-stu-id="8ee65-147">11</span></span></td>
<td><span data-ttu-id="8ee65-148">B1</span><span class="sxs-lookup"><span data-stu-id="8ee65-148">B1</span></span></td>
<td><span data-ttu-id="8ee65-149">100</span><span class="sxs-lookup"><span data-stu-id="8ee65-149">100</span></span></td>
<td><span data-ttu-id="8ee65-150">Stck.</span><span class="sxs-lookup"><span data-stu-id="8ee65-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="8ee65-151">1200,00 €</span><span class="sxs-lookup"><span data-stu-id="8ee65-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="8ee65-152">12,00 €</span><span class="sxs-lookup"><span data-stu-id="8ee65-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee65-153">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="8ee65-153">Inventory object</span></span></td>
<td><span data-ttu-id="8ee65-154">H</span><span class="sxs-lookup"><span data-stu-id="8ee65-154">A</span></span></td>
<td><span data-ttu-id="8ee65-155">1</span><span class="sxs-lookup"><span data-stu-id="8ee65-155">1</span></span></td>
<td><span data-ttu-id="8ee65-156">11</span><span class="sxs-lookup"><span data-stu-id="8ee65-156">11</span></span></td>
<td><span data-ttu-id="8ee65-157">B2</span><span class="sxs-lookup"><span data-stu-id="8ee65-157">B2</span></span></td>
<td><span data-ttu-id="8ee65-158">50</span><span class="sxs-lookup"><span data-stu-id="8ee65-158">50</span></span></td>
<td><span data-ttu-id="8ee65-159">Stck.</span><span class="sxs-lookup"><span data-stu-id="8ee65-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="8ee65-160">600,00 €</span><span class="sxs-lookup"><span data-stu-id="8ee65-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="8ee65-161">12,00 €</span><span class="sxs-lookup"><span data-stu-id="8ee65-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="8ee65-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8ee65-162">Additional resources</span></span>
--------

[<span data-ttu-id="8ee65-163">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="8ee65-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="8ee65-164">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="8ee65-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="8ee65-165">Neuheiten und Änderungen</span><span class="sxs-lookup"><span data-stu-id="8ee65-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



