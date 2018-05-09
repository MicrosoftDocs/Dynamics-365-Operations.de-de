--- 
title: "Kaufverträge erfüllen"
description: "Dieses Verfahren zeigt Ihnen, wie einen Kaufvertrag über die Zuordnung von Aufträgen erfüllt wird."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d2f6bf58344a1128fa4bf635e2fa27f2049e513e
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="f4c91-103">Kaufverträge erfüllen</span><span class="sxs-lookup"><span data-stu-id="f4c91-103">Fulfill sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4c91-104">Dieses Verfahren zeigt Ihnen, wie einen Kaufvertrag über die Zuordnung von Aufträgen erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="f4c91-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="f4c91-105">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4c91-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f4c91-106">Bevor Sie mit diesem Leitfaden starten, vergewissern Sie sich, einen gültigen Kaufvertrag vom Typ "Produktwertszusage " vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f4c91-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="f4c91-107">Alternativ können Sie den Leitfaden "Kaufvertrag erstellen" ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4c91-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="f4c91-108">Genehmigen einer Bestellung über den Kaufvertrags</span><span class="sxs-lookup"><span data-stu-id="f4c91-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="f4c91-109">Wechseln Sie zu "Vertrieb und Marketing" > "Kaufverträge" > "Kaufverträge".</span><span class="sxs-lookup"><span data-stu-id="f4c91-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="f4c91-110">Öffnen Sie in der Liste den Kaufvertrag, für den Sie die Bestellung genehmigen möchten.</span><span class="sxs-lookup"><span data-stu-id="f4c91-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="f4c91-111">Klicken Sie im Aktivitätsbereich auf "Kaufvertrag".</span><span class="sxs-lookup"><span data-stu-id="f4c91-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="f4c91-112">Klicken Sie auf "Kaufvertrag genehmigen".</span><span class="sxs-lookup"><span data-stu-id="f4c91-112">Click Release order.</span></span>
    * <span data-ttu-id="f4c91-113">Da der Text oben auf der Seite "Freigabeauftrag erstellen" zeigt die Details, die für die Auftragspositionen benötigt werden. Diese weiche abhängig von, ob der Vertrag mengen- oder wertbasiert ist ab.</span><span class="sxs-lookup"><span data-stu-id="f4c91-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="f4c91-114">Der Vertrag in diesem Leitfaden hat den Typ "Produktwertszusage".</span><span class="sxs-lookup"><span data-stu-id="f4c91-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="f4c91-115">Daher ist der Abschnitt "Positionen" dieser Seite leer.</span><span class="sxs-lookup"><span data-stu-id="f4c91-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="f4c91-116">Wenn die Zusage auf der Menge basiert, werden die Positionsinformationen aus dem Vertrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="f4c91-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="f4c91-117">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="f4c91-117">Click Create.</span></span>
    * <span data-ttu-id="f4c91-118">Die Nachricht informiert Sie darüber, dass eine Bestellung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f4c91-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="f4c91-119">Da der Auftrag keine Positionen enthält, müssen Sie Auftragspositionsdetails hinzufügen, um den Freigabeprozess abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f4c91-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="f4c91-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4c91-120">Close the page.</span></span>
