--- 
title: "Eine Kostenzuweisungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen"
description: "Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="e47cf-103">Eine Kostenzuweisungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="e47cf-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e47cf-104">Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e47cf-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="e47cf-105">Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="e47cf-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="e47cf-106">Eine Richtlinie erstellen</span><span class="sxs-lookup"><span data-stu-id="e47cf-106">Create a policy</span></span>
1. <span data-ttu-id="e47cf-107">Wechseln Sie zu Kostenbuchhaltung > Richtlinien > Kostenverteilungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="e47cf-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="e47cf-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e47cf-108">Click New.</span></span>
3. <span data-ttu-id="e47cf-109">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e47cf-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="e47cf-110">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="e47cf-111">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="e47cf-111">Select Organization.</span></span>  
5. <span data-ttu-id="e47cf-112">Geben Sie im Feld "Statistische Dimension" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="e47cf-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e47cf-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="e47cf-114">Zuordnungsregel erstellen</span><span class="sxs-lookup"><span data-stu-id="e47cf-114">Create allocation rules</span></span>
1. <span data-ttu-id="e47cf-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e47cf-115">Click New.</span></span>
2. <span data-ttu-id="e47cf-116">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="e47cf-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e47cf-117">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="e47cf-118">Im Feld Kostenverhalten wählen Sie Total aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="e47cf-119">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="e47cf-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e47cf-120">Click New.</span></span>
7. <span data-ttu-id="e47cf-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="e47cf-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="e47cf-122">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="e47cf-123">Im Feld Kostenverhalten wählen Sie Total aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="e47cf-124">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="e47cf-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e47cf-125">Click New.</span></span>
12. <span data-ttu-id="e47cf-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="e47cf-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="e47cf-127">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="e47cf-128">Im Feld Kostenverhalten wählen Sie Total aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="e47cf-129">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="e47cf-130">Fahren Sie fort, bis Sie alle Regeln erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e47cf-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="e47cf-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e47cf-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="e47cf-132">Die Richtlinie einer Kostensteuerungseinheit zuweisen</span><span class="sxs-lookup"><span data-stu-id="e47cf-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="e47cf-133">Richtlinienzuweisungen für Kostensteuerungseinheit.</span><span class="sxs-lookup"><span data-stu-id="e47cf-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="e47cf-134">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e47cf-134">Click New.</span></span>
3. <span data-ttu-id="e47cf-135">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="e47cf-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e47cf-136">Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="e47cf-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="e47cf-137">Die Regeln sind Gültigkeitsdaten.</span><span class="sxs-lookup"><span data-stu-id="e47cf-137">The rules are date-effective.</span></span> <span data-ttu-id="e47cf-138">Ein Benutzer oder das System kann die Regeln ablaufen lassen, wenn eine neuere Version erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e47cf-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="e47cf-139">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e47cf-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="e47cf-140">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e47cf-140">Click Save.</span></span>


