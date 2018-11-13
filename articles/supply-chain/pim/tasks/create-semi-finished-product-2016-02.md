--- 
title: Ein halbfertiges Produkt erstellen (Februar 2016)
description: Diese Aufgabe konzentriert sich auf das Erstellen eines halbfertigen Produkts.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9caeae552471eed1cb1d8630f387ca31107fcece
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-semi-finished-product-february-2016"></a><span data-ttu-id="f3933-103">Ein halbfertiges Produkt erstellen (Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="f3933-103">Create a semi-finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3933-104">Diese Aufgabe konzentriert sich auf das Erstellen eines halbfertigen Produkts.</span><span class="sxs-lookup"><span data-stu-id="f3933-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="f3933-105">Es ist die zweite Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="f3933-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="f3933-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="f3933-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="f3933-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="f3933-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f3933-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f3933-108">Click New.</span></span>
3. <span data-ttu-id="f3933-109">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f3933-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f3933-110">Geben Sie für dieses Beispiel BOM_2 ein.</span><span class="sxs-lookup"><span data-stu-id="f3933-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="f3933-111">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-112">Wählen Sie STD aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-112">Select STD.</span></span> <span data-ttu-id="f3933-113">STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f3933-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="f3933-114">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-115">Wählen Sie z. B. „Audio” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-115">For example, select Audio.</span></span> <span data-ttu-id="f3933-116">Dies hat keine Auswirkungen auf Kostenberechnungen.</span><span class="sxs-lookup"><span data-stu-id="f3933-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="f3933-117">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-118">Wählen Sie „SiteWH” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-118">Select SiteWH.</span></span> <span data-ttu-id="f3933-119">Nur „Standort” und „Lagerort” werden für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3933-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="f3933-120">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-121">Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet, wählen Sie „Keine” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="f3933-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f3933-122">Click OK.</span></span>
9. <span data-ttu-id="f3933-123">Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="f3933-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="f3933-124">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="f3933-124">Click Default order settings.</span></span>
11. <span data-ttu-id="f3933-125">Wählen Sie im Feld „Standardauftragstyp” die Option „Produktion” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="f3933-126">Da dies ein halbfertiges Produkt ist, das produziert wird, wählen Sie „Produktion” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="f3933-127">Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-128">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f3933-129">Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-130">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="f3933-131">Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-132">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="f3933-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f3933-133">Close the page.</span></span>
16. <span data-ttu-id="f3933-134">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="f3933-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="f3933-135">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="f3933-135">Click Item price.</span></span>
18. <span data-ttu-id="f3933-136">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f3933-136">Click New.</span></span>
19. <span data-ttu-id="f3933-137">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f3933-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="f3933-138">Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-139">Wählen Sie für dieses Beispiel „Version 10” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="f3933-140">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-141">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="f3933-142">Legen Sie „Preis” auf „10” fest.</span><span class="sxs-lookup"><span data-stu-id="f3933-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="f3933-143">Geben Sie für dieses Beispiel einen Kostenpreis von 10 ein.</span><span class="sxs-lookup"><span data-stu-id="f3933-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="f3933-144">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f3933-144">Click Save.</span></span>
24. <span data-ttu-id="f3933-145">Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.</span><span class="sxs-lookup"><span data-stu-id="f3933-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="f3933-146">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f3933-146">Close the page.</span></span>
26. <span data-ttu-id="f3933-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f3933-147">Close the page.</span></span>
27. <span data-ttu-id="f3933-148">Klicken Sie auf BOM_2, um sie zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f3933-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="f3933-149">Erweitern Sie den Abschnitt „Kosten verwalten”.</span><span class="sxs-lookup"><span data-stu-id="f3933-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="f3933-150">Geben Sie im Feld „Kostengruppe” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="f3933-151">Wählen Sie für dieses Beispiel die Option „Kostengruppe M1” aus.</span><span class="sxs-lookup"><span data-stu-id="f3933-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="f3933-152">Verwenden Sie die Verknüpfung zum Speichern eines Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="f3933-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="f3933-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f3933-153">Close the page.</span></span>

