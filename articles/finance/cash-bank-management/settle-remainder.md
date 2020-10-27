---
title: Rest ausgleichen
description: Sie können den Ausgleich über die noch zu bezahlenden Betragsaktivität ausgleichen, indem Sie den Betrag einem Sachkonto zuweisen.
author: mikefalkner
manager: aolson
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 52b0b456a6d9879c480ac3f076a32e382426a89c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977790"
---
# <a name="settle-remainder"></a>Rest ausgleichen

[!include [banner](../includes/banner.md)]

Sie können den Ausgleich über die noch zu bezahlenden Betragsaktivität ausgleichen, indem Sie den Betrag einem Sachkonto oder einem anderen Debitor zuweisen. Sie können die verbleibenden Beträge ausgleichen, wenn Sie die Beträge ausgleichen, die in einer Erfassung eingegeben wurden, oder wenn Sie nur offene Buchungen ausgleichen.

## <a name="setting-up-defaults"></a>Benutzerstandards ausgleichen 
Sie müssen die Restfunktion aktivieren und die Standardeinstellungen einrichten, bevor Sie Restbetra ausgleichen verwenden

1)  Klicken Sie auf **Debitor > Parameter > Ausgleiche** oder **Kreditor > Parameter > Ausgleiche**
2)  Wählen Sie die Registerkarte **Ausgleich** aus und klicken **Aktivieren Sie Rest ausgleichen**
3)  Wählen Sie unter **Standardursachencode** einen Standardursachencode aus. Die Ursachencodes müssen unter **Debitor > Einrichtung > Debitorentilgungsursachencodes** oder **Kreditor > Einrichtung > Debitorentilgungsursachencodes** bereits eingerichtet worden sein. Der **Standardbank-Restkonto** wird als Standard dem Konto zum Tilgungsursachencode zugewiesen.
3)  Aktualisieren Sie den Bericht **Standardbank-Restkonto** nach Bedarf.
4)  Wählen Sie in **Standardjournal** eine Zahlungserfassung aus, die verwendet wird, wenn Sie eine Zahlungserfassung erstellen möchten wenn Sie nur vereinbarende offene Buchungen ausgleichen möchten. Wenn Sie die Bankrestfunktion aktivieren, müssen Sie ein Standardjournal hinzufügen.

## <a name="settle-remainder-from-a-journal"></a>Restschuld einer Erfassung ausgleichen
Wenn Sie die Funktion **Restschuld begleichen** nicht aktivieren, können Sie keine Buchung in eine Erfassung eingeben noch diese anschließen und Transaktionen ausgleichen, wie Sie es in der Vergangenheit vorgenommen haben. Wenn Sie auf die Schaltfläche **OK** klicken, wechselt der offene Saldo auf der Rechnung und wird um den Bargeldbetrag verringert. Wenn das Bargeld die Rechnung nicht vollständig ausgleicht, bleibt die Rechnung mit dem Restsaldo bis zur Bezahlung offen.

Wenn die Funktion **Saldo begleichen** aktiviert ist, können Sie den Restbetrag mit einem Sachkonto ausgleichen. Sie können den verbleibenden Saldo auf ein anderes Debitorenkonto (für Debitorenbuchungen) oder auch ein anderes Kreditorenkonto (für Kreditorenbuchungen) übertragen, anstatt die Rechnungen offen zu lassen. 

Um den Rest von der Seite **Ausgleich** ausgleichen, führen Sie die folgenden Schritte aus:

