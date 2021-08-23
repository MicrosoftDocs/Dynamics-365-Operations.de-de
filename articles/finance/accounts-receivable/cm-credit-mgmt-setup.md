---
title: Einrichtung der Parameter für das Kreditmanagement
description: In diesem Thema werden die Optionen beschrieben, mit denen Sie das Kreditmanagement konfigurieren können, um die Anforderungen Ihres Unternehmens zu erfüllen.
author: mikefalkner
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 128c23af03754791f5ed300da78099a13cb6fa0898834361d4a3e1cda41a224e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769154"
---
# <a name="credit-management-parameters-setup"></a>Einrichtung der Parameter für das Kreditmanagement

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Optionen beschrieben, mit denen Sie das Kreditmanagement konfigurieren können, um die Anforderungen Ihres Unternehmens zu erfüllen. Um mit der Verwendung der Kreditverwaltungsfunktionen zu beginnen, richten Sie die Parameter auf der Seite **Kreditmanagement- und Inkassoparameter** ein (**Kreditmanagement und Inkasso \> Einstellungen \> Kreditmanagementparameter**).

## <a name="credit-parameters"></a>Kreditparameter

Es gibt vier Inforegister im Abschnitt **Kredit**, in denen Sie die Parameter ändern können, die das Kreditmanagement steuern: **Kreditsperren**, **Kreditmanagement-Prüfung**, **Kreditmanagement-Statistiken** und **Kreditlimiten**. In den folgenden Abschnitten werden die Einstellungen beschrieben, die auf jedem Inforegister verfügbar sind.

### <a name="credit-holds"></a>Kreditsperren

- Stellen Sie die Option **Bearbeitung des Kundenauftragswerts nach Freigabe des Auftragsstopps zulassen** auf **Nein**, um zu verlangen, dass die Buchungsregeln erneut überprüft werden, wenn der Kundenauftragswert (erweiterter Preis) seit der Freigabe des Kundenauftrags aus der Warteliste erhöht wurde. .
- Im Feld **Gründe für stornierte Bestellungen** wählen Sie den Freigabegrund aus, der standardmäßig verwendet wird, wenn ein Kundenauftrag storniert wird, für den das Kreditmanagement eingestellt war.
- Stellen Sie die Option **Kreditlimit für Debitorenkreditgruppen überprüfen** auf **Ja**, um das Kreditlimit einer Debitorenkreditgruppe zu überprüfen, wenn der Kunde in einem Kundenauftrag zu einer Debitorenkreditgruppe gehört. Das Kreditlimit für die Gruppe wird überprüft, und wenn es ausreicht, wird das Kreditlimit für den Debitor überprüft.
- Setzen Sie die Option **Kreditlimit prüfen, wenn Zahlungsbedingungen erhöht werden** Option auf **Ja**, um die Rangfolge der Zahlungsbedingungen zu prüfen und festzustellen, ob die Zahlungsbedingungen auf dem Kundenauftrag von den Standardzahlungsbedingungen für den Kunden abweichen. Wenn die neuen Zahlungsbedingungen einen höheren Rang als die ursprünglichen Zahlungsbedingungen haben, wird die Bestellung im Kreditmanagement zurückgestellt.
- Setzen Sie die Option **Kreditlimit prüfen, wenn ein Abrechnungsrabatt erhöht wird** Option auf **Ja**, um die Rangfolge der Abrechnungsrabatte zu prüfen und festzustellen, ob der Skonto auf den Kundenauftrag vom Standardskonto für den Kunden abweicht. Wenn der neue Skonto einen höheren Rang als der ursprüngliche Skonto hat, wird die Bestellung im Kreditmanagement zurückgestellt.
- Im Feld **Grund für die Freigabe geänderter Aufträge** wählen Sie den Freigabegrund aus, der standardmäßig verwendet wird, wenn geänderte Aufträge automatisch aus der Kreditverwaltung freigegeben werden.
- Stellen Sie die Option **Sperrregel für abgelaufenes Kreditlimit ignorieren, wenn das Ablaufdatum leer ist** auf **Ja**, um das Verhalten der Regel **Kreditlimit abgelaufen** zu steuern. Stellen Sie die Option auf **Nein**, um eine Bestellung zu sperren, wenn das Ablaufdatum leer ist.
- In der Lagerverwaltung können Ladungen zum Zeitpunkt der Auftragserfassung angelegt werden. Stellen Sie die Option **Blockierte Ladungspositionen entfernen** auf **Nein**, um Auftragspositionen auf der Last zu lassen, wenn ein Kundenauftrag mit einer Kreditlimitsperre belegt ist. Die Ladung kann nicht verarbeitet werden, solange der Kundenauftrag mit einer Sperre belegt ist. Stellen Sie die Option auf **Ja**, um Auftragspositionen von der Last zu entfernen, wenn ein Kundenauftrag mit einer Kreditlimitsperre belegt ist. Die Last kann dann verarbeitet werden.
- Kundenaufträge können automatisch aus der Kreditmanagementprüfung freigegeben werden. Wählen Sie im Feld **Grund für die automatische Freigabe** den Freigabegrund aus, der standardmäßig verwendet wird, wenn Kundenaufträge automatisch freigegeben werden.
- Kundenaufträge können automatisch aus der Kreditmanagementprüfung freigegeben werden. Wählen Sie im Feld **Automatisch freigeben** die Option **Ohne Buchung**, um die Sperre einer Bestellung aufzuheben. Sie müssen den Prozess, der die Bestellung zurückstellt, manuell ausführen. Wählen Sie **Mit Buchung**, um den Auftrag zu buchen, indem Sie denselben Buchungsprozess verwenden, der ausgeführt wurde, als der Kundenauftrag zurückgestellt wurde.