7. <span data-ttu-id="f4c91-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4c91-121">Close the page.</span></span>
8. <span data-ttu-id="f4c91-122">Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="f4c91-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="f4c91-123">Wählen Sie in der Liste den Auftrag, der als Ergebnis der Auftragsgenehmigung in der vorherigen Aufgabe erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f4c91-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="f4c91-124">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f4c91-124">Click Add line.</span></span>
11. <span data-ttu-id="f4c91-125">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4c91-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="f4c91-126">Wählen Sie im Feld "Artikelnummer" den Artikel aus, der auf dem zugeordneten Kaufvertrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4c91-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="f4c91-127">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f4c91-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f4c91-128">Stellen Sie sicher, dass Sie eine Menge eingeben, die den Nettobetrag unter den Wert des zugeordneten Kaufvertrags bringt lässt.</span><span class="sxs-lookup"><span data-stu-id="f4c91-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="f4c91-129">Beachten Sie, dass, da der Auftrag mit dem Vertrag verknüpft ist, der verhandelte Rabattprozentsatz auf die Auftragsposition angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4c91-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="f4c91-130">Klicken Sie auf "Position aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="f4c91-130">Click Update line.</span></span>
15. <span data-ttu-id="f4c91-131">Klicken Sie auf "Zugeordnet".</span><span class="sxs-lookup"><span data-stu-id="f4c91-131">Click Attached.</span></span>
    * <span data-ttu-id="f4c91-132">Die Seite "Zugeordneter Vertrag" zeigt die Kennung und die Vertragsbedingungen an, über die die Position freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4c91-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="f4c91-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4c91-133">Close the page.</span></span>
17. <span data-ttu-id="f4c91-134">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="f4c91-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="f4c91-135">Klicken Sie auf "Zugeordneter Kaufvertrag".</span><span class="sxs-lookup"><span data-stu-id="f4c91-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="f4c91-136">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="f4c91-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="f4c91-137">Klicken Sie auf die Registerkarte "Erfüllung".</span><span class="sxs-lookup"><span data-stu-id="f4c91-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="f4c91-138">Die Erfüllungsregisterkarte zeit eine Zusammenfassung aller Auftragspositionen, ihren Erfüllungsstatus sowie der Betrag oder die Menge die noch nicht freigegeben wurde an, die dieser Zusage zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f4c91-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="f4c91-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4c91-139">Close the page.</span></span>
22. <span data-ttu-id="f4c91-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4c91-140">Close the page.</span></span>
23. <span data-ttu-id="f4c91-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f4c91-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="f4c91-142">Anwenden des Kaufvertrags im Bestellungsprozess</span><span class="sxs-lookup"><span data-stu-id="f4c91-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="f4c91-143">Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="f4c91-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="f4c91-144">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f4c91-144">Click New.</span></span>
3. <span data-ttu-id="f4c91-145">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4c91-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f4c91-146">Wählen Sie in der Liste den Debitor aus, der im Kaufvertrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4c91-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="f4c91-147">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4c91-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f4c91-148">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="f4c91-148">Expand the General section.</span></span>
7. <span data-ttu-id="f4c91-149">Klicken Sie im Feld "Kaufvertragskennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4c91-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f4c91-150">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4c91-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f4c91-151">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="f4c91-151">Click Yes.</span></span>
10. <span data-ttu-id="f4c91-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4c91-152">Click OK.</span></span>
11. <span data-ttu-id="f4c91-153">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4c91-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="f4c91-154">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4c91-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f4c91-155">Wählen Sie im Feld "Artikelnummer" den Artikel aus, der auf dem zugeordneten Kaufvertrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4c91-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="f4c91-156">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4c91-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="f4c91-157">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="f4c91-157">Click Save.</span></span>
16. <span data-ttu-id="f4c91-158">Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".</span><span class="sxs-lookup"><span data-stu-id="f4c91-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="f4c91-159">Klicken Sie auf "Lieferschein buchen".</span><span class="sxs-lookup"><span data-stu-id="f4c91-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="f4c91-160">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="f4c91-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="f4c91-161">Wählen Sie "Ja" im Feld "Buchung" aus.</span><span class="sxs-lookup"><span data-stu-id="f4c91-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="f4c91-162">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4c91-162">Click OK.</span></span>
21. <span data-ttu-id="f4c91-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f4c91-163">Click OK.</span></span>
22. <span data-ttu-id="f4c91-164">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="f4c91-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="f4c91-165">Klicken Sie auf "Zugeordneter Kaufvertrag".</span><span class="sxs-lookup"><span data-stu-id="f4c91-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="f4c91-166">Klicken Sie auf die Registerkarte "Erfüllung".</span><span class="sxs-lookup"><span data-stu-id="f4c91-166">Click the Fulfillment tab.</span></span>


