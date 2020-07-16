---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (25. Juni 2020)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Human Resources entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 6/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc1931cee0f3da15e07908f221282ad6b57e1681
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500436"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="8af9a-103">Neuerungen und Änderungen in Dynamics 365 Human Resources (23. Juni 2020)</span><span class="sxs-lookup"><span data-stu-id="8af9a-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

<span data-ttu-id="8af9a-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="8af9a-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8af9a-105">Änderungen gelten für Build-Nummer 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="8af9a-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="8af9a-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.</span><span class="sxs-lookup"><span data-stu-id="8af9a-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="8af9a-107">Wenn eine Registrierung für einen gekündigten Mitarbeiter abgelaufen ist, werden Urlaubstyp, Saldo und Betrag im Formular für die Urlaubsregistrierung (444867) gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8af9a-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="8af9a-108">Die Werte unter **Urlaubstyp**, **Saldo** und **Betrag** werden jetzt beibehalten, anstatt bei dieser Auswahl gelöscht zu werden.</span><span class="sxs-lookup"><span data-stu-id="8af9a-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="8af9a-109">Falsch prognostizierter Saldo, wenn die neue Funktion (Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan) aktiviert ist (456553)</span><span class="sxs-lookup"><span data-stu-id="8af9a-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="8af9a-110">Der prognostizierte Saldo wird jetzt korrekt angezeigt, wenn diese Funktion aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="8af9a-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="8af9a-111">Entitäten mit Beziehungen, die zu doppelten Navigationseigenschaften führen (456486)</span><span class="sxs-lookup"><span data-stu-id="8af9a-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="8af9a-112">Diese Version behebt ein Problem mit den Navigationseigenschaften (Beziehungen) mehrerer Entitäten.</span><span class="sxs-lookup"><span data-stu-id="8af9a-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="8af9a-113">Doppelte Beziehungen werden erkannt.</span><span class="sxs-lookup"><span data-stu-id="8af9a-113">Duplicate relations are detected.</span></span> <span data-ttu-id="8af9a-114">Diese Szenarien wurden alle korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8af9a-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="8af9a-115">Unternehmensübergreifende Kommentare zur Leistungsbeurteilung (455536)</span><span class="sxs-lookup"><span data-stu-id="8af9a-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="8af9a-116">Unternehmensübergreifende Kommentare zu Leistungsbeurteilungen sind mit dieser Fehlerkorrektur jetzt sichtbar.</span><span class="sxs-lookup"><span data-stu-id="8af9a-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="8af9a-117">Diese Änderung korrigiert die Ansicht der Kommentare des Prüfers, die in verschiedenen Unternehmen für dieselbe Leistungsbeurteilung eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="8af9a-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="8af9a-118">Inkonsistenz bei der Anzeige von Vergütungsverwaltungsdaten (432562)</span><span class="sxs-lookup"><span data-stu-id="8af9a-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="8af9a-119">Die Self-Service-Übersicht für Manager bietet jetzt eine konsistente Ansicht der Vergütungsdaten.</span><span class="sxs-lookup"><span data-stu-id="8af9a-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="8af9a-120">Abhängig davon, wie Sie zu den **Vergütungsdetails** eines Mitarbeiters navigieren, werden diese den Managern jetzt konsistent angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8af9a-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="8af9a-121">Datum des Inkrafttretens des festen Vergütungsplans ist standardmäßig das heutige Datum (411994)</span><span class="sxs-lookup"><span data-stu-id="8af9a-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="8af9a-122">Das Startdatum der Vergütung basiert nun auf dem Startdatum der Position, die dem Mitarbeiter zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8af9a-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="8af9a-123">„Aktivieren Sie die Halbtagesdefinition“ im Formular für Urlaub und Abwesenheit ist beim Öffnen des Formulars deaktiviert (452607)</span><span class="sxs-lookup"><span data-stu-id="8af9a-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="8af9a-124">Mit dieser Änderung wird **Aktivieren Sie die Halbtagesdefinition** aktiviert, bis neue Urlaubstransaktionen existieren.</span><span class="sxs-lookup"><span data-stu-id="8af9a-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="8af9a-125">Veröffentlichung in HcmDiscussionEntity über Excel nicht möglich; Feldfehler TotalRatingScore (453899)</span><span class="sxs-lookup"><span data-stu-id="8af9a-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="8af9a-126">Sie können das Feld **TotalRatingScore** jetzt mit **HCMDiscussionEntity** im Excel-Arbeitsmappen-Designer aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8af9a-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="8af9a-127">Vorschau</span><span class="sxs-lookup"><span data-stu-id="8af9a-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="8af9a-128">Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="8af9a-128">Database logging</span></span>

