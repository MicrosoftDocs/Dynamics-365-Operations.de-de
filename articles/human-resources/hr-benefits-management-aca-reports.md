---
title: Berichte zum Affordable Care Act in der Vorteilsverwaltung generieren
description: In diesem Thema wird beschrieben, wie Sie mit der Vorteilsverwaltung Informationen nachverfolgen können, die auf Formular 1095-B und Formular 1095-C für das Arbeitgebermandat des Affordable Care Act (ACA) angegeben sind.
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 2e4b250f4a059719067a9e19bbf3ce4aecc9bb1f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112712"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="7f29b-103">ACA-Berichte in der Vorteilsverwaltung generieren</span><span class="sxs-lookup"><span data-stu-id="7f29b-103">Generate ACA reports in Benefits management</span></span>

<span data-ttu-id="7f29b-104">Mit der Vorteilsverwaltung können Sie Informationen nachverfolgen, die auf Formular 1095-B und Formular 1095-C für das Arbeitgebermandat des Affordable Care Act (ACA) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7f29b-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="7f29b-105">Wie die ACA-Berichtsfunktion im alten **Vorteils**-Arbeitsbereich gilt diese Funktionalität nur für juristische Personen in den USA.</span><span class="sxs-lookup"><span data-stu-id="7f29b-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="7f29b-106">Um diese Funktionalität nutzen zu können, müssen Sie zuerst **Erweiterte Vorteilsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7f29b-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="7f29b-107">Weitere Informationen, einschließlich wichtiger Vorbehalte zur Vorteilsverwaltung finden Sie unter [Aktivieren oder Deaktivieren der Vorteilsverwaltung](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="7f29b-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f29b-108">Sie können ACA-Berichte nur entweder im Arbeitsbereich **Vorteilsverwaltung** oder im alten Arbetisbereich **Vorteile** verwenden, nicht in beiden.</span><span class="sxs-lookup"><span data-stu-id="7f29b-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="7f29b-109">Wenn Sie beispielsweise zur Vorteilsverwaltung gewechselt sind, ist die ACA-Berichterstellung nur über Arbeitsbereich **Vorteilsverwaltung** verfügbar, nicht über den alten Arbeitsbereich **Vorteile**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="7f29b-110">Wenn Sie in der Mitte eines Beitrittsjahres zur Vorteilsverwaltung wechseln, müssen Sie die Mitarbeiterdaten für das gesamte Jahr korrekt in der Vorteilsverwaltung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7f29b-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="7f29b-111">Auf diese Weise stellen Sie sicher, dass Sie für das ganze Jahr genaue Berichtsinformationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="7f29b-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="7f29b-112">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="7f29b-112">Getting started</span></span>

