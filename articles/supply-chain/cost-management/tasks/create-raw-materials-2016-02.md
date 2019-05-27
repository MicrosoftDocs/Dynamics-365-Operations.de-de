---
title: Rohmaterialien erstellen (nur Februar 2016)
description: Diese Aufgabe konzentriert sich auf das Erstellen der Komponenten fertiger und halbfertiger Produkte.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 869acddf6f7e9754bb4952176ded4b22c74eaffd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563295"
---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="94ab2-103">Rohmaterialien erstellen (nur Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="94ab2-103">Create raw materials (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94ab2-104">Diese Aufgabe konzentriert sich auf das Erstellen der Komponenten fertiger und halbfertiger Produkte.</span><span class="sxs-lookup"><span data-stu-id="94ab2-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="94ab2-105">Es ist die dritte Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="94ab2-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="94ab2-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="94ab2-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="94ab2-107">Das erste Material erstellen</span><span class="sxs-lookup"><span data-stu-id="94ab2-107">Create the first material</span></span>
1. <span data-ttu-id="94ab2-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="94ab2-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="94ab2-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="94ab2-109">Click New.</span></span>
3. <span data-ttu-id="94ab2-110">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="94ab2-111">Geben Sie für dieses Beispiel ITEM_A ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="94ab2-112">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-113">Wählen Sie STD aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-113">Select STD.</span></span> <span data-ttu-id="94ab2-114">STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="94ab2-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="94ab2-115">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-116">Wählen Sie z. B. „Audio” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-116">For example, select Audio.</span></span> <span data-ttu-id="94ab2-117">Dies hat keine Auswirkungen auf Kostenberechnungen.</span><span class="sxs-lookup"><span data-stu-id="94ab2-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="94ab2-118">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-119">Wählen Sie „SiteWH” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-119">Select SiteWH.</span></span> <span data-ttu-id="94ab2-120">Nur „Standort” und „Lagerort” werden für die Demonstration verwendet.</span><span class="sxs-lookup"><span data-stu-id="94ab2-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="94ab2-121">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-122">Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="94ab2-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="94ab2-123">Wählen Sie „Keine” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-123">Select None.</span></span>  
8. <span data-ttu-id="94ab2-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="94ab2-124">Click OK.</span></span>
9. <span data-ttu-id="94ab2-125">Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="94ab2-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="94ab2-126">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="94ab2-126">Click Default order settings.</span></span>
11. <span data-ttu-id="94ab2-127">Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-128">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="94ab2-129">Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-130">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="94ab2-131">Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-132">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="94ab2-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-133">Close the page.</span></span>
15. <span data-ttu-id="94ab2-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-134">Close the page.</span></span>
16. <span data-ttu-id="94ab2-135">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="94ab2-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="94ab2-136">Klicken Sie auf ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="94ab2-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="94ab2-137">Erweitern Sie den Abschnitt „Kosten verwalten”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="94ab2-138">Geben Sie im Feld „Kostengruppe” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="94ab2-139">Geben Sie für dieses Beispiel M2 ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="94ab2-140">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="94ab2-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="94ab2-141">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-141">Click Item price.</span></span>
21. <span data-ttu-id="94ab2-142">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="94ab2-142">Click New.</span></span>
22. <span data-ttu-id="94ab2-143">Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-144">Wählen Sie für dieses Beispiel 10 aus. Dies ist der standardmäßige Nachkalkulationstyp.</span><span class="sxs-lookup"><span data-stu-id="94ab2-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="94ab2-145">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-146">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="94ab2-147">Geben Sie im Feld "Preis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="94ab2-148">Geben Sie für dieses Beispiel 10 ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="94ab2-149">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="94ab2-149">Click Save.</span></span>
26. <span data-ttu-id="94ab2-150">Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="94ab2-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-151">Close the page.</span></span>
28. <span data-ttu-id="94ab2-152">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="94ab2-153">Das zweite Material erstellen</span><span class="sxs-lookup"><span data-stu-id="94ab2-153">Create the second material</span></span>
1. <span data-ttu-id="94ab2-154">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="94ab2-154">Click New.</span></span>
2. <span data-ttu-id="94ab2-155">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="94ab2-156">Geben Sie für dieses Beispiel ITEM_B ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="94ab2-157">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-158">Wählen Sie STD aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-158">Select STD.</span></span> <span data-ttu-id="94ab2-159">STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="94ab2-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="94ab2-160">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-161">Wählen Sie z. B. „Audio” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-161">For example, select Audio.</span></span> <span data-ttu-id="94ab2-162">Dies hat keine Auswirkungen auf Kostenberechnungen.</span><span class="sxs-lookup"><span data-stu-id="94ab2-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="94ab2-163">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-164">Wählen Sie „SiteWH” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-164">Select SiteWH.</span></span> <span data-ttu-id="94ab2-165">Nur „Standort” und „Lagerort” werden für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="94ab2-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="94ab2-166">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-167">Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="94ab2-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="94ab2-168">Wählen Sie „Keine” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-168">Select None.</span></span>  
7. <span data-ttu-id="94ab2-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="94ab2-169">Click OK.</span></span>
8. <span data-ttu-id="94ab2-170">Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="94ab2-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="94ab2-171">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="94ab2-171">Click Default order settings.</span></span>
10. <span data-ttu-id="94ab2-172">Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-173">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="94ab2-174">Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-175">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="94ab2-176">Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-177">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="94ab2-178">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-178">Close the page.</span></span>
14. <span data-ttu-id="94ab2-179">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-179">Close the page.</span></span>
15. <span data-ttu-id="94ab2-180">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="94ab2-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="94ab2-181">Klicken Sie auf ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="94ab2-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="94ab2-182">Erweitern Sie den Abschnitt „Kosten verwalten”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="94ab2-183">Geben Sie im Feld „Kostengruppe” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="94ab2-184">Geben Sie für dieses Beispiel M2 ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="94ab2-185">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="94ab2-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="94ab2-186">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-186">Click Item price.</span></span>
20. <span data-ttu-id="94ab2-187">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="94ab2-187">Click New.</span></span>
21. <span data-ttu-id="94ab2-188">Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-189">Wählen Sie für dieses Beispiel 10 aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-189">For this example, select 10.</span></span> <span data-ttu-id="94ab2-190">Das ist der standardmäßige Nachkalkulationstyp.</span><span class="sxs-lookup"><span data-stu-id="94ab2-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="94ab2-191">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-192">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="94ab2-193">Geben Sie im Feld "Preis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="94ab2-194">Geben Sie für die Demonstration 10 ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="94ab2-195">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="94ab2-195">Click Save.</span></span>
25. <span data-ttu-id="94ab2-196">Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="94ab2-197">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-197">Close the page.</span></span>
27. <span data-ttu-id="94ab2-198">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="94ab2-199">Das dritte Material erstellen</span><span class="sxs-lookup"><span data-stu-id="94ab2-199">Create the third material</span></span>
1. <span data-ttu-id="94ab2-200">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="94ab2-200">Click New.</span></span>
2. <span data-ttu-id="94ab2-201">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="94ab2-202">Geben Sie für die Demonstration ITEM_C ein</span><span class="sxs-lookup"><span data-stu-id="94ab2-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="94ab2-203">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-204">Wählen Sie STD aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-204">Select STD.</span></span> <span data-ttu-id="94ab2-205">STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="94ab2-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="94ab2-206">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-207">Wählen Sie z. B. „Audio” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-207">For example, select Audio.</span></span> <span data-ttu-id="94ab2-208">Dies hat keine Auswirkungen auf Kostenberechnungen.</span><span class="sxs-lookup"><span data-stu-id="94ab2-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="94ab2-209">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-210">Wählen Sie „SiteWH” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-210">Select SiteWH.</span></span> <span data-ttu-id="94ab2-211">Nur „Standort” und „Lagerort” werden für die Demonstration verwendet.</span><span class="sxs-lookup"><span data-stu-id="94ab2-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="94ab2-212">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-213">Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="94ab2-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="94ab2-214">Wählen Sie „Keine” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-214">Select None.</span></span>  
7. <span data-ttu-id="94ab2-215">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="94ab2-215">Click OK.</span></span>
8. <span data-ttu-id="94ab2-216">Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="94ab2-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="94ab2-217">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="94ab2-217">Click Default order settings.</span></span>
10. <span data-ttu-id="94ab2-218">Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-219">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="94ab2-220">Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-221">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="94ab2-222">Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-223">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="94ab2-224">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-224">Close the page.</span></span>
14. <span data-ttu-id="94ab2-225">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-225">Close the page.</span></span>
15. <span data-ttu-id="94ab2-226">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="94ab2-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="94ab2-227">Klicken Sie auf ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="94ab2-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="94ab2-228">Erweitern Sie den Abschnitt „Kosten verwalten”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="94ab2-229">Geben Sie im Feld „Kostengruppe” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="94ab2-230">Geben Sie für dieses Beispiel M1 ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="94ab2-231">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="94ab2-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="94ab2-232">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-232">Click Item price.</span></span>
20. <span data-ttu-id="94ab2-233">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="94ab2-233">Click New.</span></span>
21. <span data-ttu-id="94ab2-234">Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-235">Wählen Sie für dieses Beispiel 10 aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-235">For this example, select 10.</span></span> <span data-ttu-id="94ab2-236">Das ist der standardmäßige Nachkalkulationstyp.</span><span class="sxs-lookup"><span data-stu-id="94ab2-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="94ab2-237">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="94ab2-238">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="94ab2-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="94ab2-239">Geben Sie im Feld "Preis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="94ab2-240">Geben Sie für dieses Beispiel 10 ein.</span><span class="sxs-lookup"><span data-stu-id="94ab2-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="94ab2-241">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="94ab2-241">Click Save.</span></span>
25. <span data-ttu-id="94ab2-242">Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.</span><span class="sxs-lookup"><span data-stu-id="94ab2-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="94ab2-243">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-243">Close the page.</span></span>
27. <span data-ttu-id="94ab2-244">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94ab2-244">Close the page.</span></span>

