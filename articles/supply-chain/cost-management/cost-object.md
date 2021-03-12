---
title: Kostenobjekte
description: Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden. Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden. Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.
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
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65a0f72f8d97bda36bacd691d545807c413f8825
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967657"
---
# <a name="cost-objects"></a><span data-ttu-id="490ee-105">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="490ee-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="490ee-106">Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden.</span><span class="sxs-lookup"><span data-stu-id="490ee-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="490ee-107">Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden.</span><span class="sxs-lookup"><span data-stu-id="490ee-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="490ee-108">Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.</span><span class="sxs-lookup"><span data-stu-id="490ee-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="490ee-109">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="490ee-109">Cost objects</span></span>

<span data-ttu-id="490ee-110">Auf der Seite **Kostenobjekte** werden alle Kostenobjekte aufgeführt, die für ein Produkt erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="490ee-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="490ee-111">Die Kostenobjekte werden durch Daten aus den folgenden Ressourcen definiert:</span><span class="sxs-lookup"><span data-stu-id="490ee-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="490ee-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="490ee-112">Product</span></span>
-   <span data-ttu-id="490ee-113">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="490ee-113">Product dimension group</span></span>
-   <span data-ttu-id="490ee-114">Lagerdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="490ee-114">Storage dimension group</span></span>
-   <span data-ttu-id="490ee-115">Rückverfolgungsgruppe</span><span class="sxs-lookup"><span data-stu-id="490ee-115">Tracking dimension group</span></span>

<span data-ttu-id="490ee-116">**Hinweis:** Ein Kostenobjekte stellt nur ein Kostenelement des Typs **Direktmaterial** dar.</span><span class="sxs-lookup"><span data-stu-id="490ee-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="490ee-117">Ein Kostenobjekte und ein Bestandsobjekt unterscheiden sich dadurch, dass ein Kostenträger durch die Lagerungsdimensionen definiert wird, die für den wertmäßigen Bestand ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="490ee-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="490ee-118">Ein Artikel hat zum Beispiel die folgende Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="490ee-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="490ee-119">**Standort:** Physischer Bestand = Ja, wertmäßiger Bestand = Ja</span><span class="sxs-lookup"><span data-stu-id="490ee-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="490ee-120">**Lagerort:** Physischer Bestand = Ja, wertmäßiger Bestand = Nein</span><span class="sxs-lookup"><span data-stu-id="490ee-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="490ee-121">**Chargennummer:** Physischer Bestand = Ja, wertmäßiger Bestand = Nein</span><span class="sxs-lookup"><span data-stu-id="490ee-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="490ee-122">In der folgenden Tabelle zeigt, was ein Kostenobjekte ist und was ein Bestandsobjekt ist.</span><span class="sxs-lookup"><span data-stu-id="490ee-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="490ee-123">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="490ee-123">Object type</span></span>      | <span data-ttu-id="490ee-124">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="490ee-124">Item number</span></span> | <span data-ttu-id="490ee-125">Standort</span><span class="sxs-lookup"><span data-stu-id="490ee-125">Site</span></span> | <span data-ttu-id="490ee-126">Lagerort</span><span class="sxs-lookup"><span data-stu-id="490ee-126">Warehouse</span></span> | <span data-ttu-id="490ee-127">Chargennummer</span><span class="sxs-lookup"><span data-stu-id="490ee-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="490ee-128">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="490ee-128">Cost object</span></span>      | <span data-ttu-id="490ee-129"> -</span><span class="sxs-lookup"><span data-stu-id="490ee-129">x</span></span>           | <span data-ttu-id="490ee-130"> -</span><span class="sxs-lookup"><span data-stu-id="490ee-130">x</span></span>    |           |           |
| <span data-ttu-id="490ee-131">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="490ee-131">Inventory object</span></span> | <span data-ttu-id="490ee-132"> -</span><span class="sxs-lookup"><span data-stu-id="490ee-132">x</span></span>           | <span data-ttu-id="490ee-133"> -</span><span class="sxs-lookup"><span data-stu-id="490ee-133">x</span></span>    |  <span data-ttu-id="490ee-134"> -</span><span class="sxs-lookup"><span data-stu-id="490ee-134">x</span></span>        | <span data-ttu-id="490ee-135"> -</span><span class="sxs-lookup"><span data-stu-id="490ee-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="490ee-136">Ansammlung von Kosten und Mengen</span><span class="sxs-lookup"><span data-stu-id="490ee-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="490ee-137">Der Wert im Feld **Wert** ist eine Summe der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="490ee-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="490ee-138">Phys. Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="490ee-138">Physical cost amount</span></span>
    -   <span data-ttu-id="490ee-139">Wertmäßiger Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="490ee-139">Financial cost amount</span></span>
    -   <span data-ttu-id="490ee-140">Regulierungen</span><span class="sxs-lookup"><span data-stu-id="490ee-140">Adjustments</span></span>
-   <span data-ttu-id="490ee-141">Der Wert im Feld **Menge** ist eine Summe der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="490ee-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="490ee-142">Empfangen</span><span class="sxs-lookup"><span data-stu-id="490ee-142">Received</span></span>
    -   <span data-ttu-id="490ee-143">Abgesetzt</span><span class="sxs-lookup"><span data-stu-id="490ee-143">Deducted</span></span>
    -   <span data-ttu-id="490ee-144">Gebuchte Menge</span><span class="sxs-lookup"><span data-stu-id="490ee-144">Posted quantity</span></span>
-   <span data-ttu-id="490ee-145">Das Feld **Durchschnittlichen Einheitenkosten** ist ein berechnetes Feld.</span><span class="sxs-lookup"><span data-stu-id="490ee-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="490ee-146">Der Wert wird berechnet, indem der Wert **Wert** durch den Wert **Menge** geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="490ee-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="490ee-147">**Hinweis:** Der Parameter **Physischen Wert einbeziehen** hat keinen Einfluss auf die vorhergehenden Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="490ee-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="490ee-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="490ee-148">Additional resources</span></span>
--------

[<span data-ttu-id="490ee-149">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="490ee-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="490ee-150">Lagerdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="490ee-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="490ee-151">Rückverfolgungsangabengruppe</span><span class="sxs-lookup"><span data-stu-id="490ee-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="490ee-152">Neuheiten und Änderungen</span><span class="sxs-lookup"><span data-stu-id="490ee-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="490ee-153">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="490ee-153">Cost entries</span></span>](cost-entries.md)



