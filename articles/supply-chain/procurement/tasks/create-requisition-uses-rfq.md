---
title: Eine Anforderung erstellen, die eine Angebotsanforderung verwendet
description: Dieses Thema erklärt, wie man Preis- und Kreditoreninformationen einer Bestellanforderung von einem Angebotsanforderungsprozess aus hinzufügt.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05ff98b5fd95fa345d344e54d9116c73434e5de5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018895"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="def02-103">Eine Anforderung erstellen, die eine Angebotsanforderung verwendet</span><span class="sxs-lookup"><span data-stu-id="def02-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="def02-104">Dieses Thema erklärt, wie man Preis- und Kreditoreninformationen einer Bestellanforderung von einem Angebotsanforderungsprozess aus hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="def02-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="def02-105">Das Beispiel, das in diesem Leitfaden gezeigt wird, kann in dem USMF-Demodatenunternehmen verwendet werden, und Sie müssen als Administrator angemeldet sein, um alle Schritte abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="def02-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="def02-106">Die Aufgaben in diesem Leitfaden würden gewöhnlich von Prokuristen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="def02-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="def02-107">Eine Anforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="def02-107">Create a requisition</span></span>
1. <span data-ttu-id="def02-108">Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Bestellanforderungen > Von mir vorbereitete Bestellanforderungen**.</span><span class="sxs-lookup"><span data-stu-id="def02-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="def02-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-109">Select **New**.</span></span>
3. <span data-ttu-id="def02-110">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="def02-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="def02-111">Geben Sie im Feld **Angefordertes Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="def02-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="def02-112">Geben Sie ein Datum in das Feld **Abschlussstichtag** ein.</span><span class="sxs-lookup"><span data-stu-id="def02-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="def02-113">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="def02-113">Select **OK**.</span></span>
7. <span data-ttu-id="def02-114">Geben Sie im Feld **Grund** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="def02-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="def02-115">Wählen Sie **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-115">Select **Add line**.</span></span>
9. <span data-ttu-id="def02-116">Wählen Sie im Feld **Beschaffungskategorie** eine Kategorie im Baum aus, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="def02-117">Geben Sie im Feld **Produktname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="def02-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="def02-118">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="def02-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="def02-119">Geben Sie im Feld **Einheit** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="def02-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="def02-120">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="def02-120">Select **Save**.</span></span>
14. <span data-ttu-id="def02-121">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="def02-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="def02-122">Wählen Sie **Senden**.</span><span class="sxs-lookup"><span data-stu-id="def02-122">Select **Submit**.</span></span>
16. <span data-ttu-id="def02-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="def02-123">Close the page.</span></span>
17. <span data-ttu-id="def02-124">Wählen Sie **Senden**.</span><span class="sxs-lookup"><span data-stu-id="def02-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="def02-125">Eine Workflowaufgabe neu zuweisen</span><span class="sxs-lookup"><span data-stu-id="def02-125">Reassign a workflow task</span></span>
<span data-ttu-id="def02-126">Die folgende Aufgabe besteht darin, eine Angebotsanforderung zu erstellen, um Angebote von Lieferanten für das Produkt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="def02-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="def02-127">In den USMF-Demodaten wird der Anforderungsworkflow mit einer Regel eingerichtet, damit, wenn ein Kreditor nicht ausgewählt ist oder der Einzelpreis für eine Position 0 ist, eine Aufgabe einer spezifischen Arbeitskraft zugewiesen wird, um eine Angebotsanforderung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="def02-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="def02-128">Um mit diesem Leitfaden fortzufahren, müssen Sie diese Aufgabe einem anderen Benutzer (Sie selbst) erneut zuweisen.</span><span class="sxs-lookup"><span data-stu-id="def02-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="def02-129">Sie können dies nur tun, wenn Sie als "Administrator" angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="def02-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="def02-130">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="def02-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="def02-131">Wählen Sie **Historie anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-131">Select **View history**.</span></span>
3. <span data-ttu-id="def02-132">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="def02-132">Refresh the page.</span></span>
4. <span data-ttu-id="def02-133">Erweitern Sie den Abschnitt **Verfolgungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="def02-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="def02-134">Im Baum wählen Sie dann die Position aus, die mit „Positionsworkflow aktiviert am“ beginnt.</span><span class="sxs-lookup"><span data-stu-id="def02-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="def02-135">Wählen Sie **Workflowdetails anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="def02-136">Erweitern Sie den Abschnitt **Arbeitsaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="def02-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="def02-137">Wählen Sie **Neu zuordnen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="def02-138">Wählen Sie im Feld **Benutzer** die Option **Administrator** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="def02-139">Wählen Sie **Neu zuordnen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="def02-140">Schließen Sie die beiden Seiten.</span><span class="sxs-lookup"><span data-stu-id="def02-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="def02-141">Eine Angebotsanforderung erstellen</span><span class="sxs-lookup"><span data-stu-id="def02-141">Create an RFQ</span></span>

