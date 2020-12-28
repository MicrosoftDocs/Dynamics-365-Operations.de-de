---
title: Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen
description: Kostenaufteilungsregeln werden verwendet, um Kosten zu verteilen, die wertmäßig für eine Kollektivkostenstelle gezählt wurden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66921d5eddb31ffba0946c41f634719a684e4ad1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443506"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="41f7f-103">Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="41f7f-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41f7f-104">Kostenaufteilungsregeln werden verwendet, um Kosten zu verteilen, die wertmäßig für eine Kollektivkostenstelle gezählt wurden.</span><span class="sxs-lookup"><span data-stu-id="41f7f-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="41f7f-105">Der Kosten-Buchhalter stird sichergestellt, dass die Kosten den Kostenstellen verteilt sind, auf Grundlage der ausgewählten Verrechnungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="41f7f-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="41f7f-106">Eine Richtlinie und die entsprechenden Regeln werden einer Kostenkontrollsteuereinheit zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="41f7f-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="41f7f-107">Dieser Aufgabenleitfaden verwendet ein Beispiel, um anzuzeigen, wie eine Kostenaufteilungsrichtlinie und die entsprechenden Regeln erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="41f7f-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="41f7f-108">Eine Richtlinie erstellen</span><span class="sxs-lookup"><span data-stu-id="41f7f-108">Create a policy</span></span>
1. <span data-ttu-id="41f7f-109">Wechseln Sie zu Kostenbuchhaltung > Richtlinien > Kostenverteilungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="41f7f-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="41f7f-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="41f7f-110">Click New.</span></span>
3. <span data-ttu-id="41f7f-111">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="41f7f-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="41f7f-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="41f7f-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="41f7f-113">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="41f7f-114">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="41f7f-114">Select Organization.</span></span>  
6. <span data-ttu-id="41f7f-115">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="41f7f-116">Wählen Sie CDS P/L aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="41f7f-117">Geben Sie im Feld "Statistische Dimension" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="41f7f-118">Statistische Elemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="41f7f-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="41f7f-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="41f7f-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="41f7f-120">Erstellen von Richtlinienregeln</span><span class="sxs-lookup"><span data-stu-id="41f7f-120">Create rules for the policy</span></span>
1. <span data-ttu-id="41f7f-121">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="41f7f-121">Click New.</span></span>
2. <span data-ttu-id="41f7f-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="41f7f-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="41f7f-123">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41f7f-124">Gesamte Hierarchie erweitern, um 094 auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="41f7f-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="41f7f-125">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41f7f-126">Wählen Sie weitere Betriebskosten und wählen Sie dann 605110 Reinigung.</span><span class="sxs-lookup"><span data-stu-id="41f7f-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="41f7f-127">Wählen Sie im Feld Kostenverhalten eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="41f7f-128">Wählen Sie Fixkosten.</span><span class="sxs-lookup"><span data-stu-id="41f7f-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="41f7f-129">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="41f7f-130">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="41f7f-130">Click New.</span></span>
8. <span data-ttu-id="41f7f-131">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="41f7f-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="41f7f-132">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41f7f-133">Gesamte Hierarchie erweitern, um 094 auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="41f7f-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="41f7f-134">Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41f7f-135">Wählen Sie weitere Betriebskosten und wählen Sie dann 605150 Miete.</span><span class="sxs-lookup"><span data-stu-id="41f7f-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="41f7f-136">Wählen Sie im Feld Kostenverhalten eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="41f7f-137">Wählen Sie Fixkosten.</span><span class="sxs-lookup"><span data-stu-id="41f7f-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="41f7f-138">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="41f7f-139">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="41f7f-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="41f7f-140">Weisen Sie einer Kostenkontrollesteuereinheit Regeln zu</span><span class="sxs-lookup"><span data-stu-id="41f7f-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="41f7f-141">Richtlinienzuweisungen für Kostensteuerungseinheit.</span><span class="sxs-lookup"><span data-stu-id="41f7f-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="41f7f-142">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="41f7f-142">Click New.</span></span>
3. <span data-ttu-id="41f7f-143">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="41f7f-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="41f7f-144">Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="41f7f-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="41f7f-145">Wählen Sie 1. September im gültigen Geschäftsjahr aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="41f7f-146">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41f7f-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="41f7f-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="41f7f-147">Click Save.</span></span>

