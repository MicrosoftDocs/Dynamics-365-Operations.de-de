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
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58f888a373af33832c24518fbb5483c3de2d1a58
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208702"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="fc5fd-103">Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="fc5fd-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc5fd-104">Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="fc5fd-105">Eine Richtlinie und die entsprechenden Regeln müssen einer Kostenkontrollesteuereinheit zugewiesen werden, sodass die Richtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="fc5fd-106">Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="fc5fd-107">Erstellen Sie eine Kosten-Verhaltenshierarchie</span><span class="sxs-lookup"><span data-stu-id="fc5fd-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="fc5fd-108">Wechseln Sie zu Kostenrechnung > Dimensionen > Dimensionshierarchien.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="fc5fd-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-109">Click New.</span></span>
3. <span data-ttu-id="fc5fd-110">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-110">Click Create.</span></span>
4. <span data-ttu-id="fc5fd-111">Im Dimensionshierarchienamengebiet geben Sie " Kostenverhaltenshierarchie "ein.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="fc5fd-112">Geben Sie im Feld Dimension einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-113">Kostenelement auswählen.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="fc5fd-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-114">Click Save.</span></span>
7. <span data-ttu-id="fc5fd-115">Klicken Sie auf "Hierarchie anzeigen".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="fc5fd-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-116">Click New.</span></span>
9. <span data-ttu-id="fc5fd-117">Geben Sie im Feld "Knotenname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="fc5fd-118">Fixkosten eingeben.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="fc5fd-119">Wählen Sie in der Strukturdarstellung "Kostenverhaltenshierarchie " aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="fc5fd-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-120">Click New.</span></span>
12. <span data-ttu-id="fc5fd-121">Geben Sie im Feld "Knotenname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="fc5fd-122">Variable Kosten eingeben.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="fc5fd-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-123">Click Save.</span></span>
14. <span data-ttu-id="fc5fd-124">Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Fixkosten aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="fc5fd-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-125">Click New.</span></span>
16. <span data-ttu-id="fc5fd-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="fc5fd-127">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-128">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="fc5fd-129">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-130">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="fc5fd-131">Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Variable Kosten aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="fc5fd-132">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-132">Click New.</span></span>
21. <span data-ttu-id="fc5fd-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="fc5fd-134">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-135">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="fc5fd-136">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-137">Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="fc5fd-138">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="fc5fd-139">Erstellen von Richtlinien und Regeln</span><span class="sxs-lookup"><span data-stu-id="fc5fd-139">Create the policy and rules</span></span>
1. <span data-ttu-id="fc5fd-140">Wechseln Sie zu Kostenaufteilung > Richtlinien > Kostenverhaltensrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="fc5fd-141">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-141">Click New.</span></span>
3. <span data-ttu-id="fc5fd-142">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="fc5fd-143">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-144">Wählen Sie die Richtlinienhierarchie aus, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="fc5fd-145">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-146">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="fc5fd-146">Select Organization.</span></span>  
6. <span data-ttu-id="fc5fd-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-147">Click Save.</span></span>
7. <span data-ttu-id="fc5fd-148">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-148">Click New.</span></span>
8. <span data-ttu-id="fc5fd-149">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fc5fd-150">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-151">Gesamte Hierarchie erweitern, um variable Kosten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="fc5fd-152">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fc5fd-153">Standardmäßig ist der variable Prozentsatz 100 Prozent.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="fc5fd-154">Richtlinienzuweisungen für Kostensteuerungseinheit.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="fc5fd-155">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-155">Click New.</span></span>
13. <span data-ttu-id="fc5fd-156">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="fc5fd-157">Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="fc5fd-158">Die Regeln sind Datum-effektiv und eine Regel kann von einem Benutzer oder vom System gestrichcen werde, wenn eine neuere Version erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="fc5fd-159">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc5fd-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="fc5fd-160">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fc5fd-160">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]