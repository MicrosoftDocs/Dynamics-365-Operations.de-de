---
title: Umsatzprovisionen registrieren
description: Dieses Verfahren zeigt Ihnen, wie Verkaufsprovisionen berechnet und registriert werden.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355149"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="ceb48-103">Umsatzprovisionen registrieren</span><span class="sxs-lookup"><span data-stu-id="ceb48-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ceb48-104">Dieses Verfahren zeigt Ihnen, wie Verkaufsprovisionen berechnet und registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ceb48-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="ceb48-105">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="ceb48-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="ceb48-106">Bevor Sie mit diesem Leitfaden beginnen, führen Sie den Leitfaden "Vertriebsprovisionsregeln einrichten" aus, um sicherzustellen, das Sie alle erforderlichen Provisionsberechnungseinstellungen haben.</span><span class="sxs-lookup"><span data-stu-id="ceb48-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="ceb48-107">Beachten Sie den Debitor und die Artikelnummern, die Sie für den Provisionsprozess ausgewählt haben und verwenden Sie diese, wenn Sie gebeten werden, einen Auftrag in diesem Leitfaden zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ceb48-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="ceb48-108">Fakturieren eines Auftrag, der einen Verkäufer für eine Provision qualifiziert</span><span class="sxs-lookup"><span data-stu-id="ceb48-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="ceb48-109">Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="ceb48-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="ceb48-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ceb48-110">Click New.</span></span>
3. <span data-ttu-id="ceb48-111">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ceb48-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ceb48-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ceb48-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ceb48-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ceb48-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ceb48-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ceb48-114">Click OK.</span></span>
7. <span data-ttu-id="ceb48-115">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="ceb48-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="ceb48-116">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="ceb48-116">Click Change view.</span></span>
9. <span data-ttu-id="ceb48-117">Klicken Sie auf die Kopfzeilenansicht.</span><span class="sxs-lookup"><span data-stu-id="ceb48-117">Click Header view.</span></span>
10. <span data-ttu-id="ceb48-118">Erweitern Sie den Abschnitt 'Einstellungen'.</span><span class="sxs-lookup"><span data-stu-id="ceb48-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="ceb48-119">Der Wert im Feld "Verkaufsgruppe" stellt eine Gruppe mit einem oder mehreren Verkäufern die ihr zugewiesen wurden dar.</span><span class="sxs-lookup"><span data-stu-id="ceb48-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="ceb48-120">Die Personen in der Gruppe sind die, die Provisionen erhalten, wenn der Auftrag fakturiert wird, entsprechend der vordefinierten Sätze und der Verteilung.</span><span class="sxs-lookup"><span data-stu-id="ceb48-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="ceb48-121">Der Wert wird aus der Debitorenkarte kopiert, Sie können ihn jedoch ändern.</span><span class="sxs-lookup"><span data-stu-id="ceb48-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="ceb48-122">Die Verkaufsgruppe wird auch in die Auftragsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="ceb48-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="ceb48-123">Sie können diese ändern, sodass sie von der im Kopf und/oder den Positionen variieren kann.</span><span class="sxs-lookup"><span data-stu-id="ceb48-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="ceb48-124">Der Wert im Feld "Provisionsgruppe" ist eine Gruppe, die Sie für einen oder mehrere Debitoren mit dem Zweck der Nachverfolgungs von Provisionen erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ceb48-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="ceb48-125">Der Wert wird aus der Debitorenkarte kopiert, Sie können ihn jedoch ändern.</span><span class="sxs-lookup"><span data-stu-id="ceb48-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="ceb48-126">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="ceb48-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="ceb48-127">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="ceb48-127">Click Change view.</span></span>
13. <span data-ttu-id="ceb48-128">Klicken Sie auf Positionsansicht.</span><span class="sxs-lookup"><span data-stu-id="ceb48-128">Click Line view.</span></span>
14. <span data-ttu-id="ceb48-129">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ceb48-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ceb48-130">Wählen Sie in der Liste den Artikel aus, für den Sie Provisionen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="ceb48-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="ceb48-131">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ceb48-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ceb48-132">Beachten Sie den Nettobetrag der Position.</span><span class="sxs-lookup"><span data-stu-id="ceb48-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="ceb48-133">Er stellt den Umsatzerlös dar, der in diesem Beispiel die Grundlage für Provisionsberechnung ist.</span><span class="sxs-lookup"><span data-stu-id="ceb48-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="ceb48-134">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ceb48-134">Click Save.</span></span>
18. <span data-ttu-id="ceb48-135">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="ceb48-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="ceb48-136">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="ceb48-136">Click Invoice.</span></span>
20. <span data-ttu-id="ceb48-137">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="ceb48-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="ceb48-138">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="ceb48-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="ceb48-139">Wählen Sie "Ja" im Feld "Buchung" aus.</span><span class="sxs-lookup"><span data-stu-id="ceb48-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="ceb48-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ceb48-140">Click OK.</span></span>
24. <span data-ttu-id="ceb48-141">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ceb48-141">Click OK.</span></span>
    * <span data-ttu-id="ceb48-142">Es kann eine Minute dauern die Transaktion zu buchen.</span><span class="sxs-lookup"><span data-stu-id="ceb48-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="ceb48-143">Geben Sie der Verarbeitung ausreichend Zeit und schließen Sie nicht die Seite.</span><span class="sxs-lookup"><span data-stu-id="ceb48-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="ceb48-144">Überprüfen der erfassten Verkaufsprovisionen</span><span class="sxs-lookup"><span data-stu-id="ceb48-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="ceb48-145">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="ceb48-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="ceb48-146">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="ceb48-146">Click Invoice.</span></span>
3. <span data-ttu-id="ceb48-147">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="ceb48-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="ceb48-148">Klicken Sie auf "Provisionstransaktionen".</span><span class="sxs-lookup"><span data-stu-id="ceb48-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="ceb48-149">Die Registerkarte "Überblick" zeigt Positionen an, welche die provisionsfälligen Beträge für die Verkäufer darstellen, die dem fakturierten Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ceb48-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="ceb48-150">Sehen wir uns die Einzelheiten an.</span><span class="sxs-lookup"><span data-stu-id="ceb48-150">Let's review the details.</span></span>     
    * <span data-ttu-id="ceb48-151">Wenn Sie "Vertriebsprovisionsregeln einrichten" verwendet haben, um die Provisionsverkaufsgruppe einzurichten, gibt es zwei Verkäufer für Verkaufsprovisionen und die Provision wird gleichmäßig zwischen ihnen geteilt.</span><span class="sxs-lookup"><span data-stu-id="ceb48-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="ceb48-152">In diesem Beispiel wird der Gesamtbetrag der Provision als Prozentsatz des Umsatzerlöse berechnet (der Nettobetrag der Auftragsposition).</span><span class="sxs-lookup"><span data-stu-id="ceb48-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="ceb48-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ceb48-153">Close the page.</span></span>
6. <span data-ttu-id="ceb48-154">Klicken Sie auf Beleg.</span><span class="sxs-lookup"><span data-stu-id="ceb48-154">Click Voucher.</span></span>
    * <span data-ttu-id="ceb48-155">Sie können die Belegbuchungen für die Provisionsbeträge, die für die vordefinierten Provisionsausgaben gebucht werden, anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ceb48-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

