---
title: Eine Kostenzuweisungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen
description: Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006310d07dfa5b75941ca248736800bbb9e8e7b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969327"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="5a5e3-103">Eine Kostenzuweisungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="5a5e3-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a5e3-104">Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="5a5e3-105">Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="5a5e3-106">Eine Richtlinie erstellen</span><span class="sxs-lookup"><span data-stu-id="5a5e3-106">Create a policy</span></span>
1. <span data-ttu-id="5a5e3-107">Wechseln Sie zu Kostenbuchhaltung > Richtlinien > Kostenverteilungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="5a5e3-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5a5e3-108">Click New.</span></span>
3. <span data-ttu-id="5a5e3-109">Geben Sie im Feld "Richtliniennamen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="5a5e3-110">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="5a5e3-111">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="5a5e3-111">Select Organization.</span></span>  
5. <span data-ttu-id="5a5e3-112">Geben Sie im Feld "Statistische Dimension" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="5a5e3-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5a5e3-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="5a5e3-114">Zuordnungsregel erstellen</span><span class="sxs-lookup"><span data-stu-id="5a5e3-114">Create allocation rules</span></span>
1. <span data-ttu-id="5a5e3-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5a5e3-115">Click New.</span></span>
2. <span data-ttu-id="5a5e3-116">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="5a5e3-117">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="5a5e3-118">Im Feld Kostenverhalten wählen Sie Total aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="5a5e3-119">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="5a5e3-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5a5e3-120">Click New.</span></span>
7. <span data-ttu-id="5a5e3-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="5a5e3-122">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="5a5e3-123">Im Feld Kostenverhalten wählen Sie Total aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="5a5e3-124">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="5a5e3-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5a5e3-125">Click New.</span></span>
12. <span data-ttu-id="5a5e3-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="5a5e3-127">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="5a5e3-128">Im Feld Kostenverhalten wählen Sie Total aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="5a5e3-129">Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="5a5e3-130">Fahren Sie fort, bis Sie alle Regeln erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="5a5e3-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5a5e3-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="5a5e3-132">Die Richtlinie einer Kostensteuerungseinheit zuweisen</span><span class="sxs-lookup"><span data-stu-id="5a5e3-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="5a5e3-133">Richtlinienzuweisungen für Kostensteuerungseinheit.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="5a5e3-134">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5a5e3-134">Click New.</span></span>
3. <span data-ttu-id="5a5e3-135">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5a5e3-136">Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="5a5e3-137">Die Regeln sind Gültigkeitsdaten.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-137">The rules are date-effective.</span></span> <span data-ttu-id="5a5e3-138">Ein Benutzer oder das System kann die Regeln ablaufen lassen, wenn eine neuere Version erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="5a5e3-139">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5a5e3-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="5a5e3-140">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5a5e3-140">Click Save.</span></span>