<span data-ttu-id="7f29b-113">Um Informationen für 1095 Formulare zu verfolgen, erstellen Sie zunächst eine oder mehrere Dispositionssteuerungsgruppen für Affordable Care.</span><span class="sxs-lookup"><span data-stu-id="7f29b-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="7f29b-114">Diese Gruppen geben die folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="7f29b-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="7f29b-115">Das Angebot für Disposition, das einem Mitarbeiter zur Verfügung gestellt wurde</span><span class="sxs-lookup"><span data-stu-id="7f29b-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="7f29b-116">Der Arbeitnehmeranteil an der niedrigsten monatlichen Prämie, wenn die Kosten über der Bundesarmutsgrenze liegen</span><span class="sxs-lookup"><span data-stu-id="7f29b-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="7f29b-117">Der Safe Harbor, der gegebenenfalls vom Arbeitgeber genutzt wird</span><span class="sxs-lookup"><span data-stu-id="7f29b-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="7f29b-118">Mit Affordable Care-Dispositionssteuerungsgruppen können Sie diese Informationen für mehrere Mitarbeiterdatensätze mit denselben Bedingungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="7f29b-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="7f29b-119">Sie können einem oder mehreren Mitarbeitern problemlos Gruppen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="7f29b-120">Erstellen oder bearbeiten Sie eine Affordable Care-Dispositionssteuerungsgruppe</span><span class="sxs-lookup"><span data-stu-id="7f29b-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="7f29b-121">Im **Vorteilsverwaltung**-Arbeitsbereich wählen Sie **Affordable Care-Dispositionssteuerungsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Affordable Care-Dispositionssteuerungsgruppe auswählen](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="7f29b-123">Wählen Sie **Neu** aus, um eine neue Affordable Care-Dispositionssteuerungsgruppe zu erstellen, oder **Bearbeiten**, um eine vorhandene Gruppe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7f29b-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![„Neu“ oder „Bearbeiten“ auswählen](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="7f29b-125">Stellen Sie die folgenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="7f29b-125">Set the following fields.</span></span>

    | <span data-ttu-id="7f29b-126">Feld</span><span class="sxs-lookup"><span data-stu-id="7f29b-126">Field</span></span> | <span data-ttu-id="7f29b-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f29b-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="7f29b-128">Name</span><span class="sxs-lookup"><span data-stu-id="7f29b-128">Name</span></span> | <span data-ttu-id="7f29b-129">Geben Sie einen Namen für die Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="7f29b-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="7f29b-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f29b-130">Description</span></span> | <span data-ttu-id="7f29b-131">Geben Sie eine Beschreibung der Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="7f29b-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="7f29b-132">Abdeckungsangebot</span><span class="sxs-lookup"><span data-stu-id="7f29b-132">Offer of coverage</span></span> | <span data-ttu-id="7f29b-133">Die Disposition, die den Mitarbeitern, ihren Ehepartnern oder Partnern und ihren Unterhaltsberechtigten angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="7f29b-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="7f29b-134">Mitarbeiteranteil an den Kosten</span><span class="sxs-lookup"><span data-stu-id="7f29b-134">Employee share of cost</span></span> | <span data-ttu-id="7f29b-135">Der Betrag, für den der Mitarbeiter zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="7f29b-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="7f29b-136">Gültiger Abschnitt 4980H in den Bestimmungen des amerikanischen Handelsministeriums (Safe Harbor)</span><span class="sxs-lookup"><span data-stu-id="7f29b-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="7f29b-137">Der Code für 4980H Safe Harbor oder Transition Relief.</span><span class="sxs-lookup"><span data-stu-id="7f29b-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="7f29b-138">Startmonat des Vergütungsplans</span><span class="sxs-lookup"><span data-stu-id="7f29b-138">Plan start month</span></span> | <span data-ttu-id="7f29b-139">Wählen Sie den Kalendermonat aus, an dem Ihr Vorteilsplan beginnt.</span><span class="sxs-lookup"><span data-stu-id="7f29b-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="7f29b-140">Gruppe gültig ab</span><span class="sxs-lookup"><span data-stu-id="7f29b-140">Group valid from</span></span> | <span data-ttu-id="7f29b-141">Das erste Datum, an dem dieser Datensatz gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7f29b-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="7f29b-142">Gruppe gültig bis</span><span class="sxs-lookup"><span data-stu-id="7f29b-142">Group valid through</span></span> | <span data-ttu-id="7f29b-143">Das letzte Datum, an dem dieser Datensatz gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7f29b-143">The last date when this record is valid.</span></span> <span data-ttu-id="7f29b-144">Wenn es kein Ablaufdatum gibt, geben Sie ein **Niemals** ein.</span><span class="sxs-lookup"><span data-stu-id="7f29b-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Erstellen einer Dispositionssteuerungsgruppe](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="7f29b-146">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="7f29b-147">Einer Affordable Care-Dispositionssteuerungsgruppe mehrere Mitarbeiter zuweisen</span><span class="sxs-lookup"><span data-stu-id="7f29b-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="7f29b-148">Im **Vorteilsverwaltung**-Arbeitsbereich wählen Sie **Affordable Care-Dispositionssteuerungsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="7f29b-149">Wählen Sie die Gruppe aus, der Mitarbeiter zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="7f29b-150">Wählen Sie **Massen-Zuweisung** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-150">Select **Mass assignment**.</span></span>

    ![Auswählen Sie Massen-Zuweisung](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="7f29b-152">Wählen Sie Mitarbeiter in der Liste aus und wählen Sie dann **Zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Zuweisen der ausgewählten Mitarbeiter zu einer Gruppe](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="7f29b-154">Mehrere Versionen von Dispositionsoptionen beibehalten</span><span class="sxs-lookup"><span data-stu-id="7f29b-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="7f29b-155">Sie können mehrere Versionen einer beliebigen Dispositionssteuerungsgruppe beibehalten.</span><span class="sxs-lookup"><span data-stu-id="7f29b-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="7f29b-156">Wenn sich in Ihrer Organisation oder den angebotenen Vorteile etwas ändert, können Sie die Informationen der Gruppe auf dem neuesten Stand halten, ohne eine neue Gruppe erstellen und Mitarbeiter neu zuweisen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="7f29b-157">Nachdem Sie Affordable Care-Dispositionssteuerungsgruppen erstellt haben, können Sie ihnen durch Massen-Zuweisung Mitarbeiter zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="7f29b-158">Sie können Mitarbeiter auch einzeln Gruppen zuordnen und angeben, ob ACA-Informationen verfolgt und gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="7f29b-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="7f29b-159">Wenn Sie keine ACA-Informationen für einen Mitarbeiter verfolgen und melden müssen, können Sie die Option **Disposition melden** auf **Nein** festlegen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="7f29b-160">Beispielsweise haben Sie möglicherweise Teilzeitbeschäftigte, für die keine ACA-Berichterstattung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7f29b-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="7f29b-161">Standardwerte für einen Mitarbeiter überschreiben</span><span class="sxs-lookup"><span data-stu-id="7f29b-161">Override default values for an employee</span></span>

<span data-ttu-id="7f29b-162">Für Mitarbeiter, die einer Affordable Care-Dispositionssteuerungsgruppe zugeordnet sind, können Sie die folgenden Optionen für alle Monate ändern, für die andere Werte erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="7f29b-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="7f29b-163">Abdeckungsangebot</span><span class="sxs-lookup"><span data-stu-id="7f29b-163">Offer of coverage</span></span>
- <span data-ttu-id="7f29b-164">Mitarbeiteranteil an den Kosten</span><span class="sxs-lookup"><span data-stu-id="7f29b-164">Employee share of cost</span></span>
- <span data-ttu-id="7f29b-165">Gültiger Abschnitt 4980H in den Bestimmungen des amerikanischen Handelsministeriums (Safe Harbor)</span><span class="sxs-lookup"><span data-stu-id="7f29b-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="7f29b-166">Für ACA-Berichte aus dem Jahr 2020 müssen Sie auf dem Formular 1095-C sowohl die Postleitzahl der Arbeitsstelle als auch die für Zuhause angeben.</span><span class="sxs-lookup"><span data-stu-id="7f29b-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="7f29b-167">Die Werte werden basierend auf den aktuell aktiven Standorten automatisch eingegeben.</span><span class="sxs-lookup"><span data-stu-id="7f29b-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="7f29b-168">Wenn einer der Standorte während eines Teils des Jahres anders war, müssen Sie den Wert überschreiben.</span><span class="sxs-lookup"><span data-stu-id="7f29b-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="7f29b-169">Das **Postleitzahl**-Feld (Zeile 17) des 1095-C-Berichts wird nur ausgefüllt, wenn der Code **Angebot für Disposition** wie folgt **1L** bis **1Q** enthält:</span><span class="sxs-lookup"><span data-stu-id="7f29b-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="7f29b-170">**1L, 1M oder 1N:** Die Postleitzahl des Hauptwohnsitzes</span><span class="sxs-lookup"><span data-stu-id="7f29b-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="7f29b-171">**1O, 1P, 1Q:** Die Postleitzahl des Hauptarbeitsplatzes</span><span class="sxs-lookup"><span data-stu-id="7f29b-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="7f29b-172">Führen Sie die folgenden Schritte aus, um Ausnahmen für Werte einer Affordable Care-Dispositionssteuerungsgruppe einzugeben.</span><span class="sxs-lookup"><span data-stu-id="7f29b-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="7f29b-173">Wählen Sie im Arbeitsbereich **Personalverwaltung** **Links** und dann **Arbeitskräfte** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="7f29b-174">Wählen Sie den Mitarbeiter in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="7f29b-175">Auf der **Beschäftigung**-Registerkarte im **Mehr Informationen**-Abschnitt wählen Sie **Affordable Care-Dispositionssteuerungsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Optionen für einen Mitarbeiter ändern](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="7f29b-177">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-177">Select **Edit**.</span></span>
5. <span data-ttu-id="7f29b-178">Aktivieren Sie für jeden Monat, für den Änderungen erforderlich sind, das Kontrollkästchen **Standard überschreiben** und ändern Sie die anderen Werte nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7f29b-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Standardwerte überschreiben](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="7f29b-180">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="7f29b-181">Gesundheitsvorsorgedisposition melden</span><span class="sxs-lookup"><span data-stu-id="7f29b-181">Report health care coverage</span></span>

<span data-ttu-id="7f29b-182">Sie müssen alle vom Arbeitgeber unterstützten, selbstversicherten Krankenversicherungen für Vollzeit- und Teilzeitbeschäftigte nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="7f29b-183">Nehmen Sie jeden Mitarbeiter zusammen mit seinen Unterhaltsberechtigten in den 1095-C-Bericht für die Monate auf, in denen er versichert war.</span><span class="sxs-lookup"><span data-stu-id="7f29b-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="7f29b-184">Befolgen Sie diese Schritte, um anzugeben, ob ein Vorteilsplan gemeldet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7f29b-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="7f29b-185">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** die Option **Vorteilspläne** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="7f29b-186">Wählen Sie den zu meldenden Vorteilsplan aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="7f29b-187">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-187">Select **Edit**.</span></span>
4. <span data-ttu-id="7f29b-188">Legen Sie die Option **Gemäß Affordable Care Act gemeldet** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="7f29b-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Melden von Gesundheitsvorsorgeabdeckung](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="7f29b-190">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-190">Select **Save**.</span></span>

<span data-ttu-id="7f29b-191">Wenn ein Mitarbeiter eine Krankenversicherung für einen Unterhaltsberechtigten wählt, wird der Versicherungszeitraum des Unterhaltsberechtigten durch das Datum bestimmt, an dem der Unterhaltsberechtigte registriert oder entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="7f29b-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="7f29b-192">Die Dispositionstermine für Unterhaltsberechtigte werden automatisch auf der Grundlage des Zeitraums berechnet, in dem der Unterhaltsberechtigte während des Registrierungsjahres berechtigt und in einem Plan aktiv war.</span><span class="sxs-lookup"><span data-stu-id="7f29b-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="7f29b-193">1095-B- und 1095-C-Formulare generieren</span><span class="sxs-lookup"><span data-stu-id="7f29b-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="7f29b-194">Sie können ACA-Formulare 1095-B und 1095-C generieren und dann an jeden der Mitarbeiter verteilen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="7f29b-195">Sie können das Formular 1095-C und die entsprechenden 1094-C-Übermittlungsdateien auch elektronisch generieren, um sie an den Internal Revenue Service (IRS) zu senden.</span><span class="sxs-lookup"><span data-stu-id="7f29b-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="7f29b-196">Im Arbeitsbereich **Vorteilsverwaltung** wählen Sie **ACA-Formular 1095-B** oder **ACA-Formular 1095-C**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="7f29b-197">Ändern Sie die Parameter nach Bedarf und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f29b-198">Wenn Sie 1095-C Formulare für mehr als 500 Mitarbeiter drucken, erhalten Sie mehr als eine PDF-Datei.</span><span class="sxs-lookup"><span data-stu-id="7f29b-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="7f29b-199">Wir empfehlen Ihnen, den Wert des Felds **Maximale Dateigröße in Megabyte** auf der Seite **Parameter für die Dokumentenverwaltung** auf **150** zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="7f29b-200">(Um diese Seite schnell zu öffnen, können Sie das Suchfeld in der Navigationsleiste verwenden.)</span><span class="sxs-lookup"><span data-stu-id="7f29b-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Ändern der maximalen Dateigröße](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="7f29b-202">Verwenden Sie das Suchfeld in der Navigationsleiste, um den Status Ihrer Berichte zu überprüfen und anzuzeigen und die Seite **Elektronische Berichterstattung** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Suchen nach der Seite „Elektronische Berichterstattung“](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="7f29b-204">Wählen Sie den anzuzeigenden Bericht aus und wählen Sie dann **Dateien anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-204">Select the report to view, and then select **Show files**.</span></span>

    ![Anzeigen von Dateien](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="7f29b-206">Wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-206">Select **Open**.</span></span>

    ![Öffnen einer Datei](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="7f29b-208">Öffnen Sie in der Benachrichtigungsleiste am unteren Rand des Browserfensters die Zip-Datei und wählen Sie den Bericht aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="7f29b-209">Sie können die PDF-Datei anzeigen oder drucken.</span><span class="sxs-lookup"><span data-stu-id="7f29b-209">You can view or print the PDF file.</span></span>

    ![1095-C-Beispielformular](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="7f29b-211">Informationen zur ACA-Disposition anzeigen</span><span class="sxs-lookup"><span data-stu-id="7f29b-211">View ACA coverage information</span></span>

<span data-ttu-id="7f29b-212">Die Seite **Disposition für Affordable Care Act für Arbeitskraft** zeigt die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="7f29b-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="7f29b-213">Mitarbeiter, die jeder Dispositionssteuerungsgruppe zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="7f29b-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="7f29b-214">Mitarbeiter, die nicht in einen Bericht aufgenommen werden müssen</span><span class="sxs-lookup"><span data-stu-id="7f29b-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="7f29b-215">Nicht zugewiesene Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="7f29b-215">Unassigned employees</span></span>

<span data-ttu-id="7f29b-216">Führen Sie die folgenden Schritte aus, um diese Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f29b-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="7f29b-217">Im **Vorteilsverwaltung**-Arbeitsbereich wählen Sie **Disposition für Affordable Care Act für Arbeitskraft**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="7f29b-218">Wählen Sie im Feld **Gruppenname** eine Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-218">In the **Group name** field, select a group.</span></span>

    ![Anzeigen der ACA-Disposition](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="7f29b-220">Wenn beliebige Standardwerte der Affordable Care-Dispositionssteuerungsgruppe überschrieben wurden, wird ein Sternchen neben dem geänderten Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f29b-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="7f29b-221">Wenn die Werte für alle 12 Monate identisch sind und nicht überschrieben wurden, wird der Wert in der Spalte **Alle 12 Monate** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f29b-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="7f29b-222">Sie können Mitarbeiter anzeigen, die als nicht ACA-meldepflichtig markiert sind und für die kein 1095-C-Formular erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7f29b-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="7f29b-223">Im Feld **Filtern nach** wählen Sie **Nicht ACA-meldepflichtig** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="7f29b-224">Sie können Mitarbeiter anzeigen, die keiner Gruppe oder einer abgelaufenen Gruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7f29b-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="7f29b-225">Im Feld **Filtern nach** wählen Sie **Nicht zugewiesene oder abgelaufene Gruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="7f29b-226">Nach Excel exportieren</span><span class="sxs-lookup"><span data-stu-id="7f29b-226">Export to Excel</span></span>

<span data-ttu-id="7f29b-227">Befolgen Sie diesen Schritten, um eine der Listen nach Microsoft Excel zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="7f29b-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="7f29b-228">Wählen Sie die Schaltfläche **In Microsoft Office öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="7f29b-229">Wählen Sie **Zeitweise HCM-Personalwesentabelle für internen Gebrauch**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="7f29b-230">Wählen Sie **Herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="7f29b-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="7f29b-231">ACA-meldepflichtige Unterhaltsberechtigte anzeigen</span><span class="sxs-lookup"><span data-stu-id="7f29b-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="7f29b-232">Wenn Sie versicherte Personen melden müssen, weil Sie selbstversicherten Versicherungsschutz bieten, können Sie Unterhaltsberechtigte anzeigen, die im Rahmen von Vorteilsplänen versichert sind, die als **ACA-meldepflichtig** gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="7f29b-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="7f29b-233">Wählen Sie im Aktionsbereich **Disposition für Unterhaltsberechtigte anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f29b-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Anzeigen der Disposition für Unterhaltsberechtigte](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="7f29b-235">Dispositionsinformationen für Unterhaltsberechtigte des Mitarbeiters werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f29b-235">Coverage information for the employee's dependents is shown.</span></span>

![Abdeckung für Unterhaltsberechtigte](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="7f29b-237">Auf der Seite werden nur Vorteilspläne angezeigt, die als **ACA-meldepflichtig** gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="7f29b-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>
