---
title: Eine Frage mit vordefinierten Antworten erstellen
description: Fragen mit vordefinierten Antworten ermöglichen die Angabe von Optionen, aus denen der Befragte auswählen kann.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3b90bb2a4981f32feb10ee1192e9c4d2e604e7a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071476"
---
# <a name="create-a-closed-ended-question"></a>Eine Frage mit vordefinierten Antworten erstellen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Fragen mit vordefinierten Antworten ermöglichen die Angabe von Optionen, aus denen der Befragte auswählen kann. Zunächst müssen Sie die Antwortgruppe mit den Antworten erstellen, dann erstellen Sie die Frage, die die Antwortgruppe verwendet. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-an-answer-group"></a>Erstellen einer Antwortgruppe
1. Gehen Sie zu **Fragebogen** > **Entwurf** > **Antwortgruppen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Antwortgruppe** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
    * Verwenden Sie die Funktion **Randomisieren**, um die Antworten jedes Mal, wenn die Antwortgruppe für eine Frage verwendet wird, nach dem Zufallsprinzip in eine andere Reihenfolge zu bringen.  
5. Klicken Sie auf **Antwort**.
6. Klicken Sie auf **Neu**.
    * Die Sequenznummer steuert die Reihenfolge, in der die Antworten angezeigt werden, es sei denn, **Zufällig** ist für die **Antwortgruppe** ausgewählt.  
    * Punkte können zu den Antworten für den Fragebogen vergeben werden.  
7. Geben Sie im Feld **Punkte** eine Zahl ein.
    * Die richtige Antwort kann markiert werden, um anzugeben, dass die ausgewählte Antwort richtig ist. Dies kann auch für die Punktzahl im Fragebogen verwendet werden.  
8. Geben Sie im Feld **Antwort** einen Wert ein.
    * Fahren Sie fort, Antwortauswahloptionen für die Antwortgruppe zu erstellen.  
9. Klicken Sie auf **Neu**.
10. Geben Sie im Feld **Punkte** eine Zahl ein.
11. Geben Sie im Feld **Antwort** einen Wert ein.
12. Klicken Sie auf **Neu**.
13. Geben Sie im Feld **Punkte** eine Zahl ein.
14. Geben Sie im Feld **Antwort** einen Wert ein.
15. Klicken Sie auf **Neu**.
16. Geben Sie im Feld **Punkte** eine Zahl ein.
17. Geben Sie im Feld **Antwort** einen Wert ein.
18. Klicken Sie auf **Neu**.
19. Geben Sie im Feld **Punkte** eine Zahl ein.
20. Geben Sie im Feld **Antwort** einen Wert ein.
21. Schließen Sie die Seite.
22. Schließen Sie die Seite.

## <a name="create-the-question"></a>Frage erstellen
1. Gehen Sie zu **Fragebogen** > **Entwerfen** > **Fragen**.
2. Klicken Sie auf **Neu**.
3. Verwenden Sie das Feld **Typ**, um verwandte Fragen zusammenzufassen.
    * Sie können die Eingabetypen **Kontrollkästchen**, **Alternative Schaltfläche** oder **Kombinationsfeld** für geschlossene Fragen verwenden.  
4. Wählen Sie im Feld **Eingabetyp** eine Option aus.
5. Geben Sie im Feld **Antwortgruppe** einen Wert ein oder wählen Sie einen Wert aus.
6. Geben Sie im Feld **Text** einen Wert ein.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
