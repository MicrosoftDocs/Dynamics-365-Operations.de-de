---
title: Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen
description: Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7961cfb4ad0e20c49d327d83f56c08811598ac1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428709"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="eb0ce-103">Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen</span><span class="sxs-lookup"><span data-stu-id="eb0ce-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb0ce-104">Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="eb0ce-105">Die ersten 4 Aufzeichnungen richten Daten ein, die benötigt werden, um diese Prozedur abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="eb0ce-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="eb0ce-107">Diese Aufgabe wird normalerweise vom Produktdesigner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="eb0ce-108">Wählen Sie das Produkt aus</span><span class="sxs-lookup"><span data-stu-id="eb0ce-108">Select the product</span></span>
1. <span data-ttu-id="eb0ce-109">Klicken Sie auf "Freigegebene Produktverwaltung".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="eb0ce-110">Klicken Sie auf "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-110">Click Released products.</span></span>
3. <span data-ttu-id="eb0ce-111">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="eb0ce-112">Suchen Sie den freigegebenen Produktmaster mit dimensionsbasierter Konfigurationstechnologie, die Sie im ersten Aufgabenleitfaden in dieser Sequenz erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="eb0ce-113">Klicken Sie im Aktivitätsbereich auf "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="eb0ce-114">Klicken Sie auf "Stücklistenversionen".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="eb0ce-115">Erstellen Sie neue Stückliste und Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="eb0ce-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="eb0ce-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-116">Click New.</span></span>
2. <span data-ttu-id="eb0ce-117">Klicken Sie auf "Stückliste" und "Stücklistenversion".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="eb0ce-118">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="eb0ce-119">Festlegen eines Standorts</span><span class="sxs-lookup"><span data-stu-id="eb0ce-119">Setting a site</span></span>  
    * <span data-ttu-id="eb0ce-120">In dieser Prozedur legen wir keinen bestimmten Standort für die Stückliste fest.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="eb0ce-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-121">Click OK.</span></span>
5. <span data-ttu-id="eb0ce-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-122">Click New.</span></span>
    * <span data-ttu-id="eb0ce-123">In dieser Prozedur fügen wir vier Positionen der Stückliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="eb0ce-124">Zwei Positionen stellen Kabeloptionen dar und zwei Positionen stellen Gehäuseoptionen dar.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="eb0ce-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="eb0ce-126">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="eb0ce-127">Wählen Sie Artikelnummer "A0001", HDMI 6'-Kabel, aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="eb0ce-128">Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="eb0ce-129">Wählen Sie die Kabelvariantengruppe aus, die im Leitfaden 4 in dieser Reihenfolge erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="eb0ce-130">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-130">Click New.</span></span>
    * <span data-ttu-id="eb0ce-131">Wählen Sie Artikelnummer "A0002", HDMI 12'-Kabel, aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="eb0ce-132">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="eb0ce-133">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="eb0ce-134">Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="eb0ce-135">Wählen Sie erneut die Kabelvariantengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="eb0ce-136">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-136">Click New.</span></span>
14. <span data-ttu-id="eb0ce-137">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="eb0ce-138">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="eb0ce-139">Wählen Sie Artikelnummer "D0002 Gehäuse" aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="eb0ce-140">Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="eb0ce-141">Wählen Sie die Gehäusevariantengruppe für diese Stücklistenposition aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="eb0ce-142">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-142">Click New.</span></span>
18. <span data-ttu-id="eb0ce-143">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="eb0ce-144">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="eb0ce-145">Wählen Sie Artikelnummer "M0007 StandardCabinet" als letzte Stücklistenposition aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="eb0ce-146">Geben Sie im Feld "Variantengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="eb0ce-147">Wählen Sie die Gehäusevariantengruppe für die letzte Stücklistenposition aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="eb0ce-148">Genehmigen und aktivieren</span><span class="sxs-lookup"><span data-stu-id="eb0ce-148">Approve and activate</span></span>
1. <span data-ttu-id="eb0ce-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-149">Close the page.</span></span>
2. <span data-ttu-id="eb0ce-150">Klicken Sie auf Genehmigen.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-150">Click Approve.</span></span>
3. <span data-ttu-id="eb0ce-151">Geben Sie im Feld 'Genehmig von' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="eb0ce-152">Wählen Sie "Ja" aus in "Mächten Sie auch die Stückliste genehmigen?".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="eb0ce-153">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="eb0ce-153">Click OK.</span></span>
6. <span data-ttu-id="eb0ce-154">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="eb0ce-154">Click Activate.</span></span>

