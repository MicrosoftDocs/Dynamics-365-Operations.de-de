---
title: Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen
description: Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0db1c35779a468d9a86d18eb6c849d40bc8c03a3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820081"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="59c6b-103">Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen</span><span class="sxs-lookup"><span data-stu-id="59c6b-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59c6b-104">Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="59c6b-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="59c6b-105">Die ersten 4 Aufzeichnungen richten Daten ein, die benötigt werden, um diese Prozedur abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="59c6b-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="59c6b-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="59c6b-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="59c6b-107">Diese Aufgabe wird normalerweise vom Produktdesigner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59c6b-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="59c6b-108">Wählen Sie das Produkt aus</span><span class="sxs-lookup"><span data-stu-id="59c6b-108">Select the product</span></span>
1. <span data-ttu-id="59c6b-109">Klicken Sie auf "Freigegebene Produktverwaltung".</span><span class="sxs-lookup"><span data-stu-id="59c6b-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="59c6b-110">Klicken Sie auf "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="59c6b-110">Click Released products.</span></span>
3. <span data-ttu-id="59c6b-111">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="59c6b-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="59c6b-112">Suchen Sie den freigegebenen Produktmaster mit dimensionsbasierter Konfigurationstechnologie, die Sie im ersten Aufgabenleitfaden in dieser Sequenz erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="59c6b-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="59c6b-113">Klicken Sie im Aktivitätsbereich auf "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="59c6b-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="59c6b-114">Klicken Sie auf "Stücklistenversionen".</span><span class="sxs-lookup"><span data-stu-id="59c6b-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="59c6b-115">Erstellen Sie neue Stückliste und Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="59c6b-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="59c6b-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="59c6b-116">Click New.</span></span>
2. <span data-ttu-id="59c6b-117">Klicken Sie auf "Stückliste" und "Stücklistenversion".</span><span class="sxs-lookup"><span data-stu-id="59c6b-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="59c6b-118">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="59c6b-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="59c6b-119">Festlegen eines Standorts</span><span class="sxs-lookup"><span data-stu-id="59c6b-119">Setting a site</span></span>  
    * <span data-ttu-id="59c6b-120">In dieser Prozedur legen wir keinen bestimmten Standort für die Stückliste fest.</span><span class="sxs-lookup"><span data-stu-id="59c6b-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="59c6b-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="59c6b-121">Click OK.</span></span>
5. <span data-ttu-id="59c6b-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="59c6b-122">Click New.</span></span>
    * <span data-ttu-id="59c6b-123">In dieser Prozedur fügen wir vier Positionen der Stückliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="59c6b-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="59c6b-124">Zwei Positionen stellen Kabeloptionen dar und zwei Positionen stellen Gehäuseoptionen dar.</span><span class="sxs-lookup"><span data-stu-id="59c6b-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="59c6b-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="59c6b-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="59c6b-126">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="59c6b-127">Wählen Sie Artikelnummer "A0001", HDMI 6'-Kabel, aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="59c6b-128">Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="59c6b-129">Wählen Sie die Kabelvariantengruppe aus, die im Leitfaden 4 in dieser Reihenfolge erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="59c6b-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="59c6b-130">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="59c6b-130">Click New.</span></span>
    * <span data-ttu-id="59c6b-131">Wählen Sie Artikelnummer "A0002", HDMI 12'-Kabel, aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="59c6b-132">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="59c6b-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="59c6b-133">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="59c6b-134">Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="59c6b-135">Wählen Sie erneut die Kabelvariantengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="59c6b-136">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="59c6b-136">Click New.</span></span>
14. <span data-ttu-id="59c6b-137">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="59c6b-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="59c6b-138">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="59c6b-139">Wählen Sie Artikelnummer "D0002 Gehäuse" aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="59c6b-140">Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="59c6b-141">Wählen Sie die Gehäusevariantengruppe für diese Stücklistenposition aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="59c6b-142">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="59c6b-142">Click New.</span></span>
18. <span data-ttu-id="59c6b-143">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="59c6b-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="59c6b-144">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="59c6b-145">Wählen Sie Artikelnummer "M0007 StandardCabinet" als letzte Stücklistenposition aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="59c6b-146">Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="59c6b-147">Wählen Sie die Gehäusevariantengruppe für die letzte Stücklistenposition aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="59c6b-148">Genehmigen und aktivieren</span><span class="sxs-lookup"><span data-stu-id="59c6b-148">Approve and activate</span></span>
1. <span data-ttu-id="59c6b-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="59c6b-149">Close the page.</span></span>
2. <span data-ttu-id="59c6b-150">Klicken Sie auf Genehmigen.</span><span class="sxs-lookup"><span data-stu-id="59c6b-150">Click Approve.</span></span>
3. <span data-ttu-id="59c6b-151">Geben Sie im Feld 'Genehmig von' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59c6b-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="59c6b-152">Wählen Sie "Ja" aus in "Mächten Sie auch die Stückliste genehmigen?".</span><span class="sxs-lookup"><span data-stu-id="59c6b-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="59c6b-153">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="59c6b-153">Click OK.</span></span>
6. <span data-ttu-id="59c6b-154">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="59c6b-154">Click Activate.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]