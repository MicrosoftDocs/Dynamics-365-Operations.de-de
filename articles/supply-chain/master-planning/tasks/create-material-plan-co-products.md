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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "337140"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="6e218-103">Erstellen Sie einen Materialplan für Co-Produkte</span><span class="sxs-lookup"><span data-stu-id="6e218-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e218-104">Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.</span><span class="sxs-lookup"><span data-stu-id="6e218-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="6e218-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="6e218-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="6e218-106">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="6e218-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="6e218-107">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="6e218-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="6e218-108">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="6e218-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="6e218-109">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="6e218-109">Click New.</span></span>
4. <span data-ttu-id="6e218-110">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="6e218-110">Click Sales order.</span></span>
5. <span data-ttu-id="6e218-111">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e218-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="6e218-112">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="6e218-112">Example: US-001</span></span>  
6. <span data-ttu-id="6e218-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6e218-113">Click OK.</span></span>
7. <span data-ttu-id="6e218-114">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e218-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6e218-115">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="6e218-115">Example: P6003</span></span>  
8. <span data-ttu-id="6e218-116">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="6e218-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6e218-117">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="6e218-117">Example: 50000</span></span>  
9. <span data-ttu-id="6e218-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6e218-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="6e218-119">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="6e218-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="6e218-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6e218-120">Close the page.</span></span>
2. <span data-ttu-id="6e218-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6e218-121">Close the page.</span></span>
3. <span data-ttu-id="6e218-122">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="6e218-122">Click Master planning.</span></span>
4. <span data-ttu-id="6e218-123">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e218-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6e218-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e218-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6e218-125">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="6e218-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="6e218-126">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="6e218-126">Click Run.</span></span>
7. <span data-ttu-id="6e218-127">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="6e218-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="6e218-128">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="6e218-128">Click Filter.</span></span>
9. <span data-ttu-id="6e218-129">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="6e218-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="6e218-130">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e218-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="6e218-131">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="6e218-131">Example: P6003</span></span>  
11. <span data-ttu-id="6e218-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6e218-132">Click OK.</span></span>
12. <span data-ttu-id="6e218-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6e218-133">Click OK.</span></span>
13. <span data-ttu-id="6e218-134">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="6e218-134">Click Planned orders.</span></span>
14. <span data-ttu-id="6e218-135">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6e218-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6e218-136">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="6e218-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="6e218-137">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="6e218-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="6e218-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e218-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6e218-139">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e218-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="6e218-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e218-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="6e218-141">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="6e218-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="6e218-142">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e218-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6e218-143">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6e218-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="6e218-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6e218-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="6e218-145">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="6e218-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="6e218-146">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="6e218-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="6e218-147">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="6e218-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="6e218-148">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="6e218-148">Click New.</span></span>
4. <span data-ttu-id="6e218-149">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="6e218-149">Click Sales order.</span></span>
5. <span data-ttu-id="6e218-150">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e218-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="6e218-151">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="6e218-151">Example: US-001</span></span>  
6. <span data-ttu-id="6e218-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6e218-152">Click OK.</span></span>
7. <span data-ttu-id="6e218-153">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e218-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6e218-154">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="6e218-154">Example: P6003</span></span>  
8. <span data-ttu-id="6e218-155">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="6e218-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6e218-156">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="6e218-156">Example: 50000</span></span>  
9. <span data-ttu-id="6e218-157">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6e218-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="6e218-158">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="6e218-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="6e218-159">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e218-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="6e218-160">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e218-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6e218-161">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="6e218-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="6e218-162">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="6e218-162">Click Run.</span></span>
4. <span data-ttu-id="6e218-163">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="6e218-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="6e218-164">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="6e218-164">Click Filter.</span></span>
6. <span data-ttu-id="6e218-165">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="6e218-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="6e218-166">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e218-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="6e218-167">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="6e218-167">Example: P6003</span></span>  
8. <span data-ttu-id="6e218-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6e218-168">Click OK.</span></span>
9. <span data-ttu-id="6e218-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6e218-169">Click OK.</span></span>
10. <span data-ttu-id="6e218-170">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="6e218-170">Click Planned orders.</span></span>
11. <span data-ttu-id="6e218-171">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6e218-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6e218-172">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="6e218-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="6e218-173">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="6e218-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="6e218-174">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e218-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6e218-175">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e218-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="6e218-176">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e218-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6e218-177">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="6e218-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="6e218-178">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e218-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6e218-179">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6e218-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="6e218-180">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6e218-180">Close the page.</span></span>
17. <span data-ttu-id="6e218-181">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="6e218-181">Click Master planning.</span></span>
18. <span data-ttu-id="6e218-182">Wechseln Sie zu "Produktprogrammplan" > Einrichten > Produktprogrammplan-Parameter.</span><span class="sxs-lookup"><span data-stu-id="6e218-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="6e218-183">Wählen Sie im Feld "Alle Planungsprozessfelder deaktivieren" Nein aus.</span><span class="sxs-lookup"><span data-stu-id="6e218-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="6e218-184">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6e218-184">Close the page.</span></span>

