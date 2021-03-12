---
title: Bestandsobjektwerte
description: Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 914c7e8c757664ec791b46924600b74c9c979e8f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967432"
---
# <a name="inventory-object-values"></a><span data-ttu-id="9ece1-103">Bestandsobjektwerte</span><span class="sxs-lookup"><span data-stu-id="9ece1-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ece1-104">Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="9ece1-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="9ece1-105">Eine Neuen Funktionen mit der Bezeichnung, **physische Menge** zeigt die Werte eines bestimmten Bestandsobjekts an.</span><span class="sxs-lookup"><span data-stu-id="9ece1-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="9ece1-106">Ein Kostenobjekt stellt die Entitätsebene dar, in der Bestandsbuchhaltung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ece1-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="9ece1-107">Weitere Informationen zu den Kostenobjekten finden Sie unter [Kostenobjekte](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="9ece1-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="9ece1-108">Damit die Werte eines bestimmten Bestandsobjekts anzuzeigen, klicken Sie **Physische Menge** auf der Seite **Kostenträger**.</span><span class="sxs-lookup"><span data-stu-id="9ece1-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="9ece1-109">Hier wird dargestellt, wie der Wert eines Bestandsobjekts berechnet wird:</span><span class="sxs-lookup"><span data-stu-id="9ece1-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="9ece1-110">Bestandsobjekt. Wert = Kostenträger. Durchschnittliche Einheitenkosten × Bestandsobjekt. Menge</span><span class="sxs-lookup"><span data-stu-id="9ece1-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="9ece1-111">Die folgenden Beispiele zeigen, wie die Werte eines Bestandsobjekts und des Kostenträgers berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="9ece1-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="9ece1-112">Zwei Produktzugangsereignisse werden auf Artikel A erfasst:</span><span class="sxs-lookup"><span data-stu-id="9ece1-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="9ece1-113">Produktzugang 1: Menge = 100 PCs, Betrag = 1.000,00 €, Standort = 1, Lagerort =11, Chargennummer</span><span class="sxs-lookup"><span data-stu-id="9ece1-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="9ece1-114">= B1</span><span class="sxs-lookup"><span data-stu-id="9ece1-114">= B1</span></span>
-   <span data-ttu-id="9ece1-115">Produktzugang 2: Menge = 50 PCs, Betrag = 800,00 €, Standort = 1, Lagerort =11, Chargennummer</span><span class="sxs-lookup"><span data-stu-id="9ece1-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="9ece1-116">= B2</span><span class="sxs-lookup"><span data-stu-id="9ece1-116">= B2</span></span>

