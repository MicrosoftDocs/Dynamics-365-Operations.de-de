---
title: Umsatzprovisionen registrieren
description: In diesem Thema wird erläutert, wie Verkaufsprovisionen berechnet und registriert werden.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82c8dc2f284923b5583bf983413a015b9ece8252
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205928"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="b4724-103">Umsatzprovisionen registrieren</span><span class="sxs-lookup"><span data-stu-id="b4724-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4724-104">In diesem Thema wird erläutert, wie Verkaufsprovisionen berechnet und registriert werden.</span><span class="sxs-lookup"><span data-stu-id="b4724-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="b4724-105">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4724-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="b4724-106">Bevor Sie mit diesem Leitfaden beginnen, führen Sie den Leitfaden "Vertriebsprovisionsregeln einrichten" aus, um sicherzustellen, das Sie alle erforderlichen Provisionsberechnungseinstellungen haben.</span><span class="sxs-lookup"><span data-stu-id="b4724-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="b4724-107">Beachten Sie den Debitor und die Artikelnummern, die Sie für den Provisionsprozess ausgewählt haben und verwenden Sie diese, wenn Sie gebeten werden, einen Auftrag in diesem Leitfaden zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b4724-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="b4724-108">Fakturieren eines Auftrag, der einen Verkäufer für eine Provision qualifiziert</span><span class="sxs-lookup"><span data-stu-id="b4724-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="b4724-109">Gehen Sie im Navigationsbereich zu **Module > Vertrieb und Marketing > Kundenaufträge > Alle Kundenaufträge**.</span><span class="sxs-lookup"><span data-stu-id="b4724-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="b4724-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b4724-110">Select **New**.</span></span>
3. <span data-ttu-id="b4724-111">Wählen Sie im Feld **Kundenkonto** den gewünschten Datensatz aus dem Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="b4724-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="b4724-112">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4724-112">Select **OK**.</span></span>
5. <span data-ttu-id="b4724-113">Wählen Sie im Aktivitätsbereich **Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="b4724-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="b4724-114">Wählen Sie **Ansicht ändern**.</span><span class="sxs-lookup"><span data-stu-id="b4724-114">Select **Change view**.</span></span>
7. <span data-ttu-id="b4724-115">Wählen Sie **Kopfansicht**.</span><span class="sxs-lookup"><span data-stu-id="b4724-115">Select **Header view**.</span></span>
8. <span data-ttu-id="b4724-116">Erweitern Sie den Abschnitt **Einrichtung**.</span><span class="sxs-lookup"><span data-stu-id="b4724-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="b4724-117">Der Wert im Feld **Vertriebsgruppe** repräsentiert eine Gruppe, der ein oder mehrere Außendienstmitarbeiter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4724-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="b4724-118">Die Personen in der Gruppe sind die, die Provisionen erhalten, wenn der Auftrag fakturiert wird, entsprechend der vordefinierten Sätze und der Verteilung.</span><span class="sxs-lookup"><span data-stu-id="b4724-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="b4724-119">Der Wert wird aus der Debitorenkarte kopiert, Sie können ihn jedoch ändern.</span><span class="sxs-lookup"><span data-stu-id="b4724-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="b4724-120">Die Verkaufsgruppe wird auch in die Auftragsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="b4724-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="b4724-121">Sie können diese ändern, sodass sie von der im Kopf und/oder den Positionen variieren kann.</span><span class="sxs-lookup"><span data-stu-id="b4724-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="b4724-122">Der Wert im Feld **Provisionsgruppe** repräsentiert eine Gruppe, die Sie für einen oder mehrere Kunden angelegt haben, um Provisionen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="b4724-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="b4724-123">Der Wert wird aus der Debitorenkarte kopiert, Sie können ihn jedoch ändern.</span><span class="sxs-lookup"><span data-stu-id="b4724-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="b4724-124">Wählen Sie im Aktivitätsbereich **Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="b4724-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="b4724-125">Wählen Sie **Ansicht ändern**.</span><span class="sxs-lookup"><span data-stu-id="b4724-125">Select **Change view**.</span></span>
11. <span data-ttu-id="b4724-126">Wählen Sie **Linienansicht**.</span><span class="sxs-lookup"><span data-stu-id="b4724-126">Select **Line view**.</span></span>
12. <span data-ttu-id="b4724-127">Wählen Sie im Dropdown-Menü des Feldes **Artikelnummer** den Punkt aus, den Sie für Provisionen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="b4724-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="b4724-128">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b4724-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="b4724-129">Beachten Sie den Nettobetrag der Position.</span><span class="sxs-lookup"><span data-stu-id="b4724-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="b4724-130">Er stellt den Umsatzerlös dar, der in diesem Beispiel die Grundlage für Provisionsberechnung ist.</span><span class="sxs-lookup"><span data-stu-id="b4724-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="b4724-131">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b4724-131">Select **Save**.</span></span>
15. <span data-ttu-id="b4724-132">Wählen Sie im Aktionsbereich **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="b4724-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="b4724-133">Wählen Sie **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="b4724-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="b4724-134">Erweitern Sie den Abschnitt **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="b4724-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="b4724-135">Wählen Sie im Feld **Menge** die Option **Alle** aus.</span><span class="sxs-lookup"><span data-stu-id="b4724-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="b4724-136">Wählen Sie **Ja** im Feld **Buchung**.</span><span class="sxs-lookup"><span data-stu-id="b4724-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="b4724-137">Wählen Sie **OK**, dann **OK** im nächsten Fenster.</span><span class="sxs-lookup"><span data-stu-id="b4724-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="b4724-138">Es kann eine Minute dauern die Transaktion zu buchen.</span><span class="sxs-lookup"><span data-stu-id="b4724-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="b4724-139">Geben Sie der Verarbeitung ausreichend Zeit und schließen Sie nicht die Seite.</span><span class="sxs-lookup"><span data-stu-id="b4724-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="b4724-140">Überprüfen der erfassten Verkaufsprovisionen</span><span class="sxs-lookup"><span data-stu-id="b4724-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="b4724-141">Wählen Sie im Aktionsbereich **Rechnung** und dann erneut **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="b4724-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="b4724-142">Wählen Sie im Aktionsbereich **Rechnung** und dann **Provisionstransaktionen**.</span><span class="sxs-lookup"><span data-stu-id="b4724-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="b4724-143">Auf der Registerkarte **Übersicht** werden Zeilen mit den Provisionsbeträgen angezeigt, die an Vertriebsmitarbeiter zu zahlen sind, die dem fakturierten Kundenauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4724-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="b4724-144">Sehen wir uns die Einzelheiten an.</span><span class="sxs-lookup"><span data-stu-id="b4724-144">Let's review the details.</span></span>  
    - <span data-ttu-id="b4724-145">Wenn Sie die Gruppe **Provisionsverkauf** mit dem Leitfaden „Provisionierungsregeln einrichten“ eingerichtet haben, gibt es zwei Verkäufer, die eine Provision erhalten, und die Provision wird zu gleichen Teilen auf sie aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="b4724-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="b4724-146">In diesem Beispiel wird der Gesamtbetrag der Provision als Prozentsatz des Umsatzerlöse berechnet (der Nettobetrag der Auftragsposition).</span><span class="sxs-lookup"><span data-stu-id="b4724-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="b4724-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b4724-147">Close the page.</span></span>
4. <span data-ttu-id="b4724-148">Wählen Sie **Beleg**.</span><span class="sxs-lookup"><span data-stu-id="b4724-148">Select **Voucher**.</span></span> <span data-ttu-id="b4724-149">Sie können die Belegbuchungen für die Provisionsbeträge, die für die vordefinierten Provisionsausgaben gebucht werden, anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b4724-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]