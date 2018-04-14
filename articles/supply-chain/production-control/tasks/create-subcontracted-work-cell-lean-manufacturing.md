--- 
title: "Eine Fremdarbeitszelle für Lean Manufacturing erstellen"
description: "Um Arbeit für Lean Manufacturing zu modellieren, müssen Sie eine Fertigungszelle erstellen, die dem Kreditor zugeordnet ist, der die Arbeit bereitstellt."
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d5b7149551df33d439980ec4e04fa343749daa16
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="85d9b-103">Eine Fremdarbeitszelle für Lean Manufacturing erstellen</span><span class="sxs-lookup"><span data-stu-id="85d9b-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85d9b-104">Um Arbeit für Lean Manufacturing zu modellieren, müssen Sie eine Fertigungszelle erstellen, die dem Kreditor zugeordnet ist, der die Arbeit bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="85d9b-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="85d9b-105">Eine Fertigungszelle wird an den Kreditor über die Zuordnung eine Ressource vom Kreditorentyps verknüpft.</span><span class="sxs-lookup"><span data-stu-id="85d9b-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="85d9b-106">Wenn Sie dieser Buchung im USMF-Vorführungsunternehmen wiedergeben, können Sie Kreditorenkontokennung 1002 und 1. Standort auswählen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="85d9b-107">Erstellen einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="85d9b-107">Create a vendor resource</span></span>
1. <span data-ttu-id="85d9b-108">Wechseln Sie zu "Ressourcen".</span><span class="sxs-lookup"><span data-stu-id="85d9b-108">Go to Resources.</span></span>
2. <span data-ttu-id="85d9b-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="85d9b-109">Click New.</span></span>
3. <span data-ttu-id="85d9b-110">Geben Sie im Feld "Ressource" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="85d9b-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="85d9b-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="85d9b-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="85d9b-112">Wählen Sie im Feld Kreditor den Typ aus.</span><span class="sxs-lookup"><span data-stu-id="85d9b-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="85d9b-113">Klicken Sie im Feld "Händler" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="85d9b-114">Ressourcengruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="85d9b-114">Create the resource group</span></span>
1. <span data-ttu-id="85d9b-115">Wechseln Sie zu "Ressourcengruppen".</span><span class="sxs-lookup"><span data-stu-id="85d9b-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="85d9b-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="85d9b-116">Click New.</span></span>
3. <span data-ttu-id="85d9b-117">Geben Sie im Feld "Ressourcengruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="85d9b-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="85d9b-118">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="85d9b-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="85d9b-119">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="85d9b-120">Wählen Sie den Standort aus, dem die Fertigungszelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85d9b-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="85d9b-121">In der Theorie kann ein Standort einen einzelnen Standort darstellen, der von einem Kreditor bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="85d9b-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="85d9b-122">Allerdings werden in den meisten Fällen Ressourcen aktuell dem Standort zugeordnet, der die Aufträge in  Fremdarbeit ausführt.</span><span class="sxs-lookup"><span data-stu-id="85d9b-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="85d9b-123">Beachten Sie, dass die von Eingangs- und Ausgangslagerorte geregelten Fertigungszellen demselben Standort entsprechen müssen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="85d9b-124">Geben Sie im Feld "Standort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="85d9b-124">In the Site field, type a value.</span></span>
7. @SysTaskRecorder:_RequestClose
8. <span data-ttu-id="85d9b-125">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen Arbeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="85d9b-125">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="85d9b-126">Klicken Sie im Feld "Eingangslagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-126">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="85d9b-127">Wählen Sie den Lagerort und Lagerplatz aus, die das Material für die Kreditor-verwaltete Arbeitsgruppe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85d9b-127">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="85d9b-128">In vielen Fällen werden der Lagerort und der Lagerplatz modelliert, indem Sie einen separaten Lagerort pro Lieferant und pro Fertigungszelle für einen Lagerplatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="85d9b-128">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="85d9b-129">Klicken Sie im Feld "Lagerplatz für Wareneingang" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="85d9b-130">Klicken Sie im Feld "Ausgangslagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-130">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="85d9b-131">Definieren Sie den Lagerort und Lagerplatz, an dem das Material gebucht wird, wenn die von gesetzlichen Bestimmungen unterliegenden Aktivitäten der Fertigungszelle gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="85d9b-131">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="85d9b-132">Der Lagerort und der Ort können am Kreditorenstandort sein, wenn der Kreditor an die Kanban-Einzelvorgänge berichtet.</span><span class="sxs-lookup"><span data-stu-id="85d9b-132">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="85d9b-133">Alternativ kann der Lagerort und der Lagerplatz der empfangende Speicherort sein, der mit dem nächsten Schritt des Produktionsflusses verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="85d9b-133">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="85d9b-134">Klicken Sie im Feld "Lagerplatz für Warenausgang" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-134">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="85d9b-135">Erweitern oder reduzieren Sie den Abschnitt "Kalender".</span><span class="sxs-lookup"><span data-stu-id="85d9b-135">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="85d9b-136">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-136">Click Add.</span></span>
15. <span data-ttu-id="85d9b-137">Klicken Sie im Feld "Kalender" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-137">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="85d9b-138">Wählen Sie den Kalender aus, der die Arbeitszeit der angegebenen Arbeitsgruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="85d9b-138">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="85d9b-139">Für wichtige Ressourcen empfehlen wir jedoch, die bestimmten Kalender zu definieren, die die Ausführung für die  Arbeitszeiten und die zugehörigen Fertigungszelle- oder Kapazitäten des Kreditorenstandorts darstellen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-139">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="85d9b-140">Erweitern oder reduzieren Sie den Abschnitt Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-140">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="85d9b-141">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-141">Click Add.</span></span>
    * <span data-ttu-id="85d9b-142">Eine Ressourcengruppe muss eine zugehörige Ressource des Kreditorentyps haben, der die Ressourcengruppe auf dem Kreditorenkonto zugeordnet hat.</span><span class="sxs-lookup"><span data-stu-id="85d9b-142">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="85d9b-143">Klicken Sie im Feld Ressourcen auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-143">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="85d9b-144">Wählen Sie die Kreditorenressource aus, die Sie in der vorherigen Unteraufgabe erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="85d9b-144">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="85d9b-145">Erweitern oder reduzieren Sie den Abschnitt "Arbeisgruppenkapazität".</span><span class="sxs-lookup"><span data-stu-id="85d9b-145">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="85d9b-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-146">Click Add.</span></span>
    * <span data-ttu-id="85d9b-147">Eine Fertigungszelle muss eine festgelegte Kapazität verfügen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-147">A work cell must have a defined capacity.</span></span> <span data-ttu-id="85d9b-148">In diesem Beispiel erstellen wir eine Durchsatzkapazität von 100 Stück pro Standardarbeitstag.</span><span class="sxs-lookup"><span data-stu-id="85d9b-148">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="85d9b-149">Klicken Sie im Feld "Produktionsflussmodell" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-149">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="85d9b-150">Wählen Sie im Feld "Kapazitätsperiode" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="85d9b-150">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="85d9b-151">Geben Sie im Feld "Durchschnittliche Durchsatzmenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="85d9b-151">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="85d9b-152">Klicken Sie im Feld "Einheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85d9b-152">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="85d9b-153">"Auflösen" verändert die Einheit.</span><span class="sxs-lookup"><span data-stu-id="85d9b-153">ResolveChanges the Unit.</span></span>


