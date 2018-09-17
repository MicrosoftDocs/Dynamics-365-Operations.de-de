--- 
title: Eine Anlage splitten
description: In dieser Aufgabenanleitung wird ein Prozentanteil eines Anlagenbuches zu einem neuen Anlagenbuch aufgeteilt.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="split-a-fixed-asset"></a>Eine Anlage splitten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dieser Aufgabenanleitung wird ein Prozentanteil eines Anlagenbuches zu einem neuen Anlagenbuch aufgeteilt.  Dabei werden die "Buchhalterrolle" und die USMF-Demodaten verwendet.


## <a name="create-a-new-fixed-asset"></a>Neue Anlage erstellen
1. Wechseln Sie zu Anlagen > Anlagen > Anlagen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Anlagengruppe" einen Wert ein oder wählen Sie einen Wert aus.
4. Notieren Sie sich die Anlagennummer, die später im Teilungsprozess zu verwenden ist.
5. Geben Sie im Feld "Name" einen Wert ein.
6. Schließt das Formular.

## <a name="split-a-fixed-asset"></a>Eine Anlage splitten
1. Suchen Sie in der Liste die zu teilende Anlage und wählen Sie diese aus.
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
3. Klicken Sie auf Bücher.
    * Wählen Sie das Buch aus, um die neue Anlage aufzuteilen.  
4. Klicken Sie auf Funktionen.
5. Klicken Sie auf "Anlage aufteilen".
6. Geben Sie im Feld "Zielanlage" einen Wert ein oder wählen Sie einen Wert aus.
7. Klicken Sie im Feld An Buch auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Geben Sie im Feld "Transaktionsdatum" ein Datum ein.
9. Geben Sie im Feld "Prozent" eine Zahl ein.
10. Geben Sie im Feld 'Journal' einen Wert ein, oder wählen Sie einen Wert aus.
11. Klicken Sie auf "OK".

## <a name="post-the-journal-transaction"></a>Die Erfassungstransaktion buchen
1. Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".
2. Wählen Sie in der Liste die Erfassung aus, die mit dem Teilungsprozess erstellt wurde.
3. Klicken Sie auf "Positionen".
    * Überprüfen Sie die erstellten Erfassungspositionen.  Eine "Anschaffungsänderungstransaktion" wird für die ursprüngliche Anlage erstellt, um den Wert um den Prozentsatz zu verringern, der im Teilungsprozess angegeben wird.  Eine "Anschaffungstransaktion" wird für die neue Anlage für denselben Betrag erstellt.  
4. Klicken Sie auf "Buchen".


