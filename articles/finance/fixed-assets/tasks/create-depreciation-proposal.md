---
title: Abschreibungsvorschlag erstellen
description: In diesem Artikel wird beschrieben, wie Abschreibungschargenvorschläge funktionieren, und es wird erläutert, wie Abschreibungen für Anlagen vorgeschlagen werden.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1f39a1412c6f96fe0a8261602a88a6a3c3cd6b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858495"
---
# <a name="create-a-depreciation-proposal"></a>Abschreibungsvorschlag erstellen

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Abschreibungschargenvorschläge funktionieren, und es wird erläutert, wie Abschreibungen für Anlagen vorgeschlagen werden. Bei dieser Aufgabe werden das Demo-Unternehmen USMF sowie die Buchhalterrolle verwendet.


## <a name="create-a-depreciation-proposal"></a>Abschreibungsvorschlag erstellen
1. Wechseln Sie im Navigationsbereich zu **Anlagen > Journaleinträge > Abschreibungsvorschlag erstellen**.
2. Wählen Sie im Feld **Name der Erfassung** eine Option in der Dropdownliste aus.
3. Geben Sie im Feld **Bis Datum** ein Datum ein.

    - Wählen Sie die Option **Abschreibung zusammenfassen** aus, um monatliche Abschreibungen in einer einzelnen Erfassungsposition zusammenzufassen.  
    - Ist also beispielsweise das Bis-Datum der 31. März 2015, kann der folgende Buchungstext generiert werden: Abschreibung seit 31. Januar 2015. Das Feld **Datum** in den vorgeschlagenen Erfassungspositionen wird dann auf den 31. März 2015 festgelegt.  
    - Der Abschreibungsvorschlag kann nach Anlage, Anlagengruppe oder nach anderen Kriterien mithilfe der Option **Filter** gefiltert werden.  
    - Wenn Sie das Formular **Anschaffungs- oder Abschreibungsvorschläge für Anlagen erstellen** verwenden, können Sie Abschreibung in Chargen vorschlagen. Dies wird für größere Vorschläge empfohlen, die mehr Systemressourcen verwenden werden. Wenn Sie die Chargenoption auswählen, können Sie weiterhin in diesem Zeitraum andere Aufgaben abschließen. Wenn Sie Abschreibung auf diese Weise vorschlagen, wird die Abschreibung für Wertmodelle für Anlagen berechnet.  

4. Wählen Sie **Erfassung erstellen** aus.

## <a name="review-depreciation-entries"></a>Abschreibungseinträge prüfen
1. Gehen Sie im Navigationsbereich zu **Module > Anlage > Journalbuchungen > Anlagenbuchhaltung**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Wählen Sie **Positionen** aus.
4. Wählen Sie **Buchen** aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
