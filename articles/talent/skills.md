---
title: Angleichen der Belegschaftsqualifikationen mit der Geschäftstätigkeit
description: Sie können auch die Qualifikationen nachverfolgen, die Arbeitskräfte, Bewerber oder Kontaktpersonen haben oder haben sollen um ihre Rollen effektiv auszuführen. Sie können auch die Qualifikationen angeben, die für eine bestimmte Stelle erforderlich sind.
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 0b86a8d134ef553db6719f4cefb02e4acfc00ae5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304505"
---
# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="76c94-104">Angleichen der Belegschaftsqualifikationen mit der Geschäftstätigkeit</span><span class="sxs-lookup"><span data-stu-id="76c94-104">Align workforce skills with business needs</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="76c94-105">Sie können auch die Qualifikationen nachverfolgen, die Arbeitskräfte, Bewerber oder Kontaktpersonen haben oder haben sollen um ihre Rollen effektiv auszuführen.</span><span class="sxs-lookup"><span data-stu-id="76c94-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="76c94-106">Sie können auch die Qualifikationen angeben, die für eine bestimmte Stelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="76c94-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="76c94-107">Beispiele für Fähigkeiten, die Sie erfassen können, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="76c94-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="76c94-108">Supervisor-Qualität – Die Fähigkeit, die Arbeit anderer zu beaufsichtigen.</span><span class="sxs-lookup"><span data-stu-id="76c94-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="76c94-109">Führungsqualitäten – Die Fähigkeit, Mitarbeiter und Geschäftsbereiche anzuführen.</span><span class="sxs-lookup"><span data-stu-id="76c94-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="76c94-110">Planungsqualitäten – Die Fähigkeit vorausschauend zu denken, Visionen zu formen und diese umzusetzen.</span><span class="sxs-lookup"><span data-stu-id="76c94-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="76c94-111">HTML – Die Möglichkeit, HTML-Code zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="76c94-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="76c94-112">Bevor Sie eine Qualifikation einer Person oder einer Stelle zuweisen, eine Fähigkeitszuordnungssuche, oder ein Fähigkeitsprofil erstellen, müssen Sie Informationen zu den Qualifikationen auf der Seite **Qualifikationen** eingeben.</span><span class="sxs-lookup"><span data-stu-id="76c94-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="76c94-113">Für jede Qualifikation können Sie einen Fähigkeitstyp und ein Bewertungsmodell auswählen.</span><span class="sxs-lookup"><span data-stu-id="76c94-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="76c94-114">Bewertungsmodelle</span><span class="sxs-lookup"><span data-stu-id="76c94-114">Rating models</span></span>
<span data-ttu-id="76c94-115">Bewertungsmodelle helfen, die tatsächliche Qualifikationsebene einer Person auszuwerten, die Ebene an der sie arbeiten um sie zu erhalten, oder die Qualifikationsebene, die für eine Stelle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="76c94-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="76c94-116">Sie können bis zu 10 Ebenen für ein Bewertungsmodell eingeben.</span><span class="sxs-lookup"><span data-stu-id="76c94-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="76c94-117">Jede Ebene in einem Bewertungsmodell wird ein Faktor zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="76c94-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="76c94-118">Der Faktorwert wird verwendet, um die Bewertungen der Fähigkeiten zu normalisieren, die verschiedene Bewertungsmodelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="76c94-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="76c94-119">Der Faktor muss eine Zahl zwischen 0 und 9 sein, und jede Ebene muss einen eindeutigen Faktor haben.</span><span class="sxs-lookup"><span data-stu-id="76c94-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="76c94-120">Ebenen mit höheren Faktorwerten umfassen mehr Gewicht in einem Bewertungsmodell.</span><span class="sxs-lookup"><span data-stu-id="76c94-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="76c94-121">Geben Sie Qualifikationen für eine Stelle an</span><span class="sxs-lookup"><span data-stu-id="76c94-121">Specify job skills</span></span>
<span data-ttu-id="76c94-122">Wenn Sie Informationen zu einer Stelle eingeben, können Sie die Qualifikationen angeben, die eine Person haben sollte, um für die Stelle geeignet zu sein.</span><span class="sxs-lookup"><span data-stu-id="76c94-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="76c94-123">Darüber hinaus können Sie die gewünschte Stufe für jede Qualifikation sowie die Wichtigkeit der Fähigkeit angeben.</span><span class="sxs-lookup"><span data-stu-id="76c94-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="76c94-124">Für unterschiedliche Stellen ist eine bestimmte Qualifikation u. U. unterschiedlich wichtig.</span><span class="sxs-lookup"><span data-stu-id="76c94-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="76c94-125">Geben Sie Qualifikationen für Arbeitskräfte, Bewerber oder Kontakte ein</span><span class="sxs-lookup"><span data-stu-id="76c94-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="76c94-126">Sie können Zielqualifikationen oder tatsächliche Qualifikationen für Arbeitskräfte, Bewerber oder Kontakte eingeben.</span><span class="sxs-lookup"><span data-stu-id="76c94-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="76c94-127">Eine Zielqualifikation ist eine Qualifikation, die eine Person plant zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="76c94-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="76c94-128">Eine tatsächliche Qualifikation ist eine Qualifikation, die eine Person derzeit hat.</span><span class="sxs-lookup"><span data-stu-id="76c94-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="76c94-129">Fähigkeitszuordnung und Fähigkeitszuordnungsprofile</span><span class="sxs-lookup"><span data-stu-id="76c94-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="76c94-130">Sie können eine Qualifikationszuordnungssuche erstellen, um eine Arbeitskraft, einen Bewerber oder einen Kontakt zu finden, die bzw. der für die bestimmte Art der Aufgabe qualifiziert ist.</span><span class="sxs-lookup"><span data-stu-id="76c94-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="76c94-131">Qualifikationszuordnungssuchen suchen nach Fähigkeiten, Ausbildungen, Bescheinigungen, Positionen mit Vertrauenswürdigkeit und Projekterfahrung und geben Ergebnisse zurück, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="76c94-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="76c94-132">Beispielsweise kann es sinnvoll sein, zu wissen, welche Arbeitskräfte in der Organisation ihr CPA erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="76c94-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="76c94-133">Mit Qualifikationszuordnungsprofilen finden Sie Mitarbeiter oder Kandidaten mit Fähigkeiten, die den Unternehmensanforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="76c94-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="76c94-134">So können Sie beispielsweise ein Qualifikationszuordnungsprofil für eine offene Position in Ihrer Organisation erstellen.</span><span class="sxs-lookup"><span data-stu-id="76c94-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="76c94-135">Wenn Sie ein Profil für einen bestimmten Stelle erstellen und Qualifikationen, Bescheinigungen und Ausbildung aus diesem Einzelvorgang auf das Profil kopieren, können Sie Arbeitskräfte, Bewerber und Kontaktpersonen suchen, die mit einer oder mehreren der Kriterien übereinstimmen, die für das Profil eingegeben sind. Sie können eine Liste der Kandidaten anzeigen, deren Qualifikationen am besten mit den Qualifikationen übereinstimmen, die für die Stelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="76c94-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

