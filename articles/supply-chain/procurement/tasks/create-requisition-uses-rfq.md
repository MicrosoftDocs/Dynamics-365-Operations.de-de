--- 
title: Eine Anforderung erstellen, die eine Angebotsanforderung verwendet
description: "Dieser Leitfaden zeigt, wie man Preis- und Kreditoreninformationen einer Bestellanforderung von einem Angebotsanforderungsprozess aus hinzufügt."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2c2daad961ec5c47ca49b2e53a2118570caf6a58
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="bc232-103">Eine Anforderung erstellen, die eine Angebotsanforderung verwendet</span><span class="sxs-lookup"><span data-stu-id="bc232-103">Create a requisition that uses an RFQ</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc232-104">Dieser Leitfaden zeigt, wie man Preis- und Kreditoreninformationen einer Bestellanforderung von einem Angebotsanforderungsprozess aus hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc232-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="bc232-105">Das Beispiel, das in diesem Leitfaden gezeigt wird, kann in dem USMF-Demodatenunternehmen verwendet werden, und Sie müssen als Administrator angemeldet sein, um alle Schritte abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bc232-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="bc232-106">Die Aufgaben in diesem Leitfaden würden gewöhnlich von Prokuristen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bc232-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="bc232-107">Eine Anforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="bc232-107">Create a requisition</span></span>
1. <span data-ttu-id="bc232-108">Wechseln Sie zu "Beschaffung" >"Bestellanforderungen" > "Von mir vorbereitete Bestellanforderungen".</span><span class="sxs-lookup"><span data-stu-id="bc232-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="bc232-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="bc232-109">Click New.</span></span>
3. <span data-ttu-id="bc232-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bc232-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="bc232-111">Geben Sie im Feld "Angefordertes Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="bc232-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="bc232-112">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="bc232-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="bc232-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bc232-113">Click OK.</span></span>
7. <span data-ttu-id="bc232-114">Geben Sie im Feld 'Grund' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="bc232-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="bc232-115">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="bc232-115">Click Add line.</span></span>
9. <span data-ttu-id="bc232-116">Wählen Sie im Feld "Beschaffungskategorie" eine Kategorie im Baum aus, und klicken Sie dann auf O.K.</span><span class="sxs-lookup"><span data-stu-id="bc232-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="bc232-117">Geben Sie im Feld "Produktname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bc232-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="bc232-118">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="bc232-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="bc232-119">Geben Sie im Feld 'Einheit' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="bc232-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="bc232-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="bc232-120">Click Save.</span></span>
14. <span data-ttu-id="bc232-121">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf ''.</span><span class="sxs-lookup"><span data-stu-id="bc232-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="bc232-122">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="bc232-122">Click Submit.</span></span>
16. <span data-ttu-id="bc232-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc232-123">Close the page.</span></span>
17. <span data-ttu-id="bc232-124">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="bc232-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="bc232-125">Eine Workflowaufgabe neu zuweisen</span><span class="sxs-lookup"><span data-stu-id="bc232-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="bc232-126">Die folgende Aufgabe besteht darin, eine Angebotsanforderung zu erstellen, um Angebote von Lieferanten für das Produkt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bc232-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="bc232-127">In den USMF-Demodaten wird der Anforderungsworkflow mit einer Regel eingerichtet, damit, wenn ein Kreditor nicht ausgewählt ist oder der Einzelpreis für eine Position 0 ist, eine Aufgabe einer spezifischen Arbeitskraft zugewiesen wird, um eine Angebotsanforderung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc232-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="bc232-128">Um mit diesem Leitfaden fortzufahren, müssen Sie diese Aufgabe einem anderen Benutzer (Sie selbst) erneut zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bc232-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="bc232-129">Sie können dies nur tun, wenn Sie als "Administrator" angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="bc232-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="bc232-130">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf ''.</span><span class="sxs-lookup"><span data-stu-id="bc232-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="bc232-131">Klicken Sie auf "Verlauf anzeigen".</span><span class="sxs-lookup"><span data-stu-id="bc232-131">Click View history.</span></span>
3. <span data-ttu-id="bc232-132">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc232-132">Refresh the page.</span></span>
4. <span data-ttu-id="bc232-133">Erweitern Sie den Abschnitt "Verfolgungsdetails".</span><span class="sxs-lookup"><span data-stu-id="bc232-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="bc232-134">Im Baum wählen Sie 'die Position aus, die mit "Positionsworkflow aktiviert am"' beginnt.</span><span class="sxs-lookup"><span data-stu-id="bc232-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="bc232-135">Klicken Sie auf "Workflowdetails anzeigen".</span><span class="sxs-lookup"><span data-stu-id="bc232-135">Click View workflow details.</span></span>
7. <span data-ttu-id="bc232-136">Erweitern Sie den Abschnitt "Arbeitsaufgaben".</span><span class="sxs-lookup"><span data-stu-id="bc232-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="bc232-137">Klicken Sie auf "Neu zuweisen".</span><span class="sxs-lookup"><span data-stu-id="bc232-137">Click Reassign.</span></span>
9. <span data-ttu-id="bc232-138">Wählen Sie im Feld "Benutzer" die Option "Administrator" aus.</span><span class="sxs-lookup"><span data-stu-id="bc232-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="bc232-139">Klicken Sie auf "Neu zuweisen".</span><span class="sxs-lookup"><span data-stu-id="bc232-139">Click Reassign.</span></span>
11. <span data-ttu-id="bc232-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc232-140">Close the page.</span></span>
12. <span data-ttu-id="bc232-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc232-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="bc232-142">Eine Angebotsanforderung erstellen</span><span class="sxs-lookup"><span data-stu-id="bc232-142">Create an RFQ</span></span>
1. <span data-ttu-id="bc232-143">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc232-143">Refresh the page.</span></span>
2. <span data-ttu-id="bc232-144">Klicken Sie auf "Angebotsanforderung".</span><span class="sxs-lookup"><span data-stu-id="bc232-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="bc232-145">Wählen Sie im Feld "Kaufende juristische Person" die Option "USMF" aus.</span><span class="sxs-lookup"><span data-stu-id="bc232-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="bc232-146">Sie müssen dieselbe juristische Person auswählen, die auf der Anforderungsposition ist.</span><span class="sxs-lookup"><span data-stu-id="bc232-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="bc232-147">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="bc232-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bc232-148">Wenn Sie mehrere Positionen auf Ihrer Bestellanforderung hatten, wählen Sie alle die Positionen aus, die Sie zur Angebotsanforderung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="bc232-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="bc232-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bc232-149">Click OK.</span></span>
6. <span data-ttu-id="bc232-150">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc232-150">Refresh the page.</span></span>
7. <span data-ttu-id="bc232-151">Öffnen Sie die Infobox und erweitern Sie dann den Abschnitt "Zugehörige Dokumente".</span><span class="sxs-lookup"><span data-stu-id="bc232-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="bc232-152">Sie haben möglicherweise bereits die Infobox offen.</span><span class="sxs-lookup"><span data-stu-id="bc232-152">You may already have the FactBox open.</span></span> <span data-ttu-id="bc232-153">Suchen Sie nach dem Symbol, auf der sich ein Pfeil befindet. Es befindet sich rechts von den Umschaltflächen "Positionen/Header".</span><span class="sxs-lookup"><span data-stu-id="bc232-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="bc232-154">Wenn der Pfeil nach rechts zeigt, ist die Infobox bereits offen.</span><span class="sxs-lookup"><span data-stu-id="bc232-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="bc232-155">Wenn der Pfeil nach links zeigt, klicken Sie auf ihn, um die Infobox zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bc232-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="bc232-156">Klicken Sie auf den Link im Feld "Angebotsanforderung", um die Angebotsanforderung zu öffnen, die soeben erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc232-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="bc232-157">Klicken Sie auf "Kopfzeile".</span><span class="sxs-lookup"><span data-stu-id="bc232-157">Click Header.</span></span>
10. <span data-ttu-id="bc232-158">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bc232-158">Click Add.</span></span>
11. <span data-ttu-id="bc232-159">Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="bc232-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="bc232-160">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bc232-160">Click Add.</span></span>
13. <span data-ttu-id="bc232-161">Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="bc232-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="bc232-162">Klicken Sie auf Senden.</span><span class="sxs-lookup"><span data-stu-id="bc232-162">Click Send.</span></span>
15. <span data-ttu-id="bc232-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bc232-163">Click OK.</span></span>
16. <span data-ttu-id="bc232-164">Klicken Sie auf "Antwort eingeben".</span><span class="sxs-lookup"><span data-stu-id="bc232-164">Click Enter reply.</span></span>
17. <span data-ttu-id="bc232-165">Klicken Sie im Aktivitätsbereich auf "Antworten".</span><span class="sxs-lookup"><span data-stu-id="bc232-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="bc232-166">Klicken Sie auf "Daten in Antwort kopieren".</span><span class="sxs-lookup"><span data-stu-id="bc232-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="bc232-167">Dies kopiert Daten, wie die Menge und die Datumsangaben, von der Angebotsanforderung zur Antwort.</span><span class="sxs-lookup"><span data-stu-id="bc232-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="bc232-168">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="bc232-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="bc232-169">Dies ist der Preis, den Sie vom Kreditor empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="bc232-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="bc232-170">Sie sollten auch zusätzliche Information vom Kreditor eingeben.</span><span class="sxs-lookup"><span data-stu-id="bc232-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="bc232-171">Klicken Sie auf "Annehmen".</span><span class="sxs-lookup"><span data-stu-id="bc232-171">Click Accept.</span></span>
21. <span data-ttu-id="bc232-172">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="bc232-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="bc232-173">Überprüfen Sie, dass Kreditor und Preis an die Anforderung übertragen worden sind</span><span class="sxs-lookup"><span data-stu-id="bc232-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="bc232-174">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc232-174">Close the page.</span></span>
2. <span data-ttu-id="bc232-175">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="bc232-175">Click Lines.</span></span>
3. <span data-ttu-id="bc232-176">Klicken Sie auf "Zugehörige Informationen".</span><span class="sxs-lookup"><span data-stu-id="bc232-176">Click Related information.</span></span>
4. <span data-ttu-id="bc232-177">Klicken Sie auf "Bestellanforderung".</span><span class="sxs-lookup"><span data-stu-id="bc232-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="bc232-178">Wählen Sie die Position aus, die zur Angebotsanforderung übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="bc232-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="bc232-179">Überprüfen Sie, dass der Preis und der Kreditor zur Anforderung kopiert worden sind.</span><span class="sxs-lookup"><span data-stu-id="bc232-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="bc232-180">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf ''.</span><span class="sxs-lookup"><span data-stu-id="bc232-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="bc232-181">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="bc232-181">Click Complete.</span></span>
8. <span data-ttu-id="bc232-182">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc232-182">Close the page.</span></span>
9. <span data-ttu-id="bc232-183">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="bc232-183">Click Complete.</span></span>


