---
title: Erstellen Sie einen Materialplan für Co-Produkte
description: Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8e9067cdd8851da31c07a92217001e447f400d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983390"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="c7eee-103">Erstellen Sie einen Materialplan für Co-Produkte</span><span class="sxs-lookup"><span data-stu-id="c7eee-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7eee-104">Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.</span><span class="sxs-lookup"><span data-stu-id="c7eee-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="c7eee-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="c7eee-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="c7eee-106">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="c7eee-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="c7eee-107">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="c7eee-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="c7eee-108">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="c7eee-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="c7eee-109">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="c7eee-109">Click New.</span></span>
4. <span data-ttu-id="c7eee-110">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="c7eee-110">Click Sales order.</span></span>
5. <span data-ttu-id="c7eee-111">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c7eee-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="c7eee-112">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="c7eee-112">Example: US-001</span></span>  
6. <span data-ttu-id="c7eee-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c7eee-113">Click OK.</span></span>
7. <span data-ttu-id="c7eee-114">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c7eee-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c7eee-115">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="c7eee-115">Example: P6003</span></span>  
8. <span data-ttu-id="c7eee-116">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c7eee-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c7eee-117">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="c7eee-117">Example: 50000</span></span>  
9. <span data-ttu-id="c7eee-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c7eee-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="c7eee-119">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="c7eee-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="c7eee-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c7eee-120">Close the page.</span></span>
2. <span data-ttu-id="c7eee-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c7eee-121">Close the page.</span></span>
3. <span data-ttu-id="c7eee-122">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="c7eee-122">Click Master planning.</span></span>
4. <span data-ttu-id="c7eee-123">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c7eee-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c7eee-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c7eee-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7eee-125">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="c7eee-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="c7eee-126">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="c7eee-126">Click Run.</span></span>
7. <span data-ttu-id="c7eee-127">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="c7eee-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="c7eee-128">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="c7eee-128">Click Filter.</span></span>
9. <span data-ttu-id="c7eee-129">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="c7eee-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="c7eee-130">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c7eee-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="c7eee-131">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="c7eee-131">Example: P6003</span></span>  
11. <span data-ttu-id="c7eee-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c7eee-132">Click OK.</span></span>
12. <span data-ttu-id="c7eee-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c7eee-133">Click OK.</span></span>
13. <span data-ttu-id="c7eee-134">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="c7eee-134">Click Planned orders.</span></span>
14. <span data-ttu-id="c7eee-135">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c7eee-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c7eee-136">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="c7eee-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="c7eee-137">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c7eee-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="c7eee-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c7eee-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c7eee-139">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7eee-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="c7eee-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c7eee-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="c7eee-141">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="c7eee-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="c7eee-142">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c7eee-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7eee-143">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c7eee-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="c7eee-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c7eee-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="c7eee-145">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="c7eee-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="c7eee-146">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="c7eee-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="c7eee-147">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="c7eee-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="c7eee-148">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="c7eee-148">Click New.</span></span>
4. <span data-ttu-id="c7eee-149">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="c7eee-149">Click Sales order.</span></span>
5. <span data-ttu-id="c7eee-150">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c7eee-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="c7eee-151">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="c7eee-151">Example: US-001</span></span>  
6. <span data-ttu-id="c7eee-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c7eee-152">Click OK.</span></span>
7. <span data-ttu-id="c7eee-153">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c7eee-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c7eee-154">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="c7eee-154">Example: P6003</span></span>  
8. <span data-ttu-id="c7eee-155">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c7eee-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c7eee-156">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="c7eee-156">Example: 50000</span></span>  
9. <span data-ttu-id="c7eee-157">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c7eee-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="c7eee-158">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="c7eee-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="c7eee-159">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c7eee-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="c7eee-160">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c7eee-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7eee-161">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="c7eee-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="c7eee-162">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="c7eee-162">Click Run.</span></span>
4. <span data-ttu-id="c7eee-163">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="c7eee-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="c7eee-164">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="c7eee-164">Click Filter.</span></span>
6. <span data-ttu-id="c7eee-165">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="c7eee-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="c7eee-166">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c7eee-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="c7eee-167">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="c7eee-167">Example: P6003</span></span>  
8. <span data-ttu-id="c7eee-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c7eee-168">Click OK.</span></span>
9. <span data-ttu-id="c7eee-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c7eee-169">Click OK.</span></span>
10. <span data-ttu-id="c7eee-170">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="c7eee-170">Click Planned orders.</span></span>
11. <span data-ttu-id="c7eee-171">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c7eee-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c7eee-172">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="c7eee-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="c7eee-173">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c7eee-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="c7eee-174">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c7eee-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c7eee-175">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7eee-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="c7eee-176">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c7eee-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c7eee-177">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="c7eee-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="c7eee-178">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c7eee-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7eee-179">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c7eee-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="c7eee-180">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c7eee-180">Close the page.</span></span>
17. <span data-ttu-id="c7eee-181">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="c7eee-181">Click Master planning.</span></span>
18. <span data-ttu-id="c7eee-182">Wechseln Sie zu "Produktprogrammplan" > Einrichten > Produktprogrammplan-Parameter.</span><span class="sxs-lookup"><span data-stu-id="c7eee-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="c7eee-183">Wählen Sie im Feld "Alle Planungsprozessfelder deaktivieren" Nein aus.</span><span class="sxs-lookup"><span data-stu-id="c7eee-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="c7eee-184">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c7eee-184">Close the page.</span></span>

