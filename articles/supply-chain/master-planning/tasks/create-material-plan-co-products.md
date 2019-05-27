---
title: Erstellen Sie einen Materialplan für Co-Produkte
description: Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555999"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8cfa1-103">Erstellen Sie einen Materialplan für Co-Produkte</span><span class="sxs-lookup"><span data-stu-id="8cfa1-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8cfa1-104">Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="8cfa1-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="8cfa1-106">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="8cfa1-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="8cfa1-107">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="8cfa1-108">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="8cfa1-109">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-109">Click New.</span></span>
4. <span data-ttu-id="8cfa1-110">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-110">Click Sales order.</span></span>
5. <span data-ttu-id="8cfa1-111">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="8cfa1-112">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="8cfa1-112">Example: US-001</span></span>  
6. <span data-ttu-id="8cfa1-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-113">Click OK.</span></span>
7. <span data-ttu-id="8cfa1-114">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8cfa1-115">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="8cfa1-115">Example: P6003</span></span>  
8. <span data-ttu-id="8cfa1-116">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8cfa1-117">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="8cfa1-117">Example: 50000</span></span>  
9. <span data-ttu-id="8cfa1-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8cfa1-119">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="8cfa1-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="8cfa1-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-120">Close the page.</span></span>
2. <span data-ttu-id="8cfa1-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-121">Close the page.</span></span>
3. <span data-ttu-id="8cfa1-122">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-122">Click Master planning.</span></span>
4. <span data-ttu-id="8cfa1-123">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8cfa1-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8cfa1-125">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="8cfa1-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="8cfa1-126">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-126">Click Run.</span></span>
7. <span data-ttu-id="8cfa1-127">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="8cfa1-128">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-128">Click Filter.</span></span>
9. <span data-ttu-id="8cfa1-129">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="8cfa1-130">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8cfa1-131">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="8cfa1-131">Example: P6003</span></span>  
11. <span data-ttu-id="8cfa1-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-132">Click OK.</span></span>
12. <span data-ttu-id="8cfa1-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-133">Click OK.</span></span>
13. <span data-ttu-id="8cfa1-134">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-134">Click Planned orders.</span></span>
14. <span data-ttu-id="8cfa1-135">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8cfa1-136">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="8cfa1-137">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="8cfa1-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8cfa1-139">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="8cfa1-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="8cfa1-141">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="8cfa1-142">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8cfa1-143">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="8cfa1-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="8cfa1-145">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="8cfa1-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="8cfa1-146">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="8cfa1-147">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="8cfa1-148">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-148">Click New.</span></span>
4. <span data-ttu-id="8cfa1-149">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-149">Click Sales order.</span></span>
5. <span data-ttu-id="8cfa1-150">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="8cfa1-151">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="8cfa1-151">Example: US-001</span></span>  
6. <span data-ttu-id="8cfa1-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-152">Click OK.</span></span>
7. <span data-ttu-id="8cfa1-153">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8cfa1-154">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="8cfa1-154">Example: P6003</span></span>  
8. <span data-ttu-id="8cfa1-155">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8cfa1-156">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="8cfa1-156">Example: 50000</span></span>  
9. <span data-ttu-id="8cfa1-157">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8cfa1-158">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="8cfa1-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="8cfa1-159">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="8cfa1-160">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8cfa1-161">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="8cfa1-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="8cfa1-162">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-162">Click Run.</span></span>
4. <span data-ttu-id="8cfa1-163">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="8cfa1-164">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-164">Click Filter.</span></span>
6. <span data-ttu-id="8cfa1-165">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="8cfa1-166">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8cfa1-167">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="8cfa1-167">Example: P6003</span></span>  
8. <span data-ttu-id="8cfa1-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-168">Click OK.</span></span>
9. <span data-ttu-id="8cfa1-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-169">Click OK.</span></span>
10. <span data-ttu-id="8cfa1-170">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-170">Click Planned orders.</span></span>
11. <span data-ttu-id="8cfa1-171">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8cfa1-172">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="8cfa1-173">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="8cfa1-174">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8cfa1-175">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="8cfa1-176">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8cfa1-177">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="8cfa1-178">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8cfa1-179">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="8cfa1-180">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-180">Close the page.</span></span>
17. <span data-ttu-id="8cfa1-181">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="8cfa1-181">Click Master planning.</span></span>
18. <span data-ttu-id="8cfa1-182">Wechseln Sie zu "Produktprogrammplan" > Einrichten > Produktprogrammplan-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="8cfa1-183">Wählen Sie im Feld "Alle Planungsprozessfelder deaktivieren" Nein aus.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="8cfa1-184">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8cfa1-184">Close the page.</span></span>

