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
ms.sourcegitcommit: 273ced77a61d485426c0830556e4401e782e86c4
ms.openlocfilehash: 1ba2ae3ad92149636714701448d4dac8296d6613
ms.contentlocale: de-de
ms.lasthandoff: 10/24/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="05355-103">Routen erstellen (nur Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="05355-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05355-104">Diese Aufgabe konzentriert sich auf das Erstellen der Produktionsarbeitspläne für ein fertiges Produkt und ein halbfertiges Produkt.</span><span class="sxs-lookup"><span data-stu-id="05355-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="05355-105">Es ist die fünfte Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="05355-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="05355-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="05355-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="05355-107">Arbeitsplan für ein halbfertiges Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="05355-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="05355-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="05355-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="05355-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05355-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="05355-110">Wählen Sie die Artikelnummer BOM_2 aus.</span><span class="sxs-lookup"><span data-stu-id="05355-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="05355-111">Klicken Sie im Aktivitätsbereich auf "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="05355-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="05355-112">Klicken Sie auf "Arbeitsplan".</span><span class="sxs-lookup"><span data-stu-id="05355-112">Click Route.</span></span>
5. <span data-ttu-id="05355-113">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05355-113">Click New.</span></span>
6. <span data-ttu-id="05355-114">Klicken Sie auf Arbeitsplan und Arbeitsplanversion.</span><span class="sxs-lookup"><span data-stu-id="05355-114">Click Route and route version.</span></span>
7. <span data-ttu-id="05355-115">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05355-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="05355-116">Geben Sie beispielsweise ROUTE_2 ein.</span><span class="sxs-lookup"><span data-stu-id="05355-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="05355-117">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05355-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="05355-118">Geben Sie für dieses Beispiel „Standort 1” ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05355-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="05355-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05355-119">Click OK.</span></span>
10. <span data-ttu-id="05355-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05355-120">Click New.</span></span>
11. <span data-ttu-id="05355-121">Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05355-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="05355-122">Wählen Sie für dieses Beispiel „Zusammenstellung” aus.</span><span class="sxs-lookup"><span data-stu-id="05355-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="05355-123">Geben Sie im Feld "Laufzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="05355-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="05355-124">Geben Sie beispielsweise "1" ein.</span><span class="sxs-lookup"><span data-stu-id="05355-124">For example, type 1.</span></span> <span data-ttu-id="05355-125">Ausführungszeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="05355-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="05355-126">Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05355-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="05355-127">Wählen Sie für dieses Beispiel „STD” aus.</span><span class="sxs-lookup"><span data-stu-id="05355-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="05355-128">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="05355-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="05355-129">Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05355-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="05355-130">Wählen Sie für dieses Beispiel „Zusammenstellung” aus.</span><span class="sxs-lookup"><span data-stu-id="05355-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="05355-131">Klicken Sie auf die Registerkarte 'Zeiten'.</span><span class="sxs-lookup"><span data-stu-id="05355-131">Click the Times tab.</span></span>
17. <span data-ttu-id="05355-132">Geben Sie im Feld „Rüstzeit” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="05355-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="05355-133">Geben Sie für dieses Beispiel 1 ein.</span><span class="sxs-lookup"><span data-stu-id="05355-133">For this example, type 1.</span></span> <span data-ttu-id="05355-134">Rüstzeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="05355-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="05355-135">Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.</span><span class="sxs-lookup"><span data-stu-id="05355-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="05355-136">Klicken Sie auf Genehmigen.</span><span class="sxs-lookup"><span data-stu-id="05355-136">Click Approve.</span></span>
20. <span data-ttu-id="05355-137">Wählen Sie „Ja” aus in „Möchten Sie auch den Arbeitsplan genehmigen?”.</span><span class="sxs-lookup"><span data-stu-id="05355-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="05355-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05355-138">Click OK.</span></span>
22. <span data-ttu-id="05355-139">Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.</span><span class="sxs-lookup"><span data-stu-id="05355-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="05355-140">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="05355-140">Click Activate.</span></span>
24. <span data-ttu-id="05355-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05355-141">Close the page.</span></span>
25. <span data-ttu-id="05355-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05355-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="05355-143">Arbeitsplan für ein fertiges Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="05355-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="05355-144">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05355-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="05355-145">Wählen Sie die Artikelnummer BOM_1 aus.</span><span class="sxs-lookup"><span data-stu-id="05355-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="05355-146">Klicken Sie im Aktivitätsbereich auf "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="05355-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="05355-147">Klicken Sie auf "Arbeitsplan".</span><span class="sxs-lookup"><span data-stu-id="05355-147">Click Route.</span></span>
4. <span data-ttu-id="05355-148">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05355-148">Click New.</span></span>
5. <span data-ttu-id="05355-149">Klicken Sie auf Arbeitsplan und Arbeitsplanversion.</span><span class="sxs-lookup"><span data-stu-id="05355-149">Click Route and route version.</span></span>
6. <span data-ttu-id="05355-150">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05355-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="05355-151">Geben Sie für dieses Beispiel ROUTE_1 ein.</span><span class="sxs-lookup"><span data-stu-id="05355-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="05355-152">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05355-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="05355-153">Geben Sie für dieses Beispiel „Standort 1” ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05355-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="05355-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05355-154">Click OK.</span></span>
9. <span data-ttu-id="05355-155">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05355-155">Click New.</span></span>
10. <span data-ttu-id="05355-156">Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05355-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="05355-157">Wählen Sie für dieses Beispiel „Verpackung” aus.</span><span class="sxs-lookup"><span data-stu-id="05355-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="05355-158">Geben Sie im Feld "Laufzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="05355-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="05355-159">Geben Sie für dieses Beispiel 1 ein.</span><span class="sxs-lookup"><span data-stu-id="05355-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="05355-160">Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05355-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="05355-161">Wählen Sie für dieses Beispiel „STD” aus.</span><span class="sxs-lookup"><span data-stu-id="05355-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="05355-162">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="05355-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="05355-163">Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05355-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="05355-164">Wählen Sie für dieses Beispiel „Verpackung” aus.</span><span class="sxs-lookup"><span data-stu-id="05355-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="05355-165">Klicken Sie auf die Registerkarte 'Zeiten'.</span><span class="sxs-lookup"><span data-stu-id="05355-165">Click the Times tab.</span></span>
16. <span data-ttu-id="05355-166">Geben Sie im Feld „Rüstzeit” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="05355-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="05355-167">Geben Sie für dieses Beispiel 1 ein.</span><span class="sxs-lookup"><span data-stu-id="05355-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="05355-168">Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.</span><span class="sxs-lookup"><span data-stu-id="05355-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="05355-169">Klicken Sie auf Genehmigen.</span><span class="sxs-lookup"><span data-stu-id="05355-169">Click Approve.</span></span>
19. <span data-ttu-id="05355-170">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05355-170">Click OK.</span></span>
20. <span data-ttu-id="05355-171">Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.</span><span class="sxs-lookup"><span data-stu-id="05355-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="05355-172">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="05355-172">Click Activate.</span></span>
22. <span data-ttu-id="05355-173">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05355-173">Close the page.</span></span>
23. <span data-ttu-id="05355-174">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05355-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="05355-175">Automatischen Verbrauch der Rüstzeit aktivieren</span><span class="sxs-lookup"><span data-stu-id="05355-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="05355-176">Wechseln Sie zu „Produktionssteuerung” > „Einrichten”  >„Arbeitspläne” > „Arbeitsplangruppen”.</span><span class="sxs-lookup"><span data-stu-id="05355-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="05355-177">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05355-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="05355-178">Wählen Sie STD in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="05355-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="05355-179">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="05355-179">Click Edit.</span></span>
4. <span data-ttu-id="05355-180">Wählen Sie „Ja” im Feld „Rüstzeit” aus.</span><span class="sxs-lookup"><span data-stu-id="05355-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="05355-181">Rüstzeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="05355-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="05355-182">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05355-182">Click Save.</span></span>
6. <span data-ttu-id="05355-183">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05355-183">Close the page.</span></span>


