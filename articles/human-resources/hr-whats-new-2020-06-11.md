---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (11. Juni 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 11. Juni 2020 neu sind oder geändert wurden.
author: andreabichsel
manager: tfehr
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ff359f65afc03a1b5691fddc078f73682e99e44
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127800"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="8450d-103">Neuerungen und Änderungen in Dynamics 365 Human Resources (11. Juni 2020)</span><span class="sxs-lookup"><span data-stu-id="8450d-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="8450d-104">Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind.</span><span class="sxs-lookup"><span data-stu-id="8450d-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8450d-105">Änderungen gelten für Build-Nummer 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="8450d-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="8450d-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.</span><span class="sxs-lookup"><span data-stu-id="8450d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="8450d-107">Ein optimiertes Mitarbeiterformular führt manchmal dazu, dass die Schaltflächen zum Schließen des untergeordneten Formulars (X) nicht mehr funktionieren (442369)</span><span class="sxs-lookup"><span data-stu-id="8450d-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="8450d-108">Wenn das neue Formular **Arbeitskraft** aktiviert ist, funktioniert die Schaltfläche Schließen (**X**) gelegentlich nicht bei untergeordneten Formularen.</span><span class="sxs-lookup"><span data-stu-id="8450d-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="8450d-109">Dieses Problem trat zeitweise auf.</span><span class="sxs-lookup"><span data-stu-id="8450d-109">This problem was intermittent.</span></span> <span data-ttu-id="8450d-110">Sie können das Formular schließen, nachdem Sie es verlassen und wieder aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="8450d-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="8450d-111">Sie können beispielsweise links einen Menüpunkt auswählen und zurück zum Formular **Arbeitskraft** navigieren und dieses schließen.</span><span class="sxs-lookup"><span data-stu-id="8450d-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="8450d-112">Die Veröffentlichung dieser Woche behebt dieses Problem.</span><span class="sxs-lookup"><span data-stu-id="8450d-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="8450d-113">Die Entität der persönlichen Kontaktperson des Arbeitnehmers exportiert keine persönlichen Kontakte mit einem übergeordneten Beziehungstyp</span><span class="sxs-lookup"><span data-stu-id="8450d-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="8450d-114">Mit dieser Version exportiert die **Persönlicher Ansprechpartner des Arbeitnehmers** alle Beziehungstypen.</span><span class="sxs-lookup"><span data-stu-id="8450d-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="8450d-115">Die HcmPositionWorkerAssignmentV2Entity sollte standardmäßig Teil des Ceridian Payroll-Integrationspakets sein (448506)</span><span class="sxs-lookup"><span data-stu-id="8450d-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="8450d-116">Mit dieser Änderung ist die **HcmPositionWorkerAssignmentV2Entity** im Ceridian Payroll Integration Package enthalten.</span><span class="sxs-lookup"><span data-stu-id="8450d-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="8450d-117">Vorschau</span><span class="sxs-lookup"><span data-stu-id="8450d-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="8450d-118">Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="8450d-118">Database logging</span></span>

<span data-ttu-id="8450d-119">Mit der Datenbankprotokollierungsfunktion können Sie festlegen, welche Tabelle und Felder überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="8450d-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="8450d-120">Außerdem können Sie die Ereignisse bestimmen, die die Änderungsverfolgung auslösen sollen.</span><span class="sxs-lookup"><span data-stu-id="8450d-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="8450d-121">Sie verwenden Datenbankprotokollierungsfunktionen, um diese Änderungen im Laufe der Zeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8450d-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="8450d-122">Weitere Informationen finden Sie unter [Konfigurieren und verwalten Sie die Datenbankprotokollierung](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="8450d-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="8450d-123">Human Resources Anwendung in Teams</span><span class="sxs-lookup"><span data-stu-id="8450d-123">Human Resources application in Teams</span></span>

<span data-ttu-id="8450d-124">Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern.</span><span class="sxs-lookup"><span data-stu-id="8450d-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="8450d-125">Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8450d-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="8450d-126">Weitere Informationen finden Sie unter [Human Resources App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="8450d-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="8450d-127">Data Management Framework (DMF) Entitäten für das Leistungsmanagement</span><span class="sxs-lookup"><span data-stu-id="8450d-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="8450d-128">Leistungsverwaltungsentitäten geben frei.</span><span class="sxs-lookup"><span data-stu-id="8450d-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="8450d-129">Mit DMF-Entitäten können Daten importiert und exportiert werden, um so das Leistungsmanagement einfach zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8450d-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="8450d-130">Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement bereit.</span><span class="sxs-lookup"><span data-stu-id="8450d-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="8450d-131">Die Vorlage exportiert und importiert die Daten nacheinander, um die Datenabhängigkeiten zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="8450d-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="8450d-132">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="8450d-132">Buy and sell leave</span></span> 

<span data-ttu-id="8450d-133">Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können.</span><span class="sxs-lookup"><span data-stu-id="8450d-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="8450d-134">Dieser Prozess wird häufig manuell verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8450d-134">This process is often managed manually.</span></span> <span data-ttu-id="8450d-135">Diese Funktion automatisiert die Verwaltung von Richtlinien und Anforderungen für die Personalabteilung.</span><span class="sxs-lookup"><span data-stu-id="8450d-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="8450d-136">Es rationalisiert den Urlaubsmanagementprozess und hilft, Fehler zu beseitigen.</span><span class="sxs-lookup"><span data-stu-id="8450d-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="8450d-137">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="8450d-137">For more information, see:</span></span>

- [<span data-ttu-id="8450d-138">Kauf- und Verkaufsurlaubsrichtlinien verwalten</span><span class="sxs-lookup"><span data-stu-id="8450d-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="8450d-139">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="8450d-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="8450d-140">Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan</span><span class="sxs-lookup"><span data-stu-id="8450d-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="8450d-141">Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8450d-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="8450d-142">Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Abgrenzungsrichtlinien Klarheit über den Abgrenzungsprozess.</span><span class="sxs-lookup"><span data-stu-id="8450d-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="8450d-143">Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="8450d-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="8450d-144">Fügen Sie Anhänge zu Freizeitanfragen hinzu</span><span class="sxs-lookup"><span data-stu-id="8450d-144">Add attachments to time off requests</span></span>

<span data-ttu-id="8450d-145">Die Möglichkeit, genehmigten Urlaubsanträgen Anhänge hinzuzufügen, ist in der aktuellen COVID-19-Umgebung von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="8450d-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="8450d-146">Mitarbeiter können diese Anhänge jetzt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8450d-146">Employees can now add these attachments.</span></span> <span data-ttu-id="8450d-147">Sie haben auch mehr Einblick, wie Aktualisierungen vorgenommen werden, um Anfragen zu hinterlassen.</span><span class="sxs-lookup"><span data-stu-id="8450d-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="8450d-148">Weitere Informationen finden Sie unter [Fügen Sie einer vorhandenen Anforderung einen Anhang hinzu](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="8450d-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="8450d-149">Ursachencode für Ansammlungsaussetzungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8450d-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="8450d-150">Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="8450d-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="8450d-151">Vortragungsregeln</span><span class="sxs-lookup"><span data-stu-id="8450d-151">Carry forward rules</span></span> 

<span data-ttu-id="8450d-152">Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="8450d-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="8450d-153">Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="8450d-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="8450d-154">Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="8450d-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="8450d-155">Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen</span><span class="sxs-lookup"><span data-stu-id="8450d-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="8450d-156">Sie können eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="8450d-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="8450d-157">Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein.</span><span class="sxs-lookup"><span data-stu-id="8450d-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="8450d-158">Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.</span><span class="sxs-lookup"><span data-stu-id="8450d-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="8450d-159">DMF-Entität verfügbar für Ansammlungsaussetzungen</span><span class="sxs-lookup"><span data-stu-id="8450d-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="8450d-160">Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.</span><span class="sxs-lookup"><span data-stu-id="8450d-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="8450d-161">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="8450d-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="8450d-162">Neue Plattformfunktionen</span><span class="sxs-lookup"><span data-stu-id="8450d-162">New platform capabilities</span></span> 

<span data-ttu-id="8450d-163">Mithilfe der Personalisierung können Sie Felder obligatorisch machen.</span><span class="sxs-lookup"><span data-stu-id="8450d-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="8450d-164">Für diese Funktion müssen Sie **Gespeicherte Ansichten** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8450d-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="8450d-165">Name des Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="8450d-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="8450d-166">In den Human Resources-Parametern ist eine neue Option verfügbar, mit der der Name des Mitarbeiter-Self-Service-Arbeitsbereichs auf Self-Service aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8450d-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="8450d-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8450d-167">See also</span></span>

[<span data-ttu-id="8450d-168">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="8450d-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="8450d-169">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2</span><span class="sxs-lookup"><span data-stu-id="8450d-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="8450d-170">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="8450d-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="8450d-171">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="8450d-171">Manage features</span></span>](hr-admin-manage-features.md)