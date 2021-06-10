---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (23. Juli 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 23. Juli 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e48b0694418710322957de811952e12da22b0509
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055388"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="c8828-103">Neuerungen und Änderungen in Dynamics 365 Human Resources (23. Juli 2020)</span><span class="sxs-lookup"><span data-stu-id="c8828-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c8828-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="c8828-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c8828-105">Änderungen gelten für Build-Nummer 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="c8828-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="c8828-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.</span><span class="sxs-lookup"><span data-stu-id="c8828-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="c8828-107">Das Löschen von Finanzdimensionen für eine Position funktioniert nicht wie erwartet (445476)</span><span class="sxs-lookup"><span data-stu-id="c8828-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="c8828-108">Durch das Entfernen von Dimensionen aus einer Position werden jetzt dieselben Positionen aus Dataverse entfernt.</span><span class="sxs-lookup"><span data-stu-id="c8828-108">Removing dimensions from a position now removes those same positions from Dataverse.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="c8828-109">Nicht in der Hierarchie enthaltene Positionen zeigen inaktive Positionen (397257)</span><span class="sxs-lookup"><span data-stu-id="c8828-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="c8828-110">Inaktive Positionen (mit abgelaufener Dauer) werden in der Positionshierarchie nicht mehr als **Positionen nicht in Hierarchie** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8828-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="c8828-111">Die Prüfung zwischen LeaveEnrollmentEntity und HcmWorkerEntity bei Importen im Datenverwaltungsframework (DMF) führt zu langsamen Datenladevorgängen (442324)</span><span class="sxs-lookup"><span data-stu-id="c8828-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="c8828-112">Änderungen in diesem Release erhöhen die Leistung von **LeaveEnrollmentEntity**.</span><span class="sxs-lookup"><span data-stu-id="c8828-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="c8828-113">Personalisierung in der Organisationsverwaltung nicht möglich (447490)</span><span class="sxs-lookup"><span data-stu-id="c8828-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="c8828-114">Mit dieser Änderung können Sie jetzt die Links in der **Organisationsverwaltung** personalisieren.</span><span class="sxs-lookup"><span data-stu-id="c8828-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="c8828-115">Vorschau</span><span class="sxs-lookup"><span data-stu-id="c8828-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="c8828-116">Pflichtfelder</span><span class="sxs-lookup"><span data-stu-id="c8828-116">Mandatory fields</span></span> 

<span data-ttu-id="c8828-117">Mithilfe der Personalisierungsfunktionen für die Personalabteilung können Sie Felder jetzt zu Pflichtfeldern machen.</span><span class="sxs-lookup"><span data-stu-id="c8828-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="c8828-118">Diese Funktion erfordert **Gespeicherte Ansichten**.</span><span class="sxs-lookup"><span data-stu-id="c8828-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="c8828-119">Human Resources Anwendung in Teams</span><span class="sxs-lookup"><span data-stu-id="c8828-119">Human Resources application in Teams</span></span>

<span data-ttu-id="c8828-120">Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern.</span><span class="sxs-lookup"><span data-stu-id="c8828-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="c8828-121">Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c8828-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="c8828-122">Weitere Informationen finden Sie unter [Human Resources App in Teams](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="c8828-122">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="c8828-123">Data Management Framework (DMF) Entitäten für das Leistungsmanagement</span><span class="sxs-lookup"><span data-stu-id="c8828-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="c8828-124">Leistungsverwaltungsentitäten geben frei.</span><span class="sxs-lookup"><span data-stu-id="c8828-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="c8828-125">Mit DMF-Entitäten können Daten importiert und exportiert werden, um so das Leistungsmanagement einfach zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c8828-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="c8828-126">Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement bereit.</span><span class="sxs-lookup"><span data-stu-id="c8828-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="c8828-127">Die Vorlage exportiert und importiert die Daten nacheinander, um die Datenabhängigkeiten zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="c8828-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="c8828-128">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="c8828-128">Buy and sell leave</span></span> 

<span data-ttu-id="c8828-129">Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können.</span><span class="sxs-lookup"><span data-stu-id="c8828-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="c8828-130">Dieser Prozess wird häufig manuell verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c8828-130">This process is often managed manually.</span></span> <span data-ttu-id="c8828-131">Diese Funktion automatisiert die Verwaltung von Richtlinien und Anforderungen für die Personalabteilung.</span><span class="sxs-lookup"><span data-stu-id="c8828-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="c8828-132">Es rationalisiert den Urlaubsmanagementprozess und hilft, Fehler zu beseitigen.</span><span class="sxs-lookup"><span data-stu-id="c8828-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="c8828-133">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="c8828-133">For more information, see:</span></span>

- [<span data-ttu-id="c8828-134">Kauf- und Verkaufsurlaubsrichtlinien verwalten</span><span class="sxs-lookup"><span data-stu-id="c8828-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="c8828-135">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="c8828-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="c8828-136">Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan</span><span class="sxs-lookup"><span data-stu-id="c8828-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="c8828-137">Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c8828-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="c8828-138">Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Urlaubsfälligkeitsrichtlinien Klarheit für den Fälligkeitsprozess.</span><span class="sxs-lookup"><span data-stu-id="c8828-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="c8828-139">Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="c8828-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="c8828-140">Anhänge zu Abwesenheitsfragen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c8828-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="c8828-141">Die Möglichkeit, genehmigten Urlaubsanträgen Anhänge hinzuzufügen, ist in der aktuellen COVID-19-Umgebung von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c8828-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="c8828-142">Mitarbeiter können diese Anhänge jetzt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c8828-142">Employees can now add these attachments.</span></span> <span data-ttu-id="c8828-143">Sie haben auch mehr Einblick, wie Aktualisierungen vorgenommen werden, um Anfragen zu hinterlassen.</span><span class="sxs-lookup"><span data-stu-id="c8828-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="c8828-144">Weitere Informationen finden Sie unter [Fügen Sie einer vorhandenen Anforderung einen Anhang hinzu](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="c8828-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="c8828-145">Ursachencode für Ansammlungsaussetzungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c8828-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="c8828-146">Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c8828-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="c8828-147">Vortragungsregeln</span><span class="sxs-lookup"><span data-stu-id="c8828-147">Carry forward rules</span></span> 

<span data-ttu-id="c8828-148">Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="c8828-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="c8828-149">Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="c8828-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="c8828-150">Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="c8828-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="c8828-151">Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen</span><span class="sxs-lookup"><span data-stu-id="c8828-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="c8828-152">Sie können eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="c8828-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="c8828-153">Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein.</span><span class="sxs-lookup"><span data-stu-id="c8828-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="c8828-154">Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.</span><span class="sxs-lookup"><span data-stu-id="c8828-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="c8828-155">DMF-Entität verfügbar für Ansammlungsaussetzungen</span><span class="sxs-lookup"><span data-stu-id="c8828-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="c8828-156">Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.</span><span class="sxs-lookup"><span data-stu-id="c8828-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c8828-157">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="c8828-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="c8828-158">In Dataverse enthaltene Prüflistenentitäten</span><span class="sxs-lookup"><span data-stu-id="c8828-158">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="c8828-159">Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Dataverse verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c8828-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="c8828-160">Plattformänderungen</span><span class="sxs-lookup"><span data-stu-id="c8828-160">Platform changes</span></span>

<span data-ttu-id="c8828-161">Plattformupdate 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="c8828-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="c8828-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8828-162">See also</span></span>

[<span data-ttu-id="c8828-163">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="c8828-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="c8828-164">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2</span><span class="sxs-lookup"><span data-stu-id="c8828-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="c8828-165">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="c8828-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="c8828-166">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="c8828-166">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]