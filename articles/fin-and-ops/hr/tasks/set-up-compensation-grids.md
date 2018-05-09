--- 
title: "Vergütungsraster einrichten"
description: "Vergütungsstrukturen werden zur Definition und Pflege der Vergütungsstrukturen für feste Vergütungspläne verwendet."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8344534fb7708eaa18a3c84e233cccc889e54226
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="9d1c7-103">Vergütungsraster einrichten</span><span class="sxs-lookup"><span data-stu-id="9d1c7-103">Set up compensation grids</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d1c7-104">Vergütungsstrukturen werden zur Definition und Pflege der Vergütungsstrukturen für feste Vergütungspläne verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="9d1c7-105">Vergütungsraster können zwischen mehreren Plänen geteilt oder kopiert werden, wenn Sie einen neuen Vergütungsplan erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="9d1c7-106">Vor dem Erstellen eines Vergütungsrasters müssen Ebenen und Referenzpunkte eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="9d1c7-107">In diesem Beispiel erstellen Sie einen neuen Gradtyp für Vergütungsraster mit Demodaten für Ebenen und Referenzpunkte.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="9d1c7-108">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="9d1c7-109">Informationen zum Vergütungsraster einrichten</span><span class="sxs-lookup"><span data-stu-id="9d1c7-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="9d1c7-110">Wechseln Sie zu "Personalverwaltung" > "Vergütung" > "Feste Vergütung" > "Vergütungsraster".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="9d1c7-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-111">Click New.</span></span>
3. <span data-ttu-id="9d1c7-112">Geben Sie im Feld "Raster" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="9d1c7-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9d1c7-114">Wählen Sie im Feld "Typ" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="9d1c7-115">Geben Sie im Feld 'Referenzeinstellungen' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="9d1c7-116">Geben Sie im Feld "Währung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="9d1c7-117">Geben Sie im Feld "Währung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="9d1c7-118">Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="9d1c7-119">Level zur Vergütungsstruktur hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9d1c7-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="9d1c7-120">Klicken Sie auf "Vergütungsstruktur".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="9d1c7-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="9d1c7-122">Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="9d1c7-123">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-123">Click New.</span></span>
5. <span data-ttu-id="9d1c7-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9d1c7-125">Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="9d1c7-126">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-126">Click New.</span></span>
8. <span data-ttu-id="9d1c7-127">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9d1c7-128">Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="9d1c7-129">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-129">Click New.</span></span>
11. <span data-ttu-id="9d1c7-130">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="9d1c7-131">Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="9d1c7-132">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-132">Click New.</span></span>
14. <span data-ttu-id="9d1c7-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="9d1c7-134">Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="9d1c7-135">Füllen der Vergütungsstruktur mit Werten</span><span class="sxs-lookup"><span data-stu-id="9d1c7-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="9d1c7-136">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9d1c7-137">An diesem Punkt können Vergütungswerte manuell in jedes Feld in der Tabelle eingegeben werden, oder die Massenänderungsfunktionen kann zum Eintragen von mehreren Felder und für grundlegende Berechnungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="9d1c7-138">Klicken Sie auf "Massenänderung".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-138">Click Mass change.</span></span>
    * <span data-ttu-id="9d1c7-139">Bei diesem Raster wenden wir zuerst den Wert den Mittelwert der ersten Ebene auf alle Felder in der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="9d1c7-140">Dies dient als Grundlage für die Vergütungsmatrix.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="9d1c7-141">Wählen Sie im Feld "Regulierungstyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="9d1c7-142">Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="9d1c7-143">Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="9d1c7-144">Klicken Sie auf "Auf Raster anwenden".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="9d1c7-145">Jetzt verwenden wir die Massenänderungsfunktion, um die Beträge in jeder nächste Ebene über einen bestimmten Prozentsatz oder Betrag zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="9d1c7-146">In diesem Beispiel hat jeder Grad einen Umfang von 12,5% zwischen den Mittelwerten.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="9d1c7-147">Wählen Sie im Feld "Regulierungstyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="9d1c7-148">Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="9d1c7-149">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9d1c7-150">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="9d1c7-151">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="9d1c7-152">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="9d1c7-153">Klicken Sie auf "Auf Raster anwenden".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="9d1c7-154">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="9d1c7-155">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="9d1c7-156">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="9d1c7-157">Klicken Sie auf "Auf Raster anwenden".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="9d1c7-158">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="9d1c7-159">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="9d1c7-160">Klicken Sie auf "Auf Raster anwenden".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="9d1c7-161">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="9d1c7-162">Klicken Sie auf "Auf Raster anwenden".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="9d1c7-163">Jetzt verwenden wir die Massenänderungsfunktion, um die Mindest- und Höchstwerte für Referenzpunkte auf jede Ebene einzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="9d1c7-164">In diesem Beispiel wird ein Umfang von 50 % verwendet, so das der minimale Referenzpunkt um -20% und der maximale um +20% reguliert wird.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="9d1c7-165">Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="9d1c7-166">Geben Sie im Feld 'Referenzpunkt' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="9d1c7-167">Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="9d1c7-168">Klicken Sie auf "Auf Raster anwenden".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="9d1c7-169">Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="9d1c7-170">Geben Sie im Feld 'Referenzpunkt' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="9d1c7-171">Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.</span><span class="sxs-lookup"><span data-stu-id="9d1c7-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="9d1c7-172">Klicken Sie auf "Auf Raster anwenden".</span><span class="sxs-lookup"><span data-stu-id="9d1c7-172">Click Apply to grid.</span></span>


