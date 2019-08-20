---
title: Auftragsrechnungen erstellen
description: Dieses Aufgabenhandbuch beschreibt, wie ein Auftrag fakturiert wird, einschließlich des Zusammenführens von Rechnungen sowie der Stapelverarbeitung.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba8e0f02f2d1eb12cecc2c434fbca1e198cddbe9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842952"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="4d963-103">Auftragsrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="4d963-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d963-104">Dieses Aufgabenhandbuch beschreibt, wie ein Auftrag fakturiert wird, einschließlich des Zusammenführens von Rechnungen sowie der Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="4d963-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="4d963-105">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d963-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="4d963-106">Eine Rechnung von einem Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="4d963-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="4d963-107">Wechseln Sie zu "Debitoren" > "Aufträge" > "Versendete, jedoch nicht fakturierte Aufträge".</span><span class="sxs-lookup"><span data-stu-id="4d963-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="4d963-108">Wählen Sie einen Auftrag in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="4d963-109">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="4d963-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="4d963-110">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="4d963-110">Click Invoice.</span></span>
    * <span data-ttu-id="4d963-111">Beachten Sie, dass diesem Auftrag mehrere Lieferscheine zugeordneten sind.</span><span class="sxs-lookup"><span data-stu-id="4d963-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="4d963-112">Darin wird nur das Wort <multiple> anstelle der Lieferscheinnummer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d963-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="4d963-113">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="4d963-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="4d963-114">Buchen muss auf "Ja" festgelegt werden, um die Rechnung zu buchen.</span><span class="sxs-lookup"><span data-stu-id="4d963-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="4d963-115">Sie können auch das Buchen ausschalten und die Rechnung nur drucken.</span><span class="sxs-lookup"><span data-stu-id="4d963-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="4d963-116">Sie können jedoch das gleiche Ergebnis erreichen, indem Sie eine Proforma-Rechnung anstelle einer Rechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d963-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="4d963-117">Diese Option wird für Stapelverarbeitungsaufträge genutzt.</span><span class="sxs-lookup"><span data-stu-id="4d963-117">This option is used for batch jobs.</span></span> <span data-ttu-id="4d963-118">Die Anfrage läuft, wenn der Batchauftrag ausgeführt wrid.</span><span class="sxs-lookup"><span data-stu-id="4d963-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="4d963-119">Wählen Sie im Feld "Drucken" die Option "Nach" aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="4d963-120">Wählen Sie "Ja" für "Rechnung drucken" aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="4d963-121">Die Druckverwaltung kann mehrere Kopien der Rechnung drucken und auch die Rechnung per E-Mail als PDF-Datei senden.</span><span class="sxs-lookup"><span data-stu-id="4d963-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="4d963-122">Wählen Sie im Feld "Chargen Drucken" die Option "Zusammenfassen" aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="4d963-123">Wählen Sie im Feld "Kreditlimit prüfen" die Option "Saldo" aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="4d963-124">Klicken Sie auf "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="4d963-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="4d963-125">Aufträge in einer einzelnen Rechnung kombinieren</span><span class="sxs-lookup"><span data-stu-id="4d963-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="4d963-126">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="4d963-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="4d963-127">Suchen Sie einen Debitoren, bei dem mehrere Rechnungen offen sind.</span><span class="sxs-lookup"><span data-stu-id="4d963-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="4d963-128">Wählen Sie einen offenen Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-128">Select an open sales order.</span></span>
4. <span data-ttu-id="4d963-129">Wählen Sie einen weiteren offenen Auftrag für denselben Debitoren aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="4d963-130">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="4d963-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="4d963-131">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="4d963-131">Click Invoice.</span></span>
7. <span data-ttu-id="4d963-132">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="4d963-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="4d963-133">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="4d963-134">Beachten Sie, dass zwei Rechnungen im Abschnitt "Übersicht" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4d963-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="4d963-135">Jetzt führen wir sie in einer einzelnen Rechnung zusammen.</span><span class="sxs-lookup"><span data-stu-id="4d963-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="4d963-136">Wählen Sie im Feld "Sammelaktualisierung für" die Option "Rechnungskonto" aus.</span><span class="sxs-lookup"><span data-stu-id="4d963-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="4d963-137">Klicken Sie auf "Anordnen", um die Aufträge in einer einzelnen Rechnung zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="4d963-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="4d963-138">Die beiden Aufträge werden nun in einer einzelnen Rechnung zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="4d963-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="4d963-139">Klicken Sie auf "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="4d963-139">Click Cancel.</span></span>
12. <span data-ttu-id="4d963-140">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="4d963-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="4d963-141">Rechnungen in einer Charge buchen</span><span class="sxs-lookup"><span data-stu-id="4d963-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="4d963-142">Wechseln Sie zu "Debitoren" > "Rechnungen" > "Chargenrechnungsstellung" > "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="4d963-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="4d963-143">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="4d963-143">Click Select.</span></span>
3. <span data-ttu-id="4d963-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4d963-144">Click OK.</span></span>
4. <span data-ttu-id="4d963-145">Klicken Sie auf "Charge".</span><span class="sxs-lookup"><span data-stu-id="4d963-145">Click Batch.</span></span>
5. <span data-ttu-id="4d963-146">Klicken auf "Ja", um die Stapelverarbeitung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4d963-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="4d963-147">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="4d963-147">Click Recurrence.</span></span>
7. <span data-ttu-id="4d963-148">Tage auswählen</span><span class="sxs-lookup"><span data-stu-id="4d963-148">Select Days</span></span>
8. <span data-ttu-id="4d963-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4d963-149">Click OK.</span></span>
9. <span data-ttu-id="4d963-150">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4d963-150">Click OK.</span></span>
10. <span data-ttu-id="4d963-151">Klicken Sie auf "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="4d963-151">Click Cancel.</span></span>
11. <span data-ttu-id="4d963-152">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="4d963-152">Click Yes.</span></span>

