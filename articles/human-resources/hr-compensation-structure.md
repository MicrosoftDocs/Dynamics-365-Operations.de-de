---
title: Entwicklung einer Vergütungsstruktur
description: Dieser Artikel führt Sie durch die Erstellung eines festen Vergütungsplans und die Anmeldung von Mitarbeitern in den Plan durch die Regeln für die Anspruchsberechtigung.
author: andreabichsel
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75d1a05d4f94689581e2a67a13adeef6b14ac0cd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800902"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="77109-103">Entwicklung einer Vergütungsstruktur</span><span class="sxs-lookup"><span data-stu-id="77109-103">Develop a compensation structure</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="77109-104">Dieser Artikel führt Sie durch die Erstellung eines festen Vergütungsplans und die Anmeldung von Mitarbeitern in den Plan durch die Regeln für die Anspruchsberechtigung.</span><span class="sxs-lookup"><span data-stu-id="77109-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="77109-105">Dieser Artikel verwendet die USMF-Demodaten und gilt für Vergütungs- und Leistungsmanager.</span><span class="sxs-lookup"><span data-stu-id="77109-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="77109-106">Erstellen eines festen Vergütungsplans</span><span class="sxs-lookup"><span data-stu-id="77109-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="77109-107">Wählen Sie **Vergütungsmanagement**.</span><span class="sxs-lookup"><span data-stu-id="77109-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="77109-108">Wählen Sie **Feste Vergütungspläne**.</span><span class="sxs-lookup"><span data-stu-id="77109-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="77109-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="77109-109">Select **New**.</span></span>

