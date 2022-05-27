---
title: Stundungszeitpläne in Umsatzerlös- und Ausgabenstundungen
description: In diesem Thema werden Stundungszeitpläne in Umsatzerlös- und Ausgabenstundungen beschrieben.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9135ac733496a0c5d79669c35972c273c209f81d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685976"
---
# <a name="deferral-schedules"></a>Stundungszeitpläne

Stundungszeitpläne werden erstellt, nachdem eine Transaktion gebucht wurde.

Auf der Seite **Alle Stundungszeitpläne** oder **Aktive Stundungszeitpläne** können Sie die Details zu einem Stundungszeitpläne anzeigen. Die angezeigten Informationen hängen von der Art des Stundungszeitplans (linear oder ereignisbasiert) und der Buchungsart ab. Sie umfassen die Stundungszeitplanpositionen und die Gesamtbeträge des Stundungszeitplans. Sie können die Seite auch verwenden, um den Stundungszeitplan zu ändern.

## <a name="recognize-revenue"></a>Erkennen von Umsatzerlösen

> [!NOTE]
> - Beginnen Sie bei Schritt 1, um Umsatzerlöse für einen Stundungszeitplan zu erkennen.
> - Beginnen Sie bei Schritt 2, um Umsatzerlöse für mehrere Stundungszeitpläne zu erkennen.

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** im Raster **Zeitplanpositionen** die Positionen aus, die Sie erkennen möchten, und wählen Sie dann **Erkennen** aus.
2. Legen Sie auf der Seite **Erkennungsverarbeitung** das Feld **Erkennungsaktivität** auf **Erkennungsjournal erstellen** fest.
3. Wählen Sie im Feld **Abschnittsdatum** den Stichtag aus. Die Verarbeitung umfasst nur Positionen, deren Enddatum kleiner oder gleich dem ausgewählten Stichtag ist.
4. Wählen Sie **Filter** aus, und fügen Sie Datenfilter hinzu, sodass die Liste nur den Bereich der gewünschten Datensätze anzeigt.
5. Wählen Sie **Vorschau anzeigen**, um die Positionen anzuzeigen.
6. Wählen Sie in der Positionsliste alle Positionen aus, die Sie nicht verarbeiten möchten, und wählen Sie dann **Entfernen** aus.
7. Wählen Sie aus, ob Sie den Erfassungsjournaleintrag zusammenfassen möchten.
8. Im Abschnitt **Transaktionsdatum** können Sie das Transaktionsdatum mit einem bestimmten Datum überschreiben, an dem die Transaktion verarbeitet werden soll. Das Transaktionsdatum kann für geschlossene Perioden angegeben werden.
9. Um die Verarbeitung als Teil eines Stapels durchzuführen, wählen Sie **Stapel** aus. Legen Sie im Dialogfeld **Stapelverarbeitung** die Parameter für den Stapel fest, und wählen Sie dann **OK**, um zur Seite **Erkennungsverarbeitung** zurückzukehren. Die Umsatzerkennung wird später verarbeitet, sobald der Stapel verarbeitet wird.
10. Wählen Sie **Verarbeiten** aus. Wenn Sie die Transaktion keinem Stapel hinzugefügt haben, werden alle Positionen sofort verarbeitet. Andernfalls werden die Positionen verarbeitet, sobald der Stapel verarbeitet wird.

## <a name="modify-a-schedule"></a>Zeitplan ändern

Um einen Stundungszeitplan zu ändern, gehen Sie wie folgt vor.

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** den gewünschten Stundungszeitplan aus, und wählen Sie dann **Buchhaltung \> Zeitplan ändern** aus.
2. Bearbeiten Sie auf der Seite **Zeitplan ändern** die gewünschten Optionen. Je nach Stundungszeitplan können Sie nicht alle Optionen bearbeiten.
3. Wählen Sie **Vorschau** aus, um die Änderungen am Stundungszeitplan zu überprüfen.
4. Wählen Sie **OK** aus.