1)  Auf der Seite **Ausgleich** markieren Sie die Rechnungen oder die Buchungen, die Sie ausgleichen möchten.
2)  Klicken Sie auf die Schaltfläche **Rest ausgleichen**.
3)  Ein Dialogfeld wird zum Anzeigen geöffent und der Betrag wird angezeigt, der mit einem Sachkonto ausgegelichen wird, das Datum, das verwendet wird, um den Rest auszugleichen, den Standardursachencode von den Parametern und das Standardkonto von den Parametern. 
4)  Wählen Sie einen neuen Ausgleichsgrund aus, wenn Sie den Standardgrund ändern möchten. Das Verrechnungskonto wird geändert, das dem Ursachencode zugeordnet ist.
5)  Bearbeiten Sie das Verrechnungskonto, wenn Sie es ändern möchten.
6)  Wenn Sie Debitorenbuchungen ausgleichen und der Rest auf einen anderen Debitor verschoben werden soll, wählen Sie einen Debitor aus **Ausgleichen Rest anhand Debitorenkonto** aus. Wenn Sie Lieferantenbuchungen ausgleichen und der Rest auf einen anderen Lieferanten verschoben werden soll, wählen Sie einen Lieferanten aus **Ausgleichen Rest anhand Lieferantenkonto** aus.
6)  **Rest ausgleichen** anklicken.
7)  Die **Erfassung** mit dem Lizenzvertrag wird angezeigt. Eine zusätzliche Erfassungsposition wird der Erfassung das Bankrestbetrag als der Betrag und dem Ausgleichsrestkonto als Gegenkonto hinzugefügt. Wenn Sie einen Debitor oder Lieferant hinzufügen, sodass der Regulierungsbetrag zu einem anderen Debitor oder Lieferanten verschoben werden kann, ist eine weitere Position zur Erfassung hinzuzufügen, um den Ausgleichsbetrag zu diesem Debitor oder Kreditor zu verschieben.

Wenn Sie die Erfassung buchen, wird ein offener Posten vollständig ausgeglichen. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Rest ausgelichen, wenn Sie nur offene Transaktionen ausgleichen
Sie können auch den Rest ausgleichen, wenn Sie offene Transaktionen ohne Erfassung ausgleichen.

Um den Rest auszugleichen, führen Sie die folgenden Schritte aus:

1)  Auf der Seite **Ausgleich** markieren Sie die Rechnungen oder die Buchungen, die Sie ausgleichen möchten.
2)  **Rest ausgleichen** anklicken.
3)  Ein Dialogfeld wird zum Anzeigen geöffent und der Betrag wird angezeigt, der mit einem Sachkonto ausgegelichen wird, das Datum, das verwendet wird, um den Rest auszugleichen, den Standardursachencode von den Parametern und das Standardkonto von den Parametern. 
4)  Wählen Sie einen neuen Ausgleichsgrund aus, wenn Sie den Standardgrund ändern möchten. Das Verrechnungskonto wird geändert, das dem Ursachencode zugeordnet ist.
5)  Bearbeiten Sie das V**errechnungskonto**, wenn Sie es ändern möchten.
6)  Wenn Sie Debitorenbuchungen ausgleichen und der Rest auf einen anderen Debitor verschoben werden soll, wählen Sie einen Debitor aus **Ausgleichen Rest anhand Debitorenkonto** aus. Wenn Sie Lieferantenbuchungen ausgleichen und der Rest auf einen anderen Lieferanten verschoben werden soll, wählen Sie einen Lieferanten aus **Ausgleichen Rest anhand Lieferantenkonto** aus.
7)  Sie können auch eine Zahlungserfassung mit dem Ausgleichsrest auswählen oder ihn nur buchen ohne eine Erfassung zu erstellen. Wählen Sie **Ja** für **Bearbeiten in der Erfassung**, um eine Zahlungserfassung zu erstellen. Sie können die Zahlungserfassung weiter bearbeiten, die Sie erstellen.
8)  **Rest ausgleichen** anklicken. Wenn Sie sich entscheiden, eine Erfassung zu erstellen, wird die Schaltfläche zu **Erfassung erstellen** geändert. **Erfassung erstellen** anklicken.
9)  Wenn Sie eine Zahlungserfassung erstellt haben, wird die Erfassungsseite **Rest ausgleichen** geöffnet. Eine zusätzliche Erfassungsposition wird der Erfassung für den Ausgleich des Restbetrags mit dem als Ausgleichsrestkonto als Gegenkonto hinzugefügt. Wenn Sie einen Debitor oder Lieferant hinzufügen, sodass der Regulierungsbetrag zu einem anderen Debitor oder Lieferanten verschoben werden kann, ist eine weitere Position zur Erfassung hinzuzufügen, um den Ausgleichsbetrag zu diesem Debitor oder Kreditor zu verschieben.