4. <span data-ttu-id="77109-110">Geben Sie in das Feld **Plan** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="77109-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="77109-111">Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="77109-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="77109-112">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="77109-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="77109-113">Wählen Sie im Feld **Typ** aus, ob es sich bei dem festen Vergütungsplan um einen Plan **Band**, **Grad** oder **Schritt** handelt.</span><span class="sxs-lookup"><span data-stu-id="77109-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="77109-114">Das Ankreuzfeld **Empfehlung erlaubt** dient als Standardwert für alle Maßnahmen, die diesem Plan in einem Prozessereignis hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="77109-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="77109-115">Das Zulassen von Empfehlungen bietet Ihnen die Möglichkeit, den berechneten Richtbetrag zu überschreiben, wenn die Vergütung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="77109-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="77109-116">Mit dem Feld **Bereichstoleranz außerhalb des Bereichs** können Sie angeben, wie Sie Vergütungsbeträge behandeln wollen, die außerhalb des für die gegebene Ebene angegebenen Bereichs der Vergütungsstruktur liegen.</span><span class="sxs-lookup"><span data-stu-id="77109-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="77109-117">Wenn Sie das Feld **Bereichstoleranz außerhalb des Bereichs** auf **Keine** setzen, können Sie jeden beliebigen Vergütungsbetrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="77109-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="77109-118">**Weiche Toleranz** warnt die Benutzer, wenn der Ausgleichsbetrag unter dem Minimum oder über den maximalen Bezugspunktbeträgen für diese Ebene liegt.</span><span class="sxs-lookup"><span data-stu-id="77109-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="77109-119">Benutzer können die Warnung ignorieren und fortfahren.</span><span class="sxs-lookup"><span data-stu-id="77109-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="77109-120">**Harte Toleranz** erzeugt einen Fehler, wenn die Vergütung eines Mitarbeiters außerhalb des minimalen und maximalen Bezugspunktbetrags für diese Stufe liegt, und passt die Vergütung des Mitarbeiters automatisch so an, dass sie in den Bereich fällt.</span><span class="sxs-lookup"><span data-stu-id="77109-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="77109-121">Das Feld **Einstellungsregel** berechnet die Vergütung eines Mitarbeiters während eines Prozessereignisses.</span><span class="sxs-lookup"><span data-stu-id="77109-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="77109-122">Das Feld **Einstellungsregel** von **Prozent** berechnet eine Erhöhung, die anteilig für die Dauer der Beschäftigung des Mitarbeiters in dem Zyklus berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="77109-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="77109-123">Geben Sie im Feld **Währung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="77109-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="77109-124">Geben Sie in das Feld **Lohnratenumwandlung** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="77109-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="77109-125">Erweitern Sie den Abschnitt **Bereichsausnutzungsmatrix**.</span><span class="sxs-lookup"><span data-stu-id="77109-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="77109-126">Fügen Sie optional Bereichsauslastungsdatensätze hinzu, damit Mitarbeiter schneller zu ihrem Mittelwert gelangen und langsamer den Maximalwert ihres Bereichs erreichen.</span><span class="sxs-lookup"><span data-stu-id="77109-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="77109-127">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="77109-127">Select **Save**.</span></span> <span data-ttu-id="77109-128">Dadurch wird die Drucktaste **Vergütung** eingerichtet und Sie können mit der Definition Ihrer Vergütungsstruktur für den Plan fortfahren.</span><span class="sxs-lookup"><span data-stu-id="77109-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="77109-129">Wählen Sie **Vergütung einrichten**.</span><span class="sxs-lookup"><span data-stu-id="77109-129">Select **Set up compensation**.</span></span> <span data-ttu-id="77109-130">Sie können eine Vergütungsstruktur mit einer dieser drei Methoden anlegen:</span><span class="sxs-lookup"><span data-stu-id="77109-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="77109-131">Erstellen Sie eine völlig neue Struktur, indem Sie eine Reihe von Bezugspunkten auswählen und die Ebenen hinzufügen, um Ihre eigene Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77109-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="77109-132">Kopieren Sie eine Vergütungsstruktur aus einem bestehenden Plan als Ausgangspunkt und ändern Sie sie für den neuen Plan.</span><span class="sxs-lookup"><span data-stu-id="77109-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="77109-133">Wählen Sie ein bestehendes Vergütungsraster aus.</span><span class="sxs-lookup"><span data-stu-id="77109-133">Select an existing compensation grid.</span></span> <span data-ttu-id="77109-134">Wenn ein anderer Plan bereits das Vergütungsgitter verwendet, spiegelt der andere Plan ebenfalls alle Änderungen wider, die Sie am Gitter vornehmen.</span><span class="sxs-lookup"><span data-stu-id="77109-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="77109-135">Wählen Sie **Neues aus vorhandener Vergütungsmatrix erstellen**.</span><span class="sxs-lookup"><span data-stu-id="77109-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="77109-136">Geben Sie in das Feld **Kopieren von Raster** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="77109-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="77109-137">Optional können Sie den Namen des neuen Vergütungsrasters, das Sie anlegen, ändern, indem Sie das ausgewählte Raster kopieren.</span><span class="sxs-lookup"><span data-stu-id="77109-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="77109-138">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="77109-138">Select **OK**.</span></span>

19. <span data-ttu-id="77109-139">Wählen Sie **Massenänderung**.</span><span class="sxs-lookup"><span data-stu-id="77109-139">Select **Mass change**.</span></span> <span data-ttu-id="77109-140">Mit **Massenänderung** können Sie die Beträge der Vergütungsmatrix beibehalten, indem Sie eine prozentuale oder pauschale Betragserhöhung auf eine oder mehrere Ebenen oder Bezugspunkte anwenden.</span><span class="sxs-lookup"><span data-stu-id="77109-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="77109-141">Geben Sie in das Feld **Anpassungsbetrag** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="77109-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="77109-142">Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.</span><span class="sxs-lookup"><span data-stu-id="77109-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="77109-143">Klicken Sie auf **Anwendung auf Raster**.</span><span class="sxs-lookup"><span data-stu-id="77109-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="77109-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="77109-144">Close the page.</span></span> <span data-ttu-id="77109-145">Nachdem Sie die Vergütungsstruktur angelegt haben, können Sie auswählen, welcher der Referenzpunkte als Kontrollpunkt für den festen Vergütungsplan verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77109-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="77109-146">Der Kontrollpunkt wird zur Berechnung des Kompensationsverhältnisses eines Mitarbeiters verwendet.</span><span class="sxs-lookup"><span data-stu-id="77109-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="77109-147">Geben Sie in das Feld **Kontrollpunkt** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="77109-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="77109-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="77109-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="77109-149">Legen Sie eine Zulässigkeitsregel für den festen Vergütungsplan an.</span><span class="sxs-lookup"><span data-stu-id="77109-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="77109-150">Sie können einem Mitarbeiter erst dann einen festen Vergütungsplan zuordnen, wenn Sie die Zulässigkeitsregeln für den Plan definiert haben.</span><span class="sxs-lookup"><span data-stu-id="77109-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="77109-151">Wählen Sie **Zulässigkeitsregeln**.</span><span class="sxs-lookup"><span data-stu-id="77109-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="77109-152">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="77109-152">Select **New**.</span></span>