<span data-ttu-id="8af9a-129">Mit der Datenbankprotokollierung können Sie festlegen, welche Tabellen und Felder überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="8af9a-130">Außerdem können Sie die Ereignisse bestimmen, die die Änderungsverfolgung auslösen sollen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="8af9a-131">Sie verwenden Datenbankprotokollierungsfunktionen, um diese Änderungen im Laufe der Zeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="8af9a-132">Weitere Informationen finden Sie unter [Konfigurieren und verwalten Sie die Datenbankprotokollierung](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="8af9a-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="8af9a-133">Pflichtfelder</span><span class="sxs-lookup"><span data-stu-id="8af9a-133">Mandatory fields</span></span> 

<span data-ttu-id="8af9a-134">Mithilfe der Personalisierungsfunktionen für die Personalabteilung können Sie Felder jetzt zu Pflichtfeldern machen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="8af9a-135">Diese Funktion erfordert **Gespeicherte Ansichten**.</span><span class="sxs-lookup"><span data-stu-id="8af9a-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="8af9a-136">Human Resources Anwendung in Teams</span><span class="sxs-lookup"><span data-stu-id="8af9a-136">Human Resources application in Teams</span></span>

<span data-ttu-id="8af9a-137">Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern.</span><span class="sxs-lookup"><span data-stu-id="8af9a-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="8af9a-138">Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="8af9a-139">Weitere Informationen finden Sie unter [Human Resources App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="8af9a-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="8af9a-140">Data Management Framework (DMF) Entitäten für das Leistungsmanagement</span><span class="sxs-lookup"><span data-stu-id="8af9a-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="8af9a-141">Leistungsverwaltungsentitäten geben frei.</span><span class="sxs-lookup"><span data-stu-id="8af9a-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="8af9a-142">Mit DMF-Entitäten können Daten importiert und exportiert werden, um so das Leistungsmanagement einfach zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8af9a-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="8af9a-143">Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement bereit.</span><span class="sxs-lookup"><span data-stu-id="8af9a-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="8af9a-144">Die Vorlage exportiert und importiert die Daten nacheinander, um die Datenabhängigkeiten zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="8af9a-145">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="8af9a-145">Buy and sell leave</span></span> 

<span data-ttu-id="8af9a-146">Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können.</span><span class="sxs-lookup"><span data-stu-id="8af9a-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="8af9a-147">Dieser Prozess wird häufig manuell verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8af9a-147">This process is often managed manually.</span></span> <span data-ttu-id="8af9a-148">Diese Funktion automatisiert die Verwaltung von Richtlinien und Anforderungen für die Personalabteilung.</span><span class="sxs-lookup"><span data-stu-id="8af9a-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="8af9a-149">Es rationalisiert den Urlaubsmanagementprozess und hilft, Fehler zu beseitigen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="8af9a-150">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="8af9a-150">For more information, see:</span></span>

- [<span data-ttu-id="8af9a-151">Kauf- und Verkaufsurlaubsrichtlinien verwalten</span><span class="sxs-lookup"><span data-stu-id="8af9a-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="8af9a-152">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="8af9a-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="8af9a-153">Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan</span><span class="sxs-lookup"><span data-stu-id="8af9a-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="8af9a-154">Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8af9a-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="8af9a-155">Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Abgrenzungsrichtlinien Klarheit über den Abgrenzungsprozess.</span><span class="sxs-lookup"><span data-stu-id="8af9a-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="8af9a-156">Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="8af9a-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="8af9a-157">Fügen Sie Anhänge zu Freizeitanfragen hinzu</span><span class="sxs-lookup"><span data-stu-id="8af9a-157">Add attachments to time off requests</span></span>

<span data-ttu-id="8af9a-158">Die Möglichkeit, genehmigten Urlaubsanträgen Anhänge hinzuzufügen, ist in der aktuellen COVID-19-Umgebung von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="8af9a-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="8af9a-159">Mitarbeiter können diese Anhänge jetzt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-159">Employees can now add these attachments.</span></span> <span data-ttu-id="8af9a-160">Sie haben auch mehr Einblick, wie Aktualisierungen vorgenommen werden, um Anfragen zu hinterlassen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="8af9a-161">Weitere Informationen finden Sie unter [Fügen Sie einer vorhandenen Anforderung einen Anhang hinzu](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="8af9a-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="8af9a-162">Ursachencode für Ansammlungsaussetzungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8af9a-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="8af9a-163">Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="8af9a-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="8af9a-164">Vortragungsregeln</span><span class="sxs-lookup"><span data-stu-id="8af9a-164">Carry forward rules</span></span> 

<span data-ttu-id="8af9a-165">Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="8af9a-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="8af9a-166">Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="8af9a-167">Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="8af9a-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="8af9a-168">Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen</span><span class="sxs-lookup"><span data-stu-id="8af9a-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="8af9a-169">Sie können eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="8af9a-170">Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein.</span><span class="sxs-lookup"><span data-stu-id="8af9a-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="8af9a-171">Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="8af9a-172">DMF-Entität verfügbar für Ansammlungsaussetzungen</span><span class="sxs-lookup"><span data-stu-id="8af9a-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="8af9a-173">Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.</span><span class="sxs-lookup"><span data-stu-id="8af9a-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="8af9a-174">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="8af9a-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="8af9a-175">Name des Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="8af9a-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="8af9a-176">Unter **Personalverwaltungsparameter** ist eine neue Option verfügbar, mit der der Name des Mitarbeiter-Self-Service-Arbeitsbereichs auf Self-Service aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8af9a-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="8af9a-177">In Common Data Service enthaltene Prüflistenentitäten</span><span class="sxs-lookup"><span data-stu-id="8af9a-177">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="8af9a-178">Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Common Data Service verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="8af9a-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Common Data Service.</span></span>
