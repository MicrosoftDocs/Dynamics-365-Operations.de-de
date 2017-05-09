---
title: Anzeigen und beurteilen der Ergebnisse eines Fragebogens
description: "In diesem Thema wird beschrieben, wie Sie die Ergebnisse von Fragebögen anzeigen und bewerten können, die die Befragten abgeschlossen haben."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: bcf59ea8862280675c9fb711d2aab1e8dff18806
ms.lasthandoff: 03/31/2017


---

# <a name="view-and-evaluate-the-results-of-a-questionnaire"></a>Anzeigen und beurteilen der Ergebnisse eines Fragebogens

In diesem Thema wird beschrieben, wie Sie die Ergebnisse von Fragebögen anzeigen und bewerten können, die die Befragten abgeschlossen haben. 

Nachdem die Befragungsteilnehmer einen Fragebogen ausgefüllt haben, können Sie die Fragebogenergebnisse folgendermaßen anzeigen und auswerten:

-   **Ausgefüllte Antwortsitzungen** - Anzeigen von Details zu ausgefüllten Fragebögen der Befragten und Generieren von Berichten, um Antworten zusammenzufassen, auch zu den erworbenen Punkten.
-   **Ergebnisgruppen** - Anzeigen von Ergebnisgruppedetails und -statistiken für Fragebögen. Die Ergebnisgruppenstatistik kann für eine einzelne Antwortsitzung oder für alle Beantwortungssitzungen eines Fragebogens generiert werden.
-   **Fragebogenstatistik** - Angeben von Kriterien für die Berechnung von Statistiken für eine bestimmte Gruppe von Teilnehmern.

Es können auch verschiedene Berichte generiert werden, um Ergebnisse nach Person, Antwortsitzung oder Ergebnisgruppe sortiert anzuzeigen. Die folgenden Berichte zu ausgefüllten Fragebögen sind verfügbar:

-   Antworten
-   Antworten pro Fragebogen
-   Antworten pro Person
-   Rückmeldungsanalyse

## <a name="answer-session-results"></a>Antwortsitzungsergebnisse
Nachdem die Teilnehmer einen Fragebogen ausgefüllt haben, können Sie die Ergebnisse abgeschlossener Antwortsitzungen anzeigen. Eine Antwortsitzung ist die Beantwortung eines Fragebogens durch einen Benutzer. Sie können Details zu abgeschlossenen Antwortsitzungen auf der Seite **Antworten** anzeigen. Die Antwortsitzungen, die auf der Seite **Antworten** enthalten sind, werden auf verschiedene Weise gefiltert, abhängig davon, wie Sie die Seite öffnen:

-   Alle Fragebögen
-   Ein bestimmter Fragebogen
-   Eine bestimmte Person

Auf der Seite **Antworten** können Sie Details zu Antworten, erzielten Punkten, den Antworten eines Teilnehmers in jeder Ergebnisgruppe und zur Fragenhierarchie anzeigen, die im ausgewählten Fragebogen verwendet wird. Sie können auch die folgenden Berichte generieren und drucken:

-   **Ergebnisbericht** - Dieser Bericht zeigt eine grafische Darstellung der Punkte, die pro Ergebnisgruppe für die ausgewählte Antwortsitzung erzielt wurden.
-   **Antwortbericht** - In diesem Bericht werden die Antworten angezeigt, die der Befragte für jede Frage zum Fragebogen ausgewählt hat.
-   **Falsche Antworten** - Dieser Bericht werden Informationen zu den falschen Antworten des Befragten angezeigt.

**Hinweis:** Der **Ergebnisse**-Bericht ist nur verfügbar, wenn Sie Ergebnisgruppen im Fragebogen verwendet und wenn Sie auf der Seite **Ergebnisse** auf der Seite **Fragebögen** ausgewählt haben. Der **Antwort**-Bericht und der **Falsche Antworten**-Bericht sind nur verfügbar, wenn Sie auf der Seite **Antwortbericht** der Seite **Fragebögen** ausgewählt haben.

## <a name="questionnaire-statistics"></a>Fragebogenstatistik
Mithilfe der Fragebogenstatistik können Sie die Ergebnisse eines ausgefüllten Fragebogen analysieren, der auf den Berechnungen beruht, die Sie definieren. Um Berechnungen zu definieren, müssen Sie die folgenden Aufgaben ausführen:

-   Wählen Sie Kriterien aus, um die Statistik zu berechnen und anzuzeigen.
    -   Sie können Statistiken nach Fragebogen, Fragen, Fragenzeilen oder Ergebnisgruppen anzeigen.
    -   Wählen Sie den Diagrammtyp aus, der verwendet wird, wenn Sie Ergebnisse anzeigen.
    -   Wählen Sie die Typen von Personen im Netzwerk aus, z. B. Mitarbeiter, Kontaktperson oder Bewerber, deren Antworten einbezogen werden sollen. Sie können auch Antworten von Fragebögen einbeziehen, die anonym ausgefüllt wurden.
    -   Richten Sie Intervalle ein, die auf dem Alter oder Dienstalter beruhen, um die Ergebnisse zu analysieren.
-   Hier können Sie Einstellungen auswählen oder anzeigen, mit denen das Thema der Statistik enger eingegrenzt werden kann. Wenn Sie z. B. eine Postleitzahl auswählen, können Sie die Ergebnisse für alle Befragten im betreffenden geografischen Gebiet analysieren.
-   Wählen Sie Kriterien aus, oder zeigen Sie Kriterien an, um die Ergebnisse nach Merkmalen des Befragten oder des Fragebogens zu analysieren. Wenn Sie z. B. die **Postleitzahl** auswählen, können Sie die Korrelation zwischen dem Standort eines Befragten und den richtigen Antworten analysieren.

Die festgelegten Einstellungen werden gespeichert und können zur regelmäßigen Neuberechnung der Ergebnisse verwendet werden.

<a name="see-also"></a>Siehe auch
--------

[Entwurf von Fragebögen](design-questionnaires.md)

[Verwenden von Fragebögen](questionnaires.md)

[Verteilen und Abschließen von Fragebögen](distribute-questionnaires.md)