### <a name="straight-line-deferral-schedules"></a>Lineare Stundungszeitpläne

Wenn der Stundungszeitplan keine erkannten oder extern gebuchten Positionen enthält, können Sie den gesamten Stundungszeitplan einschließlich des Startdatums ändern.

Wenn der Stundungszeitplan erkannte oder extern gebuchte Positionen enthält und Sie den Stundungszeitplan ändern, hängt das daraus resultierende Verhalten des Stundungszeitplans vom Neuberechnungsdatum und dem Stundungsenddatum der erkannten Positionen ab. Standardmäßig bestimmt die erste nicht erkannte Periode das Stundungsenddatum.

Um das Erkennungsdatum zu verwenden, wählen Sie einen der folgenden Werte im Feld **Start des Zeitplans** aus: 
- **Ausgleich** – Der Betrag, nachdem alle erkannten Positionen neu berechnet wurden.
- **Stornierung** – Alle Positionen nach dem Neuberechnungsdatum werden storniert, indem der angegebene Erfassungsname und das Buchungsdatum verwendet werden. Der Betrag nach dem Neuberechnungsdatum wird dann neu berechnet.

Wenn eine Vorlage verwendet wird, werden die übersprungenen Perioden ignoriert und die Vorlage wird nur zur Berechnung des Enddatums verwendet.

### <a name="event-based-deferral-schedules"></a>Ereignisbasierte Stundungszeitpläne

Bei einem ereignisbasierten Stundungszeitplan können Sie alle nicht erkannten Positionen ändern.

Wenn der Stundungszeitplan erkannte oder extern gebuchte Positionen enthält, können Sie die Vorlage und den Umlagetyp für den Stundungszeitplan nicht ändern. Wenn Sie einen vorhandenen Stundungszeitplan ändern, können Sie den Wert im Feld **Separate Ereignisse pro Einheit erstellen** nicht ändern.

Wird eine Position erkannt oder extern gebucht, wird das Kontrollkästchen **Erkannt** aktiviert.

## <a name="modify-a-deferral-or-recognition-account"></a>Stundungs- oder Erkennungskonto ändern

Gehen Sie wie folgt vor, um das Stundungs- oder Erkennungskonto für einen Stundungszeitplan zu ändern.

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** den gewünschten Stundungszeitplan aus, und wählen Sie dann **Buchhaltung \> Konto ändern** aus.
2. Wählen Sie auf der Seite **Konto ändern** das Konto aus, das Sie ändern möchten (Stundung, kurzfristig oder Erkennung).
3. Wählen Sie im Feld **Neues Konto** das neue Konto aus.
4. Wählen Sie aus, ob Änderungen am Konto Regulierungserfassungen erstellen sollen.
5. Wenn Sie im vorherigen Schritt die Option auf **Ja** festgelegt haben, wählen Sie im Feld **Erfassungsname** den Erfassungsnamen aus, und geben Sie das Transaktionsdatum in das Feld **Transaktionsdatum** ein.
6. Wählen Sie **OK** aus.

## <a name="put-a-deferral-schedule-on-hold"></a>Stundungszeitplan sperren

Um einen Stundungszeitplan zu sperren, gehen Sie wie folgt vor.

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** den gewünschten Stundungszeitplan aus, und wählen Sie dann **Sperre \> Sperre platzieren** aus.
2. Wählen Sie auf der Seite **Sperre platzieren** aus, ob der Saldo vom Stundungskonto oder vom Sperrkonto übertragen werden soll.
3. Wenn Sie sich entschieden haben, den Saldo zu übertragen, wählen Sie im Feld **Erfassungsname** den Erfassungsnamen und im Feld **Sperrkonto** das Sperrkonto aus, und geben Sie das Transaktionsdatum in das Feld **Transaktionsdatum** ein.
4. Wählen Sie **OK** aus.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Sperre von einem Stundungszeitplan entfernen

Gehen Sie wie folgt vor, um eine Sperre von einem Stundungszeitplan zu entfernen.

