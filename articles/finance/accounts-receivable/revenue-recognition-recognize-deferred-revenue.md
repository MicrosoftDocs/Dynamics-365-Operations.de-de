---
title: Verzögerte Umsatzerlöse erkennen
description: Dieses Thema enthält Informationen zum Erkennen von Umsatzerlösen mithilfe der Umsatzerkennungsfunktion.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: f6b221104d7012d82a0021b6d8f9cc10fe44cb7b8f3473ab8e7ae7a89be0a5e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726109"
---
# <a name="recognize-deferred-revenue"></a>Verzögerte Umsatzerlöse erkennen

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Die Funktion zur Umsatzerkennung kann nicht mithilfe der Funktionsverwaltung aktiviert werden. Derzeit erfolgt die Aktivierung mit Konfigurationsschlüsseln.

In diesem Thema wird die Erkennung von Umsatzerlösen im Umsatzerkennungszeitplan beschrieben. Nachdem eine Rechnung für einen Auftrag gebucht wurde, wird ein Umsatzerkennungszeitplan für jede Auftragsposition erstellt, die einen Umsatzerlöszeitplan hat. Der Umsatzerlöszeitplan in einer Position wird verwendet, um zu bestimmen, ob der Umsatz der Position verzögert werden soll.

## <a name="view-revenue-recognition-schedule-details"></a>Anzeigen der Details des Umsatzerkennungszeitplans

Es gibt zwei Möglichkeiten, auf die Details des Umsatzerkennungszeitplans zuzugreifen.

- Sie können den Umsatzerkennungszeitplan direkt über einen fakturierten Auftrag öffnen. In diesem Fall werden die Informationen im Umsatzerlöszeitplan gefiltert, sodass nur die Details für den ausgewählten Auftrag angezeigt werden. Dieser Ansatz ist hilfreich, wenn Sie die Zeitplandetails für einen Auftrag prüfen.
- Sie können den Umsatzerkennungszeitplan über die Seite **Umsatzerkennung \> Periodische Aufgaben** öffnen. Dieser Ansatz wird häufig verwendet, wenn der Umsatzerlös am Ende einer Periode erfasst wird. Beim ersten Öffnen der Seite werden keine Informationen angezeigt. Verwenden Sie die Filter über dem Raster, um die anzuzeigenden Kriterien für die Zeitplandetails zu definieren. Sie können die Rechnungsdaten filtern, indem Sie einen Zeitraum, einen Auftrag, einen Debitor, eine Projektkennung oder einen Status eingeben.

[![Abbildung der Seite „Umsatzerlöszeitpläne“.](./media/revenue-recognition-schedule-page.png)](./media/revenue-recognition-schedule-page.png)

Die Finanzdimensionen der Auftragsposition werden unter dem Raster im Inforegister **Finanzdimension** angezeigt. Diese Dimensionen wurden während der Buchung in den verzögerten Umsatzerlösen berücksichtigt. Sie werden auch bei der Erfassung der Umsatzerlöse einbezogen. Welche Dimensionswerte verwendet werden, hängt von der Kontostruktur ab, die den Hauptkonten für den Umsatzerlös und den verzögerten Umsatzerlös zugewiesen wurde.

## <a name="recognize-revenue"></a>Erkennen von Umsatzerlösen

Sie erfassen den Umsatzerlös, indem Sie den Prozess **Erfassung erstellen** auf der Seite **Umsatz erkennen** ausführen. Sie können diese Seite entweder über den Auftrag oder über **Periodische Aufgaben** öffnen. Wenn der Prozess über den Auftrag ausgeführt wird, wird der Umsatzerlös nur für den ausgewählten Auftrag erfasst. Normalerweise wird stattdessen der Prozess **Periodische Aufgaben** ausgeführt, sodass der Umsatzerlös für alle gebuchten Auftragsrechnungen erfasst wird.

