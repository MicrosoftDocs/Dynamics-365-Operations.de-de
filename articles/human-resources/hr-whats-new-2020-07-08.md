---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (08. Juli 2020)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Human Resources entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 7/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8fe7bc33407bd5781d565f854c0f096766da5fc9
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555387"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="ad484-103">Neuerungen und Änderungen in Dynamics 365 Human Resources (8. Juli 2020)</span><span class="sxs-lookup"><span data-stu-id="ad484-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

<span data-ttu-id="ad484-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="ad484-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ad484-105">Änderungen gelten für Build-Nummer 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="ad484-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="ad484-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.</span><span class="sxs-lookup"><span data-stu-id="ad484-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="ad484-107">Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="ad484-107">Database logging</span></span>

<span data-ttu-id="ad484-108">Mit der Datenbankprotokollierung können Sie festlegen, welche Tabellen und Felder überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ad484-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="ad484-109">Außerdem können Sie die Ereignisse bestimmen, die die Änderungsverfolgung auslösen sollen.</span><span class="sxs-lookup"><span data-stu-id="ad484-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="ad484-110">Sie verwenden Datenbankprotokollierungsfunktionen, um diese Änderungen im Laufe der Zeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad484-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="ad484-111">Weitere Informationen finden Sie unter [Konfigurieren und verwalten Sie die Datenbankprotokollierung](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="ad484-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="ad484-112">Name des Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ad484-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="ad484-113">In **Personalverwaltungsparameter** können Sie jetzt den Namen des Arbeitsbereichs **Mitarbeiter-Self-Service** zu **Self-Service** ändern.</span><span class="sxs-lookup"><span data-stu-id="ad484-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="ad484-114">Weitere Informationen finden Sie unter [Mitarbeiter-Self-Service-Arbeitsbereichsname ändern](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="ad484-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="ad484-115">Offener Beitrittszugriff der Vorteilsverwaltung außerhalb des Zeitraums</span><span class="sxs-lookup"><span data-stu-id="ad484-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="ad484-116">Dieses Release behebt einen Fehler, bei dem Mitarbeiter auf Vorteile des offenen Beitritts außerhalb des Beitrittszeitraums zugreifen konnten oder ohne ein Life-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ad484-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="ad484-117">Wenn Sie den offenen Beitritt im Mitarbeiter-Self-Service demonstrieren möchten, müssen Sie die offenen Beitrittsdaten auf heute (oder früher) anpassen, um darauf zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="ad484-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="ad484-118">Sie können diese Einstellung unter **Vorteilsverwaltung > Regeln und Optionszeiträume** ändern.</span><span class="sxs-lookup"><span data-stu-id="ad484-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="ad484-119">Mitarbeiterbeitrittsbestätigung per E-Mail senden</span><span class="sxs-lookup"><span data-stu-id="ad484-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="ad484-120">Sie können jetzt E-Mails an Mitarbeiter senden, nachdem diese ihre Vorteilsauswahl abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="ad484-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="ad484-121">Sie können entweder eine Standardnachricht senden oder eine E-Mail-Vorlage der Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad484-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="ad484-122">Diese Einstellungen finden Sie unter **Personalverwaltungsparameter > Vorteilsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="ad484-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="ad484-123">Die stornierte Abwesenheit wird in der kommenden arbeitsfreien Zeit weiterhin im Arbeitsbereich „Personen“ angezeigt (441358)</span><span class="sxs-lookup"><span data-stu-id="ad484-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="ad484-124">Stornierte Abwesenheit wird nicht mehr als bevorstehende arbeitsfreie Zeit auf den Urlaubskarten im Arbeitsbereich **Personen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad484-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="ad484-125">Die Abteilungsentitätseigenschaft in der Entität „PositionV2“ (456486) kann nicht verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ad484-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="ad484-126">Sie können jetzt eine Abteilung hinzufügen, ohne eine doppelte Relation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad484-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="ad484-127">PayrollWorkerEnrolledBenefitDetailEntity sollte nur das berechnete Feld für Pensionspläne verwenden (459779)</span><span class="sxs-lookup"><span data-stu-id="ad484-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="ad484-128">Beim Exportieren der Entität **PayrollWorkerEnrolledBenefitDetailEntity** bestimmt der Export, ob sie ein berechnetes Feld basierend auf einer Ratentabelle verwenden oder das Feld **ContributionAmountCur** in der Sicherungstabelle verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="ad484-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="ad484-129">Die von der Datenentität verwendete Logik verwendet die Ratentabelle in Situationen, in denen die Anwendung dies normalerweise nicht tut.</span><span class="sxs-lookup"><span data-stu-id="ad484-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="ad484-130">Diese Logik bewirkt, dass die Entitätsexporte einen Nullwert für diese Spalte zurückgeben, da keine Berechnungsratentabelle vorhanden ist und das Produkt dem Kunden nicht erlaubt, eine anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ad484-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="ad484-131">Verwirrende Übersetzungen in tschechischer Sprache in Personalverwaltung und Mitarbeiter-Self-Service (400276)</span><span class="sxs-lookup"><span data-stu-id="ad484-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="ad484-132">Dieses Release korrigiert die Übersetzungen für **Unternehmensverzeichnis**, **Nächster angemeldeter Kurs**, **Stelle** und **Position**.</span><span class="sxs-lookup"><span data-stu-id="ad484-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="ad484-133">In der WorkCalendarEmployment-Tabelle sind die erstellten und geänderten Systemfelder nicht aktiviert (460171)</span><span class="sxs-lookup"><span data-stu-id="ad484-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="ad484-134">Erstellte und geänderte Systemfelder sind jetzt in der Tabelle **WorkCalendarEmployment** in der Personalverwaltung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ad484-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="ad484-135">Nullreferenzausnahme für Einstellung und Details für zukünftigen Mitarbeiter hinzufügen (455475)</span><span class="sxs-lookup"><span data-stu-id="ad484-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="ad484-136">Dieses Release korrigiert einen Fehler (Nullreferenz) in der optimierten Mitarbeitereingabe, wenn Sie einen Mitarbeiter mit der Option zum **Einstellen und Details hinzufügen** einstellen.</span><span class="sxs-lookup"><span data-stu-id="ad484-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="ad484-137">Änderungen in der Common Data Service-Arbeitskraftentität spiegeln sich nicht in der Personalverwaltung wider (455652)</span><span class="sxs-lookup"><span data-stu-id="ad484-137">Changes made in the Common Data Service Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="ad484-138">Änderungen an den folgenden Feldern in der Entität **Arbeitskraft** in Common Data Service werden jetzt in der Personalverwaltung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ad484-138">Changes made to the following fields in the **Worker** entity in Common Data Service will now show up in Human Resources:</span></span>

