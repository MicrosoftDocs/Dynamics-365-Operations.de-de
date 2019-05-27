---
title: Eine Kostenaufschlüsselungsrichtlinie erstellen
description: Dieses Verfahren zeigt, wie eine Rollup-Kostenrichtlinie und Regeln für die Richtlinie erstellt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f1fa434061832bd306cef13afc46c7f3adab0c0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543747"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="888de-103">Eine Kostenaufschlüsselungsrichtlinie erstellen</span><span class="sxs-lookup"><span data-stu-id="888de-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="888de-104">Dieses Verfahren zeigt, wie eine Rollup-Kostenrichtlinie und Regeln für die Richtlinie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="888de-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="888de-105">Die Demodaten, die verwendet werden, um diese Prozedur zu erstellen, sind USP2.</span><span class="sxs-lookup"><span data-stu-id="888de-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="888de-106">Eine Richtlinie erstellen</span><span class="sxs-lookup"><span data-stu-id="888de-106">Create a policy</span></span>
1. <span data-ttu-id="888de-107">Wechseln Sie zu Kostenbuchhaltung > Richtlinien > Kostenrollup-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="888de-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="888de-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="888de-108">Click New.</span></span>
3. <span data-ttu-id="888de-109">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="888de-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="888de-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="888de-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="888de-111">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-112">Kostenkategorie wählen</span><span class="sxs-lookup"><span data-stu-id="888de-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="888de-113">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-114">Kostenkategorie wählen</span><span class="sxs-lookup"><span data-stu-id="888de-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="888de-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="888de-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="888de-116">Erstellen von Kostenrollup-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="888de-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="888de-117">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="888de-117">Click New.</span></span>
2. <span data-ttu-id="888de-118">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="888de-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="888de-119">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-120">Wählen Sie 007 aus.</span><span class="sxs-lookup"><span data-stu-id="888de-120">Select 007.</span></span>  
4. <span data-ttu-id="888de-121">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-122">Kostenkategorie CE wählen</span><span class="sxs-lookup"><span data-stu-id="888de-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="888de-123">Geben Sie im Feld „Sekundäres Kostenelement” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-124">In vorliegenden Beispiel ordnen Sie das sekundäre Element CC-007 der Kostenstelle zu.</span><span class="sxs-lookup"><span data-stu-id="888de-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="888de-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="888de-125">Click New.</span></span>
7. <span data-ttu-id="888de-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="888de-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="888de-127">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-128">Wählen Sie 008 aus.</span><span class="sxs-lookup"><span data-stu-id="888de-128">Select 008.</span></span>  
9. <span data-ttu-id="888de-129">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-130">Kostenkategorie CE wählen</span><span class="sxs-lookup"><span data-stu-id="888de-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="888de-131">Geben Sie im Feld „Sekundäres Kostenelement” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-132">In vorliegenden Beispiel ordnen Sie das sekundäre Element CC-008 der Kostenstelle zu.</span><span class="sxs-lookup"><span data-stu-id="888de-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="888de-133">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="888de-133">Click New.</span></span>
12. <span data-ttu-id="888de-134">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="888de-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="888de-135">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-136">Wählen Sie 009 aus.</span><span class="sxs-lookup"><span data-stu-id="888de-136">Select 009.</span></span>  
14. <span data-ttu-id="888de-137">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-138">Kostenkategorie CE wählen</span><span class="sxs-lookup"><span data-stu-id="888de-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="888de-139">Geben Sie im Feld „Sekundäres Kostenelement” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="888de-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="888de-140">In vorliegenden Beispiel ordnen Sie das sekundäre Element CC-009 der Kostenstelle zu.</span><span class="sxs-lookup"><span data-stu-id="888de-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="888de-141">Fahren Sie fort, bis alle Kostenstellen den entsprechenden sekundären Kostenfaktoren zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="888de-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="888de-142">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="888de-142">Click Save.</span></span>