### <a name="credit-management-checkpoint"></a>Prüfpunkt für Kreditverwaltung

Sie können den Zeitpunkt festlegen, zu dem Kundenaufträge auf Kreditprobleme geprüft werden. Das Inforegister **Kreditmanagement-Checkpoint** identifiziert die Belegbuchungsprozesse, die die Verarbeitung von Kreditverwaltungsregeln umfassen. Sie können die Kreditregeln auch überprüfen, während Sie entweder eine Pro-forma-Buchung oder eine vollständige Buchung des Kundenauftrags durchführen. Aktivieren Sie die Kontrollkästchen, um die Buchungsprozesse zu definieren, bei denen ein Auftrag zurückgestellt werden soll, wenn nach der Verarbeitung der Sperrregeln für das Kreditmanagement ein Problem festgestellt wird.

Sie können auch die Anzahl der Kulanztage festlegen, bevor die Kreditregeln erneut überprüft werden. Obwohl Sie festlegen können, dass die Kreditverwaltungsregeln beim Buchen überprüft werden, werden die Regeln für die angegebene Anzahl von Kulanztagen nicht überprüft. Beispielsweise bestätigen Sie einen Kundenauftrag am ersten Tag und geben zwei Kulanztage für den Bestätigungsschritt an. In diesem Fall werden die Kreditregeln beim nächsten Buchungsschritt (z. B. Erstellung eines Lieferscheins oder Fakturierung der Bestellung) erst am 4. Tag überprüft. Am oder nach dem vierten Tag werden die Regeln beim Buchen erneut überprüft, und die Anzahl der Kulanztage wird auf den Wert geändert, der für den nächsten Buchungsprüfpunkt angegeben ist.

Wenn Sie die Anzahl der Kulanztage nicht angeben, werden die Kreditregeln bei jedem Buchungsschritt überprüft, der für die Ausführung der Kreditverwaltungsregeln eingerichtet wurde. Wenn Sie den Kundenauftrag ohne Buchung freigeben und dann denselben Auftragsverarbeitungsschritt erneut ausführen, werden die Kreditregeln erneut überprüft. Beispielsweise wird eine Bestellung nach einer Bestätigung zurückgestellt und Sie geben sie entweder mit oder ohne Buchung frei. In diesem Fall wird die Bestellung erneut zurückgestellt, wenn Sie sie erneut bestätigen. Verwenden Sie Kulanztage, wenn die Bestellung mit dem nächsten Verarbeitungsschritt fortgesetzt werden soll, ohne dass sie erneut zurückgestellt wird.

