--- 
title: "Aufträge ohne Lagerort liefern"
description: Dieser Leitfaden veranschaulicht, wie ein Auftrag aktualisiert wird, wenn Produkte an den Debitor versendet werden.
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3f1b9dd4b99bcbcc6cfbc5cfd8e3271fa80c628c
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="3bab8-103">Aufträge ohne Lagerort liefern</span><span class="sxs-lookup"><span data-stu-id="3bab8-103">Ship sales orders without warehousing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3bab8-104">Dieser Leitfaden veranschaulicht, wie ein Auftrag aktualisiert wird, wenn Produkte an den Debitor versendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bab8-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="3bab8-105">Der Leitfaden betrifft den Erfüllungsfluss, der nicht für die Lagerortverwaltung eingerichtet ist (weder grundlegende oder erweiterte Lagerung) und daher keine Produktentnahme vor Lieferung erfassen muss.</span><span class="sxs-lookup"><span data-stu-id="3bab8-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="3bab8-106">Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bab8-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="3bab8-107">In beiden Fällen erstellen Sie einen Auftrag für ein inventarisiertes Produkt mit einer Menge größer als 1, bevor Sie mit der Aufgabe beginnen.</span><span class="sxs-lookup"><span data-stu-id="3bab8-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="3bab8-108">Um ein Buchungsfehler zu vermeiden, müssen Sie überprüfen ob die verfügbare Menge des Produkts im Standort und Lagerort, den Sie im Auftrag ausgewählt haben, in der Auftragsmenge enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3bab8-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="3bab8-109">Lieferschein für eine Bestellung buchen</span><span class="sxs-lookup"><span data-stu-id="3bab8-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="3bab8-110">Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="3bab8-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="3bab8-111">Wählen Sie in der Liste den Auftrag aus, den Sie für diese Aufgabe erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="3bab8-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="3bab8-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3bab8-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3bab8-113">Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".</span><span class="sxs-lookup"><span data-stu-id="3bab8-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="3bab8-114">Klicken Sie auf "Lieferschein buchen".</span><span class="sxs-lookup"><span data-stu-id="3bab8-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="3bab8-115">Erweitern oder reduzieren Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="3bab8-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="3bab8-116">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="3bab8-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="3bab8-117">Andere Optionen sind "Jetzt liefern" und "Entnommen":</span><span class="sxs-lookup"><span data-stu-id="3bab8-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="3bab8-118">Falls die Auftragsposition teilweise geliefert werden soll und das Feld Jetzt liefern auf der Auftragsposition eine Menge enthält, würden Sie Jetzt liefern auswählen.</span><span class="sxs-lookup"><span data-stu-id="3bab8-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="3bab8-119">Wenn der Erfüllungsfluss Ihrer Organisation die Entnahme als separater Prozess umfasst, der über eine Entnahmeliste verwaltet und erfasst wird, würden Sie "Entnommen" auswählen.</span><span class="sxs-lookup"><span data-stu-id="3bab8-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="3bab8-120">Überprüfen Sie, ob die Buchungsoption auf "Ja" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3bab8-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="3bab8-121">Legen Sie die Option "Lieferschein drucken" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="3bab8-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="3bab8-122">Die Registerkarte "Überblick" enthält eine Liste der in dieser Buchung zu erstellende Lieferscheine.</span><span class="sxs-lookup"><span data-stu-id="3bab8-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="3bab8-123">Wenn Sie einen einzelnen Auftrag liefern, gibt es in der Regel einen Lieferschein.</span><span class="sxs-lookup"><span data-stu-id="3bab8-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="3bab8-124">Wenn die Positionen dieses Auftrags von unterschiedlichen Standorten versendet werden sollen, wird das Buchen automatisch in die entsprechende Anzahl von Dokumenten geteilt.</span><span class="sxs-lookup"><span data-stu-id="3bab8-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="3bab8-125">Dies ist eine erforderliche Bedingung, die nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3bab8-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="3bab8-126">Ebenso wird die Buchung ebenfalls in mehrere Dokumente aufgeteilt, wenn die Positionen des Auftrags zu verschiedenen Lieferadressen versendet werden sollen, und die Lieferrichtlinie so eingerichtet ist, dass eine Teilung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3bab8-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="3bab8-127">Wählen Sie auf der Registerkarte "Positionen" die Zeile die zu liefernde Auftragsposition aus.</span><span class="sxs-lookup"><span data-stu-id="3bab8-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="3bab8-128">Wählen Sie im Feld "Aktualisieren" eine Zahl kleiner als die ursprüngliche Menge ein.</span><span class="sxs-lookup"><span data-stu-id="3bab8-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="3bab8-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3bab8-129">Click OK.</span></span>
12. <span data-ttu-id="3bab8-130">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="3bab8-130">Click Yes.</span></span>
13. <span data-ttu-id="3bab8-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3bab8-131">Close the page.</span></span>
14. <span data-ttu-id="3bab8-132">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="3bab8-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="3bab8-133">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="3bab8-133">Click Change view.</span></span>
16. <span data-ttu-id="3bab8-134">Klicken Sie auf die Kopfzeilenansicht.</span><span class="sxs-lookup"><span data-stu-id="3bab8-134">Click Header view.</span></span>
    * <span data-ttu-id="3bab8-135">Wenn alle Positionen im Auftrag vollständig geliefert wurden, wird der Auftragsstatus von "Offen" auf "Geliefert" geändert.</span><span class="sxs-lookup"><span data-stu-id="3bab8-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="3bab8-136">In diesem Beispiel ist die Auftragsposition teilweise geliefert worden.</span><span class="sxs-lookup"><span data-stu-id="3bab8-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="3bab8-137">Daher verbleibt der Auftragsstatus "Offen".</span><span class="sxs-lookup"><span data-stu-id="3bab8-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="3bab8-138">Das Feld "Dokumentstatus" wird auf "Lieferschein" festgelegt, da mindestens eine der Auftragspositionen geliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="3bab8-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="3bab8-139">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="3bab8-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="3bab8-140">Klicken Sie auf "Positionsmenge".</span><span class="sxs-lookup"><span data-stu-id="3bab8-140">Click Line quantity.</span></span>
19. <span data-ttu-id="3bab8-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3bab8-141">Close the page.</span></span>
20. <span data-ttu-id="3bab8-142">Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".</span><span class="sxs-lookup"><span data-stu-id="3bab8-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="3bab8-143">Klicken Sie auf "Lieferschein".</span><span class="sxs-lookup"><span data-stu-id="3bab8-143">Click Packing slip.</span></span>
    * <span data-ttu-id="3bab8-144">Die Seite "Lieferscheinerfassung" enthält alle Lieferscheindokumente, die für Ihren Auftrag generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3bab8-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="3bab8-145">Sie können Details jedes Dokuments zu prüfen und drucken, wenn Sie wünschen.</span><span class="sxs-lookup"><span data-stu-id="3bab8-145">You can review details of each document and print them, if you wish.</span></span>  


