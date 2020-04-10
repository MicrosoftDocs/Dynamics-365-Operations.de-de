---
title: Eine Kanban-Regel mithilfe eines Mindestbestandsereignisses erstellen
description: Diese Prozedur konzentriert sich auf die Einstellungen, die benötigt werden, um eine Kanban-Regel unter Verwendung eines Mindestbestandsereignisses zu erstellen, um zu garantieren, dass ein spezifisches Produkt immer an einem spezifischen Lagerplatz verfügbar ist.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6ca5a2e2180235e51ef569fd93ad06867c3dddae
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149319"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="c1cec-103">Eine Kanban-Regel mithilfe eines Mindestbestandsereignisses erstellen</span><span class="sxs-lookup"><span data-stu-id="c1cec-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1cec-104">Diese Prozedur konzentriert sich auf die Einstellungen, die benötigt werden, um eine Kanban-Regel unter Verwendung eines Mindestbestandsereignisses zu erstellen, um zu garantieren, dass ein spezifisches Produkt immer an einem spezifischen Lagerplatz verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c1cec-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="c1cec-105">Eine Kanban-Regel wird erstellt, um Material zum Lagerplatz zu übertragen, wenn das Bestandsniveau unterhalb von 200 Stücke fällt.</span><span class="sxs-lookup"><span data-stu-id="c1cec-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="c1cec-106">Durch das Ausführen der Verarbeitung des bedarfsverursachenden Ereignisses werden die erforderlichen Kanbans erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1cec-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="c1cec-107">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="c1cec-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c1cec-108">Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrom-Manager vorgesehen, da diese die Produktion eines neuen oder geänderten Produkts in einer schlanken Umgebung vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="c1cec-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="c1cec-109">Neue Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="c1cec-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="c1cec-110">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="c1cec-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="c1cec-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c1cec-111">Click New.</span></span>
3. <span data-ttu-id="c1cec-112">Wählen Sie im Feld "Typ" die Option "Entnahme" aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="c1cec-113">Dieser Typ wird verwendet, um Kanban-Umlagerungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1cec-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="c1cec-114">Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="c1cec-115">Die "Ereignisstrategie" wird verwendet, um die Kanban-Umlagerungen auf Grundlage eines Ereignisses zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1cec-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="c1cec-116">Später in dieser Prozedur lösen Sie Kanban-Umlagerungen mithilfe der Bestandswiederbeschaffung aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="c1cec-117">Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c1cec-118">Geben Sie "ReplenishSpeakerComponents" ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="c1cec-119">Diese Umlagerungsaktivität hat Zugangs- (Ausgangs-)Lagerort und Lagerplatz 12. Das bedeutet, dass Materialien zu Lagerplatz 12 in Lagerort 12 verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="c1cec-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="c1cec-120">Erweitern Sie den Abschnitt "Details".</span><span class="sxs-lookup"><span data-stu-id="c1cec-120">Expand the Details section.</span></span>
7. <span data-ttu-id="c1cec-121">Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="c1cec-122">Wählen Sie M0007 aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-122">Select M0007.</span></span>  
8. <span data-ttu-id="c1cec-123">Erweitern Sie den Abschnitt "Ereignis".</span><span class="sxs-lookup"><span data-stu-id="c1cec-123">Expand the Events section.</span></span>
9. <span data-ttu-id="c1cec-124">Wählen Sie im Feld "Bestandswiederbeschaffungsereignis" die Option "Charge" aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="c1cec-125">Dies erstellt Kanbans, um Materialbedarf am verknüpften Lagerplatz während der "Verarbeitung von bedarfsverursachenden Ereignissen" zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c1cec-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="c1cec-126">Die Mindestmenge für den Artikel festlegen</span><span class="sxs-lookup"><span data-stu-id="c1cec-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="c1cec-127">Klicken Sie, um dem Link im Feld "Produkt" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="c1cec-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="c1cec-128">Klicken Sie, um dem Link im Feld "Artikelnummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="c1cec-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="c1cec-129">Erweitern Sie die Infobox "Produktbild".</span><span class="sxs-lookup"><span data-stu-id="c1cec-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="c1cec-130">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="c1cec-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="c1cec-131">Klicken Sie auf "Artikeldeckung".</span><span class="sxs-lookup"><span data-stu-id="c1cec-131">Click Item coverage.</span></span>
6. <span data-ttu-id="c1cec-132">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c1cec-132">Click New.</span></span>
7. <span data-ttu-id="c1cec-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c1cec-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c1cec-134">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c1cec-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="c1cec-135">Legen Sie den "Lagerort" auf 12 fest.</span><span class="sxs-lookup"><span data-stu-id="c1cec-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="c1cec-136">Legen Sie das Minimum auf "200" fest.</span><span class="sxs-lookup"><span data-stu-id="c1cec-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="c1cec-137">Stapelereignis-Erstellungseinzelvorgang ausführen</span><span class="sxs-lookup"><span data-stu-id="c1cec-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="c1cec-138">Wechseln Sie zu "Produktionssteuerung" > "Periodisches Aufgaben" > "Kanban-Einzelvorgangs-Stapelverarbeitung" > "Verarbeitung des bedarfsverursachenden Ereignisses".</span><span class="sxs-lookup"><span data-stu-id="c1cec-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="c1cec-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c1cec-139">Click OK.</span></span>
3. <span data-ttu-id="c1cec-140">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="c1cec-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="c1cec-141">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c1cec-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c1cec-142">Wählen Sie die Kanban-Regel aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c1cec-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="c1cec-143">Erweitern Sie den Abschnitt "Kanbans".</span><span class="sxs-lookup"><span data-stu-id="c1cec-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="c1cec-144">Beachten Sie, dass ein Kanban erstellt wurde, um das erforderliche Material an Lagerort 12 zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="c1cec-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