1. Wählen Sie in der Liste **Alle Stundungszeitpläne** den gewünschten Stundungszeitplan aus, und wählen Sie dann **Sperre \> Sperre entfernen** aus.
2. Wählen Sie im Feld **Erfassungsname** den Namen der Erfassung aus.
3. Geben Sie im Feld **Transaktionsdatum** das Transaktionsdatum ein.
4. Wählen Sie **OK** aus.

## <a name="cancel-unrecognized-amounts"></a>Nicht erkannte Beträge stornieren

> [!NOTE]
> Bereits erkannte oder extern gebuchte Positionen sind von diesem Prozess ausgenommen.

Um nicht erkannte Beträge in einem Stundungszeitplan zu stornieren, gehen Sie wie folgt vor.

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** den gewünschten Stundungszeitplan aus, und wählen Sie dann **Stornieren \> Nicht erkannte Beträge** aus.
2. Geben Sie auf der Seite **Nicht realisierten Betrag stornieren** an, ob Stornierungseinträge erstellt werden sollen.
3. Wenn Sie sich entschieden haben, Stornierungseinträge zu erstellen, wählen Sie im Feld **Erfassungsname** den Erfassungsnamen und im Feld **Stornierungskonto** das Stornierungskonto aus, und geben Sie das Transaktionsdatum in das Feld **Transaktionsdatum** ein.
4. Wählen Sie **OK** aus.

## <a name="cancel-a-completed-schedule"></a>Abgeschlossenen Zeitplan stornieren

Verwenden Sie die Seite **Alle Stundungszeitpläne**, um alle erfassten oder extern gebuchten Beträge zu stornieren und den Stundungszeitplan zu stornieren, um eine weitere Erkennung zu verhindern.

Um einen ganzen Stundungszeitplan zu stornieren, gehen Sie wie folgt vor.

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** den gewünschten Stundungszeitplan aus, und wählen Sie dann **Stornieren \> Zeitplan abschließen** aus.
2. Geben Sie auf der Seite **Gesamten Zeitplan stornieren** an, ob Stornierungseinträge erstellt werden sollen.
3. Wenn Sie sich entschieden haben, Stornierungseinträge zu erstellen, wählen Sie im Feld **Erfassungsname** den Erfassungsnamen und im Feld **Stornierungskonto** das Stornierungskonto aus, und geben Sie das Transaktionsdatum in das Feld **Transaktionsdatum** ein.
4. Wählen Sie **OK** aus.

## <a name="reverse-transactions"></a>Transaktionen stornieren

> [!NOTE]
> - Beginnen Sie bei Schritt 1, um die Umsatzerkennung für einen Stundungszeitplan zu stornieren.
> - Beginnen Sie bei Schritt 2, um die Umsatzerkennung für mehrere Stundungszeitpläne zu stornieren.

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** im Raster **Zeitplanpositionen** die Positionen aus, deren Erkennung Sie aufheben möchten, und wählen Sie dann **Stornieren** aus.
2. Legen Sie auf der Seite **Erkennungsverarbeitung** das Feld **Erkennungsaktivität** auf **Erkennungsjournal stornieren** fest.
3. Wählen Sie im Feld **Abschnittsdatum** den Stichtag aus. Die Verarbeitung umfasst nur Positionen, deren Enddatum kleiner oder gleich dem angegebenen Stichtag ist.
4. Wählen Sie **Filter** aus, und fügen Sie Datenfilter hinzu, sodass die Liste nur den Bereich der gewünschten Datensätze anzeigt.
5. Wählen Sie **Vorschau anzeigen**, um die Positionen anzuzeigen.
6. Wählen Sie in der Positionsliste alle Positionen aus, die Sie nicht verarbeiten möchten, und wählen Sie dann **Entfernen** aus.
7. Die Felder **Name** und **Beschreibung** werden automatisch mit dem standardmäßigen Erfassungsnamen und der Beschreibung aktualisiert. Sie können die Werte je nach Bedarf ändern. Sie können auch angeben, ob Sie den Erfassungsjournaleintrag zusammenfassen möchten.
8. Im Abschnitt **Transaktionsdatum** können Sie das Transaktionsdatum mit einem bestimmten Datum überschreiben, an dem die Transaktion verarbeitet werden soll. Das Transaktionsdatum kann für geschlossene Perioden angegeben werden.
9. Um die Verarbeitung als Teil eines Stapels durchzuführen, wählen Sie **Stapel** aus. Legen Sie im Dialogfeld **Stapelverarbeitung** die Parameter für den Stapel fest, und wählen Sie dann **OK**, um zur Seite **Erkennungsverarbeitung** zurückzukehren. Die Stornierung der Umsatzerkennung wird später verarbeitet, sobald der Stapel verarbeitet wird.
10. Wählen Sie **OK** aus. Wenn Sie die Transaktion keinem Stapel hinzugefügt haben, werden alle Positionen sofort verarbeitet. Andernfalls werden die Positionen verarbeitet, sobald der Stapel verarbeitet wird.

