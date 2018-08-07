--- 
title: Einen Abschreibungsvorschlag erstellen
description: "In dieser Prozedur wird beschrieben, wie Abschreibungschargenvorschläge funktionieren und erläutert, wie Abschreibung für Anlagen vorgeschlagen wird."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07d8cf2f1c46b99dfcd1d7c3419fe835f37c5a02
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-depreciation-proposal"></a>Einen Abschreibungsvorschlag erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dieser Prozedur wird beschrieben, wie Abschreibungschargenvorschläge funktionieren und erläutert, wie Abschreibung für Anlagen vorgeschlagen wird. Bei dieser Aufgabe werden das Demo-Unternehmen USMF sowie die Buchhalterrolle verwendet.


## <a name="create-depreciation-proposal"></a>Abschreibungsvorschlag erstellen
1. Wechseln Sie zu "Anlagen" > "Erfassungseinträge" > "Abschreibungsvorschlag" erstellen.
2. Klicken Sie im Feld "Erfassungsname" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Geben Sie in das Feld "Bis Datum" ein Datum ein.
    * Wählen Sie die Option "Abschreibung zusammenfassen" aus, um monatliche Abschreibungen in einer einzelnen Erfassungsposition zusammenzufassen.  
    * Ist also beispielsweise das Bis-Datum der 31. März 2015 ist, kann der folgende Buchungstext generiert werden: "Abschreibung seit 31. Januar 2015." Das Feld Datum in den vorgeschlagenen Erfassungspositionen wird dann auf den 31. März 2015 festgelegt.  
    * Der Abschreibungsvorschlag kann nach Anlage, Anlagengruppe oder nach anderen Kriterien mithilfe der Option "Filter" gefiltert werden.  
    * Wenn Sie das Formular "Anschaffungs- oder Abschreibungsvorschläge für Anlagen erstellen" verwenden, können Sie Abschreibung in Chargen vorschlagen. Dies wird für größere Vorschläge empfohlen, die mehr Systemressourcen verwenden werden. Wenn Sie die Chargenoption auswählen, können Sie weiterhin in diesem Zeitraum andere Aufgaben abschließen. Wenn Sie Abschreibung auf diese Weise vorschlagen, wird die Abschreibung für Wertmodelle für Anlagen berechnet.  
5. Klicken Sie auf "Erfassung erstellen".

## <a name="review-depreciation-entries"></a>Abschreibungseinträge prüfen
1. Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie auf "Positionen".
4. Klicken Sie auf "Buchen".


