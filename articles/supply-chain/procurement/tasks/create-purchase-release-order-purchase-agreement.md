---
title: Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag erstellen
description: Im folgenden Verfahren, wie ein Kaufvertrag verwendet, wenn Sie eine Bestellung erstellen.
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c45db4ac01be831c0c75f888d313d61d934fc33f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "328883"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="c203c-103">Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag erstellen</span><span class="sxs-lookup"><span data-stu-id="c203c-103">Create a purchase release order from a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c203c-104">Im folgenden Verfahren, wie ein Kaufvertrag verwendet, wenn Sie eine Bestellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="c203c-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="c203c-105">Der Kaufvertrag muss angewendet werden, wenn Sie die Bestellung anlegen, da es allgemeine Begriffe gibt, die in den Bestellkopf kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c203c-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="c203c-106">In der Regel steht diese Aufgabe von einem Einkaufsvertreter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c203c-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="c203c-107">Als Komponente für dieses Manuell, müssen Sie einen gültigen Kaufvertrag mit einer Produktmengenzusage für einen Kreditor und Artikel verwenden.</span><span class="sxs-lookup"><span data-stu-id="c203c-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="c203c-108">Die gleichen Verfahren kann verwendet werden, wenn Sie einen Kaufvertrag mit anderen Typen von Zusagen haben.</span><span class="sxs-lookup"><span data-stu-id="c203c-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="c203c-109">Sie können diese Anleitung im Demodatenunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="c203c-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="c203c-110">Wenn Sie USMF verwenden, können Sie Handbuch "Erstellen eines Kaufvertrags" zuerst ausführen, um die erforderlichen Vorbedingungen für dieses Handbuch einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c203c-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="c203c-111">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="c203c-111">Create a purchase order</span></span>
1. <span data-ttu-id="c203c-112">Bestellungsvorbereitungs des Arbeitsbereich anzeigen</span><span class="sxs-lookup"><span data-stu-id="c203c-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="c203c-113">Neue Bestellung</span><span class="sxs-lookup"><span data-stu-id="c203c-113">Click New purchase order.</span></span>
3. <span data-ttu-id="c203c-114">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c203c-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c203c-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c203c-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c203c-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c203c-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c203c-117">Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="c203c-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="c203c-118">Klicken Sie im Feld "Kaufvertragsklassifizierung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c203c-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c203c-119">Alle verfügbaren Vereinbarungen für den Kreditor werden hier aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c203c-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="c203c-120">Finden Sie die gültige Vereinbarung, die Sie verwenden wollen.</span><span class="sxs-lookup"><span data-stu-id="c203c-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="c203c-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c203c-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c203c-122">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="c203c-122">Click Yes.</span></span>
10. <span data-ttu-id="c203c-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c203c-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="c203c-124">Hinzufügen einer Line</span><span class="sxs-lookup"><span data-stu-id="c203c-124">Add a line</span></span>
1. <span data-ttu-id="c203c-125">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c203c-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c203c-126">Sind bestimmte Lager- oder Lagerplatzdimensionen auf der Zusage besteht, müssen Sie die denselben Werten in der Bestellposition eingeben, um die Vereinbarung auszunutzen.</span><span class="sxs-lookup"><span data-stu-id="c203c-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="c203c-127">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c203c-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c203c-128">Der Standort bereits wird mit dem Standardwert aus dem Auftrag oder Kreditor ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="c203c-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="c203c-129">Ist dies der Fall, fahren Sie diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="c203c-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="c203c-130">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c203c-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c203c-131">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c203c-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c203c-132">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c203c-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c203c-133">Überprüfen Sie, ob der Preis aus der Zusage kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="c203c-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="c203c-134">Hiermit wird die Zusage</span><span class="sxs-lookup"><span data-stu-id="c203c-134">Look up the commitment</span></span>
1. <span data-ttu-id="c203c-135">Klicken Sie auf "Position aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="c203c-135">Click Update line.</span></span>
2. <span data-ttu-id="c203c-136">Klicken Sie auf "Zugeordnet".</span><span class="sxs-lookup"><span data-stu-id="c203c-136">Click Attached.</span></span>
    * <span data-ttu-id="c203c-137">Hier können Sie Details für den Kaufvertrag abrufen.</span><span class="sxs-lookup"><span data-stu-id="c203c-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="c203c-138">So können Sie den Preis finden und ob der Preis und Rabatt korrigiert werden, damit es, das heißt dass, wenn Sie Preis oder Rabatt auf die Bestellung zu einem anderen Wert als auf der Zusage ändern, das System den Link entfernt, sodass die Bestellposition nicht die Zusage erfüllt.</span><span class="sxs-lookup"><span data-stu-id="c203c-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="c203c-139">Sie können außerdem feststellen, ob das Maximum erzwungene Option ist aktiviert ist, das heißt, dass die Menge in der Zusage nicht überschritten werden kann, indem Sie alle Einkäufe summiert, die die Zusage erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c203c-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="c203c-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c203c-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="c203c-141">Rahmenbestellung einrichten</span><span class="sxs-lookup"><span data-stu-id="c203c-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="c203c-142">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="c203c-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="c203c-143">Rahmenbestellungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c203c-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="c203c-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c203c-144">Close the page.</span></span>
4. <span data-ttu-id="c203c-145">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c203c-145">Close the page.</span></span>

