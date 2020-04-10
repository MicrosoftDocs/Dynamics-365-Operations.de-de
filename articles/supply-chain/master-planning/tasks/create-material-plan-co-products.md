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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148077"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="439e9-103">Erstellen Sie einen Materialplan für Co-Produkte</span><span class="sxs-lookup"><span data-stu-id="439e9-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="439e9-104">Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.</span><span class="sxs-lookup"><span data-stu-id="439e9-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="439e9-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="439e9-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="439e9-106">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="439e9-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="439e9-107">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="439e9-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="439e9-108">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="439e9-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="439e9-109">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="439e9-109">Click New.</span></span>
4. <span data-ttu-id="439e9-110">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="439e9-110">Click Sales order.</span></span>
5. <span data-ttu-id="439e9-111">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="439e9-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="439e9-112">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="439e9-112">Example: US-001</span></span>  
6. <span data-ttu-id="439e9-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="439e9-113">Click OK.</span></span>
7. <span data-ttu-id="439e9-114">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="439e9-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="439e9-115">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="439e9-115">Example: P6003</span></span>  
8. <span data-ttu-id="439e9-116">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="439e9-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="439e9-117">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="439e9-117">Example: 50000</span></span>  
9. <span data-ttu-id="439e9-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="439e9-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="439e9-119">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="439e9-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="439e9-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="439e9-120">Close the page.</span></span>
2. <span data-ttu-id="439e9-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="439e9-121">Close the page.</span></span>
3. <span data-ttu-id="439e9-122">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="439e9-122">Click Master planning.</span></span>
4. <span data-ttu-id="439e9-123">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="439e9-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="439e9-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="439e9-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="439e9-125">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="439e9-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="439e9-126">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="439e9-126">Click Run.</span></span>
7. <span data-ttu-id="439e9-127">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="439e9-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="439e9-128">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="439e9-128">Click Filter.</span></span>
9. <span data-ttu-id="439e9-129">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="439e9-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="439e9-130">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="439e9-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="439e9-131">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="439e9-131">Example: P6003</span></span>  
11. <span data-ttu-id="439e9-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="439e9-132">Click OK.</span></span>
12. <span data-ttu-id="439e9-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="439e9-133">Click OK.</span></span>
13. <span data-ttu-id="439e9-134">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="439e9-134">Click Planned orders.</span></span>
14. <span data-ttu-id="439e9-135">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="439e9-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="439e9-136">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="439e9-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="439e9-137">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="439e9-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="439e9-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="439e9-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="439e9-139">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="439e9-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="439e9-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="439e9-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="439e9-141">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="439e9-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="439e9-142">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="439e9-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="439e9-143">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="439e9-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="439e9-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="439e9-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="439e9-145">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="439e9-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="439e9-146">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="439e9-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="439e9-147">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="439e9-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="439e9-148">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="439e9-148">Click New.</span></span>
4. <span data-ttu-id="439e9-149">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="439e9-149">Click Sales order.</span></span>
5. <span data-ttu-id="439e9-150">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="439e9-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="439e9-151">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="439e9-151">Example: US-001</span></span>  
6. <span data-ttu-id="439e9-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="439e9-152">Click OK.</span></span>
7. <span data-ttu-id="439e9-153">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="439e9-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="439e9-154">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="439e9-154">Example: P6003</span></span>  
8. <span data-ttu-id="439e9-155">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="439e9-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="439e9-156">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="439e9-156">Example: 50000</span></span>  
9. <span data-ttu-id="439e9-157">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="439e9-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="439e9-158">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="439e9-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="439e9-159">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="439e9-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="439e9-160">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="439e9-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="439e9-161">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="439e9-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="439e9-162">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="439e9-162">Click Run.</span></span>
4. <span data-ttu-id="439e9-163">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="439e9-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="439e9-164">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="439e9-164">Click Filter.</span></span>
6. <span data-ttu-id="439e9-165">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="439e9-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="439e9-166">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="439e9-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="439e9-167">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="439e9-167">Example: P6003</span></span>  
8. <span data-ttu-id="439e9-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="439e9-168">Click OK.</span></span>
9. <span data-ttu-id="439e9-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="439e9-169">Click OK.</span></span>
10. <span data-ttu-id="439e9-170">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="439e9-170">Click Planned orders.</span></span>
11. <span data-ttu-id="439e9-171">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="439e9-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="439e9-172">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="439e9-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="439e9-173">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="439e9-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="439e9-174">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="439e9-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="439e9-175">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="439e9-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="439e9-176">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="439e9-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="439e9-177">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="439e9-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="439e9-178">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="439e9-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="439e9-179">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="439e9-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="439e9-180">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="439e9-180">Close the page.</span></span>
17. <span data-ttu-id="439e9-181">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="439e9-181">Click Master planning.</span></span>
18. <span data-ttu-id="439e9-182">Wechseln Sie zu "Produktprogrammplan" > Einrichten > Produktprogrammplan-Parameter.</span><span class="sxs-lookup"><span data-stu-id="439e9-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="439e9-183">Wählen Sie im Feld "Alle Planungsprozessfelder deaktivieren" Nein aus.</span><span class="sxs-lookup"><span data-stu-id="439e9-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="439e9-184">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="439e9-184">Close the page.</span></span>

