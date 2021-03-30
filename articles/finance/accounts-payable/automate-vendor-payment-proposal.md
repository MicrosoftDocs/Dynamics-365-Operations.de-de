---
title: Automatisieren Sie Kreditorenzahlungsvorschläge
description: In diesem Thema wird erläutert, wie Organisationen, die Lieferanten nach einem wiederkehrenden Zeitplan bezahlen, den Prozess der Generierung von Lieferantenzahlungsvorschlägen automatisieren können.
author: kweekley
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d6a53b2cb48856083f3b2e40fca8adb92f4e5113
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250649"
---
# <a name="automate-vendor-payment-proposals"></a>Automatisieren Sie Kreditorenzahlungsvorschläge

[!include [banner](../includes/banner.md)]

Organisationen, die Lieferanten nach einem wiederkehrenden Zeitplan bezahlen, können den Prozess der Generierung von Lieferantenzahlungsvorschlägen nun automatisieren. Automatisierungen von Lieferantenzahlungsvorschlägen definieren die folgenden Details:

- Wenn Zahlungsvorschläge ausgeführt werden
- Nach welchen Kriterien werden die zu zahlenden Rechnungen ausgewählt
- In welchem Lieferantenzahlungsjournal werden die resultierenden Zahlungen gespeichert

Automatisierungen von Zahlungsvorschlägen buchen die Zahlungen nicht automatisch. Daher können Sie weiterhin alle Validierungs- und Workflowprozesse verwenden, die Sie derzeit zum Genehmigen der erstellten Zahlungen verwenden.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Definieren Sie das Auftreten von Lieferantenzahlungsvorschlägen

Automatisierungen von Lieferantenzahlungsvorschlägen verwenden das Framework zur Prozessautomatisierung. Verschiedene Geschäftsprozesse verwenden dieses Framework, um die Wiederholung eines ausgewählten Prozesses zu definieren. Für Lieferantenzahlungsvorschläge kann auf die Automatisierung unter **Abbrechnungsverbindlichkeiten \> Zahlungseinrichtung \> Prozessautomatisierung** zugegriffen werden.

Verwenden Sie zuerst die Automatisierungsoption **Neuen Prozess erstellen** und wählen Sie **Zahlungsvorschlag des Anbieters**. Ein Assistent führt Sie dann durch den Prozess des Einrichtens des Lieferantenzahlungsvorschlags.

## <a name="general-page"></a>Allgemeine Seite

Auf der Seite **Allgemeines** geben Sie auf der Seite des Assistenten den Namen des Lieferantenzahlungsvorschlags ein, den Sie erstellen. Wenn Sie beispielsweise alle inländischen Anbieter am Montag per Scheck bezahlen, geben Sie einen aussagekräftigen Namen ein wie **Inländisch\_Prüfen**. Der von Ihnen eingegebene Name wird in der Wochenansicht der Prozessautomatisierung im Arbeitsplatz **Lieferantenzahlungen** angezeigt.

Definieren Sie als Nächstes den Eigentümer des erstellten Zahlungsjournals. Der Eigentümer ist normalerweise der Zahlungsangestellte für Kreditorenkonten (AP), der nach seiner Erstellung für das Zahlungsjournal verantwortlich ist.

Die verbleibenden Einstellungen auf der Seite sind allgemein gehalten und werden verwendet, um das Auftrittsmuster für diese Version des Lieferantenzahlungsvorschlags zu definieren. Wenn es sich bei einem Ereignis beispielsweise um Scheckzahlungen am Montag handelt, können Sie es so definieren, dass es wöchentlich ausgeführt wird, und Sie können Montag als Wochentag auswählen, an dem es ausgeführt wird. Sie können auch einen frühen Zeitplan eingeben, z. B. 2:00 Uhr, damit die Prozessautomatisierung vor Beginn des nächsten Geschäftstages abgeschlossen ist.

Es ist wichtig, dass Sie verstehen, dass Sie den Assistenten verwenden, um zu definieren, wann der Zahlungsvorschlag des Anbieters verarbeitet wird. Sie definieren nicht, wann die Lieferantenzahlungen generiert, gedruckt und gebucht werden. In der Wochenansicht wird die Prozessautomatisierung für Lieferantenzahlungsvorschläge an den Tagen angezeigt, die im Auftrittsmuster ausgewählt sind.

