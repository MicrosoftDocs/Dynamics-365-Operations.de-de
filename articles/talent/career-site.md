---
title: Karrierestandortsfunktionen in Attract
description: "Dieser Artikel gibt eine Übersicht über die Funktionen der Karriereseite für Kandidaten in Microsoft Dynamics 365 for Talent - Attract. Es wird auch beschrieben, wie diese Funktionen eingerichtet werden."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: de-de
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="eab48-104">Karrierestandortsfunktionen in Attract</span><span class="sxs-lookup"><span data-stu-id="eab48-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eab48-105">Dieser Artikel gibt eine Übersicht über die Funktionen der Karriereseite für Kandidaten in Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="eab48-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="eab48-106">Es wird auch beschrieben, wie diese Funktionen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="eab48-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="eab48-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="eab48-107">Overview</span></span>

<span data-ttu-id="eab48-108">Attract eine Karriereseite für jede Umgebung in einem Mandanten bietet.</span><span class="sxs-lookup"><span data-stu-id="eab48-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="eab48-109">Wenn beispielsweise eine Organisation über eine Entwicklungsumgebung und einer Testumgebung verfügt, wird eine Karriereseite für die Entwicklungsumgebung und eine weitere für die der Testumgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="eab48-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="eab48-110">Jede Karriereseite ist **vollständig isoliert** und verfügt über einen eigenen Authentifizierungsmechanismus.</span><span class="sxs-lookup"><span data-stu-id="eab48-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="eab48-111">Stellen- und Kandidatenprofile werden zwischen Karriereseiten nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="eab48-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="eab48-112">Standardmäßig ist die Karriereseite öffentlich.</span><span class="sxs-lookup"><span data-stu-id="eab48-112">By default, the career site is public.</span></span> <span data-ttu-id="eab48-113">Daher können Kandidaten alle Stellen anzeigen, die als extern markiert werden, ohne sich anmelden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="eab48-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="eab48-114">Allerdings ist für alle weiteren Aktivitäten erforderlich, dass die Kandidaten sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="eab48-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="eab48-115">Verwaltung der Website mit Stellenangeboten</span><span class="sxs-lookup"><span data-stu-id="eab48-115">Career site management</span></span>

<span data-ttu-id="eab48-116">Die folgenden Elemente einer Karriereseite werden durch Einstellungen gesteuert:</span><span class="sxs-lookup"><span data-stu-id="eab48-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="eab48-117">**Organisationsname:** Der Organisationsname wird auf der Navigationsleiste oben auf der Karriereseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eab48-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="eab48-118">Wenn sie den Organisationsnamen auswählen, gelangen Kandidaten auf eine Seite, auf der alle offenen Stellen aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eab48-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="eab48-119">**Organisationslogo:** Ein Bild des Organisationslogos wird oben links der Karriereseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eab48-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="eab48-120">Wenn sie das Logobild auswählen, gelangen Kandidaten auf eine Seite, auf der alle offenen Stellen aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eab48-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="eab48-121">Um die Werte für den Organisationsnamen und das Logo festzulegen, melden Sie sich als Administrator in Attract an, wählen Sie im Menü **Einstellungen** (Zahnradsymbol) die Option **Administratorcenter** und anschließend die Registerkarte **Unternehmensdaten** aus.</span><span class="sxs-lookup"><span data-stu-id="eab48-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="eab48-122">Das Logobild, das auf der Karriereseite angezeigt wird, weist eine feste Höhe von 20 Pixeln (px) auf.</span><span class="sxs-lookup"><span data-stu-id="eab48-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="eab48-123">Das Bild, das Sie im Administratorcenter hinzufügen, wird passend skaliert.</span><span class="sxs-lookup"><span data-stu-id="eab48-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="eab48-124">Daher kann sich die Breite abhängig vom Bild ändern.</span><span class="sxs-lookup"><span data-stu-id="eab48-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="eab48-125">URL der Karriereseite</span><span class="sxs-lookup"><span data-stu-id="eab48-125">Career site URL</span></span>

