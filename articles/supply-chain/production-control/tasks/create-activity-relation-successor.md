---
title: Aktivitätsrelation erstellen -  Nachfolger
description: Der Ablauf von Aktivitäten in einem Leanproduktionsfluss wird durch Aktivitätsrelationen dokumentiert.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07ebb7d2158964a5d8862df998fe470032a0d354
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550412"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="5e1b7-103">Aktivitätsrelation erstellen -  Nachfolger</span><span class="sxs-lookup"><span data-stu-id="5e1b7-103">Create activity relation - Successor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e1b7-104">Der Ablauf von Aktivitäten in einem Leanproduktionsfluss wird durch Aktivitätsrelationen dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="5e1b7-105">Diese Aufzeichnung zeigt, wie Sie eine Aktivitätsrelation erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="5e1b7-106">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="5e1b7-106">Prerequisites:</span></span>

- <span data-ttu-id="5e1b7-107">Ein Produktionsfluss und eine Version im Entwurfsmodus.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="5e1b7-108">Zwei Aktivitäten, die im Produktionsfluss aufeinander folgen, werden erstellt, sind aber nicht verknüpft.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="5e1b7-109">Produktionsflussversion suchen</span><span class="sxs-lookup"><span data-stu-id="5e1b7-109">Find the production flow version</span></span> 
1. <span data-ttu-id="5e1b7-110">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="5e1b7-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="5e1b7-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5e1b7-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5e1b7-113">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="5e1b7-114">Wählen Sie in der Liste ein Entwurfsversion aus.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="5e1b7-115">Aktivitätsrelationen können zum Entwurf oder zu aktiven Versionen eines Produktionsflusses hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="5e1b7-116">Aktivitätsüberblick öffnen</span><span class="sxs-lookup"><span data-stu-id="5e1b7-116">Open the activity overview</span></span>
1. <span data-ttu-id="5e1b7-117">Klicken Sie auf "Aktivitäten".</span><span class="sxs-lookup"><span data-stu-id="5e1b7-117">Click Activities.</span></span>
    * <span data-ttu-id="5e1b7-118">Beachten Sie, dass im Formular alle Aktivitäten des Produktionsflusses angezeigt werden, die der Version der Produktionsflüsse zugeordnet sind, in der Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="5e1b7-119">Eine Folgeaktivität hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5e1b7-119">Add a Successor</span></span>
1. <span data-ttu-id="5e1b7-120">Klicken Sie "Folgeaktivität hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5e1b7-120">Click Add successor.</span></span>
2. <span data-ttu-id="5e1b7-121">Klicken Sie im Feld "Aktivität" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5e1b7-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5e1b7-123">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5e1b7-124">Markieren Sie das Kontrollkästchen "Einschränkung".</span><span class="sxs-lookup"><span data-stu-id="5e1b7-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="5e1b7-125">Geben Sie eine Zahl in das Feld 'Einschränkungswert' ein.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="5e1b7-126">Die Einschränkungszeit ist die Zeit, die zwischen dem geplanten Enddatum der vorherigen Aktivität (Fälligkeitsdatum und Uhrzeit) und dem geplantem Start der Folgeaktivität eingeplant wird.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="5e1b7-127">Geben Sie im Feld "Einheit" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="5e1b7-128">Geben Sie im Feld "Zykluszeitanteil" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="5e1b7-129">Wenn beide Aktionen am gleichen Takt ausgeführt werden, sollte der Zykluszeitanteil 1 sein.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="5e1b7-130">Wenn die vorherige Aktivität die doppelten Geschwindigkeit der Folgeaktivität ausgeführt wird, sollte das Verhältnis 2 sein.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="5e1b7-131">Anhand des Anteils werden die durchschnittlichen Zykluszeiten für alle Aktivitäten des Produktionsflusses berechnet.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="5e1b7-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5e1b7-132">Click OK.</span></span>
10. <span data-ttu-id="5e1b7-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-133">Close the page.</span></span>
11. <span data-ttu-id="5e1b7-134">Klicken Sie auf die Registerkarte "GridPanel".</span><span class="sxs-lookup"><span data-stu-id="5e1b7-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="5e1b7-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-135">Close the page.</span></span>
13. <span data-ttu-id="5e1b7-136">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-136">Refresh the page.</span></span>

