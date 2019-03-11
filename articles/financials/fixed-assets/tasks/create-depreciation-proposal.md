---
title: Abschreibungsvorschlag erstellen
description: In dieser Prozedur wird beschrieben, wie Abschreibungschargenvorschläge funktionieren und erläutert, wie Abschreibung für Anlagen vorgeschlagen wird.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "361290"
---
# <a name="create-depreciation-proposal"></a>Abschreibungsvorschlag erstellen

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

