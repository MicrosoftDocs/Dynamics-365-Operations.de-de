--- 
title: "Rohmaterialien erstellen (nur Februar 2016)"
description: Diese Aufgabe konzentriert sich auf das Erstellen der Komponenten fertiger und halbfertiger Produkte.
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f1c10e0f8275d928c1455cd99105aece8780e7f0
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="9828f-103">Rohmaterialien erstellen (nur Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="9828f-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9828f-104">Diese Aufgabe konzentriert sich auf das Erstellen der Komponenten fertiger und halbfertiger Produkte.</span><span class="sxs-lookup"><span data-stu-id="9828f-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="9828f-105">Es ist die dritte Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="9828f-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="9828f-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="9828f-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="9828f-107">Das erste Material erstellen</span><span class="sxs-lookup"><span data-stu-id="9828f-107">Create the first material</span></span>
1. <span data-ttu-id="9828f-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="9828f-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="9828f-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9828f-109">Click New.</span></span>
3. <span data-ttu-id="9828f-110">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="9828f-111">Geben Sie für dieses Beispiel ITEM_A ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="9828f-112">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-113">Wählen Sie STD aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-113">Select STD.</span></span> <span data-ttu-id="9828f-114">STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="9828f-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="9828f-115">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-116">Wählen Sie z. B. „Audio” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-116">For example, select Audio.</span></span> <span data-ttu-id="9828f-117">Dies hat keine Auswirkungen auf Kostenberechnungen.</span><span class="sxs-lookup"><span data-stu-id="9828f-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="9828f-118">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-119">Wählen Sie „SiteWH” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-119">Select SiteWH.</span></span> <span data-ttu-id="9828f-120">Nur „Standort” und „Lagerort” werden für die Demonstration verwendet.</span><span class="sxs-lookup"><span data-stu-id="9828f-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="9828f-121">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-122">Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9828f-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="9828f-123">Wählen Sie „Keine” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-123">Select None.</span></span>  
8. <span data-ttu-id="9828f-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9828f-124">Click OK.</span></span>
9. <span data-ttu-id="9828f-125">Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="9828f-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="9828f-126">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="9828f-126">Click Default order settings.</span></span>
11. <span data-ttu-id="9828f-127">Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-128">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="9828f-129">Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-130">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="9828f-131">Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-132">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="9828f-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-133">Close the page.</span></span>
15. <span data-ttu-id="9828f-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-134">Close the page.</span></span>
16. <span data-ttu-id="9828f-135">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9828f-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9828f-136">Klicken Sie auf ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="9828f-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="9828f-137">Erweitern Sie den Abschnitt „Kosten verwalten”.</span><span class="sxs-lookup"><span data-stu-id="9828f-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="9828f-138">Geben Sie im Feld „Kostengruppe” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="9828f-139">Geben Sie für dieses Beispiel M2 ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="9828f-140">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="9828f-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="9828f-141">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="9828f-141">Click Item price.</span></span>
21. <span data-ttu-id="9828f-142">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9828f-142">Click New.</span></span>
22. <span data-ttu-id="9828f-143">Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-144">Wählen Sie für dieses Beispiel 10 aus. Dies ist der standardmäßige Nachkalkulationstyp.</span><span class="sxs-lookup"><span data-stu-id="9828f-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="9828f-145">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-146">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="9828f-147">Geben Sie im Feld "Preis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="9828f-148">Geben Sie für dieses Beispiel 10 ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="9828f-149">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9828f-149">Click Save.</span></span>
26. <span data-ttu-id="9828f-150">Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.</span><span class="sxs-lookup"><span data-stu-id="9828f-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="9828f-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-151">Close the page.</span></span>
28. <span data-ttu-id="9828f-152">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="9828f-153">Das zweite Material erstellen</span><span class="sxs-lookup"><span data-stu-id="9828f-153">Create the second material</span></span>
1. <span data-ttu-id="9828f-154">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9828f-154">Click New.</span></span>
2. <span data-ttu-id="9828f-155">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="9828f-156">Geben Sie für dieses Beispiel ITEM_B ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="9828f-157">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-158">Wählen Sie STD aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-158">Select STD.</span></span> <span data-ttu-id="9828f-159">STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="9828f-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="9828f-160">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-161">Wählen Sie z. B. „Audio” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-161">For example, select Audio.</span></span> <span data-ttu-id="9828f-162">Dies hat keine Auswirkungen auf Kostenberechnungen.</span><span class="sxs-lookup"><span data-stu-id="9828f-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="9828f-163">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-164">Wählen Sie „SiteWH” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-164">Select SiteWH.</span></span> <span data-ttu-id="9828f-165">Nur „Standort” und „Lagerort” werden für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9828f-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="9828f-166">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-167">Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9828f-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="9828f-168">Wählen Sie „Keine” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-168">Select None.</span></span>  
7. <span data-ttu-id="9828f-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9828f-169">Click OK.</span></span>
8. <span data-ttu-id="9828f-170">Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="9828f-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="9828f-171">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="9828f-171">Click Default order settings.</span></span>
10. <span data-ttu-id="9828f-172">Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-173">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="9828f-174">Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-175">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="9828f-176">Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-177">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="9828f-178">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-178">Close the page.</span></span>
14. <span data-ttu-id="9828f-179">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-179">Close the page.</span></span>
15. <span data-ttu-id="9828f-180">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9828f-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9828f-181">Klicken Sie auf ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="9828f-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="9828f-182">Erweitern Sie den Abschnitt „Kosten verwalten”.</span><span class="sxs-lookup"><span data-stu-id="9828f-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="9828f-183">Geben Sie im Feld „Kostengruppe” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="9828f-184">Geben Sie für dieses Beispiel M2 ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="9828f-185">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="9828f-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="9828f-186">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="9828f-186">Click Item price.</span></span>
20. <span data-ttu-id="9828f-187">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9828f-187">Click New.</span></span>
21. <span data-ttu-id="9828f-188">Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-189">Wählen Sie für dieses Beispiel 10 aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-189">For this example, select 10.</span></span> <span data-ttu-id="9828f-190">Das ist der standardmäßige Nachkalkulationstyp.</span><span class="sxs-lookup"><span data-stu-id="9828f-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="9828f-191">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-192">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="9828f-193">Geben Sie im Feld "Preis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="9828f-194">Geben Sie für die Demonstration 10 ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="9828f-195">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9828f-195">Click Save.</span></span>
25. <span data-ttu-id="9828f-196">Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.</span><span class="sxs-lookup"><span data-stu-id="9828f-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="9828f-197">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-197">Close the page.</span></span>
27. <span data-ttu-id="9828f-198">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="9828f-199">Das dritte Material erstellen</span><span class="sxs-lookup"><span data-stu-id="9828f-199">Create the third material</span></span>
1. <span data-ttu-id="9828f-200">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9828f-200">Click New.</span></span>
2. <span data-ttu-id="9828f-201">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="9828f-202">Geben Sie für die Demonstration ITEM_C ein</span><span class="sxs-lookup"><span data-stu-id="9828f-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="9828f-203">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-204">Wählen Sie STD aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-204">Select STD.</span></span> <span data-ttu-id="9828f-205">STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="9828f-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="9828f-206">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-207">Wählen Sie z. B. „Audio” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-207">For example, select Audio.</span></span> <span data-ttu-id="9828f-208">Dies hat keine Auswirkungen auf Kostenberechnungen.</span><span class="sxs-lookup"><span data-stu-id="9828f-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="9828f-209">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-210">Wählen Sie „SiteWH” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-210">Select SiteWH.</span></span> <span data-ttu-id="9828f-211">Nur „Standort” und „Lagerort” werden für die Demonstration verwendet.</span><span class="sxs-lookup"><span data-stu-id="9828f-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="9828f-212">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-213">Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9828f-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="9828f-214">Wählen Sie „Keine” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-214">Select None.</span></span>  
7. <span data-ttu-id="9828f-215">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9828f-215">Click OK.</span></span>
8. <span data-ttu-id="9828f-216">Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="9828f-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="9828f-217">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="9828f-217">Click Default order settings.</span></span>
10. <span data-ttu-id="9828f-218">Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-219">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="9828f-220">Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-221">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="9828f-222">Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-223">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="9828f-224">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-224">Close the page.</span></span>
14. <span data-ttu-id="9828f-225">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-225">Close the page.</span></span>
15. <span data-ttu-id="9828f-226">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9828f-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9828f-227">Klicken Sie auf ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="9828f-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="9828f-228">Erweitern Sie den Abschnitt „Kosten verwalten”.</span><span class="sxs-lookup"><span data-stu-id="9828f-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="9828f-229">Geben Sie im Feld „Kostengruppe” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="9828f-230">Geben Sie für dieses Beispiel M1 ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="9828f-231">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="9828f-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="9828f-232">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="9828f-232">Click Item price.</span></span>
20. <span data-ttu-id="9828f-233">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9828f-233">Click New.</span></span>
21. <span data-ttu-id="9828f-234">Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-235">Wählen Sie für dieses Beispiel 10 aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-235">For this example, select 10.</span></span> <span data-ttu-id="9828f-236">Das ist der standardmäßige Nachkalkulationstyp.</span><span class="sxs-lookup"><span data-stu-id="9828f-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="9828f-237">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="9828f-238">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="9828f-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="9828f-239">Geben Sie im Feld "Preis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="9828f-240">Geben Sie für dieses Beispiel 10 ein.</span><span class="sxs-lookup"><span data-stu-id="9828f-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="9828f-241">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9828f-241">Click Save.</span></span>
25. <span data-ttu-id="9828f-242">Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.</span><span class="sxs-lookup"><span data-stu-id="9828f-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="9828f-243">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-243">Close the page.</span></span>
27. <span data-ttu-id="9828f-244">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9828f-244">Close the page.</span></span>


