---
title: Kaufvertrag erstellen
description: Dieses Thema führt Sie durch die Erstellung eines Kaufvertrags.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428646"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="0ae2a-103">Kaufvertrag erstellen</span><span class="sxs-lookup"><span data-stu-id="0ae2a-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ae2a-104">Dieses Thema führt Sie durch die Erstellung eines Kaufvertrags.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="0ae2a-105">Dadurch wird normalerweise von einem Einkaufsleiter bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="0ae2a-106">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0ae2a-107">Sie müssen Einstellungen Kaufvertragsklassifizierungen haben, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="0ae2a-108">Sobald Sie eine Vereinbarung erstellt haben, können Sie diese verwenden, wenn Sie eine Bestellung erstellen, und dieses kopiert die Kaufvertragszustände in den Kopf und alle möglichen Positionen in der Reihenfolge angezeigt, die in der Vereinbarung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="0ae2a-109">Erstellen Sie eine neue Rahmenbestellung</span><span class="sxs-lookup"><span data-stu-id="0ae2a-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="0ae2a-110">Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Kaufverträge > Kaufverträge**.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="0ae2a-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-111">Click **New**.</span></span>
3. <span data-ttu-id="0ae2a-112">Wählen Sie im Feld **Kreditorenkonto** das Dropdownmenü aus und wählen Sie die Zeile des gewünschten Datensatzes aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="0ae2a-113">Wählen Sie im Feld **Kaufvertragsklassifizierung** das Dropdownmenü aus und wählen Sie die Zeile des gewünschten Datensatzes aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="0ae2a-114">Erweitern Sie das Inforegister **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="0ae2a-115">Geben Sie im Feld **Ablaufdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="0ae2a-116">Dieses Ablaufdatum ist der Standardwert für alle Zusagepositionen und bestimmt, wie lange jede einzelne Zusage gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="0ae2a-117">Geben Sie im Feld **Dokumenttitel** einen Namen für den neuen Kaufvertrag ein.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="0ae2a-118">Lassen Sie das Feld **Standardzusage** festgelegt auf **Produktmengenzusage** (oder ändern Sie es, falls es noch nicht darauf festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="0ae2a-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="0ae2a-119">Der standardmäßige Zusagewert bestimmt Die verfügbaren Optionen in der Vertragspositionen.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="0ae2a-120">Wenn Sie einen neuen Zusagetyp erfordern, wenn Sie die Vereinbarungspositionen erstellen, müssen Sie die standardmäßige Zusage auch im Kopf ändern.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="0ae2a-121">Es gibt 4 Typen von Zusagen: **Produktmengenzusage** – für eine bestimmte Menge eines Produkts; **Produktwertzusage** – für einen bestimmten Währungsbetrag eines Produkts; **Produktkategoriewertzusage** – für einen bestimmten Währungsbetrag in einer Beschaffungskategorie, in der der Betrag für einen Katalogartikel oder einen nicht im Katalog enthaltenen Artikel sein kann; **Wertzusage** – für einen bestimmten Währungsbetrag, der durch ein beliebiges Produkt oder von einer beliebigen Beschaffungskategorie gedeckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="0ae2a-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="0ae2a-123">Zusage hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0ae2a-123">Add a commitment</span></span>
1. <span data-ttu-id="0ae2a-124">Wählen Sie **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-124">Select **Add line**.</span></span>
2. <span data-ttu-id="0ae2a-125">Wählen Sie im Feld **Artikelnummer** den gewünschten Datensatz aus dem Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="0ae2a-126">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="0ae2a-127">Dies ist die Gesamtmenge, die Sie Lieferscheinbuchung, von Ihrem Lieferanten kaufen.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="0ae2a-128">Geben Sie im Feld **Einzelpreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="0ae2a-129">Erweitern Sie den Abschnitt **Positionsdetails**.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="0ae2a-130">Legen Sie die Option **Maximum wird erzwungen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="0ae2a-131">Die Option **Maximum wird erzwungen** begrenzt die Verwendung der Zusage.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="0ae2a-132">Sie können nur bis zu der Menge einkaufen, die im Feld **Menge** für die Position angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="0ae2a-133">Kopfzeilenbedingungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0ae2a-133">Add header conditions</span></span>
1. <span data-ttu-id="0ae2a-134">Wählen Sie im Aktivitätsbereich **Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="0ae2a-135">Wählen Sie **Ansicht wechseln** aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-135">Select **Change view**.</span></span>
3. <span data-ttu-id="0ae2a-136">Wählen Sie **Kopfzeilenansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-136">Select **Header view**.</span></span>
4. <span data-ttu-id="0ae2a-137">Erweitern Sie den Abschnitt **Bedingungen**.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="0ae2a-138">Wählen Sie im Feld **Zahlungsmethode** den gewünschten Datensatz im Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="0ae2a-139">Die Zahlungsbedingungen vom Kreditorenkonto werden hier standardmäßig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="0ae2a-140">Wählen Sie im Feld **Lieferart** den gewünschten Datensatz im Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="0ae2a-141">Wählen Sie im Feld **Lieferbedingungen** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="0ae2a-142">Bestätigen und Aktivieren des Kaufvertrags</span><span class="sxs-lookup"><span data-stu-id="0ae2a-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="0ae2a-143">Wählen Sie im Aktivitätsbereich **Kaufvertrag** aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="0ae2a-144">Wählen Sie **Bestätigung** aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-144">Select **Confirmation**.</span></span> <span data-ttu-id="0ae2a-145">Setzen Sie die Option **Vertrag als 'Effektiv' kennzeichnen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="0ae2a-146">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-146">Select **OK**.</span></span>
4. <span data-ttu-id="0ae2a-147">Wählen Sie im Aktivitätsbereich **Kaufvertrag** aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="0ae2a-148">Wählen Sie **Kaufvertragsbestätigungen** aus.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="0ae2a-149">Die Option **Vorschau anzeigen/Drucken** ermöglicht es Ihnen, ein Dokument für den Kaufvertrag zu generieren, den Sie an den Kreditor senden oder für diesen drucken können.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="0ae2a-150">Wenn Sie die Vereinbarung später aktualisieren und sie wieder-bestätigen, werden beide Versionen hier angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="0ae2a-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-151">Close the page.</span></span>

