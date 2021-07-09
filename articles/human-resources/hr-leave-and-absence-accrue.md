---
title: Urlaubs- und Abwesenheitspläne antizipieren
description: Sie können Urlaub und Abwesenheit in Dynamics 365 Human Resources für mehrere Mitarbeiter oder für eine Einzelperson abgrenzen.
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ddd4c55f6ebfbe91fb949a92cb379f51d826c465
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303463"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="79f4a-103">Urlaubs- und Abwesenheitspläne antizipieren</span><span class="sxs-lookup"><span data-stu-id="79f4a-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="79f4a-104">Sie können Urlaub und Abwesenheit in Dynamics 365 Human Resources für mehrere Mitarbeiter oder für eine Einzelperson abgrenzen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="79f4a-105">Abwesenheit und Urlaub für mehrere Mitarbeiter erfassen</span><span class="sxs-lookup"><span data-stu-id="79f4a-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="79f4a-106">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="79f4a-107">Unter **Urlaub verwalten**, wählen Sie **Urlaubs- und Abwesenheitspläne aufbauen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="79f4a-108">Das Dialogfeld **Urlaubs- und Abwesenheitspläne** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79f4a-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="79f4a-109">Unter **Aufgelaufen ab** wählen Sie entweder **Heutiges Datum** oder wählen Sie **Benutzerdefiniertes Datum** und geben Sie ein benutzerdefiniertes Datum ein.</span><span class="sxs-lookup"><span data-stu-id="79f4a-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="79f4a-110">Wenn Sie Rückstellungen für alle Unternehmen erstellen möchten, wählen Sie **Alle Unternehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="79f4a-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="79f4a-111">Wenn Sie Rückstellungen für einen einzelnen Urlaubsplan bearbeiten möchten, wählen Sie **Nein** für **Alle Pläne** aus, und dann wählen Sie **Urlaubsplan** aus.</span><span class="sxs-lookup"><span data-stu-id="79f4a-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="79f4a-112">Wenn Sie alle Unternehmen auswählen, können Sie keinen einzelnen Urlaubsplan auswählen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-112">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="79f4a-113">Wenn Sie den Erfassungsprozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="79f4a-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

    1. <span data-ttu-id="79f4a-114">Geben Sie Informationen für den Erfassungsprozess ein.</span><span class="sxs-lookup"><span data-stu-id="79f4a-114">Enter information for the accrual process.</span></span>
    2. <span data-ttu-id="79f4a-115">Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie dann die Wiederholungsinformationen ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and then select **OK**.</span></span>
    3. <span data-ttu-id="79f4a-116">Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>
    4. <span data-ttu-id="79f4a-117">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-117">Select **OK**.</span></span> <span data-ttu-id="79f4a-118">Der Erfassungsprozess wird mit den von Ihnen festgelegten Parametern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79f4a-118">The accrual process will run with the parameters you set.</span></span> 

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="79f4a-119">Abwesenheit und Urlaub für einen Mitarbeiter antizipieren</span><span class="sxs-lookup"><span data-stu-id="79f4a-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="79f4a-120">Wählen Sie im Datensatz des Mitarbeiters **Abweseneheit** aus.</span><span class="sxs-lookup"><span data-stu-id="79f4a-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="79f4a-121">**Urlaubs- und Abwesenheitspläne antizipieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="79f4a-122">Das Dialogfeld **Urlaubs- und Abwesenheitspläne** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79f4a-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="79f4a-123">Unter **Aufgelaufen ab** wählen Sie entweder **Heutiges Datum** oder wählen Sie **Benutzerdefiniertes Datum** und geben Sie ein benutzerdefiniertes Datum ein.</span><span class="sxs-lookup"><span data-stu-id="79f4a-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="79f4a-124">Wenn Sie Rückstellungen für alle Unternehmen erstellen möchten, wählen Sie **Alle Unternehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="79f4a-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="79f4a-125">Wenn Sie Rückstellungen für einen einzelnen Urlaubsplan bearbeiten möchten, wählen Sie **Nein** für **Alle Pläne** aus, und dann wählen Sie **Urlaubsplan** aus.</span><span class="sxs-lookup"><span data-stu-id="79f4a-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="79f4a-126">Wenn Sie alle Unternehmen auswählen, können Sie keinen einzelnen Urlaubsplan auswählen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-126">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="79f4a-127">Wenn Sie den Erfassungsprozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="79f4a-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="79f4a-128">Geben Sie Informationen für den Erfassungsprozess ein.</span><span class="sxs-lookup"><span data-stu-id="79f4a-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="79f4a-129">Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="79f4a-130">Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="79f4a-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-131">Select **OK**.</span></span> <span data-ttu-id="79f4a-132">Der Erfassungsprozess wird mit den von Ihnen festgelegten Parametern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79f4a-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="79f4a-133">Aufgelaufene Abwesenheit und Urlaub für mehrere Mitarbeiter löschen</span><span class="sxs-lookup"><span data-stu-id="79f4a-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="79f4a-134">Löschen Sie Abgrenzungssätze für einen bestimmten Plan und Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="79f4a-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="79f4a-135">Abgrenzungsdaten müssen heute oder in der Zukunft datiert werden.</span><span class="sxs-lookup"><span data-stu-id="79f4a-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="79f4a-136">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="79f4a-137">Unter **Urlaub verwalten**, wählen Sie **Aufgelaufene Urlaubs- und Abwesenheitspläne löschen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="79f4a-138">Im Dialogfeld **Aufgelaufene Urlaubs- und Abwesenheitspläne löschen** wählen Sie **Plan verlassen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span>