Weitere Informationen zu den anderen Feldern auf der Seite **Allgemeines** finden Sie in der Dokumentation zur Prozessautomatisierung.

## <a name="vendor-payment-proposal-page"></a>Seite Kreditorenzahlungsvorschlag

Die nächste Seite im Assistenten ist die Seite **Zahlungsvorschlag des Anbieters**. Sie wird verwendet, um die Kriterien für die Auswahl der Lieferantenrechnungen zu definieren, die bezahlt werden sollen. Im Allgemeinen finden Sie dieselben Optionen im Zahlungsvorschlag im Lieferantenzahlungsjournal. Es gibt jedoch einige Ausnahmen. Beispielsweise müssen alle Daten auf dieser Seite als relative Daten definiert werden, da sich das Datum des Zahlungsvorschlags jedes Mal ändert, wenn der Vorschlag ausgeführt wird.

### <a name="journal-name"></a>Erfassungsname

Das Feld **Journalname** definiert den Journalnamen, in dem die Lieferantenzahlungen erstellt werden. Die Ergebnisse der Automatisierung des Lieferantenzahlungsvorschlags erstellen Zahlungen im definierten Journal, das Journal wird jedoch nicht gebucht.

### <a name="from-date-and-to-date"></a>Von-Datum und Bis-Datum

Anstatt ein Von-Datum und ein Bis-Datum zu definieren, um Rechnungen basierend auf dem Fälligkeitsdatum oder dem Skontodatum auszuwählen, müssen Sie die Option **Definieren Sie aktuelle Kriterien** und das Feld **Anzahl der Tage Anpassung für Bis heute** zum Definieren des Datums bis verwenden. Bei der Automatisierung von Zahlungsvorschlägen gibt es kein Konzept für ein Ab-Datum.

Standardmäßig ist die Option **Definieren Sie aktuelle Kriterien** auf **Nein**. Wenn Sie diesen Standardwert verwenden, wählt der Prozess alle Rechnungen zur Zahlung aus, wenn der Prozess ausgeführt wird, da kein Bis-Datum definiert wurde.

Wenn Sie die Option **Definieren Sie aktuelle Kriterien** auf **Ja** festlegen, benutzen Sie das Feld **Anzahl der Tage Anpassung für Bis heute** zum Definieren des Datums, an dem Rechnungen als die angegebene Anzahl von Tagen vor oder nach dem Datum ausgewählt werden, an dem der Prozess ausgeführt wird. Die Zahl kann positiv, negativ oder 0 (Null) sein. Das System zahlt dann Rechnungen, bei denen die Fälligkeitstermine oder Skontodaten die angegebene Anzahl von Tagen vor oder nach dem Datum sind, an dem der Prozess ausgeführt wird. Beispielsweise erstellt die Zahlungsreihe für alle Rechnungen, die am oder vor Freitag fällig sind, Zahlungen per Scheck an alle Lieferanten am Mittwoch. Legen Sie in diesem Fall das Feld der **Anzahl der Tage der Anpassung für Bis heute** auf **2** fest. Wenn der Zahlungsvorschlag am Mittwoch, dem 25. März, ausgeführt wird, werden alle Rechnungen mit einem Fälligkeitsdatum oder einem Skontodatum am oder vor dem 27. März zur Zahlung ausgewählt.

### <a name="minimum-payment-date"></a>Mindestzahlungsdatum

Das Mindestzahlungsdatum definiert das früheste Datum, das beim Erstellen von Zahlungen erstellt wird. Sie müssen zuerst die Option **Definieren Sie Kriterien für das Mindestzahlungsdatum** auf **Ja** festlegen. Mit dieser Einstellung können Sie die Funktion für das Mindestzahlungsdatum verwenden. Wenn Sie diese Option auf **Ja** festlegen, benutzen Sie das Feld **Anzahl der Tage Anpassung für Mindestzahlungsdatum**, um das Mindestzahlungsdatum als die definierte Anzahl Tage vor oder nach dem Datum, an dem der Prozess ausgeführt wird, zu definieren. Die Zahl kann positiv, negativ oder 0 (Null) sein. Beispielsweise generiert die Zahlungsreihe Zahlungen am Mittwoch, um alle Zahlungen einzuschließen, deren Mindestzahlungsdatum am vorhergehenden Montag liegt. Legen Sie in diesem Fall das Feld der **Anzahl der Tage der Anpassung für das minimale Zahlungsdatum** auf **-2** fest.