## <a name="apply-or-unapply-a-credit-note"></a>Gutschrift anwenden oder zurücknehmen

Gehen Sie wie folgt vor, um eine Gutschrift anzuwenden:

> [!NOTE]
> Wenn Sie eine Gutschrift auf der Seite **Stundung der Auftragstransaktion** erstellen und die Option **Vorhandenen Zeitplan anpassen** auf **Ja** festlegen, wird die Gutschrift automatisch auf den Zeitplan angewendet, sobald die Gutschrift gebucht wird.

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** den gewünschten Stundungszeitplan aus.
2. Wählen Sie in der Liste **Kreditanpassungen** eine Position aus, und wählen Sie dann **Anwenden** aus.
3. Geben Sie auf der Seite **Gutschrift anwenden (Stundungen)** das Neuberechnungsdatum im Feld **Datum der Neuberechnung** sowie das Enddatum im Feld **Endtermin** ein.
4. Wählen Sie in der Liste **Header** den **Auftrag** aus, der über Gutschriften verfügt.
5. Wählen Sie in der Liste **Positionen** die Position aus.
6. Wählen Sie **OK** aus.
7. Wählen Sie **Ja** aus.

> [!NOTE]
> Um eine Gutschrift auf mehrere einzelne Artikel aus verschiedenen Rechnungen anzuwenden, müssen Sie diese Schritte wiederholen.

Gehen Sie wie folgt vor, um eine Gutschrift zurückzunehmen:

1. Wählen Sie auf der Seite **Alle Stundungszeitpläne** den gewünschten Stundungszeitplan aus.
2. Wählen Sie in der Liste **Kreditanpassungen** die Rechnung aus, und wählen Sie dann **Nicht anwenden** aus.
3. Wählen Sie **Ja** aus.

## <a name="fields"></a>Felder

Die Seite **Alle Stundungszeitpläne** enthält die folgenden Felder.

