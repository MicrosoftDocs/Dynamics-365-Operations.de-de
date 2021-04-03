---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (18. Februar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 18. Februar 2020 neu sind oder geändert wurden.
author: andreabichsel
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66ffd9d0ffcf0e8466be785274ef5fb0fceda7a9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463789"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="4d090-103">Neuerungen oder Änderungen in Dynamics 365 Human Resources (18. Februar 2020)</span><span class="sxs-lookup"><span data-stu-id="4d090-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4d090-104">Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind.</span><span class="sxs-lookup"><span data-stu-id="4d090-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4d090-105">Änderungen gelten für Build-Nummer 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="4d090-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="4d090-106">Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.</span><span class="sxs-lookup"><span data-stu-id="4d090-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="4d090-107">Plattformupdate 32</span><span class="sxs-lookup"><span data-stu-id="4d090-107">Platform update 32</span></span> 

<span data-ttu-id="4d090-108">Plattform-Update 32 ist jetzt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4d090-108">Platform update 32 is now available.</span></span> <span data-ttu-id="4d090-109">Weitere Informationen finden Sie unter [Was ist neu oder geändert in Plattform-Update 32 für Finance and Operations (Februar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="4d090-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="4d090-110">Die Suchwerte werden bei der Änderung der Ansichtsoptionen in rationalisierter Mitarbeiterform gespeichert (383833)</span><span class="sxs-lookup"><span data-stu-id="4d090-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="4d090-111">Das neue Formular **Mitarbeiter** merkt sich jetzt Suchwerte, wenn Sie die Ansichtsoptionen ändern und Änderungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="4d090-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="4d090-112">Vergütungsmanagement-Zusammenfassungskacheln in der Vorschaufunktion leiten in das falsche Formular um (401861)</span><span class="sxs-lookup"><span data-stu-id="4d090-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="4d090-113">Die Kacheln für die Verwaltung der festen und variablen Vergütung zeigen jetzt die richtigen Datensätze im neuen Formular **Arbeiter** an.</span><span class="sxs-lookup"><span data-stu-id="4d090-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="4d090-114">Gilt nur für die rationalisierte Vorschaufunktion für Mitarbeiterformulare.</span><span class="sxs-lookup"><span data-stu-id="4d090-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="4d090-115">Sie können diese Vorschaufunktion unter **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4d090-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="4d090-116">Weitere Informationen finden Sie unter [Funktionsverwaltung](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="4d090-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a><span data-ttu-id="4d090-117">Leeres Statusfeld für einige Abwesenheitsantragssätze in Dataverse (414915)</span><span class="sxs-lookup"><span data-stu-id="4d090-117">Empty Status field for some leave request records in Dataverse (414915)</span></span>

<span data-ttu-id="4d090-118">Diese Änderung korrigiert ein Problem in Dataverse, wenn das Feld **Status** in einem Urlaubsantrag auf **Überprüfung** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4d090-118">This change corrects an issue in Dataverse when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="4d090-119">Die Dataverse spiegelt nun den Status wider.</span><span class="sxs-lookup"><span data-stu-id="4d090-119">Dataverse now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="4d090-120">Qualifikationslückenanalyse nur für zugeordnete Stelle möglich (411390)</span><span class="sxs-lookup"><span data-stu-id="4d090-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="4d090-121">Sie können jetzt eine Analyse der Qualifikationslücke für jede in der Personalabteilung definierte Stelle durchführen.</span><span class="sxs-lookup"><span data-stu-id="4d090-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="4d090-122">Die Systemwährung wird in neuen Umgebungen nicht von Dataverse mit der Personalabteilung synchronisiert (418011)</span><span class="sxs-lookup"><span data-stu-id="4d090-122">System currency doesn't sync from Dataverse to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="4d090-123">Die Systemwährung in Dataverse kann nun mit der Personalabteilung synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d090-123">The system currency in Dataverse can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="4d090-124">Vorschau</span><span class="sxs-lookup"><span data-stu-id="4d090-124">In preview</span></span>

- [<span data-ttu-id="4d090-125">Vorschaufunktionen für Urlaub und Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="4d090-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="4d090-126">Vorschaufunktionen der Leistungsverwaltung</span><span class="sxs-lookup"><span data-stu-id="4d090-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="4d090-127">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="4d090-127">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="4d090-128">Aktualisierte Dataverse-Lösung</span><span class="sxs-lookup"><span data-stu-id="4d090-128">Updated Dataverse solution</span></span>

<span data-ttu-id="4d090-129">Eine neue Dataverse Lösung wird in Kürze mit den folgenden Änderungen verfügbar sein:</span><span class="sxs-lookup"><span data-stu-id="4d090-129">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="4d090-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d090-130">Description</span></span> | <span data-ttu-id="4d090-131">Änderung</span><span class="sxs-lookup"><span data-stu-id="4d090-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="4d090-132">**Stelle/Position** Entitätsänderungen</span><span class="sxs-lookup"><span data-stu-id="4d090-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="4d090-133">**Kompensationsregion** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-133">**Compensation region** added</span></span></br><span data-ttu-id="4d090-134">**Finanzdimensionen** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="4d090-135">**Arbeitskraft** Entitätsänderungen</span><span class="sxs-lookup"><span data-stu-id="4d090-135">**Worker** entity changes</span></span> | <span data-ttu-id="4d090-136">**Namensfolge** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-136">**Name sequence** added</span></span></br><span data-ttu-id="4d090-137">**Arbeitet von zu Hause** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-137">**Works from home** added</span></span></br><span data-ttu-id="4d090-138">**Sprache** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-138">**Language** added</span></span></br><span data-ttu-id="4d090-139">**Dienstalterdatum** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-139">**Seniority date** added</span></span></br><span data-ttu-id="4d090-140">**Jahrestag** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-140">**Anniversary date** added</span></span></br><span data-ttu-id="4d090-141">**Ursprüngliches Einstellungsdatum** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-141">**Original hire date** added</span></span> |
| <span data-ttu-id="4d090-142">**Beschäftigung** Entitätsänderungen</span><span class="sxs-lookup"><span data-stu-id="4d090-142">**Employment** entity changes</span></span> | <span data-ttu-id="4d090-143">**Finanzdimensionen** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-143">**Financial dimensions** added</span></span></br><span data-ttu-id="4d090-144">**Kündigungsgrund** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-144">**Termination reason** added</span></span></br><span data-ttu-id="4d090-145">**Kündigungsdatum** umbenannt von **Übergangsdatum**</span><span class="sxs-lookup"><span data-stu-id="4d090-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="4d090-146">**Probezeitdatum** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-146">**Probation date** added</span></span> |
| <span data-ttu-id="4d090-147">**Arbeitskraftadresse** Entitätsänderungen</span><span class="sxs-lookup"><span data-stu-id="4d090-147">**Worker address** entity changes</span></span> | <span data-ttu-id="4d090-148">**Straße** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-148">**Street address** added</span></span></br><span data-ttu-id="4d090-149">**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="4d090-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="4d090-150">Neue variable Vergütung-Einrichtungsentitäten</span><span class="sxs-lookup"><span data-stu-id="4d090-150">New variable compensation setup entities</span></span> | <span data-ttu-id="4d090-151">**Plantyp für variable Vergütung**</span><span class="sxs-lookup"><span data-stu-id="4d090-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="4d090-152">**Plan für variable Vergütung**</span><span class="sxs-lookup"><span data-stu-id="4d090-152">**Compensation variable plan**</span></span></br><span data-ttu-id="4d090-153">**Übertragungsregeln**</span><span class="sxs-lookup"><span data-stu-id="4d090-153">**Vesting rules**</span></span></br><span data-ttu-id="4d090-154">**Variable Planstufe zur Vergütung**</span><span class="sxs-lookup"><span data-stu-id="4d090-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="4d090-155">Neue **Arbeitskraftkalender-Beschäftigung** Entität</span><span class="sxs-lookup"><span data-stu-id="4d090-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="4d090-156">**Arbeitkraftkalender-Entität** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="4d090-157">Neue **Lohnpositionsdetail** Entität</span><span class="sxs-lookup"><span data-stu-id="4d090-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="4d090-158">**Lohnpositionsdetail** hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4d090-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="4d090-159">Neue **Titel** Entität</span><span class="sxs-lookup"><span data-stu-id="4d090-159">New **Title** entity</span></span> | <span data-ttu-id="4d090-160">**Titel** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4d090-160">**Title** added.</span></span> <span data-ttu-id="4d090-161">Die neue Einheit **Titel** wird in den Synchronisationsprozess zwischen Human Resources und Dataverse einbezogen.</span><span class="sxs-lookup"><span data-stu-id="4d090-161">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="4d090-162">Sie wird nicht zunächst von **Job-Position** oder **Job** Entitäten referenziert.</span><span class="sxs-lookup"><span data-stu-id="4d090-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4d090-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d090-163">See also</span></span>

[<span data-ttu-id="4d090-164">Neuigkeiten oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="4d090-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="4d090-165">Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 </span><span class="sxs-lookup"><span data-stu-id="4d090-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="4d090-166">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="4d090-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="4d090-167">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="4d090-167">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]