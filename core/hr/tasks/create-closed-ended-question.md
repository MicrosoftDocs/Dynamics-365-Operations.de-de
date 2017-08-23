--- 
title: Eine Frage mit vordefinierten Antworten erstellen
description: "Fragen mit vordefinierten Antworten ermöglichen die Angabe von Optionen, aus denen der Befragte auswählen kann."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 71b2a2da0b705b84f79adcff25672855e7b5253f
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-closed-ended-question"></a>Eine Frage mit vordefinierten Antworten erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Fragen mit vordefinierten Antworten ermöglichen die Angabe von Optionen, aus denen der Befragte auswählen kann. Zunächst müssen Sie die Antwortgruppe mit den Antworten erstellen, dann erstellen Sie die Frage, die die Antwortgruppe verwendet. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-an-answer-group"></a>Erstellen einer Antwortgruppe
1. Wechseln Sie zu "Fragebogen" > "Entwurf" > "Antwortgruppen"
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Antwortgruppe" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Verwenden Sie die Randomisierungsfunktionen, um die Antworten bei jeder Verwendung der Antwortgruppe für eine Frage zufällig in einen anderen Reihenfolge anzuordnen.  
5. Klicken Sie auf "Antwort".
6. Klicken Sie auf "Neu".
    * "Sequenznummer" steuert die Reihenfolge, in der die Antworten angezeigt werden, es sei denn, "Zufällig festlegen" wird für die Antwortgruppe ausgewählt.  
    * Punkte können zu den Antworten für den Fragebogen vergeben werden.  
7. Geben Sie im Feld "Punkte" eine Zahl ein.
    * Die richtige Antwort kann markiert werden, um anzugeben, dass die ausgewählte Antwort richtig ist. Dies kann auch für die Punktzahl im Fragebogen verwendet werden.  
8. Geben Sie im Feld "Antwort" einen Wert ein.
    * Fahren Sie fort, Antwortauswahloptionen für die Antwortgruppe zu erstellen.  
9. Klicken Sie auf "Neu".
10. Geben Sie im Feld "Punkte" eine Zahl ein.
11. Geben Sie im Feld "Antwort" einen Wert ein.
12. Klicken Sie auf Neu.
13. Geben Sie im Feld "Punkte" eine Zahl ein.
14. Geben Sie im Feld "Antwort" einen Wert ein.
15. Klicken Sie auf Neu.
16. Geben Sie im Feld "Punkte" eine Zahl ein.
17. Geben Sie im Feld "Antwort" einen Wert ein.
18. Klicken Sie auf Neu.
19. Geben Sie im Feld "Punkte" eine Zahl ein.
20. Geben Sie im Feld "Antwort" einen Wert ein.
21. Schließen Sie die Seite.
22. Schließen Sie die Seite.

## <a name="create-the-question"></a>Frage erstellen
1. Wechseln Sie zu "Fragebogen" > "Entwerfen" > "Fragen".
2. Klicken Sie auf "Neu".
3. Verwenden Sie das Feld "Typ", um zusammenhängende Fragen zu gruppieren.
    * Sie können Kontrollkästchen, alternative Schaltflächen oder Kombinationsfelder für Fragen mit vordefinierten Antworten als Eingabetypen verwenden.  
4. Wählen Sie im Feld "Eingabetyp" eine Option aus.
5. Geben Sie im Feld "Antwortgruppe" einen Wert ein oder wählen Sie einen Wert aus.
6. Geben Sie im Feld "Text" einen Wert ein.