- <span data-ttu-id="ad484-139">**Arbeitet von zu Hause aus**</span><span class="sxs-lookup"><span data-stu-id="ad484-139">**Works from home**</span></span>
- <span data-ttu-id="ad484-140">**Dienstalterdatum**</span><span class="sxs-lookup"><span data-stu-id="ad484-140">**Seniority date**</span></span>
- <span data-ttu-id="ad484-141">**Jahrestag**</span><span class="sxs-lookup"><span data-stu-id="ad484-141">**Anniversary date**</span></span>
- <span data-ttu-id="ad484-142">**Ursprüngliches Einstellungsdatum**</span><span class="sxs-lookup"><span data-stu-id="ad484-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="ad484-143">Die korrekte Vergütungsstufe basiert nicht standardmäßig auf der Stelle, die der Position zugewiesenen ist (394136)</span><span class="sxs-lookup"><span data-stu-id="ad484-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="ad484-144">Mit dieser Änderung basieren die korrekten Vergütungsstufen-Standardwerte auf den Datensätzen **Datum des Inkrafttretens** für die **Positionsdetails** und das **Startdatum** der **Vergütungsplanzuordnung**.</span><span class="sxs-lookup"><span data-stu-id="ad484-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="ad484-145">Vorschau</span><span class="sxs-lookup"><span data-stu-id="ad484-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="ad484-146">Pflichtfelder</span><span class="sxs-lookup"><span data-stu-id="ad484-146">Mandatory fields</span></span> 

<span data-ttu-id="ad484-147">Mithilfe der Personalisierungsfunktionen für die Personalabteilung können Sie Felder jetzt zu Pflichtfeldern machen.</span><span class="sxs-lookup"><span data-stu-id="ad484-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="ad484-148">Diese Funktion erfordert **Gespeicherte Ansichten**.</span><span class="sxs-lookup"><span data-stu-id="ad484-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="ad484-149">Human Resources Anwendung in Teams</span><span class="sxs-lookup"><span data-stu-id="ad484-149">Human Resources application in Teams</span></span>

