---
title: "Neuheiten oder Änderungen in Dynamics 365 for Talent Core HR (10. September 2018)"
description: "In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind."
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 7d4a049a44374276655dce696b5bbbe2e6f9fba9
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.contentlocale: de-de
ms.lasthandoff: 09/12/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a><span data-ttu-id="77ab9-103">Neuheiten oder Änderungen in Dynamics 365 for Talent Core HR (10. September 2018)</span><span class="sxs-lookup"><span data-stu-id="77ab9-103">What's new or changed in Dynamics 365 for Talent Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77ab9-104">**Build 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="77ab9-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="77ab9-105">In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="77ab9-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="77ab9-106">Gestatten Sie bestimmte Zeit auf Freizeitanforderungen (halbe Tage)</span><span class="sxs-lookup"><span data-stu-id="77ab9-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="77ab9-107">Wenn Urlaub und Abwesenheit eingerichtet wird, sodass Freizeit in Tagen übermittelt wird, können Sie jetzt auch eine Halbtagsdefinition aktivieren.</span><span class="sxs-lookup"><span data-stu-id="77ab9-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="77ab9-108">Wenn Benutzer Freizeitanforderungen senden, können Sie angeben, ob diese die erste oder zweite Hälfte vom freiem Tag anfordern.</span><span class="sxs-lookup"><span data-stu-id="77ab9-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="77ab9-109">Standardmäßig ist diese Option deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="77ab9-109">By default, this option is turned off.</span></span> <span data-ttu-id="77ab9-110">Damit Mitarbeiter die erste oder zweite Hälfte von freiem Tag anfordern können, müssen Sie diese Option im Bereich **Urlaub und Abwesenheit** im Bereich Personalverwaltungsparameter aktivieren.</span><span class="sxs-lookup"><span data-stu-id="77ab9-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="77ab9-111">Das Sicherheitsrecht für diese Funktion wird in den Personalverwaltungsparametern verwaltet.</span><span class="sxs-lookup"><span data-stu-id="77ab9-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="77ab9-112">Prüfung von Urlaub- und Abwesenheitseinträgen</span><span class="sxs-lookup"><span data-stu-id="77ab9-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="77ab9-113">Abhängig davon, wie der Urlaub konfiguriert wird, erhalten Mitarbeiter eine Warnung, wenn sie versuchen, eine Freizeitanforderung zu senden, die länger ist als ihr Arbeitstag.</span><span class="sxs-lookup"><span data-stu-id="77ab9-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="77ab9-114">Das bedeutet, sie werden gewarnt, wenn Sie versuchen, mehr als einen ganzen Tag Urlaub an einem bestimmten Datum eingeben möchten.</span><span class="sxs-lookup"><span data-stu-id="77ab9-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="77ab9-115">Diese Prüfung ist immer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="77ab9-115">This validation is always turned on.</span></span> <span data-ttu-id="77ab9-116">Immer wenn Mitarbeiter den Tagschwellenwert überschreiten, der definiert wird, erhalten diese eine Warnung in ihrer Freizeitanforderung.</span><span class="sxs-lookup"><span data-stu-id="77ab9-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="77ab9-117">Zusätzliche Felder für Bedingungsanweisungen in den Workflows</span><span class="sxs-lookup"><span data-stu-id="77ab9-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="77ab9-118">Weitere Felder wurden den Bedingungsanweisungen und den Platzhaltern für mehrere Workflows in Core HR hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="77ab9-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="77ab9-119">Die folgenden Felder wurden der Kompensation, Kündigung und den Übergangsworkflow hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="77ab9-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="77ab9-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="77ab9-120">EmploymentType</span></span>
- <span data-ttu-id="77ab9-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="77ab9-121">LegalEntity</span></span>
- <span data-ttu-id="77ab9-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="77ab9-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="77ab9-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="77ab9-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="77ab9-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="77ab9-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="77ab9-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="77ab9-125">TransitionDate</span></span>
- <span data-ttu-id="77ab9-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="77ab9-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="77ab9-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="77ab9-127">WorkerStartDate</span></span>
- <span data-ttu-id="77ab9-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="77ab9-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="77ab9-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="77ab9-129">ProbationEndDate</span></span>
- <span data-ttu-id="77ab9-130">Position</span><span class="sxs-lookup"><span data-stu-id="77ab9-130">Position</span></span>
- <span data-ttu-id="77ab9-131">Gewerkschaft</span><span class="sxs-lookup"><span data-stu-id="77ab9-131">Union</span></span>
- <span data-ttu-id="77ab9-132">Abteilung</span><span class="sxs-lookup"><span data-stu-id="77ab9-132">Department</span></span>
- <span data-ttu-id="77ab9-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="77ab9-133">PositionType</span></span>
- <span data-ttu-id="77ab9-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="77ab9-134">CompLocation</span></span>
- <span data-ttu-id="77ab9-135">Titel</span><span class="sxs-lookup"><span data-stu-id="77ab9-135">Title</span></span>
- <span data-ttu-id="77ab9-136">Stelle</span><span class="sxs-lookup"><span data-stu-id="77ab9-136">Job</span></span>
- <span data-ttu-id="77ab9-137">JobType</span><span class="sxs-lookup"><span data-stu-id="77ab9-137">JobType</span></span>
- <span data-ttu-id="77ab9-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="77ab9-138">JobFamily</span></span>
- <span data-ttu-id="77ab9-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="77ab9-139">JobFunction</span></span>