> <span data-ttu-id="76c94-136">**Hinweis** Nur Arbeitskräfte, Bewerber und Kontaktpersonen, die ausgewählt werden, um in die Qualifikationszuordnungssuchen einbezogen zu werden, können in einer Qualifikationszuordnungsergebnisliste angezeigt werden oder in einem Qualifikationsprofil einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="76c94-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="76c94-137">Wenn Sie eine Arbeitskraft, einen Bewerber oder eine Kontaktperson in Qualifikationszuordnungssuchen, wählen Sie auf den folgenden Seiten in **Qualifikationszuordnung einschließen** "Ja" aus:</span><span class="sxs-lookup"><span data-stu-id="76c94-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>
> 
> + <span data-ttu-id="76c94-138">Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="76c94-138">Worker</span></span>
> + <span data-ttu-id="76c94-139">Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="76c94-139">Employee</span></span>
> + <span data-ttu-id="76c94-140">Bewerber</span><span class="sxs-lookup"><span data-stu-id="76c94-140">Applicant</span></span>
> + <span data-ttu-id="76c94-141">Kontakte</span><span class="sxs-lookup"><span data-stu-id="76c94-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="76c94-142">Qualifikationsdefizitanalyse und Qualifikationsprofilanalyse</span><span class="sxs-lookup"><span data-stu-id="76c94-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="76c94-143">Sie können eine Qualifikationsprofilanalyse erstellen, um eine Liste der Kompetenzen für eine Arbeitskraft, einen Bewerber oder eine Kontaktperson zu einem bestimmten Datum anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="76c94-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="76c94-144">Sie können eine Qualifikationsdefizitanalyse erstellen, um die Qualifikationen einer Person zu vergleichen und die Qualifikationen, die für eine spezifische Stelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="76c94-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="additional-resources"></a><span data-ttu-id="76c94-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="76c94-145">Additional resources</span></span>
--------

[<span data-ttu-id="76c94-146">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="76c94-146">Human resources</span></span>](index.md)



