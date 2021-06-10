---
title: Qualifikationen aufzeichnen
description: Sie können eine Qualifikations-Mapping-Suche erstellen, um eine qualifizierte Person in Dynamics 365 Human Resources zu finden.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076593"
---
# <a name="map-skills"></a><span data-ttu-id="9f0eb-103">Qualifikationen aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="9f0eb-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9f0eb-104">Sie können eine Qualifikations-Mapping-Suche erstellen, um eine qualifizierte Person in Dynamics 365 Human Resources zu finden.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="9f0eb-105">Qualifikations-Mapping-Suchen geben Ergebnisse für Kriterien zurück, die Sie eingeben, indem Sie die folgenden Informationen durchsehen:</span><span class="sxs-lookup"><span data-stu-id="9f0eb-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="9f0eb-106">Qualifikationen</span><span class="sxs-lookup"><span data-stu-id="9f0eb-106">Skills</span></span>
- <span data-ttu-id="9f0eb-107">Ausbildung</span><span class="sxs-lookup"><span data-stu-id="9f0eb-107">Education</span></span>
- <span data-ttu-id="9f0eb-108">Bescheinigungen</span><span class="sxs-lookup"><span data-stu-id="9f0eb-108">Certificates</span></span>
- <span data-ttu-id="9f0eb-109">Positionen</span><span class="sxs-lookup"><span data-stu-id="9f0eb-109">Positions</span></span>
- <span data-ttu-id="9f0eb-110">Projekterfahrung</span><span class="sxs-lookup"><span data-stu-id="9f0eb-110">Project experience</span></span>

<span data-ttu-id="9f0eb-111">Sie können beispielsweise Personen in Ihrer Organisation finden, die ihren CPA verdient haben.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="9f0eb-112">Mit Qualifikationszuordnungsprofilen finden Sie Mitarbeiter oder Kandidaten mit Fähigkeiten, die den Unternehmensanforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="9f0eb-113">Nur Arbeitskräfte, Bewerber und Kontaktpersonen, die ausgewählt werden, um in die Qualifikationszuordnungssuchen einbezogen zu werden, können in einer Qualifikationszuordnungsergebnisliste angezeigt oder in einem Qualifikationsprofil einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="9f0eb-114">Wenn Sie eine Arbeitskraft, einen Bewerber oder eine Kontaktperson in Qualifikationszuordnungssuchen, wählen Sie auf den folgenden Seiten in **Qualifikationszuordnung einschließen** **Ja** aus:</span><span class="sxs-lookup"><span data-stu-id="9f0eb-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="9f0eb-115">Worker</span><span class="sxs-lookup"><span data-stu-id="9f0eb-115">Worker</span></span><br>
> - <span data-ttu-id="9f0eb-116">Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9f0eb-116">Employee</span></span><br>
> - <span data-ttu-id="9f0eb-117">Bewerber</span><span class="sxs-lookup"><span data-stu-id="9f0eb-117">Applicant</span></span><br>
> - <span data-ttu-id="9f0eb-118">Kontakte</span><span class="sxs-lookup"><span data-stu-id="9f0eb-118">Contacts</span></span><br>

<span data-ttu-id="9f0eb-119">Um ein Qualifikations-Mapping zu erstellen, gehen Sie zu **Mitarbeiterentwicklung> Links > Qualifikations-Mapping**.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="9f0eb-120">Um ein Qualifikations-Mappingprofil zu erstellen, gehen Sie zu **Mitarbeiterentwicklung> Links > Qualifikations-Mappingprofil**.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="9f0eb-121">Qualifikationsdefizitanalyse und Qualifikationsprofilanalyse</span><span class="sxs-lookup"><span data-stu-id="9f0eb-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="9f0eb-122">Sie können eine Fähigkeitsprofilanalyse erstellen, um eine Liste der Kompetenzen einer Person anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="9f0eb-123">Sie können eine Fähigkeitslückenanalyse erstellen, um die Qualifikationen einer Person mit den Qualifikationen zu vergleichen, die für eine Stelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="9f0eb-124">Um eine Lückenanalyse zu erstellen, gehen Sie zu **Mitarbeiterentwicklung > Links > Qualifikationslückenanalyse Stelle – Person**.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="9f0eb-125">Um ein Qualifikationsprofilanalyse zu erstellen, gehen Sie zu **Mitarbeiterentwicklung > Links > Qualifikationsprofilanalyse**.</span><span class="sxs-lookup"><span data-stu-id="9f0eb-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f0eb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f0eb-126">See also</span></span>

[<span data-ttu-id="9f0eb-127">Fähigkeiten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9f0eb-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="9f0eb-128">Geben Sie Fähigkeiten ein</span><span class="sxs-lookup"><span data-stu-id="9f0eb-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]