Hier ist ein Beispiel, das zeigt, wie die Felder für das Bis-Datum und das Mindestzahlungsdatum zusammenarbeiten. Die Automatisierung des Zahlungsvorschlags soll am Mittwoch ausgeführt werden. Das Feld **Anzahl der Tage der Anpassung für Bis heute** ist auf **1** festgelegt, um das Bis-Datum basierend auf dem Fälligkeitsdatum zu definieren. Die **Anzahl der Tage der Anpassung für das minimale Zahlungsdatum** ist auf **-2** festgelegt. Wenn die Automatisierung des Zahlungsprozesses am Mittwoch, dem 25. März, beginnt, werden alle Rechnungen, die am oder vor dem 26. März fällig sind, in den Zahlungsvorschlag aufgenommen. Zahlungsvorschläge werden folgendermaßen generiert:

- Alle Rechnungen, die am oder vor dem 23. März fällig sind, haben ein Zahlungsdatum am 23. März.
- Rechnungen, die am oder vor dem 24. März fällig sind, haben ein Zahlungsdatum am 24. März.
- Rechnungen, die am oder vor dem 25. März fällig sind, haben ein Zahlungsdatum am 25. März.
- Rechnungen, die am oder vor dem 26. März fällig sind, haben ein Zahlungsdatum am 26. März.

### <a name="summarized-payment-date"></a>Zahlungsdatum im Überblick

Das zusammengefasste Zahlungsdatum wird nur verwendet, wenn das Feld **Periode** für die Zahlungsmethode auf **Summe** gesetzt ist. Wenn das Feld **Periode** auf **Total** für Ihre Zahlungsmethode festgelegt ist, müssen Sie die Option **Definieren Sie zusammengefasste Kriterien für das Zahlungsdatum** auf **Ja** festlegen. Wenn Sie diese Option auf **Ja** festlegen, benutzen Sie das Feld **Anzahl der Tage Anpassung für zusammengefasstes Zahlungsdatum**, um das zusammengefasste Zahlungsdatum als die definierte Anzahl Tage vor oder nach dem Datum, an dem der Prozess ausgeführt wird, zu definieren. Die Zahl kann positiv, negativ oder 0 (Null) sein. Beispielsweise generiert die Serie am Mittwoch Zahlungen, und das Unternehmen möchte am Mittwoch eine zusammengefasste Zahlung erstellen. Legen Sie in diesem Fall das Feld der **Anzahl der Tage der Anpassung für das zusammengefasste Zahlungsdatum** auf **0** fest.

### <a name="records-to-include"></a>Einzuschließende Datensätze

Die Filteroptionen können weiterhin für den Zahlungsvorschlag definiert werden. Wenn ein Filter definiert ist, werden die Filterkriterien auf der Assistentenseite nicht angezeigt. Sie können jedoch durch erneutes Öffnen des Filters angezeigt werden.