Sie können für einige Buchungsprüfpunkte keine Kulanztage angeben, für andere jedoch keine. Sie müssen alle Buchungsprüfpunkte so einrichten, dass sie Kulanztage haben, oder Sie müssen sie alle so einrichten, dass sie keine Kulanztage haben.

- Markieren Sie das Kontrollkästchen **Buchen**, um die Kreditverwaltungsregeln auszuführen, wenn der Buchungsprüfpunkt ausgeführt wird, der in der Zeile angezeigt wird. Wenn Sie das Kontrollkästchen nicht aktivieren, werden die Regeln während des gesamten Buchungsvorgangs nur einmal überprüft.
- Wenn Sie das Kontrollkästchen **Buchen** auswählen, geben Sie die Anzahl der Kulanztage an, die vergehen sollen, bevor die Sperrregeln erneut überprüft werden. Sie können keine Kulanztage hinzufügen, wenn das Kontrollkästchen **Buchen** deaktiviert ist.
- Markieren Sie das Kontrollkästchen **Proforma**, um die Kreditverwaltungsregeln auszuführen, wenn der Proforma-Buchungsprüfpunkt ausgeführt wird, der in der Zeile angezeigt wird. In den meisten Fällen ist das Feld **Buchen** auf **Nein** gesetzt im Dialogfeld, das beim Buchen eines Kundenauftrags angezeigt wird.
- Wenn Sie das Kontrollkästchen **Buchen** auswählen, geben Sie die Anzahl der Kulanztage an, die vergehen sollen, bevor die Sperrregeln erneut überprüft werden. Sie können keine Kulanztage hinzufügen, wenn das Kontrollkästchen **Buchen** deaktiviert ist.

### <a name="credit-management-statistics"></a>Kreditverwaltungsstatistik

Mehrere Kreditmanagementstatistiken sind in der Infobox **Statistiken zum Kundenkreditmanagement** auf der Seite **Kunde** enthalten. Sie müssen mehrere Werte angeben, die zur Berechnung dieser Statistiken erforderlich sind. Geben Sie die Anzahl der Monate ein, die zur Berechnung der folgenden Werte in der Infobox **Statistiken zum Kundenkreditmanagement** verwendet werden:

1. Dauer der ausstehenden Verkäufe in Tagen 1
2. Dauer der ausstehenden Verkäufe in Tagen 2
3. Durchschnittlicher Kontostand 1
4. Durchschnittlicher Kontostand 2
5. Durchschnittliches Kreditlimit %%
6. Durchschnittliche Exposition %%

### <a name="credit-limits"></a>Kreditlimits

- Im Kreditmanagement wird das Kundenkreditlimit in der Währung des Kunden angezeigt. Sie müssen den Wechselkurstyp für das Kreditlimit in der Währung des Kunden definieren. Wählen Sie im Feld **Kreditlimit-Wechselkursart** die Art des Wechselkurses aus, mit dem das primäre Kreditlimit in das Kreditlimit des Debitors konvertiert werden soll.
- Stellen Sie die Option **Manuelle Bearbeitung von Kreditlimits zulassen** auf **Nein**, um zu verhindern, dass Benutzer Kreditlimits auf der Seite **Debitor** bearbeiten. Wenn diese Option auf **Nein** gesetzt ist, können Änderungen am Kreditlimit eines Debitors nur durch die Buchung von Transaktionen zur Anpassung des Kreditlimits vorgenommen werden.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Zahlenfolgen und gemeinsame Zahlenfolgenparameter

Für die Bearbeitung von Kreditlimitanpassungen ist eine Journal-ID erforderlich. Sie müssen die Kreditlimitanpassungsnummer hinzufügen, die zum Generieren der Journal-ID verwendet werden soll.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]