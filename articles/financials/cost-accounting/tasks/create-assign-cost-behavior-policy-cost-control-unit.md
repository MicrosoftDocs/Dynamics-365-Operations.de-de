--- 
title: "Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen"
description: Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c7b39b7649aaef0d354b61e3d70b6cac887282ed
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="d0fee-103">Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="d0fee-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0fee-104">Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.</span><span class="sxs-lookup"><span data-stu-id="d0fee-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="d0fee-105">Eine Richtlinie und die entsprechenden Regeln müssen einer Kostenkontrollesteuereinheit zugewiesen werden, sodass die Richtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="d0fee-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="d0fee-106">Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d0fee-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="d0fee-107">Erstellen Sie eine Kosten-Verhaltenshierarchie</span><span class="sxs-lookup"><span data-stu-id="d0fee-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="d0fee-108">Wechseln Sie zu Kostenrechnung > Dimensionen > Dimensionshierarchien.</span><span class="sxs-lookup"><span data-stu-id="d0fee-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="d0fee-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0fee-109">Click New.</span></span>
3. <span data-ttu-id="d0fee-110">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="d0fee-110">Click Create.</span></span>
4. <span data-ttu-id="d0fee-111">Im Dimensionshierarchienamengebiet geben Sie " Kostenverhaltenshierarchie "ein.</span><span class="sxs-lookup"><span data-stu-id="d0fee-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="d0fee-112">Geben Sie im Feld Dimension einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-113">Kostenelement auswählen.</span><span class="sxs-lookup"><span data-stu-id="d0fee-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="d0fee-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d0fee-114">Click Save.</span></span>
7. <span data-ttu-id="d0fee-115">Klicken Sie auf "Hierarchie anzeigen".</span><span class="sxs-lookup"><span data-stu-id="d0fee-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="d0fee-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0fee-116">Click New.</span></span>
9. <span data-ttu-id="d0fee-117">Geben Sie im Feld "Knotenname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d0fee-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="d0fee-118">Fixkosten eingeben.</span><span class="sxs-lookup"><span data-stu-id="d0fee-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="d0fee-119">Wählen Sie in der Strukturdarstellung "Kostenverhaltenshierarchie " aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="d0fee-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0fee-120">Click New.</span></span>
12. <span data-ttu-id="d0fee-121">Geben Sie im Feld "Knotenname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d0fee-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="d0fee-122">Variable Kosten eingeben.</span><span class="sxs-lookup"><span data-stu-id="d0fee-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="d0fee-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d0fee-123">Click Save.</span></span>
14. <span data-ttu-id="d0fee-124">Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Fixkosten aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="d0fee-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0fee-125">Click New.</span></span>
16. <span data-ttu-id="d0fee-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0fee-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="d0fee-127">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-128">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="d0fee-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="d0fee-129">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-130">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="d0fee-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="d0fee-131">Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Variable Kosten aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="d0fee-132">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0fee-132">Click New.</span></span>
21. <span data-ttu-id="d0fee-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0fee-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="d0fee-134">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-135">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="d0fee-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="d0fee-136">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-137">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="d0fee-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="d0fee-138">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d0fee-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="d0fee-139">Erstellen von Richtlinien und Regeln</span><span class="sxs-lookup"><span data-stu-id="d0fee-139">Create the policy and rules</span></span>
1. <span data-ttu-id="d0fee-140">Wechseln Sie zu Kostenaufteilung > Richtlinien > Kostenverhaltensrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="d0fee-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="d0fee-141">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0fee-141">Click New.</span></span>
3. <span data-ttu-id="d0fee-142">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d0fee-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="d0fee-143">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-144">Wählen Sie die Richtlinienhierarchie aus, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="d0fee-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="d0fee-145">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-146">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="d0fee-146">Select Organization.</span></span>  
6. <span data-ttu-id="d0fee-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d0fee-147">Click Save.</span></span>
7. <span data-ttu-id="d0fee-148">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0fee-148">Click New.</span></span>
8. <span data-ttu-id="d0fee-149">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0fee-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d0fee-150">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-151">Gesamte Hierarchie erweitern, um variable Kosten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d0fee-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="d0fee-152">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d0fee-153">Standardmäßig ist der variable Prozentsatz 100 Prozent.</span><span class="sxs-lookup"><span data-stu-id="d0fee-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="d0fee-154">Richtlinienzuweisungen für Kostensteuerungseinheit.</span><span class="sxs-lookup"><span data-stu-id="d0fee-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="d0fee-155">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0fee-155">Click New.</span></span>
13. <span data-ttu-id="d0fee-156">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0fee-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="d0fee-157">Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="d0fee-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="d0fee-158">Die Regeln sind Datum-effektiv und eine Regel kann von einem Benutzer oder vom System gestrichcen werde, wenn eine neuere Version erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d0fee-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="d0fee-159">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0fee-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="d0fee-160">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d0fee-160">Click Save.</span></span>