4. <span data-ttu-id="79f4a-139">Falls zutreffend, wählen Sie **Saldo-Anpassungen löschen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="79f4a-140">Geben Sie ein oder wählen Sie **Datum Urlaub aussetzen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="79f4a-141">Dieses Datum muss entweder heute oder in der Zukunft liegen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-141">This date has to be either today or in the future.</span></span>

6. <span data-ttu-id="79f4a-142">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-142">Select **OK**.</span></span> <span data-ttu-id="79f4a-143">Der Erfassungsprozess löscht Abgrenzungen mit den von Ihnen festgelegten Parametern.</span><span class="sxs-lookup"><span data-stu-id="79f4a-143">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="79f4a-144">Aufgelaufene Abwesenheit und Urlaub für einzelne Mitarbeiter löschen</span><span class="sxs-lookup"><span data-stu-id="79f4a-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="79f4a-145">Wählen Sie im Datensatz des Mitarbeiters **Abweseneheit** aus.</span><span class="sxs-lookup"><span data-stu-id="79f4a-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="79f4a-146">**Aufgelaufene Urlaubs- und Abwesenheitspläne löschen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="79f4a-147">Im Dialogfeld **Aufgelaufene Urlaubs- und Abwesenheitspläne löschen** wählen Sie **Plan verlassen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span>

4. <span data-ttu-id="79f4a-148">Falls zutreffend, wählen Sie **Saldo-Anpassungen löschen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="79f4a-149">Geben Sie ein oder wählen Sie **Datum Urlaub aussetzen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="79f4a-150">Das Datum muss entweder heute oder in der Zukunft liegen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-150">This date must be either today or in the future.</span></span>

6. <span data-ttu-id="79f4a-151">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-151">Select **OK**.</span></span> <span data-ttu-id="79f4a-152">Der Erfassungsprozess löscht Abgrenzungen mit den von Ihnen festgelegten Parametern.</span><span class="sxs-lookup"><span data-stu-id="79f4a-152">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="79f4a-153">Überprüfen Sie die Abgrenzungs- und Löschprozesse</span><span class="sxs-lookup"><span data-stu-id="79f4a-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="79f4a-154">**Rückstellungsprüfung verlassen** zeigt jedes Mal an, wenn Sie eine Rückstellung für einen oder alle Mitarbeiter ausführen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="79f4a-155">Das Datum und die Person, die die Aktion ausgeführt hat, werden ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79f4a-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="79f4a-156">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="79f4a-157">Unter **Urlaub verwalten**, wählen Sie **Aufgelaufene Urlaubs- und Abwesenheitsprüfung löschen**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="leave-accrual-transaction-auditing"></a><span data-ttu-id="79f4a-158">Überwachung von Urlaubsabgrenzungstransaktionen</span><span class="sxs-lookup"><span data-stu-id="79f4a-158">Leave accrual transaction auditing</span></span>

