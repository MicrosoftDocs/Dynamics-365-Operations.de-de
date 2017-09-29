--- 
title: Rechnungsdaten mit einer Kreditorenrechnung in Kreditorenkonten eingeben
description: "Dieser Aufgabenleitfaden unterstützt Sie beim Erstellen einer Kreditorenrechnung anhand einer Bestellung und beim Anzeigen der Ergebnisse des Abgleichs von Bestellung, Zugang und Rechnung (dreiseitiger Abgleich)."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 48535a283cbdfdc7343a20105b139c527cac85f4
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a><span data-ttu-id="b8813-103">Rechnungsdaten mit einer Kreditorenrechnung in Kreditorenkonten eingeben</span><span class="sxs-lookup"><span data-stu-id="b8813-103">Key invoice data into accounts payable using a vendor invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8813-104">Dieser Aufgabenleitfaden unterstützt Sie beim Erstellen einer Kreditorenrechnung anhand einer Bestellung und beim Anzeigen der Ergebnisse des Abgleichs von Bestellung, Zugang und Rechnung (dreiseitiger Abgleich).</span><span class="sxs-lookup"><span data-stu-id="b8813-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="b8813-105">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="b8813-105">Create a purchase order</span></span>
1. <span data-ttu-id="b8813-106">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="b8813-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="b8813-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b8813-107">Click New.</span></span>
3. <span data-ttu-id="b8813-108">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8813-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b8813-109">Suchen Sie einen Kreditor, um ihn auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b8813-109">Find a vendor to select.</span></span> <span data-ttu-id="b8813-110">Führen Sie beispielsweise einen Bildlauf nach unten zu US-104 durch.</span><span class="sxs-lookup"><span data-stu-id="b8813-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="b8813-111">Wählen Sie Kreditor US-104 aus.</span><span class="sxs-lookup"><span data-stu-id="b8813-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="b8813-112">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b8813-112">Click OK.</span></span>
7. <span data-ttu-id="b8813-113">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8813-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b8813-114">Wählen Sie einen Lagerartikel aus.</span><span class="sxs-lookup"><span data-stu-id="b8813-114">Select an inventory item.</span></span> <span data-ttu-id="b8813-115">Wählen Sie beispielsweise die Artikelnummer 1000 aus.</span><span class="sxs-lookup"><span data-stu-id="b8813-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="b8813-116">Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="b8813-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="b8813-117">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="b8813-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="b8813-118">Sie können die Abgleichsrichtlinie außer Kraft setzen, um keinen Abgleich, einen zweiseitigen Abgleich oder einen dreiseitigen Abgleich zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8813-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="b8813-119">Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="b8813-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="b8813-120">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="b8813-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="b8813-121">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="b8813-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="b8813-122">Die Produkte empfangen</span><span class="sxs-lookup"><span data-stu-id="b8813-122">Receive the products</span></span>
1. <span data-ttu-id="b8813-123">Klicken Sie im Aktivitätsbereich auf "Empfangen".</span><span class="sxs-lookup"><span data-stu-id="b8813-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="b8813-124">Klicken Sie auf "Produktzugang".</span><span class="sxs-lookup"><span data-stu-id="b8813-124">Click Product receipt.</span></span>
3. <span data-ttu-id="b8813-125">Geben Sie im Feld "Produktzugang" die Produktzugangsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="b8813-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="b8813-126">Geben Sie beispielsweise "PR123" ein.</span><span class="sxs-lookup"><span data-stu-id="b8813-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="b8813-127">Klicken Sie auf "OK", um den Produktzugang zu buchen.</span><span class="sxs-lookup"><span data-stu-id="b8813-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="b8813-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b8813-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="b8813-129">Eine Kreditorenrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="b8813-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="b8813-130">Wechseln Sie zu Kreditoren > Bestellungen > Bestellungen wurden empfangen, jedoch nicht fakturiert.</span><span class="sxs-lookup"><span data-stu-id="b8813-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="b8813-131">Wählen Sie die Bestellung aus, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b8813-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="b8813-132">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="b8813-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="b8813-133">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="b8813-133">Click Invoice.</span></span>
5. <span data-ttu-id="b8813-134">Geben Sie im Feld "Nummer" die Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="b8813-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="b8813-135">Geben Sie im Feld "Rechnungsbeschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b8813-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="b8813-136">Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="b8813-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="b8813-137">Geben Sie im Feld "Einzelpreis" die Zahl 1200 ein.</span><span class="sxs-lookup"><span data-stu-id="b8813-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="b8813-138">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b8813-138">Click Add line.</span></span>
10. <span data-ttu-id="b8813-139">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8813-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b8813-140">Suchen Sie in der Liste die Installationsgebühr-Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="b8813-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="b8813-141">Beispielsweise S0001</span><span class="sxs-lookup"><span data-stu-id="b8813-141">For example, S0001</span></span>
12. <span data-ttu-id="b8813-142">Wählen Sie die Installationsgebühr-Artikelnummer aus.</span><span class="sxs-lookup"><span data-stu-id="b8813-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="b8813-143">Beachten Sie, dass kein Abgleich ausgeführt wurde, seit Sie die Änderungen vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="b8813-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="b8813-144">Klicken Sie auf "Status des Abgleichs aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="b8813-144">Click Update match status.</span></span>
14. <span data-ttu-id="b8813-145">Klicken Sie im Aktivitätsbereich auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="b8813-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="b8813-146">Klicken Sie auf "Detailabgleich".</span><span class="sxs-lookup"><span data-stu-id="b8813-146">Click Matching details.</span></span>
    * <span data-ttu-id="b8813-147">Die neue Position mit Diensten muss nicht abgeglichen werden, damit bleibt der Status "Nicht ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="b8813-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="b8813-148">Wählen Sie den Produktzugang für den Lagerartikel aus, den Sie empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="b8813-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="b8813-149">Die Position mit dem Produktzugang wurde abgeglichen, allerdings stimmen Menge oder Preis nicht überein, daher wird ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="b8813-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="b8813-150">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b8813-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="b8813-151">Jetzt, da der Preis je Einheit übereinstimmt, wird der Status zu "Bestanden" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b8813-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="b8813-152">Wenn Ihre Richtlinie Abweichungen zulässt oder wenn der Abgleich nur eine Warnung ist, können Sie die Rechnung dennoch buchen.</span><span class="sxs-lookup"><span data-stu-id="b8813-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="b8813-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b8813-153">Close the page.</span></span>
19. <span data-ttu-id="b8813-154">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="b8813-154">Click Post.</span></span>
20. <span data-ttu-id="b8813-155">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="b8813-155">Close the form.</span></span>
    * <span data-ttu-id="b8813-156">Beachten Sie, dass die Bestellung nicht mehr als "Empfangen", sondern als "Nicht fakturiert" aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="b8813-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


