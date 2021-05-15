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
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920704"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="0cdf1-103">Eine Stückliste für einen dimensionsbasierten Produktmaster erstellen</span><span class="sxs-lookup"><span data-stu-id="0cdf1-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0cdf1-104">Für diese Prozedur sollten Sie die vorherigen 4 Leitfäden in dieser Reihenfolge der acht Aufzeichnungen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="0cdf1-105">Die ersten 4 Aufzeichnungen richten Daten ein, die benötigt werden, um diese Prozedur abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="0cdf1-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0cdf1-107">Diese Aufgabe wird normalerweise vom Produktdesigner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="0cdf1-108">Wählen Sie das Produkt aus</span><span class="sxs-lookup"><span data-stu-id="0cdf1-108">Select the product</span></span>

1. <span data-ttu-id="0cdf1-109">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0cdf1-110">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0cdf1-111">Suchen Sie den freigegebenen Produktmaster mit dimensionsbasierter Konfigurationstechnologie, die Sie im ersten Aufgabenleitfaden in dieser Sequenz erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="0cdf1-112">Wählen Sie im Aktivitätsbereich **Techniker**.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="0cdf1-113">Wählen Sie **Stücklisten-Versionen**.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="0cdf1-114">Erstellen Sie neue Stückliste und Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="0cdf1-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="0cdf1-115">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-115">Select **New**.</span></span>
1. <span data-ttu-id="0cdf1-116">Wählen Sie **Stückliste und Stückliste Version**.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="0cdf1-117">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="0cdf1-118">Festlegen eines Standorts</span><span class="sxs-lookup"><span data-stu-id="0cdf1-118">Setting a site</span></span>  
    * <span data-ttu-id="0cdf1-119">In dieser Prozedur legen wir keinen bestimmten Standort für die Stückliste fest.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="0cdf1-120">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-120">Select **OK**.</span></span>
1. <span data-ttu-id="0cdf1-121">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-121">Select **New**.</span></span>
    * <span data-ttu-id="0cdf1-122">In dieser Prozedur fügen wir vier Positionen der Stückliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="0cdf1-123">Zwei Positionen stellen Kabeloptionen dar und zwei Positionen stellen Gehäuseoptionen dar.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="0cdf1-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cdf1-125">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0cdf1-126">Wählen Sie Artikelnummer "A0001", HDMI 6'-Kabel, aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="0cdf1-127">Geben Sie in das Feld **Konfigurationsgruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0cdf1-128">Wählen Sie die in Anleitung 4 erstellte Kabelkonfigurationsgruppe in dieser Sequenz.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="0cdf1-129">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-129">Select **New**.</span></span>
    * <span data-ttu-id="0cdf1-130">Wählen Sie Artikelnummer "A0002", HDMI 12'-Kabel, aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="0cdf1-131">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cdf1-132">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="0cdf1-133">Geben Sie in das Feld **Konfigurationsgruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0cdf1-134">Wählen Sie erneut die Kabelkonfigurationsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="0cdf1-135">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-135">Select **New**.</span></span>
1. <span data-ttu-id="0cdf1-136">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cdf1-137">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0cdf1-138">Wählen Sie Artikelnummer "D0002 Gehäuse" aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="0cdf1-139">Geben Sie in das Feld **Konfigurationsgruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0cdf1-140">Wählen Sie die Gehäusekonfigurationsgruppe für diese Stückliste-Zeile.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="0cdf1-141">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-141">Select **New**.</span></span>
1. <span data-ttu-id="0cdf1-142">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cdf1-143">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0cdf1-144">Wählen Sie Artikelnummer "M0007 StandardCabinet" als letzte Stücklistenposition aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="0cdf1-145">Geben Sie in das Feld **Konfigurationsgruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0cdf1-146">Wählen Sie die Gehäusekonfigurationsgruppe für die letzte Zeile der Stückliste aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="0cdf1-147">Genehmigen und aktivieren</span><span class="sxs-lookup"><span data-stu-id="0cdf1-147">Approve and activate</span></span>

1. <span data-ttu-id="0cdf1-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-148">Close the page.</span></span>
1. <span data-ttu-id="0cdf1-149">Wählen Sie **Genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-149">Select **Approve**.</span></span>
1. <span data-ttu-id="0cdf1-150">Geben Sie im Feld **Genehmigt von** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="0cdf1-151">Wählen Sie *Ja* im Feld **Wollen Sie die Stückliste auch genehmigen?**.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="0cdf1-152">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-152">Select **OK**.</span></span>
1. <span data-ttu-id="0cdf1-153">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0cdf1-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]