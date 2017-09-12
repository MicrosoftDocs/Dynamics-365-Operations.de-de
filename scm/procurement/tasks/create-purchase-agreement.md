--- 
title: Kaufvertrag erstellen
description: "Diese Prozedur führt Sie durch die Erstellung eines Kaufvertrags."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0d0cc6508071bea3f622bc21f06aa55d2b757b6f
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="4ecd9-103">Kaufvertrag erstellen</span><span class="sxs-lookup"><span data-stu-id="4ecd9-103">Create a purchase agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ecd9-104">Diese Prozedur führt Sie durch die Erstellung eines Kaufvertrags.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="4ecd9-105">Dadurch wird normalerweise von einem Einkaufsleiter bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="4ecd9-106">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4ecd9-107">Sie müssen Einstellungen Kaufvertragsklassifizierungen haben, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="4ecd9-108">Sobald Sie eine Vereinbarung erstellt haben, können Sie diese verwenden, wenn Sie eine Bestellung erstellen, und dieses kopiert die Kaufvertragszustände in den Kopf und alle möglichen Positionen in der Reihenfolge angezeigt, die in der Vereinbarung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="4ecd9-109">Erstellen Sie eine neue Rahmenbestellung</span><span class="sxs-lookup"><span data-stu-id="4ecd9-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="4ecd9-110">Wechseln Sie zu "Beschaffung" > "Kaufverträge" > "Kaufverträge".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="4ecd9-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-111">Click New.</span></span>
3. <span data-ttu-id="4ecd9-112">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4ecd9-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4ecd9-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4ecd9-115">Klicken Sie im Feld "Kaufvertragsklassifizierung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4ecd9-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="4ecd9-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="4ecd9-118">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-118">Expand the General section.</span></span>
10. <span data-ttu-id="4ecd9-119">Geben Sie im Feld "Ablaufdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="4ecd9-120">Dieses Ablaufdatum ist der Standardwert für alle Zusagepositionen und bestimmt, wie lange jede einzelne Zusage gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="4ecd9-121">Geben Sie im Feld Dokumenttitel einen Namen für den neuen Kaufvertrag ein.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="4ecd9-122">Überlassen Sie dem Standard Zusagefeldsatz Produktmengenzusage (oder ändern Sie sie, wenn keine Zuordnung zu diesem festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="4ecd9-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="4ecd9-123">Der standardmäßige Zusagewert bestimmt Die verfügbaren Optionen in der Vertragspositionen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="4ecd9-124">Wenn Sie einen neuen Zusagetyp erfordern, wenn Sie die Vereinbarungspositionen erstellen, müssen Sie die standardmäßige Zusage im Kopf ändern.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="4ecd9-125">Es gibt 4 Typen von Zusagen: Produktmengenzusage - für eine bestimmte Menge eines Produkts; Produktwertszusage - für einen bestimmten Währungsbetrag eines Produkts; Produktkategoriewertszusage - für einen bestimmten Währungsbetrag in einer Beschaffungskategorie, in der der Betrag für einen Katalogartikel oder einen nicht im Katalog enthaltenen Artikel sein kann; Wertszusage - für einen bestimmten Währungsbetrag, der durch ein beliebiges Produkt oder von einer beliebigen Beschaffungskategorie gedeckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="4ecd9-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="4ecd9-127">Zusage hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4ecd9-127">Add a commitment</span></span>
1. <span data-ttu-id="4ecd9-128">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-128">Click Add line.</span></span>
2. <span data-ttu-id="4ecd9-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4ecd9-130">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4ecd9-131">Wählen Sie das Produkt aus, das Sie eine Zusage für hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="4ecd9-132">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4ecd9-133">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4ecd9-134">Dies ist die Gesamtmenge, die Sie Lieferscheinbuchung, von Ihrem Lieferanten kaufen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="4ecd9-135">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="4ecd9-136">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="4ecd9-137">Legen Sie die Option "Maximum wird erzwungen" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="4ecd9-138">Die Höchstzahl ist erzwungene Optionsgrenzen der Verwendung der Zusage.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="4ecd9-139">Sie können auf die Menge nur kaufen, die im Feld für die Position angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="4ecd9-140">Reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="4ecd9-141">Kopfzeilenbedingungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4ecd9-141">Add header conditions</span></span>
1. <span data-ttu-id="4ecd9-142">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="4ecd9-143">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-143">Click Change view.</span></span>
3. <span data-ttu-id="4ecd9-144">Klicken Sie auf die Kopfzeilenansicht.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-144">Click Header view.</span></span>
4. <span data-ttu-id="4ecd9-145">Erweitern Sie den Abschnitt "Bedingungen".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="4ecd9-146">Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4ecd9-147">Die Zahlungsbedingungen vom Kreditorenkonto werden hier standardmäßig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="4ecd9-148">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4ecd9-149">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4ecd9-150">Klicken Sie im Feld "Lieferart" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4ecd9-151">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4ecd9-152">Klicken Sie im Feld "Lieferbedingungen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4ecd9-153">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="4ecd9-154">Bestätigen und Aktivieren des Kaufvertrags</span><span class="sxs-lookup"><span data-stu-id="4ecd9-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="4ecd9-155">Klicken Sie im Aktivitätsbereich auf "Kaufvertrag".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="4ecd9-156">Klicken Sie auf Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-156">Click Confirmation.</span></span>
    * <span data-ttu-id="4ecd9-157">Setzen Sie die Option "Vertrag als 'Effektiv' kennzeichnen" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="4ecd9-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-158">Click OK.</span></span>
4. <span data-ttu-id="4ecd9-159">Klicken Sie im Aktivitätsbereich auf "Kaufvertrag".</span><span class="sxs-lookup"><span data-stu-id="4ecd9-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="4ecd9-160">Klicken Sie auf Kaufvertragsbestätigungen.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="4ecd9-161">Die Vorschau anzeigen/der Druckoption ermöglicht es Ihnen, ein Dokument für den Kaufvertrag zu generieren, den Sie oder Kreditor senden können dann drucken.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="4ecd9-162">Wenn Sie die Vereinbarung später aktualisieren und sie wieder-bestätigen, werden beide Versionen hier angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="4ecd9-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4ecd9-163">Close the page.</span></span>


