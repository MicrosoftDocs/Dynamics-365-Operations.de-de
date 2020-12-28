---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (25. Februar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 25. Februar 2020 neu sind oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1302686aeba52de484ad520efe292fafefc39ebf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526809"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="06104-103">Neuerungen oder Änderungen in Dynamics 365 Human Resources (25. Februar 2020)</span><span class="sxs-lookup"><span data-stu-id="06104-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="06104-104">Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind.</span><span class="sxs-lookup"><span data-stu-id="06104-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="06104-105">Änderungen gelten für Build-Nummer 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="06104-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="06104-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.</span><span class="sxs-lookup"><span data-stu-id="06104-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="06104-107">Aktivieren Sie die DMF-Entität (Case Management Navigation and Data Management Framework) (414754)</span><span class="sxs-lookup"><span data-stu-id="06104-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="06104-108">Diese Vorschaufunktion ermöglicht eine zusätzliche Navigation zu Fällen der Fallverwaltung.</span><span class="sxs-lookup"><span data-stu-id="06104-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="06104-109">Sie können diese Vorschaufunktion im Arbeitsbereich **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="06104-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="06104-110">Diese Menüpunkte erscheinen im Arbeitsbereich **Compliance** von Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="06104-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="06104-111">Mit dieser Änderung kann die Personalabteilung auf Folgendes zugreifen:</span><span class="sxs-lookup"><span data-stu-id="06104-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="06104-112">Alle Anfragen</span><span class="sxs-lookup"><span data-stu-id="06104-112">All cases</span></span>
- <span data-ttu-id="06104-113">Meine Anfragen</span><span class="sxs-lookup"><span data-stu-id="06104-113">My cases</span></span>
- <span data-ttu-id="06104-114">Meine offenen Anfragen</span><span class="sxs-lookup"><span data-stu-id="06104-114">My open cases</span></span>
- <span data-ttu-id="06104-115">Meine überfälligen Anfragen</span><span class="sxs-lookup"><span data-stu-id="06104-115">My overdue cases</span></span>
- <span data-ttu-id="06104-116">Per Workflow zugewiesene Anfragen</span><span class="sxs-lookup"><span data-stu-id="06104-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="06104-117">Zusammen mit diesen neuen Ansichten in Fällen, ist die **Falldetail** DMF-Entität ebenfalls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="06104-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="06104-118">Aktivieren Sie Beziehungsdefinitionen in der globalen Adresse bBook (414762)</span><span class="sxs-lookup"><span data-stu-id="06104-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="06104-119">Beziehungen sind jetzt im globalen Adressbuch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="06104-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="06104-120">Vor der Veröffentlichung dieser Woche hat das **Beziehung** Faktenfeld alle systemdefinierten Beziehungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="06104-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="06104-121">Jetzt können Sie diese Beziehungen auf der globalen Adressbuchseite definieren.</span><span class="sxs-lookup"><span data-stu-id="06104-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="06104-122">Eine Position kann entfernt werden, wenn für die Position aktive Vergütungsdatensätze vorhanden sind (414568)</span><span class="sxs-lookup"><span data-stu-id="06104-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="06104-123">Bei dieser Änderung wird eine Warnung angezeigt, wenn Sie versuchen, eine Position zu löschen, und ein Mitarbeiter über einen aktiven Vergütungsdatensatz für dieselbe Position verfügt.</span><span class="sxs-lookup"><span data-stu-id="06104-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="06104-124">In diesem Fall müssen Sie den festen Vergütungsdatensatz des Mitarbeiters aktualisieren, bevor Sie die Position entfernen.</span><span class="sxs-lookup"><span data-stu-id="06104-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="06104-125">Der Workflow zur Leistungsüberprüfung fügt gelegentlich Abmeldungen von Personen hinzu, die nicht Teil des Prozesses sind (414171)</span><span class="sxs-lookup"><span data-stu-id="06104-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="06104-126">Diese Änderung behebt ein Problem, bei dem zusätzliche Abmeldeteilnehmer zur Leistungsüberprüfung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="06104-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="06104-127">Arbeitskraftposition-Zuordnung nicht erstellt in Common Data Service, wenn im Dialogfeld Neuer Mitarbeiter (413479) ausgewählt</span><span class="sxs-lookup"><span data-stu-id="06104-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="06104-128">Diese Änderung behebt ein Problem, wenn ein neuer Mitarbeiter eingestellt und die neue Einstellung einer Position über den Dialog **Neue Arbeitskraft** zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="06104-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="06104-129">Jetzt spiegelt sich die Positionszuweisung in Common Data Service wider.</span><span class="sxs-lookup"><span data-stu-id="06104-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="06104-130">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="06104-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="06104-131">Aktualisierte Common Data Service-Lösung</span><span class="sxs-lookup"><span data-stu-id="06104-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="06104-132">Eine neue Common Data Service Lösung wird in Kürze mit den folgenden Änderungen verfügbar sein:</span><span class="sxs-lookup"><span data-stu-id="06104-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="06104-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06104-133">Description</span></span> | <span data-ttu-id="06104-134">Änderung</span><span class="sxs-lookup"><span data-stu-id="06104-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="06104-135">**Stelle/Position** Entitätsänderungen</span><span class="sxs-lookup"><span data-stu-id="06104-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="06104-136">**Kompensationsregion** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-136">**Compensation region** added</span></span></br><span data-ttu-id="06104-137">**Finanzdimensionen** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="06104-138">**Arbeitskraft** Entitätsänderungen</span><span class="sxs-lookup"><span data-stu-id="06104-138">**Worker** entity changes</span></span> | <span data-ttu-id="06104-139">**Namensfolge** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-139">**Name sequence** added</span></span></br><span data-ttu-id="06104-140">**Arbeitet von zu Hause** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-140">**Works from home** added</span></span></br><span data-ttu-id="06104-141">**Sprache** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-141">**Language** added</span></span></br><span data-ttu-id="06104-142">**Dienstalterdatum** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-142">**Seniority date** added</span></span></br><span data-ttu-id="06104-143">**Jahrestag** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-143">**Anniversary date** added</span></span></br><span data-ttu-id="06104-144">**Ursprüngliches Einstellungsdatum** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-144">**Original hire date** added</span></span> |
| <span data-ttu-id="06104-145">**Beschäftigung** Entitätsänderungen</span><span class="sxs-lookup"><span data-stu-id="06104-145">**Employment** entity changes</span></span> | <span data-ttu-id="06104-146">**Finanzdimensionen** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-146">**Financial dimensions** added</span></span></br><span data-ttu-id="06104-147">**Kündigungsgrund** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-147">**Termination reason** added</span></span></br><span data-ttu-id="06104-148">**Kündigungsdatum** umbenannt von **Übergangsdatum**</span><span class="sxs-lookup"><span data-stu-id="06104-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="06104-149">**Probezeitdatum** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-149">**Probation date** added</span></span> |
| <span data-ttu-id="06104-150">**Arbeitskraftadresse** Entitätsänderungen</span><span class="sxs-lookup"><span data-stu-id="06104-150">**Worker address** entity changes</span></span> | <span data-ttu-id="06104-151">**Straße** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-151">**Street address** added</span></span></br><span data-ttu-id="06104-152">**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="06104-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="06104-153">Neue variable Vergütung-Einrichtungsentitäten</span><span class="sxs-lookup"><span data-stu-id="06104-153">New variable compensation setup entities</span></span> | <span data-ttu-id="06104-154">**Plantyp für variable Vergütung**</span><span class="sxs-lookup"><span data-stu-id="06104-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="06104-155">**Plan für variable Vergütung**</span><span class="sxs-lookup"><span data-stu-id="06104-155">**Compensation variable plan**</span></span></br><span data-ttu-id="06104-156">**Übertragungsregeln**</span><span class="sxs-lookup"><span data-stu-id="06104-156">**Vesting rules**</span></span></br><span data-ttu-id="06104-157">**Variable Planstufe zur Vergütung**</span><span class="sxs-lookup"><span data-stu-id="06104-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="06104-158">Neue **Arbeitskraftkalender-Beschäftigung** Entität</span><span class="sxs-lookup"><span data-stu-id="06104-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="06104-159">**Arbeitkraftkalender-Entität** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="06104-160">Neue **Lohnpositionsdetail** Entität</span><span class="sxs-lookup"><span data-stu-id="06104-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="06104-161">**Lohnpositionsdetail** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="06104-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="06104-162">Neue **Titel** Entität</span><span class="sxs-lookup"><span data-stu-id="06104-162">New **Title** entity</span></span> | <span data-ttu-id="06104-163">**Titel** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="06104-163">**Title** added.</span></span> <span data-ttu-id="06104-164">Die neue Einheit **Titel** wird in den Synchronisationsprozess zwischen Human Resources und Common Data Service einbezogen.</span><span class="sxs-lookup"><span data-stu-id="06104-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="06104-165">Sie wird nicht zunächst von **Job-Position** oder **Job** Entitäten referenziert.</span><span class="sxs-lookup"><span data-stu-id="06104-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="06104-166">In den nächsten Wochen werden diese Entitätsänderungen in allen Umgebungen verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="06104-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="06104-167">So installieren Sie die neueste Common Data Service Lösung für Human Resources manuell:</span><span class="sxs-lookup"><span data-stu-id="06104-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="06104-168">Gehen Sie zum [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="06104-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="06104-169">Wählen Sie **Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="06104-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="06104-170">Suchen Sie die Umgebung, die Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="06104-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="06104-171">Dies sollte dem **Umgebungsname** im Abschnitt **Common Data Service Information** im Formular **Über** in Human Resources entsprechen.</span><span class="sxs-lookup"><span data-stu-id="06104-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="06104-172">Wählen Sie die Umgebung aus, um die Umgebungsdetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="06104-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="06104-173">Wählen Sie auf der Aktivitätsleiste oben **Lösungen verwalten**.</span><span class="sxs-lookup"><span data-stu-id="06104-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="06104-174">Ein neues Browserfenster wird geöffnet und navigiert zu **Dynamics 365 Admin Center** im Kontext Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="06104-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="06104-175">Wählen Sie in der Liste **Lösung** den Eintrag **Dynamics 365 Human Resources Anker**.</span><span class="sxs-lookup"><span data-stu-id="06104-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="06104-176">Wählen Sie **Aktualisierung**, um die neueste Lösung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="06104-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="06104-177">Vorschau</span><span class="sxs-lookup"><span data-stu-id="06104-177">In preview</span></span>

<span data-ttu-id="06104-178">Die folgenden Vorschaufunktionen wird am 3. Februar 2020 verfügbar:</span><span class="sxs-lookup"><span data-stu-id="06104-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="06104-179">**Urlaubs- und Abwesenheitsfunktion** - Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsverwaltung, Vorschaufunktion](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="06104-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="06104-180">**Vorschaufunktion für das Leistungsmanagement** – Weitere Informationen, einschließlich bekannter Probleme, finden Sie unter [Übersicht über das Leistungsmanagement](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="06104-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="06104-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06104-181">See also</span></span>

[<span data-ttu-id="06104-182">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="06104-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="06104-183">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 </span><span class="sxs-lookup"><span data-stu-id="06104-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="06104-184">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="06104-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="06104-185">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="06104-185">Manage features</span></span>](hr-admin-manage-features.md)