--- 
title: "Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen"
description: Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
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
ms.openlocfilehash: 392cb83ceb8612a2e73cc54bb2d8d40c62a6b7b6
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="966ae-103">Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="966ae-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="966ae-104">Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.</span><span class="sxs-lookup"><span data-stu-id="966ae-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="966ae-105">Eine Richtlinie und die entsprechenden Regeln müssen einer Kostenkontrollesteuereinheit zugewiesen werden, sodass die Richtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="966ae-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="966ae-106">Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="966ae-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="966ae-107">Erstellen Sie eine Kosten-Verhaltenshierarchie</span><span class="sxs-lookup"><span data-stu-id="966ae-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="966ae-108">Wechseln Sie zu Kostenrechnung > Dimensionen > Dimensionshierarchien.</span><span class="sxs-lookup"><span data-stu-id="966ae-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="966ae-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="966ae-109">Click New.</span></span>
3. <span data-ttu-id="966ae-110">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="966ae-110">Click Create.</span></span>
4. <span data-ttu-id="966ae-111">Im Dimensionshierarchienamengebiet geben Sie " Kostenverhaltenshierarchie "ein.</span><span class="sxs-lookup"><span data-stu-id="966ae-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="966ae-112">Geben Sie im Feld Dimension einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-113">Kostenelement auswählen.</span><span class="sxs-lookup"><span data-stu-id="966ae-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="966ae-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="966ae-114">Click Save.</span></span>
7. <span data-ttu-id="966ae-115">Klicken Sie auf "Hierarchie anzeigen".</span><span class="sxs-lookup"><span data-stu-id="966ae-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="966ae-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="966ae-116">Click New.</span></span>
9. <span data-ttu-id="966ae-117">Geben Sie im Feld "Knotenname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="966ae-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="966ae-118">Fixkosten eingeben.</span><span class="sxs-lookup"><span data-stu-id="966ae-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="966ae-119">Wählen Sie in der Strukturdarstellung "Kostenverhaltenshierarchie " aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="966ae-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="966ae-120">Click New.</span></span>
12. <span data-ttu-id="966ae-121">Geben Sie im Feld "Knotenname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="966ae-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="966ae-122">Variable Kosten eingeben.</span><span class="sxs-lookup"><span data-stu-id="966ae-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="966ae-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="966ae-123">Click Save.</span></span>
14. <span data-ttu-id="966ae-124">Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Fixkosten aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="966ae-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="966ae-125">Click New.</span></span>
16. <span data-ttu-id="966ae-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="966ae-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="966ae-127">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-128">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="966ae-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="966ae-129">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-130">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="966ae-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="966ae-131">Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Variable Kosten aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="966ae-132">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="966ae-132">Click New.</span></span>
21. <span data-ttu-id="966ae-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="966ae-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="966ae-134">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-135">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="966ae-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="966ae-136">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-137">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="966ae-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="966ae-138">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="966ae-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="966ae-139">Erstellen von Richtlinien und Regeln</span><span class="sxs-lookup"><span data-stu-id="966ae-139">Create the policy and rules</span></span>
1. <span data-ttu-id="966ae-140">Wechseln Sie zu Kostenaufteilung > Richtlinien > Kostenverhaltensrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="966ae-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="966ae-141">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="966ae-141">Click New.</span></span>
3. <span data-ttu-id="966ae-142">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="966ae-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="966ae-143">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-144">Wählen Sie die Richtlinienhierarchie aus, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="966ae-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="966ae-145">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-146">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="966ae-146">Select Organization.</span></span>  
6. <span data-ttu-id="966ae-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="966ae-147">Click Save.</span></span>
7. <span data-ttu-id="966ae-148">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="966ae-148">Click New.</span></span>
8. <span data-ttu-id="966ae-149">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="966ae-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="966ae-150">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-151">Gesamte Hierarchie erweitern, um variable Kosten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="966ae-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="966ae-152">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="966ae-153">Standardmäßig ist der variable Prozentsatz 100 Prozent.</span><span class="sxs-lookup"><span data-stu-id="966ae-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="966ae-154">Richtlinienzuweisungen für Kostensteuerungseinheit.</span><span class="sxs-lookup"><span data-stu-id="966ae-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="966ae-155">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="966ae-155">Click New.</span></span>
13. <span data-ttu-id="966ae-156">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="966ae-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="966ae-157">Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="966ae-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="966ae-158">Die Regeln sind Datum-effektiv und eine Regel kann von einem Benutzer oder vom System gestrichcen werde, wenn eine neuere Version erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="966ae-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="966ae-159">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="966ae-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="966ae-160">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="966ae-160">Click Save.</span></span>


