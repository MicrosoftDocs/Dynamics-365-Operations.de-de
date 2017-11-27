---
title: "Angleichen der Belegschaftsqualifikationen mit der Geschäftstätigkeit"
description: "Sie können auch die Qualifikationen nachverfolgen, die Arbeitskräfte, Bewerber oder Kontaktpersonen haben oder haben sollen um ihre Rollen effektiv auszuführen. Sie können auch die Qualifikationen angeben, die für eine bestimmte Stelle erforderlich sind."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e9e66d3c6309c195e076fd86c31aa0adade97394
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="align-workforce-skills-with-business-needs"></a>Angleichen der Belegschaftsqualifikationen mit der Geschäftstätigkeit

[!include[banner](includes/banner.md)]


Sie können auch die Qualifikationen nachverfolgen, die Arbeitskräfte, Bewerber oder Kontaktpersonen haben oder haben sollen um ihre Rollen effektiv auszuführen. Sie können auch die Qualifikationen angeben, die für eine bestimmte Stelle erforderlich sind.

Beispiele für Fähigkeiten, die Sie erfassen können, umfassen Folgendes:
-   Supervisor-Qualität – Die Fähigkeit, die Arbeit anderer zu beaufsichtigen.
-   Führungsqualitäten – Die Fähigkeit, Mitarbeiter und Geschäftsbereiche anzuführen.
-   Planungsqualitäten – Die Fähigkeit vorausschauend zu denken, Visionen zu formen und diese umzusetzen.
-   HTML – Die Möglichkeit, HTML-Code zu schreiben.

Bevor Sie eine Qualifikation einer Person oder einer Stelle zuweisen, eine Fähigkeitszuordnungssuche, oder ein Fähigkeitsprofil erstellen, müssen Sie Informationen zu den Qualifikationen auf der Seite **Qualifikationen** eingeben. Für jede Qualifikation können Sie einen Fähigkeitstyp und ein Bewertungsmodell auswählen.

## <a name="rating-models"></a>Bewertungsmodelle
Bewertungsmodelle helfen, die tatsächliche Qualifikationsebene einer Person auszuwerten, die Ebene an der sie arbeiten um sie zu erhalten, oder die Qualifikationsebene, die für eine Stelle erforderlich ist. Sie können bis zu 10 Ebenen für ein Bewertungsmodell eingeben.  Jede Ebene in einem Bewertungsmodell wird ein Faktor zugewiesen.  Der Faktorwert wird verwendet, um die Bewertungen der Fähigkeiten zu normalisieren, die verschiedene Bewertungsmodelle verwenden.  Der Faktor muss eine Zahl zwischen 0 und 9 sein, und jede Ebene muss einen eindeutigen Faktor haben.  Ebenen mit höheren Faktorwerten umfassen mehr Gewicht in einem Bewertungsmodell.

## <a name="specify-job-skills"></a>Geben Sie Qualifikationen für eine Stelle an
Wenn Sie Informationen zu einer Stelle eingeben, können Sie die Qualifikationen angeben, die eine Person haben sollte, um für die Stelle geeignet zu sein.  Darüber hinaus können Sie die gewünschte Stufe für jede Qualifikation sowie die Wichtigkeit der Fähigkeit angeben. Für unterschiedliche Stellen ist eine bestimmte Qualifikation u. U. unterschiedlich wichtig.

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>Geben Sie Qualifikationen für Arbeitskräfte, Bewerber oder Kontakte ein
Sie können Zielqualifikationen oder tatsächliche Qualifikationen für Arbeitskräfte, Bewerber oder Kontakte eingeben. Eine Zielqualifikation ist eine Qualifikation, die eine Person plant zu erreichen. Eine tatsächliche Qualifikation ist eine Qualifikation, die eine Person derzeit hat.

## <a name="skill-mapping-and-skill-mapping-profiles"></a>Fähigkeitszuordnung und Fähigkeitszuordnungsprofile
Sie können eine Qualifikationszuordnungssuche erstellen, um eine Arbeitskraft, einen Bewerber oder einen Kontakt zu finden, die bzw. der für die bestimmte Art der Aufgabe qualifiziert ist. Qualifikationszuordnungssuchen suchen nach Fähigkeiten, Ausbildungen, Bescheinigungen, Positionen mit Vertrauenswürdigkeit und Projekterfahrung und geben Ergebnisse zurück, die den angegebenen Kriterien entsprechen.  Beispielsweise kann es sinnvoll sein, zu wissen, welche Arbeitskräfte in der Organisation ihr CPA erhalten haben.

Mit Qualifikationszuordnungsprofilen finden Sie Mitarbeiter oder Kandidaten mit Fähigkeiten, die den Unternehmensanforderungen entsprechen.  So können Sie beispielsweise ein Qualifikationszuordnungsprofil für eine offene Position in Ihrer Organisation erstellen. Wenn Sie ein Profil für einen bestimmten Stelle erstellen und Qualifikationen, Bescheinigungen und Ausbildung aus diesem Einzelvorgang auf das Profil kopieren, können Sie Arbeitskräfte, Bewerber und Kontaktpersonen suchen, die mit einer oder mehreren der Kriterien übereinstimmen, die für das Profil eingegeben sind. Sie können eine Liste der Kandidaten anzeigen, deren Qualifikationen am besten mit den Qualifikationen übereinstimmen, die für die Stelle erforderlich sind.

>**Hinweis** Nur Arbeitskräfte, Bewerber und Kontaktpersonen, die ausgewählt werden, um in die Qualifikationszuordnungssuchen einbezogen zu werden, können in einer Qualifikationszuordnungsergebnisliste angezeigt werden oder in einem Qualifikationsprofil einbezogen werden. Wenn Sie eine Arbeitskraft, einen Bewerber oder eine Kontaktperson in Qualifikationszuordnungssuchen, wählen Sie auf den folgenden Seiten in **Qualifikationszuordnung einschließen** "Ja" aus:

> + Arbeitskraft
> + Mitarbeiter
> + Bewerber
> + Kontakte

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>Qualifikationsdefizitanalyse und Qualifikationsprofilanalyse
Sie können eine Qualifikationsprofilanalyse erstellen, um eine Liste der Kompetenzen für eine Arbeitskraft, einen Bewerber oder eine Kontaktperson zu einem bestimmten Datum anzuzeigen. Sie können eine Qualifikationsdefizitanalyse erstellen, um die Qualifikationen einer Person zu vergleichen und die Qualifikationen, die für eine spezifische Stelle erforderlich sind.  



<a name="see-also"></a>Siehe auch
--------

[Personalverwaltung](index.md)




