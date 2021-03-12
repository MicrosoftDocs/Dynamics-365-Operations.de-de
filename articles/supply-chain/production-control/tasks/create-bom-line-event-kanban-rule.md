---
title: Kanban-Regel für ein Stücklistenpositionsereignis erstellen
description: Diese Aufgabe konzentriert sich auf die Einstellungen, die zum Erstellen einer Ereignis-Kanban-Regel erforderlich sind, um die Beschaffung für Produktions-Stücklistenpositionen in einer gemischten schlanken und klassischen Produktionsumgebung sicherzustellen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcef749139635b2d8858a85154ff7619c16857d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998752"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="9fe12-103">Kanban-Regel für ein Stücklistenpositionsereignis erstellen</span><span class="sxs-lookup"><span data-stu-id="9fe12-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fe12-104">Diese Aufgabe konzentriert sich auf die Einstellungen, die zum Erstellen einer Ereignis-Kanban-Regel erforderlich sind, um die Beschaffung für Produktions-Stücklistenpositionen in einer gemischten schlanken und klassischen Produktionsumgebung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="9fe12-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="9fe12-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="9fe12-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="9fe12-106">Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrommanager vorgesehen, da dieser die Produktion eines neuen oder geänderten Produkts vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="9fe12-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="9fe12-107">Neue Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="9fe12-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="9fe12-108">Wechseln Sie zu "Produktionssteuerung" > "Periodische Aufgaben" > "Kanban-Mengenberechnung" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="9fe12-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="9fe12-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9fe12-109">Click New.</span></span>
3. <span data-ttu-id="9fe12-110">Wählen Sie im Feld "Typ" die Option "Entnahme" aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="9fe12-111">Der "Entnahmetyp" wird verwendet, um Umlagerungs-Kanbans zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fe12-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="9fe12-112">Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="9fe12-113">Die "Ereignisstrategie" wird ausgewählt, um die Übertragung von Kanbans auf Grundlage eines Ereignisses zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fe12-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="9fe12-114">Später im Aufgabenleitfaden lösen wir sie aus, indem wir einen Produktionsauftrag vorkalkulieren.</span><span class="sxs-lookup"><span data-stu-id="9fe12-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="9fe12-115">Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="9fe12-116">Geben Sie "ReplenishSpeakerComponents" ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="9fe12-117">Diese Umlagerungsaktivität hat Zugangs- (Ausgangs-)Lagerort und Lagerplatz 12. Das bedeutet, dass Material zu Lagerplatz 12 in Lagerort 12 verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="9fe12-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="9fe12-118">Erweitern Sie den Abschnitt "Details".</span><span class="sxs-lookup"><span data-stu-id="9fe12-118">Expand the Details section.</span></span>
7. <span data-ttu-id="9fe12-119">Geben Sie im Feld "Produkt" den Wert "M0001" ein, oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="9fe12-120">Erweitern Sie den Abschnitt "Ereignis".</span><span class="sxs-lookup"><span data-stu-id="9fe12-120">Expand the Events section.</span></span>
9. <span data-ttu-id="9fe12-121">Wählen Sie im Feld "Stücklisten-Positionsereignis" die Option "Automatisch" aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="9fe12-122">Wenn das Feld "Stücklistenpositionsereignis" auf "Automatisch" festgelegt ist, wird Kanban erstellt, um die Materialanforderungen für Produktionsauftrags-Stücklistenpositionen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="9fe12-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="9fe12-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fe12-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="9fe12-124">Erstellen und ändern Sie einen neuen Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="9fe12-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="9fe12-125">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="9fe12-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="9fe12-126">Klicken Sie auf "Neuer Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="9fe12-126">Click New production order.</span></span>
3. <span data-ttu-id="9fe12-127">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9fe12-128">Geben Sie "L0001" ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="9fe12-129">Wir verwenden Artikel L0001, da Artikel M0001 in der Stückliste für Artikel L0001 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9fe12-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="9fe12-130">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="9fe12-130">Click Create.</span></span>
5. <span data-ttu-id="9fe12-131">Klicken Sie in der Liste auf den Link in der Zeile für "L0001".</span><span class="sxs-lookup"><span data-stu-id="9fe12-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="9fe12-132">Klicken Sie auf "Stückliste".</span><span class="sxs-lookup"><span data-stu-id="9fe12-132">Click BOM.</span></span>
7. <span data-ttu-id="9fe12-133">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9fe12-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9fe12-134">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="9fe12-134">Click Edit.</span></span>
9. <span data-ttu-id="9fe12-135">Wählen Sie im Feld "Positionstyp" die Option "Lieferung mit Bedarfsverursachung" aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="9fe12-136">"Lieferung mit Bedarfsverursachung" ist ausgewählt, um die Beschaffungserstellung eines Kanban auszulösen.</span><span class="sxs-lookup"><span data-stu-id="9fe12-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="9fe12-137">Wählen Sie "Nein" im Feld "Ressourcenverbrauch" aus.</span><span class="sxs-lookup"><span data-stu-id="9fe12-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="9fe12-138">Das Deaktivieren des Kontrollkästchens "Ressourcenverbrauch" ermöglicht es uns, den Lagerort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9fe12-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="9fe12-139">Erweitern Sie den Abschnitt "Lagerungsdimensionen".</span><span class="sxs-lookup"><span data-stu-id="9fe12-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="9fe12-140">Geben Sie im Feld Lagerort "12" ein.</span><span class="sxs-lookup"><span data-stu-id="9fe12-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="9fe12-141">Lagerort wird auf 12 festgelegt, da dies der Ausgangslagerort für die Entnahmeaktivität ist.</span><span class="sxs-lookup"><span data-stu-id="9fe12-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="9fe12-142">Geben Sie im Feld "Lagerplatz" den Wert "12" ein.</span><span class="sxs-lookup"><span data-stu-id="9fe12-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="9fe12-143">Lagerplatz wird auf 12 festgelegt, da dies der Ausgangslagerplatz der Entnahmeaktivität ist.</span><span class="sxs-lookup"><span data-stu-id="9fe12-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="9fe12-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fe12-144">Close the page.</span></span>
15. <span data-ttu-id="9fe12-145">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fe12-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="9fe12-146">Nehmen Sie eine Vorkalkulation des Produktionsauftrags vor und zeigen Sie den erstellten Kanban an</span><span class="sxs-lookup"><span data-stu-id="9fe12-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="9fe12-147">Klicken Sie auf "Vorkalkulation".</span><span class="sxs-lookup"><span data-stu-id="9fe12-147">Click Estimate.</span></span>
    * <span data-ttu-id="9fe12-148">Die Vorkalkulation des Produktionsauftrags löst die Erstellung des zugeordneten Kanbans aus, um Artikel M0001 zu liefern.</span><span class="sxs-lookup"><span data-stu-id="9fe12-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="9fe12-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9fe12-149">Click OK.</span></span>
3. <span data-ttu-id="9fe12-150">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fe12-150">Close the page.</span></span>
4. <span data-ttu-id="9fe12-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9fe12-151">Close the page.</span></span>
5. <span data-ttu-id="9fe12-152">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="9fe12-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="9fe12-153">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9fe12-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9fe12-154">Wählen Sie die Ereignis-Kanban-Regel aus, die für "M0001 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9fe12-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="9fe12-155">Erweitern Sie den Abschnitt "Kanbans".</span><span class="sxs-lookup"><span data-stu-id="9fe12-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="9fe12-156">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9fe12-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9fe12-157">Beachten Sie das Kanban, das erstellt wird, um M0001 für den vorkalkulierten Produktionsauftrag zu liefern.</span><span class="sxs-lookup"><span data-stu-id="9fe12-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="9fe12-158">Dies ist der letzte Schritt!</span><span class="sxs-lookup"><span data-stu-id="9fe12-158">This is the last step!</span></span>  

