---
title: Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen
description: Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16d9dceb4c2a22eab9a5ecb8501393444f20498b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187819"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="acfc5-103">Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="acfc5-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="acfc5-104">Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.</span><span class="sxs-lookup"><span data-stu-id="acfc5-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="acfc5-105">Eine Richtlinie und die entsprechenden Regeln müssen einer Kostenkontrollesteuereinheit zugewiesen werden, sodass die Richtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="acfc5-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="acfc5-106">Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="acfc5-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="acfc5-107">Erstellen Sie eine Kosten-Verhaltenshierarchie</span><span class="sxs-lookup"><span data-stu-id="acfc5-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="acfc5-108">Wechseln Sie zu Kostenrechnung > Dimensionen > Dimensionshierarchien.</span><span class="sxs-lookup"><span data-stu-id="acfc5-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="acfc5-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acfc5-109">Click New.</span></span>
3. <span data-ttu-id="acfc5-110">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="acfc5-110">Click Create.</span></span>
4. <span data-ttu-id="acfc5-111">Im Dimensionshierarchienamengebiet geben Sie " Kostenverhaltenshierarchie "ein.</span><span class="sxs-lookup"><span data-stu-id="acfc5-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="acfc5-112">Geben Sie im Feld Dimension einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-113">Kostenelement auswählen.</span><span class="sxs-lookup"><span data-stu-id="acfc5-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="acfc5-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="acfc5-114">Click Save.</span></span>
7. <span data-ttu-id="acfc5-115">Klicken Sie auf "Hierarchie anzeigen".</span><span class="sxs-lookup"><span data-stu-id="acfc5-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="acfc5-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acfc5-116">Click New.</span></span>
9. <span data-ttu-id="acfc5-117">Geben Sie im Feld "Knotenname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="acfc5-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="acfc5-118">Fixkosten eingeben.</span><span class="sxs-lookup"><span data-stu-id="acfc5-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="acfc5-119">Wählen Sie in der Strukturdarstellung "Kostenverhaltenshierarchie " aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="acfc5-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acfc5-120">Click New.</span></span>
12. <span data-ttu-id="acfc5-121">Geben Sie im Feld "Knotenname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="acfc5-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="acfc5-122">Variable Kosten eingeben.</span><span class="sxs-lookup"><span data-stu-id="acfc5-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="acfc5-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="acfc5-123">Click Save.</span></span>
14. <span data-ttu-id="acfc5-124">Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Fixkosten aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="acfc5-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acfc5-125">Click New.</span></span>
16. <span data-ttu-id="acfc5-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="acfc5-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="acfc5-127">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-128">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="acfc5-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="acfc5-129">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-130">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="acfc5-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="acfc5-131">Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Variable Kosten aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="acfc5-132">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acfc5-132">Click New.</span></span>
21. <span data-ttu-id="acfc5-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="acfc5-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="acfc5-134">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-135">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="acfc5-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="acfc5-136">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-137">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="acfc5-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="acfc5-138">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="acfc5-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="acfc5-139">Erstellen von Richtlinien und Regeln</span><span class="sxs-lookup"><span data-stu-id="acfc5-139">Create the policy and rules</span></span>
1. <span data-ttu-id="acfc5-140">Wechseln Sie zu Kostenaufteilung > Richtlinien > Kostenverhaltensrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="acfc5-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="acfc5-141">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acfc5-141">Click New.</span></span>
3. <span data-ttu-id="acfc5-142">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="acfc5-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="acfc5-143">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-144">Wählen Sie die Richtlinienhierarchie aus, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="acfc5-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="acfc5-145">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-146">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="acfc5-146">Select Organization.</span></span>  
6. <span data-ttu-id="acfc5-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="acfc5-147">Click Save.</span></span>
7. <span data-ttu-id="acfc5-148">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acfc5-148">Click New.</span></span>
8. <span data-ttu-id="acfc5-149">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="acfc5-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="acfc5-150">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-151">Gesamte Hierarchie erweitern, um variable Kosten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="acfc5-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="acfc5-152">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="acfc5-153">Standardmäßig ist der variable Prozentsatz 100 Prozent.</span><span class="sxs-lookup"><span data-stu-id="acfc5-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="acfc5-154">Richtlinienzuweisungen für Kostensteuerungseinheit.</span><span class="sxs-lookup"><span data-stu-id="acfc5-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="acfc5-155">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acfc5-155">Click New.</span></span>
13. <span data-ttu-id="acfc5-156">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="acfc5-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="acfc5-157">Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="acfc5-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="acfc5-158">Die Regeln sind Datum-effektiv und eine Regel kann von einem Benutzer oder vom System gestrichcen werde, wenn eine neuere Version erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="acfc5-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="acfc5-159">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acfc5-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="acfc5-160">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="acfc5-160">Click Save.</span></span>

