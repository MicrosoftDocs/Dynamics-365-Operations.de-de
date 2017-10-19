--- 
title: Routen erstellen (nur Februar 2016)
description: "Diese Aufgabe konzentriert sich auf das Erstellen der Produktionsarbeitspläne für ein fertiges Produkt und ein halbfertiges Produkt."
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
ms.openlocfilehash: 2df913543d89a502aecfe7e2fe61265a8a1a121c
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="27aba-103">Routen erstellen (nur Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="27aba-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27aba-104">Diese Aufgabe konzentriert sich auf das Erstellen der Produktionsarbeitspläne für ein fertiges Produkt und ein halbfertiges Produkt.</span><span class="sxs-lookup"><span data-stu-id="27aba-104">This task focuses on creating the production routes for a finished product and and a semi-finished product.</span></span> <span data-ttu-id="27aba-105">Es ist die fünfte Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="27aba-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="27aba-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="27aba-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="27aba-107">Arbeitsplan für ein halbfertiges Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="27aba-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="27aba-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="27aba-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="27aba-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="27aba-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="27aba-110">Wählen Sie die Artikelnummer BOM_2 aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="27aba-111">Klicken Sie im Aktivitätsbereich auf "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="27aba-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="27aba-112">Klicken Sie auf "Arbeitsplan".</span><span class="sxs-lookup"><span data-stu-id="27aba-112">Click Route.</span></span>
5. <span data-ttu-id="27aba-113">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="27aba-113">Click New.</span></span>
6. <span data-ttu-id="27aba-114">Klicken Sie auf Arbeitsplan und Arbeitsplanversion.</span><span class="sxs-lookup"><span data-stu-id="27aba-114">Click Route and route version.</span></span>
7. <span data-ttu-id="27aba-115">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="27aba-116">Geben Sie beispielsweise ROUTE_2 ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="27aba-117">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="27aba-118">Geben Sie für dieses Beispiel „Standort 1” ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="27aba-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="27aba-119">Click OK.</span></span>
10. <span data-ttu-id="27aba-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="27aba-120">Click New.</span></span>
11. <span data-ttu-id="27aba-121">Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="27aba-122">Wählen Sie für dieses Beispiel „Zusammenstellung” aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="27aba-123">Geben Sie im Feld "Laufzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="27aba-124">Geben Sie beispielsweise "1" ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-124">For example, type 1.</span></span> <span data-ttu-id="27aba-125">Ausführungszeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="27aba-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="27aba-126">Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="27aba-127">Wählen Sie für dieses Beispiel „STD” aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="27aba-128">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="27aba-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="27aba-129">Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="27aba-130">Wählen Sie für dieses Beispiel „Zusammenstellung” aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="27aba-131">Klicken Sie auf die Registerkarte 'Zeiten'.</span><span class="sxs-lookup"><span data-stu-id="27aba-131">Click the Times tab.</span></span>
17. <span data-ttu-id="27aba-132">Geben Sie im Feld „Rüstzeit” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="27aba-133">Geben Sie für dieses Beispiel 1 ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-133">For this example, type 1.</span></span> <span data-ttu-id="27aba-134">Rüstzeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="27aba-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="27aba-135">Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.</span><span class="sxs-lookup"><span data-stu-id="27aba-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="27aba-136">Klicken Sie auf Genehmigen.</span><span class="sxs-lookup"><span data-stu-id="27aba-136">Click Approve.</span></span>
20. <span data-ttu-id="27aba-137">Wählen Sie „Ja” aus in „Möchten Sie auch den Arbeitsplan genehmigen?”.</span><span class="sxs-lookup"><span data-stu-id="27aba-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="27aba-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="27aba-138">Click OK.</span></span>
22. <span data-ttu-id="27aba-139">Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.</span><span class="sxs-lookup"><span data-stu-id="27aba-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="27aba-140">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27aba-140">Click Activate.</span></span>
24. <span data-ttu-id="27aba-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="27aba-141">Close the page.</span></span>
25. <span data-ttu-id="27aba-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="27aba-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="27aba-143">Arbeitsplan für ein fertiges Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="27aba-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="27aba-144">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="27aba-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="27aba-145">Wählen Sie die Artikelnummer BOM_1 aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="27aba-146">Klicken Sie im Aktivitätsbereich auf "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="27aba-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="27aba-147">Klicken Sie auf "Arbeitsplan".</span><span class="sxs-lookup"><span data-stu-id="27aba-147">Click Route.</span></span>
4. <span data-ttu-id="27aba-148">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="27aba-148">Click New.</span></span>
5. <span data-ttu-id="27aba-149">Klicken Sie auf Arbeitsplan und Arbeitsplanversion.</span><span class="sxs-lookup"><span data-stu-id="27aba-149">Click Route and route version.</span></span>
6. <span data-ttu-id="27aba-150">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="27aba-151">Geben Sie für dieses Beispiel ROUTE_1 ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="27aba-152">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="27aba-153">Geben Sie für dieses Beispiel „Standort 1” ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="27aba-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="27aba-154">Click OK.</span></span>
9. <span data-ttu-id="27aba-155">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="27aba-155">Click New.</span></span>
10. <span data-ttu-id="27aba-156">Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="27aba-157">Wählen Sie für dieses Beispiel „Verpackung” aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="27aba-158">Geben Sie im Feld "Laufzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="27aba-159">Geben Sie für dieses Beispiel 1 ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="27aba-160">Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="27aba-161">Wählen Sie für dieses Beispiel „STD” aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="27aba-162">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="27aba-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="27aba-163">Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="27aba-164">Wählen Sie für dieses Beispiel „Verpackung” aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="27aba-165">Klicken Sie auf die Registerkarte 'Zeiten'.</span><span class="sxs-lookup"><span data-stu-id="27aba-165">Click the Times tab.</span></span>
16. <span data-ttu-id="27aba-166">Geben Sie im Feld „Rüstzeit” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="27aba-167">Geben Sie für dieses Beispiel 1 ein.</span><span class="sxs-lookup"><span data-stu-id="27aba-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="27aba-168">Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.</span><span class="sxs-lookup"><span data-stu-id="27aba-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="27aba-169">Klicken Sie auf Genehmigen.</span><span class="sxs-lookup"><span data-stu-id="27aba-169">Click Approve.</span></span>
19. <span data-ttu-id="27aba-170">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="27aba-170">Click OK.</span></span>
20. <span data-ttu-id="27aba-171">Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.</span><span class="sxs-lookup"><span data-stu-id="27aba-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="27aba-172">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27aba-172">Click Activate.</span></span>
22. <span data-ttu-id="27aba-173">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="27aba-173">Close the page.</span></span>
23. <span data-ttu-id="27aba-174">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="27aba-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="27aba-175">Automatischen Verbrauch der Rüstzeit aktivieren</span><span class="sxs-lookup"><span data-stu-id="27aba-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="27aba-176">Wechseln Sie zu „Produktionssteuerung” > „Einrichten”  >„Arbeitspläne” > „Arbeitsplangruppen”.</span><span class="sxs-lookup"><span data-stu-id="27aba-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="27aba-177">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="27aba-178">Wählen Sie STD in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="27aba-179">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="27aba-179">Click Edit.</span></span>
4. <span data-ttu-id="27aba-180">Wählen Sie „Ja” im Feld „Rüstzeit” aus.</span><span class="sxs-lookup"><span data-stu-id="27aba-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="27aba-181">Rüstzeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="27aba-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="27aba-182">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="27aba-182">Click Save.</span></span>
6. <span data-ttu-id="27aba-183">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="27aba-183">Close the page.</span></span>


