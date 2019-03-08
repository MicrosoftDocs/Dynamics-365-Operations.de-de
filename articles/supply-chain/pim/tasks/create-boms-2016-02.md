---
title: Stücklisten Erstellen (Februar 2016)
description: Diese Aufgabe konzentriert sich auf das Erstellen der Stücklistenstruktur für ein fertiges Produkt und ein halbfertiges Produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "333207"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="5b6f8-103">Stücklisten Erstellen (Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="5b6f8-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b6f8-104">Diese Aufgabe konzentriert sich auf das Erstellen der Stücklistenstruktur für ein fertiges Produkt und ein halbfertiges Produkt.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="5b6f8-105">Es ist die vierte Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="5b6f8-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="5b6f8-107">Stückliste für ein halbfertiges Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="5b6f8-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="5b6f8-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="5b6f8-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5b6f8-110">Wählen Sie die Artikelnummer BOM_2 aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="5b6f8-111">Klicken Sie im Aktivitätsbereich auf "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="5b6f8-112">Klicken Sie auf "Stücklistenversionen".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-112">Click BOM versions.</span></span>
5. <span data-ttu-id="5b6f8-113">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-113">Click New.</span></span>
6. <span data-ttu-id="5b6f8-114">Klicken Sie auf "Stückliste" und "Stücklistenversion".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="5b6f8-115">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="5b6f8-116">Geben Sie beispielsweise BOM_2 ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="5b6f8-117">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6f8-118">Geben Sie für dieses Beispiel „Standort 1” ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="5b6f8-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-119">Click OK.</span></span>
10. <span data-ttu-id="5b6f8-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-120">Click New.</span></span>
11. <span data-ttu-id="5b6f8-121">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="5b6f8-122">Geben Sie für dieses Beispiel ITEM_C ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="5b6f8-123">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6f8-124">Geben Sie für dieses Beispiel 11 ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="5b6f8-125">Klicken Sie auf "Kopfzeile".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-125">Click Header.</span></span>
14. <span data-ttu-id="5b6f8-126">Klicken Sie auf „Genehmigung”, um Stücklisten zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="5b6f8-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-127">Click OK.</span></span>
16. <span data-ttu-id="5b6f8-128">Klicken Sie auf Genehmigen.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-128">Click Approve.</span></span>
    * <span data-ttu-id="5b6f8-129">Die Schaltfläche „Genehmigen” auf dem ToolBar im Stücklisten-Versionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="5b6f8-130">Wenn sie nicht angezeigt wird, klicken Sie „Kopfzeile” oben rechts auf der Seite „Stücklisten”, um „Genehmigen” anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="5b6f8-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-131">Click OK.</span></span>
18. <span data-ttu-id="5b6f8-132">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-132">Click Activate.</span></span>
19. <span data-ttu-id="5b6f8-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-133">Close the page.</span></span>
20. <span data-ttu-id="5b6f8-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-134">Close the page.</span></span>
21. <span data-ttu-id="5b6f8-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="5b6f8-136">Stückliste für ein fertiges Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="5b6f8-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="5b6f8-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5b6f8-138">Wählen Sie die Artikelnummer BOM_1 aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="5b6f8-139">Klicken Sie im Aktivitätsbereich auf "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="5b6f8-140">Klicken Sie auf "Stücklistenversionen".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-140">Click BOM versions.</span></span>
4. <span data-ttu-id="5b6f8-141">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-141">Click New.</span></span>
5. <span data-ttu-id="5b6f8-142">Klicken Sie auf "Stückliste" und "Stücklistenversion".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="5b6f8-143">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="5b6f8-144">Geben Sie beispielsweise BOM_1 ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="5b6f8-145">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6f8-146">Geben Sie für dieses Beispiel „Standort 1” ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="5b6f8-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-147">Click OK.</span></span>
9. <span data-ttu-id="5b6f8-148">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-148">Click New.</span></span>
10. <span data-ttu-id="5b6f8-149">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="5b6f8-150">Geben Sie für dieses Beispiel ITEM_A ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="5b6f8-151">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6f8-152">Wählen Sie für dieses Beispiel 11 aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="5b6f8-153">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-153">Click New.</span></span>
13. <span data-ttu-id="5b6f8-154">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="5b6f8-155">Geben Sie für dieses Beispiel ITEM_B ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="5b6f8-156">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6f8-157">Geben Sie für dieses Beispiel 11 ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="5b6f8-158">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-158">Click New.</span></span>
16. <span data-ttu-id="5b6f8-159">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="5b6f8-160">Geben Sie für dieses Beispiel BOM_2 ein.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="5b6f8-161">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="5b6f8-162">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6f8-163">Geben Sie für dieses Beispiel Lagerort 11 ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="5b6f8-164">Klicken Sie auf "Kopfzeile".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-164">Click Header.</span></span>
20. <span data-ttu-id="5b6f8-165">Klicken Sie auf „Genehmigung”, um Stücklisten zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="5b6f8-166">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-166">Click OK.</span></span>
22. <span data-ttu-id="5b6f8-167">Klicken Sie auf Genehmigen.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-167">Click Approve.</span></span>
    * <span data-ttu-id="5b6f8-168">Die Schaltfläche „Genehmigen” auf dem ToolBar im Stücklisten-Versionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="5b6f8-169">Wenn sie nicht angezeigt wird, klicken Sie „Kopfzeile” oben rechts auf der Seite „Stücklisten”, um „Genehmigen” anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="5b6f8-170">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5b6f8-170">Click OK.</span></span>
24. <span data-ttu-id="5b6f8-171">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-171">Click Activate.</span></span>
25. <span data-ttu-id="5b6f8-172">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-172">Close the page.</span></span>
26. <span data-ttu-id="5b6f8-173">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-173">Close the page.</span></span>
27. <span data-ttu-id="5b6f8-174">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5b6f8-174">Close the page.</span></span>

