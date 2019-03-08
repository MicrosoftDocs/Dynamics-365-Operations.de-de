---
title: Übertragungsaktivitäten für Lean Manufacturing erstellen
description: Erstellen Sie eine Umlagerungsaktivität für Lean Manufacturing.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36f79ef189924b0f3bd38cb764e73c6a0793353e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "331206"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="8b4bc-103">Übertragungsaktivitäten für Lean Manufacturing erstellen</span><span class="sxs-lookup"><span data-stu-id="8b4bc-103">Create transfer activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b4bc-104">Erstellen Sie eine Umlagerungsaktivität für Lean Manufacturing.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="8b4bc-105">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="8b4bc-105">Prerequisites:</span></span> 

1. <span data-ttu-id="8b4bc-106">Ein Produktionsfluss und eine Version, die nicht aktiv ist, müssen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="8b4bc-107">"Von und Nach-Lagerort und Lagerplatz" muss erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="8b4bc-108">Optional sollte die Wiederbeschaffung oder die auffüllende Arbeitsgruppe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="8b4bc-109">Produktionsflussversion suchen</span><span class="sxs-lookup"><span data-stu-id="8b4bc-109">Find the production flow version</span></span>
1. <span data-ttu-id="8b4bc-110">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="8b4bc-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="8b4bc-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8b4bc-112">Beachten Sie, dass der Produktionsfluss eine Version im Status "Entwurf" aufweisen muss.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="8b4bc-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="8b4bc-114">Neue Aktivität erstellen</span><span class="sxs-lookup"><span data-stu-id="8b4bc-114">Create a new activity</span></span>
1. <span data-ttu-id="8b4bc-115">Klicken Sie auf "Aktivitäten".</span><span class="sxs-lookup"><span data-stu-id="8b4bc-115">Click Activities.</span></span>
    * <span data-ttu-id="8b4bc-116">Stellen Sie sicher, dass der ausgewählte Produktionsfluss eine Version im Entwurf hat und wählen Sie diese Version aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="8b4bc-117">Klicken Sie auf "Neue Planaktivität erstellen".</span><span class="sxs-lookup"><span data-stu-id="8b4bc-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="8b4bc-118">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-118">Click Next.</span></span>
4. <span data-ttu-id="8b4bc-119">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8b4bc-120">Wählen Sie im Feld "Aktivitätstyp" "Übertragen"aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="8b4bc-121">Geben Sie im Feld "Verarbeitungsmenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="8b4bc-122">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="8b4bc-123">Arbeitsgruppen auswählen</span><span class="sxs-lookup"><span data-stu-id="8b4bc-123">Select the Work cells</span></span>
1. <span data-ttu-id="8b4bc-124">Klicken Sie im Feld "Wiederbeschaffung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8b4bc-125">Wählen Sie eine Arbeitsgruppe, um den Ausgangslagerplatz der Arbeitsgruppe und das Formular "Lagerplatz" in der Umlagerungsaktivität zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="8b4bc-126">Das Gleiche kann mit der ergänzten Arbeitsgruppe erfolgen, um den Zielort der Umlagerungsaktivität festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="8b4bc-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="8b4bc-128">Lageraktualisierungen definieren</span><span class="sxs-lookup"><span data-stu-id="8b4bc-128">Define the inventory updates</span></span>
1. <span data-ttu-id="8b4bc-129">Wählen Sie im Feld "Produkttyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="8b4bc-130">Beachten Sie, dass eine Umlagerung nicht den Typ des Produkts ändert.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="8b4bc-131">Sie können Fertigprodukte oder Halbfertigprodukte umlagern (Umlagerung zwischen zwei Aktivitäten eines Produktionsflusses und u. U. des Kanban-Flusses).</span><span class="sxs-lookup"><span data-stu-id="8b4bc-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="8b4bc-132">Wenn Sie Fertigprodukte übertragen, können Sie auswählen, ob die Entnahme oder das Empfangen zu einer Lagerbuchung führt.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="8b4bc-133">Umlagerungsorte definieren</span><span class="sxs-lookup"><span data-stu-id="8b4bc-133">Define the transfer locations</span></span>
1. <span data-ttu-id="8b4bc-134">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-134">Click Next.</span></span>
2. <span data-ttu-id="8b4bc-135">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8b4bc-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="8b4bc-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8b4bc-138">Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8b4bc-139">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8b4bc-140">Im Feld "Verfrachtet von" wählen Sie "Versender" aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="8b4bc-141">Folgende Optionen stehen zur Auswahl: Versender - die Organisation, die den Versandlagerort betreibt, Empfänger - die Organisation, die den empfangenden Lagerort betreibt, Spediteur - ein Drittanbieter.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="8b4bc-142">Wenn die Betreiber-Organisation ein Kreditor ist, benötigt die Umlagerungsaktivität eine Fremdarbeitsereinbarung.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="8b4bc-143">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="8b4bc-144">Aktivitätszeiten definieren</span><span class="sxs-lookup"><span data-stu-id="8b4bc-144">Define the activity times</span></span>
1. <span data-ttu-id="8b4bc-145">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8b4bc-146">Die Definition einer Laufzeit ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="8b4bc-147">Die Ausführungszeit wird verwendet, um Kosten und die Durchlaufzeiten der Kanban-Einzelvorgänge zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="8b4bc-148">Ausführungszeiten werden nicht verwendet, um die Kapazitätsauslastung und den Verbrauch zu berechnen. Diese werden nach der Zykluszeit berechnet, abgeleitet aus der Produktionsflussversionsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="8b4bc-149">Geben Sie im Feld "Zeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="8b4bc-150">Geben Sie im Feld "Einheiten" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="8b4bc-151">Wählen Sie die Zeiteinheit aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-151">Select the Time unit.</span></span>
5. <span data-ttu-id="8b4bc-152">Geben Sie im Feld "Nach Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="8b4bc-153">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8b4bc-154">Wartezeiten sind optional.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="8b4bc-155">Geben Sie im Feld "Zeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="8b4bc-156">Geben Sie im Feld "Einheiten" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="8b4bc-157">Wählen Sie die Zeiteinheit aus.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-157">Select the Time unit.</span></span>
10. <span data-ttu-id="8b4bc-158">Geben Sie im Feld "Nach Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="8b4bc-159">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-159">Click Next.</span></span>
12. <span data-ttu-id="8b4bc-160">Klicken Sie auf Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-160">Click Finish.</span></span>
13. <span data-ttu-id="8b4bc-161">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-161">Close the page.</span></span>

