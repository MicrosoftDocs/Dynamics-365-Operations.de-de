--- 
title: Lieferzeitplan erstellen
description: "Diese Prozedur zeigt, wie ein Lieferzeitplan für einen Auftrag erstellt wird."
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 13add634e275a0156c2c0f87d1fec80385d62fea
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="30ae0-103">Lieferzeitplan erstellen</span><span class="sxs-lookup"><span data-stu-id="30ae0-103">Create a delivery schedule</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30ae0-104">Diese Prozedur zeigt, wie ein Lieferzeitplan für einen Auftrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="30ae0-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="30ae0-105">Ein Lieferzeitplan wird verwendet, wenn eine Menge für einen Auftrag oder ein Angebot angefordert wird, um in mehreren Lieferungen geliefert zu werden.</span><span class="sxs-lookup"><span data-stu-id="30ae0-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="30ae0-106">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="30ae0-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="30ae0-107">Lieferzeitplan erstellen</span><span class="sxs-lookup"><span data-stu-id="30ae0-107">Create delivery schedule</span></span>
1. <span data-ttu-id="30ae0-108">Wechseln Sie zu "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="30ae0-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="30ae0-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="30ae0-109">Click New.</span></span>
3. <span data-ttu-id="30ae0-110">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="30ae0-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="30ae0-111">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="30ae0-111">Click OK.</span></span>
5. <span data-ttu-id="30ae0-112">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="30ae0-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="30ae0-113">Geben Sie im Feld "Menge" eine Zahl ein, die größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="30ae0-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="30ae0-114">Klicken Sie auf "Auftragsposition".</span><span class="sxs-lookup"><span data-stu-id="30ae0-114">Click Sales order line.</span></span>
8. <span data-ttu-id="30ae0-115">Klicken Sie auf "Lieferzeitplan".</span><span class="sxs-lookup"><span data-stu-id="30ae0-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="30ae0-116">Die Seite "Lieferzeitplan" ist der Ort, an dem Sie die Anzahl von Lieferungen angeben können, in denen die Gesamtmenge der Auftragsposition an den Debitor geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="30ae0-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="30ae0-117">Standardmäßig kopiert das System die Gesamtmenge und andere Lieferdetails der ursprünglichen Auftragsposition in die erste Lieferzeitplanposition.</span><span class="sxs-lookup"><span data-stu-id="30ae0-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="30ae0-118">In diesem Beispiel erstellen wir einen Zeitplan für zwei Lieferungen, wobei das Datum der zweiten Lieferung um eine Woche nach der ersten verschoben ist.</span><span class="sxs-lookup"><span data-stu-id="30ae0-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="30ae0-119">Geben Sie im Feld "Menge" eine Zahl ein, die Teil der Gesamtmenge ist.</span><span class="sxs-lookup"><span data-stu-id="30ae0-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="30ae0-120">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="30ae0-120">Click New.</span></span>
11. <span data-ttu-id="30ae0-121">Geben Sie im Feld "Menge" die verbleibende Menge ein.</span><span class="sxs-lookup"><span data-stu-id="30ae0-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="30ae0-122">Geben Sie im Feld "Angefordertes Lieferdatum" ein Datum ein, das eine Woche nach dem Datum der ersten Lieferposition liegt.</span><span class="sxs-lookup"><span data-stu-id="30ae0-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="30ae0-123">Die beiden Optionen im Inforegister "Konvertierung von Belastungen" steuern, wie Sie die Belastungen über die Lieferzeitplanpositionen verteilen möchten, sobald diese der ursprünglichen Auftragsposition zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="30ae0-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="30ae0-124">Wenn Sie "Bruttobeträge kopieren" auswählen, wird derselbe Belastungsbetrag zu jeder Position kopiert.</span><span class="sxs-lookup"><span data-stu-id="30ae0-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="30ae0-125">Die Option "Zu Lieferpositionen zuordnen" verteilt die Belastung gleichmäßig auf die Lieferpositionen.</span><span class="sxs-lookup"><span data-stu-id="30ae0-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="30ae0-126">Nur feste Belastungen können aufgeteilt werden, wohingegen variable Belastungen nach wie vor in die Positionen kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="30ae0-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="30ae0-127">Verschieben Sie den Cursor weg von der zweiten Lieferposition, um die Seite zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="30ae0-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="30ae0-128">Sie können die Gesamtmenge nachverfolgen, die den Lieferzeitplanpositionen zugeordnet ist, indem Sie die Felder "Summe" und "Verbleibend" betrachten.</span><span class="sxs-lookup"><span data-stu-id="30ae0-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="30ae0-129">Wenn die Restmenge Null ist, ist die gesamte Menge aus der ursprünglichen Position dem Zeitplan zugewiesen worden.</span><span class="sxs-lookup"><span data-stu-id="30ae0-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="30ae0-130">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="30ae0-130">Click OK.</span></span>
    * <span data-ttu-id="30ae0-131">Der Lieferzeitplan wurde jetzt in die Auftragspositionen kopiert.</span><span class="sxs-lookup"><span data-stu-id="30ae0-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="30ae0-132">Die ursprüngliche Auftragsposition, die als "Geschäftsbezogene Position" bezeichnet wird, ist in eine "Auftragsposition mit mehreren Lieferungen" umgewandelt worden.</span><span class="sxs-lookup"><span data-stu-id="30ae0-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="30ae0-133">Sie ist mit einem eindeutig identifizierbarem Symbol markiert und fungiert als eine Kopfzeile für die Lieferpositionen.</span><span class="sxs-lookup"><span data-stu-id="30ae0-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="30ae0-134">Die beiden neuen Positionen, die als Lieferpositionen bezeichnet werden, bilden einen Lieferzeitplan.</span><span class="sxs-lookup"><span data-stu-id="30ae0-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="30ae0-135">Der Auftrag wird anhand dieser Positionen und nicht der ursprünglichen Position verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="30ae0-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="30ae0-136">Wenn Dokumente wie Auftragsbestätigungen, Kommissionierlisten, Lieferscheine oder Rechnungen gedruckt werden, werden nur die Lieferpositionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="30ae0-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="30ae0-137">Die Lieferpositionen können verschiedene Lieferdaten, Mengen, Lieferarten und Lagerdimensionen haben, wie Standort und Lagerort.</span><span class="sxs-lookup"><span data-stu-id="30ae0-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="30ae0-138">Allerdings müssen die Produktdimensionen immer mit denen in der geschäftsbezogenen Position übereinstimmen und können nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="30ae0-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="30ae0-139">Geben Sie im Feld "Menge" eine Zahl ein, die größer als die aktuelle ist.</span><span class="sxs-lookup"><span data-stu-id="30ae0-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="30ae0-140">Wählen Sie die geschäftsbezogene Position aus, um die Auswirkung der Mengenneuberechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="30ae0-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="30ae0-141">Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".</span><span class="sxs-lookup"><span data-stu-id="30ae0-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="30ae0-142">Klicken Sie auf "Lieferschein buchen".</span><span class="sxs-lookup"><span data-stu-id="30ae0-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="30ae0-143">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="30ae0-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="30ae0-144">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="30ae0-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="30ae0-145">Beachten Sie, dass der Lieferschein für die beiden Lieferzeitplanpositionen und nicht die ursprüngliche Auftragsposition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="30ae0-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="30ae0-146">Wählen Sie "Ja" im Feld "Lieferschein drucken" aus.</span><span class="sxs-lookup"><span data-stu-id="30ae0-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="30ae0-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="30ae0-147">Click OK.</span></span>
23. <span data-ttu-id="30ae0-148">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="30ae0-148">Click Yes.</span></span>
24. <span data-ttu-id="30ae0-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="30ae0-149">Close the page.</span></span>


