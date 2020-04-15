---
title: Eine Kanban-Regel für mehrere Aktivitäten erstellen
description: Diese Prozedur zeigt an, wie man eine Kanban-Regel erstellt, die mehrere Aktivitäten von einem Produktionsfluss umfasst.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b52e33c34a2fd151765833c68eab9091b22405cc
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147019"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="2fd26-103">Eine Kanban-Regel für mehrere Aktivitäten erstellen</span><span class="sxs-lookup"><span data-stu-id="2fd26-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2fd26-104">Diese Prozedur zeigt an, wie man eine Kanban-Regel erstellt, die mehrere Aktivitäten von einem Produktionsfluss umfasst.</span><span class="sxs-lookup"><span data-stu-id="2fd26-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="2fd26-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="2fd26-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="2fd26-106">Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrom-Manager vorgesehen, da diese die Produktion eines neuen oder geänderten Produkts in einer schlanken Umgebung vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="2fd26-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="2fd26-107">Neue Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="2fd26-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="2fd26-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="2fd26-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="2fd26-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2fd26-109">Click New.</span></span>
3. <span data-ttu-id="2fd26-110">Wählen Sie im Feld "Wiederbeschaffungsstrategie" die Option "Geplant" aus.</span><span class="sxs-lookup"><span data-stu-id="2fd26-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="2fd26-111">Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2fd26-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="2fd26-112">Wählen Sie "SpeakerAssemblyAndPolish" aus.</span><span class="sxs-lookup"><span data-stu-id="2fd26-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="2fd26-113">Aktivieren Sie das Kontrollkästchen "Mehrere Aktivitäten".</span><span class="sxs-lookup"><span data-stu-id="2fd26-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="2fd26-114">Der Zweck besteht darin, mehr als eine Aktivität in die Kanban-Regel einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="2fd26-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="2fd26-115">Sie wählen einen Pfad im Produktionsfluss aus, wenn Sie die letzte Planaktivität auswählen.</span><span class="sxs-lookup"><span data-stu-id="2fd26-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="2fd26-116">Geben Sie im Feld "Letzte Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2fd26-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="2fd26-117">Wählen Sie "SpeakerTestAndPackaging" aus.</span><span class="sxs-lookup"><span data-stu-id="2fd26-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="2fd26-118">Nachdem Sie den Wert auswählen, wird eine Seite automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2fd26-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="2fd26-119">Wählen Sie den Kanban-Fluss SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="2fd26-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="2fd26-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2fd26-120">Click OK.</span></span>  
7. <span data-ttu-id="2fd26-121">Erweitern Sie den Abschnitt "Details".</span><span class="sxs-lookup"><span data-stu-id="2fd26-121">Expand the Details section.</span></span>
8. <span data-ttu-id="2fd26-122">Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2fd26-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="2fd26-123">Wählen Sie Artikel L0006 aus.</span><span class="sxs-lookup"><span data-stu-id="2fd26-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="2fd26-124">Kanban erstellen und Einzelvorgänge anzeigen</span><span class="sxs-lookup"><span data-stu-id="2fd26-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="2fd26-125">Erweitern Sie den Abschnitt "Kanbans".</span><span class="sxs-lookup"><span data-stu-id="2fd26-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="2fd26-126">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2fd26-126">Click Add.</span></span>
3. <span data-ttu-id="2fd26-127">Geben Sie im Feld "Zahl neuer Kanbans" die Zahl "1" ein.</span><span class="sxs-lookup"><span data-stu-id="2fd26-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="2fd26-128">Dadurch wird ein Kanban erstellt.</span><span class="sxs-lookup"><span data-stu-id="2fd26-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="2fd26-129">Legen Sie "Produktmenge" auf '3' fest.</span><span class="sxs-lookup"><span data-stu-id="2fd26-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="2fd26-130">Kanban verarbeitet 3 Produkte.</span><span class="sxs-lookup"><span data-stu-id="2fd26-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="2fd26-131">Geben Sie im Feld "Datum/Uhrzeit der Fälligkeit" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="2fd26-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="2fd26-132">Sie können "Heute" eingeben.</span><span class="sxs-lookup"><span data-stu-id="2fd26-132">You can enter Today.</span></span>  
6. <span data-ttu-id="2fd26-133">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="2fd26-133">Click Create.</span></span>
7. <span data-ttu-id="2fd26-134">Klicken Sie auf Details.</span><span class="sxs-lookup"><span data-stu-id="2fd26-134">Click Details.</span></span>
    * <span data-ttu-id="2fd26-135">Beachten Sie, dass das Kanban zwei Prozesseinzelvorgänge vom Produktionsfluss hat.</span><span class="sxs-lookup"><span data-stu-id="2fd26-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="2fd26-136">Das erste ist "SpeakerAssemblyAndPolish" und das zweite ist "SpeakerTestAndPackaging".</span><span class="sxs-lookup"><span data-stu-id="2fd26-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="2fd26-137">Dies ist der letzte Schritt!</span><span class="sxs-lookup"><span data-stu-id="2fd26-137">This is the last step!</span></span>  