1. <span data-ttu-id="def02-142">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="def02-142">Refresh the page.</span></span>
2. <span data-ttu-id="def02-143">Wählen Sie **Angebotsanforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="def02-144">Wählen Sie im Feld **Kaufende juristische Person** die Option **USMF** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="def02-145">Sie müssen dieselbe juristische Person auswählen, die auch auf der Anforderungsposition ist.</span><span class="sxs-lookup"><span data-stu-id="def02-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="def02-146">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="def02-146">In the list, mark the selected row.</span></span> <span data-ttu-id="def02-147">Wenn Sie mehrere Positionen auf Ihrer Bestellanforderung hatten, wählen Sie alle die Positionen aus, die Sie zur Angebotsanforderung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="def02-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="def02-148">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="def02-148">Select **OK**.</span></span>
6. <span data-ttu-id="def02-149">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="def02-149">Refresh the page.</span></span>
7. <span data-ttu-id="def02-150">Überprüfen Sie, ob die Infobox geöffnet ist, und erweitern Sie dann den Abschnitt **Zugehörige Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="def02-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="def02-151">Wählen Sie den Link im Feld **Angebotsanforderung** aus, um die Angebotsanforderung zu öffnen, die soeben erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="def02-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="def02-152">Wählen Sie **Kopfzeile** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-152">Select **Header**.</span></span>
10. <span data-ttu-id="def02-153">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-153">Select **Add**.</span></span>
11. <span data-ttu-id="def02-154">Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="def02-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="def02-155">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-155">Select **Add**.</span></span>
13. <span data-ttu-id="def02-156">Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="def02-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="def02-157">Wählen Sie **Senden** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-157">Select **Send**.</span></span>
15. <span data-ttu-id="def02-158">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="def02-158">Select **OK**.</span></span>
16. <span data-ttu-id="def02-159">Wählen Sie **Antwort eingeben** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="def02-160">Klicken Sie im Aktivitätsbereich auf **Antworten**.</span><span class="sxs-lookup"><span data-stu-id="def02-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="def02-161">Wählen Sie **Daten in Antwort kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="def02-162">Dies kopiert Daten, wie die Menge und die Datumsangaben, von der Angebotsanforderung zur Antwort.</span><span class="sxs-lookup"><span data-stu-id="def02-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="def02-163">Geben Sie im Feld **Einzelpreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="def02-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="def02-164">Dies ist der Preis, den Sie vom Lieferant empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="def02-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="def02-165">Sie sollten auch zusätzliche Information vom Kreditor eingeben.</span><span class="sxs-lookup"><span data-stu-id="def02-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="def02-166">Wählen Sie **Akzeptieren** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-166">Select **Accept**.</span></span>
21. <span data-ttu-id="def02-167">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="def02-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="def02-168">Überprüfen Sie, dass Kreditor und Preis an die Anforderung übertragen worden sind</span><span class="sxs-lookup"><span data-stu-id="def02-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="def02-169">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="def02-169">Close the page.</span></span>
2. <span data-ttu-id="def02-170">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-170">Select **Lines**.</span></span>
3. <span data-ttu-id="def02-171">Wählen Sie **Zugehörige Informationen** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-171">Select **Related information**.</span></span>
4. <span data-ttu-id="def02-172">Wählen Sie **Bestellanforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="def02-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="def02-173">Wählen Sie die Position aus, die zur Angebotsanforderung übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="def02-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="def02-174">Überprüfen Sie, dass der Preis und der Kreditor zur Anforderung kopiert worden sind.</span><span class="sxs-lookup"><span data-stu-id="def02-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="def02-175">Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="def02-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="def02-176">Wählen Sie „Abgeschlossen” aus.</span><span class="sxs-lookup"><span data-stu-id="def02-176">Select Complete.</span></span>
8. <span data-ttu-id="def02-177">Wählen Sie die Seite aus.</span><span class="sxs-lookup"><span data-stu-id="def02-177">Select the page.</span></span>
9. <span data-ttu-id="def02-178">Wählen Sie „Abgeschlossen” aus.</span><span class="sxs-lookup"><span data-stu-id="def02-178">Select Complete.</span></span>

