---
title: Verarbeitungsaktivitäten für Lean Manufacturing erstellen
description: Erstellen Sie eine Prozessaktivität für Lean Manufacturing.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46d6b7696d606333a170eaa1c06b9e0503ae1e02
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829017"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="a06de-103">Verarbeitungsaktivitäten für Lean Manufacturing erstellen</span><span class="sxs-lookup"><span data-stu-id="a06de-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a06de-104">Erstellen Sie eine Prozessaktivität für Lean Manufacturing.</span><span class="sxs-lookup"><span data-stu-id="a06de-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="a06de-105">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="a06de-105">Prerequisites:</span></span> 

1. <span data-ttu-id="a06de-106">Ein Produktionsfluss und eine Version, die nicht aktiv ist, müssen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a06de-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="a06de-107">Eine Arbeitsgruppe muss erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a06de-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="a06de-108">Produktionsflussversion suchen</span><span class="sxs-lookup"><span data-stu-id="a06de-108">Find the production flow version</span></span>
1. <span data-ttu-id="a06de-109">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="a06de-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="a06de-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a06de-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a06de-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a06de-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="a06de-112">Neue Aktivität erstellen</span><span class="sxs-lookup"><span data-stu-id="a06de-112">Create a new activity</span></span>
1. <span data-ttu-id="a06de-113">Klicken Sie auf "Aktivitäten".</span><span class="sxs-lookup"><span data-stu-id="a06de-113">Click Activities.</span></span>
    * <span data-ttu-id="a06de-114">Stellen Sie sicher, dass der ausgewählte Produktionsfluss eine Version im Entwurf hat und wählen Sie diese Version aus.</span><span class="sxs-lookup"><span data-stu-id="a06de-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="a06de-115">Klicken Sie auf "Neue Planaktivität erstellen".</span><span class="sxs-lookup"><span data-stu-id="a06de-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="a06de-116">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="a06de-116">Click Next.</span></span>
4. <span data-ttu-id="a06de-117">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a06de-118">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a06de-119">Beachten Sie, dass der Name für einen angegebenen Produktionsfluss für alle Versionen eindeutig sein muss.</span><span class="sxs-lookup"><span data-stu-id="a06de-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="a06de-120">Geben Sie im Feld "Verarbeitungsmenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="a06de-121">Beachten Sie, dass, egal welche Einzelvorgangsmenge verarbeitet wird, dies die Mindestmenge pro Einzelvorgang ist, um die Lohnkosten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a06de-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="a06de-122">Wenn Einzelvorgangsmengen von dieser Menge abweichen, wird eine Lohnkostenabweichung erstellt.</span><span class="sxs-lookup"><span data-stu-id="a06de-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="a06de-123">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="a06de-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="a06de-124">Arbeitsgruppe auswählen.</span><span class="sxs-lookup"><span data-stu-id="a06de-124">Select the work cell</span></span>
1. <span data-ttu-id="a06de-125">Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a06de-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="a06de-126">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a06de-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="a06de-127">Lageraktualisierungen definieren</span><span class="sxs-lookup"><span data-stu-id="a06de-127">Define the inventory updates</span></span>
1. <span data-ttu-id="a06de-128">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Zugang zum verfügbaren Lagerbestand aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="a06de-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="a06de-129">Wenn "Aktualisierung am Lager = kein" ist, können Sie die Aktivität definieren, um ein Halbfertigprodukt anzunehmen (diese Aktivität erreicht nicht die nächste Stücklistenebene).</span><span class="sxs-lookup"><span data-stu-id="a06de-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="a06de-130">Sie können auch auswählen, ob Sie Halbfertigprodukte verbrauchen wollen.</span><span class="sxs-lookup"><span data-stu-id="a06de-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="a06de-131">Entnahmeaktivitäten definieren</span><span class="sxs-lookup"><span data-stu-id="a06de-131">Define the picking activities</span></span>
1. <span data-ttu-id="a06de-132">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="a06de-132">Click Next.</span></span>
2. <span data-ttu-id="a06de-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a06de-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a06de-134">Eine standardmäßige Entnahmeaktivität wird für den Wareneingang der ausgewählten Arbeitsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="a06de-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="a06de-135">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a06de-135">Click Add.</span></span>
    * <span data-ttu-id="a06de-136">Sie können zusätzliche Kommissionieraktivitäten für bestimmte Produkte, die nicht in der Arbeitsgruppeneingabeaktivität bereitgestellt werden, erstellen.</span><span class="sxs-lookup"><span data-stu-id="a06de-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="a06de-137">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a06de-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a06de-138">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="a06de-139">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a06de-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a06de-140">Mit dieser Definition werden alle Materialien, die in der Aktivität verbraucht werden, dem standardmäßigen Eingangslagerort und Lagerplatz entnommen, mit Ausnahme des Artikels, der nicht in der zweiten Entnahmeaktivität definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a06de-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="a06de-141">Dieser Artikel wird aus einem anderen Lagerort und Lagerplatz entnommen.</span><span class="sxs-lookup"><span data-stu-id="a06de-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="a06de-142">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a06de-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a06de-143">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a06de-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a06de-144">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Ausschuss erfassen".</span><span class="sxs-lookup"><span data-stu-id="a06de-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="a06de-145">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="a06de-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="a06de-146">Aktivitätszeiten definieren</span><span class="sxs-lookup"><span data-stu-id="a06de-146">Define the activity times</span></span>
1. <span data-ttu-id="a06de-147">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a06de-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a06de-148">Die Definition einer Laufzeit ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a06de-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="a06de-149">Die Laufzeit wird verwendet, um Kosten und die Durchsatzzeiten der Kanban-Einzelvorgänge zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a06de-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="a06de-150">Ausführungszeiten werden nicht verwendet, um die Kapazitätsauslastung und Verbrauch zu berechnen. Diese werden nach der Zykluszeit berechnet, abgeleitet aus der Produktionsflussversionsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="a06de-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="a06de-151">Geben Sie im Feld "Zeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="a06de-152">Geben Sie im Feld "Einheiten" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="a06de-153">Wählen Sie die Zeiteinheit aus.</span><span class="sxs-lookup"><span data-stu-id="a06de-153">Select the Time unit.</span></span>
5. <span data-ttu-id="a06de-154">Geben Sie im Feld "Nach Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="a06de-155">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a06de-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a06de-156">Wartezeiten sind optional.</span><span class="sxs-lookup"><span data-stu-id="a06de-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="a06de-157">Geben Sie im Feld "Zeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="a06de-158">Geben Sie im Feld "Einheiten" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="a06de-159">Wählen Sie die Zeiteinheit aus.</span><span class="sxs-lookup"><span data-stu-id="a06de-159">Select the Time unit.</span></span>
10. <span data-ttu-id="a06de-160">Geben Sie im Feld "Nach Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="a06de-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="a06de-161">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="a06de-161">Click Next.</span></span>
12. <span data-ttu-id="a06de-162">Klicken Sie auf Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="a06de-162">Click Finish.</span></span>
13. <span data-ttu-id="a06de-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a06de-163">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]