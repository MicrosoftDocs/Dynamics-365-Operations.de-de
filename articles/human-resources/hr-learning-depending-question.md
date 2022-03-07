---
title: Eine Frage stellen, die von der Antwort auf die vorherige Frage abhängt
description: Bedingte Fragen bieten die Möglichkeit, basierend auf der vorhergehenden Antwort anzugeben, welche nachfolgende Frage einem Befragungsteilnehmer angezeigt wird.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f28f75a902121f23c92a919b539517dbdb191447
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066724"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Eine Frage stellen, die von der Antwort auf die vorherige Frage abhängt


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bedingte Fragen bieten die Möglichkeit, basierend auf der vorhergehenden Antwort anzugeben, welche nachfolgende Frage einem Befragungsteilnehmer angezeigt wird. Wenn Sie zum Beispiel "Bevorzugen Sie Kaffee oder Tee?" fragen, kann eine logische nachfolgende Frage abhängig davon ermittelt werden, ob der Befragte Kaffee oder Tee als Antwort auswählt. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="find-the-existing-questionnaire"></a>Durchsuchen des vorhandenen Fragebogens
1. Gehen Sie zu **Fragebogen** > **Entwerfen** > **Fragebögen**.
2. Wählen Sie den WorkFH-Fragebogen in der Liste aus.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Alle Fragen und Unterfragen zum Fragebogen hinzufügen
1. Klicken Sie auf **Fragen**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie im Feld **Frage** die Fragenummer 00016 aus.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf **Speichern**.
7. Schließen Sie die Seite.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Legen Sie die Fragebogensequenz auf "Bedingt" fest und machen Sie die Frage abhängig von der entsprechenden Frage
1. Klicken Sie auf **Bearbeiten**.
2. Erweitern Sie den Abschnitt **Einrichtung**.
3. Wählen Sie im Feld **Reihenfolge Fragen** „Bedingt“ aus.
4. Klicken Sie auf **Bedingte** Frage.
5. Wählen Sie in der Struktur "Fragen\Erläutern Sie, warum Sie die vorherige Frage so beantwortet haben?" aus.
6. Wählen Sie im Feld **Primäre Frage** die Frage 00009 aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Geben Sie im Feld **Antwort** die Antwortsequenzkennung der Antwortoption ein, von der die Frage abhängig sein soll. Geben Sie beispielsweise 1 für die erste Antwortoption ein.
9. Klicken Sie auf **Speichern**.
10. Wählen Sie in der Struktur "Fragen\Ich werde angemessen für meine Arbeit bezahlt" aus.
    * Beachten Sie, dass die Fragenstruktur aktualisiert wird, sodass die Abhängigkeit angezeigt wird.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
