---
title: Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben
description: In diesem Thema wird beschrieben, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9c54f610e45d288ed58fd209d290d73bfe1ff2f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820664"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="4b090-103">Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben</span><span class="sxs-lookup"><span data-stu-id="4b090-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b090-104">In diesem Thema wird beschrieben, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b090-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="4b090-105">Nehmen Sie anschließend den Rechnungspool, um die Rechnung mit einer Bestellung abzugleichen und die Ausgaben auf der Kreditorenrechnungsseite abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4b090-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="4b090-106">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="4b090-106">Create a purchase order</span></span>
1. <span data-ttu-id="4b090-107">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Bestellungen > Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="4b090-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="4b090-108">Klicken Sie auf **Neu** , um eine neue Bestellung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b090-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="4b090-109">Wählen Sie im Feld **Kreditorenkonto** einen Lieferant aus der Dropdownliste, um eine Option auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4b090-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="4b090-110">Wählen Sie z. B. Händler **1001** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="4b090-111">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b090-111">Select **OK**.</span></span>
5. <span data-ttu-id="4b090-112">Wählen Sie im Feld **Artikelnummer** die Services-Artikelnummer aus der Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="4b090-113">Wählen Sie z. B. **S0001** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-113">For example, select **S0001**.</span></span> <span data-ttu-id="4b090-114">Der Nettobetrag ist 75,00.</span><span class="sxs-lookup"><span data-stu-id="4b090-114">The net amount is 75.00.</span></span>  <span data-ttu-id="4b090-115">Der ist der Betrag, den wir auf der Rechnung erwarten.</span><span class="sxs-lookup"><span data-stu-id="4b090-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="4b090-116">Wählen Sie im Aktivitätsbereich **Einkauf** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="4b090-117">Wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="4b090-118">Erstellen und buchen und fakturieren</span><span class="sxs-lookup"><span data-stu-id="4b090-118">Create and post and invoice</span></span>
1. <span data-ttu-id="4b090-119">Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="4b090-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="4b090-120">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-120">Select **New**.</span></span>
3. <span data-ttu-id="4b090-121">Öffnen Sie die Suche, um den Namen des Rechnungsregisters auswählen, das Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4b090-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="4b090-122">Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="4b090-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="4b090-123">Klicken Sie auf **Positionen**, um das Register zu öffnen und Ausgabenpositionen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="4b090-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="4b090-124">Wählen Sie in der Suche einen Händler aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="4b090-125">Wählen Sie z. B. Händler **1001** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="4b090-126">Geben Sie im Feld **Rechnung** die Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="4b090-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="4b090-127">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4b090-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="4b090-128">Geben Sie im Feld **Kredit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4b090-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="4b090-129">Öffnen Sie im Feld **Bestellung** die Dropdownliste, um die Bestellung auszuwählen, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4b090-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="4b090-130">Markieren Sie im Feld **Genehmigt von** einen Genehmiger in der Dropdownliste und klicken Sie **Auswählen**, um diesen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4b090-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="4b090-131">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="4b090-132">Öffnen einer Rechnung aus dem Pool und Abgleichen mit einer Bestellung, um den Rechnungsprozess abzuschließen</span><span class="sxs-lookup"><span data-stu-id="4b090-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="4b090-133">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Rechnungen > Rechnungspool**.</span><span class="sxs-lookup"><span data-stu-id="4b090-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="4b090-134">Klicken Sie auf **Bestellung**, um eine Kreditorenrechnung aus der Rechnung im Pool zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b090-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="4b090-135">Wählen Sie die Rechnung aus, die Sie prüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="4b090-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="4b090-136">Klicken Sie auf **Abgleichstatus**, um den Abgleich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4b090-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="4b090-137">Wählen Sie im Aktivitätsbereich **Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="4b090-138">Wählen Sie **Ansicht wechseln** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-138">Select **Change view**.</span></span>
7. <span data-ttu-id="4b090-139">Wählen SIe **Rasteransicht** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="4b090-140">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-140">Select **Post**.</span></span>
9. <span data-ttu-id="4b090-141">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="4b090-141">Close the form.</span></span>
10. <span data-ttu-id="4b090-142">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Kreditoren > Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="4b090-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="4b090-143">Wählen Sie den Händler aus, der auf der Bestellung war.</span><span class="sxs-lookup"><span data-stu-id="4b090-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="4b090-144">Wählen Sie z. B. Händler **1001** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="4b090-145">Wählen Sie im Aktivitätsbereich **Kreditoren** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="4b090-146">Wählen Sie **Buchungen** aus.</span><span class="sxs-lookup"><span data-stu-id="4b090-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="4b090-147">Wählen Sie die Rechnung aus, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4b090-147">Select the invoice that you created.</span></span> <span data-ttu-id="4b090-148">Die Rechnungsbuchabgrenzung wurde storniert und auf das entsprechende Ausgabenkonto gebucht.</span><span class="sxs-lookup"><span data-stu-id="4b090-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]