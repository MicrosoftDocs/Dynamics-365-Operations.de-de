---
title: Kreditlimitanpassungen
description: In diesem Thema wird das Einrichten und Hinzufügen von Kreditlimitanpassungen erläutert.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d96f50db4379a44ad8f2b06725db654a27393f9
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734802"
---
# <a name="credit-limit-adjustments"></a>Kreditlimitanpassungen 

[!include [banner](../includes/banner.md)]

Mit Kreditlimitanpassungen können Kreditmanager die Kreditlimits und Ablaufdaten eines einzelnen Kunden, einer Kundengruppe oder aller Kunden über einen Buchungsprozess aktualisieren. Sie können Einträge zur Anpassung des Kreditlimits hinzufügen, um Kunden und Kundenkreditgruppen zu aktualisieren, oder Sie können sie zur Berechnung automatischer Kreditlimits verwenden. Die Einträge können dann überprüft, zur Genehmigung über einen Workflow gesendet und auf Debitorenkonten gebucht werden.

## <a name="set-up-credit-limit-adjustments"></a>Kreditlimitanpassungen einrichten

Sie können Einträge im Journal für die **Kreditlimitanpassung** auf der Seite **Kreditlimitanpassung** (**Kreditverwaltung \> Kreditlimitanpassungen \> Kreditlimitanpassungen**) erstellen.

1. Wählen Sie **Neu** aus. Es wird eine neue Gruppe von Einträgen mit einer Kreditlimitanpassungsnummer erstellt.
2. Wählen Sie die Art der Kreditlimitanpassung:

    - Wählen Sie **Kreditlimit**, um das Kreditlimit des Kunden zu ändern.
    - Wählen Sie **Temporäres Kreditlimit**, um ein temporäres Kreditlimit zu erstellen, anstatt das aktuelle Kreditlimit des Debitoren zu ändern. Temporäre Kreditlimits überschreiben das Kreditlimit eines Debitoren für einen definierten Zeitraum. Nach Ablauf dieser Frist wird das Kreditlimit des Debitoren erneut verwendet.
3. Geben Sie eine Beschreibung ein. 

Wenn das Kontrollkästchen **Gebucht** aktiviert ist, wurden die Kreditlimits angewendet. Das Feld **Genehmigungsstatus** gibt den Workflow-Status des Journals an. Ein Workflow ist optional.

### <a name="add-credit-limit-adjustments"></a>Kreditlimitanpassungen hinzufügen

Um Kreditlimitanpassungen manuell hinzuzufügen, wählen Sie **Positionen** aus und befolgen Sie dann diese Schritte.

1. Um eine Kreditlimitanpassung für einen Debitoren hinzuzufügen, verwenden Sie das Menü **Kundenanpassungen**. Um ein Kreditlimit für eine Debitorenkreditgruppe hinzuzufügen, wählen Sie **Anpassungen der Debitorenkreditgruppe**.
2. Geben Sie ein Debitorenkonto für das Rechnungsdebitorenkonto ein, das mit dem neuen Kreditlimit aktualisiert werden soll. Wenn Sie **Anpassungen der Kundenkreditgruppen** in Schritt 1 ausgewählt haben, geben Sie die Kundenkreditgruppe ein. Sie können nicht gleichzeitig ein Debitorenkonto und eine Debitorenkreditgruppen-ID in derselben Erfassungsposition eingeben.

    Das aktuelle Kreditlimit wird angezeigt und der Name wird automatisch angezeigt.

3. Geben Sie das neue Kreditlimit ein, das das aktuelle Kreditlimit ersetzen soll, wenn der Kreditlimiteintrag gebucht wird.
4. Geben Sie ein Datum ein, um das neue Ablaufdatum für das Kundenkreditlimit festzulegen. Sie müssen ein Ablaufdatum für das Kreditlimit eingeben, wenn Sie eine Anpassung für das Kreditlimit erstellen.

Das Feld **Genehmigungsstatus** gibt den Workflow-Status der Erfassungsposition an.