Die verbleibenden Felder für den Vorschlag funktionieren genauso wie für den Zahlungsvorschlag im Lieferantenzahlungsjournal. Informationen zu den anderen Feldern finden Sie unter [Erstellen Sie Lieferantenzahlungen mithilfe des Zahlungsvorschlags](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Einige länder-/regionenspezifische Felder und einige Felder des öffentlichen Sektors sind in der Automatisierung von Lieferantenzahlungsvorschlägen noch nicht verfügbar.

Wir empfehlen Ihnen, anhand Ihrer Anforderungen zu bewerten, ob die Automatisierung für Ihr Unternehmen von Vorteil ist.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Zeigen Sie die Ergebnisse einer Automatisierung von Lieferantenzahlungsvorschlägen an

Nachdem die Automatisierungsserie für Lieferantenzahlungsvorschläge erstellt wurde, werden die Vorkommen für jede Zahlung in der Wochenansicht der Prozessautomatisierung angezeigt. Für Lieferantenzahlungen wurde die Wochenansicht für die Prozessautomatisierung dem Arbeitsbereich **Lieferantenzahlungen** und die Seite **Prozessautomatisierung** hinzugefügt.

[![Wochenansicht der Prozessautomatisierung im Arbeitsbereich Lieferantenzahlungen](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

Die Wochenansicht der Prozessautomatisierung im Arbeitsbereich **Lieferantenzahlungen** zeigt nur Automatisierungen von Lieferantenzahlungsvorschlägen an. Es werden alle Zahlungsvorgänge für die aktuelle Woche für alle juristischen Personen angezeigt, für die der angemeldete Benutzer Sicherheitsberechtigungen hat. Wenn der AP-Zahlungsangestellte beispielsweise für Zahlungen in den USMF- und USSI-Unternehmen verantwortlich ist, sieht er oder sie das Auftreten der Automatisierung des Lieferantenzahlungsvorschlags für diese beiden Unternehmen, jedoch nicht für andere Unternehmen.

[![Wochenansicht der Prozessautomatisierung für die USMF- und USSI-Unternehmen](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Jedes Ereignis zeigt dem Unternehmen an, in dem das Zahlungsjournal erstellt wurde oder wird. Wenn Zahlungen mithilfe zentraler Zahlungen erstellt werden, wird als Unternehmen das Unternehmen angezeigt, in dem Zahlungen erstellt werden. Das Ereignis zeigt nicht unbedingt an, welche Unternehmensrechnungen bezahlt werden.

Der Name jedes Ereignisses wird ebenfalls angezeigt, um den Zahlungsvorschlag zu identifizieren.

Zusätzlich wird der Status jedes Auftretens angezeigt. Folgende Status werden verwendet:

- **Geplant** – Der Zahlungsvorschlag ist geplant, wurde jedoch noch nicht ausgeführt.
- **Fehler** – Der Zahlungsvorschlag wurde ausgeführt, es ist jedoch ein Fehler aufgetreten. Sie können die Fehler anzeigen, indem Sie die Schaltfläche **Ergebnisse anzeigen** wählen.
- **Abgeschlossen** – Der Zahlungsvorschlag wurde erfolgreich ausgeführt. Sie können die Zahlung anzeigen, indem Sie den Link **Zahlung anzeigen** wählen. Dieser Link öffnet das Zahlungsjournal, das durch das Ereignis erstellt wurde.

Nachdem die Zahlungen erstellt wurden, können Sie die Zahlungsbeträge im Journal anzeigen. Die Beträge werden in der Transaktionswährung angezeigt. Wenn das Zahlungsjournal beispielsweise Zahlungen sowohl in US-Dollar als auch in kanadischen Dollar enthält, werden die Gesamtzahlungen für jede Währung angezeigt. 

Das Zahlungsjournal kann gelöscht werden, nachdem es durch die Prozessautomatisierung erstellt wurde. Wenn eine Zahlung vollständig gelöscht wird, treten folgende Ereignisse auf:

- Der Status der Prozessautomatisierung für die Woche bleibt **Abgeschlossen**.
- Der Prozess entfernt die Zahlungssummen und der Link **Zahlungen anzeigen** wird durch eine Schaltfläche **Ergebnisse anzeigen** ersetzt.
- Wenn Sie die Ergebnisse anzeigen, erhalten Sie eine Nachricht, dass das ursprüngliche Journal gelöscht wurde.

Nach dem Löschen einer Zahlung werden die Rechnungen wieder zur Zahlung geöffnet. Anschließend kann ein neues Ereignis erstellt werden, um die Rechnungen erneut zu bezahlen.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Automatisierung von Lieferantenzahlungsvorschlägen bearbeiten

Mit dem Prozessautomatisierungsframework können Sie die Zahlung, die Serie und die Vorkommen bearbeiten, die für den Zahlungsvorschlag erstellt wurden. Die Serie kann entweder von der Seite **Prozessautomatisierung** oder Wochenansicht der Prozessautomatisierung bearbeitet werden. Wenn der AP-Manager beispielsweise beschließt, alle Schecks für inländische Anbieter am Mittwoch statt am Montag zu generieren, kann er ein Ereignis in der Wochenansicht finden und **Anzeigen/Bearbeiten – Serie** auswählen. Wenn Sie eine Serie bearbeiten, werden Sie vom System aufgefordert, anzugeben, ob die Änderung an allen vorhandenen Vorkommen oder nur an neuen Vorkommen vorgenommen werden soll. Historische Ereignisse, die bereits den Status **Abgeschlossen** haben oder in einem Status **Fehler** endeten, werden nicht geändert.

Sie können auch ein neues Vorkommen hinzufügen oder ein vorhandenes Vorkommen ändern. Das nächste Auftreten von Zahlungsvorschlägen ist beispielsweise für Mittwoch, den 1. Januar, geplant, aber dieses Datum ist ein Feiertag. Sie können das Ereignis entweder von der Seite **Prozessautomatisierung** oder Wochenansicht der Prozessautomatisierung bearbeiten. Es wird eine Seite geöffnet, auf der die Zeitplandetails und Zahlungsvorschlagskriterien aufgeführt sind. Hier können Sie die geplante Uhrzeit und das Datum bearbeiten. Sie können auch die Kriterien für Zahlungsvorschläge bearbeiten, wenn Änderungen erforderlich sind. Wenn Sie beispielsweise das geplante Datum des Zahlungsvorgangs vom 1. bis 2. Januar ändern, möchten Sie möglicherweise auch die relativen Daten für das Datum bis ändern.

Sie können auch ein Ereignis oder eine Serie deaktivieren. Um ein Ereignis zu deaktivieren und die Verarbeitung dafür auszusetzen, wählen Sie es in der Wochenansicht der Prozessautomatisierung aus und wählen Sie dann **Deaktivieren**. Sie können eine Serie auf der Seite **Prozessautomatisierung** deaktivieren.

## <a name="security-for-payment-proposal-automations"></a>Sicherheit für die Automatisierung von Lieferantenzahlungsvorschlägen

Die folgenden Aufgaben und Berechtigungen wurden für die Automatisierung von Lieferantenzahlungsvorschlägen hinzugefügt. Diese Aufgaben und Berechtigungen sind die Standardsicherheitseinstellungen, können jedoch je nach den Anforderungen Ihres Unternehmens geändert werden. Wenn beispielsweise nicht nur der AP-Manager, sondern auch der AP-Zahlungsmitarbeiter die Wiederholung eines Zeitplans bearbeiten und erstellen kann, weisen Sie die Berechtigung **Zeitplanereignisse pflegen** gegenüber der Person in der Rolle des AP-Zahlungsangestellten zu.

| Abgabe                              | Rolle                                                                       | Berechtigungen |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Zeitplanserien verwalten          | Leiter Kreditorenkonten                                                   | Diese Pflicht gewährt die Rechte zum Erstellen und Verwalten der Automatisierungsserien und -ereignisse für Zahlungsvorschläge durch die folgenden Berechtigungen:<ul><li>Zeitplanereignisse pflegen</li><li>Zeitplanserien verwalten</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Zeigen Sie die wöchentliche Ansicht der Vorkommnisse an</li></ul> |
| Abfrage zu geplanten Ereignissen | Kreditorenbuchhalter, Kreditorenbuchhaltung Zentraler Zahlungsangestellter | Diese Pflicht gewährt die Rechte zum Anzeigen der Automatisierungsserien und -ereignisse für Zahlungsvorschläge durch die folgenden Berechtigungen:<ul><li>Zeitplanereignisse anzeigen</li><li>Zeigen Sie die wöchentlichen Vorkommnisse an</li></ul> |
| Erkundigen Sie sich nach Zeitreihen      | Keiner                                                                       | Diese Pflicht gewährt die Rechte zum Anzeigen der Einstellungen der Serien und -ereignisse für die folgenden Berechtigungen:<ul><li>Zeitplanereignisse anzeigen</li><li>Zeigen Sie die Seite mit der Vorkommensliste an</li><li>Zeigen Sie die wöchentlichen Vorkommnisse an</li></ul>|
| Zeitplanereignisse pflegen     | Keiner                                                                       | Diese Pflicht gewährt das Recht, ein Ereignis durch die folgenden Berechtigungen zu erstellen und aufrechtzuerhalten:<ul><li>Zeitplanereignisse pflegen</li><li>Zeigen Sie die wöchentlichen Vorkommnisse an</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]