3. <span data-ttu-id="77109-153">Geben Sie in das Feld **Zulässigkeit** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="77109-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="77109-154">Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="77109-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="77109-155">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="77109-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="77109-156">Sowohl feste als auch variable Vergütungspläne verwenden Zulässigkeitsregeln.</span><span class="sxs-lookup"><span data-stu-id="77109-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="77109-157">Wählen Sie im Feld **Typ** die Art des Plans aus.</span><span class="sxs-lookup"><span data-stu-id="77109-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="77109-158">Geben Sie im Feld **Plan** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="77109-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="77109-159">Wählen Sie die Kriterien aus, die ein Mitarbeiter erfüllen muss, um für den Vergütungsplan berechtigt zu sein.</span><span class="sxs-lookup"><span data-stu-id="77109-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="77109-160">Die Kriterien können umfassen:</span><span class="sxs-lookup"><span data-stu-id="77109-160">Criteria can include:</span></span>

    - <span data-ttu-id="77109-161">**Abteilung**</span><span class="sxs-lookup"><span data-stu-id="77109-161">**Department**</span></span>
    - <span data-ttu-id="77109-162">**Gewerkschaft**</span><span class="sxs-lookup"><span data-stu-id="77109-162">**Labor union**</span></span>
    - <span data-ttu-id="77109-163">**Standort** (**Vergütungsregion**)</span><span class="sxs-lookup"><span data-stu-id="77109-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="77109-164">**Job**</span><span class="sxs-lookup"><span data-stu-id="77109-164">**Job**</span></span>
    - <span data-ttu-id="77109-165">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="77109-165">**Function**</span></span>
    - <span data-ttu-id="77109-166">**Stellentyp**</span><span class="sxs-lookup"><span data-stu-id="77109-166">**Job type**</span></span>
    - <span data-ttu-id="77109-167">**Vergütungsstufe**</span><span class="sxs-lookup"><span data-stu-id="77109-167">**Compensation level**</span></span>
    
    <span data-ttu-id="77109-168">Der Mitarbeiter muss alle angegebenen Kriterien erfüllen, um für den Vergütungsplan berechtigt zu sein.</span><span class="sxs-lookup"><span data-stu-id="77109-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="77109-169">Wenn Sie keine Kriterien angeben, sind alle Mitarbeiter für den Vergütungsplan berechtigt.</span><span class="sxs-lookup"><span data-stu-id="77109-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="77109-170">Wenn ein Mitarbeiter die in der Zulässigkeitsregel angegebenen Kriterien nicht erfüllt oder keine Zulässigkeitsregel für einen Vergütungsplan angegeben wurde, erscheint der Vergütungsplan nicht in der Nachschlagsliste, wenn Sie einen Satz für eine feste Vergütung für einen Mitarbeiter anlegen.</span><span class="sxs-lookup"><span data-stu-id="77109-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="77109-171">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="77109-171">Close the page.</span></span>

8. <span data-ttu-id="77109-172">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="77109-172">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]