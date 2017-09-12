--- 
title: "Materialplan für Co-Produkte erstellen"
description: "Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0b413-103">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="0b413-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b413-104">Der Produktionsplaner plant den Materialbedarf für Artikel, die Co-Produkte der Formel sind.</span><span class="sxs-lookup"><span data-stu-id="0b413-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="0b413-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="0b413-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="0b413-106">Anforderung für ein Co-Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="0b413-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="0b413-107">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="0b413-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="0b413-108">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="0b413-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="0b413-109">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="0b413-109">Click New.</span></span>
4. <span data-ttu-id="0b413-110">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="0b413-110">Click Sales order.</span></span>
5. <span data-ttu-id="0b413-111">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0b413-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="0b413-112">Beispiel: US-001</span><span class="sxs-lookup"><span data-stu-id="0b413-112">Example: US-001</span></span>  
6. <span data-ttu-id="0b413-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0b413-113">Click OK.</span></span>
7. <span data-ttu-id="0b413-114">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0b413-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="0b413-115">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="0b413-115">Example: P6003</span></span>  
8. <span data-ttu-id="0b413-116">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0b413-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="0b413-117">Beispiel: 50000</span><span class="sxs-lookup"><span data-stu-id="0b413-117">Example: 50000</span></span>  
9. <span data-ttu-id="0b413-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b413-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0b413-119">Materialplan für Co-Produkte erstellen</span><span class="sxs-lookup"><span data-stu-id="0b413-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="0b413-120">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="0b413-120">Click Master planning.</span></span>
2. <span data-ttu-id="0b413-121">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0b413-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0b413-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b413-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0b413-123">Beispiel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="0b413-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="0b413-124">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="0b413-124">Click Run.</span></span>
5. <span data-ttu-id="0b413-125">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="0b413-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="0b413-126">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="0b413-126">Click Filter.</span></span>
7. <span data-ttu-id="0b413-127">In der Liste wählen Sie die Zeile für Feld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="0b413-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="0b413-128">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0b413-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0b413-129">Beispiel: P6003</span><span class="sxs-lookup"><span data-stu-id="0b413-129">Example: P6003</span></span>  
9. <span data-ttu-id="0b413-130">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0b413-130">Click OK.</span></span>
10. <span data-ttu-id="0b413-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0b413-131">Click OK.</span></span>
11. <span data-ttu-id="0b413-132">Klicken Sie auf "Bestellvorschläge".</span><span class="sxs-lookup"><span data-stu-id="0b413-132">Click Planned orders.</span></span>
12. <span data-ttu-id="0b413-133">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="0b413-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0b413-134">Filtern Sie beispielsweise im Feld "Artikelnummer" mit dem Wert "P6000".</span><span class="sxs-lookup"><span data-stu-id="0b413-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="0b413-135">Filtern nach Formelartikel, der ein Co-Produkt des Artikels hat, für das Sie einen Auftrag erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="0b413-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="0b413-136">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b413-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0b413-137">Aktivieren Sie beliebige der Zeilen aus, die durch den Filter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b413-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="0b413-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b413-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="0b413-139">Erweitern oder reduzieren Sie den Abschnitt "Bedarfsverursacher".</span><span class="sxs-lookup"><span data-stu-id="0b413-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="0b413-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b413-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0b413-141">Der Auftragsvorschlag wird zum Auftrag für das Co-Produkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0b413-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="0b413-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0b413-142">Close the page.</span></span>