<span data-ttu-id="9ece1-117">In der folgenden Tabelle wird das Berechnungsergebnis für einen Kostenträger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ece1-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="9ece1-118">Das Ergebnis sehen Sie auf der Seite **Kostenobjekt**.</span><span class="sxs-lookup"><span data-stu-id="9ece1-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="9ece1-119">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="9ece1-119">Object type</span></span></th>
<th><span data-ttu-id="9ece1-120">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="9ece1-120">Item number</span></span></th>
<th><span data-ttu-id="9ece1-121">Standort</span><span class="sxs-lookup"><span data-stu-id="9ece1-121">Site</span></span></th>
<th><span data-ttu-id="9ece1-122">Menge</span><span class="sxs-lookup"><span data-stu-id="9ece1-122">Quantity</span></span></th>
<th><span data-ttu-id="9ece1-123">Lagereinheit</span><span class="sxs-lookup"><span data-stu-id="9ece1-123">Inventory unit</span></span></th>
<th><span data-ttu-id="9ece1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9ece1-124">Value</span></span></th>
<th><span data-ttu-id="9ece1-125">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="9ece1-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ece1-126">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="9ece1-126">Cost object</span></span></td>
<td><span data-ttu-id="9ece1-127">A:</span><span class="sxs-lookup"><span data-stu-id="9ece1-127">A</span></span></td>
<td><span data-ttu-id="9ece1-128">1</span><span class="sxs-lookup"><span data-stu-id="9ece1-128">1</span></span></td>
<td><span data-ttu-id="9ece1-129">150</span><span class="sxs-lookup"><span data-stu-id="9ece1-129">150</span></span></td>
<td><span data-ttu-id="9ece1-130">Stck.</span><span class="sxs-lookup"><span data-stu-id="9ece1-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="9ece1-131">1800,00 €</span><span class="sxs-lookup"><span data-stu-id="9ece1-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="9ece1-132">12,00 €</span><span class="sxs-lookup"><span data-stu-id="9ece1-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9ece1-133">In der folgenden Tabelle wird das Berechnungsergebnis für ein Bestandsobjekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ece1-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="9ece1-134">Das Ergebnis sehen Sie, wenn Sie auf der Seite **Physische Menge** auf der Seite **Kostenobjekt** klicken.</span><span class="sxs-lookup"><span data-stu-id="9ece1-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="9ece1-135">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="9ece1-135">Object type</span></span></th>
<th><span data-ttu-id="9ece1-136">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="9ece1-136">Item number</span></span></th>
<th><span data-ttu-id="9ece1-137">Standort</span><span class="sxs-lookup"><span data-stu-id="9ece1-137">Site</span></span></th>
<th><span data-ttu-id="9ece1-138">Lagerort</span><span class="sxs-lookup"><span data-stu-id="9ece1-138">Warehouse</span></span></th>
<th><span data-ttu-id="9ece1-139">Chargennummer</span><span class="sxs-lookup"><span data-stu-id="9ece1-139">Batch No.</span></span></th>
<th><span data-ttu-id="9ece1-140">Menge</span><span class="sxs-lookup"><span data-stu-id="9ece1-140">Quantity</span></span></th>
<th><span data-ttu-id="9ece1-141">Lagereinheit</span><span class="sxs-lookup"><span data-stu-id="9ece1-141">Inventory unit</span></span></th>
<th><span data-ttu-id="9ece1-142">Wert</span><span class="sxs-lookup"><span data-stu-id="9ece1-142">Value</span></span></th>
<th><span data-ttu-id="9ece1-143">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="9ece1-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ece1-144">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="9ece1-144">Inventory object</span></span></td>
<td><span data-ttu-id="9ece1-145">A:</span><span class="sxs-lookup"><span data-stu-id="9ece1-145">A</span></span></td>
<td><span data-ttu-id="9ece1-146">1</span><span class="sxs-lookup"><span data-stu-id="9ece1-146">1</span></span></td>
<td><span data-ttu-id="9ece1-147">11</span><span class="sxs-lookup"><span data-stu-id="9ece1-147">11</span></span></td>
<td><span data-ttu-id="9ece1-148">B1</span><span class="sxs-lookup"><span data-stu-id="9ece1-148">B1</span></span></td>
<td><span data-ttu-id="9ece1-149">100</span><span class="sxs-lookup"><span data-stu-id="9ece1-149">100</span></span></td>
<td><span data-ttu-id="9ece1-150">Stck.</span><span class="sxs-lookup"><span data-stu-id="9ece1-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="9ece1-151">1200,00 €</span><span class="sxs-lookup"><span data-stu-id="9ece1-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="9ece1-152">12,00 €</span><span class="sxs-lookup"><span data-stu-id="9ece1-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ece1-153">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="9ece1-153">Inventory object</span></span></td>
<td><span data-ttu-id="9ece1-154">H</span><span class="sxs-lookup"><span data-stu-id="9ece1-154">A</span></span></td>
<td><span data-ttu-id="9ece1-155">1</span><span class="sxs-lookup"><span data-stu-id="9ece1-155">1</span></span></td>
<td><span data-ttu-id="9ece1-156">11</span><span class="sxs-lookup"><span data-stu-id="9ece1-156">11</span></span></td>
<td><span data-ttu-id="9ece1-157">B2</span><span class="sxs-lookup"><span data-stu-id="9ece1-157">B2</span></span></td>
<td><span data-ttu-id="9ece1-158">50</span><span class="sxs-lookup"><span data-stu-id="9ece1-158">50</span></span></td>
<td><span data-ttu-id="9ece1-159">Stck.</span><span class="sxs-lookup"><span data-stu-id="9ece1-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="9ece1-160">600,00 €</span><span class="sxs-lookup"><span data-stu-id="9ece1-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="9ece1-161">12,00 €</span><span class="sxs-lookup"><span data-stu-id="9ece1-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="9ece1-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9ece1-162">Additional resources</span></span>
--------

[<span data-ttu-id="9ece1-163">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="9ece1-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="9ece1-164">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="9ece1-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="9ece1-165">Neuheiten und Änderungen</span><span class="sxs-lookup"><span data-stu-id="9ece1-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



