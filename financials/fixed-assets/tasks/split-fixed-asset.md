--- 
title: Eine Anlage splitten
description: In dieser Aufgabenanleitung wird ein Prozentanteil eines Anlagenbuches zu einem neuen Anlagenbuch aufgeteilt.
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5aea1aab9f6b084bd0c5bd2119639bff3555bb8a
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="split-a-fixed-asset"></a>Eine Anlage splitten

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


