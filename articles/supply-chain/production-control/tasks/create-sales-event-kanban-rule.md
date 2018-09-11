--- 
title: "Kanban-Regel für ein Verkaufsereignis erstellen"
description: "Ziel dieser Prozedur ist es, die notwendigen Einstellungen vorzunehmen, um eine Kanban-Regel zu erstellen, die während der Auftragserstellung ausgelöst wird."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: e727f240b7aebe501f073cf8c4e311530e7605e1
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="95b34-103">Kanban-Regel für ein Verkaufsereignis erstellen</span><span class="sxs-lookup"><span data-stu-id="95b34-103">Create a sales event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95b34-104">Ziel dieser Prozedur ist es, die notwendigen Einstellungen vorzunehmen, um eine Kanban-Regel zu erstellen, die während der Auftragserstellung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="95b34-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="95b34-105">Die Ereignis-Kanban-Regel füllt Anforderungen auf, die von Auftragspositionen stammen.</span><span class="sxs-lookup"><span data-stu-id="95b34-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="95b34-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="95b34-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="95b34-107">Dies ist für den Verfahrenstechniker oder den Wertstrom-Manager vorgesehen, da dieser die Produktion eines neuen oder geänderten Produkts vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="95b34-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="95b34-108">Neue Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="95b34-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="95b34-109">Wechseln Sie zu Kanban-Regeln.</span><span class="sxs-lookup"><span data-stu-id="95b34-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="95b34-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="95b34-110">Click New.</span></span>
3. <span data-ttu-id="95b34-111">Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="95b34-112">Die Auswahl "Ereignis" bedeutet, dass die Kanban-Regel durch ein Ereignis, beispielsweise die Erstellung einer Auftragsposition, ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="95b34-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="95b34-113">Diese Informationen werden in den Bereichen verwendet, bei denen jeder Kanban einen bestimmten Bedarf beinhalten soll.</span><span class="sxs-lookup"><span data-stu-id="95b34-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="95b34-114">Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="95b34-115">Wählen Sie "Endmontage" aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="95b34-116">Erweitern Sie den Abschnitt "Details".</span><span class="sxs-lookup"><span data-stu-id="95b34-116">Expand the Details section.</span></span>
6. <span data-ttu-id="95b34-117">Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="95b34-118">Wählen Sie L0050 aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="95b34-119">Ereignis definieren</span><span class="sxs-lookup"><span data-stu-id="95b34-119">Define an event</span></span>
1. <span data-ttu-id="95b34-120">Erweitern Sie den Abschnitt "Ereignis".</span><span class="sxs-lookup"><span data-stu-id="95b34-120">Expand the Events section.</span></span>
2. <span data-ttu-id="95b34-121">Wählen Sie im Feld "Verkaufsereignis" "Automatisch".</span><span class="sxs-lookup"><span data-stu-id="95b34-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="95b34-122">Wenn Sie die Verkaufsereignis "Automatisch" auswählt haben, wird diese Kanban-Regel automatisch ausgelöst, wenn eine Verkaufsposition mit dem Produkt- und Zugangslagerplatz übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="95b34-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="95b34-123">In diesem Verfahren ist es Produkt L0050 auf Lagerort 13.</span><span class="sxs-lookup"><span data-stu-id="95b34-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="95b34-124">Legen Sie die "Mindestmenge für Ereignis" auf '50' fest.</span><span class="sxs-lookup"><span data-stu-id="95b34-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="95b34-125">Mit einer Mindestereignismenge von 50 wird die Kanban-Regel nur von Ereignissen mit einer Menge von 50 oder mehr ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="95b34-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="95b34-126">Erweitern Sie den Abschnitt "Produktionsfluss".</span><span class="sxs-lookup"><span data-stu-id="95b34-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="95b34-127">Beachten Sie, dass der Zugangslagerplatz Lagerort 13 ist.</span><span class="sxs-lookup"><span data-stu-id="95b34-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="95b34-128">Das bedeutet, dass diese Kanban-Regel für diesen Lagerplatz ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="95b34-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="95b34-129">In diesem Beispiel löst eine Verkaufsposition für Produkt L0050, mit einer Menge von 50 oder mehr, auf Lagerort 13, diese Kanban-Regel aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="95b34-130">Erstellen Sie eine Verkaufsposition, um die Ereignis-Kanban-Regel auszulösen.</span><span class="sxs-lookup"><span data-stu-id="95b34-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="95b34-131">Wechseln Sie zu "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="95b34-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="95b34-132">Eine Warnung wird angezeigt, wenn die Kanban-Regel gespeichert wird, was bedeutet, dass Kanbans in Echtzeit während der Auftragserstellung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="95b34-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="95b34-133">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="95b34-133">Click New.</span></span>
3. <span data-ttu-id="95b34-134">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="95b34-135">Wählen Sie z.B. "US-003" aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="95b34-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="95b34-136">Click OK.</span></span>
5. <span data-ttu-id="95b34-137">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "L0050" ein.</span><span class="sxs-lookup"><span data-stu-id="95b34-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="95b34-138">Geben Sie im Feld 'Standort' den Wert '1' ein.</span><span class="sxs-lookup"><span data-stu-id="95b34-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="95b34-139">Wählen Sie Standort 1 aus, da Lagerort 13 auf Standort 1. ist.</span><span class="sxs-lookup"><span data-stu-id="95b34-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="95b34-140">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="95b34-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="95b34-141">Legen Sie den "Lagerort" auf 13 fest.</span><span class="sxs-lookup"><span data-stu-id="95b34-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="95b34-142">Legen Sie die Menge auf "75" fest.</span><span class="sxs-lookup"><span data-stu-id="95b34-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="95b34-143">Geben Sie eine Menge von 50 oder höher ein, um die erstellte Kanban-Regel auszulösen.</span><span class="sxs-lookup"><span data-stu-id="95b34-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="95b34-144">Überprüfen Sie, ob ein Kanban erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95b34-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="95b34-145">Klicken Sie auf "Produkt und Beschaffung".</span><span class="sxs-lookup"><span data-stu-id="95b34-145">Click Product and supply.</span></span>
2. <span data-ttu-id="95b34-146">Klicken Sie auf "Bedarfsverursacherstruktur anzeigen".</span><span class="sxs-lookup"><span data-stu-id="95b34-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="95b34-147">Beachten Sie, dass ein Kanban mit derselben Menge wie die Auftragsposition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95b34-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="95b34-148">Sie können außerdem die Materialabgänge sehen, die erforderlich sind, um L0050 zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="95b34-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="95b34-149">Dies ist der letzte Schritt in diesem Verfahren.</span><span class="sxs-lookup"><span data-stu-id="95b34-149">This is the last step in this procedure.</span></span>  


