--- 
title: "Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen"
description: "Kostenaufteilungsregeln werden verwendet, um Kosten zu verteilen, die wertmäßig für eine Kollektivkostenstelle gezählt wurden."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3096266510af2171c639a7c02c6698e4952a66cc
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="c4731-103">Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="c4731-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4731-104">Kostenaufteilungsregeln werden verwendet, um Kosten zu verteilen, die wertmäßig für eine Kollektivkostenstelle gezählt wurden.</span><span class="sxs-lookup"><span data-stu-id="c4731-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="c4731-105">Der Kosten-Buchhalter stird sichergestellt, dass die Kosten den Kostenstellen verteilt sind, auf Grundlage der ausgewählten Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="c4731-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="c4731-106">Eine Richtlinie und die entsprechenden Regeln werden einer Kostenkontrollsteuereinheit zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c4731-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="c4731-107">Dieser Aufgabenleitfaden verwendet ein Beispiel, um anzuzeigen, wie eine Kostenaufteilungsrichtlinie und die entsprechenden Regeln erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c4731-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="c4731-108">Eine Richtlinie erstellen</span><span class="sxs-lookup"><span data-stu-id="c4731-108">Create a policy</span></span>
1. <span data-ttu-id="c4731-109">Wechseln Sie zu Kostenbuchhaltung > Richtlinien > Kostenverteilungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="c4731-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="c4731-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c4731-110">Click New.</span></span>
3. <span data-ttu-id="c4731-111">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c4731-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="c4731-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c4731-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c4731-113">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c4731-114">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="c4731-114">Select Organization.</span></span>  
6. <span data-ttu-id="c4731-115">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c4731-116">Wählen Sie CDS P/L aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="c4731-117">Geben Sie im Feld "Statistische Dimension" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="c4731-118">Statistische Elemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="c4731-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="c4731-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c4731-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="c4731-120">Erstellen von Richtlinienregeln</span><span class="sxs-lookup"><span data-stu-id="c4731-120">Create rules for the policy</span></span>
1. <span data-ttu-id="c4731-121">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c4731-121">Click New.</span></span>
2. <span data-ttu-id="c4731-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c4731-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c4731-123">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c4731-124">Gesamte Hierarchie erweitern, um 094 auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c4731-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="c4731-125">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c4731-126">Wählen Sie weitere Betriebskosten und wählen Sie dann 605110 Reinigung.</span><span class="sxs-lookup"><span data-stu-id="c4731-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="c4731-127">Wählen Sie im Feld Kostenverhalten eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="c4731-128">Wählen Sie Fixkosten.</span><span class="sxs-lookup"><span data-stu-id="c4731-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="c4731-129">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="c4731-130">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c4731-130">Click New.</span></span>
8. <span data-ttu-id="c4731-131">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c4731-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c4731-132">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c4731-133">Gesamte Hierarchie erweitern, um 094 auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c4731-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="c4731-134">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c4731-135">Wählen Sie weitere Betriebskosten und wählen Sie dann 605150 Miete.</span><span class="sxs-lookup"><span data-stu-id="c4731-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="c4731-136">Wählen Sie im Feld Kostenverhalten eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="c4731-137">Wählen Sie Fixkosten.</span><span class="sxs-lookup"><span data-stu-id="c4731-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="c4731-138">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="c4731-139">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c4731-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="c4731-140">Weisen Sie einer Kostenkontrollesteuereinheit Regeln zu</span><span class="sxs-lookup"><span data-stu-id="c4731-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="c4731-141">Richtlinienzuweisungen für Kostensteuerungseinheit.</span><span class="sxs-lookup"><span data-stu-id="c4731-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="c4731-142">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c4731-142">Click New.</span></span>
3. <span data-ttu-id="c4731-143">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c4731-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c4731-144">Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="c4731-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="c4731-145">Wählen Sie 1. September im gültigen Geschäftsjahr aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="c4731-146">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c4731-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="c4731-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c4731-147">Click Save.</span></span>


