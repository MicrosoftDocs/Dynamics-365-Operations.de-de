---
title: Entscheidende Rechnungsdaten im Kreditorensystem mithilfe der Kreditorenrechnung
description: Dieser Aufgabenleitfaden unterstützt Sie beim Erstellen einer Kreditorenrechnung anhand einer Bestellung und beim Anzeigen der Ergebnisse des Abgleichs von Bestellung, Zugang und Rechnung (dreiseitiger Abgleich).
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7abae6d680d899a0294ad3c298a4b0264ba01d0b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835429"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="1c04f-103">Entscheidende Rechnungsdaten im Kreditorensystem mithilfe der Kreditorenrechnung</span><span class="sxs-lookup"><span data-stu-id="1c04f-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c04f-104">Dieser Aufgabenleitfaden unterstützt Sie beim Erstellen einer Kreditorenrechnung anhand einer Bestellung und beim Anzeigen der Ergebnisse des Abgleichs von Bestellung, Zugang und Rechnung (dreiseitiger Abgleich).</span><span class="sxs-lookup"><span data-stu-id="1c04f-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="1c04f-105">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="1c04f-105">Create a purchase order</span></span>
1. <span data-ttu-id="1c04f-106">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Bestellungen > Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="1c04f-107">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-107">Click **New**.</span></span>
3. <span data-ttu-id="1c04f-108">Klicken Sie im Feld **Kreditorenkonto** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1c04f-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1c04f-109">Suchen Sie einen Kreditor, um ihn auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1c04f-109">Find a vendor to select.</span></span> <span data-ttu-id="1c04f-110">Führen Sie beispielsweise einen Bildlauf nach unten zu US-104 durch.</span><span class="sxs-lookup"><span data-stu-id="1c04f-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="1c04f-111">Wählen Sie Kreditor US-104 aus.</span><span class="sxs-lookup"><span data-stu-id="1c04f-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="1c04f-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-112">Click **OK**.</span></span>
7. <span data-ttu-id="1c04f-113">Klicken Sie im Feld **Artikelnummer** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1c04f-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1c04f-114">Wählen Sie einen Lagerartikel aus.</span><span class="sxs-lookup"><span data-stu-id="1c04f-114">Select an inventory item.</span></span> <span data-ttu-id="1c04f-115">Wählen Sie beispielsweise die Artikelnummer 1000 aus.</span><span class="sxs-lookup"><span data-stu-id="1c04f-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="1c04f-116">Erweitern Sie das Inforegister **Positionsdetails**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="1c04f-117">Klicken Sie auf die Registerkarte **Einstellungen**. Sie können die Abgleichsrichtlinie überschreiben, um keinen Abgleich, einen zweiseitigen Abgleich oder einen dreiseitigen Abgleich zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c04f-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="1c04f-118">Klicken Sie im Aktionsbereich auf **Einkauf**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="1c04f-119">Klicken Sie auf **Bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="1c04f-120">Die Produkte empfangen</span><span class="sxs-lookup"><span data-stu-id="1c04f-120">Receive the products</span></span>
1. <span data-ttu-id="1c04f-121">Klicken Sie im Aktionsbereich auf **Empfangen**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="1c04f-122">Klicken Sie auf **Produktzugang**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="1c04f-123">Geben Sie im Feld **Produktzugang** die Produktzugangsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="1c04f-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="1c04f-124">Geben Sie beispielsweise "PR123" ein.</span><span class="sxs-lookup"><span data-stu-id="1c04f-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="1c04f-125">Klicken Sie auf **OK**, um den Produktzugang zu buchen.</span><span class="sxs-lookup"><span data-stu-id="1c04f-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="1c04f-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1c04f-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="1c04f-127">Eine Kreditorenrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="1c04f-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="1c04f-128">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Bestellungen > Empfangene, jedoch nicht fakturierte Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="1c04f-129">Wählen Sie die Bestellung aus, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="1c04f-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="1c04f-130">Klicken Sie im Aktivitätsbereich auf **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="1c04f-131">Klicken Sie auf **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="1c04f-132">Geben Sie im Feld **Nummer** die Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="1c04f-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="1c04f-133">Geben Sie im Feld **Rechnungsbeschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c04f-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="1c04f-134">Geben Sie im Feld **Rechnungsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="1c04f-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="1c04f-135">Geben Sie im Feld **Einzelpreis** die Zahl 1200 ein.</span><span class="sxs-lookup"><span data-stu-id="1c04f-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="1c04f-136">Klicken Sie auf **Position hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-136">Click **Add line**.</span></span>
10. <span data-ttu-id="1c04f-137">Klicken Sie im Feld **Artikelnummer** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1c04f-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="1c04f-138">Suchen Sie in der Liste die Installationsgebühr-Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="1c04f-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="1c04f-139">Beispielsweise S0001</span><span class="sxs-lookup"><span data-stu-id="1c04f-139">For example, S0001</span></span>
12. <span data-ttu-id="1c04f-140">Wählen Sie die Installationsgebühr-Artikelnummer aus.</span><span class="sxs-lookup"><span data-stu-id="1c04f-140">Select the installation charge item number.</span></span> <span data-ttu-id="1c04f-141">Beachten Sie, dass kein Abgleich ausgeführt wurde, seit Sie die Änderungen vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="1c04f-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="1c04f-142">Klicken Sie auf **Status des Abgleichs aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="1c04f-143">Klicken Sie im Aktionsbereich auf **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="1c04f-144">Klicken Sie auf **Detailabgleich**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-144">Click **Matching details**.</span></span> <span data-ttu-id="1c04f-145">Die neue Position mit Diensten muss nicht abgeglichen werden, damit bleibt der Status "Nicht ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="1c04f-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="1c04f-146">Wählen Sie den Produktzugang für den Lagerartikel aus, den Sie empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="1c04f-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="1c04f-147">Die Position mit dem Produktzugang wurde abgeglichen, allerdings stimmen Menge oder Preis nicht überein, daher wird ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="1c04f-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="1c04f-148">Geben Sie im Feld **Einzelpreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1c04f-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="1c04f-149">Jetzt, da der Preis je Einheit übereinstimmt, wird der Status zu "Bestanden" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1c04f-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="1c04f-150">Wenn Ihre Richtlinie Abweichungen zulässt oder wenn der Abgleich nur eine Warnung ist, können Sie die Rechnung dennoch buchen.</span><span class="sxs-lookup"><span data-stu-id="1c04f-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="1c04f-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1c04f-151">Close the page.</span></span>
19. <span data-ttu-id="1c04f-152">Klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="1c04f-152">Click **Post**.</span></span>
20. <span data-ttu-id="1c04f-153">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="1c04f-153">Close the form.</span></span> <span data-ttu-id="1c04f-154">Beachten Sie, dass die Bestellung nicht mehr als "Empfangen", sondern als "Nicht fakturiert" aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="1c04f-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

