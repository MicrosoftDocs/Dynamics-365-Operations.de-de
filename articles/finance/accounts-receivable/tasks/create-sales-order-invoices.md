---
title: Auftragsrechnungen erstellen
description: Dieses Aufgabenhandbuch beschreibt, wie ein Auftrag fakturiert wird, einschließlich des Zusammenführens von Rechnungen sowie der Stapelverarbeitung.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d2e1dd552f529d09756c1ddeec39fc54a1f073a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241585"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="e6a3c-103">Auftragsrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="e6a3c-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6a3c-104">Dieses Aufgabenhandbuch beschreibt, wie ein Auftrag fakturiert wird, einschließlich des Zusammenführens von Rechnungen sowie der Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="e6a3c-105">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="e6a3c-106">Eine Rechnung von einem Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="e6a3c-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="e6a3c-107">Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Aufträge > Versendete, jedoch nicht fakturierte Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="e6a3c-108">Wählen Sie einen Auftrag in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="e6a3c-109">Klicken Sie im **Aktionsbereich** auf **Rechnung > Generieren > Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="e6a3c-110">Beachten Sie, dass diesem Auftrag mehrere Lieferscheine zugeordneten sind.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="e6a3c-111">Darin wird nur das Wort <multiple> anstelle der Lieferscheinnummer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="e6a3c-112">Erweitern Sie den Abschnitt **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="e6a3c-113">Buchen muss auf "Ja" festgelegt werden, um die Rechnung zu buchen.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="e6a3c-114">Sie können auch das Buchen ausschalten und die Rechnung nur drucken.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="e6a3c-115">Sie können jedoch das gleiche Ergebnis erreichen, indem Sie eine Proforma-Rechnung anstelle einer Rechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="e6a3c-116">Diese Option wird für Stapelverarbeitungsaufträge genutzt.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-116">This option is used for batch jobs.</span></span> <span data-ttu-id="e6a3c-117">Die Anfrage läuft, wenn der Batchauftrag ausgeführt wrid.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="e6a3c-118">Wählen Sie im Feld **Drucken** die Option „Nach“ aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="e6a3c-119">Wählen Sie **Ja** für **Rechnung drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="e6a3c-120">Die Druckverwaltung kann mehrere Kopien der Rechnung drucken und auch die Rechnung per E-Mail als PDF-Datei senden.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="e6a3c-121">Wählen Sie im Feld **Zuschläge drucken** die Option „Zusammenfassen“ aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="e6a3c-122">Wählen Sie im Feld **Kreditlimit prüfen** die Option „Saldo“ aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="e6a3c-123">Klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="e6a3c-124">Aufträge in einer einzelnen Rechnung kombinieren</span><span class="sxs-lookup"><span data-stu-id="e6a3c-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="e6a3c-125">Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Aufträge > Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="e6a3c-126">Suchen Sie einen Debitoren, bei dem mehrere Rechnungen offen sind.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="e6a3c-127">Wählen Sie mehrere offene Aufträge desselben Debitors aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="e6a3c-128">Klicken Sie im **Aktionsbereich** auf **Rechnung > Generieren > Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="e6a3c-129">Erweitern Sie den Abschnitt **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="e6a3c-130">Wählen Sie im Feld **Menge** die Option „Alle“ aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="e6a3c-131">Beachten Sie, dass zwei Rechnungen im Abschnitt "Übersicht" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="e6a3c-132">Jetzt führen wir sie in einer einzelnen Rechnung zusammen.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="e6a3c-133">Wählen Sie im Feld **Sammelaktualisierung für** die Option „Rechnungskonto“ aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="e6a3c-134">Klicken Sie auf **Anordnen**, um die Aufträge in einer einzelnen Rechnung zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="e6a3c-135">Die beiden Aufträge werden nun in einer einzelnen Rechnung zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="e6a3c-136">Klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="e6a3c-137">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="e6a3c-138">Rechnungen in einer Charge buchen</span><span class="sxs-lookup"><span data-stu-id="e6a3c-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="e6a3c-139">Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Rechnungen > Rechnungsstellung in Chargen > Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="e6a3c-140">Klicken Sie auf **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-140">Click **Select**.</span></span>
3. <span data-ttu-id="e6a3c-141">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-141">Click **OK**.</span></span>
4. <span data-ttu-id="e6a3c-142">Klicken Sie auf **Charge**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-142">Click **Batch**.</span></span>
5. <span data-ttu-id="e6a3c-143">Wählen Sie für **Stapelverarbeitung** die Option **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="e6a3c-144">Klicken Sie auf **Wiederholung**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="e6a3c-145">Wählen Sie **Tage** aus.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-145">Select **Days**.</span></span>
8. <span data-ttu-id="e6a3c-146">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-146">Click **OK**.</span></span>
9. <span data-ttu-id="e6a3c-147">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-147">Click **OK**.</span></span>
10. <span data-ttu-id="e6a3c-148">Klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="e6a3c-149">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]