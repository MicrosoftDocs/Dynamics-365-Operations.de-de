---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (14. Dezember 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/12/2019
ms.locfileid: "949850"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="65dc7-103">Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (14. Dezember 2018)</span><span class="sxs-lookup"><span data-stu-id="65dc7-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65dc7-104">**Build 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="65dc7-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="65dc7-105">In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="65dc7-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="65dc7-106">Änderungen</span><span class="sxs-lookup"><span data-stu-id="65dc7-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="65dc7-107">USA - ACA (Affordable Care Act) Unterstützung für Steuerjahr2018 Formulare 1095-B und 1095-C</span><span class="sxs-lookup"><span data-stu-id="65dc7-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="65dc7-108">Jedes Jahr müssen entsprechende große Arbeitgeber (ALEs) allen Vollzeitmitarbeitern ein 1095-C bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="65dc7-109">Darüber hinaus, muss der Arbeitgeber, wenn er eine eigenversicherte Deckung ereitstellt, das 1095-C (wenn sie ein ALE sind) und das 1095-B (wenn sei ein kleiner Arbeitgeber sind), für alle Voll- und Teilzeitmitarbeiter bereitstellen, di von diesem Gesundheitsplan gedeckt sind.</span><span class="sxs-lookup"><span data-stu-id="65dc7-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="65dc7-110">Diese Funktion bietet druckbare Formulare für das 1095-C und 1095-B.</span><span class="sxs-lookup"><span data-stu-id="65dc7-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="65dc7-111">Beim Import wir das Feld SubmittedByPersonId auf HcmPerfJournalEntity ignoriert</span><span class="sxs-lookup"><span data-stu-id="65dc7-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="65dc7-112">Wenn Leistungsjournaleinträge importiert/exportiert werden, wird das Feld **Übermittelt von** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="65dc7-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="65dc7-113">Mit dieser Änderung bezeichnet der Wert den Wert **Importieren/Exportieren** in der Tabelle beim Export, sofern das System aktualisiert wird mit dem Wert importiert, der in der Importdatei angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="65dc7-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="65dc7-114">Analyseregisterkarte auf dem "Urlaub- und Abwesenheits" Arbeitsbereich zeigt Fehler " OpenConnectionError "für Nicht-System Administratorrollen an</span><span class="sxs-lookup"><span data-stu-id="65dc7-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="65dc7-115">Mit dieser Aktualisierung werden keine Fehler ausgegeben, wenn die Registerkarte **Analyse** auf dem Arbeitsbereich **Ein Sonderurlaub und Abwesenheit** geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="65dc7-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="65dc7-116">Mitarbeiter-Self-Service, Positions-Hierarchie Drop-Down von der Kachel kann übergeordneten Knoten nicht abrufen</span><span class="sxs-lookup"><span data-stu-id="65dc7-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="65dc7-117">Eine Änderung wurde vorgenommen, um den Fehler zu beheben, der den verlassenen übergeordneten Knoten abruft, wenn die Positionshierarchie personalisiert wurde, um auf einem vorhandenen Arbeitsbereich angezeigt zu werden und eine Position in der Hierarchie auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="65dc7-118">Hierbei muss der System-Administrator die Lohnregisterkarte in der Positionsseite sehen</span><span class="sxs-lookup"><span data-stu-id="65dc7-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="65dc7-119">Eine Änderung wurde vorgenommen, um die richtigen Sicherheitselemente im vorhandenen Recht einzubeziehen: "Verwalten von Lohnarbeitskraft und Positionsdetail".</span><span class="sxs-lookup"><span data-stu-id="65dc7-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="65dc7-120">Mit dieser Änderung hat der Lohn-Administrator standardmäßig Zugriff auf Lohnfeldern auf der Positionsseite.</span><span class="sxs-lookup"><span data-stu-id="65dc7-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="65dc7-121">Fehler, wenn Leistungsbeurteilung zum Manager und dem %Reviews.PerfPeriod% Platzhalter übermittelt wird in den Unterordnungsanweisungen</span><span class="sxs-lookup"><span data-stu-id="65dc7-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="65dc7-122">Eine Änderung wird vorgenommen, die den "NULL-Verweis" Fehler behebt, der beim Berechnen des %Reviews.PerfPeriod% Platzhalter in den Unterordnungsanweisungen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="65dc7-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="65dc7-123">Belegschafts-Power BI Bericht zeigt den Fehler, wenn Arbeitskraftdienstalterdatum ein Schalttag ist</span><span class="sxs-lookup"><span data-stu-id="65dc7-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="65dc7-124">Mit dieser Änderung werden Schalttage nun Power BI unterstützt.</span><span class="sxs-lookup"><span data-stu-id="65dc7-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="65dc7-125">Integration zwischen Core HR und Atract</span><span class="sxs-lookup"><span data-stu-id="65dc7-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="65dc7-126">Eine Änderung wird vorgenommen, um die Integration zwischen Core HR und Attract im Bezug zu Kandidaten, die angestellt werden, zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="65dc7-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="65dc7-127">Damit angestellte Kandidaten im **Personalführung** Arbeitsbereich angezeigt werden, werden die folgenden Common Data Service Entitäten verwendet:</span><span class="sxs-lookup"><span data-stu-id="65dc7-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="65dc7-128">StellenBewerbung</span><span class="sxs-lookup"><span data-stu-id="65dc7-128">Job Application</span></span>
- <span data-ttu-id="65dc7-129">Status-Grund muss auf Angebot akzeptiert festgelegt werden </span><span class="sxs-lookup"><span data-stu-id="65dc7-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="65dc7-130">Enthält Kandidaten und Stellenangebot</span><span class="sxs-lookup"><span data-stu-id="65dc7-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="65dc7-131">Kandidat</span><span class="sxs-lookup"><span data-stu-id="65dc7-131">Candidate</span></span>
-   <span data-ttu-id="65dc7-132">Informationen zum Kandidaten</span><span class="sxs-lookup"><span data-stu-id="65dc7-132">Provides Candidate information</span></span>

<span data-ttu-id="65dc7-133">Stellenangebote</span><span class="sxs-lookup"><span data-stu-id="65dc7-133">Job Opening</span></span>
-   <span data-ttu-id="65dc7-134">Enthält Stellenangebot-Kennung und Stellenangebot-Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="65dc7-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="65dc7-135">Stellenangebots-Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="65dc7-135">Job Opening Participants</span></span>
-   <span data-ttu-id="65dc7-136">Vorgesetzte bereitstellen</span><span class="sxs-lookup"><span data-stu-id="65dc7-136">Provides Hiring Manager</span></span>

<span data-ttu-id="65dc7-137">Wenn ein Kandidat zur Personalführung hinzugefügt wird, kann der Kandidat mithilfe eine neue Option nun auch entlassen werden mithilfe der Option auf der Kandidatenkarte.</span><span class="sxs-lookup"><span data-stu-id="65dc7-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="65dc7-138">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="65dc7-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="65dc7-139">Sonderurlaub und Abwesenheit: Zukünftige Urlaub- und Planungsurlaubsalden</span><span class="sxs-lookup"><span data-stu-id="65dc7-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="65dc7-140">Wenn die Änderungen vorgenommen wurden, können Mitarbeiter Freizeit planen und zukünftige Freizeitanforderungen anfragen, ohne dass sich dies auf aktuelle Freizeitbilanz auszuwirkt, da die Darstellung der Freizeit ebenfalls ändert.</span><span class="sxs-lookup"><span data-stu-id="65dc7-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="65dc7-141">Der verfügbare angezeigte Saldo ist der Betrag der verfügbaren Freizeit einschließlich Abgrenzungen von heute und alle genehmigten Urlaubanforderungen zur Endzeit.</span><span class="sxs-lookup"><span data-stu-id="65dc7-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="65dc7-142">Wenn die Möglichkeit zur Planung freigegeben wird, ändert sich der angezeigte Saldo, um den aktuellen Saldo der Freizeit einschließlich Abgrenzungen von heute und Anforderungen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="65dc7-143">Mitarbeiter und Manager finden diese aktualisierten Salden im Mitarbeiter- und Manager-Self-Service im Fenster **Freizeit** und **Freizeitsalden**.</span><span class="sxs-lookup"><span data-stu-id="65dc7-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="65dc7-144">Leiter der Personalabteilung finden diese aktualisierten Salden in **Personen** und unter**Zugeordneten Urlaubpläne** des Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="65dc7-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="65dc7-145">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="65dc7-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="65dc7-146">Prüffehler in der Integration mit Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="65dc7-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="65dc7-147">Die folgenden Probleme wurden für die aktuelle Vorlage für Integrierung von Talent mit Dynamics 365 for Finance and Operations identifiziert.</span><span class="sxs-lookup"><span data-stu-id="65dc7-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="65dc7-148">Eine neue Vorlage wird bald veröffentlicht und für alle neuen Integrationsprojekten angewendet, die erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="65dc7-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="65dc7-149">Für vorhandene Integrationsprojekt können die Aufgabenzuordnungen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="65dc7-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="65dc7-150">Weitere Informationen finden Sie in der aktualisierten Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="65dc7-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="65dc7-151">Die Stellenposition für die übergeordneten Arbeitsaufgabeaufgabenzuweisung integriert keine Daten.</span><span class="sxs-lookup"><span data-stu-id="65dc7-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="65dc7-152">Dies ist ein Problem, das derzeit untersucht wird.</span><span class="sxs-lookup"><span data-stu-id="65dc7-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="65dc7-153">Es gibt keine Problemumgehung in der aktuellen Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="65dc7-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="65dc7-154">Die Abteilung für die Organisationseinheitsaufgabe benötigt die folgenden aktualisierte Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="65dc7-155">Bestehendes Datenquellenfeld</span><span class="sxs-lookup"><span data-stu-id="65dc7-155">Existing source field</span></span>          | <span data-ttu-id="65dc7-156">Neue Quellfeldkennung</span><span class="sxs-lookup"><span data-stu-id="65dc7-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="65dc7-157">cdm_description (Beschreibung)</span><span class="sxs-lookup"><span data-stu-id="65dc7-157">cdm_description (Description)</span></span>  | <span data-ttu-id="65dc7-158">cdm_name (Name)</span><span class="sxs-lookup"><span data-stu-id="65dc7-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="65dc7-159">Ein zusätzliche Zuordnung muss ebenfalls hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="65dc7-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="65dc7-160">Wählen Sie das letzte Feld **Kein** aus, um den anschließenden Zuordnung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="65dc7-161">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="65dc7-161">Source field</span></span>                   | <span data-ttu-id="65dc7-162">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="65dc7-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="65dc7-163">cdm_description (Beschreibung)</span><span class="sxs-lookup"><span data-stu-id="65dc7-163">cdm_description (Description)</span></span>  | <span data-ttu-id="65dc7-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="65dc7-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="65dc7-165">Die aktualisierten Zuordnungen sollten wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-165">The updated mappings should look like the following image.</span></span>

![Abteilungen zur Organisationseinheitsaufgabe](./media/DepartmentMapping.png)


<span data-ttu-id="65dc7-167">Die Aufgaben für die Stellendetailaufgabe benötigt die folgenden aktualisierte Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="65dc7-168">Bestehendes Datenquellenfeld</span><span class="sxs-lookup"><span data-stu-id="65dc7-168">Existing source field</span></span>          | <span data-ttu-id="65dc7-169">Neue Quellfeldkennung</span><span class="sxs-lookup"><span data-stu-id="65dc7-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="65dc7-170">cdm_name (Name)</span><span class="sxs-lookup"><span data-stu-id="65dc7-170">cdm_name (Name)</span></span>                | <span data-ttu-id="65dc7-171">cdm_description (Beschreibung)</span><span class="sxs-lookup"><span data-stu-id="65dc7-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="65dc7-172">cdm_name (Beschreibung)</span><span class="sxs-lookup"><span data-stu-id="65dc7-172">cdm_name (Description)</span></span>         | <span data-ttu-id="65dc7-173">cdm_jobdescription (Stellenbeschreibung)</span><span class="sxs-lookup"><span data-stu-id="65dc7-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="65dc7-174">Die aktualisierten Zuordnungen sollten wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-174">The updated mappings should look like the image below.</span></span>

![Stellen zu Stellendetailaufgaben](./media/JobMapping.png)

<span data-ttu-id="65dc7-176">Die Arbeiter zu Arbeiteraufgaben benötigt die folgenden aktualisierte Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="65dc7-177">Bestehendes Datenquellenfeld</span><span class="sxs-lookup"><span data-stu-id="65dc7-177">Existing source field</span></span>                 | <span data-ttu-id="65dc7-178">Neue Quellfeldkennung</span><span class="sxs-lookup"><span data-stu-id="65dc7-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="65dc7-179">cdm_emailaddress1 (E-Mail Adresse 1)</span><span class="sxs-lookup"><span data-stu-id="65dc7-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="65dc7-180">cdm_primaryemailaddress (Primäre E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="65dc7-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="65dc7-181">cdm_telephone1 (Telefon 1)</span><span class="sxs-lookup"><span data-stu-id="65dc7-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="65dc7-182">cdm_primarytelephone (Primäres Telefon)</span><span class="sxs-lookup"><span data-stu-id="65dc7-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="65dc7-183">Das Geschlechtsfeld muss auch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="65dc7-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="65dc7-184">Wählen Sie den Zuordnungstyp **F-N**(Funktion) für Geschlecht aus und aktualisieren Sie die folgenden Wertzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="65dc7-185">Common Data Service Wert</span><span class="sxs-lookup"><span data-stu-id="65dc7-185">Common Data Service value</span></span>                   | <span data-ttu-id="65dc7-186">Finance and Operations Wert</span><span class="sxs-lookup"><span data-stu-id="65dc7-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="65dc7-187">75440000</span><span class="sxs-lookup"><span data-stu-id="65dc7-187">75440000</span></span>                    | <span data-ttu-id="65dc7-188">Männl.</span><span class="sxs-lookup"><span data-stu-id="65dc7-188">Male</span></span>                                             |
| <span data-ttu-id="65dc7-189">75440001</span><span class="sxs-lookup"><span data-stu-id="65dc7-189">75440001</span></span>                    | <span data-ttu-id="65dc7-190">Weibl.</span><span class="sxs-lookup"><span data-stu-id="65dc7-190">Female</span></span>                                           |
| <span data-ttu-id="65dc7-191">75440002</span><span class="sxs-lookup"><span data-stu-id="65dc7-191">75440002</span></span>                    | <span data-ttu-id="65dc7-192">Keines</span><span class="sxs-lookup"><span data-stu-id="65dc7-192">None</span></span>                                             | 
| <span data-ttu-id="65dc7-193">75440003</span><span class="sxs-lookup"><span data-stu-id="65dc7-193">75440003</span></span>                    | <span data-ttu-id="65dc7-194">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="65dc7-194">NonSpecific</span></span>                                      |

<span data-ttu-id="65dc7-195">Die aktualisierten Zuordnungen sollten wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="65dc7-195">The updated mappings should look like the following images.</span></span>

![Arbeitskräfte einer Arbeitskraftaufgabe zuweisen](./media/WorkerMapping.png)

![Geschlechtsfeld-Umwandlung](./media/WorkerTransform.png)
