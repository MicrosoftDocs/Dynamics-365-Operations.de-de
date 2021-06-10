---
title: Fähigkeiten konfigurieren
description: Sie können die Fähigkeiten Ihrer Arbeitskraft in Dynamics 365 Human Resources verfolgen. Sie können auch die Qualifikationen angeben, die für eine bestimmte Stelle erforderlich sind.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076558"
---
# <a name="configure-skills"></a><span data-ttu-id="6e6b0-104">Fähigkeiten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6e6b0-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6e6b0-105">Sie können die Fähigkeiten Ihrer Arbeitskraft in Dynamics 365 Human Resources verfolgen.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6e6b0-106">Sie können auch die Qualifikationen angeben, die für eine bestimmte Stelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="6e6b0-107">Beispiele für Fähigkeiten, die Sie erfassen können, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6e6b0-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="6e6b0-108">Supervisor-Qualität – Die Fähigkeit, die Arbeit anderer zu beaufsichtigen.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="6e6b0-109">Führungsqualitäten – Die Fähigkeit, Mitarbeiter und Geschäftsbereiche anzuführen.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="6e6b0-110">Planungsqualitäten – Die Fähigkeit vorausschauend zu denken, Visionen zu formen und diese umzusetzen.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="6e6b0-111">HTML – Die Möglichkeit, HTML-Code zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="6e6b0-112">Wenn Sie noch keine Qualifikationstypen und Bewertungsmodelle eingerichtet haben, müssen Sie einige hinzufügen, bevor Sie Qualifikationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="6e6b0-113">Die folgenden Personen können Qualifikationen für eine Arbeitskraft eingeben:</span><span class="sxs-lookup"><span data-stu-id="6e6b0-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="6e6b0-114">Arbeitskräfte können ihre Qualifikationen im Employee Self-Service eingeben.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="6e6b0-115">Diese Fähigkeiten erfordern die Zustimmung des Managers.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-115">These skills require manager approval.</span></span>
- <span data-ttu-id="6e6b0-116">Manager können Fähigkeiten für ihre Mitarbeiter eingeben.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="6e6b0-117">Sie können einen Workflow erstellen, der diese Fähigkeiten automatisch genehmigt.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="6e6b0-118">Erstellen eines Qualifikationstyps</span><span class="sxs-lookup"><span data-stu-id="6e6b0-118">Create a skill type</span></span>

<span data-ttu-id="6e6b0-119">Qualifikationstypen sind Kategorien, unter die einzelne Fähigkeiten fallen, z. B. Verwaltung oder Vertrieb.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="6e6b0-120">In dem **Personalentwicklung** Arbeitsbereich wählen Sie **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="6e6b0-121">Unter **Kompetenzaufbau** wählen Sie **Qualifikationstypen** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="6e6b0-122">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-122">Select **New**.</span></span>

4. <span data-ttu-id="6e6b0-123">Füllen Sie dann die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="6e6b0-123">Complete the following fields:</span></span>

   - <span data-ttu-id="6e6b0-124">**Qualifikationstypen**: Geben Sie einen eindeutigen Namen für den Qualifikationstyp ein.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="6e6b0-125">**Beschreibung**: Geben Sie eine eindeutige Beschreibung für den Qualifikationstyp ein.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="6e6b0-126">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="6e6b0-127">Neues Bewertungsmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="6e6b0-127">Create a rating model</span></span>

<span data-ttu-id="6e6b0-128">Bewertungsmodelle helfen, die tatsächliche Qualifikationsebene einer Person auszuwerten, die Ebene an der sie arbeiten zu erhalten, oder die Qualifikationsebene, die für eine Stelle erforderlich ist, zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="6e6b0-129">Jede Ebene in einem Bewertungsmodell wird ein Faktor zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="6e6b0-130">In dem **Personalentwicklung** Arbeitsbereich wählen Sie **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="6e6b0-131">Unter **Kompetenzaufbau**, wählen Sie **Bewertungsmodelle**.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="6e6b0-132">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-132">Select **New**.</span></span>

4. <span data-ttu-id="6e6b0-133">Füllen Sie dann die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="6e6b0-133">Complete the following fields:</span></span>

   - <span data-ttu-id="6e6b0-134">**Bewertung**: Geben Sie einen Namen für das Bewertungsmodell ein, z.B. **Kompetenzen**.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="6e6b0-135">**Beschreibung** : Geben Sie eine Beschreibung für das Bewertungsmodell ein, z.B. **Qualifikationsbewertungen**.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="6e6b0-136">In dem Abschnitt **Ebenen** wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="6e6b0-137">Füllen Sie für jede Ebene, die Sie hinzufügen möchten, die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="6e6b0-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="6e6b0-138">**Ebene**: Geben Sie einen Namen für die Ebene ein.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="6e6b0-139">**Beschreibung**: Geben Sie hier eine Beschreibung der Ebene ein.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="6e6b0-140">**Faktor**: Geben Sie einen Faktorwert von 0-9 ein.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="6e6b0-141">Faktoren helfen, die Bewertungen der Fähigkeiten zu normalisieren, die verschiedene Bewertungsmodelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="6e6b0-142">Jede Ebener muss einen eindeutigen Faktor haben.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-142">Each level must have a unique factor.</span></span> <span data-ttu-id="6e6b0-143">Ebenen mit höheren Faktorwerten umfassen mehr Gewicht in einem Bewertungsmodell.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="6e6b0-144">Fügen Sie nach Bedarf weitere Ebenen hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="6e6b0-145">Sie können bis zu 10 Ebenen für jedes Bewertungsmodell eingeben.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="6e6b0-146">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="6e6b0-147">Erstellen einer Qualifikation</span><span class="sxs-lookup"><span data-stu-id="6e6b0-147">Create a skill</span></span>

<span data-ttu-id="6e6b0-148">Bevor Sie eine Qualifikation einer Person oder einer Stelle zuweisen, eine Fähigkeitszuordnungssuche, oder ein Fähigkeitsprofil erstellen, müssen Sie Informationen zu den einzelnen Qualifikationen auf der Seite **Qualifikationen** eingeben.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="6e6b0-149">Für jede Qualifikation können Sie einen Fähigkeitstyp und ein Bewertungsmodell auswählen.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="6e6b0-150">In dem **Personalentwicklung** Arbeitsbereich wählen Sie **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="6e6b0-151">Unter **Kompetenzaufbau** wählen Sie **Qualifikationen** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="6e6b0-152">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-152">Select **New**.</span></span>

4. <span data-ttu-id="6e6b0-153">Füllen Sie dann die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="6e6b0-153">Complete the following fields:</span></span>

   - <span data-ttu-id="6e6b0-154">**Qualifikationen**: Geben Sie einen eindeutigen Namen für die Qualifikation ein.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="6e6b0-155">**Beschreibung**: Geben Sie eine eindeutige Beschreibung für die Qualifikation ein.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="6e6b0-156">**Bewertung**: Wählen Sie das Bewertungsmodell aus, das für diese Qualifikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="6e6b0-157">**Qualifikationstyp**: Wählen Sie aus der Liste der Qualifikations-Typen aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="6e6b0-158">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6b0-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e6b0-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e6b0-159">See also</span></span>

[<span data-ttu-id="6e6b0-160">Geben Sie Fähigkeiten ein</span><span class="sxs-lookup"><span data-stu-id="6e6b0-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="6e6b0-161">Qualifikationen aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="6e6b0-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]