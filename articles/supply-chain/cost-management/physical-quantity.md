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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547858"
---
# <a name="inventory-object-values"></a><span data-ttu-id="7f19d-103">Bestandsobjektwerte</span><span class="sxs-lookup"><span data-stu-id="7f19d-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f19d-104">Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="7f19d-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="7f19d-105">Eine Neuen Funktionen mit der Bezeichnung, **physische Menge** zeigt die Werte eines bestimmten Bestandsobjekts an.</span><span class="sxs-lookup"><span data-stu-id="7f19d-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="7f19d-106">Ein Kostenobjekt stellt die Entitätsebene dar, in der Bestandsbuchhaltung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f19d-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="7f19d-107">Weitere Informationen zu den Kostenobjekten finden Sie unter [Kostenobjekte](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="7f19d-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="7f19d-108">Damit die Werte eines bestimmten Bestandsobjekts anzuzeigen, klicken Sie **Physische Menge** auf der Seite **Kostenträger**.</span><span class="sxs-lookup"><span data-stu-id="7f19d-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="7f19d-109">Hier wird dargestellt, wie der Wert eines Bestandsobjekts berechnet wird:</span><span class="sxs-lookup"><span data-stu-id="7f19d-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="7f19d-110">Bestandsobjekt. Wert = Kostenträger. Durchschnittliche Einheitenkosten × Bestandsobjekt. Menge</span><span class="sxs-lookup"><span data-stu-id="7f19d-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="7f19d-111">Die folgenden Beispiele zeigen, wie die Werte eines Bestandsobjekts und des Kostenträgers berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="7f19d-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="7f19d-112">Zwei Produktzugangsereignisse werden auf Artikel A erfasst:</span><span class="sxs-lookup"><span data-stu-id="7f19d-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="7f19d-113">Produktzugang 1: Menge = 100 PCs, Betrag = 1.000,00 €, Standort = 1, Lagerort =11, Chargennummer</span><span class="sxs-lookup"><span data-stu-id="7f19d-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="7f19d-114">= B1</span><span class="sxs-lookup"><span data-stu-id="7f19d-114">= B1</span></span>
-   <span data-ttu-id="7f19d-115">Produktzugang 2: Menge = 50 PCs, Betrag = 800,00 €, Standort = 1, Lagerort =11, Chargennummer</span><span class="sxs-lookup"><span data-stu-id="7f19d-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="7f19d-116">= B2</span><span class="sxs-lookup"><span data-stu-id="7f19d-116">= B2</span></span>

