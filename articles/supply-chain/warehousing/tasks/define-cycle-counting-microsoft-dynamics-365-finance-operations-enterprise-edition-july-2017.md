---
title: 'Zykluszählung definieren '
description: Zykluszählung ist ein Lagerortprozess, den Sie verwenden können, um Artikel des verfügbaren Lagerbestands zu überwachen.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8b7f39fc9a91d9fe219445e409d000266e24775
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429062"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="ddaa8-103">Zykluszählung definieren </span><span class="sxs-lookup"><span data-stu-id="ddaa8-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ddaa8-104">Zykluszählung ist ein Lagerortprozess, den Sie verwenden können, um Artikel des verfügbaren Lagerbestands zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="ddaa8-105">Diese Aufgabenerfassung zeigt, wie Sie: eine standardmäßige Inventurarbeitspriorität einrichten; ein Menüelement des mobilen Geräts aktivieren, um Entnahme und Zähleroperationen zu verarbeiten; einen Inventurschwellenwertauslöser aktivieren, wenn ein Lagerplatz leer wird; einen Zykluszählungsplan für einen bestimmten Artikel innerhalb eines bestimmten Lagerorts aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="ddaa8-106">Normalerweise werden diese Aufgaben von einem Lagerortleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="ddaa8-107">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="ddaa8-108">Priorität der Inventurarbeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="ddaa8-109">Gehen Sie im **Navigationsbereich** zu **Module > Lagerortverwaltung > Einstellungen > Parameter für Lagerortverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="ddaa8-110">Klicken Sie auf die Registerkarte **Permanente Inventurprüfung**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="ddaa8-111">Geben Sie im Feld **Standardmäßige Arbeitspriorität für Zykluszählung** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="ddaa8-112">Dieser Schritt ändert die Priorität der Zykluszählungsarbeit im Vergleich zu anderen Arten Arbeit am Lagerort.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="ddaa8-113">Wenn Sie eine niedrigere Nummer für die Zykluszählung als für andere Arbeitsarten setzen, steigt die Priorität der Zykluszählungsarbeit an.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="ddaa8-114">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-114">Click **Save**.</span></span>
5. <span data-ttu-id="ddaa8-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="ddaa8-116">Aktivieren des mobilen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-116">Enable the mobile device</span></span>
1. <span data-ttu-id="ddaa8-117">Gehen Sie im **Navigationsbereich** zu **Module > Lagerortverwaltung > Einstellungen > Mobiles Gerät > Menüelemente des mobilen Geräts**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="ddaa8-118">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-118">Click **New**.</span></span>
3. <span data-ttu-id="ddaa8-119">Geben Sie im Feld **Menüoptionsname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="ddaa8-120">Geben Sie im Feld **Titel** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="ddaa8-121">Wählen Sie im Feld **Modus** 'Arbeit' aus.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="ddaa8-122">Legen Sie die Option **Vorhandene Arbeit verwenden** auf „Ja“ fest.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="ddaa8-123">Wenn Sie diese Option auswählen, sucht das System nach vorhandener Arbeit, wenn das Menüelement des mobilen Geräts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="ddaa8-124">Wählen Sie im Feld **Geleitet von** 'Systemgeleitet' fest.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="ddaa8-125">Wenn "das referenzierte System" aktiviert ist, ist der Lagerarbeiter aufgefordert, Arbeit zu öffnen, die im definierten Arbeitsklassen ist.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="ddaa8-126">(Wir erstellen diese Arbeitsklassen weiter)</span><span class="sxs-lookup"><span data-stu-id="ddaa8-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="ddaa8-127">Erweitern Sie das Inforegister **Arbeitsklassen**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="ddaa8-128">Nun erstellen wir zwei Arbeitsklassen, die mit dem Menüelement des mobilen Geräts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="ddaa8-129">Wenn das Menüelement verwendet wird, werden diese Arbeitsklassen abgefragt, und dadurch wird dem Benutzer die Arbeit mit der höchsten Priorität angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="ddaa8-130">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-130">Click **New**.</span></span>
10. <span data-ttu-id="ddaa8-131">Wählen Sie im Feld **Arbeitsklassenkennung** einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="ddaa8-132">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-132">Click **New**.</span></span>
12. <span data-ttu-id="ddaa8-133">Wählen Sie im Feld **Arbeitsklassenkennung** einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="ddaa8-134">Klicken Sie im **Aktivitätsbereich** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="ddaa8-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-135">Close the page.</span></span>
15. <span data-ttu-id="ddaa8-136">Gehen Sie im **Navigationsbereich** zu **Module > Lagerortverwaltung > Einstellungen > Mobiles Gerät > Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="ddaa8-137">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ddaa8-138">Wählen Sie in der Struktur das Menüelement aus, das Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="ddaa8-139">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-139">Click **Edit**.</span></span>
19. <span data-ttu-id="ddaa8-140">Klicken Sie auf den Pfeil, um das Menüelement dem Menü hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="ddaa8-141">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="ddaa8-142">Schwellenwert für Zykluszählung erstellen</span><span class="sxs-lookup"><span data-stu-id="ddaa8-142">Create a counting threshold</span></span>
1. <span data-ttu-id="ddaa8-143">Gehen Sie im **Navigationsbereich** zu **Module > Lagerortverwaltung > Einstellungen > Zykluszählung > Permanente Inventur-Schwellenwerte**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="ddaa8-144">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-144">Click **New**.</span></span>
3. <span data-ttu-id="ddaa8-145">Geben Sie im Feld **Schwellenwertkennung für Zykluszählung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="ddaa8-146">Legen Sie die Option **Permanente Inventur sofort verarbeiten** auf „Ja“ fest.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="ddaa8-147">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="ddaa8-148">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-148">Click **Save**.</span></span>
7. <span data-ttu-id="ddaa8-149">Klicken Sie auf **Lagerplätze auswählen**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="ddaa8-150">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ddaa8-151">Wählen Sie im Feld **Kriterien** einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="ddaa8-152">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-152">Click **OK**.</span></span>
11. <span data-ttu-id="ddaa8-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="ddaa8-154">Zykluszählungsplan erstellen</span><span class="sxs-lookup"><span data-stu-id="ddaa8-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="ddaa8-155">Gehen Sie im **Navigationsbereich** zu **Module > Lagerortverwaltung > Einstellungen > Zykluszählung > Permanente Inventurpläne**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="ddaa8-156">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-156">Click **New**.</span></span>
3. <span data-ttu-id="ddaa8-157">Geben Sie im Feld **Zykluszählungs-Plankennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="ddaa8-158">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ddaa8-159">Geben Sie im Feld **Maximale Anzahl von Zykluszählungen** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="ddaa8-160">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-160">Click **Save**.</span></span>
7. <span data-ttu-id="ddaa8-161">Klicken Sie auf **Lagerplätze auswählen**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="ddaa8-162">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ddaa8-163">Wählen Sie im Feld **Kriterien** einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="ddaa8-164">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-164">Click **OK**.</span></span>
11. <span data-ttu-id="ddaa8-165">Geben Sie im Feld **Tage zwischen Zykluszählung** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="ddaa8-166">Wenn beispielsweise der Wert, der im Feld **Tage zwischen permanenter Inventur** angegeben ist, 5 ist, wird die permanente Inventurarbeit alle fünf Tage erstellt.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="ddaa8-167">Wenn jedoch Zykluszählungsarbeit an Tag drei verarbeitet wird, wird die nächste Zykluszählungsarbeit fünf Tage nachdem die letzte Zyklusinventur verarbeitet wurde, erstellt, am Tag acht.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="ddaa8-168">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-168">Click **Save**.</span></span>
13. <span data-ttu-id="ddaa8-169">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-169">Click **New**.</span></span>
14. <span data-ttu-id="ddaa8-170">Geben Sie im Feld **Laufende Nummer** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="ddaa8-171">Die Sortierreihenfolge ist von der kleinsten Nummer zur größten Nummer.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="ddaa8-172">Der Wert muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="ddaa8-173">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="ddaa8-174">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="ddaa8-175">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-175">Click **Save**.</span></span>
18. <span data-ttu-id="ddaa8-176">Klicken Sie auf die Abfrage **Produkt definieren**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="ddaa8-177">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="ddaa8-178">Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="ddaa8-179">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-179">Click **OK**.</span></span>
22. <span data-ttu-id="ddaa8-180">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-180">Close the page.</span></span>

