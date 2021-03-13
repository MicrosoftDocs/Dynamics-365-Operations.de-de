---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (14. Mai 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 14. Mai 2020 neu sind oder geändert wurden.
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8d65236d316035722451a871afabedc6ab73f7a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127848"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="46118-103">Neuerungen oder Änderungen in Dynamics 365 Human Resources (14. Mai 2020)</span><span class="sxs-lookup"><span data-stu-id="46118-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="46118-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="46118-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="46118-105">Änderungen gelten für Build-Nummer 8.1.3244.</span><span class="sxs-lookup"><span data-stu-id="46118-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="46118-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die Supportnummern in Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="46118-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="46118-107">Plattformänderungen</span><span class="sxs-lookup"><span data-stu-id="46118-107">Platform changes</span></span>

<span data-ttu-id="46118-108">Plattformänderungen sind in der Version dieser Woche enthalten.</span><span class="sxs-lookup"><span data-stu-id="46118-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="46118-109">Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.10 von Finance and Operations Apps (Mai 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span><span class="sxs-lookup"><span data-stu-id="46118-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span></span> <span data-ttu-id="46118-110">Diese Version enthält Fehlerkorrekturen und Änderungen an gespeicherten Ansichten.</span><span class="sxs-lookup"><span data-stu-id="46118-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="46118-111">Sicherstellen, dass Dataverse-Auswahllisten mit den Urlaubsaufzählungen (436343) übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="46118-111">Ensure Dataverse picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="46118-112">Dataverse-Auswahllisten sind nun mit den Urlaubsaufzählungen konsistent.</span><span class="sxs-lookup"><span data-stu-id="46118-112">Dataverse picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="46118-113">Benutzern das Konfigurieren des Urlaubsanforderungsworkflows basierend auf dem Anforderungsbetrag erlauben (300044)</span><span class="sxs-lookup"><span data-stu-id="46118-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="46118-114">Benutzer können Urlaubsanforderungsworkflows basierend auf Anforderungsbeträgen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="46118-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="46118-115">Neues Arbeitskraftformular stellt Daten über das Menü „Ansicht“ bereit, wenn die erweiterte Sicherheit aktiviert ist (403185)</span><span class="sxs-lookup"><span data-stu-id="46118-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="46118-116">In dieser Version ist die Anzeige von Mitarbeitern für verschiedene juristische Personen korrigiert, wenn der erweiterte Zugriff aktiviert ist und auf Arbeitskräfte in anderen Unternehmen zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="46118-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="46118-117">Ausführung von Urlaubsrückstellungen für einen einzelnen Plan oder ein einzelnes Unternehmen zulassen (318844)</span><span class="sxs-lookup"><span data-stu-id="46118-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="46118-118">Mit dieser Änderung können Sie Abgrenzungen für ein Unternehmen oder einen Plan ausführen.</span><span class="sxs-lookup"><span data-stu-id="46118-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="46118-119">Das Vollzeitäquivalent der Position im Formular für registrierte Arbeitskräfte anzeigen (414658)</span><span class="sxs-lookup"><span data-stu-id="46118-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="46118-120">Der Vollzeitäquivalent-Wert der Position einer Arbeitskraft bestimmt den Abgrenzungssatz einer Arbeitskraft, wenn die Option „Vollzeitäquivalent“ für den Urlaubstyp aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="46118-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="46118-121">Dieses Feld ist jetzt im Formular **Registrierte Arbeitskräfte** und im Dialogfeld **Massenregistrierung** enthalten.</span><span class="sxs-lookup"><span data-stu-id="46118-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="46118-122">Stapelverarbeitungsauftrag für Ablauf des Urlaubssaldos hinzufügen (431266)</span><span class="sxs-lookup"><span data-stu-id="46118-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="46118-123">Ein neuer Stapelverarbeitungsauftrag, der täglich ausgeführt wird, ist nun verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46118-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="46118-124">Es verringert den verbleibenden Urlaubssaldo, wenn Ablauftermine aktuell werden.</span><span class="sxs-lookup"><span data-stu-id="46118-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="46118-125">Beim Exportieren persönlicher Kontakte für einen Mitarbeiter mit der Entität „Persönliche Kontaktperson der Arbeitskraft“ kein Export persönlicher Kontakte vom Beziehungstyp „Übergeordnet“ (345893)</span><span class="sxs-lookup"><span data-stu-id="46118-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="46118-126">Die Datenentität **Persönliche Kontaktperson der Arbeitskraft** (**HcmPersonalContactPersonEntity** in DMF und **PersonalContactPerson** in OData) konnte keine persönlichen Kontakte mit dem Beziehungstyp **Übergeordnet** exportieren.</span><span class="sxs-lookup"><span data-stu-id="46118-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="46118-127">Dieses Problem wurde für persönliche Kontakte behoben, die nach dieser Änderung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="46118-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="46118-128">Bestehende persönliche Kontakte vom Typ **Übergeordnet** werden in einer späteren Version behoben.</span><span class="sxs-lookup"><span data-stu-id="46118-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="46118-129">Ursachencodes werden in verschiedenen Szenarien angezeigt, wenn sie als Urlaub und Abwesenheit markiert sind und das optimierte Mitarbeiterformular aktiviert ist (434163).</span><span class="sxs-lookup"><span data-stu-id="46118-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="46118-130">Diese Änderung beschränkt die Ursachencodes ausschließlich auf Urlaubs- und Abwesenheitscodes, wenn Sie die optimierte Eingabe von Mitarbeitern aktivieren.</span><span class="sxs-lookup"><span data-stu-id="46118-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="46118-131">Vorschaufunktion zum Zuweisen eines Urlaubsplans zu Mitarbeitern in der Zukunft zeigt Fehler an (433555)</span><span class="sxs-lookup"><span data-stu-id="46118-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="46118-132">Mit dieser Änderung wird eine Fehlermeldung korrigiert, wenn ein Urlaubsplan zwei Urlaubstypen aufweist und Sie versuchen, einen Mitarbeiter zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="46118-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="46118-133">Banner „Erste Schritte“ wird für alle Benutzer angezeigt (441731)</span><span class="sxs-lookup"><span data-stu-id="46118-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="46118-134">Mit dieser Änderung wird das Banner „Erste Schritte“ für Benutzer ausgeblendet, die keine Systemadministratoren oder Datenverwaltungsadministratoren sind.</span><span class="sxs-lookup"><span data-stu-id="46118-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="46118-135">Die Entität „Arbeitskraftadresse“ von Dataverse funktioniert in Bezug auf Gültigkeitsdatumswerte für Datum/Uhrzeit in Human Resources unterschiedlich (425071)</span><span class="sxs-lookup"><span data-stu-id="46118-135">The Dataverse Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="46118-136">Durch diese Änderung bleiben die Adressinformationen in bestimmten Szenarien basierend auf den Datumsangaben der Adresse ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="46118-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="46118-137">Einer genehmigten Urlaubsanforderung kann kein Anhang hinzugefügt werden (425407)</span><span class="sxs-lookup"><span data-stu-id="46118-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="46118-138">Mit der Veröffentlichung dieser Woche können Sie genehmigten Urlaubsanforderungen Anhänge hinzufügen, ohne die Urlaubsanforderung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="46118-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="46118-139">Vorschau</span><span class="sxs-lookup"><span data-stu-id="46118-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="46118-140">Urlaub aussetzen</span><span class="sxs-lookup"><span data-stu-id="46118-140">Leave suspension</span></span>

<span data-ttu-id="46118-141">Sie können Urlaub und Abwesenheit in der Personalabteilung für einen Mitarbeiter aussetzen.</span><span class="sxs-lookup"><span data-stu-id="46118-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="46118-142">Durch das Aussetzen des Urlaubs werden die Urlaubsrückstellungen für ausgewählte Urlaubstypen gestoppt.</span><span class="sxs-lookup"><span data-stu-id="46118-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="46118-143">Wenn die Aussetzung erfolgt, nachdem eine Rückstellung bearbeitet wurde, führt die Aussetzung des Urlaubs zu einer anteiligen Anpassung des Urlaubssaldos des Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="46118-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="46118-144">Weitere Informationen finden Sie unter [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="46118-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="46118-145">Update der Benutzererfahrung, um anzuzeigen, dass die Ansammlung ausgesetzt ist (429550)</span><span class="sxs-lookup"><span data-stu-id="46118-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="46118-146">Die Benutzererfahrung zeigt nun an, dass das Ansammlung für einen Plan ausgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="46118-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="46118-147">Urlaubsansammlung für angegebene Abwesenheitstypen (272447) aussetzen</span><span class="sxs-lookup"><span data-stu-id="46118-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="46118-148">In dieser Version kann die Personalverwaltung eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="46118-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="46118-149">Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein.</span><span class="sxs-lookup"><span data-stu-id="46118-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="46118-150">Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.</span><span class="sxs-lookup"><span data-stu-id="46118-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="46118-151">DMF-Entität verfügbar für Ansammlungsaussetzungen (429549)</span><span class="sxs-lookup"><span data-stu-id="46118-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="46118-152">Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.</span><span class="sxs-lookup"><span data-stu-id="46118-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="46118-153">Ursachencode für Ansammlungsaussetzungen (429547) hinzufügen</span><span class="sxs-lookup"><span data-stu-id="46118-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="46118-154">Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="46118-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="46118-155">Beginnen Sie mit dem Übergang von Personalverwaltungsparametern zu Urlaubs- und Abwesenheitsparametern</span><span class="sxs-lookup"><span data-stu-id="46118-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="46118-156">In dieser Version wird mit der Kombination von Personalverwaltungsparametern mit Urlaubs- und Abwesenheitsparametern begonnen.</span><span class="sxs-lookup"><span data-stu-id="46118-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="46118-157">Vortragungsregeln</span><span class="sxs-lookup"><span data-stu-id="46118-157">Carry forward rules</span></span>

<span data-ttu-id="46118-158">Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="46118-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="46118-159">Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="46118-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="46118-160">Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="46118-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="46118-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46118-161">See also</span></span>

[<span data-ttu-id="46118-162">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="46118-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="46118-163">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 </span><span class="sxs-lookup"><span data-stu-id="46118-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="46118-164">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="46118-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="46118-165">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="46118-165">Manage features</span></span>](hr-admin-manage-features.md)