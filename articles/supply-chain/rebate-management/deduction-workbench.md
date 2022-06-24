---
title: Verwalten von Abzügen mit der Abzugsworkbench
description: In diesem Artikel wird beschrieben, wie die Abzugsworkbench verwendet wird, sodass Sie Debitorenzahlungen verarbeiten können, die Abzüge enthalten.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 607ad528b56d1f0c9a78e113f67c920cdae6e620
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873607"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Verwalten von Abzügen mit der Abzugsworkbench

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie die Abzugsworkbench verwendet wird, sodass Sie Debitorenzahlungen verarbeiten können, die Abzüge enthalten.

Ein Debitor, dem eine Rückvergütung geschuldet wird, kann sich entscheiden, nicht auf eine Rückvergütungsauszahlung zu warten. Stattdessen kann der Debitor eine Zahlung senden, die einen Abzug für den Betrag der Rückvergütung umfasst. Um diesen Typ von Buchung zu verarbeiten, können Sie die Abzugsworkbench verwenden, um Abzüge mit offenen Habenbuchungen abzugleichen, Abzüge aufzuteilen, Abzüge zu verweigern und Abzüge abzuschreiben.

> [!NOTE]
> Die Abzugsworkbench war lange Zeit Teil der Vertriebs- und Marketingfunktionalität in Microsoft Dynamics 365 Supply Chain Management. Sie wurde jedoch jetzt so erweitert, dass sie auch mit dem neueren Modul **Rückvergütungsverwaltung** funktioniert. In diesem Artikel wird beschrieben, wie Sie sowohl ältere Funktionen als auch die Rückvergütungsverwaltungsfunktionen der Abzugsworkbench verwenden. Wenn Sie jedoch [das Modul **Rückvergütungsverwaltung** noch nicht für Ihr System](rebate-management-enable.md) aktiviert haben, stehen Ihnen einige der hier beschriebenen Funktionen nicht zur Verfügung.

## <a name="prerequisites"></a>Voraussetzungen

### <a name="set-up-the-old-deduction-management-system"></a>Das alte Abzugsmanagementsystem einrichten

Sie können die Abzugsworkbench zusammen mit den alten Abzugsverwaltungsfunktionen von Supply Chain Management verwenden, auch wenn Sie das Modul **Rückvergütungsverwaltung** nicht nutzen. Sie müssen Ihr System jedoch zunächst wie in diesem Abschnitt beschrieben vorbereiten.

Bevor Sie die Abzugsworkbench verwenden können, müssen Sie die Einrichtungsaufgaben ausführen, die in [Abzugsverwaltung einrichten](/dynamicsax-2012/appuser-itpro/set-up-deduction-management) beschrieben werden. Sie sollten auch einen Typ von Rückvergütungsvereinbarungen für den Debitor eingerichtet haben: entweder eine Debitorenrückvergütung, wie in [Einrichten und Verwalten von Debitorenrückvergütungen](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates) beschrieben, oder eine Handelsvergütungsrückvergütung.

Wenn Sie einen Abzug auf eine Debitorenrückvergütung anwenden, müssen Sie die folgenden Aufgaben ausführen:

- [Ihre Debitorenrückvergütungen einrichten](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Genehmigen und bearbeiten Sie die Rückvergütung, damit Sie die Abzugsworkbench verwenden können.

Wenn Sie einen Abzug auf eine Handelsvergütungsrückvergütung anwenden, müssen Sie die folgenden Aufgaben ausführen:

- Richten Sie Rückverrechnungsrückvergütungen ein.
- Wenden Sie Rückverrechnungsrückvergütungen an.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Debitorenkonten und Abzüge konfigurieren

Das System zeichnet alle Abzugsereignisse in einem Anspruchsjournal auf. Daher muss Ihr System ein Journal enthalten, das für diesen Zweck verwendet werden kann. Wenn Sie noch kein Anspruchsjournal haben, richten Sie es jetzt ein. Dieses Journal wird benötigt, um Abzüge direkt in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite zu erstellen.

Um eine Regel für ein neues Erfassungsjournal für Abzüge einzurichten, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Hauptbuch \> Erfassungseinstellungen \> Journale**.
1. Wählen Sie **Neu** und legen Sie die folgenden Felder für den neuen Journalnamen fest:

    - **Name**: Geben Sie hier einen eindeutigen Namen für das Anspruchsjournal ein.
    - **Beschreibung**: Geben Sie eine kurze Beschreibung des neuen Journals ein.
    - **Journaltyp**: Wählen Sie *Täglich* aus.
    - **Belegnummern**: Weisen Sie einen vorhandenen Nummernkreis zu. Alternativ können Sie einen neuen Nummernkreis mit dem Geltungsbereich Unternehmen erstellen und ihn dem neuen Journalnamen zuweisen.

1. Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.
1. Auf der Registerkarte **Abzüge** gehen Sie auf das Inforegister **Allgemein**, stellen Sie das Feld **Anspruchsjournalname** auf den gerade erstellten Journalnamen ein.
1. Auf dem Inforegister **Rücklieferung** setzen Sie die folgenden Felder fest:

    - **Rücklieferung erstellen**: Legen Sie in dieser Option fest,, was das System tun soll, wenn eine mengenbasierte Rücklieferung genehmigt wird:

        - *Ja*: Eine Rücklieferung wird erstellt.
        - *Nein*: Ein negativer Auftrag wird erstellt.

    - **Ohne zugeordnete Rechnung erstellen**: Wählen Sie einen Wert aus, der angibt, was das System tun soll, wenn ein mengenbasierter Anspruch genehmigt wird, aber keine Rechnung zugeordnet ist:

        - *Akzeptieren*: Rücklieferung wird erstellt.
        - *Warnung*: Eine Rücklieferung wird erstellt, aber es wird die folgende Warnmeldung angezeigt: „Anspruch ist keiner Rechnung zugeordnet.“
        - *Fehler*: Es wird keine Rücklieferung erstellt und die folgende Fehlermeldung angezeigt: „Anspruch ist keiner Rechnung zugeordnet. Die Aktualisierung wurde abgebrochen.“

    - **Rücklieferung vor Abzugsgenehmigung erstellen**: Setzen Sie diese Option auf *Ja*, wenn Rücklieferungen erstellt werden können, bevor die Rücklieferung genehmigt wird. Diese Einstellung gilt nur für mengenbezogene Ansprüche, bei denen die Option **Rücklieferung erstellen** auf *Ja* gestellt ist.

### <a name="configure-general-ledger-parameters"></a>Hauptbuchparameter konfigurieren

Wenn das System ein Anspruchsjournal für einen neuen Abzug erstellt, erstellt es auch zwei neue Debitorentransaktionen: eine zum Verrechnen des Anspruchsbetrags mit der ursprünglichen Rechnung und eine zum Registrieren einer Debitorenschuld in Höhe des Anspruchs (da der Anspruch noch nicht genehmigt wurde). Daher müssen Sie Ihr System so einrichten, dass ein einzelner Beleg mehrere Debitorenpositionen haben kann.

Führen Sie die folgenden Schritte aus, um einem einzelnen Beleg mehrere Debitorenpositionen zuzuweisen.

1. Wechseln Sie zu **Hauptbuch \> Sachkonto-Einstellungen \> Hauptbuchparameter**.
1. Auf der Registerseite **Hauptbuch** gehen Sie zum Inforegister **Allgemein**, stellen Sie die Option **Mehrere Transaktionen innerhalb eines Belegs erlauben** auf *Ja*.
1. Wenn Sie eine Warnmeldung erhalten, wählen Sie **Schließen**, um die Änderung zu akzeptieren.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Abzugsgründe erstellen

Das System verlangt, dass Benutzer für jeden Abzug, den sie direkt in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite eingeben, einen Grund angeben. Der Grund bestimmt, wie der Abzug gehandhabt wird, wenn er genehmigt wird.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsgründe**.
1. Wählen Sie **Neu**, um dem Raster eine Zeile hinzuzufügen, und legen Sie dann die folgenden Felder dafür fest:

    - **Anspruchsursache**: Geben Sie hier einen eindeutigen Namen für die Ursache ein.
    - **Beschreibung**: Geben Sie eine Beschreibung des Grunds ein, um weitere Informationen zur Verwendung bereitzustellen.
    - **Anspruchsgrundlage**: Wählen Sie eine Anspruchsgrundlage für die Anspruchsursache:

        - *Preisbasiert*: Erstellen Sie bei der Genehmigung eine Freitextgutschrift.
        - *Mengenbasiert*: Legen Sie bei der Genehmigung einen negativen Auftrag oder eine Rücklieferung an.

    - **Ursachencode für Rückgabe**: Wählen Sie einen Ursachencode für die Rückgabe aus, der als Wert des **Ursachencodes für die Rückgabe** für die Rücklieferung gilt.
    - **Typ**: Wählen Sie einen Abzugstyp aus. Der Wert **Abzugsgegenkonto** für den ausgewählten Typ wird verwendet, um das Feld **Abzugsgegenkonto** festzulegen, wenn ein Abzug oder Anspruch erstellt wird. Abzugstypen sind auf der Seite **Abzugstypen** festgelegt (**Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugstypen**).
    - **Anspruchsbuchungskonto**: Dieses Feld ist nur verfügbar, wenn das Feld **Anspruchsgrundlage** auf *Preisbasiert* gesetzt ist. Wenn ein preisbasierter Anspruch genehmigt wird, ordnet das System das Sachkonto, das Sie hier auswählen, als Wert **Hauptkonto** für den Entwurf der Freitext-Gutschrift zu.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Die periodische Aufgabe „Genehmigte Abzüge ausgleichen“ einrichten

Für Abzüge, die durch die Verwendung des Befehls **Neuer Abzug** auf der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite erstellt wurden, können Sie die periodische Aufgabe *Genehmigte Abzüge ausgleichen* einrichten, um Abzüge und Gutschriften mit übereinstimmenden **Abzugskennung**-Werten und Beträgen automatisch auszugleichen.

Um diese Aufgabe zu planen, gehen Sie zu **Vertrieb und Marketing \> Periodische Aufgaben \> Genehmigte Abzüge ausgleichen** und richten Sie Optionen, Filter und einen Zeitplan ein, genau wie für andere Arten periodischer Aufgaben.

> [!NOTE]
> Wenn die Option **Automatischer Ausgleich** auf *Ja* auf der Registerkarte **Ausgleich** der Seite **Debitorenparameter** (**Debitoren \> Setup \> Debitorenparameter**) gesetzt ist, funktioniert die periodische Aufgabe *Genehmigte Abzüge ausgleichen* nicht, da das Guthaben automatisch ausgeglichen wird.

## <a name="create-a-deduction"></a>Einen Abzug erstellen

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Erstellen Sie einen Abzugsjournaleintrag, indem Sie das Debitorenzahlungsjournal verwenden

Gehen Sie folgendermaßen vor, um einen Journaleintrag zu erstellen:

1. Gehen Sie zu **Debitorenkonten \> Zahlungen \> Kundenzahlungserfassung**.
1. Wählen Sie **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. Im Feld **Name** für die neue Zeile wählen Sie den Namen des Journals aus.
1. Wählen Sie im Aktivitätsbereich **Positionen** aus.
1. Geben Sie das Datum, das Unternehmenskonto und die Debitorenkontonummer ein.
1. Wählen Sie im Feld **Rechnung** die Rechnung aus, der der Abzug zugeordnet ist.
1. Geben Sie im Feld **Gutschrift** den Betrag ein, den der Kunde gezahlt hat.
1. Wählen Sie **OK**, um zu bestätigen, dass der Betrag niedriger als die Summe der markierten Buchung ist.
1. Wählen Sie den Gegenkontotyp und das Gegenkonto aus.
1. Wählen Sie in der Symbolleiste über dem Raster **Abzüge**.
1. Wählen Sie auf der Seite **Abzug** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen. Das Feld **Abzugskennung** für die neue Zeile wird automatisch gesetzt.
1. Wählen Sie im Feld **Typ** den Abzugstyp.
1. Geben Sie im Feld **Betrag** den Betrag ein, der im Feld **Saldo** unter der Abzugsliste angezeigt ist. Dieser Betrag stellt den Betrag dar, den der Debitor von der Zahlung abgezogen hat.
1. Schließen Sie die Seite **Abzug**. Sie sind wieder auf der Seite **Debitorenzahlungen**, die nun eine neue Zeile für den Abzug anzeigt.
1. Wählen Sie im Aktivitätsbereich **Überprüfen \> Überprüfen** aus. Sie sollten die folgende Nachricht erhalten: „Journal ist OK.“
1. Wählen Sie im Aktionsbereich **Buchen** aus.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Einen Abzug mit der Abzugsworkbench erstellen

Um einen neuen Abzug in der Abzugsworkbench zu erstellen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Neuer Abzug** aus.

    Im Dialogfeld **Neuer Abzug** ist das Feld **Abzugskennung** basierend auf dem **Abzugskennung**-Nummernkreis festgelegt, der auf der Seite **Parameter der Handelsvergütungsverwaltung** definiert ist (**Vertrieb und Marketing \> Setup \> Handelsvergütungen \> Parameter der Handelsvergütungsverwaltung**).

1. Stellen Sie die folgenden Felder ein:

    - **Debitorenkonto**: Wählen Sie das Debitorenkonto aus, für das der Abzug gilt.
    - **Externe Anspruchsnummer**: Geben Sie die Anspruchsreferenz des Debitors ein.
    - **Anspruchsbetrag**: Geben Sie den Anspruchsbetrag inklusive Steuern ein. Der Wert muss positiv sein.
    - **Währung**: Wählen Sie die Währung für den Abzug. Der Standardwert ist die Währung, die für das ausgewählte Debitorenkonto eingestellt ist.
    - **Anspruchsgrundlage**: Wählen Sie die Anspruchsgrundlage. Die Anspruchsgrundlage bestimmt den Typ der Habenbuchung, die nach der Genehmigung des Abzugs oder des Anspruchs erstellt wird.

        - *Preisbasiert*: Es wird ein Entwurf einer Freitextrechnung erstellt.
        - *Mengenbasiert*: Ein negativer Auftrag oder eine Rücklieferung wird erstellt.

    - **Anspruchsdatum**: Wählen Sie das Datum des Anspruchs. Der aktuelle Wert ist das aktuelle Datum.
    - **Anspruchsursache**: Wählen Sie den Ursachencode aus, der für den aktuellen Abzug gilt. Die von Ihnen ausgewählte Anspruchsgrundlage wirkt sich darauf aus, welche Optionen gelten. Weitere Informationen zum Erstellen und Konfigurieren der hier zur Auswahl stehenden Anspruchsursachen finden Sie im Abschnitt [Abzugsgründe erstellen](#deduction-reasons) weiter oben in diesem Artikel.
    - **Hinweise**: Fügen Sie alle zutreffenden Hinweise hinzu. Wenn der Anspruch genehmigt wurde, kann die genehmigende Person die Hinweise des Anspruchs bearbeiten oder ergänzen.
    - **Anspruchsjournal erstellen**: Setzen Sie in dieser Option fest, ob das Anspruchsjournal erstellt werden soll, wenn der Anspruch oder Abzug erstellt wird:

        - *Ja*: Das System erstellt und veröffentlicht ein allgemeines Journal mithilfe des Anspruchsjournals, das auf der Seite **Debitorenparameter** eingerichtet ist. (Weitere Informationen finden Sie im Abschnitt [Debitoren und Abzüge konfigurieren](#accounts-receivable-deductions) weiter oben in diesem Artikel.) Wenn dem Anspruch eine Rechnung zugeordnet ist, wird das Anspruchsjournal verwendet, um den Saldo der entsprechenden Rechnung zu reduzieren. Wird der Anspruch später abgelehnt, werden das Anspruchsjournal und die Ausgleiche (sofern eine Rechnung zugeordnet wurde) storniert.
        - *Nein*: Zu diesem Zeitpunkt wird kein Anspruchsjournal erstellt. Es wird erstellt, wenn der Anspruch genehmigt wurde. Eine Rechnung kann weiterhin dem neuen Anspruch zugeordnet werden, auch wenn kein Anspruchsjournal erstellt wird. Der Ausgleich kann jedoch nicht ohne das Anspruchsjournal erfolgen.

1. Wählen Sie **OK** aus.

    Ein neuer Abzug wird erstellt. Wenn Sie die Option **Anspruchsjournal erstellen** auf *Ja* gesetzt haben, werden folgende Transaktionen gebucht:

    - **Zwei neue Debitorentransaktionen**: Eine Transaktion gleicht den Anspruchsbetrag mit der Originalrechnung aus. Die andere Transaktion erfasst die Schuld eines Debitors in Höhe des Anspruchs, da der Anspruch noch nicht genehmigt wurde. Die ursprüngliche Rechnungstransaktion und die Gegentransaktion des Anspruchs werden automatisch zum Ausgleich vorgemerkt, wenn Sie die Rechnung zuordnen, indem Sie im Aktivititätsbereich **Verwalten \> Rechnung zuordnen**.
    - **Zwei Gegenbuchungen**: Diese Transaktionen werden auf dem Sachkonto **Abzugsgegenkonto** veröffentlicht.
    - **Anspruchsjournal**: Um das Anspruchsjournal für jeden Abzug anzuzeigen, der in der Abzugsworkbench angezeigt wird, wählen Sie die Registerkarte **Verweise**. Das Anspruchsjournal wird im Feld **Nummer der Stapelverarbeitserfassung** angezeigt. Sie können das Anspruchsjournal auch auf der Registerkarte **Abzugsereignisse** ansehen. Dort hat es als **Aktualisierungstyp** den Wert *Abgleichen*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Abzug aus einem Debitorenausgleich erstellen

Der Prozess des Erstellens eines Abzugs aus einem Debitorenausgleich ähnelt dem Prozess des Erstellens eines Abzugs über die Abzugsworkbench. Der Debitor und Rechnungswährung werden jedoch automatisch eingestellt und die Rechnung zugeordnet. Sie müssen im Aktivitätsbereich nicht **Verwalten \> Rechnung zuordnen** auswählen, wenn Sie einen Anspruch oder einen Abzug über die Debitorenausgleichsseite erstellen.

1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
1. Wählen Sie den Debitor aus, für das Sie einen Abzug erstellen möchten.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Mahnen** in der Gruppe **Ausgleichen** die Option **Transaktionen ausgleichen** aus.
1. Wählen Sie im Dialogfeld **Transaktionen ausgleichen** die Registerkarte **Übersicht** aus, wählen Sie die Rechnung aus, für die der Abzug erstellt werden soll.
1. Wählen Sie in der Symbolleiste **Abzüge \> Neuer Abzug** aus.

    Im Dialogfeld **Neuer Abzug** ist das Feld **Abzugskennung** basierend auf dem **Abzugskennung**-Nummernkreis festgelegt, der auf der Seite **Parameter der Handelsvergütungsverwaltung** definiert ist (**Vertrieb und Marketing \> Setup \> Handelsvergütungen \> Parameter der Handelsvergütungsverwaltung**). Das Feld **Debitorenkonto** wird auf das Debitorenkonto eingestellt, für das der Abzug gilt.

1. Stellen Sie die folgenden Felder ein:

    - **Externe Anspruchsnummer**: Geben Sie die Anspruchsreferenz des Debitors ein.
    - **Anspruchsbetrag**: Geben Sie den Anspruchsbetrag inklusive Steuern ein. Der Wert muss positiv sein.
    - **Währung**: Wählen Sie die Währung für den Abzug. Der Standardwert ist die Währung, die für das ausgewählte Debitorenkonto eingestellt ist.
    - **Anspruchsgrundlage**: Wählen Sie die Anspruchsgrundlage. Die Anspruchsgrundlage bestimmt den Typ der Habenbuchung, die nach der Genehmigung des Abzugs oder des Anspruchs erstellt wird.

        - *Preisbasiert*: Es wird ein Entwurf einer Freitextrechnung erstellt.
        - *Mengenbasiert*: Ein negativer Auftrag oder eine Rücklieferung wird erstellt.

    - **Anspruchsdatum**: Wählen Sie das Datum des Anspruchs. Der aktuelle Wert ist das aktuelle Datum.
    - **Anspruchsursache**: Wählen Sie den Ursachencode aus, der für den aktuellen Abzug gilt. Die von Ihnen ausgewählte Anspruchsgrundlage wirkt sich darauf aus, welche Optionen gelten. Weitere Informationen zum Erstellen und Konfigurieren der hier zur Auswahl stehenden Anspruchsursachen finden Sie im Abschnitt [Abzugsgründe erstellen](#deduction-reasons) weiter oben in diesem Artikel.
    - **Hinweise**: Fügen Sie alle zutreffenden Hinweise hinzu. Wenn der Anspruch genehmigt wurde, kann die genehmigende Person die Hinweise des Anspruchs bearbeiten oder ergänzen.
    - **Anspruchsjournal erstellen**: Setzen Sie in dieser Option fest, ob das Anspruchsjournal erstellt werden soll, wenn der Anspruch oder Abzug erstellt wird:

        - *Ja*: Das System erstellt und veröffentlicht ein allgemeines Journal mithilfe des Anspruchsjournals, das auf der Seite **Debitorenparameter** eingerichtet ist. (Weitere Informationen finden Sie im Abschnitt [Debitoren und Abzüge konfigurieren](#accounts-receivable-deductions) weiter oben in diesem Artikel.) Wenn dem Anspruch eine Rechnung zugeordnet ist, wird das Anspruchsjournal verwendet, um den Saldo der entsprechenden Rechnung zu reduzieren. Wird der Anspruch später abgelehnt, werden das Anspruchsjournal und die Ausgleiche (sofern eine Rechnung zugeordnet wurde) storniert.
        - *Nein*: Zu diesem Zeitpunkt wird kein Anspruchsjournal erstellt. Es wird erstellt, wenn der Anspruch genehmigt wurde. Eine Rechnung kann weiterhin dem neuen Anspruch zugeordnet werden, auch wenn kein Anspruchsjournal erstellt wird. Der Ausgleich kann jedoch nicht ohne das Anspruchsjournal erfolgen.

1. Wählen Sie **OK** aus.

    Ein neuer Abzug wird erstellt. Wenn Sie die Option **Anspruchsjournal erstellen** auf *Ja* gesetzt haben, werden folgende Transaktionen gebucht:

    - **Zwei neue Debitorentransaktionen**: Eine Transaktion gleicht den Anspruchsbetrag mit der Originalrechnung aus. Die andere Transaktion erfasst die Schuld eines Debitors in Höhe des Anspruchs, da der Anspruch noch nicht genehmigt wurde. Die ursprüngliche Rechnungstransaktion und die Gegentransaktion des Anspruchs werden automatisch zum Ausgleich vorgemerkt, wenn Sie die Rechnung zuordnen, indem Sie im Aktivititätsbereich **Verwalten \> Rechnung zuordnen**.
    - **Zwei Gegenbuchungen**: Diese Transaktionen werden auf dem Sachkonto **Abzugsgegenkonto** veröffentlicht.
    - **Anspruchsjournal**: Um das Anspruchsjournal für jeden Abzug anzuzeigen, der in der Abzugsworkbench angezeigt wird, wählen Sie die Registerkarte **Verweise**. Das Anspruchsjournal wird im Feld **Nummer der Stapelverarbeitserfassung** angezeigt. Sie können das Anspruchsjournal auch auf der Registerkarte **Abzugsereignisse** ansehen. Dort hat es als **Aktualisierungstyp** den Wert *Abgleichen*.

    Sie sind wieder auf der Seite **Transaktionen ausgleichen**, die nun die ausgewählte Rechnung als markiert anzeigt. Die Schaltfläche **Veröffentlichen** ist nur verfügbar, wenn Sie die Option **Anspruchsjournal erstellen** auf *Ja* steht. Wenn verfügbar, wählen Sie **Veröffentlichen**, um den Saldo auf der Rechnung um den **Anspruchsbetrag** zu reduzieren.

### <a name="create-a-deduction-from-a-customer-page"></a>Abzug aus einer Debitorenseite erstellen

Der Prozess des Erstellens eines Abzugs aus einer Debitorenseite ähnelt dem Prozess des Erstellens eines Abzugs über die Abzugsworkbench. Der Kunde wird jedoch automatisch eingestellt.

1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
1. Wählen Sie den Debitor aus, für das Sie einen Abzug erstellen möchten.
1. Klicken Sie alternativ im Aktivitätsbereich auf der Registerkarte **Mahnen** in der Gruppe **Abzüge** auf **Abzüge erstellen**.

    Im Dialogfeld **Neuer Abzug** ist das Feld **Abzugskennung** basierend auf dem **Abzugskennung**-Nummernkreis festgelegt, der auf der Seite **Parameter der Handelsvergütungsverwaltung** definiert ist (**Vertrieb und Marketing \> Setup \> Handelsvergütungen \> Parameter der Handelsvergütungsverwaltung**). Das Feld **Debitorenkonto** wird auf das Debitorenkonto eingestellt, für das der Abzug gilt.

1. Stellen Sie die folgenden Felder ein:

    - **Externe Anspruchsnummer**: Geben Sie die Anspruchsreferenz des Debitors ein.
    - **Anspruchsbetrag**: Geben Sie den Anspruchsbetrag inklusive Steuern ein. Der Wert muss positiv sein.
    - **Währung**: Wählen Sie die Währung für den Abzug. Der Standardwert ist die Währung, die für das ausgewählte Debitorenkonto eingestellt ist.
    - **Anspruchsgrundlage**: Wählen Sie die Anspruchsgrundlage. Die Anspruchsgrundlage bestimmt den Typ der Habenbuchung, die nach der Genehmigung des Abzugs oder des Anspruchs erstellt wird.

        - *Preisbasiert*: Es wird ein Entwurf einer Freitextrechnung erstellt.
        - *Mengenbasiert*: Ein negativer Auftrag oder eine Rücklieferung wird erstellt.

    - **Anspruchsdatum**: Wählen Sie das Datum des Anspruchs. Der aktuelle Wert ist das aktuelle Datum.
    - **Anspruchsursache**: Wählen Sie den Ursachencode aus, der für den aktuellen Abzug gilt. Die von Ihnen ausgewählte Anspruchsgrundlage wirkt sich darauf aus, welche Optionen gelten. Weitere Informationen zum Erstellen und Konfigurieren der hier zur Auswahl stehenden Anspruchsursachen finden Sie im Abschnitt [Abzugsgründe erstellen](#deduction-reasons) weiter oben in diesem Artikel.
    - **Hinweise**: Fügen Sie alle zutreffenden Hinweise hinzu. Wenn der Anspruch genehmigt wurde, kann die genehmigende Person die Hinweise des Anspruchs bearbeiten oder ergänzen.
    - **Anspruchsjournal erstellen**: Setzen Sie in dieser Option fest, ob das Anspruchsjournal erstellt werden soll, wenn der Anspruch oder Abzug erstellt wird:

        - *Ja*: Das System erstellt und veröffentlicht ein allgemeines Journal mithilfe des Anspruchsjournals, das auf der Seite **Debitorenparameter** eingerichtet ist. (Weitere Informationen finden Sie im Abschnitt [Debitoren und Abzüge konfigurieren](#accounts-receivable-deductions) weiter oben in diesem Artikel.) Wenn dem Anspruch eine Rechnung zugeordnet ist, wird das Anspruchsjournal verwendet, um den Saldo der entsprechenden Rechnung zu reduzieren. Wird der Anspruch später abgelehnt, werden das Anspruchsjournal und die Ausgleiche (sofern eine Rechnung zugeordnet wurde) storniert.
        - *Nein*: Zu diesem Zeitpunkt wird kein Anspruchsjournal erstellt. Es wird erstellt, wenn der Anspruch genehmigt wurde. Eine Rechnung kann weiterhin dem neuen Anspruch zugeordnet werden, auch wenn kein Anspruchsjournal erstellt wird. Der Ausgleich kann jedoch nicht ohne das Anspruchsjournal erfolgen.

1. Wählen Sie **OK** aus.

    Ein neuer Abzug wird erstellt. Wenn Sie die Option **Anspruchsjournal erstellen** auf *Ja* gesetzt haben, werden folgende Transaktionen gebucht:

    - **Zwei neue Debitorentransaktionen**: Eine Transaktion gleicht den Anspruchsbetrag mit der Originalrechnung aus. Die andere Transaktion erfasst die Schuld eines Debitors in Höhe des Anspruchs, da der Anspruch noch nicht genehmigt wurde. Die ursprüngliche Rechnungstransaktion und die Gegentransaktion des Anspruchs werden automatisch zum Ausgleich vorgemerkt, wenn Sie die Rechnung zuordnen, indem Sie im Aktivititätsbereich **Verwalten \> Rechnung zuordnen**.
    - **Zwei Gegenbuchungen**: Diese Transaktionen werden auf dem Sachkonto **Abzugsgegenkonto** veröffentlicht.
    - **Anspruchsjournal**: Um das Anspruchsjournal für jeden Abzug anzuzeigen, der in der Abzugsworkbench angezeigt wird, wählen Sie die Registerkarte **Verweise**. Das Anspruchsjournal wird im Feld **Nummer der Stapelverarbeitserfassung** angezeigt. Sie können das Anspruchsjournal auch auf der Registerkarte **Abzugsereignisse** ansehen. Dort hat es als **Aktualisierungstyp** den Wert *Abgleichen*.

## <a name="create-a-credit-note-for-a-customer"></a>Eine Gutschrift für einen Debitor erstellen

Danach, wenn eine genehmigte Rückvergütung für den Debitor vorhanden ist, können Sie eine Gutschrift für das Debitorenkonto erstellen, welche bei Bedarf die Rückvergütung darstellt. Die Gutschrift wird dann in der Abzugsworkbench angezeigt, wo sie einem Abzug zugeordnet werden kann.

Gehen Sie folgendermaßen vor, um eine Gutschrift zu erstellen:

1. Wechseln Sie zu **Vertrieb und Marketing \> Debitoren \> Alle Debitoren**.
1. Auswählen des Debitors
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Mahnen** in der Gruppe **Ausgleichen** die Option **Transaktionen ausgleichen** aus.
1. Wählen Sie im Dialogfeld **Transaktionen ausgleichen** die Transaktion aus, auf die die Rückvergütung angewendet wurde.
1. Wählen Sie in der Symbolleiste im Menü **Funktionen** den Typ des geltenden Rückvergütungsprogramms aus.
1. Auf der **Rückvergütung** wählen Sie die Registerkarte **Übersicht** und dann das Kontrollkästchen **Markieren** neben der entsprechenden Rückvergütungs-ID.
1. Wählen Sie im Aktivitätsbereich **Funktionen \> Gutschrift erstellen** aus.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Einen Abzug in der Abzugsworkbench verarbeiten

In der Abzugsworkbench können Sie Abzüge mit offenen Habenbuchungen abgleichen, Abzüge aufteilen, Abzüge verweigern und Abzüge abschreiben.

Abhängig davon, wie Sie einen Abzug verarbeiten möchten, führen Sie eine oder mehrere der Prozeduren in den folgenden Unterabschnitten aus. Sie können die Prozeduren nach Bedarf kombinieren. So können Sie beispielsweise einen Abzug in zwei Teile aufteilen und dann einen Teil einer Gutschrift zuordnen, aber den Rest in der Workbench lassen, sodass Sie ihn später einer anderen Gutschrift zuordnen können. Sie können auch einen Abzug einer Gutschrift zuordnen, die kleiner als der Abzugsbetrag ist, und den Restsaldo des Abzugs dann verweigern oder abschreiben.

### <a name="match-a-deduction-to-a-credit"></a>Einen Abzug mit einer Gutschrift abgleichen

Gehen Sie folgendermaßen vor, um einen Abzug mit einer Gutschrift abzugleichen.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** für den Abzugsprozess.
1. Wählen Sie im Abschnitt **Offene Transaktionen** das Kontrollkästchen **Markieren**, damit die Gutschrift mit dem Abzug abgeglichen werden kann. Wenn mehrere Gutschriften aufgeführt sind, können Sie mehr als eine Gutschrift auswählen, um sie mit dem Abzug abzugleichen. Wenn Sie möchten, dass das System automatisch Gutschriften auswählt, die dem Betrag des Abzugs entsprechen, wählen Sie in der Symbolleiste eine entsprechende Option aus dem Menü **Abzugsbetrag auswählen**.
1. Wählen Sie im Aktivitätsbereich auf **Verwalten \> Abgleichen**. Das System ordnet den Abzug der Gutschrift zu. Wenn ein Saldo für den Abzug verbleibt, wird dieser im Feld **Verbleibender Betrag** auf der Registerkarte **Abzüge** angezeigt.

    > [!NOTE]
    > Für Abzüge, die mit dem Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite erstellt wurden, steht der Befehl **Verwalten \> Abgleichen** nur zur Verfügung, wenn das Feld **Anspruchsstatus** auf *Akzeptiert* gesetzt ist. Mit diesem Befehl kann die preis- oder mengenbasierte Transaktion manuell der zugehörigen Gutschrift im Abschnitt **Offene Transaktionen** zugeordnet werden. Diese Gutschrift entsteht entweder bei der Genehmigung des Abzugs (durch Verwendung des Befehl **Verwalten \> Abzug genehmigen**) oder wenn er einer bestehenden Gutschrift zugeordnet wird, wie im Artikel [Außerhalb des Abzugsgenehmigungsprozesses erstellte Gutschriften](#credits-outside-approval) weiter unten beschrieben. Die periodische Aufgabe *Genehmigte Abzüge ausgleichen* (**Vertrieb und Marketing \> Periodische Aufgaben \> Genehmigte Abzüge ausgleichen**) kann auch verwendet werden, um Abzüge und Gutschriften automatisch auszugleichen, bei denen die **Abzugskennung**-Werte und Beträge übereinstimmen.

### <a name="split-a-deduction"></a>Einen Abzug teilen

Gehen Sie zum Teilen eines Abzugs folgendermaßen vor.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** für den Abzugsprozess.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Teilen**.
1. Im Dialogfeld **Teilen** geben Sie im Feld **Betrag teilen** den Betrag ein, der vom Hauptabzug abgeteilt werden soll. Wählen Sie dann **OK** aus.
1. Beachten Sie auf der Registerkarte **Abzüge**, dass ein neuer Datensatz für den geteilten Betrag aufgeführt wird. Der ursprüngliche Abzusdatensatz enthält den Rest des Abzugssaldos. Sie können jetzt die zwei Teile der ursprünglichen Rückvergütung separat verwalten.
1. Wählen Sie den ursprünglichen Abzugsdatensatz und dann die Registerkarte **Verweise** aus. Das Feld **Betrag teilen** zeigt den Betrag an, der vom ursprünglichen Betrag abgeteilt wurde.

### <a name="attach-an-invoice-to-a-deduction"></a>Einem Abzug eine Rechnung zuordnen

Sie können eine Rechnung einem Abzug zuordnen, wenn der Abzug mit dem Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite erstellt wurde, und wenn derzeit keine Rechnung zugeordnet ist (d. h. die Spalte **Rechnung** ist leer).

Gehen Sie wie folgt vor, um eine Rechnung einem Abzug zuzuordnen.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** für den Abzugsprozess.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Rechnung zuordnen** aus.
1. Im Dialogfeld **Rechnung zuordnen** wählen Sie eine Rechnung und dann **OK** aus.
1. Folgen Sie im Dialogfeld **Transaktionen ausgleichen** einem dieser Schritte, je nachdem, ob beim Anlegen des Abzugs ein Anspruchsjournal veröffentlicht wurde:

    - Wenn ein Anspruchsjournal veröffentlicht wurde, werden die von Ihnen ausgewählte Rechnung und die Debitorengutschrifttransaktion des Anspruchsjournals mit einem Häkchen in der Spalte **Markieren** gekennzeichnet. Wählen Sie **Buchen** aus. Der verbleibende Saldo auf der zugeordneten Rechnung wird um den Anspruchsbetrag gekürzt.
    - Wenn kein Anspruchsjournal veröffentlicht wurde, zeigt keine Transaktion ein Häkchen in der Spalte **Markieren**. Da Sie erst nach Genehmigung des Abzugs mit einem Anspruchsjournal abgleichen können, wählen Sie **Stornieren**.

### <a name="detach-an-invoice-from-a-deduction"></a>Eine Rechnung von einem Abzug trennen

Sie können eine Rechnung von einem Abzug trennen, wenn der Abzug mit dem Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite erstellt wurde, wenn derzeit eine Rechnung zugeordnet ist (d. h. die Spalte **Rechnung** enthält eine Rechnungsnummer) und das Feld **Anspruchsstatus** steht auf *Offen*. Sie müssen diese Aufgabe möglicherweise erledigen, weil eine falsche Rechnung zugeordnet wurde. Die Rechnung wird aus dem Abzug entfernt und der verbleibende Saldo wird aktualisiert, wenn er beim Zuordnen der Rechnung reduziert wurde.

Gehen Sie folgendermaßen vor, um eine Rechnung vom einem Abzug zu trennen.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** für den Abzugsprozess.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Rechnung trennen** aus.

### <a name="approve-a-deduction"></a>Einen Abzug genehmigen

Sie können Abzüge genehmigen, die erstellt wurden, indem Sie den Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite verwenden. Sie können jedoch nur Abzüge genehmigen, wenn das Feld **Anspruchsstatus** auf *Offen* steht.

Gehen Sie zum Genehmigen eines Abzugs folgendermaßen vor.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** für den Abzugsprozess.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Abzug genehmigen** aus.
1. Bearbeiten Sie bei Bedarf im Dialogfeld **Abzug genehmigen** die Informationen im Wert **Hinweis** oder fügen Sie neue hinzu.
1. Wenn der Abzug preisbasiert ist und keine Rechnung zugeordnet wurde, wählen Sie eine Artikel-Mehrwertsteuergruppe aus. Normalerweise ist die Artikel-Mehrwertsteuergruppe auf der Rechnung festgelegt. Daher muss der Mehrwertsteuercode angegeben werden, wenn er nicht einer Rechnung zugeordnet ist.
1. Wählen Sie **OK** aus.

    Zu diesem Zeitpunkt können keine weiteren Änderungen am Abzug vorgenommen werden. Wenn die Option **Anspruchsjournal erstellen** auf *Nein* gesetzt wurde, als der Abzug erstellt wurde, wird das Abzugsjournal erstellt und veröffentlicht, wenn der Abzug genehmigt wird. Nachdem der Abzug genehmigt wurde, wird die Gutschrift automatisch erstellt und geöffnet. Der Typ hängt vom Wert unter **Anspruchsgrundlage** des Werts ab:

    - *Preisbasiert*: Bei einem preisbasierten Abzug wird für das Debitorenkonto eine Freitextrechnung erstellt. Sie können eine Beschreibung hinzufügen und die Gutschrift buchen. Die folgenden Felder werden beim Erstellen des Entwurfs durch den Abzug ausgefüllt:

        - **Abzugskennung**: Dieses Feld wird der Kopfzeile hinzugefügt, um die Rückverfolgbarkeit bis zum Abzug zu ermöglichen.
        - **Hauptkonto**: Der Wert wird bestimmt durch den Wert **Anspruchsbuchungskonto**, der für die Abzugsursache festgelegt wird, die dem Abzug zugeordnet ist.
        - **Artikel-Mehrwertsteuergruppe**: Der Wert richtet sich nach der zugeordneten Rechnung oder nach dem Wert, den Sie bei der Genehmigung des Abzugs ausgewählt haben.
        - **Preis je Einheit**: Der Wert ist die Gutschrift des Anspruchsbetrags des Abzugs.
        - **Rechnungstext**: Standardmäßig ist dieses Feld auf den Wert unter **Hinweise** des Abzugs eingestellt.

    - *Mengenbasiert*: Bei einem mengenbasierten Abzug wird ein offener Auftrag oder eine Rücklieferung angelegt. Die Einstellung **Rücklieferung erstellen** auf der Seite **[Debitorenparameter](#accounts-receivable-deductions)** bestimmt, ob ein Auftrag oder eine Rücklieferung erstellt wird, wenn der Abzug genehmigt wird. Die Seite **Aufträge kopieren** erscheint und wird gefiltert, um Zeilen anzuzeigen, in denen das Feld **Rechnungskonto** auf das Debitorenkonto des Abzugs gesetzt ist. Führen Sie die folgenden Schritte aus:

        1. Im Inforegister **Rechnungen** zeigt der Abschnitt **Kopfzeilen** die Verkaufsrechnungen an, bei denen der Wert **Rechnungskonto** mit dem Debitorenkonto des Abzugs übereinstimmt. Wählen Sie eine zutreffende Verkaufsrechnung aus.
        1. Der Abschnitt **Positionen** zeigt alle Positionen aus der ausgewählten Verkaufsrechnung. Aktivieren Sie das Kontrollkästchen **Auswählen** für jede Position, die Sie kopieren möchten. Wählen Sie alternativ im Abschnitt **Kopfzeilen** das Kontrollkästchen **Alles Auswählen** für den Auftrag, um alle seine Positionen auszuwählen.
        1. Passen Sie den Wert **Menge** für eine oder mehrere Positionen nach Bedarf an.

            Alle Positionen, die Sie bisher ausgewählt haben, werden auf dem Inforegister **Zum Kopieren ausgewählte Positionen oder Kopfzeile** aufgeführt.

        1. Wiederholen Sie die beiden vorherigen Schritte nach Bedarf, bis alle erforderlichen Positionen auf dem Inforegister **Zum Kopieren ausgewählte Positionen oder Kopfzeile** aufgeführt sind.
        1. Wählen Sie **OK** aus.

            Die neue Rücklieferung wird geöffnet und die folgenden Felder werden automatisch ausgefüllt:

            - **Abzugskennung**: Dieses Feld wird der Kopfzeile hinzugefügt, um die Rückverfolgbarkeit bis zum Abzug zu ermöglichen.
            - **Ursachencode für Rückgabe**: Standardmäßig ist dieses Feld auf den Wert **Ursachencode für Rückgabe** festgelegt, der für die Abzugsursache gesetzt wird, die dem Abzug zugeordnet ist.

Nachdem die Gutschrift in Rechnung gestellt wurde, erscheint sie im Abschnitt **Offene Transaktionen** der Abzugsworkbench nach der anwendbaren **Abzugskennung**. Das Feld **Anspruchstyp** wird auf *Sonstige Gutschriften* gesetzt. Die Gutschrift steht zur Verfügung, bis sie mit dem Abzug auf eine der folgenden Arten ausgeglichen wurde:

- Sie gleichen sie manuell aus, indem Sie im Aktivitätsbereich **Verwalten \> Abgleichen** auswählen.
- Sie wird automatisch durch die periodische Aufgabe *Genehmigte Ansprüche ausgleichen* ausgeglichen (**Vertrieb und Marketing \> Periodische Aufgaben \> Genehmigte Ansprüche ausgleichen**).
- Sie wird automatisch ausgeglichen, weil die Option **Automatische Ausgleich** der Registerkarte **Ausgleich** auf der Seite **Debitorenparameter** auf *Ja* gestellt ist.

Um die Gutschrift anzuzeigen, die bei der Genehmigung des Abzugs erstellt wird, können Sie auch die Schaltfläche **Offene Gutschrift** im Abschnitt **Offene Transaktionen** der Abzugswerkbank verwenden.

### <a name="create-a-return-order"></a>Erstellen einer Rücklieferung

Sie können eine Rücklieferung für Abzüge erstellen, die erstellt wurden, indem Sie den Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite verwenden. Alle folgenden Bedingungen müssen jedoch erfüllt sein:

- Das Feld **Anspruchsgrundlage** muss auf *Mengenbasiert* gesetzt sein.
- Das Feld **Anspruchsstatus** muss auf *Offen* stehen.
- Die Option **Rücklieferung erstellen** auf der Registerkarte **Abzüge** der Seite **[Debitorenparameter](#accounts-receivable-deductions)** muss auf *Ja* stehen.
- Die Option **Rücklieferung vor Abzugsgenehmigung erstellen** auf der Registerkarte **Abzüge** der Seite **[Debitorenparameter](#accounts-receivable-deductions)** muss auf *Ja* stehen.

Gehen Sie folgendermaßen vor, um eine Rücklieferung zu erstellen.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** für den Abzugsprozess.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Rücklieferung erstellen** aus.
1. Bearbeiten Sie bei Bedarf im Dialogfeld **Abzug genehmigen** die Informationen im bestehenden Wert **Hinweise** oder fügen Sie neue hinzu und wählen Sie dann **OK**.
1. Im Dialogfeld **Aufträge kopieren** im Inforegister **Rechnungen** zeigt der Abschnitt **Kopfzeilen** die Verkaufsrechnungen an, bei denen der Wert **Rechnungskonto** mit dem Debitorenkonto des Abzugs übereinstimmt. Wählen Sie eine zutreffende Verkaufsrechnung aus.
1. Der Abschnitt **Positionen** zeigt alle Positionen aus der ausgewählten Verkaufsrechnung. Aktivieren Sie das Kontrollkästchen **Auswählen** für jede Position, die Sie kopieren möchten. Wählen Sie alternativ im Abschnitt **Kopfzeilen** das Kontrollkästchen **Alles Auswählen** für den Auftrag, um alle seine Positionen auszuwählen.
1. Passen Sie den Wert **Menge** für eine oder mehrere Positionen nach Bedarf an.

    Alle Positionen, die Sie bisher ausgewählt haben, werden auf dem Inforegister **Zum Kopieren ausgewählte Positionen oder Kopfzeile** aufgeführt.

1. Wiederholen Sie die beiden vorherigen Schritte nach Bedarf, bis alle erforderlichen Positionen auf dem Inforegister **Zum Kopieren ausgewählte Positionen oder Kopfzeile** aufgeführt sind.
1. Wählen Sie **OK** aus.

    Die neue Rücklieferung wird geöffnet und die folgenden Felder werden automatisch ausgefüllt:

    - **Abzugskennung**: Dieses Feld wird der Kopfzeile hinzugefügt, um die Rückverfolgbarkeit bis zum Abzug zu ermöglichen.
    - **Ursachencode für Rückgabe**: Standardmäßig ist dieses Feld auf den Wert **Ursachencode für Rückgabe** festgelegt, der für die Abzugsursache gesetzt wird, die dem Abzug zugeordnet ist.

### <a name="deny-a-deduction"></a>Einen Abzug verweigern

Gehen Sie zum Verweigern eines Abzugs folgendermaßen vor.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** für den Abzugsprozess.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Verweigern**.
1. Wählen Sie im Dialogfeld **Verweigern** den Ursachencode für die Verweigerung aus, und wählen Sie dann **OK**.
1. Wählen Sie im Feld **Anzeigen** unter dem Aktivitätsbereich *Geschlossen* aus.

    Die Registerkarte **Abzüge** zeigt den verweigerten Abzug an und das Feld **Verbleibender Betrag** für den Abzug wird auf *0,00* festgelegt.

    Bei Abzügen, die mit dem Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite erstellt wurden, kommt es zu den folgenden Ereignissen:

    - Auf der Registerkarte **Verweise** werden die Felder im Abschnitt **Verweigerung** aktualisiert.
    - Wenn Sie beim Erstellen des Abzugs das Erstellen des Anspruchsjournals ausgewählt haben und dem Abzug eine Rechnung zugeordnet haben, die den Rechnungssaldo reduziert, wird die Rechnung getrennt und der verbleibende Saldo der zuvor angehängten Rechnung wird um den Betrag des abgelehnten Anspruchs erhöht.
    - Das Feld **Status** wird auf *Geschlossen* festgelegt.
    - Das Feld **Anspruchsstatus** des Abzugs wird auf *Abgelehnt* festgelegt.

Um eine Verweigerung umzukehren, gehen Sie folgendermaßen vor.

1. Wählen Sie auf der Registerkrte **Abzüge** einen verweigerten Abzug aus.
1. Wählen Sie im Aktivitätsbereich **Verweigerung rückgängig machen**.

    Bei Abzügen, die mit dem Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite erstellt wurden, kommt es zu den folgenden Ereignissen:

    - Auf der Registerkarte **Verweise** werden die Felder im Abschnitt **Verweigerung** aktualisiert.
    - Das Feld **Status** wird auf *Offen* festgelegt.
    - Das Feld **Anspruchsstatus** des Abzugs wird auf *Offen* festgelegt.

### <a name="write-off-a-deduction"></a>Einen Abzug abschreiben

Gehen Sie zum Abschreiben eines Abzugs folgendermaßen vor.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** für den Abzugsprozess.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Abschreiben**.
1. Wählen Sie im Dialogfeld **Abschreiben** den Ursachencode für die Abschreibung aus, und wählen Sie dann **OK**.
1. Wählen Sie im Feld **Anzeigen** die Option *Geschlossen* aus.

    Die Registerkarte **Abzüge** zeigt den abgeschriebenen Abzug an und das Feld **Verbleibender Betrag** für den Abzug wird auf *0,00* festgelegt.

    Bei Abzügen, die mit dem Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite erstellt wurden, kommt es zu den folgenden Ereignissen:

    - Auf der Registerkarte **Verweise** werden die Felder im Abschnitt **Abschreiben** aktualisiert.
    - Wenn Sie das Anspruchsjournal beim Erstellen des Abzugs erstellt haben, wird ein Anspruchsjournal für den Abschreibungsursachencode des Abzugs veröffentlicht. Sie können diesen Eintrag auf der Registerkarte **Abzugsereignisse** ansehen, wo der Wert **Aktualisierungstyp** *Abschreiben* lautet.
    - Das Feld **Status** wird auf *Geschlossen* festgelegt.
    - Das Feld **Anspruchsstatus** des Abzugs wird auf *Abschreiben* festgelegt.

Um eine Abschreibung rückgängig zu machen, gehen Sie folgendermaßen vor.

1. Wählen Sie auf der Registerkrte **Abzüge** einen verweigerten Abzug aus.
1. Wählen Sie im Aktivitätsbereich **Abschreibung rückgängig machen** aus.

    Bei Abzügen, die mit dem Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite erstellt wurden, kommt es zu den folgenden Ereignissen:

    - Auf der Registerkarte **Verweise** werden die Felder im Abschnitt **Abschreiben** aktualisiert.
    - Wenn Sie das Anspruchsjournal beim Erstellen des Abzugs erstellt haben, wird ein Anspruchsjournal für den Abschreibungsursachencode des Abzugs veröffentlicht. Sie können diesen Eintrag auf der Registerkarte **Abzugsereignisse** ansehen, wo der Wert **Aktualisierungstyp** *Abschreibung rückgängig machen* lautet.
    - Das Feld **Status** wird auf *Offen* festgelegt.
    - Das Feld **Anspruchsstatus** des Abzugs wird auf *Offen* festgelegt.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Außerhalb des Abzugsgenehmigungsprozesses erstellte Gutschriften

Dieser Abschnitt gilt nur für Abzüge, die erstellt wurden, indem Sie den Befehl **Neuer Abzug** in der Abzugsworkbench, dem Debitorenausgleich oder der Debitorenseite verwenden.

Möglicherweise haben verschiedene Benutzer bereits eine Freitextrechnung, eine Rücklieferung oder einen negativen Auftrag für den Anspruch eines Kunden außerhalb des **Abzugsgenehmigungsprozesses** erstellt. Wenn der vorhandene Abzug in der Abzugsworkbench genehmigt wird, erstellt das System automatisch eine weitere Freitextrechnung, Rücklieferung oder einen negativen Auftrag. In diesem Abschnitt wird beschrieben, wie Sie vorhandene Gutschriften einem Abzug zuordnen, bevor der Abzug genehmigt wird, um doppelte Gutschriften zu vermeiden.

### <a name="attach-a-credit-to-deduction"></a>Eine Gutschrift einem Abzug zuordnen

In diesem Abschnitt wird beschrieben, wie Sie eine Gutschrift einem Abzug von der Gutschrift aus zuordnen.

Nachdem dem Abzug eine Gutschrift zugeordnet wurde, können Sie sie ansehen, indem Sie die Schaltfläche **Offene Gutschrift** in der Symbolleiste des Abschnitts **Offene Transaktionen** der Abzugswerkbank verwenden.

Nachdem eine Gutschrift in Rechnung gestellt und der Abzug genehmigt wurde, erscheint die Gutschrift im Abschnitt **Offene Transaktionen** der Abzugsworkbench nach der anwendbaren **Abzugskennung**. Das Feld **Anspruchstyp** wird auf *Sonstige Gutschriften* gesetzt.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Einem Abzug eine Freitextrechnung zuordnen

Gehen Sie wie folgt vor, um eine Freitextrechnung einem Abzug zuzuordnen.

1. Wechseln Sie zu **Debitoren \> Rechnungen \> Alle Freitextrechnungen**.
1. Wählen Sie die entsprechende Rechnung aus.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Rechnung**, und wählen Sie **Gutschrift Abzug zuordnen** aus. Diese Schaltfläche ist nur verfügbar, wenn das Feld **Abzugskennung** der Freitextrechnung leer ist. Ein leeres Feld zeigt an, dass die Freitextrechnung noch nicht einem Abzug zugeordnet ist.
1. Auf der Seite **Gutschrift Abzug zuordnen** können Sie *einen* Abzug auswählen. Nur offene *preisbasierte* Abzüge stehen zur Auswahl.
1. Wählen Sie **OK** aus. Das Feld **Abzugskennung** ist in der Kopfzeile der Freitextrechnung festgelegt.

#### <a name="attach-a-return-order-to-a-deduction"></a>Einem Abzug eine Rücklieferung zuordnen

Gehen Sie wie folgt vor, um eine Rücklieferung einem Abzug zuzuordnen.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Rücklieferungen**.
1. Wählen Sie die zutreffende Nummer der eingegangenen oder offenen Genehmigungen bei Rückgabe von Handelswaren (RMA) aus.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Rücklieferung**, und wählen Sie **Gutschrift Abzug zuordnen** aus. Diese Schaltfläche ist nur verfügbar, wenn das Feld **Abzugskennung** der Rücklieferung leer ist. Ein leeres Feld zeigt an, dass die Rücklieferung noch nicht einem Abzug zugeordnet ist.
1. Auf der Seite **Gutschrift Abzug zuordnen** können Sie *einen* Abzug auswählen. Nur offene *mengenbasierte* Abzüge stehen zur Auswahl.
1. Wählen Sie **OK** aus. Das Feld **Abzugskennung** ist in der Kopfzeile der Rücklieferung festgelegt.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Einem Abzug einen Auftrag zuordnen

Gehen Sie wie folgt vor, um einen Auftrag einem Abzug zuzuordnen.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Wählen Sie den entsprechenden offenen, gelieferten oder in Rechnung gestellten Auftrag aus.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Rechnung**, und wählen Sie **Gutschrift Abzug zuordnen** aus. Diese Schaltfläche ist nur verfügbar, wenn das Feld **Abzugskennung** des Auftrags leer ist. Ein leeres Feld zeigt an, dass der Auftrag noch nicht einem Abzug zugeordnet ist.
1. Auf der Seite **Abzug zuordnen** können Sie *einen* Abzug auswählen. Nur offene *mengenbasierte* Abzüge stehen zur Auswahl.
1. Wählen Sie **OK** aus. Das Feld **Abzugskennung** ist in der Kopfzeile des Auftrags festgelegt.

#### <a name="detach-a-deduction-from-a-credit"></a>Abzug von einer Gutschrift trennen

Wenn der falsche Abzug zugeordnet wurde, können Sie ihn von der Gutschrift trennen. Alle folgenden Bedingungen müssen jedoch erfüllt sein:

- Dem Abzug ist eine Gutschrift zugeordnet.
- Das Feld **Anspruchsstatus** muss auf *Offen* stehen.

Um einen Abzug von einer Gutschrift zu trennen, gehen Sie je nach Gutschriftstyp wie folgt vor:

- **Freitextrechnungen:** Wählen Sie auf der SEite **Alle Freitextrechnungen** eine Rechnung aus. Klicken Sie dann im Aktivitätsbereich auf die Registerkarte **Rechnung**, und wählen Sie **Gutschrift vom Abzug trennen** aus.
- **Rücklieferungen** Wählen Sie auf der Seite **Alle Rücklieferungen** einen Auftrag aus. Klicken Sie dann im Aktivitätsbereich auf die Registerkarte **Rücklieferung**, und wählen Sie **Gutschrift vom Abzug trennen** aus.
- **Aufträge** Wählen Sie auf der Seite **Alle Aufträge** einen Auftrag aus. Klicken Sie dann im Aktivitätsbereich auf die Registerkarte **Rechnung**, und wählen Sie **Gutschrift vom Abzug trennen** aus.

### <a name="attach-a-deduction-to-a-credit"></a>Einen Abzug einer Gutschrift zuordnen

In diesem Abschnitt wird beschrieben, wie Sie einen Abzug einer Gutschrift vom Abzug aus zuordnen.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Einen Abzug einer Freitext-, einer Rücklieferungs- oder einer Auftragsgutschrift zuordnen

Um einen Abzug einer Freitext-, einer Rücklieferungs- oder einer Auftragsgutschrift zuordnen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Wählen Sie den entsprechenden offenen Abzug aus.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Abzug Gutschrift zuordnen** aus. Diese Schaltfläche ist nur verfügbar, wenn das Feld **Anspruchsstatus** auf *Offen* gesetzt ist.
1. Auf der Seite **Gutschrift zuordnen** können Sie *eine* Gutschrift auswählen. Der angezeigte Gutschriftstyp hängt vom Wert **Anspruchsgrundlage** des Abzugs ab:

    - *Preisbasiert*: Die Seite zeigt Freitextrechnungen für das Debitorenkonto an, bei dem das Feld **Abzugskennung** leer ist. Auch Debitorenanforderungen werden angezeigt, da die Freitextrechnung möglicherweise nicht gebucht ist. Daher hat sie möglicherweise keine Nummer, auf die verwiesen werden kann.
    - *Mengenbasiert*: Welcher Gutschriftentyp angezeigt wird, hängt von der Einstellung der Option **Rücklieferung erstellen** auf der Seite **[Debitorenparameter](#accounts-receivable-deductions)** ab:

        - *Ja*: Die Seite zeigt Rücklieferungen für das Debitorenkonto an, bei dem das Feld **Abzugskennung** leer ist.
        - *Nein*: Die Seite zeigt Aufträge für das Debitorenkonto an, bei dem das Feld **Abzugskennung** leer ist.

1. Wählen Sie **OK** aus. Das Feld **Abzugskennung** ist in der Kopfzeile der Gutschrift festgelegt.

Nachdem dem Abzug eine Gutschrift zugeordnet wurde, können Sie sie ansehen, indem Sie die Schaltfläche **Offene Gutschrift** in der Symbolleiste des Abschnitts **Offene Transaktionen** der Abzugswerkbank verwenden.

Nachdem eine Gutschrift in Rechnung gestellt und der Abzug genehmigt wurde, erscheint die Gutschrift im Abschnitt **Offene Transaktionen** der Abzugsworkbench nach der anwendbaren **Abzugskennung**. Das Feld **Anspruchstyp** wird auf *Sonstige Gutschriften* gesetzt.

#### <a name="detach-a-credit-from-the-deduction"></a>Eine Gutschrift von dem Abzug trennen

Wenn die falsche Gutschrift zugeordnet wurde, können Sie sie von dem Abzug trennen. Klicken Sie im Aktivitätsbereich auf die Gruppe **Verwalten** und wählen Sie **Abzug von Gutschrift trennen** aus. Der Wert der **Abzugskennung** wird von der Gutschrift getrennt.

Die Schaltfläche **Abzug von Gutschrift trennen** ist nur verfügbar, wenn die folgenden Bedingungen erfüllt sind:

- Dem Abzug ist eine Gutschrift zugeordnet.
- Das Feld **Anspruchsstatus** muss auf *Offen* stehen.

## <a name="create-a-one-time-promotion"></a>Eine einmalige Aktion erstellen

Manchmal haben Sie möglicherweise keine genehmigte Rückvergütung, der Sie einen Abzug zuordnen können. In diesem Fall können Sie die Funktion *einmalige Aktion* verwenden, um den Abzug einer Handelsrückvergütung anzupassen, die dem Debitor zugeordnet wird. Die Funktion *einmalige Aktion* erstellt eine neue Handelsvergütungsvereinbarung und ein Pauschalsummenverkaufereignis. Sie ordnet dann den Pauschalbetrag dem Abzug zu und nimmt die Buchungen vor, die erforderlich sind, um den Abzug zu schließen.

Diese Funktion ist hilfreich, wenn Sie Handelsvergütungen verwenden. Weitere Informationen zu Handelsvergütungen finden Sie unter [Handelsvergütungsverwaltung](../sales-marketing/trade-allowance.md).

Zunächst müssen Sie eine Vorlage einrichten, die verwendet werden kann, um die neue Handelsvergütungsvereinbarung zu erstellen. Gehen Sie zum Einrichten einer Vorlage folgendermaßen vor.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Vorlagen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie in die Felder die Informationen ein, die in den Vereinbarungen angezeigt werden sollen, die von der Vorlage erstellt werden.
1. Wählen Sie im Inforegister **Kunden** das Feld **Hierarchie** und dann eine Hierarchieebene aus.
1. Wählen Sie in der Hierarchieliste den Debitor aus, der einen nicht abgeglichenen Abzug hat, und wählen Sie dann die rechte Pfeilschaltfläche (**\>**). Der Debitor wird der Liste **Handelsvergütungsvereinbarungs-Debitoren** zugeordnet.
1. Legen Sie die restlichen Felder nach Bedarf fest und schließen Sie dann die Seite.
1. Gehen Sie zu **Vertrieb und Marketing \> Setup \> Handelsvergütung \> Parameter der Handelsvergütungsverwaltung**.
1. Auf der Registerkarte **Übersicht** wählen Sie im Feld **Vorlage für einmalige Aktion** den Namen der Vorlage aus, die zum Erstellen von einmaligen Aktionen verwendet werden soll.

Danach können Sie eine einmalige Aktion in der Abzugsworkbench erstellen. Um eine einmalige Aktion zu erstellen, führen Sie folgende Schritte aus.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Aktivieren Sie das Kontrollkästchen **Markieren** neben dem Abzugsprozess.
1. Wählen Sie im Aktivitätsbereich **Verwalten \> Abzug als einmalige Aktion ausgleichen**.
1. Folgen Sie im Dialogfeld **Einmalige Aktion** diesen Schritten, um den Abzug einem oder mehreren Geldmitteln zuzuordnen:

    1. Wählen Sie **Neu** und wählen Sie dann im Feld **Geldmittelkennung** eine Geldmittelkennung aus. Wiederholen Sie diesen Schritt, um so viele Geldmittelkennungen hinzuzufügen, wie Sie benötigen.
    1. Geben Sie im Feld **Prozent** neben jeder Geldmittelkennung den Prozentsatz des Abzugs ein, der dem Geldmittel zuzuweisen ist. Die Beträge, die Sie in den Feldern **Prozent** eingeben, müssen insgesamt 100 % ergeben.

1. Wählen Sie **OK** aus. Das System erstellt eine neue Handelsrückvergütungsvereinbarung mit einem Pauschalsummenverkaufereignis und ordnet den Pauschalbetrag dem Abzug zu.

## <a name="do-a-mass-update-of-deductions"></a>Eine Massenaktualisierung von Abzügen durchführen

Wenn Sie dieselbe Änderung an mehreren Abzügen durchführen müssen, können Sie diese Abzüge auswählen und eine Massenaktualisierung ihrer Felder durchführen.

Gehen Sie wie folgt vor, um eine Massenaktualisierung durchzuführen.

1. Gehen Sie zu **Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**.
1. Wählen Sie im Feld **Anzeigen** unter dem Aktivitätsbereich, den Typ der Abzüge aus, die Sie anzeigen möchten.
1. Aktivieren Sie das Kontrollkästchen neben jedem Abzug, den Sie aktualisieren möchten. Wählen Sie dann im Aktivitätsbereich **Verwalten \> Masseaktualisierung** aus.
1. Das Dialogfeld **Massenaktualisierung** Dialogfeld zeigt die ausgewählten Abzüge an. Aktualisieren Sie die Felder nach Bedarf und wählen Sie dann **OK**, um die Änderungen zu akzeptieren.
