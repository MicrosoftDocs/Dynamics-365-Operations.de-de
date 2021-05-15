---
title: Erstellen Sie einen Materialplan für Co-Produkte
description: Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920728"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="88873-103">Erstellen Sie einen Materialplan für Co-Produkte</span><span class="sxs-lookup"><span data-stu-id="88873-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88873-104">Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.</span><span class="sxs-lookup"><span data-stu-id="88873-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="88873-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="88873-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="88873-106">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="88873-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="88873-107">Gehen Sie zu **Vertrieb und Marketing \> Arbeitsbereiche \> Verkaufsauftragsverarbeitung und Abfrage**.</span><span class="sxs-lookup"><span data-stu-id="88873-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="88873-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-108">Select **New**.</span></span>
1. <span data-ttu-id="88873-109">**Auftrag** auswählen.</span><span class="sxs-lookup"><span data-stu-id="88873-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="88873-110">Geben Sie im Feld **Kundenkonto** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="88873-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="88873-111">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="88873-111">Example: US-001</span></span>  
1. <span data-ttu-id="88873-112">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="88873-112">Select **OK**.</span></span>
1. <span data-ttu-id="88873-113">Geben Sie im Feld **Artikelnummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="88873-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="88873-114">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="88873-114">Example: P6003</span></span>  
1. <span data-ttu-id="88873-115">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="88873-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="88873-116">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="88873-116">Example: 50000</span></span>  
1. <span data-ttu-id="88873-117">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="88873-118">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="88873-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="88873-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="88873-119">Close the page.</span></span>
1. <span data-ttu-id="88873-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="88873-120">Close the page.</span></span>
1. <span data-ttu-id="88873-121">Wählen Sie **Produktprogrammplanung**.</span><span class="sxs-lookup"><span data-stu-id="88873-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="88873-122">Wählen Sie im Feld **Plan** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="88873-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="88873-123">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="88873-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="88873-124">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="88873-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="88873-125">Wählen Sie **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-125">Select **Run**.</span></span>
1. <span data-ttu-id="88873-126">Erweitern oder klappen Sie den Abschnitt **Datensätze zum Einschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="88873-127">Wählen Sie **Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-127">Select **Filter**.</span></span>
1. <span data-ttu-id="88873-128">Wählen Sie in der Liste die Zeile für **Feld** = *Elementnummer*.</span><span class="sxs-lookup"><span data-stu-id="88873-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="88873-129">Geben Sie im Feld **Kriterien** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="88873-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="88873-130">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="88873-130">Example: P6003</span></span>  
1. <span data-ttu-id="88873-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="88873-131">Select **OK**.</span></span>
1. <span data-ttu-id="88873-132">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="88873-132">Select **OK**.</span></span>
1. <span data-ttu-id="88873-133">Wählen Sie **Bestellvorschläge** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="88873-134">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="88873-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="88873-135">Beispiel: Filtern Sie auf das Feld **Elementnummer** mit einem Wert von 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="88873-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="88873-136">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="88873-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="88873-137">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="88873-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="88873-138">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="88873-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="88873-139">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="88873-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="88873-140">Erweitern Sie den Abschnitt **Bedarfverursacher**.</span><span class="sxs-lookup"><span data-stu-id="88873-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="88873-141">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="88873-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="88873-142">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="88873-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="88873-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="88873-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="88873-144">Erstellen Sie eine zweite Anforderung für ein Kuppelprodukt</span><span class="sxs-lookup"><span data-stu-id="88873-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="88873-145">Gehen Sie zu **Vertrieb und Marketing \> Arbeitsbereiche \> Verkaufsauftragsverarbeitung und Abfrage**.</span><span class="sxs-lookup"><span data-stu-id="88873-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="88873-146">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-146">Select **New**.</span></span>
1. <span data-ttu-id="88873-147">**Auftrag** auswählen.</span><span class="sxs-lookup"><span data-stu-id="88873-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="88873-148">Geben Sie im Feld **Kundenkonto** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="88873-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="88873-149">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="88873-149">Example: US-001</span></span>  
1. <span data-ttu-id="88873-150">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="88873-150">Select **OK**.</span></span>
1. <span data-ttu-id="88873-151">Geben Sie im Feld **Artikelnummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="88873-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="88873-152">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="88873-152">Example: P6003</span></span>  
1. <span data-ttu-id="88873-153">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="88873-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="88873-154">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="88873-154">Example: 50000</span></span>  
1. <span data-ttu-id="88873-155">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="88873-156">Erstellen Sie einen zweiten Materialplan für Kuppelprodukte</span><span class="sxs-lookup"><span data-stu-id="88873-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="88873-157">Wählen Sie im Feld **Plan** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="88873-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="88873-158">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="88873-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="88873-159">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="88873-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="88873-160">Wählen Sie **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-160">Select **Run**.</span></span>
4. <span data-ttu-id="88873-161">Erweitern oder klappen Sie den Abschnitt **Datensätze zum Einschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="88873-162">Wählen Sie **Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-162">Select **Filter**.</span></span>
6. <span data-ttu-id="88873-163">Wählen Sie in der Liste die Zeile für **Feld** = *Elementnummer*.</span><span class="sxs-lookup"><span data-stu-id="88873-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="88873-164">Geben Sie im Feld *Kriterien* einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="88873-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="88873-165">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="88873-165">Example: P6003</span></span>  
8. <span data-ttu-id="88873-166">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="88873-166">Select **OK**.</span></span>
9. <span data-ttu-id="88873-167">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="88873-167">Select **OK**.</span></span>
10. <span data-ttu-id="88873-168">Wählen Sie **Bestellvorschläge** aus.</span><span class="sxs-lookup"><span data-stu-id="88873-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="88873-169">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="88873-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="88873-170">Beispiel: Filtern Sie auf das Feld **Elementnummer** mit einem Wert von 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="88873-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="88873-171">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="88873-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="88873-172">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="88873-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="88873-173">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="88873-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="88873-174">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="88873-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="88873-175">Erweitern oder reduzieren Sie den Abschnitt **Bedarfsverursacher**.</span><span class="sxs-lookup"><span data-stu-id="88873-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="88873-176">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="88873-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="88873-177">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="88873-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="88873-178">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="88873-178">Close the page.</span></span>
17. <span data-ttu-id="88873-179">Wählen Sie **Produktprogrammplanung**.</span><span class="sxs-lookup"><span data-stu-id="88873-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="88873-180">Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Produktprogrammplanparameter**.</span><span class="sxs-lookup"><span data-stu-id="88873-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="88873-181">Wählen Sie *Nein* im Feld **Alle Planungsprozesse deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="88873-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="88873-182">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="88873-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]