<span data-ttu-id="eab48-126">Wenn Sie zum ersten Mal [eine externe Stelle veröffentlichen](./Creating-jobs-Attract.md#postings) können Sie den **Bewerben**-Link aus der Attract-Anwendung kopieren.</span><span class="sxs-lookup"><span data-stu-id="eab48-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="eab48-127">Die URL für diesen Link hat folgendes Format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="eab48-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="eab48-128">Die URL der Karriereseite ist eine Teilzeichenfolge der **Bewerben**-URL.</span><span class="sxs-lookup"><span data-stu-id="eab48-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="eab48-129">Sie besteht aus allem bis zum Unternehmensnamen.</span><span class="sxs-lookup"><span data-stu-id="eab48-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="eab48-130">Daher lautet die URL der Karriereseite der vorherigen **Bewerben**-URL`https://jobs.talent.dynamics.com/jobs/<company_name>/`</span><span class="sxs-lookup"><span data-stu-id="eab48-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="eab48-131">Authentifizierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="eab48-131">Authentication options</span></span>

<span data-ttu-id="eab48-132">Kandidaten haben folgende Anmeldungsoptionen bei einer Attract-Karriereseite:</span><span class="sxs-lookup"><span data-stu-id="eab48-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="eab48-133">Persönliches Konto:</span><span class="sxs-lookup"><span data-stu-id="eab48-133">Personal account:</span></span>

    - <span data-ttu-id="eab48-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="eab48-134">LinkedIn</span></span>
    - <span data-ttu-id="eab48-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="eab48-135">Microsoft</span></span>
    - <span data-ttu-id="eab48-136">Google</span><span class="sxs-lookup"><span data-stu-id="eab48-136">Google</span></span>
    - <span data-ttu-id="eab48-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="eab48-137">Facebook</span></span>

- <span data-ttu-id="eab48-138">Geschäfts- oder Schulkonto:</span><span class="sxs-lookup"><span data-stu-id="eab48-138">Work or school account:</span></span>

    - <span data-ttu-id="eab48-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="eab48-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="eab48-140">Azure AD-Anmeldung ist nur für interne Kandidaten vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="eab48-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="eab48-141">Daher funktioniert sie nur bei internen Kandidaten, die ihre Azure AD-Unternehmensanmeldeinformationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="eab48-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="eab48-142">Ein Kandidat z. B., der derzeit ein Mitarbeiter von Contoso Ltd ist, möchte sich auf eine Stelle im nicht zugehörigen Unternehmen, Alpine Ski House bewerben.</span><span class="sxs-lookup"><span data-stu-id="eab48-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="eab48-143">In diesem Fall wird die Anmeldung fehlschlagen, wenn der Mitarbeiter versucht, seine Azure AD-Anmeldeinformationen von Contoso Ltd zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="eab48-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="eab48-144">Erstellen und Verwalten eines Profils</span><span class="sxs-lookup"><span data-stu-id="eab48-144">Create and maintain a profile</span></span>

<span data-ttu-id="eab48-145">Nachdem sich Kandidaten in der Karriereseite angemeldet haben, können sie in der Navigationsleiste oben auf der Seite **Eigenes Profil** auswählen, um ihr Profil zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="eab48-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="eab48-146">Das Profil enthält persönliche Informationen, Informationen zur Berufserfahrung, Ausbildungsdetails, Dokumente, Links und Informationen zu Qualifikationen.</span><span class="sxs-lookup"><span data-stu-id="eab48-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="eab48-147">Nachdem ein Profil erstellt wurde, kann es zur Bewerbung auf Stellen verwendet werden, an denen der Kandidat interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="eab48-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="eab48-148">Profile helfen Attract außerdem dabei, Kandidaten die richtigen Stellen zu empfehlen.</span><span class="sxs-lookup"><span data-stu-id="eab48-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="eab48-149">Die richtige Stelle finden</span><span class="sxs-lookup"><span data-stu-id="eab48-149">Find the right job</span></span>

<span data-ttu-id="eab48-150">Auf der Stellenlistenseite können Kandidaten nach einer bestimmten Stelle suchen, indem sie Suchbegriffe eingeben.</span><span class="sxs-lookup"><span data-stu-id="eab48-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="eab48-151">Die Suchfunktion sucht nach den Suchbegriffen in Stellentiteln und Stellenbeschreibungen und zeigt relevante Stellen als Ergebnis an.</span><span class="sxs-lookup"><span data-stu-id="eab48-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="eab48-152">Kandidaten können die Ergebnisse jederzeit basierend auf dem Arbeitsort oder der Stellenfunktion filtern.</span><span class="sxs-lookup"><span data-stu-id="eab48-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="eab48-153">Kandidaten können auf der Karriereseite zudem einen Reihe empfohlener Stellen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="eab48-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="eab48-154">Die Stellen, die einem Kandidaten empfohlen werden, basierend auf den vergangenen Bewerbungen, dem Profil und den Lebensläufen des Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="eab48-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="eab48-155">Stellenempfehlungen werden nur angezeigt, wenn mindestens 10 Stellen auf der Karriereseite veröffentlicht wurden und der Kandidat sein Profil vollständig ausgefüllt hat.</span><span class="sxs-lookup"><span data-stu-id="eab48-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="eab48-156">Bewerben um Stellen</span><span class="sxs-lookup"><span data-stu-id="eab48-156">Apply for jobs</span></span>

<span data-ttu-id="eab48-157">Nachdem Kandidaten die richtige Stelle gefunden haben, können sie sich bewerben, indem sie die Schaltfläche **Bewerben** auf der Stellendetailseite verwenden.</span><span class="sxs-lookup"><span data-stu-id="eab48-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="eab48-158">An diesem Punkt können Kandidaten entweder ein nagelneues Profil erstellen oder die vorhandenen Informationen in ihrem Profil überprüfen.</span><span class="sxs-lookup"><span data-stu-id="eab48-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="eab48-159">Kandidaten können bei Bedarf auch einen Lebenslauf hochladen und die Stellenbewerbung dann senden.</span><span class="sxs-lookup"><span data-stu-id="eab48-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="eab48-160">Den Bewerbungsstatus prüfen</span><span class="sxs-lookup"><span data-stu-id="eab48-160">Check application status</span></span>

<span data-ttu-id="eab48-161">Nachdem sich Kandidaten auf mindestens eine Stelle beworben haben, können Sie in der Navigationsleiste oben auf der Seite **Bewerben** auswählen, um ihre offenen und geschlossenen Bewerbungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="eab48-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="eab48-162">Wenn Kandidaten eine ihrer Bewerbungen öffnen, sehen sie die aktuelle Phase sowie alle ausstehenden Aktionselemente, die sie durchführen müssen.</span><span class="sxs-lookup"><span data-stu-id="eab48-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="eab48-163">Wenn ein Kandidat beispielsweise potenzielle Datumsangaben für ein persönliches Bewerbungsgespräch bereitstellen muss, zeigt die Seite seine Optionen an.</span><span class="sxs-lookup"><span data-stu-id="eab48-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="eab48-164">Interne Stellen</span><span class="sxs-lookup"><span data-stu-id="eab48-164">Internal jobs</span></span>

<span data-ttu-id="eab48-165">Derzeit werden Stellen, die als intern markiert und auf der Attract-Karriereseite veröffentlicht werden, dort nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eab48-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="eab48-166">Sie sind nur direkt über die **Bewerben**-URL verfügbar, die aus der Attract-Anwendung kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="eab48-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