<span data-ttu-id="77ab9-140">Die folgenden Felder wurden den Workflowpositionen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="77ab9-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="77ab9-141">Position</span><span class="sxs-lookup"><span data-stu-id="77ab9-141">Position</span></span>
- <span data-ttu-id="77ab9-142">Gewerkschaft</span><span class="sxs-lookup"><span data-stu-id="77ab9-142">Union</span></span>
- <span data-ttu-id="77ab9-143">Abteilung</span><span class="sxs-lookup"><span data-stu-id="77ab9-143">Department</span></span>
- <span data-ttu-id="77ab9-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="77ab9-144">PositionType</span></span>
- <span data-ttu-id="77ab9-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="77ab9-145">CompLocation</span></span>
- <span data-ttu-id="77ab9-146">Titel</span><span class="sxs-lookup"><span data-stu-id="77ab9-146">Title</span></span>
- <span data-ttu-id="77ab9-147">Stelle</span><span class="sxs-lookup"><span data-stu-id="77ab9-147">Job</span></span>
- <span data-ttu-id="77ab9-148">JobType</span><span class="sxs-lookup"><span data-stu-id="77ab9-148">JobType</span></span>
- <span data-ttu-id="77ab9-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="77ab9-149">JobFamily</span></span>
- <span data-ttu-id="77ab9-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="77ab9-150">JobFunction</span></span>

<span data-ttu-id="77ab9-151">Felder in den Bedingungsanweisungen und in den Platzhalter sind für alle Benutzer verfügbar, die den Zugriff haben, den oben genannten Workflow zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="77ab9-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="77ab9-152">Navigation zu Atract von der Personalführung</span><span class="sxs-lookup"><span data-stu-id="77ab9-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="77ab9-153">In Personalführung, wenn Attract nicht eingerichtet wurde, weist der Abschnitt **Kandidaten zum Anstellen** an, mit Attract zu beginnen, statt die Nachricht anzuzeigen, "Keinen Inhalt zum Anzeigen gefunden".</span><span class="sxs-lookup"><span data-stu-id="77ab9-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="77ab9-154">Andere Änderungen</span><span class="sxs-lookup"><span data-stu-id="77ab9-154">Other changes</span></span>

<span data-ttu-id="77ab9-155">Diese Version enthält eine Reihe zusätzlicher Fehlerkorrekturen:</span><span class="sxs-lookup"><span data-stu-id="77ab9-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="77ab9-156">Wenn ein Auftragnehmer angestellt wird, soll die Registerkarte **Kompensation** nicht auf der Anforderungs-/Aktionsseite verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="77ab9-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="77ab9-157">Während der Anforderungskündigungsprozesses können Sie nicht fortfahren, bis alle erforderlichen Felder Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="77ab9-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="77ab9-158">Sortierreihenfolgen und Datumsanzeigenprobleme auf der Personalführungsanalyse sind nicht behoben worden.</span><span class="sxs-lookup"><span data-stu-id="77ab9-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