Wenn die Kreditlimitanpassungen automatisch generiert werden sollen, können Sie das Menü **Generieren** im Aktionsbereich verwenden.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Temporäre Kreditlimitanpassungen hinzufügen

Um temporäre Kreditlimitanpassungen manuell hinzuzufügen, befolgen Sie diese Schritte für die Erfassungspositionen.

1. Um eine Kreditlimitanpassung für einen Debitoren hinzuzufügen, verwenden Sie das Menü **Kundenanpassungen**. Um ein Kreditlimit für eine Debitorenkreditgruppe hinzuzufügen, wählen Sie **Anpassungen der Debitorenkreditgruppe**.
2. Geben Sie ein Debitorenkonto für das Rechnungsdebitorenkonto ein, das mit dem neuen Kreditlimit aktualisiert werden soll. Wenn Sie **Anpassungen der Kundenkreditgruppen** in Schritt 1 ausgewählt haben, geben Sie die Kundenkreditgruppe ein. Sie können nicht gleichzeitig ein Debitorenkonto und eine Debitorenkreditgruppen-ID in derselben Erfassungsposition eingeben.

    Wenn bereits ein aktives oder zukünftiges temporäres Kreditlimit vorhanden ist, werden für jedes temporäre Kreditlimit das aktuelle temporäre Kreditlimit und der aktuelle Zeitraum angezeigt. Der Name wird automatisch angezeigt.

3. Geben Sie das neue Kreditlimit ein, das das aktuelle Kreditlimit ersetzen soll.
4. In den Feldern **Neu ab Datum** und **Neu bis Datum** definieren Sie den Zeitraum, in dem das erweiterte Kreditlimit gültig ist. Sie müssen die Ablaufdaten für das Kreditlimit eingeben, wenn Sie ein Journal für die Kreditlimitanpassung erstellen.

Das Feld **Genehmigungsstatus** gibt den Workflow-Status der Erfassungsposition an.

## <a name="generate-credit-limit-adjustments"></a>Kreditlimitanpassungen generieren

Sie können Kreditlimits auch automatisch anpassen lassen. Wählen Sie im Aktivitätsbereich **Generieren** und wählen Sie dann eine der folgenden Optionen aus:

- Von einem vorhandenen Debitor
- Aus einer bestehenden Debitorenkreditgruppe
- Automatische Kreditlimits

### <a name="from-existing-customer"></a>Von einem vorhandenen Debitor

Sie können Erfassungspositionen von vorhandenen Debitoren erstellen. Wenn Sie **Generieren \> Von einem vorhandenen Debitor** auswählen, wird ein Dialogfeld angezeigt, in dem Sie Kriterien zur Auswahl von Debitoren und zur Berechnung der neuen Grenzwerte angeben können.

1. Geben Sie einen Anpassungswert ein, um einen Betrag zum Kreditlimit hinzuzufügen oder von diesem abzuziehen. Geben Sie einen negativen Wert ein, um das aktuelle Kreditlimit zu verringern, oder einen positiven Wert, um es zu erhöhen.
2. Wählen Sie im Feld **Werttyp** aus, wie der in Schritt 1 eingegebene Wert zur Berechnung des neuen Kreditlimits verwendet werden soll:

    - Wählen Sie **Fester Wert**, um das Kreditlimit um einen Betrag zu ändern.
    - Wählen Sie **Prozentsatz**, um das Kreditlimit um einen Prozentsatz zu ändern.

3. Geben Sie einen Wert ein, mit dem das berechnete Kreditlimit gerundet wird. Geben Sie beispielsweise **10.00** ein, um das Kreditlimit auf die nächsten 10,00 Währungseinheiten zu runden.
4. Konfigurieren Sie das Feld **Rundungsform**, um anzugeben, ob der Rest auf- oder abgerundet werden soll.
5. Wählen Sie die Methode, die für die Datumsanpassung verwendet werden soll.

    - Wenn Sie **Absolut** auswählen, können Sie Daten eingeben, die den Zeitraum für die Kreditlimits definieren.
    - Wenn Sie **Relativ** auswählen, können Sie Versatzdaten für den Bereich eingeben. Der aktuelle Datumsbereich für das Kreditlimit wird um den Offset angepasst.

