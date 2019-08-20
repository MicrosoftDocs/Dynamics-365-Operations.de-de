---
title: Neue Entnahme-Kanban-Regel erstellen
description: Diese Prozedur zeigt die Einstellungen, die benötigt werden, um eine Kanban-Entnahmeregel für das Übertragen von Material in einer schlanken Umgebung zu erstellen.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d8647a88773b3d4c0193d64307426736d0d085d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837757"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="0e407-103">Neue Entnahme-Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="0e407-103">Create a withdrawal kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e407-104">Diese Prozedur zeigt die Einstellungen, die benötigt werden, um eine Kanban-Entnahmeregel für das Übertragen von Material in einer schlanken Umgebung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e407-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="0e407-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="0e407-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0e407-106">Diese Prozedur ist für den Fertigungsplaner oder den Wertstrommanager vorgesehen, da dieser die Auffüllung eines neuen oder geänderten Materials vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="0e407-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="0e407-107">Neue Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="0e407-107">Create new kanban rule</span></span>
1. <span data-ttu-id="0e407-108">Wechseln Sie zu Kanban-Regeln.</span><span class="sxs-lookup"><span data-stu-id="0e407-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="0e407-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0e407-109">Click New.</span></span>
3. <span data-ttu-id="0e407-110">Wählen Sie im Feld "Typ" die Option "Entnahme" aus.</span><span class="sxs-lookup"><span data-stu-id="0e407-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="0e407-111">Der "Entnahmetyp" wird verwendet, sodass Kanban-Regeln Material oder Waren übertragen können.</span><span class="sxs-lookup"><span data-stu-id="0e407-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="0e407-112">Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0e407-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="0e407-113">Wählen Sie "ReplenishSpeakerComponents" aus.</span><span class="sxs-lookup"><span data-stu-id="0e407-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="0e407-114">Diese Aktivität wird so eingerichtet, dass Komponenten aus Lagerort 11, Lagerplatz 11, nach Lagerort 12 und Lagerplatz 12 verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="0e407-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="0e407-115">Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0e407-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="0e407-116">Wählen Sie M0007 aus.</span><span class="sxs-lookup"><span data-stu-id="0e407-116">Select M0007.</span></span>  
6. <span data-ttu-id="0e407-117">Geben Sie im Feld "Lieferzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0e407-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="0e407-118">Beispiel: 60.</span><span class="sxs-lookup"><span data-stu-id="0e407-118">For example, 60.</span></span>  
7. <span data-ttu-id="0e407-119">Geben Sie im Feld "Maßeinheit" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0e407-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="0e407-120">Beispielsweise "Minuten".</span><span class="sxs-lookup"><span data-stu-id="0e407-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="0e407-121">Legen Sie Mengen für Kanban fest</span><span class="sxs-lookup"><span data-stu-id="0e407-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="0e407-122">Legen Sie "Standardmenge" auf "5" fest.</span><span class="sxs-lookup"><span data-stu-id="0e407-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="0e407-123">Dies ist die Menge, die für jeden Kanban übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="0e407-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="0e407-124">Geben Sie im Feld "Feste Kanban-Menge" die Zahl "2"ein.</span><span class="sxs-lookup"><span data-stu-id="0e407-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="0e407-125">Dies ist der Betrag von Kanbans, die aktiv sein sollen.</span><span class="sxs-lookup"><span data-stu-id="0e407-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="0e407-126">In diesem Fall 2 Kanbans, die jeweils 5 übertragen.</span><span class="sxs-lookup"><span data-stu-id="0e407-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="0e407-127">Geben Sie im Feld "Min. Warnungsgrenzwert" "1 "ein.</span><span class="sxs-lookup"><span data-stu-id="0e407-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="0e407-128">Dies wird verwendet, um die Mindestmenge vollständiger Kanbans zu verfolgen, die am Ziel sein sollen.</span><span class="sxs-lookup"><span data-stu-id="0e407-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="0e407-129">Beispielsweise wird dieses in der Kanban-Mengenübersicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e407-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="0e407-130">Geben Sie im Feld "Max. Warnungsgrenzwert" "2 "ein.</span><span class="sxs-lookup"><span data-stu-id="0e407-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="0e407-131">Wird verwendet, um die maximale Menge vollständiger Kanbans zu verfolgen, die am Ziel sein sollen.</span><span class="sxs-lookup"><span data-stu-id="0e407-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="0e407-132">Beispielsweise wird dieses in der Kanban-Mengenübersicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e407-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="0e407-133">Kanbans erstellen</span><span class="sxs-lookup"><span data-stu-id="0e407-133">Create kanbans</span></span>
1. <span data-ttu-id="0e407-134">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0e407-134">Click Save.</span></span>
    * <span data-ttu-id="0e407-135">Die Kanban-Regel muss gespeichert werden, bevor Kanbans erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="0e407-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="0e407-136">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0e407-136">Click Add.</span></span>
    * <span data-ttu-id="0e407-137">Beachten Sie, dass keine aktiven Kanbans vorhanden sind, da die vorgeschlagene "Anzahl der neuen Kanbans" 2 beträgt. Dies entspricht der "Feste Kanban-Menge".</span><span class="sxs-lookup"><span data-stu-id="0e407-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="0e407-138">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="0e407-138">Click Create.</span></span>
    * <span data-ttu-id="0e407-139">Dadurch werden zwei Kanbans erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e407-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="0e407-140">Beachten Sie, dass 2 Kanbans für jeweils 5 für diese Kanban-Entnahmeregel erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0e407-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="0e407-141">Dies ist der letzte Schritt in diesem Verfahren.</span><span class="sxs-lookup"><span data-stu-id="0e407-141">This is the last step in this procedure.</span></span>  

