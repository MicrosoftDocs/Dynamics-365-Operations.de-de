---
title: Kostenobjekte
description: Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden. Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden. Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.
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
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6501e8d809d12df421ad081662d23a6b5005f39c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742136"
---
# <a name="cost-objects"></a><span data-ttu-id="b6885-105">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="b6885-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6885-106">Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden.</span><span class="sxs-lookup"><span data-stu-id="b6885-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="b6885-107">Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden.</span><span class="sxs-lookup"><span data-stu-id="b6885-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="b6885-108">Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.</span><span class="sxs-lookup"><span data-stu-id="b6885-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="b6885-109">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="b6885-109">Cost objects</span></span>

<span data-ttu-id="b6885-110">Auf der Seite **Kostenobjekte** werden alle Kostenobjekte aufgeführt, die für ein Produkt erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="b6885-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="b6885-111">Die Kostenobjekte werden durch Daten aus den folgenden Ressourcen definiert:</span><span class="sxs-lookup"><span data-stu-id="b6885-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="b6885-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="b6885-112">Product</span></span>
-   <span data-ttu-id="b6885-113">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="b6885-113">Product dimension group</span></span>
-   <span data-ttu-id="b6885-114">Lagerdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="b6885-114">Storage dimension group</span></span>
-   <span data-ttu-id="b6885-115">Rückverfolgungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b6885-115">Tracking dimension group</span></span>

<span data-ttu-id="b6885-116">**Hinweis:** Ein Kostenobjekte stellt nur ein Kostenelement des Typs **Direktmaterial** dar.</span><span class="sxs-lookup"><span data-stu-id="b6885-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="b6885-117">Ein Kostenobjekte und ein Bestandsobjekt unterscheiden sich dadurch, dass ein Kostenträger durch die Lagerungsdimensionen definiert wird, die für den wertmäßigen Bestand ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="b6885-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="b6885-118">Ein Artikel hat zum Beispiel die folgende Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="b6885-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="b6885-119">**Standort:** Physischer Bestand = Ja, wertmäßiger Bestand = Ja</span><span class="sxs-lookup"><span data-stu-id="b6885-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="b6885-120">**Lagerort:** Physischer Bestand = Ja, wertmäßiger Bestand = Nein</span><span class="sxs-lookup"><span data-stu-id="b6885-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="b6885-121">**Chargennummer:** Physischer Bestand = Ja, wertmäßiger Bestand = Nein</span><span class="sxs-lookup"><span data-stu-id="b6885-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="b6885-122">In der folgenden Tabelle zeigt, was ein Kostenobjekte ist und was ein Bestandsobjekt ist.</span><span class="sxs-lookup"><span data-stu-id="b6885-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="b6885-123">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="b6885-123">Object type</span></span>      | <span data-ttu-id="b6885-124">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="b6885-124">Item number</span></span> | <span data-ttu-id="b6885-125">Standort</span><span class="sxs-lookup"><span data-stu-id="b6885-125">Site</span></span> | <span data-ttu-id="b6885-126">Lagerort</span><span class="sxs-lookup"><span data-stu-id="b6885-126">Warehouse</span></span> | <span data-ttu-id="b6885-127">Chargennummer</span><span class="sxs-lookup"><span data-stu-id="b6885-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="b6885-128">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="b6885-128">Cost object</span></span>      | <span data-ttu-id="b6885-129"> -</span><span class="sxs-lookup"><span data-stu-id="b6885-129">x</span></span>           | <span data-ttu-id="b6885-130"> -</span><span class="sxs-lookup"><span data-stu-id="b6885-130">x</span></span>    |           |           |
| <span data-ttu-id="b6885-131">Bestandsobjekt</span><span class="sxs-lookup"><span data-stu-id="b6885-131">Inventory object</span></span> | <span data-ttu-id="b6885-132"> -</span><span class="sxs-lookup"><span data-stu-id="b6885-132">x</span></span>           | <span data-ttu-id="b6885-133"> -</span><span class="sxs-lookup"><span data-stu-id="b6885-133">x</span></span>    |  <span data-ttu-id="b6885-134"> -</span><span class="sxs-lookup"><span data-stu-id="b6885-134">x</span></span>        | <span data-ttu-id="b6885-135"> -</span><span class="sxs-lookup"><span data-stu-id="b6885-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="b6885-136">Ansammlung von Kosten und Mengen</span><span class="sxs-lookup"><span data-stu-id="b6885-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="b6885-137">Der Wert im Feld **Wert** ist eine Summe der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="b6885-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="b6885-138">Phys. Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="b6885-138">Physical cost amount</span></span>
    -   <span data-ttu-id="b6885-139">Wertmäßiger Einstandsbetrag</span><span class="sxs-lookup"><span data-stu-id="b6885-139">Financial cost amount</span></span>
    -   <span data-ttu-id="b6885-140">Regulierungen</span><span class="sxs-lookup"><span data-stu-id="b6885-140">Adjustments</span></span>
-   <span data-ttu-id="b6885-141">Der Wert im Feld **Menge** ist eine Summe der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="b6885-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="b6885-142">Empfangen</span><span class="sxs-lookup"><span data-stu-id="b6885-142">Received</span></span>
    -   <span data-ttu-id="b6885-143">Abgesetzt</span><span class="sxs-lookup"><span data-stu-id="b6885-143">Deducted</span></span>
    -   <span data-ttu-id="b6885-144">Gebuchte Menge</span><span class="sxs-lookup"><span data-stu-id="b6885-144">Posted quantity</span></span>
-   <span data-ttu-id="b6885-145">Das Feld **Durchschnittlichen Einheitenkosten** ist ein berechnetes Feld.</span><span class="sxs-lookup"><span data-stu-id="b6885-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="b6885-146">Der Wert wird berechnet, indem der Wert **Wert** durch den Wert **Menge** geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="b6885-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="b6885-147">**Hinweis:** Der Parameter **Physischen Wert einbeziehen** hat keinen Einfluss auf die vorhergehenden Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="b6885-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b6885-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b6885-148">Additional resources</span></span>
--------

[<span data-ttu-id="b6885-149">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="b6885-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="b6885-150">Lagerdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="b6885-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="b6885-151">Rückverfolgungsangabengruppe</span><span class="sxs-lookup"><span data-stu-id="b6885-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="b6885-152">Neuheiten und Änderungen</span><span class="sxs-lookup"><span data-stu-id="b6885-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="b6885-153">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="b6885-153">Cost entries</span></span>](cost-entries.md)



