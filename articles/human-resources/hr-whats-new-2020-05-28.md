---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (28. Mai 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 28. Mai 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79026c6047f3a10366ef3b22d74caee13b371b66
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891960"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="de5a1-103">Neuerungen oder Änderungen in Dynamics 365 Human Resources (28. Mai 2020)</span><span class="sxs-lookup"><span data-stu-id="de5a1-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="de5a1-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="de5a1-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="de5a1-105">Änderungen gelten für Build-Nummer 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="de5a1-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="de5a1-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.</span><span class="sxs-lookup"><span data-stu-id="de5a1-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="de5a1-107">Die LeaveRequest-Entität funktioniert nicht, wenn Sie mehrere Typen pro Urlaubsplan aktivieren (447498)</span><span class="sxs-lookup"><span data-stu-id="de5a1-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="de5a1-108">Mit dieser Änderung ist die **LeaveEnrollmentV2Entity** verfügbar, um den Fehler zu korrigieren, der auftritt, wenn Sie mehrere Urlaubstypen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="de5a1-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="de5a1-109">Funktion zur Reduzierung von Stapelkonflikten (Vorschau) (446619)</span><span class="sxs-lookup"><span data-stu-id="de5a1-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="de5a1-110">Wenn Sie diese Funktion aktivieren, können Sie eine Verringerung der Blockierung von Batch-Framework-Tabellen erwarten, während Sie Aufgaben auswählen und Jobs beenden.</span><span class="sxs-lookup"><span data-stu-id="de5a1-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="de5a1-111">UpdateConflict beim Speichern der Arbeitskraft verhindert das Bearbeiten eines Datensatzes in People (427915)</span><span class="sxs-lookup"><span data-stu-id="de5a1-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="de5a1-112">Diese Änderung behebt einen Fehler beim Hinzufügen einer neuen Arbeitskraft beim Aktualisieren der Adressinformationen und beim Ändern der Spracheinstellungen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="de5a1-113">In diesem einzigartigen Szenario wurde ein Fehler angezeigt, der darauf hinweist, dass der Datensatz nicht aktualisiert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="de5a1-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="de5a1-114">Einer genehmigten Urlaubsanforderung kann kein Anhang hinzugefügt werden und neu eingereicht werden (425407)</span><span class="sxs-lookup"><span data-stu-id="de5a1-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="de5a1-115">Diese Änderung ermöglicht jetzt Anhänge zu genehmigten Urlaubsanträgen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="de5a1-116">Der Benutzer kann eine Vergütung für einen Mitarbeiter in einer anderen juristischen Person eingeben (409529)</span><span class="sxs-lookup"><span data-stu-id="de5a1-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="de5a1-117">Diese Änderung deaktiviert die Vergütungsoptionen, um die versehentliche Eingabe von Vergütungsdatensätzen für die falsche juristische Person zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="de5a1-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="de5a1-118">Fehler beim Übertragen eines Mitarbeiters und das Datum der Zuweisung der Mitarbeiterposition liegt vor der Positionsdauer (429402)</span><span class="sxs-lookup"><span data-stu-id="de5a1-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="de5a1-119">Fehlermeldungen beim Übertragen eines Mitarbeiters in diesem Szenario wurden aktualisiert, um die zur Behebung des Problems erforderlichen Änderungen besser zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="de5a1-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="de5a1-120">Funktionen für Anhänge in der Registrierung für Self-Service-Vorteile für Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="de5a1-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="de5a1-121">Jetzt können Sie während des Leistungsregistrierungsprozesses Anhänge für jeden Plan hinzufügen, für den sich der Mitarbeiter anmeldet.</span><span class="sxs-lookup"><span data-stu-id="de5a1-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="de5a1-122">Sie können dann die Anhänge in Formular **Von der Arbeitskraft angeforderte Leistungen**.</span><span class="sxs-lookup"><span data-stu-id="de5a1-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="de5a1-123">Vorschau</span><span class="sxs-lookup"><span data-stu-id="de5a1-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="de5a1-124">Human Resources Anwendung in Teams</span><span class="sxs-lookup"><span data-stu-id="de5a1-124">Human Resources application in Teams</span></span>

<span data-ttu-id="de5a1-125">Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern.</span><span class="sxs-lookup"><span data-stu-id="de5a1-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="de5a1-126">Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="de5a1-127">Weitere Informationen finden Sie unter [Human Resources App in Teams](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="de5a1-127">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="de5a1-128">Urlaub aussetzen</span><span class="sxs-lookup"><span data-stu-id="de5a1-128">Leave suspension</span></span>

<span data-ttu-id="de5a1-129">Sie können Urlaub und Abwesenheit in der Personalabteilung für einen Mitarbeiter aussetzen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="de5a1-130">Durch das Aussetzen des Urlaubs werden die Urlaubsrückstellungen für ausgewählte Urlaubstypen gestoppt.</span><span class="sxs-lookup"><span data-stu-id="de5a1-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="de5a1-131">Wenn die Aussetzung erfolgt, nachdem eine Rückstellung bearbeitet wurde, führt die Aussetzung des Urlaubs zu einer anteiligen Anpassung des Urlaubssaldos des Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="de5a1-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="de5a1-132">Weitere Informationen finden Sie unter [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="de5a1-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="de5a1-133">Update der Benutzererfahrung, um anzuzeigen, dass die Ansammlung ausgesetzt ist (429550)</span><span class="sxs-lookup"><span data-stu-id="de5a1-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="de5a1-134">Die Benutzererfahrung zeigt nun an, dass das Ansammlung für einen Plan ausgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="de5a1-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="de5a1-135">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="de5a1-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="de5a1-136">Datenbankprotokollierung (in der Vorschau im Juni)</span><span class="sxs-lookup"><span data-stu-id="de5a1-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="de5a1-137">Mit der Datenbankprotokollierungsfunktion können Sie festlegen, welche Tabelle und Felder überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="de5a1-138">Außerdem können Sie die Ereignisse bestimmen, die die Änderungsverfolgung auslösen sollen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="de5a1-139">Es stehen Abfragefunktionen zur Verfügung, um diese Änderungen im Laufe der Zeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="de5a1-140">Kauf und Verkauf von Urlaub (in der Vorschau am 1. Juni)</span><span class="sxs-lookup"><span data-stu-id="de5a1-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="de5a1-141">Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können.</span><span class="sxs-lookup"><span data-stu-id="de5a1-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="de5a1-142">Dieser Prozess wird häufig manuell verwaltet.</span><span class="sxs-lookup"><span data-stu-id="de5a1-142">This process is often managed manually.</span></span> <span data-ttu-id="de5a1-143">Diese Funktion bietet eine automatisiertere Möglichkeit zur Verwaltung von Richtlinien und Anforderungen für die Personalabteilung und hilft, Fehler zu vermeiden und gleichzeitig den Urlaubsverwaltungsprozess zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="de5a1-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="de5a1-144">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="de5a1-144">For more information, see:</span></span>

- [<span data-ttu-id="de5a1-145">Kauf- und Verkaufsurlaubsrichtlinien verwalten</span><span class="sxs-lookup"><span data-stu-id="de5a1-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="de5a1-146">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="de5a1-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="de5a1-147">Data Management Framework (DMF) Entitäten für das Leistungsmanagement</span><span class="sxs-lookup"><span data-stu-id="de5a1-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="de5a1-148">Leistungsverwaltungsentitäten geben frei.</span><span class="sxs-lookup"><span data-stu-id="de5a1-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="de5a1-149">Mit DMF-Entitäten können Daten importiert und exportiert werden, um das Leistungsmanagement einfach zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="de5a1-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="de5a1-150">Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="de5a1-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="de5a1-151">Die Vorlage exportiert und importiert die Daten nacheinander, um Datenabhängigkeiten zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="de5a1-152">Ursachencode für Ansammlungsaussetzungen hinzufügen (1. Juni)</span><span class="sxs-lookup"><span data-stu-id="de5a1-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="de5a1-153">Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="de5a1-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="de5a1-154">Vortragungsregeln (1. Juni)</span><span class="sxs-lookup"><span data-stu-id="de5a1-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="de5a1-155">Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="de5a1-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="de5a1-156">Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="de5a1-157">Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="de5a1-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="de5a1-158">Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen (1. Juni)</span><span class="sxs-lookup"><span data-stu-id="de5a1-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="de5a1-159">In dieser Version kann die Personalverwaltung eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="de5a1-160">Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein.</span><span class="sxs-lookup"><span data-stu-id="de5a1-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="de5a1-161">Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="de5a1-162">DMF-Entität verfügbar für Ansammlungsaussetzungen (1. Juni)</span><span class="sxs-lookup"><span data-stu-id="de5a1-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="de5a1-163">Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.</span><span class="sxs-lookup"><span data-stu-id="de5a1-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="de5a1-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de5a1-164">See also</span></span>

[<span data-ttu-id="de5a1-165">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="de5a1-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="de5a1-166">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 </span><span class="sxs-lookup"><span data-stu-id="de5a1-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="de5a1-167">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="de5a1-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="de5a1-168">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="de5a1-168">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]