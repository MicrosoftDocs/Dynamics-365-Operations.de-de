---
title: Kontostrukturen erstellen
description: Dieser Aufgabenleitfaden führt Sie durch die Erstellung einer Kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571281"
---
# <a name="create-account-structures"></a><span data-ttu-id="e976b-103">Kontostrukturen erstellen</span><span class="sxs-lookup"><span data-stu-id="e976b-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e976b-104">Dieser Aufgabenleitfaden führt Sie durch die Erstellung einer Kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="e976b-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="e976b-105">Bei den Schritten wird das Demodatunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="e976b-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="e976b-106">Wechseln Sie zu Hauptbuch > Kontenplan > Strukturen > Kontostrukturen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e976b-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="e976b-107">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e976b-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="e976b-108">Im Feld "Kontostruktur" geben Sie einen Namen ein, um den Zweck der Kontostruktur zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e976b-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="e976b-109">Geben Sie im Feld "Beschreibung" eine Beschreibung ein, um den Zweck der Kontostruktur zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e976b-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="e976b-110">Klicken Sie auf Erstellen.</span><span class="sxs-lookup"><span data-stu-id="e976b-110">Click Create.</span></span>
6. <span data-ttu-id="e976b-111">Klicken Sie auf "Segment hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="e976b-111">Click Add segment.</span></span>
7. <span data-ttu-id="e976b-112">Wählen Sie in er Liste "Dimensionen" die Dimension aus, um der Kontostruktur hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e976b-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="e976b-113">Klicken Sie auf "Segment hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="e976b-113">Click Add segment.</span></span>
9. <span data-ttu-id="e976b-114">Klicken Sie auf "Segment hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="e976b-114">Click Add segment.</span></span>
10. <span data-ttu-id="e976b-115">Wählen Sie in er Liste "Dimensionen" die Dimension aus, um der Kontostruktur hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e976b-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="e976b-116">Klicken Sie auf "Segment hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="e976b-116">Click Add segment.</span></span>
12. <span data-ttu-id="e976b-117">Klicken Sie auf "Segment hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="e976b-117">Click Add segment.</span></span>
13. <span data-ttu-id="e976b-118">Wählen Sie in er Liste "Dimensionen" die Dimension aus, um der Kontostruktur hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e976b-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="e976b-119">Klicken Sie auf "Segment hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="e976b-119">Click Add segment.</span></span>
15. <span data-ttu-id="e976b-120">Wählen Sie im Raster das Segment aus, um die zulässigen Werte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e976b-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e976b-121">Beispielsweise klicken Sie in "Hauptkonto".</span><span class="sxs-lookup"><span data-stu-id="e976b-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="e976b-122">Wählen Sie im Feld "Operator" eine Option aus (z. B., "liegt zwischen" und "schließt ein").</span><span class="sxs-lookup"><span data-stu-id="e976b-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="e976b-123">Geben Sie im Feld "Wert" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e976b-124">Beispiel: 600000.</span><span class="sxs-lookup"><span data-stu-id="e976b-124">For example, 600000.</span></span>  
18. <span data-ttu-id="e976b-125">Geben Sie im Feld "bis" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="e976b-126">Beispiel: 699999.</span><span class="sxs-lookup"><span data-stu-id="e976b-126">For example, 699999.</span></span>  
19. <span data-ttu-id="e976b-127">Klicken Sie auf Übernehmen.</span><span class="sxs-lookup"><span data-stu-id="e976b-127">Click Apply.</span></span>
20. <span data-ttu-id="e976b-128">Wählen Sie im Raster das Segment aus, um die zulässigen Werte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e976b-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e976b-129">Beispiel: "Abteilung".</span><span class="sxs-lookup"><span data-stu-id="e976b-129">For example, Department.</span></span>  
21. <span data-ttu-id="e976b-130">Wählen Sie im Feld "Operator" eine Option aus (z. B., "liegt zwischen" und "schließt ein").</span><span class="sxs-lookup"><span data-stu-id="e976b-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="e976b-131">Geben Sie im Feld "Wert" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e976b-132">Beispiel: 022.</span><span class="sxs-lookup"><span data-stu-id="e976b-132">For example, 022.</span></span>  
23. <span data-ttu-id="e976b-133">Geben Sie im Feld "bis" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="e976b-134">Beispiel: 031.</span><span class="sxs-lookup"><span data-stu-id="e976b-134">For example, 031.</span></span>  
24. <span data-ttu-id="e976b-135">Klicken Sie auf "Neue Kriterien hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="e976b-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="e976b-136">Wählen Sie im Feld "Operator" eine Option aus (z. B., "liegt zwischen" und "schließt ein").</span><span class="sxs-lookup"><span data-stu-id="e976b-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="e976b-137">Geben Sie im Feld "Wert" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e976b-138">Beispiel: 033.</span><span class="sxs-lookup"><span data-stu-id="e976b-138">For example, 033.</span></span>  
27. <span data-ttu-id="e976b-139">Geben Sie im Feld "bis" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="e976b-140">Beispiel: 034.</span><span class="sxs-lookup"><span data-stu-id="e976b-140">For example, 034.</span></span>  
28. <span data-ttu-id="e976b-141">Klicken Sie auf Übernehmen.</span><span class="sxs-lookup"><span data-stu-id="e976b-141">Click Apply.</span></span>
29. <span data-ttu-id="e976b-142">Wählen Sie im Raster das Segment aus, um die zulässigen Werte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e976b-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e976b-143">Beispiel: "Kostenstelle".</span><span class="sxs-lookup"><span data-stu-id="e976b-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="e976b-144">Geben Sie im Feld "CostCenter" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="e976b-145">Beispiel: 007..021.</span><span class="sxs-lookup"><span data-stu-id="e976b-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="e976b-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e976b-146">Click Add.</span></span>
32. <span data-ttu-id="e976b-147">Geben Sie im Feld "MainAccount" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="e976b-148">Beispiel: 600000..699999</span><span class="sxs-lookup"><span data-stu-id="e976b-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="e976b-149">Wählen Sie im Raster das Segment aus, um die zulässigen Werte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e976b-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e976b-150">Beispiel: "Abteilung".</span><span class="sxs-lookup"><span data-stu-id="e976b-150">For example, Department.</span></span>  
34. <span data-ttu-id="e976b-151">Geben Sie im Feld "Abteilung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="e976b-152">Beispiel: 032.</span><span class="sxs-lookup"><span data-stu-id="e976b-152">For example, 032.</span></span>  
35. <span data-ttu-id="e976b-153">Geben Sie im Feld "CostCenter" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e976b-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="e976b-154">Beispiel: 086.</span><span class="sxs-lookup"><span data-stu-id="e976b-154">For example, 086.</span></span>  
36. <span data-ttu-id="e976b-155">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="e976b-155">Click Validate.</span></span>
37. <span data-ttu-id="e976b-156">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e976b-156">Click Activate.</span></span>
38. <span data-ttu-id="e976b-157">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e976b-157">Click Activate.</span></span>

