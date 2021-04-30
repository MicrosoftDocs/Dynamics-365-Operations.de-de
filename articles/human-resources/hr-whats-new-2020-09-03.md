---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (03. September 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 3. September 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10978d8843e7bce2800d62b63e58152569be9631
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891768"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="01635-103">Neuerungen oder Änderungen in Dynamics 365 Human Resources (3. September 2020)</span><span class="sxs-lookup"><span data-stu-id="01635-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="01635-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="01635-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="01635-105">Änderungen gelten für Build-Nummer 8.1.3504.</span><span class="sxs-lookup"><span data-stu-id="01635-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="01635-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die Supportnummern in Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="01635-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="01635-107">Weitere Informationen zu bevorstehenden Funktionen in Human Resources finden Sie unter [Übersicht über Dynamics 365 Human Resources 2019 Versionswelle 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span><span class="sxs-lookup"><span data-stu-id="01635-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="01635-108">Weitere Informationen zum Aktualisierungsprozess für Human Resources finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="01635-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="01635-109">In dieser Version</span><span class="sxs-lookup"><span data-stu-id="01635-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="01635-110">Neues Raster für Finanzdimensionen und Dialogmuster in der gesamten Personalabteilung (469495)</span><span class="sxs-lookup"><span data-stu-id="01635-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="01635-111">Das neue Muster für Finanzdimensionen ist jetzt in folgenden Bereichen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="01635-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="01635-112">Positionsaktionen (Formular: **HcmPositionActionDetail**)</span><span class="sxs-lookup"><span data-stu-id="01635-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="01635-113">Lohn- und Einkommenscodes (Formular: **PayrollEarningCode**)</span><span class="sxs-lookup"><span data-stu-id="01635-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="01635-114">Einträge werden nicht im Urlaubskalender des Unternehmens angezeigt, wenn die Verbesserungen des Urlaubs- und Abwesenheitskalenders nicht aktiviert sind (484406)</span><span class="sxs-lookup"><span data-stu-id="01635-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="01635-115">Diese Version behebt ein Problem, bei dem Urlaubseinträge nicht im Urlaubskalender des Unternehmens angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="01635-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="01635-116">Dieses Problem tritt nur auf, wenn die Funktionsverwaltungsoption **Verbesserungen des Urlaubs- und Abwesenheitskalenders** nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="01635-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="01635-117">BenefitPlanEmployeeEntity-Problem (467597)</span><span class="sxs-lookup"><span data-stu-id="01635-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="01635-118">Diese Version behebt ein Problem mit der **BenefitsPlanEmployee**-Entität.</span><span class="sxs-lookup"><span data-stu-id="01635-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="01635-119">Beim Importieren von Mitarbeiterbeitritten werden der **Abdeckungscode** und der **Plantypcode** jetzt richtig eingestellt.</span><span class="sxs-lookup"><span data-stu-id="01635-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="01635-120">Dieses Problem führte dazu, dass Mitarbeitervorteilspläne in den Formularen **Arbeitskraft-Vorteilsplan** und **Offene Beitritte** in Self-Service für Mitarbeiter falsch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="01635-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="01635-121">Elektronische Datei 1094-C gibt fehlenden Buchstaben in XML aus (435190)</span><span class="sxs-lookup"><span data-stu-id="01635-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="01635-122">Diese Änderung behebt ein Problem mit der 1094-C-Ausgabedatei, bei der ein Zeichen fehlt, das beim Senden an das IRS benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="01635-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="01635-123">Tabelle mit variablen Vergütungen für Mitarbeiter, die dem Formular für feste Vergütungen zugeordnet ist (476117)</span><span class="sxs-lookup"><span data-stu-id="01635-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="01635-124">Diese Änderung richtet die Felder für feste Vergütung am Formular für feste Vergütung aus.</span><span class="sxs-lookup"><span data-stu-id="01635-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="01635-125">Felder für variable Vergütung sind jetzt nur mit dem Formular für variable Vergütung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="01635-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="01635-126">Urlaubsanträge sind vor der Aufnahme zulässig, wenn dieser Urlaubstyp ein negatives Mindestguthaben aufweist (469917)</span><span class="sxs-lookup"><span data-stu-id="01635-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="01635-127">Diese Änderung verbietet die Eingabe von Urlaubsanträgen vor der Aufnahme in den Plan, selbst wenn die Aufnahme ein negatives Mindestguthaben aufweist.</span><span class="sxs-lookup"><span data-stu-id="01635-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="01635-128">Sie können Anfragen nur eingeben oder einreichen, wenn der Plan aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="01635-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="01635-129">Dokumentvorlagen werden nicht heruntergeladen (457279)</span><span class="sxs-lookup"><span data-stu-id="01635-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="01635-130">Mit dieser Änderung können Sie jetzt alle Dokumentvorlagen herunterladen.</span><span class="sxs-lookup"><span data-stu-id="01635-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="01635-131">Daten werden als Spaltenüberschriften anstelle von Zeilen für das Feld Lohnsatz im Vergütungsplanbericht angezeigt(476077)</span><span class="sxs-lookup"><span data-stu-id="01635-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="01635-132">Der Analysebericht zeigt jetzt die richtigen Informationen für **Lohnsatz** an.</span><span class="sxs-lookup"><span data-stu-id="01635-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="01635-133">Vorschau</span><span class="sxs-lookup"><span data-stu-id="01635-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="01635-134">Human Resources Anwendung in Teams</span><span class="sxs-lookup"><span data-stu-id="01635-134">Human Resources application in Teams</span></span>

<span data-ttu-id="01635-135">Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern.</span><span class="sxs-lookup"><span data-stu-id="01635-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="01635-136">Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="01635-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="01635-137">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="01635-137">For more information, see:</span></span>

- <span data-ttu-id="01635-138">[Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 1</span><span class="sxs-lookup"><span data-stu-id="01635-138">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="01635-139">[Human Resources-App in Teams](./hr-admin-teams-leave-app.md) in der Dokumentation für Human Resources</span><span class="sxs-lookup"><span data-stu-id="01635-139">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="01635-140">Human Resources-App in Teams-Vorschaufunktonen</span><span class="sxs-lookup"><span data-stu-id="01635-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="01635-141">**Benachrichtigungen**: Antragssteller und Genehmigende von Anforderungen arbeitsfreier Zeit werden in der Human Resources-App in Teams benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="01635-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="01635-142">Genehmigende Personen können Freistellungsanträge genehmigen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="01635-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="01635-143">Einreicher werden benachrichtigt, wenn die Anfrage genehmigt oder abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="01635-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="01635-144">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="01635-144">For more information, see:</span></span>
   - <span data-ttu-id="01635-145">[Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 2</span><span class="sxs-lookup"><span data-stu-id="01635-145">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="01635-146">[Aktivieren von Benachrichtigungen für die Human Resources-App in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in der Dokumentation für Human Resources</span><span class="sxs-lookup"><span data-stu-id="01635-146">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="01635-147">[Aktivieren oder Deaktivieren von Team-Benachrichtigungen für einzelne Benutzer](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in der Dokumentation für Human Resources</span><span class="sxs-lookup"><span data-stu-id="01635-147">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="01635-148">[Teams-Benachrichtigungen](./hr-teams-leave-app.md#respond-to-teams-notifications) in der Dokumentation für Human Resources</span><span class="sxs-lookup"><span data-stu-id="01635-148">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="01635-149">[Anzeigen den Urlaubskalenders Ihres Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in der Dokumentation für Human Resources</span><span class="sxs-lookup"><span data-stu-id="01635-149">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="01635-150">**Manager-Kalender für arbeitsfreie Zeit**: Manager können die genehmigte und ausstehende arbeitsfreie Zeit für ihre direkten Berichte in einer Kalenderansicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="01635-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="01635-151">Diese Ansicht bietet ein einfaches Verständnis dafür, wann ihre Teammitglieder nicht arbeiten.</span><span class="sxs-lookup"><span data-stu-id="01635-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="01635-152">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="01635-152">For more information, see:</span></span>
   - <span data-ttu-id="01635-153">[Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 2</span><span class="sxs-lookup"><span data-stu-id="01635-153">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="01635-154">[Anzeigen den Urlaubskalenders Ihres Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in der Dokumentation für Human Resources</span><span class="sxs-lookup"><span data-stu-id="01635-154">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="01635-155">Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente (477004)</span><span class="sxs-lookup"><span data-stu-id="01635-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="01635-156">Eine neue Option ist jetzt verfügbar, um die **Mir zugewiesene Arbeitselemente**-Liste in der rechten Spalte des Dashboards zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="01635-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="01635-157">Mit dieser Änderung werden alle Arbeitselemente und Aufgabenlisten im selben Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="01635-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="01635-158">Aktivieren Sie diese Funktion durch Einschalten von **Vorschau – Verbesserungen der Workflow-Erfahrung** in der Funktionsverwaltung.</span><span class="sxs-lookup"><span data-stu-id="01635-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="01635-159">Weitere Informationen zur Aktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="01635-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="01635-160">Diese Funktion fördert auch die Workflow-Optionen, die in den Formularen für Personalaktionen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="01635-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="01635-161">Workflow-Optionen werden auch über das Aktion-Inforegister für den schnellen Zugriff angezeigt.</span><span class="sxs-lookup"><span data-stu-id="01635-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="01635-162">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="01635-162">For more information, see:</span></span> 

- <span data-ttu-id="01635-163">[Verbesserung der Workflow-Erfahrung in Organisation und Personalverwaltung](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) im Plan der Dynamics 365 2020 Versionswelle 2</span><span class="sxs-lookup"><span data-stu-id="01635-163">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Mir zugewiesene Arbeitsaufgaben](./media/hr-workflow-work-items-assigned-to-me.png)

![Schneller Zugriff auf Workflow-Elemente](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="01635-166">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="01635-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="01635-167">In Dataverse enthaltene Prüflistenentitäten</span><span class="sxs-lookup"><span data-stu-id="01635-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="01635-168">Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Dataverse verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="01635-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="01635-169">Ursachencodes für die Vergütungsverwaltung</span><span class="sxs-lookup"><span data-stu-id="01635-169">Benefits management reason codes</span></span>

<span data-ttu-id="01635-170">Ursachencodes für das Vergütungsverwaltung werden in Kürze mit vorhandenen Ursachencodes in der Human Resources kombiniert.</span><span class="sxs-lookup"><span data-stu-id="01635-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="01635-171">Wenn Sie in der Vergütungsverwaltung Ursachencodes mit mehr als 15 Zeichen erstellt haben, müssen Sie den Namen des Ursachencodes im Vergütungsverwaltungsformular **Ursachencodes** auf maximal 15 Zeichen ändern.</span><span class="sxs-lookup"><span data-stu-id="01635-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="01635-172">Nachdem Sie den Namen aktualisiert haben, wird der Ursachencode unter dem vorhandenen Ursachencodeformular in der Personalverwaltung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="01635-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="01635-173">Diese Änderung wird in Zukunft verfügbar sein und sich nicht auf vorhandene Funktionen auswirken.</span><span class="sxs-lookup"><span data-stu-id="01635-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="01635-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01635-174">See also</span></span>

[<span data-ttu-id="01635-175">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="01635-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="01635-176">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2</span><span class="sxs-lookup"><span data-stu-id="01635-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="01635-177">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="01635-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="01635-178">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="01635-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