| Felder | Description |
|--------|-------------|
| **Übergeordnet** | |
| **Zeitplan** | |
| Umlagetyp | Der Umlagetyp für ereignisbasierte Stundungen lautet: **Prozentsatz** oder **Betrag**. |
| Neuklassifizierungsdatum | <p>Das letzte Datum, an dem die kurzfristige Neuklassifizierung für einen Stundungszeitplan verarbeitet wurde. Dieses Datum wird jedes Mal aktualisiert, wenn die **kurzfristige Neuklassifizierung** für den Stundungszeitplan verwendet wird.</p>Dieses Feld ist nur verfügbar, wenn die kurzfristige Stundungsmethode „Rollierende Zeiträume“ oder „Festes Jahr“ verwendet wird. |
| **Konto** | |
| Stundungskonto | Das Konto, das für den Stundungsbetrag verwendet wird. |
| Erkennungskonto | Das Konto, das für den Erkennungsbetrag verwendet wird. |
| Erkennungstyp | Der Erkennungstyp. |
| Verteilungstyp | Der Verteilungstyp. |
| **Transaktion** | |
| Erstellungsquelle | Die Quelle, von der die Buchung erstellt wurde. |
| Transaktionstyp | Die Buchungsart bzw. der Transaktionstyp. |
| Auftrag | Die Auftragsnummer. |
| Rechnung | Die Rechnungsnummer. |
| Element | Die Nummer des Artikels. |
| **Abrechnungszeitplan** | |
| Abrechnungszeitplannummer | Die Nummer des entsprechenden Abrechnungszeitplans. |
| Abrechnungspositionsstatus | Der Status der entsprechenden Abrechnungszeitplanposition. |
| Externe Referenzen | Informationen zu externen Referenzen aus dem Abrechnungszeitplan: **Extern** und **Positionsnummer**. |
| Summen | <p>Betragssummen für den Stundungszeitplan:</p><ul><li>**Langfristig** – Die Summe der langfristig gestundeten Beträge. Dieser Wert ist nur verfügbar, wenn das Feld **Kurzfristige Stundungsmethode** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Keine** festgelegt ist oder der kurzfristige Betrag größer als 0 (null) ist.</li><li>**Kurzfristig** – Die Summe der kurzfristig gestundeten Beträge. Dieser Wert ist nur verfügbar, wenn das Feld **Kurzfristige Stundungsmethode** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Keine** festgelegt ist oder der kurzfristige Betrag größer als 0 (null) ist.</li><li>**Nicht erkannt** – Die Summe der nicht erkannten Beträge für alle Positionen.</li><li>**Initialisiert** – Die Summe der extern gebuchten Beträge für alle Positionen.</li><li>**Erkannt** – Die Summe der erkannten Beträge für alle Positionen.</li><li>**Extern gebucht und erkannt** – Die Summe der extern gebuchten und erkannten Beträge für alle Positionen.</li><li>**Gesamtbetrag** – Die Summe der Beträge für alle Positionen.</li></ul> |
| **Zeitplanpositionen** | |
| Position | Der laufende Nummer der Position. |
| Startdatum der Stundung | Das Startdatum des Stundungszeitplans. |
| Enddatum für Stundung | Das Enddatum des Stundungszeitplans. |
| Betrag | Der Stundungsbetrag. |
| Extern gebucht | Ein Wert, der angibt, ob die Position extern gebucht wurde. |
| Erkannt | Ein Wert, der angibt, ob die Position erkannt wurde. |
| Lfd. Nummer | Die Stapelnummer, in der der Betrag erkannt wurde. |
| Ereignisbeschreibung | Eine Beschreibung des Ereignisses. Dieses Feld ist nur für ereignisbasierte Stundungszeitpläne verfügbar. |
| **Kreditanpassungen** | |
| Rechnung | <p>Die Rechnungsnummer.</p><p>Der Wert gibt die Rechnung für die Gutschriftsanpassung an, die bereits auf den Stundungszeitplan angewendet wurde.</p> |
| Angewendeter Betrag | Der Kreditanpassungsbetrag, der bereits auf den Stundungszeitplan angewendet wurde. |
| Übernommenes Datum | Das Datum, an dem die Kreditanpassung angewendet wurde. |
| **Regulierung** | Die Anpassungswerte werden nur angezeigt, wenn eine Gutschrift für den Stundungszeitplan verarbeitet wurde. Wenn keine Gutschrift verarbeitet wurde, werden diese Werte ausgeblendet. |
| Regulierungsbetrag | Der Anpassungsgesamtbetrag, berechnet als *Ursprünglicher Betrag* – *Zeitplanbetrag*. |
| Ursprüngliches Enddatum | Das ursprüngliche Enddatum des Stundungszeitplans. |
| Ursprünglicher Zeitplanbetrag | Der Gesamtbetrag des ursprünglichen Stundungszeitplans. |
