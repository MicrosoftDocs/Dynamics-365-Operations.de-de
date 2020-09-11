---
title: Neuigkeiten oder Änderungen in Dynamics 365 Human Resources (13. April, 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 13. April 2020 neu sind oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 729490e7516d8c7aef7232c9f5c227d3207dcd68
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712423"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="90e11-103">Neuigkeiten oder Änderungen in Dynamics 365 Human Resources (13. April, 2020)</span><span class="sxs-lookup"><span data-stu-id="90e11-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

<span data-ttu-id="90e11-104">Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind.</span><span class="sxs-lookup"><span data-stu-id="90e11-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="90e11-105">Änderungen gelten für Build-Nummer 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="90e11-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="90e11-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.</span><span class="sxs-lookup"><span data-stu-id="90e11-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="90e11-107">Neue Trittfrequenz für Produktionsfreigaben</span><span class="sxs-lookup"><span data-stu-id="90e11-107">New production release cadence</span></span>

<span data-ttu-id="90e11-108">Mit dem Release von dieser Woche wird die Veröffentlichungskadenz für die Personalabteilung von einem wöchentlichen Update auf ein zweiwöchentliches Update umgestellt.</span><span class="sxs-lookup"><span data-stu-id="90e11-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="90e11-109">Um die Angleichung an sichere Bereitstellungspraktiken sicherzustellen und hohe Standards für Stabilität und Zuverlässigkeit des Dienstes aufrechtzuerhalten, dauert die Bereitstellung von Dienstaktualisierungen für alle Regionen jetzt zwei Wochen.</span><span class="sxs-lookup"><span data-stu-id="90e11-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="90e11-110">Wir führen zusätzliche Tests und Überwachungen ein, um die erfolgreiche Bereitstellung in jeder Phase des Prozesses zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="90e11-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="90e11-111">Weitere Informationen zu der Veröffentlichungshäufigkeit finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="90e11-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="90e11-112">Das Rundungsgenauigkeitsfeld kann nach Angabe eines Rundungstyps (435616) nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="90e11-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="90e11-113">Mit dieser Änderung wird das Feld **Rundungsgenauigkeit** jetzt verfügbar gemacht, nachdem Sie das Feld **Rundungsart** aktualisiert haben</span><span class="sxs-lookup"><span data-stu-id="90e11-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="90e11-114">Das Enddatum der Urlaubsregistrierung kann nicht bearbeitet werden, wenn der Urlaubsplan keine Abgrenzungsfristen hat (413628)</span><span class="sxs-lookup"><span data-stu-id="90e11-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="90e11-115">Sie können jetzt das Enddatum der Registrierung bearbeiten, ohne die Fehlermeldung „Feldabgrenzungsdatum muss ausgefüllt werden“ erhalten.</span><span class="sxs-lookup"><span data-stu-id="90e11-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="90e11-116">Die Beschäftigungseinheit wird nicht mit Common Data Service (430834) synchronisiert</span><span class="sxs-lookup"><span data-stu-id="90e11-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="90e11-117">Diese Änderung behebt ein Problem, mit dem die Beschäftigungsdaten nicht mit Common Data Service synchronisiert wurden nach dem Hinzufügen von finanziellen Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="90e11-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="90e11-118">Entfernen Sie die mehrfachen übergeordneten Zuordnungen für die Entität Arbeitskalender-Zeitintervall (431775)</span><span class="sxs-lookup"><span data-stu-id="90e11-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="90e11-119">Entfernen Sie die mehrfachen übergeordneten Zuordnungen für die Entität **Arbeitskalender-Zeitintervall**.</span><span class="sxs-lookup"><span data-stu-id="90e11-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="90e11-120">Filter mit CAST-Funktion funktioniert nicht bei OData-Aufruf Position Arbeitskraftzuweisungs-Entität (431699)</span><span class="sxs-lookup"><span data-stu-id="90e11-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="90e11-121">Dieses Update enthält eine Änderung, um Filter mit CAST-Funktion in OData für die Entität **Position -Arbeitskraftzuweisung** zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="90e11-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="90e11-122">In Vorschau</span><span class="sxs-lookup"><span data-stu-id="90e11-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="90e11-123">Urlaub aussetzen</span><span class="sxs-lookup"><span data-stu-id="90e11-123">Leave suspension</span></span>

<span data-ttu-id="90e11-124">Sie können Urlaub und Abwesenheit in der Personalabteilung für einen Mitarbeiter aussetzen.</span><span class="sxs-lookup"><span data-stu-id="90e11-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="90e11-125">Durch das Aussetzen des Urlaubs werden die Urlaubsrückstellungen für ausgewählte Urlaubstypen gestoppt.</span><span class="sxs-lookup"><span data-stu-id="90e11-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="90e11-126">Wenn die Aussetzung erfolgt, nachdem eine Rückstellung bearbeitet wurde, führt die Aussetzung des Urlaubs zu einer anteiligen Anpassung des Urlaubssaldos des Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="90e11-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="90e11-127">Weitere Informationen finden Sie unter [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="90e11-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="90e11-128">Vortragungsregeln</span><span class="sxs-lookup"><span data-stu-id="90e11-128">Carry forward rules</span></span>

<span data-ttu-id="90e11-129">Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="90e11-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="90e11-130">Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="90e11-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="90e11-131">Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="90e11-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="90e11-132">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="90e11-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="90e11-133">Anstellungsdetailsentität</span><span class="sxs-lookup"><span data-stu-id="90e11-133">Employment Details entity</span></span>

<span data-ttu-id="90e11-134">Die Entität **Beschäftigungsdetail** wurde mit den folgenden Feldern aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="90e11-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="90e11-135">**PayFrequency**</span><span class="sxs-lookup"><span data-stu-id="90e11-135">**PayFrequency**</span></span>
- <span data-ttu-id="90e11-136">**Employment Category ID**</span><span class="sxs-lookup"><span data-stu-id="90e11-136">**Employment Category ID**</span></span>
- <span data-ttu-id="90e11-137">**Employment Type**</span><span class="sxs-lookup"><span data-stu-id="90e11-137">**Employment Type**</span></span>
- <span data-ttu-id="90e11-138">**EmploymentType ID**</span><span class="sxs-lookup"><span data-stu-id="90e11-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="90e11-139">**Status Beschäftigungsvorteil**</span><span class="sxs-lookup"><span data-stu-id="90e11-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="90e11-140">Die Einrichtungsdaten für diese Felder hängen davon ab, dass das Leistungsmanagement im Arbeitsplatz **Funktionsverwaltung** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="90e11-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="90e11-141">Füllen oder aktualisieren Sie diese Felder nicht in der Entität **Beschäftigungsdetail**, da dies beim Import zu Fehlern führt.</span><span class="sxs-lookup"><span data-stu-id="90e11-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="90e11-142">Die SharePoint-Vorschau funktioniert in einigen Umgebungen nicht.</span><span class="sxs-lookup"><span data-stu-id="90e11-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="90e11-143">Wenn die Dokumentvorschau für in SharePoint gespeicherte Dokumente nicht funktioniert, versuchen Sie das folgende Verfahren:</span><span class="sxs-lookup"><span data-stu-id="90e11-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="90e11-144">Stellen Sie sicher, dass dem Administrator-Benutzerkonto eine E-Mail mit dem Benutzerdatensatz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="90e11-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="90e11-145">Diese Informationen können auf der Seite **Benutzer** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="90e11-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="90e11-146">Wenn E-Mail nicht eingerichtet ist, müssen Sie die E-Mail und den Anbieter mit dem OData-Excel-Add-In hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="90e11-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="90e11-147">Standardmäßig ist die E-Mail-Adresse im Excel-Design nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="90e11-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="90e11-148">Sie müssen das Excel-Design bearbeiten, alle Felder hinzufügen, anwenden und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="90e11-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="90e11-149">Sobald Sie diese Schritte ausgeführt haben, können Sie das Administratorkonto aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="90e11-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="90e11-150">Nachdem dem Administratorkonto ein E-Mail-Konto zugeordnet ist, melden Sie sich mit Administratorrechten bei der Personalabteilung an.</span><span class="sxs-lookup"><span data-stu-id="90e11-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="90e11-151">Greifen Sie auf einen Anhang in SharePoint zu, um die Dokumentvorschau zu starten.</span><span class="sxs-lookup"><span data-stu-id="90e11-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="90e11-152">Melden Sie sich mit einem anderen Benutzerkonto an, das Zugriff auf Anhänge hat, und überprüfen Sie, ob die Vorschau wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="90e11-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="90e11-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90e11-153">See also</span></span>

[<span data-ttu-id="90e11-154">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="90e11-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="90e11-155">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 </span><span class="sxs-lookup"><span data-stu-id="90e11-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="90e11-156">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="90e11-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="90e11-157">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="90e11-157">Manage features</span></span>](hr-admin-manage-features.md)