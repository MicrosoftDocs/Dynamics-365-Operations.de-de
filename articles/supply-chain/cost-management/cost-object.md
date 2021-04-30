---
title: Kostenobjekte
description: Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden. Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden. Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6829f24b8efa29b39f5ed742d8ca99e09bcef01
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910352"
---
# <a name="cost-objects"></a><span data-ttu-id="ae5e3-105">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="ae5e3-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae5e3-106">Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="ae5e3-107">Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="ae5e3-108">Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="ae5e3-109">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="ae5e3-109">Cost objects</span></span>

<span data-ttu-id="ae5e3-110">Auf der Seite **Kostenobjekte** werden alle Kostenobjekte aufgeführt, die für ein Produkt erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="ae5e3-111">Die Kostenobjekte werden durch Daten aus den folgenden Ressourcen definiert:</span><span class="sxs-lookup"><span data-stu-id="ae5e3-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="ae5e3-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="ae5e3-112">Product</span></span>
-   <span data-ttu-id="ae5e3-113">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="ae5e3-113">Product dimension group</span></span>
-   <span data-ttu-id="ae5e3-114">Lagerdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="ae5e3-114">Storage dimension group</span></span>
-   <span data-ttu-id="ae5e3-115">Rückverfolgungsgruppe</span><span class="sxs-lookup"><span data-stu-id="ae5e3-115">Tracking dimension group</span></span>

<span data-ttu-id="ae5e3-116">**Hinweis:** Ein Kostenobjekte stellt nur ein Kostenelement des Typs **Direktmaterial** dar.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="ae5e3-117">Ein Kostenobjekte und ein Bestandsobjekt unterscheiden sich dadurch, dass ein Kostenträger durch die Lagerungsdimensionen definiert wird, die für den wertmäßigen Bestand ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="ae5e3-118">Ein Artikel hat zum Beispiel die folgende Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="ae5e3-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="ae5e3-119">**Standort:** Physischer Bestand = Ja, wertmäßiger Bestand = Ja</span><span class="sxs-lookup"><span data-stu-id="ae5e3-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="ae5e3-120">**Lagerort:** Physischer Bestand = Ja, wertmäßiger Bestand = Nein</span><span class="sxs-lookup"><span data-stu-id="ae5e3-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="ae5e3-121">**Chargennummer:** Physischer Bestand = Ja, wertmäßiger Bestand = Nein</span><span class="sxs-lookup"><span data-stu-id="ae5e3-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="ae5e3-122">In der folgenden Tabelle zeigt, was ein Kostenobjekte ist und was ein Bestandsobjekt ist.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="ae5e3-123">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="ae5e3-123">Object type</span></span>      | <span data-ttu-id="ae5e3-124">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="ae5e3-124">Item number</span></span> | <span data-ttu-id="ae5e3-125">Standort</span><span class="sxs-lookup"><span data-stu-id="ae5e3-125">Site</span></span> | <span data-ttu-id="ae5e3-126">Lagerort</span><span class="sxs-lookup"><span data-stu-id="ae5e3-126">Warehouse</span></span> | <span data-ttu-id="ae5e3-127">Chargennummer</span><span class="sxs-lookup"><span data-stu-id="ae5e3-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="ae5e3-128">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="ae5e3-128">Cost object</span></span>      | <span data-ttu-id="ae5e3-129"> -</span><span class="sxs-lookup"><span data-stu-id="ae5e3-129">x</span></span>           | <span data-ttu-id="ae5e3-130"> -</span><span class="sxs-lookup"><span data-stu-id="ae5e3-130">x</span></span>    |           |           |
| <span data-ttu-id="ae5e3-131">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="ae5e3-131">Inventory object</span></span> | <span data-ttu-id="ae5e3-132"> -</span><span class="sxs-lookup"><span data-stu-id="ae5e3-132">x</span></span>           | <span data-ttu-id="ae5e3-133"> -</span><span class="sxs-lookup"><span data-stu-id="ae5e3-133">x</span></span>    |  <span data-ttu-id="ae5e3-134"> -</span><span class="sxs-lookup"><span data-stu-id="ae5e3-134">x</span></span>        | <span data-ttu-id="ae5e3-135"> -</span><span class="sxs-lookup"><span data-stu-id="ae5e3-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="ae5e3-136">Ansammlung von Kosten und Mengen</span><span class="sxs-lookup"><span data-stu-id="ae5e3-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="ae5e3-137">Der Wert im Feld **Wert** ist eine Summe der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="ae5e3-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="ae5e3-138">Phys. Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="ae5e3-138">Physical cost amount</span></span>
    -   <span data-ttu-id="ae5e3-139">Wertmäßiger Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="ae5e3-139">Financial cost amount</span></span>
    -   <span data-ttu-id="ae5e3-140">Regulierungen</span><span class="sxs-lookup"><span data-stu-id="ae5e3-140">Adjustments</span></span>
-   <span data-ttu-id="ae5e3-141">Der Wert im Feld **Menge** ist eine Summe der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="ae5e3-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="ae5e3-142">Empfangen</span><span class="sxs-lookup"><span data-stu-id="ae5e3-142">Received</span></span>
    -   <span data-ttu-id="ae5e3-143">Abgesetzt</span><span class="sxs-lookup"><span data-stu-id="ae5e3-143">Deducted</span></span>
    -   <span data-ttu-id="ae5e3-144">Gebuchte Menge</span><span class="sxs-lookup"><span data-stu-id="ae5e3-144">Posted quantity</span></span>
-   <span data-ttu-id="ae5e3-145">Das Feld **Durchschnittlichen Einheitenkosten** ist ein berechnetes Feld.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="ae5e3-146">Der Wert wird berechnet, indem der Wert **Wert** durch den Wert **Menge** geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="ae5e3-147">**Hinweis:** Der Parameter **Physischen Wert einbeziehen** hat keinen Einfluss auf die vorhergehenden Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="ae5e3-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ae5e3-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ae5e3-148">Additional resources</span></span>
--------

[<span data-ttu-id="ae5e3-149">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="ae5e3-149">Product dimension group</span></span>](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[<span data-ttu-id="ae5e3-150">Lagerdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="ae5e3-150">Storage dimension group</span></span>](/dynamicsax-2012//storage-dimension-groups-form)

[<span data-ttu-id="ae5e3-151">Rückverfolgungsangabengruppe</span><span class="sxs-lookup"><span data-stu-id="ae5e3-151">Tracking dimension group</span></span>](/dynamicsax-2012//tracking-dimension-groups-form)

[<span data-ttu-id="ae5e3-152">Neuheiten und Änderungen</span><span class="sxs-lookup"><span data-stu-id="ae5e3-152">What's new or changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="ae5e3-153">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="ae5e3-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]