Um die Kriterien zur Auswahl und zum Buchen des Umsatzerlöses zu definieren, wählen Sie **Erfassung erstellen** aus, um das Dialogfeld **Erfassung erstellen** zu öffnen.

[![Erstellen von Erfassungsparameteroptionen.](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

Verwenden Sie im Dialogfeld die Optionen der Feldgruppe **Bearbeitungsdatum**, um das Buchungsdatum zur Erfassung des Umsatzerlöses festzulegen. Wenn Sie **Gewähltes Datum** auswählen, können Sie im Feld **Buchungsdatum** ein Buchungsdatum eingeben. Wenn Sie **Umsatzerlöszeitplandatum** auswählen, wird das Buchungsdatum nicht verwendet. Stattdessen wird der Wert des Feldes **Erkennungsdatum** für jede Position des Zeitplans als Buchungsdatum verwendet.

Geben Sie anschließend im Feld **Referenzdatum** das Anfangsdatum für die Erkennung von Umsatzerlösen ein. Alle Positionen des Zeitplans, die am oder vor dem Anfangsdatum liegen, werden erfasst, wenn sie nicht gesperrt sind.

Nachdem Sie die Datumsangaben festgelegt haben, klicken Sie im Dialogfeld auf **OK** aus, um die Erfassung zu erstellen. Es wird eine Meldung mit der Anzahl der erstellten Transaktionen und der Erfassung angezeigt, in der sie erstellt wurden. Die Erfassung wird nicht automatisch gebucht. Der Umsatzerkennungsmanager prüft, welche Positionen des Zeitplans erkannt werden.

Nach der Ausführung des Prozesses werden die Positionen im Zeitplan, die in die Erfassung übertragen wurden, als **Verarbeitet** gekennzeichnet. Die Markierung **Verarbeitet** gibt an, dass die Positionen in die Erfassung übertragen wurden, sie können jedoch auch gebucht werden oder die Buchung kann aufgehoben werden. Nachdem die Umsatzerkennungserfassung gebucht wurde, bleibt die Markierung **Verarbeitet** erhalten. Wenn die Umsatzerkennungserfassung oder eine Position gelöscht wird, wird auch die Markierung **Verarbeitet** entfernt. Auf diese Weise kann die Position ermittelt werden, wenn der Prozess **Erfassung erstellen** erneut ausgeführt wird.

[![Seite „Umsatzerlöserkennungszeitpläne“.](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Öffnen Sie auf der Seite **Umsatzerlöserkennungserfassung** (**Umsatzerlöserkennung \> Erfassungseinträge \> Umsatzerlöserkennungserfassung**) die **Positionen**, um die Details der erfassten Daten anzuzeigen. Es wird immer eine separate Buchung für jede Position des erfassten Zeitplans erstellt, auch wenn alle Positionen mithilfe des gleichen Sachkontos am gleichen Datum gebucht werden.

[![Seite „Erfassungsbeleg“.](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

Die Spalte **Konto** enthält das verzögerte Umsatzerlössachkonto. Dieses Sachkonto kann nicht bearbeitet werden. Durch diese Einschränkung wird sichergestellt, dass das korrekte verzögerte Umsatzerlössachkonto entlastet wird. Dieses Sachkonto wird nicht mit der Kontostruktur gegengeprüft, da es seit der letzten Buchung auf dem Umsatzerlössachkonto möglicherweise geändert wurde.

Die Spalte **Gegenkonto** enthält das Umsatzerlössachkonto. Standardmäßig wird das Umsatzerlössachkonto aus den Lagerbuchungsprofilen entnommen, und die Finanzdimensionen werden aus der Auftragsposition entnommen. Dieses Sachkonto wird mit der Struktur des aktuellen Kontos gegengeprüft. Es kann jedoch bearbeitet werden, wenn sich die Kontostruktur geändert hat und zusätzliche Finanzdimensionen erfordert.

Der Standardbetrag stammt aus der entsprechenden Position des Zeitplans und kann nicht geändert werden.

Standardmäßig wird der Wechselkurs auf den Wechselkurs der Rechnung festgelegt, wenn der Auftrag mehrere Währungen hat. Durch dieses Verhalten wird sichergestellt, dass die Buchhaltungswährungs- und Berichtswährungsbeträge vollständig entlastet werden. Aufgrund der Rundung unterscheidet sich der Wechselkurs möglicherweise für die letzte Position des Zeitplans geringfügig vom Kurs der Rechnung.

Nachdem die Umsatzerkennungserfassung gebucht wurde, wird der Beleg im Zeitplan eingegeben. Wenn es mehr als einen Beleg für die gleiche Position des Zeitplans gibt, wird ein Sternchen (\*) in der Position angezeigt. Um die Belege anzuzeigen, die für diese Position gebucht wurden, wählen Sie **Belegbuchungen** aus.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Ändern der Details des Umsatzerkennungszeitplans

Die meisten Daten im Umsatzerlöszeitplan können nicht bearbeitet werden. Neue Positionen können nicht zum Zeitplan hinzugefügt werden, und vorhandene Positionen können nicht gelöscht werden. Die Umsatzerlöszeitplandetails müssen für jede Auftragsposition verwaltet werden, um sicherzustellen, dass eine Organisation im Laufe der Zeit den Betrag erfasst, der verzögert wurde.

### <a name="edit-schedule-lines"></a>Bearbeiten der Zeitplanpositionen

Einige Änderungen sind in den Positionen des Zeitplans zulässig. Die folgenden Felder können in den Positionen geändert werden:

- **Gesperrt** – Diese Markierung kann aktiviert oder deaktiviert werden, bevor die Position verarbeitet wird. Um die Markierung zu löschen, wählen Sie die Zeile und dann **Sperre entfernen** aus. Umsatzerlös kann nicht für Positionen erkannt werden, die gesperrt sind. Positionen können automatisch gesperrt werden, wenn der Umsatzerlöszeitplan für automatische Sperren eingerichtet wird.

    [![Umsatzerlöszeitpläne – Bearbeiten von Zeitplanpositionen.](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Erkennungsdatum** – Das Erkennungsdatum kann geändert werden, solange die Position noch nicht verarbeitet wird. Wenn der Prozess, der die Erfassung zur Umsatzerlöserkennung erstellt, ausgeführt wird, wird ein Datum in das Feld **Umsatz erkennen – Referenzdatum** eingegeben. Dieses Datum wird mit dem Datum im Feld **Erkennungsdatum** verglichen, um zu bestimmen, welche Positionen erkannt werden sollen.
- **Freizugebender Betrag** – Der Betrag, der freigegeben wird, kann geändert werden, solange die Position noch nicht verarbeitet wird. Sie können den Betrag des erfassten Umsatzerlöses verringern, jedoch nicht erhöhen. Mit diesem Feld kann eine Organisation einen Teil des Umsatzerlöses am Erkennungsdatum erfassen. Bei einer Änderung des Betrags wird im Feld **Verbleibender Betrag** angezeigt, wie viel Umsatz noch erkannt werden muss.
- **Freizugebende Menge** – Wenn der Umsatzerlöszeitplan für ein Vorkommen oder einen Monat eingerichtet wurde, wird im Feld **Freizugebende Menge** die Menge für die Auftragsposition angezeigt. Dieses Feld kann auch bearbeitet werden und bietet eine weitere Möglichkeit, einen Teil des Umsatzerlöses zu erkennen. Wenn beispielsweise die Menge für eine Position „5“ lautet, können Sie die Menge überschreiben, sodass sie weniger als „5“ beträgt. Der Betrag im Feld **Freizugebender Betrag** wird proportional aktualisiert.

### <a name="update-contract-terms"></a>Aktualisieren der Vertragsbedingungen

Die Umsatzerlöszeitplandetails werden basierend auf dem Umsatzerlöszeitplan erstellt, der der Auftragsposition beim Buchen der Rechnung zugeordnet wird. Wenn der Umsatzerlöszeitplan auf der Auftragsposition falsch ist, kann er nicht im Auftrag geändert werden, nachdem der Auftrag in Rechnung gestellt wurde. Stattdessen müssen Sie die Schaltfläche **Vertragsbedingungen aktualisieren** verwenden, um den Umsatzerlöszeitplan zu ändern. Der Umsatzerlöszeitplan kann entweder vor oder nach der Erkennung des Umsatzes geändert werden.

Um den Zeitplan zu ändern, wählen Sie eine beliebige Zeitplanposition für den zu ändernden Artikel aus. In der folgenden Abbildung wird die Position für Artikel S0008 ausgewählt, der mit einem12-Monats-Umsatzerlöszeitplan gebucht wurde. Wenn Sie **Vertragsbedingungen aktualisieren** auswählen, werden in einem Dialogfeld das Vertragsstart- und -enddatum sowie der Umsatzerlöszeitplan angezeigt.

[![Vertragsstart- und -enddatum.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Ändern Sie das Vertragsstart- und -enddatum, sodass der richtige Datumsbereich wiedergegeben wird. Wenn Sie den Datumsbereich ändern, muss der Wert im Feld **Anzahl der Vorkommen** mit einem Umsatzerlöszeitplan übereinstimmen, der im System definiert wurde. In diesem Beispiel muss ein 24-Monats-Umsatzerlöszeitplan eingerichtet werden, da der Vertrag in einen 24-Monats-Vertrag geändert wurde. Da der 24-Monats-Umsatzerlöszeitplan vorhanden ist, wird er standardmäßig verwendet und kann geändert werden. Wenn kein Umsatzerlöszeitplan vorhanden ist, der über eine passende Anzahl an Vorkommen verfügt, kann der Vertrag nicht geändert werden. Nachdem Sie die Aktualisierung der Vertragsbedingungen und des Umsatzerlöszeitplans abgeschlossen haben, wählen Sie im Dialogfeld **OK** aus, um die Änderungen zu speichern.

[![Aktualisierter Vertragsdatumsbereich.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Die Vertragsänderungen haben folgende Auswirkungen auf die Umsatzerlöszeitplandetails:

- Wenn kein Umsatzerlös für das Produkt erkannt wurde, werden auch alle vorherigen Zeitplandetails entfernt und durch die neuen Umsatzerlöszeitplandetails ersetzt. Beispielsweise hatte Artikel S0008 ursprünglich 12 Positionen in den Planungsdetails. Diese 12 Positionen werden basierend auf dem neuen Umsatzerlöszeitplan entfernt und durch 24 Positionen ersetzt.
- Wenn der Umsatzerlös für das Produkt erfasst wurde, wurde ein Teil des Umsatzerlöses falsch erfasst, da die Erkennung auf dem falschen Umsatzerlöszeitplan basiert. Diese Positionen müssen storniert und auf Grundlage des neuen Zeitplans neu erkannt werden. In diesem Szenario werden neue Umsatzerlöszeitplanpositionen erstellt, die am ursprünglichen Erkennungsdatum über negative Beträge verfügen. Es werden anschließend neue Positionen erstellt, um die Beträge auf Grundlage des neuen Umsatzerlöszeitplans zu erkennen. Am 8. August 2019 wurde beispielsweise ein Umsatzerlös von 10,53 US-Dollar erkannt. Am 8. September 2019 wurde ein Umsatzerlös von 13,16 US-Dollar erkannt. Daher werden zwei neue Positionen am gleichen Datum erstellt. Eine Position ist für -10,53 US-Dollar und die andere Position für -13,16 US-Dollar. Es werden anschließend 24 neue Positionen erstellt, und der gesamte verzögerte Umsatzerlös von 160,61 US-Dollar wird auf den Positionen verteilt. Sie können Rückbuchungspositionen buchen, indem Sie den Prozess **Erfassung erstellen** ausführen.

[![Umsatzerlöserkennungszeitplan.](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]