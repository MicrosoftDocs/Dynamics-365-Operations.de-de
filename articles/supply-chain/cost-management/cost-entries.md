---
title: Kosteneinträge
description: Dieser Artikel enthält Informationen zu Kosteneinträgen und wenn sie erstellt werden. Ein Kosteneintrag ist ein Datensatz, der die Menge und die Kosten eines gegebenen Ereignisses erfasst.
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
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ddd263852fc328756a6dc06bc3f02c661cbd40f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228634"
---
# <a name="cost-entries"></a><span data-ttu-id="a51c1-104">Kosteneinträge</span><span class="sxs-lookup"><span data-stu-id="a51c1-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a51c1-105">Dieser Artikel enthält Informationen zu Kosteneinträgen und wenn sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a51c1-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="a51c1-106">Ein Kosteneintrag ist ein Datensatz, der die Menge und die Kosten eines gegebenen Ereignisses erfasst.</span><span class="sxs-lookup"><span data-stu-id="a51c1-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="a51c1-107">Kosteneinträge sind Aggregationen von Lagerbuchungen, die zu aktiven Dimensionen des wertmäßigen Bestands erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="a51c1-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="a51c1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a51c1-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="a51c1-109">Beispiel 1: Keine Kosteneinträge werden erstellt</span><span class="sxs-lookup"><span data-stu-id="a51c1-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="a51c1-110">Ein Umlagerungserfassungsereignis wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="a51c1-110">A transfer journal event is registered.</span></span> <span data-ttu-id="a51c1-111">Das Ereignis überträgt ein Stück des Artikels A vom Lagerplatz A zum Lagerplatz B. Die Lagerplatzlagerungsdimension ist nicht Teil des Kostenobjekts.</span><span class="sxs-lookup"><span data-stu-id="a51c1-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="a51c1-112">Daher erstellt das Ereignis zwei Lagerbuchungen und keine Kosteneinträge.</span><span class="sxs-lookup"><span data-stu-id="a51c1-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="a51c1-113">Beispiel 2: Kosteneinträge werden erstellt</span><span class="sxs-lookup"><span data-stu-id="a51c1-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="a51c1-114">Ein Umlagerungserfassungsereignis wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="a51c1-114">A transfer journal event is registered.</span></span> <span data-ttu-id="a51c1-115">Das Ereignis überträgt zur Produktion eines Artikels von einem Standort 1 an Standort 2.</span><span class="sxs-lookup"><span data-stu-id="a51c1-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="a51c1-116">Die Standortlagerdimension wird als Teil des Kostenträgers betrachtet.</span><span class="sxs-lookup"><span data-stu-id="a51c1-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="a51c1-117">Daher erstellt das Ereignis zwei Lagerbuchungen und zwei Kosteneinträge.</span><span class="sxs-lookup"><span data-stu-id="a51c1-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="a51c1-118">Beispiel 3: Ein Kosteneintrag wird erstellt</span><span class="sxs-lookup"><span data-stu-id="a51c1-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="a51c1-119">Ein Produktzugangsereignis wird für eine Bestellung erfasst.</span><span class="sxs-lookup"><span data-stu-id="a51c1-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="a51c1-120">Das Ereignis erfasst 100 Stück des Artikels A zu Einheitenkosten von 10,00 Euro.</span><span class="sxs-lookup"><span data-stu-id="a51c1-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="a51c1-121">Da Artikel A eine Seriennummer verwendet, um den Zweck der Lagerverwaltung zu verfolgen, wird eine eindeutige Seriennummer für jeden Artikel erstellt, der eingegangen ist.</span><span class="sxs-lookup"><span data-stu-id="a51c1-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="a51c1-122">Daher erstellt das Ereignis 100 Lagerbuchungen und einen Kosteneintrag.</span><span class="sxs-lookup"><span data-stu-id="a51c1-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="a51c1-123">Kosteneinträge-Seite</span><span class="sxs-lookup"><span data-stu-id="a51c1-123">Cost entries page</span></span>
<span data-ttu-id="a51c1-124">Die neue **Kosteneinträge**-Seite ermöglicht die Anzeige und Steuerung von Erfassungen für Mengen und Kosten.</span><span class="sxs-lookup"><span data-stu-id="a51c1-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="a51c1-125">Diese Seite ergänzt die Seiten **Lagerbuchung** und **Lagerausgleich**.</span><span class="sxs-lookup"><span data-stu-id="a51c1-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="a51c1-126">Datensätze werden in chronologischer Reihenfolge für ein Ereignis erfasst.</span><span class="sxs-lookup"><span data-stu-id="a51c1-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="a51c1-127">Daher können Sie die kumulierten Kosten eines bestimmten Ereignisses oder aller Ereignisse zu einem Dokument schnell finden und steuern.</span><span class="sxs-lookup"><span data-stu-id="a51c1-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="a51c1-128">Hier ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a51c1-128">Here is an example:</span></span>

