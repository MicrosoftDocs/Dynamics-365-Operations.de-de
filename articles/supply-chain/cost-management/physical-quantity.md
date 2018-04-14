---
title: Bestandsobjektwerte
description: "Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f30227d90be5f957c4e23a08069c6dba9b07bb35
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="inventory-object-values"></a><span data-ttu-id="a8690-103">Bestandsobjektwerte</span><span class="sxs-lookup"><span data-stu-id="a8690-103">Inventory object values</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="a8690-104">Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="a8690-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="a8690-105">Eine Neuen Funktionen mit der Bezeichnung, **physische Menge** zeigt die Werte eines bestimmten Bestandsobjekts an.</span><span class="sxs-lookup"><span data-stu-id="a8690-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="a8690-106">Ein Kostenobjekt stellt die Entitätsebene dar, in der Bestandsbuchhaltung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8690-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="a8690-107">Weitere Informationen zu den Kostenobjekten finden Sie unter [Kostenobjekte](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="a8690-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="a8690-108">Damit die Werte eines bestimmten Bestandsobjekts anzuzeigen, klicken Sie **Physische Menge** auf der Seite **Kostenträger**.</span><span class="sxs-lookup"><span data-stu-id="a8690-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="a8690-109">Hier wird dargestellt, wie der Wert eines Bestandsobjekts berechnet wird:</span><span class="sxs-lookup"><span data-stu-id="a8690-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="a8690-110">Bestandsobjekt. Wert = Kostenträger. Durchschnittliche Einheitenkosten × Bestandsobjekt. Menge</span><span class="sxs-lookup"><span data-stu-id="a8690-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="a8690-111">Die folgenden Beispiele zeigen, wie die Werte eines Bestandsobjekts und des Kostenträgers berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="a8690-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="a8690-112">Zwei Produktzugangsereignisse werden auf Artikel A erfasst:</span><span class="sxs-lookup"><span data-stu-id="a8690-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="a8690-113">Produktzugang 1: Menge = 100 PCs, Betrag = 1.000,00 €, Standort = 1, Lagerort =11, Chargennummer</span><span class="sxs-lookup"><span data-stu-id="a8690-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="a8690-114">= B1</span><span class="sxs-lookup"><span data-stu-id="a8690-114">= B1</span></span>
-   <span data-ttu-id="a8690-115">Produktzugang 2: Menge = 50 PCs, Betrag = 800,00 €, Standort = 1, Lagerort =11, Chargennummer</span><span class="sxs-lookup"><span data-stu-id="a8690-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="a8690-116">= B2</span><span class="sxs-lookup"><span data-stu-id="a8690-116">= B2</span></span>

<span data-ttu-id="a8690-117">In der folgenden Tabelle wird das Berechnungsergebnis für einen Kostenträger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8690-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="a8690-118">Das Ergebnis sehen Sie auf der Seite **Kostenobjekt**.</span><span class="sxs-lookup"><span data-stu-id="a8690-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="a8690-119">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="a8690-119">Object type</span></span></th>
<th><span data-ttu-id="a8690-120">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="a8690-120">Item number</span></span></th>
<th><span data-ttu-id="a8690-121">Standort</span><span class="sxs-lookup"><span data-stu-id="a8690-121">Site</span></span></th>
<th><span data-ttu-id="a8690-122">Menge</span><span class="sxs-lookup"><span data-stu-id="a8690-122">Quantity</span></span></th>
<th><span data-ttu-id="a8690-123">Lagereinheit</span><span class="sxs-lookup"><span data-stu-id="a8690-123">Inventory unit</span></span></th>
<th><span data-ttu-id="a8690-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a8690-124">Value</span></span></th>
<th><span data-ttu-id="a8690-125">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="a8690-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8690-126">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="a8690-126">Cost object</span></span></td>
<td><span data-ttu-id="a8690-127">A:</span><span class="sxs-lookup"><span data-stu-id="a8690-127">A</span></span></td>
<td><span data-ttu-id="a8690-128">1</span><span class="sxs-lookup"><span data-stu-id="a8690-128">1</span></span></td>
<td><span data-ttu-id="a8690-129">150</span><span class="sxs-lookup"><span data-stu-id="a8690-129">150</span></span></td>
<td><span data-ttu-id="a8690-130">Stck.</span><span class="sxs-lookup"><span data-stu-id="a8690-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="a8690-131">1800,00 €</span><span class="sxs-lookup"><span data-stu-id="a8690-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="a8690-132">12,00 €</span><span class="sxs-lookup"><span data-stu-id="a8690-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8690-133">In der folgenden Tabelle wird das Berechnungsergebnis für ein Bestandsobjekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8690-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="a8690-134">Das Ergebnis sehen Sie, wenn Sie auf der Seite **Physische Menge** auf der Seite **Kostenobjekt** klicken.</span><span class="sxs-lookup"><span data-stu-id="a8690-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="a8690-135">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="a8690-135">Object type</span></span></th>
<th><span data-ttu-id="a8690-136">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="a8690-136">Item number</span></span></th>
<th><span data-ttu-id="a8690-137">Standort</span><span class="sxs-lookup"><span data-stu-id="a8690-137">Site</span></span></th>
<th><span data-ttu-id="a8690-138">Lagerort</span><span class="sxs-lookup"><span data-stu-id="a8690-138">Warehouse</span></span></th>
<th><span data-ttu-id="a8690-139">Chargennummer</span><span class="sxs-lookup"><span data-stu-id="a8690-139">Batch No.</span></span></th>
<th><span data-ttu-id="a8690-140">Menge</span><span class="sxs-lookup"><span data-stu-id="a8690-140">Quantity</span></span></th>
<th><span data-ttu-id="a8690-141">Lagereinheit</span><span class="sxs-lookup"><span data-stu-id="a8690-141">Inventory unit</span></span></th>
<th><span data-ttu-id="a8690-142">Wert</span><span class="sxs-lookup"><span data-stu-id="a8690-142">Value</span></span></th>
<th><span data-ttu-id="a8690-143">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="a8690-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8690-144">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="a8690-144">Inventory object</span></span></td>
<td><span data-ttu-id="a8690-145">A:</span><span class="sxs-lookup"><span data-stu-id="a8690-145">A</span></span></td>
<td><span data-ttu-id="a8690-146">1</span><span class="sxs-lookup"><span data-stu-id="a8690-146">1</span></span></td>
<td><span data-ttu-id="a8690-147">11</span><span class="sxs-lookup"><span data-stu-id="a8690-147">11</span></span></td>
<td><span data-ttu-id="a8690-148">B1</span><span class="sxs-lookup"><span data-stu-id="a8690-148">B1</span></span></td>
<td><span data-ttu-id="a8690-149">100</span><span class="sxs-lookup"><span data-stu-id="a8690-149">100</span></span></td>
<td><span data-ttu-id="a8690-150">Stck.</span><span class="sxs-lookup"><span data-stu-id="a8690-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="a8690-151">1200,00 €</span><span class="sxs-lookup"><span data-stu-id="a8690-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="a8690-152">12,00 €</span><span class="sxs-lookup"><span data-stu-id="a8690-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8690-153">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="a8690-153">Inventory object</span></span></td>
<td><span data-ttu-id="a8690-154">A:</span><span class="sxs-lookup"><span data-stu-id="a8690-154">A</span></span></td>
<td><span data-ttu-id="a8690-155">1</span><span class="sxs-lookup"><span data-stu-id="a8690-155">1</span></span></td>
<td><span data-ttu-id="a8690-156">11</span><span class="sxs-lookup"><span data-stu-id="a8690-156">11</span></span></td>
<td><span data-ttu-id="a8690-157">B2</span><span class="sxs-lookup"><span data-stu-id="a8690-157">B2</span></span></td>
<td><span data-ttu-id="a8690-158">50</span><span class="sxs-lookup"><span data-stu-id="a8690-158">50</span></span></td>
<td><span data-ttu-id="a8690-159">Stck.</span><span class="sxs-lookup"><span data-stu-id="a8690-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="a8690-160">600,00 €</span><span class="sxs-lookup"><span data-stu-id="a8690-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="a8690-161">12,00 €</span><span class="sxs-lookup"><span data-stu-id="a8690-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="a8690-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8690-162">See also</span></span>
--------

[<span data-ttu-id="a8690-163">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="a8690-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="a8690-164">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="a8690-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="a8690-165">Neuheiten und Änderungen</span><span class="sxs-lookup"><span data-stu-id="a8690-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)