<span data-ttu-id="ad484-150">Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern.</span><span class="sxs-lookup"><span data-stu-id="ad484-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="ad484-151">Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad484-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="ad484-152">Weitere Informationen finden Sie unter [Human Resources App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="ad484-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="ad484-153">Data Management Framework (DMF) Entitäten für das Leistungsmanagement</span><span class="sxs-lookup"><span data-stu-id="ad484-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="ad484-154">Leistungsverwaltungsentitäten geben frei.</span><span class="sxs-lookup"><span data-stu-id="ad484-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="ad484-155">Mit DMF-Entitäten können Daten importiert und exportiert werden, um so das Leistungsmanagement einfach zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ad484-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="ad484-156">Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement bereit.</span><span class="sxs-lookup"><span data-stu-id="ad484-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="ad484-157">Die Vorlage exportiert und importiert die Daten nacheinander, um die Datenabhängigkeiten zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="ad484-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="ad484-158">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="ad484-158">Buy and sell leave</span></span> 

<span data-ttu-id="ad484-159">Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können.</span><span class="sxs-lookup"><span data-stu-id="ad484-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="ad484-160">Dieser Prozess wird häufig manuell verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ad484-160">This process is often managed manually.</span></span> <span data-ttu-id="ad484-161">Diese Funktion automatisiert die Verwaltung von Richtlinien und Anforderungen für die Personalabteilung.</span><span class="sxs-lookup"><span data-stu-id="ad484-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="ad484-162">Es rationalisiert den Urlaubsmanagementprozess und hilft, Fehler zu beseitigen.</span><span class="sxs-lookup"><span data-stu-id="ad484-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="ad484-163">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="ad484-163">For more information, see:</span></span>

- [<span data-ttu-id="ad484-164">Kauf- und Verkaufsurlaubsrichtlinien verwalten</span><span class="sxs-lookup"><span data-stu-id="ad484-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="ad484-165">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="ad484-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="ad484-166">Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan</span><span class="sxs-lookup"><span data-stu-id="ad484-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="ad484-167">Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ad484-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="ad484-168">Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Urlaubsfälligkeitsrichtlinien Klarheit für den Fälligkeitsprozess.</span><span class="sxs-lookup"><span data-stu-id="ad484-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="ad484-169">Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="ad484-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="ad484-170">Anhänge zu Abwesenheitsfragen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ad484-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="ad484-171">Die Möglichkeit, genehmigten Urlaubsanträgen Anhänge hinzuzufügen, ist in der aktuellen COVID-19-Umgebung von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ad484-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="ad484-172">Mitarbeiter können diese Anhänge jetzt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad484-172">Employees can now add these attachments.</span></span> <span data-ttu-id="ad484-173">Sie haben auch mehr Einblick, wie Aktualisierungen vorgenommen werden, um Anfragen zu hinterlassen.</span><span class="sxs-lookup"><span data-stu-id="ad484-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="ad484-174">Weitere Informationen finden Sie unter [Fügen Sie einer vorhandenen Anforderung einen Anhang hinzu](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="ad484-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="ad484-175">Ursachencode für Ansammlungsaussetzungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ad484-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="ad484-176">Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="ad484-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="ad484-177">Vortragungsregeln</span><span class="sxs-lookup"><span data-stu-id="ad484-177">Carry forward rules</span></span> 

<span data-ttu-id="ad484-178">Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="ad484-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="ad484-179">Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="ad484-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="ad484-180">Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="ad484-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="ad484-181">Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen</span><span class="sxs-lookup"><span data-stu-id="ad484-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="ad484-182">Sie können eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="ad484-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="ad484-183">Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein.</span><span class="sxs-lookup"><span data-stu-id="ad484-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="ad484-184">Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.</span><span class="sxs-lookup"><span data-stu-id="ad484-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="ad484-185">DMF-Entität verfügbar für Ansammlungsaussetzungen</span><span class="sxs-lookup"><span data-stu-id="ad484-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="ad484-186">Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.</span><span class="sxs-lookup"><span data-stu-id="ad484-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="ad484-187">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="ad484-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="ad484-188">In Common Data Service enthaltene Prüflistenentitäten</span><span class="sxs-lookup"><span data-stu-id="ad484-188">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="ad484-189">Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Common Data Service verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ad484-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad484-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad484-190">See also</span></span>

[<span data-ttu-id="ad484-191">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="ad484-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="ad484-192">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 </span><span class="sxs-lookup"><span data-stu-id="ad484-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="ad484-193">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="ad484-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="ad484-194">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="ad484-194">Manage features</span></span>](hr-admin-manage-features.md)
