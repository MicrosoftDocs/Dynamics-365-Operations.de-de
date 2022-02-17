---
title: Fähigkeiten konfigurieren
description: Sie können die Fähigkeiten Ihrer Arbeitskraft in Dynamics 365 Human Resources verfolgen. Sie können auch die Qualifikationen angeben, die für eine bestimmte Stelle erforderlich sind.
author: twheeloc
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
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 13206bb3c961f001620e8b65a8b1bb39bf95ee49
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075070"
---
# <a name="configure-skills"></a>Fähigkeiten konfigurieren

> [!IMPORTANT]
> Die in diesem Thema beschriebene Funktionalität ist derzeit für Debitor-Kunden aus dem Bereich Human Resources auf der Finance-Infrastruktur verfügbar.  


Sie können die Fähigkeiten Ihrer Arbeitskraft in Dynamics 365 Human Resources verfolgen. Sie können auch die Qualifikationen angeben, die für eine bestimmte Stelle erforderlich sind.

Beispiele für Fähigkeiten, die Sie erfassen können, umfassen Folgendes:

- Supervisor-Qualität – Die Fähigkeit, die Arbeit anderer zu beaufsichtigen.
- Führungsqualitäten – Die Fähigkeit, Mitarbeiter und Geschäftsbereiche anzuführen.
- Planungsqualitäten – Die Fähigkeit vorausschauend zu denken, Visionen zu formen und diese umzusetzen.
- HTML – Die Möglichkeit, HTML-Code zu schreiben.

Wenn Sie noch keine Qualifikationstypen und Bewertungsmodelle eingerichtet haben, müssen Sie einige hinzufügen, bevor Sie Qualifikationen erstellen.

Die folgenden Personen können Qualifikationen für eine Arbeitskraft eingeben:

- Arbeitskräfte können ihre Qualifikationen im Employee Self-Service eingeben. Diese Fähigkeiten erfordern die Zustimmung des Managers.
- Manager können Fähigkeiten für ihre Mitarbeiter eingeben. Sie können einen Workflow erstellen, der diese Fähigkeiten automatisch genehmigt.

## <a name="create-a-skill-type"></a>Erstellen eines Qualifikationstyps

Qualifikationstypen sind Kategorien, unter die einzelne Fähigkeiten fallen, z. B. Verwaltung oder Vertrieb.

1. In dem **Personalentwicklung** Arbeitsbereich wählen Sie **Links** aus.

2. Unter **Kompetenzaufbau** wählen Sie **Qualifikationstypen** aus.

3. Wählen Sie **Neu** aus.

4. Füllen Sie dann die folgenden Felder aus:

   - **Qualifikationstypen**: Geben Sie einen eindeutigen Namen für den Qualifikationstyp ein.
   - **Beschreibung**: Geben Sie eine eindeutige Beschreibung für den Qualifikationstyp ein.

5. Wählen Sie **Speichern** aus.

## <a name="create-a-rating-model"></a>Neues Bewertungsmodell erstellen

Bewertungsmodelle helfen, die tatsächliche Qualifikationsebene einer Person auszuwerten, die Ebene an der sie arbeiten zu erhalten, oder die Qualifikationsebene, die für eine Stelle erforderlich ist, zu erreichen. Jede Ebene in einem Bewertungsmodell wird ein Faktor zugewiesen.

1. In dem **Personalentwicklung** Arbeitsbereich wählen Sie **Links** aus.

2. Unter **Kompetenzaufbau**, wählen Sie **Bewertungsmodelle**.

3. Wählen Sie **Neu** aus.

4. Füllen Sie dann die folgenden Felder aus:

   - **Bewertung**: Geben Sie einen Namen für das Bewertungsmodell ein, z.B. **Kompetenzen**.
   - **Beschreibung** : Geben Sie eine Beschreibung für das Bewertungsmodell ein, z.B. **Qualifikationsbewertungen**.

5. In dem Abschnitt **Ebenen** wählen Sie **Neu**. Füllen Sie für jede Ebene, die Sie hinzufügen möchten, die folgenden Felder aus:

   - **Ebene**: Geben Sie einen Namen für die Ebene ein.
   - **Beschreibung**: Geben Sie hier eine Beschreibung der Ebene ein.
   - **Faktor**: Geben Sie einen Faktorwert von 0-9 ein. Faktoren helfen, die Bewertungen der Fähigkeiten zu normalisieren, die verschiedene Bewertungsmodelle verwenden. Jede Ebener muss einen eindeutigen Faktor haben. Ebenen mit höheren Faktorwerten umfassen mehr Gewicht in einem Bewertungsmodell.

   Fügen Sie nach Bedarf weitere Ebenen hinzu. Sie können bis zu 10 Ebenen für jedes Bewertungsmodell eingeben.

6. Wählen Sie **Speichern** aus.

## <a name="create-a-skill"></a>Erstellen einer Qualifikation

Bevor Sie eine Qualifikation einer Person oder einer Stelle zuweisen, eine Fähigkeitszuordnungssuche, oder ein Fähigkeitsprofil erstellen, müssen Sie Informationen zu den einzelnen Qualifikationen auf der Seite **Qualifikationen** eingeben. Für jede Qualifikation können Sie einen Fähigkeitstyp und ein Bewertungsmodell auswählen.

1. In dem **Personalentwicklung** Arbeitsbereich wählen Sie **Links** aus.

2. Unter **Kompetenzaufbau** wählen Sie **Qualifikationen** aus.

3. Wählen Sie **Neu** aus.

4. Füllen Sie dann die folgenden Felder aus:

   - **Qualifikationen**: Geben Sie einen eindeutigen Namen für die Qualifikation ein.
   - **Beschreibung**: Geben Sie eine eindeutige Beschreibung für die Qualifikation ein.
   - **Bewertung**: Wählen Sie das Bewertungsmodell aus, das für diese Qualifikation verwendet werden soll.
   - **Qualifikationstyp**: Wählen Sie aus der Liste der Qualifikations-Typen aus.

5. Wählen Sie **Speichern** aus.

## <a name="see-also"></a>Siehe auch

[Geben Sie Fähigkeiten ein](hr-develop-enter-skills.md)<br>
[Qualifikationen aufzeichnen](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