<span data-ttu-id="7f19d-117">In der folgenden Tabelle wird das Berechnungsergebnis für einen Kostenträger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f19d-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="7f19d-118">Das Ergebnis sehen Sie auf der Seite **Kostenobjekt**.</span><span class="sxs-lookup"><span data-stu-id="7f19d-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="7f19d-119">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="7f19d-119">Object type</span></span></th>
<th><span data-ttu-id="7f19d-120">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="7f19d-120">Item number</span></span></th>
<th><span data-ttu-id="7f19d-121">Standort</span><span class="sxs-lookup"><span data-stu-id="7f19d-121">Site</span></span></th>
<th><span data-ttu-id="7f19d-122">Menge</span><span class="sxs-lookup"><span data-stu-id="7f19d-122">Quantity</span></span></th>
<th><span data-ttu-id="7f19d-123">Lagereinheit</span><span class="sxs-lookup"><span data-stu-id="7f19d-123">Inventory unit</span></span></th>
<th><span data-ttu-id="7f19d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7f19d-124">Value</span></span></th>
<th><span data-ttu-id="7f19d-125">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="7f19d-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f19d-126">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="7f19d-126">Cost object</span></span></td>
<td><span data-ttu-id="7f19d-127">A:</span><span class="sxs-lookup"><span data-stu-id="7f19d-127">A</span></span></td>
<td><span data-ttu-id="7f19d-128">1</span><span class="sxs-lookup"><span data-stu-id="7f19d-128">1</span></span></td>
<td><span data-ttu-id="7f19d-129">150</span><span class="sxs-lookup"><span data-stu-id="7f19d-129">150</span></span></td>
<td><span data-ttu-id="7f19d-130">Stck.</span><span class="sxs-lookup"><span data-stu-id="7f19d-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="7f19d-131">1800,00 €</span><span class="sxs-lookup"><span data-stu-id="7f19d-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="7f19d-132">12,00 €</span><span class="sxs-lookup"><span data-stu-id="7f19d-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7f19d-133">In der folgenden Tabelle wird das Berechnungsergebnis für ein Bestandsobjekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f19d-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="7f19d-134">Das Ergebnis sehen Sie, wenn Sie auf der Seite **Physische Menge** auf der Seite **Kostenobjekt** klicken.</span><span class="sxs-lookup"><span data-stu-id="7f19d-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="7f19d-135">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="7f19d-135">Object type</span></span></th>
<th><span data-ttu-id="7f19d-136">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="7f19d-136">Item number</span></span></th>
<th><span data-ttu-id="7f19d-137">Standort</span><span class="sxs-lookup"><span data-stu-id="7f19d-137">Site</span></span></th>
<th><span data-ttu-id="7f19d-138">Lagerort</span><span class="sxs-lookup"><span data-stu-id="7f19d-138">Warehouse</span></span></th>
<th><span data-ttu-id="7f19d-139">Chargennummer</span><span class="sxs-lookup"><span data-stu-id="7f19d-139">Batch No.</span></span></th>
<th><span data-ttu-id="7f19d-140">Menge</span><span class="sxs-lookup"><span data-stu-id="7f19d-140">Quantity</span></span></th>
<th><span data-ttu-id="7f19d-141">Lagereinheit</span><span class="sxs-lookup"><span data-stu-id="7f19d-141">Inventory unit</span></span></th>
<th><span data-ttu-id="7f19d-142">Wert</span><span class="sxs-lookup"><span data-stu-id="7f19d-142">Value</span></span></th>
<th><span data-ttu-id="7f19d-143">Durchschnittliche Einheitenkosten</span><span class="sxs-lookup"><span data-stu-id="7f19d-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f19d-144">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="7f19d-144">Inventory object</span></span></td>
<td><span data-ttu-id="7f19d-145">A:</span><span class="sxs-lookup"><span data-stu-id="7f19d-145">A</span></span></td>
<td><span data-ttu-id="7f19d-146">1</span><span class="sxs-lookup"><span data-stu-id="7f19d-146">1</span></span></td>
<td><span data-ttu-id="7f19d-147">11</span><span class="sxs-lookup"><span data-stu-id="7f19d-147">11</span></span></td>
<td><span data-ttu-id="7f19d-148">B1</span><span class="sxs-lookup"><span data-stu-id="7f19d-148">B1</span></span></td>
<td><span data-ttu-id="7f19d-149">100</span><span class="sxs-lookup"><span data-stu-id="7f19d-149">100</span></span></td>
<td><span data-ttu-id="7f19d-150">Stck.</span><span class="sxs-lookup"><span data-stu-id="7f19d-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="7f19d-151">1200,00 €</span><span class="sxs-lookup"><span data-stu-id="7f19d-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="7f19d-152">12,00 €</span><span class="sxs-lookup"><span data-stu-id="7f19d-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f19d-153">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="7f19d-153">Inventory object</span></span></td>
<td><span data-ttu-id="7f19d-154">H</span><span class="sxs-lookup"><span data-stu-id="7f19d-154">A</span></span></td>
<td><span data-ttu-id="7f19d-155">1</span><span class="sxs-lookup"><span data-stu-id="7f19d-155">1</span></span></td>
<td><span data-ttu-id="7f19d-156">11</span><span class="sxs-lookup"><span data-stu-id="7f19d-156">11</span></span></td>
<td><span data-ttu-id="7f19d-157">B2</span><span class="sxs-lookup"><span data-stu-id="7f19d-157">B2</span></span></td>
<td><span data-ttu-id="7f19d-158">50</span><span class="sxs-lookup"><span data-stu-id="7f19d-158">50</span></span></td>
<td><span data-ttu-id="7f19d-159">Stck.</span><span class="sxs-lookup"><span data-stu-id="7f19d-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="7f19d-160">600,00 €</span><span class="sxs-lookup"><span data-stu-id="7f19d-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="7f19d-161">12,00 €</span><span class="sxs-lookup"><span data-stu-id="7f19d-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="7f19d-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f19d-162">Additional resources</span></span>
--------

[<span data-ttu-id="7f19d-163">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="7f19d-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="7f19d-164">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="7f19d-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="7f19d-165">Neuheiten und Änderungen</span><span class="sxs-lookup"><span data-stu-id="7f19d-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