<span data-ttu-id="79f4a-159">Diese Funktion hilft den Managern von Urlaub und Abwesenheit, die Transaktionen zur Abgrenzung von Urlaub und Abwesenheit zu verstehen, die mit den Zeitsalden eines Mitarbeiters für eine bestimmte Urlaubsart zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="79f4a-159">This feature helps leave and absence managers understand the leave and absence accrual transactions related to an employee’s time off balances for a specific leave type.</span></span>

<span data-ttu-id="79f4a-160">Zum Anzeigen von Transaktionsdetails:</span><span class="sxs-lookup"><span data-stu-id="79f4a-160">To view transaction details:</span></span>

1. <span data-ttu-id="79f4a-161">Wählen Sie im Datensatz des Mitarbeiters **Abweseneheit** aus.</span><span class="sxs-lookup"><span data-stu-id="79f4a-161">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="79f4a-162">Wählen Sie **Freizeit anzeigen** und wählen Sie dann die Registerkarte **Saldo**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-162">Select **View time off**, and then select the **Balances** tab.</span></span>

<span data-ttu-id="79f4a-163">Wählen Sie den numerischen Wert im Feld aus, um die Abgrenzungstransaktionen anzuzeigen, die sich auf einen bestimmten Urlaubstyp beziehen in der Spalte **Aktueller Saldo**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-163">To view the accrual transactions related to a specific leave type, select the numerical value in the **Current balance** column.</span></span>

<span data-ttu-id="79f4a-164">Um die Transaktionsdetails für einen bestimmten Abgrenzungsbetrag anzuzeigen, wählen Sie eine Abgrenzungszeile aus und öffnen Sie den Bereich **Verwandte Informationen** auf der rechten Seite, und öffnen Sie dann den Bereich **Transaktionsdetails**.</span><span class="sxs-lookup"><span data-stu-id="79f4a-164">To view the transaction details for a specific accrual amount, select an accrual row, open the **Related information** panel on the right, and then open the **Transaction details** section.</span></span> <span data-ttu-id="79f4a-165">Der Abschnitt Transaktionsdetails wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="79f4a-165">The Transaction details section displays:</span></span>

- <span data-ttu-id="79f4a-166">Änderungen des Urlaubstypsaldos des Mitarbeiters</span><span class="sxs-lookup"><span data-stu-id="79f4a-166">Changes to the employee’s leave type balance</span></span>
- <span data-ttu-id="79f4a-167">Beschäftigungsdetails für den angegebenen Abgrenzungszeitraum</span><span class="sxs-lookup"><span data-stu-id="79f4a-167">Employment details for that specified accrual period</span></span>
- <span data-ttu-id="79f4a-168">Details zum Abgrenzungszeitraum und zu den Sätzen</span><span class="sxs-lookup"><span data-stu-id="79f4a-168">Details about the accrual period and rates</span></span>
- <span data-ttu-id="79f4a-169">Alle Änderungen, die vorgenommen wurden, um die Plan-Konfigurationen zu verlassen</span><span class="sxs-lookup"><span data-stu-id="79f4a-169">Any changes made to leave plan configurations</span></span>

![Zeigt die Überwachung von Urlaubsabgrenzungstransaktionen an](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a><span data-ttu-id="79f4a-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79f4a-171">See also</span></span>

[<span data-ttu-id="79f4a-172">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="79f4a-172">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="79f4a-173">Einen Urlaubs- und Abwesenheitsplan erstellen</span><span class="sxs-lookup"><span data-stu-id="79f4a-173">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
