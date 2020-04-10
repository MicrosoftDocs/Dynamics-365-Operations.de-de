---
title: Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben
description: In diesem Thema wird beschrieben, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd6de42dda650d42d703e905f8d48f73b9e4afd6
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143810"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="8f4ac-103">Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben</span><span class="sxs-lookup"><span data-stu-id="8f4ac-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f4ac-104">In diesem Thema wird beschrieben, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="8f4ac-105">Nehmen Sie anschließend den Rechnungspool, um die Rechnung mit einer Bestellung abzugleichen und die Ausgaben auf der Kreditorenrechnungsseite abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="8f4ac-106">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="8f4ac-106">Create a purchase order</span></span>
1. <span data-ttu-id="8f4ac-107">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Bestellungen > Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="8f4ac-108">Klicken Sie auf **Neu** , um eine neue Bestellung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="8f4ac-109">Wählen Sie im Feld **Kreditorenkonto** einen Lieferant aus der Dropdownliste, um eine Option auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="8f4ac-110">Wählen Sie z. B. Händler **1001** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="8f4ac-111">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-111">Select **OK**.</span></span>
5. <span data-ttu-id="8f4ac-112">Wählen Sie im Feld **Artikelnummer** die Services-Artikelnummer aus der Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="8f4ac-113">Wählen Sie z. B. **S0001** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-113">For example, select **S0001**.</span></span> <span data-ttu-id="8f4ac-114">Der Nettobetrag ist 75,00.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-114">The net amount is 75.00.</span></span>  <span data-ttu-id="8f4ac-115">Der ist der Betrag, den wir auf der Rechnung erwarten.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="8f4ac-116">Wählen Sie im Aktivitätsbereich **Einkauf** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="8f4ac-117">Wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="8f4ac-118">Erstellen und buchen und fakturieren</span><span class="sxs-lookup"><span data-stu-id="8f4ac-118">Create and post and invoice</span></span>
1. <span data-ttu-id="8f4ac-119">Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="8f4ac-120">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-120">Select **New**.</span></span>
3. <span data-ttu-id="8f4ac-121">Öffnen Sie die Suche, um den Namen des Rechnungsregisters auswählen, das Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="8f4ac-122">Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="8f4ac-123">Klicken Sie auf **Positionen**, um das Register zu öffnen und Ausgabenpositionen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="8f4ac-124">Wählen Sie in der Suche einen Händler aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="8f4ac-125">Wählen Sie z. B. Händler **1001** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="8f4ac-126">Geben Sie im Feld **Rechnung** die Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="8f4ac-127">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="8f4ac-128">Geben Sie im Feld **Kredit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="8f4ac-129">Öffnen Sie im Feld **Bestellung** die Dropdownliste, um die Bestellung auszuwählen, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="8f4ac-130">Markieren Sie im Feld **Genehmigt von** einen Genehmiger in der Dropdownliste und klicken Sie **Auswählen**, um diesen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="8f4ac-131">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="8f4ac-132">Öffnen einer Rechnung aus dem Pool und Abgleichen mit einer Bestellung, um den Rechnungsprozess abzuschließen</span><span class="sxs-lookup"><span data-stu-id="8f4ac-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="8f4ac-133">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Rechnungen > Rechnungspool**.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="8f4ac-134">Klicken Sie auf **Bestellung**, um eine Kreditorenrechnung aus der Rechnung im Pool zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="8f4ac-135">Wählen Sie die Rechnung aus, die Sie prüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="8f4ac-136">Klicken Sie auf **Abgleichstatus**, um den Abgleich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="8f4ac-137">Wählen Sie im Aktivitätsbereich **Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="8f4ac-138">Wählen Sie **Ansicht wechseln** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-138">Select **Change view**.</span></span>
7. <span data-ttu-id="8f4ac-139">Wählen SIe **Rasteransicht** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="8f4ac-140">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-140">Select **Post**.</span></span>
9. <span data-ttu-id="8f4ac-141">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-141">Close the form.</span></span>
10. <span data-ttu-id="8f4ac-142">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Kreditoren > Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="8f4ac-143">Wählen Sie den Händler aus, der auf der Bestellung war.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="8f4ac-144">Wählen Sie z. B. Händler **1001** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="8f4ac-145">Wählen Sie im Aktivitätsbereich **Kreditoren** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="8f4ac-146">Wählen Sie **Buchungen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="8f4ac-147">Wählen Sie die Rechnung aus, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-147">Select the invoice that you created.</span></span> <span data-ttu-id="8f4ac-148">Die Rechnungsbuchabgrenzung wurde storniert und auf das entsprechende Ausgabenkonto gebucht.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

