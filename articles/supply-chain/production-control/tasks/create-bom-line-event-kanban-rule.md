--- 
title: "Kanban-Regel für ein Stücklistenpositionsereignis erstellen"
description: "Diese Aufgabe konzentriert sich auf die Einstellungen, die zum Erstellen einer Ereignis-Kanban-Regel erforderlich sind, um die Beschaffung für Produktions-Stücklistenpositionen in einer gemischten schlanken und klassischen Produktionsumgebung sicherzustellen."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1083f42395284d2fceefd4a620828d1caea89174
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="953e0-103">Kanban-Regel für ein Stücklistenpositionsereignis erstellen</span><span class="sxs-lookup"><span data-stu-id="953e0-103">Create a BOM line event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="953e0-104">Diese Aufgabe konzentriert sich auf die Einstellungen, die zum Erstellen einer Ereignis-Kanban-Regel erforderlich sind, um die Beschaffung für Produktions-Stücklistenpositionen in einer gemischten schlanken und klassischen Produktionsumgebung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="953e0-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="953e0-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="953e0-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="953e0-106">Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrommanager vorgesehen, da dieser die Produktion eines neuen oder geänderten Produkts vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="953e0-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="953e0-107">Neue Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="953e0-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="953e0-108">Wechseln Sie zu "Produktionssteuerung" > "Periodische Aufgaben" > "Kanban-Mengenberechnung" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="953e0-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="953e0-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="953e0-109">Click New.</span></span>
3. <span data-ttu-id="953e0-110">Wählen Sie im Feld "Typ" die Option "Entnahme" aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="953e0-111">Der "Entnahmetyp" wird verwendet, um Umlagerungs-Kanbans zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="953e0-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="953e0-112">Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="953e0-113">Die "Ereignisstrategie" wird ausgewählt, um die Übertragung von Kanbans auf Grundlage eines Ereignisses zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="953e0-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="953e0-114">Später im Aufgabenleitfaden lösen wir sie aus, indem wir einen Produktionsauftrag vorkalkulieren.</span><span class="sxs-lookup"><span data-stu-id="953e0-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="953e0-115">Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="953e0-116">Geben Sie "ReplenishSpeakerComponents" ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="953e0-117">Diese Umlagerungsaktivität hat Zugangs- (Ausgangs-)Lagerort und Lagerplatz 12. Das bedeutet, dass Material zu Lagerplatz 12 in Lagerort 12 verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="953e0-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="953e0-118">Erweitern Sie den Abschnitt "Details".</span><span class="sxs-lookup"><span data-stu-id="953e0-118">Expand the Details section.</span></span>
7. <span data-ttu-id="953e0-119">Geben Sie im Feld "Produkt" den Wert "M0001" ein, oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="953e0-120">Erweitern Sie den Abschnitt "Ereignis".</span><span class="sxs-lookup"><span data-stu-id="953e0-120">Expand the Events section.</span></span>
9. <span data-ttu-id="953e0-121">Wählen Sie im Feld "Stücklisten-Positionsereignis" die Option "Automatisch" aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="953e0-122">Wenn das Feld "Stücklistenpositionsereignis" auf "Automatisch" festgelegt ist, wird Kanban erstellt, um die Materialanforderungen für Produktionsauftrags-Stücklistenpositionen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="953e0-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="953e0-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="953e0-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="953e0-124">Erstellen und ändern Sie einen neuen Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="953e0-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="953e0-125">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="953e0-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="953e0-126">Klicken Sie auf "Neuer Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="953e0-126">Click New production order.</span></span>
3. <span data-ttu-id="953e0-127">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="953e0-128">Geben Sie "L0001" ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="953e0-129">Wir verwenden Artikel L0001, da Artikel M0001 in der Stückliste für Artikel L0001 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="953e0-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="953e0-130">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="953e0-130">Click Create.</span></span>
5. <span data-ttu-id="953e0-131">Klicken Sie in der Liste auf den Link in der Zeile für "L0001".</span><span class="sxs-lookup"><span data-stu-id="953e0-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="953e0-132">Klicken Sie auf "Stückliste".</span><span class="sxs-lookup"><span data-stu-id="953e0-132">Click BOM.</span></span>
7. <span data-ttu-id="953e0-133">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="953e0-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="953e0-134">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="953e0-134">Click Edit.</span></span>
9. <span data-ttu-id="953e0-135">Wählen Sie im Feld "Positionstyp" die Option "Lieferung mit Bedarfsverursachung" aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="953e0-136">"Lieferung mit Bedarfsverursachung" ist ausgewählt, um die Beschaffungserstellung eines Kanban auszulösen.</span><span class="sxs-lookup"><span data-stu-id="953e0-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="953e0-137">Wählen Sie "Nein" im Feld "Ressourcenverbrauch" aus.</span><span class="sxs-lookup"><span data-stu-id="953e0-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="953e0-138">Das Deaktivieren des Kontrollkästchens "Ressourcenverbrauch" ermöglicht es uns, den Lagerort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="953e0-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="953e0-139">Erweitern Sie den Abschnitt "Lagerungsdimensionen".</span><span class="sxs-lookup"><span data-stu-id="953e0-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="953e0-140">Geben Sie im Feld Lagerort "12" ein.</span><span class="sxs-lookup"><span data-stu-id="953e0-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="953e0-141">Lagerort wird auf 12 festgelegt, da dies der Ausgangslagerort für die Entnahmeaktivität ist.</span><span class="sxs-lookup"><span data-stu-id="953e0-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="953e0-142">Geben Sie im Feld "Lagerplatz" den Wert "12" ein.</span><span class="sxs-lookup"><span data-stu-id="953e0-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="953e0-143">Lagerplatz wird auf 12 festgelegt, da dies der Ausgangslagerplatz der Entnahmeaktivität ist.</span><span class="sxs-lookup"><span data-stu-id="953e0-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="953e0-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="953e0-144">Close the page.</span></span>
15. <span data-ttu-id="953e0-145">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="953e0-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="953e0-146">Nehmen Sie eine Vorkalkulation des Produktionsauftrags vor und zeigen Sie den erstellten Kanban an</span><span class="sxs-lookup"><span data-stu-id="953e0-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="953e0-147">Klicken Sie auf "Vorkalkulation".</span><span class="sxs-lookup"><span data-stu-id="953e0-147">Click Estimate.</span></span>
    * <span data-ttu-id="953e0-148">Die Vorkalkulation des Produktionsauftrags löst die Erstellung des zugeordneten Kanbans aus, um Artikel M0001 zu liefern.</span><span class="sxs-lookup"><span data-stu-id="953e0-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="953e0-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="953e0-149">Click OK.</span></span>
3. <span data-ttu-id="953e0-150">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="953e0-150">Close the page.</span></span>
4. <span data-ttu-id="953e0-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="953e0-151">Close the page.</span></span>
5. <span data-ttu-id="953e0-152">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="953e0-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="953e0-153">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="953e0-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="953e0-154">Wählen Sie die Ereignis-Kanban-Regel aus, die für "M0001 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="953e0-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="953e0-155">Erweitern Sie den Abschnitt "Kanbans".</span><span class="sxs-lookup"><span data-stu-id="953e0-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="953e0-156">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="953e0-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="953e0-157">Beachten Sie das Kanban, das erstellt wird, um M0001 für den vorkalkulierten Produktionsauftrag zu liefern.</span><span class="sxs-lookup"><span data-stu-id="953e0-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="953e0-158">Dies ist der letzte Schritt!</span><span class="sxs-lookup"><span data-stu-id="953e0-158">This is the last step!</span></span>  