6. Verwenden Sie das Inforegister **Einzuschließende Datensätze**, um die Liste der enthaltenen Kunden zu filtern. Wenn Sie keine Filter einbeziehen, werden für alle Kunden Kreditlimiteinträge generiert.
7. Wählen Sie **OK**, um Einträge zur Anpassung des Kreditlimits zu erstellen.

### <a name="from-existing-customer-credit-group"></a>Aus einer bestehenden Debitorenkreditgruppe

Sie können Erfassungspositionen von vorhandenen Debitorenkreditgruppen erstellen. Wenn Sie **Generieren \> Aus einer bestehenden Debitorenkreditgruppe** auswählen, wird ein Dialogfeld angezeigt, in dem Sie Kriterien zur Auswahl von Debitorenkreditgruppen und zur Berechnung der neuen Grenzwerte angeben können. Die Kriterien sind dieselben, die zum Erstellen von Erfassungspositionen von vorhandenen Debitoren verwendet werden. Siehe die Schritte im vorherigen Abschnitt.

### <a name="automatic-credit-limits"></a>Automatische Kreditlimits

Sie können automatische Kreditlimits erstellen, um Debitorenkreditlimits zu definieren und zu aktualisieren. Die automatischen Kreditlimits werden für eine Risikogruppe erstellt und basieren auf bestimmten Werten, die in den Bewertungsgruppen verwendet werden. Mit diesen automatischen Kreditlimits können Sie Kreditlimiteinträge generieren. Wenn ein Debitor einer bestimmten Risikogruppe zugeordnet wurde und die Kreditinformationen des Debitors den Kriterien für ein automatisches Kreditlimit entsprechen, wird ein Eintrag zur Anpassung des Kreditlimits erstellt.

#### <a name="create-automatic-credit-limits"></a>Automatische Kreditlimits erstellen

Sie erstellen automatische Kreditlimits mithilfe von Kreditlimitanpassungen. Wenn Sie **Generieren \> Automatische Kreditlimits** auswählen, erscheint ein Dialogfeld, in dem Sie ein Ablaufdatum für die neuen Kreditlimits festlegen können, die basierend auf den Risikogruppen erstellt werden, denen Kunden zugewiesen sind. Wenn Sie fertig sind, wählen Sie **OK**, um die Kreditlimitanpassungspositionen zu erstellen.

### <a name="post-adjustments"></a>Regulierungen buchen

Nachdem Sie Kreditlimitanpassungspositionen erstellt haben, können Sie die Schaltfläche **Buchen** verwenden, um die Einträge zu buchen und die Debitorenkreditlimits zu aktualisieren. Wenn Sie jedoch einen Workflow eingerichtet haben, müssen Sie **Workflow \> Übermitteln** im Aktionsbereich auswählen, um die Erfassung zur Genehmigung zu übermitteln.

### <a name="credit-limit-adjustments-workflows"></a>Workflows Kreditlimitanpassungen

Die Workflows **Kreditlimitanpassungen** können verwendet werden, um Kreditlimitanpassungen über einen Workflow-Genehmigungsprozess zu senden. Sie können zwei Workflows auf der Seite **Kreditmanagement-Workflow** erstellen (**Kreditmanagement \> Einstellungen \> Kreditmanagement-Workflow**):

- **Kreditlimitanpassungen** – Mit diesem Workflow können Einträge auf Kopfebene genehmigt werden.
- **Kreditlimitanpassungsposition** – Dieser Workflow kann zur Genehmigung der Regulierungseinträge verwendet werden, sodass die Einträge von verschiedenen Personen genehmigt werden können, basierend auf den Kriterien im Workflow.

> [!NOTE]
> Wenn Sie den Workflow **Kreditlimitanpassungen** erstellen, können Sie ihn so einrichten, dass die Regulierungen automatisch gebucht werden, nachdem die Positionen genehmigt wurden. Fügen Sie einfach die Aufgabe **Erfassung automatisch buchen** im Workflow hinzu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