-   <span data-ttu-id="a51c1-129">Ein Produktzugangsereignis wird für Artikel A. erfasst. Es werden hundert Stück zu Einheitenkosten von EUR 10,00 empfangen.</span><span class="sxs-lookup"><span data-stu-id="a51c1-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="a51c1-130">Eine paar Tage nach der Erfassung des Rechnungsereignisses steigen die Kosten auf 11,00 EUR.</span><span class="sxs-lookup"><span data-stu-id="a51c1-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="a51c1-131">Daher ist der Gesamtbetrag nun 1.100 EUR.</span><span class="sxs-lookup"><span data-stu-id="a51c1-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="a51c1-132">Ein zweiter Beleg wird erstellt, um die Differenz von 100 EUR zu buchen.</span><span class="sxs-lookup"><span data-stu-id="a51c1-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="a51c1-133">Einige Tage später, wird ein sonstiger Zuschlag von 15,00 EUR zur Abdeckung der Transportkosten auf der Bestellung erfasst.</span><span class="sxs-lookup"><span data-stu-id="a51c1-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="a51c1-134">Beleg</span><span class="sxs-lookup"><span data-stu-id="a51c1-134">Voucher</span></span> | <span data-ttu-id="a51c1-135">Datum</span><span class="sxs-lookup"><span data-stu-id="a51c1-135">Date</span></span>       | <span data-ttu-id="a51c1-136">Referenz</span><span class="sxs-lookup"><span data-stu-id="a51c1-136">Reference</span></span>      | <span data-ttu-id="a51c1-137">Anzahl</span><span class="sxs-lookup"><span data-stu-id="a51c1-137">Number</span></span> | <span data-ttu-id="a51c1-138">Loskennung</span><span class="sxs-lookup"><span data-stu-id="a51c1-138">Lot ID</span></span>  | <span data-ttu-id="a51c1-139">Leistung</span><span class="sxs-lookup"><span data-stu-id="a51c1-139">Quantity</span></span> | <span data-ttu-id="a51c1-140">Betrag</span><span class="sxs-lookup"><span data-stu-id="a51c1-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="a51c1-141">00001</span><span class="sxs-lookup"><span data-stu-id="a51c1-141">00001</span></span>   | <span data-ttu-id="a51c1-142">01.01.2015</span><span class="sxs-lookup"><span data-stu-id="a51c1-142">01-01-2015</span></span> | <span data-ttu-id="a51c1-143">Bestellung</span><span class="sxs-lookup"><span data-stu-id="a51c1-143">Purchase order</span></span> | <span data-ttu-id="a51c1-144">100001</span><span class="sxs-lookup"><span data-stu-id="a51c1-144">100001</span></span> | <span data-ttu-id="a51c1-145">0000101</span><span class="sxs-lookup"><span data-stu-id="a51c1-145">0000101</span></span> | <span data-ttu-id="a51c1-146">100,00</span><span class="sxs-lookup"><span data-stu-id="a51c1-146">100.00</span></span>   | <span data-ttu-id="a51c1-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="a51c1-147">1000.00</span></span> |
| <span data-ttu-id="a51c1-148">00002</span><span class="sxs-lookup"><span data-stu-id="a51c1-148">00002</span></span>   | <span data-ttu-id="a51c1-149">20.01.2015</span><span class="sxs-lookup"><span data-stu-id="a51c1-149">20-01-2015</span></span> | <span data-ttu-id="a51c1-150">Bestellung</span><span class="sxs-lookup"><span data-stu-id="a51c1-150">Purchase order</span></span> | <span data-ttu-id="a51c1-151">100001</span><span class="sxs-lookup"><span data-stu-id="a51c1-151">100001</span></span> | <span data-ttu-id="a51c1-152">0000101</span><span class="sxs-lookup"><span data-stu-id="a51c1-152">0000101</span></span> |          | <span data-ttu-id="a51c1-153">100,00</span><span class="sxs-lookup"><span data-stu-id="a51c1-153">100.00</span></span>  |
| <span data-ttu-id="a51c1-154">00003</span><span class="sxs-lookup"><span data-stu-id="a51c1-154">00003</span></span>   | <span data-ttu-id="a51c1-155">31.01.2015</span><span class="sxs-lookup"><span data-stu-id="a51c1-155">31-01-2015</span></span> | <span data-ttu-id="a51c1-156">Regulierung</span><span class="sxs-lookup"><span data-stu-id="a51c1-156">Adjustment</span></span>     | <span data-ttu-id="a51c1-157">100001</span><span class="sxs-lookup"><span data-stu-id="a51c1-157">100001</span></span> | <span data-ttu-id="a51c1-158">0000101</span><span class="sxs-lookup"><span data-stu-id="a51c1-158">0000101</span></span> |          | <span data-ttu-id="a51c1-159">15:00</span><span class="sxs-lookup"><span data-stu-id="a51c1-159">15.00</span></span>   |

<span data-ttu-id="a51c1-160">Die **Kosteneinträge**-Seite ermöglicht das Filter nach der Dokumentenkennung und dem Dokumentdatum.</span><span class="sxs-lookup"><span data-stu-id="a51c1-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="a51c1-161">Kosteneinträge sind nur für [Kostenobjekte ](cost-object.md)oder freigegebene Produkte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a51c1-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a51c1-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a51c1-162">Additional resources</span></span>
--------

[<span data-ttu-id="a51c1-163">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="a51c1-163">Cost objects</span></span>](cost-object.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]