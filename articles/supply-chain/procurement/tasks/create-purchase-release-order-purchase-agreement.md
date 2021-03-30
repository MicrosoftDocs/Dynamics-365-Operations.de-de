---
title: Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag erstellen
description: Im folgenden Verfahren, wie ein Kaufvertrag verwendet, wenn Sie eine Bestellung erstellen.
author: RichardLuan
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4e9a0551c0755fd006fc030d2e1bf4f28efe951
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211956"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="ae82f-103">Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag erstellen</span><span class="sxs-lookup"><span data-stu-id="ae82f-103">Create a purchase release order from a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae82f-104">Im folgenden Verfahren, wie ein Kaufvertrag verwendet, wenn Sie eine Bestellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="ae82f-105">Der Kaufvertrag muss angewendet werden, wenn Sie die Bestellung anlegen, da es allgemeine Begriffe gibt, die in den Bestellkopf kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="ae82f-106">In der Regel steht diese Aufgabe von einem Einkaufsvertreter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae82f-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="ae82f-107">Als Komponente für dieses Manuell, müssen Sie einen gültigen Kaufvertrag mit einer Produktmengenzusage für einen Kreditor und Artikel verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae82f-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="ae82f-108">Die gleichen Verfahren kann verwendet werden, wenn Sie einen Kaufvertrag mit anderen Typen von Zusagen haben.</span><span class="sxs-lookup"><span data-stu-id="ae82f-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="ae82f-109">Sie können diese Anleitung im Demodatenunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="ae82f-110">Wenn Sie USMF verwenden, können Sie Handbuch „Erstellen eines Kaufvertrags“ zuerst ausführen, um die erforderlichen Vorbedingungen für dieses Handbuch einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ae82f-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="ae82f-111">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="ae82f-111">Create a purchase order</span></span>
1. <span data-ttu-id="ae82f-112">In **Navigationsbereich** wechseln Sie zu **Arbeitsbereiche > Bestellungsvorbereitung**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="ae82f-113">Klicken Sie auf **Neue Bestellung**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="ae82f-114">Klicken Sie im Feld **Kreditorenkonto** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ae82f-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ae82f-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ae82f-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ae82f-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ae82f-117">Erweitern Sie das Inforegister **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="ae82f-118">Klicken Sie im Feld **Kaufvertrag** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ae82f-119">Alle verfügbaren Vereinbarungen für den Kreditor werden hier aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae82f-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="ae82f-120">Finden Sie die gültige Vereinbarung, die Sie verwenden wollen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="ae82f-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ae82f-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ae82f-122">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-122">Click **Yes**.</span></span>
10. <span data-ttu-id="ae82f-123">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="ae82f-124">Hinzufügen einer Line</span><span class="sxs-lookup"><span data-stu-id="ae82f-124">Add a line</span></span>
1. <span data-ttu-id="ae82f-125">Geben Sie im Feld **Artikelnummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ae82f-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="ae82f-126">Sind bestimmte Lager- oder Lagerplatzdimensionen auf der Zusage besteht, müssen Sie die denselben Werten in der Bestellposition eingeben, um die Vereinbarung auszunutzen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="ae82f-127">Klicken Sie im Feld **Standort** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ae82f-128">Der Standort bereits wird mit dem Standardwert aus dem Auftrag oder Kreditor ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="ae82f-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="ae82f-129">Ist dies der Fall, fahren Sie diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="ae82f-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="ae82f-130">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ae82f-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ae82f-131">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ae82f-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ae82f-132">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ae82f-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="ae82f-133">Überprüfen Sie, ob der Preis aus der Zusage kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="ae82f-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="ae82f-134">Hiermit wird die Zusage</span><span class="sxs-lookup"><span data-stu-id="ae82f-134">Look up the commitment</span></span>
1. <span data-ttu-id="ae82f-135">Klicken Sie auf **Position aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-135">Click **Update line**.</span></span>
2. <span data-ttu-id="ae82f-136">Klicken Sie auf **Zugeordnet**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-136">Click **Attached**.</span></span> <span data-ttu-id="ae82f-137">Hier können Sie Details für den Kaufvertrag abrufen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="ae82f-138">So können Sie den Preis finden und ob der Preis und Rabatt korrigiert werden, damit es, das heißt dass, wenn Sie Preis oder Rabatt auf die Bestellung zu einem anderen Wert als auf der Zusage ändern, das System den Link entfernt, sodass die Bestellposition nicht die Zusage erfüllt.</span><span class="sxs-lookup"><span data-stu-id="ae82f-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="ae82f-139">Sie können außerdem feststellen, ob das Maximum erzwungene Option ist aktiviert ist, das heißt, dass die Menge in der Zusage nicht überschritten werden kann, indem Sie alle Einkäufe summiert, die die Zusage erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ae82f-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="ae82f-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ae82f-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="ae82f-141">Rahmenbestellung einrichten</span><span class="sxs-lookup"><span data-stu-id="ae82f-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="ae82f-142">Klicken Sie im **Aktivitätsbereich** auf **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="ae82f-143">Klicken Sie auf **Kaufvertrag**.</span><span class="sxs-lookup"><span data-stu-id="ae82f-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="ae82f-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ae82f-144">Close the page.</span></span>
4. <span data-ttu-id="ae82f-145">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ae82f-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]