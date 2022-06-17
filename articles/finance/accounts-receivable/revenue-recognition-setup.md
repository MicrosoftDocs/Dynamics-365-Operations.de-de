---
title: Umsatzerkennungseinstellungen
description: In diesem Artikel werden die Einrichtungsoptionen für die Umsatzerkennung und deren Auswirkungen behandelt.
author: kweekley
ms.date: 04/28/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: ef294af8d3a8f39a80b98aeba293267dcca1f29b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900012"
---
# <a name="revenue-recognition-setup"></a>Umsatzerkennungseinstellungen
[!include [banner](../includes/banner.md)]

Es wurde ein neues Modul **Umsatzerkennung** hinzugefügt, das Menüoptionen für alle erforderlichen Einstellungen enthält. In diesem Artikel werden die Einrichtungsoptionen und deren Auswirkungen behandelt.

> [!NOTE]
> Die Umsatzerkennungsfunktion ist nun über die Funktionsverwaltung standardmäßig aktiviert. Wenn Ihre Organisation diese Funktion nicht nutzt, können Sie sie im Arbeitsbereich **Funktionsverwaltung** ausschalten.
>
> Die Umsatzerkennung, einschließlich Bündelfunktion, wird in Commerce-Kanälen (E-Commerce, POS und Callcenter) nicht unterstützt. Für die Umsatzerkennung konfigurierte Artikel dürfen nicht in Bestellungen oder Transaktionen ergänzt werden, die in Commerce-Kanälen erstellt wurden.

Das Modul **Umsatzerkennung** hat folgende Einrichtungsoptionen:

- Umsatzerkennungserfassungen
- Parameter für die Umsatzerkennung
- Umsatzerlöszeitpläne 
- Bestandseinrichtung

    - Artikelgruppen und freigegebene Produkte
    - Umsatzerlöszeitplan definieren
    - Umsatzerlöspreis definieren
    - Bestandseinrichtung

        - Umsatzerlöszeitplan definieren
        - Umsatzerlöspreis definieren

    - Buchungsprofile
    - Bündel

        - Bündelkomponenten
        - Bündelartikel

- Projekteinstellungen

## <a name="revenue-recognition-journals"></a>Umsatzerkennungserfassungen

Es wurde ein neuer Erfassungstyp für Umsatzerkennung eingeführt. Diese Erfassung ist erforderlich und kommt in zwei Szenarien zum Einsatz.

Das erste Szenario tritt ein, nachdem alle vertraglichen Verpflichtungen erfüllt wurden und wenn der verzögerte Umsatzerlös erkannt wird, indem eine Umsatzerkennung basierend auf den Details des Umsatzerlöszeitplans erstellt wird. Die Erfassung enthält einen Buchhaltungseintrag, mit dem der Saldo des verzögerten Umsatzerlössachkontos auf das Umsatzerlössachkonto bewegt wird.

Das zweite Szenario findet statt, wenn eine Erfassung nach der Neuzuordnung erstellt wird. Die Neuzuordnung findet statt, wenn einem zuvor fakturierten Auftrag eine Auftragsposition hinzugefügt oder ein neuer Auftrag erstellt wird, der eine Position umfasst, die Teil des ursprünglichen Vertrags ist. Wenn eine Rechnung vor dem Hinzufügen einer neuen Auftragsposition gebucht wurde, muss ein Korrekturbuchhaltungseintrag für die gebuchte Debitorenrechnung erstellt werden.

Die Erfassung wird auf der Seite **Journale** (**Umsatzerkennung \> Einstellungen \> Journale**) eingerichtet. Der Erfassungstyp muss auf **Umsatzerkennung** festgelegt werden. 

## <a name="parameters-for-revenue-recognition"></a>Parameter für die Umsatzerkennung

Die Umsatzerkennungseinstellungen werden auf der Registerkarte **Umsatzerkennung** der Seite **Hauptbuchparameter** (**Umsatzerkennung \> Einstellungen \> Hauptbuchparameter**) konfiguriert. Folgende Einstellungen sind verfügbar:

- **Umsatzerkennungserfassungsname** – Wählen Sie die Erfassung aus, die für die Umsatzerkennung erstellt wurde. Die Erfassung ist erforderlich, wenn Umsatzerlöse aus dem Umsatzerlöszeitplan erkannt wurden oder Sie eine Neuzuordnung für einen Auftrag durchführen, der bereits fakturiert wurde.
- **Rabattzuordnungsmethode aktivieren** – Legen Sie diese Option auf **Ja** fest, um den Umsatzerlöspreis durch Zuweisung des angemessenen Marktpreises festlegen, der im Umsatzerlöspreis für jedes freigegebene Produkt definiert wird. Diese Zuteilung enthält eine Zuweisung sämtlicher Positionsrabatte der Artikel. Ist diese Option auf **Nein** festgelegt, verwendet das System den Medianpreis, der im Umsatzerlöspreis für jedes freigegebene Produkt definiert wird. Wenn die Option auf **Nein** festgelegt ist, jedoch kein Medianpreis für die freigegebenen Produkte eingerichtet wurde, erfolgt keine Zuteilung des Umsatzerlöspreises.
- **Kopfzeilenrabatte einbeziehen** – Legen Sie diese Option auf **Ja** fest, den Umsatzerlöspreis zu ermitteln, indem Sie Produkten Kopfzeilenrabatte zuweisen. Ist die Option auf **Nein** festgelegt, wird der Kopfzeilenrabatt nicht in die Umsatzerlöspreiszuteilung einbezogen.
- **Vertragsbedingungen deaktivieren** – Legen Sie diese Option auf **Ja** fest, wenn Produkte des Umsatzerlöstyps **Unterstützung nach Vertragsabschluss** freigegeben werden können, obwohl die Vertragsstart- und -enddaten nicht dafür definiert wurden. Normalerweise sind die Vertragsstart- und -enddaten für Artikel des Umsatzerlöstyps **Unterstützung nach Vertragsabschluss** erforderlich. Wenn die Vertragsstart- und -enddaten nicht definiert sind, werden die Details des Umsatzerlöszeitplans für die Buchung berechnet, indem die Anzahl der Vorkommen und das Rechnungsdatum verwendet werden.
- **Rechnungskorrekturen bei der Neuzuordnung auf Debitorenkonten buchen** – Wenn Sie die Neuzuordnung für Rechnungen ausführen, die bereits gebucht wurden, muss der Buchhaltungseintrag für gebuchte Rechnung korrigiert werden. Verwenden Sie diese Option, um anzugeben, wie die Korrektur ausgeführt werden soll.

    - Legen Sie diese Option auf **Nein** fest, um die Buchung der Korrekturtransaktion auf das Hauptbuch zu beschränken. Ist die Option auf **Nein** festgelegt, werden auch keine weiteren Dokumente für die interne Buchhaltungskorrektur in den Debitorenkonten erstellt. Sobald die Rechnung bezahlt ist, verwendet der Ausgleichsprozess den alten Buchhaltungseintrag, um mögliche Skontos bzw. erkannte Umsätze oder Verluste zu buchen.
    - Legen Sie diese Option auf **Ja** fest, um automatisch ein Rückbuchungsdokument und eine neue Rechnung für die Korrekturtransaktion in Debitorenkonten zu erstellen. Da diese Korrektur eine interne Buchhaltungskorrektur ist, werden die neuen Dokumente nicht an den Debitor gesendet oder diesem mitgeteilt. Das Rückbuchungsdokument wird mit der ursprünglichen Rechnung ausgeglichen, und die neue berichtigte Rechnung wird vom Debitor bezahlt. Beachten Sie, dass alle drei Dokumente in Berichten angezeigt werden, wie z. B. in Debitorenaufstellungen.

[![Einrichtungsinformationen.](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Umsatzerlöszeitpläne

Ein Umsatzerlöszeitplan muss für jedes Ereignis erstellt werden, durch das Umsatzerlös verzögert werden kann. Falls Ihre Organisation Support über sechs, 12, 18 und 24 Monate anbietet, müssen Sie für jede Periode einen Umsatzerlöszeitplan erstellen. Die Einstellungen des Umsatzerlöszeitplans bestimmen, wie der Umsatzerlöspreis der Anzahl von Perioden zugeteilt wird, die Sie auswählen. Sie legen weiterhin die Standarddaten fest, die für den Umsatzerlöszeitplan eingegeben werden, der beim Buchen der Rechnung erstellt wird.

Wenn Sie Umsatzerlöse nach Meilensteinen ermitteln, empfiehlt es sich, unabhängig von den Erkennungsdaten einen Umsatzerkennungszeitplan für die Anzahl der Meilensteine zu erstellen. Nachdem Sie die Zeitpläne erstellt haben, können Sie sie bearbeiten, sodass sie die erwarteten Meilensteindatumsangaben widerspiegeln. Diese Datensätze können gesperrt werden, bis Sie eine Benachrichtigung erhalten, dass die einzelnen Meilensteine erreicht wurden und Umsatz erkannt werden kann.

Umsatzerlöszeitpläne werden auf der Seite **Umsatzerlöszeitpläne** (**Umsatzerlöserkennung \> Einstellungen \> Umsatzerlöszeitpläne**) erstellt.

[![Umsatzerlöszeitpläne.](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Geben Sie in den Feldern **Umsatzerlöszeitplan** und **Beschreibung** beschreibende Werte ein. Die folgenden zusätzlichen Einstellungen werden verwendet, um den Umsatzerlöszeitplan zu erstellen, wenn die Rechnung gebucht wird.

- **Vorkommen** – Geben Sie die Anzahl der Monate oder Vorkommen für die Umsatzerlösstundung ein.
- **Automatische Sperre** – Aktivieren Sie dieses Kontrollkästchen, wenn alle Positionen des Umsatzerlösplans automatisch gesperrt werden wollen, wenn die Rechnung gebucht wird. Der Sperre muss aus jeder Position des Plans manuell entfernt werden, bevor der verzögerte Umsatzerlös der Position erkannt werden kann.
- **Automatische Vertragsbedingungen** – Aktivieren Sie dieses Kontrollkästchen, wenn das Vertragsstart-und -enddatum automatisch festgelegt werden soll. Diese Daten werden nur automatisch für freigegebene Produkte des Umsatzerlöstyps **Unterstützung nach Vertragsabschluss** festgelegt. Das Vertragsstartdatum wird automatisch auf das angeforderte Lieferdatum des Auftrags festgelegt, und das Vertragsenddatum wird automatisch auf das Startdatum zuzüglich der Anzahl der Monate oder Vorkommen festgelegt, die in den Einstellungen des Umsatzerlöszeitplans definiert sind. Beispielsweise ist das Produkt in der Auftragsposition einer einjährigen Gewährleistung zugeordnet. Der Standard-Umsatzerlöszeitplan ist **12M** (12 Monate), und das Kontrollkästchen **Automatische Vertragsbedingungen** ist für diesen Umsatzerlöszeitplan aktiviert. Wenn die Auftragsposition ein angefordertes Versanddatum vom 16. Dezember 2019 hat, wird das Standard-Vertragsstartdatum auf den 16. Dezember 2019 und das Standard-Vertragsenddatum auf den 15. Dezember 2020 festgelegt.
- **Erkennungsgrundlage** – Die Erkennungsgrundlage bestimmt, wie der Umsatzerlöspreis auf die Vorkommen verteilt wird.

    - **Monatlich nach Tagen** – Der Betrag wird auf Grundlage der tatsächlichen Tage der einzelnen Kalendermonate zugewiesen.
    - **Monatlich** – Der Betrag wird gleichmäßig auf die Anzahl der Monate zugewiesen, die in den Vorkommen definiert sind.
    - **Vorkommen** – Der Betrag wird gleichmäßig auf die Vorkommen verteilt, kann jedoch eine zusätzliche Periode enthalten, wenn Sie **Tatsächliches Startdatum** als Erkennungskonvention auswählen.
    - **Buchhaltungsperiode nach Tagen** – Der Betrag wird auf Grundlage der tatsächlichen Tage der einzelnen Buchhaltungsperioden zugewiesen. 

         - Die Ergebnisse von **Monatlich nach Tagen** und **Buchhaltungsperiode nach Tagen** sind gleich, wenn die Buchhaltungsperioden Kalendermonaten entsprechen. Die einzige Ausnahme besteht, wenn die Erkennungskonvention auf **Ende des Monat/Zeitraums** eingestellt ist und die Felder **Vertragsstartdatum** und **Enddatum** in einer Auftragsposition leer gelassen wurden.

- **Erkennungskonvention** – Die Erkennungskonvention bestimmt die Daten, die auf den Umsatzerlöszeitplan für die Rechnung angegeben sind.

    - **Tatsächliches Startdatum** – Der Zeitplan wird erstellt, indem Sie entweder das Vertragsstartdatum (für \[PCS\]-Artikel und „Unterstützung nach Vertragsabschluss“) oder das Rechnungsdatum (für wesentliche und nicht-wesentliche Artikel) verwenden.
    - **1. Tag des Monats/Zeitraums** – Das Datum der ersten Zeitplanposition ist das Vertragsstartdatum (oder das Rechnungsdatum). Allerdings werden alle folgenden Zeitplanpositionen für den ersten Tag des Monats bzw. der Buchaltungsperiode erstellt.
    - **Teilung in der Monatsmitte** – Das Datum der ersten Zeitplanposition hängt vom Rechnungsdatum ab. Wenn die Rechnung zwischen dem 1. und dem 15. des Monats gebucht wird, wird der Umsatzerlöszeitplan unter Verwendung des ersten Tag des Monats erstellt. Wenn die Rechnung zwischen dem 16. oder einem späteren Tag des Monats gebucht wird, wird der Umsatzerlöszeitplan unter Verwendung des ersten Tag des folgenden Monats erstellt.

        - **Teilung in der Monatsmitte** kann nicht ausgewählt werden, wenn die Erkennungsgrundlage auf **Buchhaltungsperiode nach Tagen** festgelegt ist.

    - **1. Tag des nächsten Monats/Zeitraums** – Das Datum, zu dem der Zeitplan beginnt, ist der erste Tag des nächsten Monats bzw. der Buchhaltungsperiode.
    - **Ende des Monats/Zeitraums** – Das Datum der ersten Zeitplanposition ist das Vertragsstartdatum (oder das Rechnungsdatum). Allerdings werden alle folgenden Zeitplanpositionen für den letzten Tag des Monats bzw. der Buchhaltungsperiode erstellt. 

Wählen Sie die Schaltfläche **Umsatzerlöszeitplandetails** aus, um die allgemeinen Perioden und die Prozentsätze anzuzeigen, die in den einzelnen Perioden berücksichtigt werden. Standardmäßig wird der Wert **Erkennungsprozentsatz** auf eine gleichmäßig festgelegte Anzahl von Perioden aufgeteilt. Wenn die Erkennungsgrundlage auf **Monatlich** festgelegt ist, kann der Erkennungsprozentsatz geändert werden. Wenn Sie den Erkennungsprozentsatz ändern, wird eine Warnmeldung angezeigt, dass die Summe nicht 100 Prozent entspricht. Wenn diese Meldung angezeigt wird, können Sie die Positionen weiter bearbeiten. Zuvor muss der Gesamtprozentsatz jedoch 100 entsprechen, damit Sie die Seite schließen können.

[![Umsatzerlöszeitplandetails.](./media/revenue-schedule-details-2nd-scrn.png)](./media/revenue-schedule-details-2nd-scrn.png)

## <a name="inventory-setup"></a>Bestandseinrichtung

Sie können Umsatzerlöse für freigegebene Produkte in Aufträgen erkennen, jedoch nicht in Verbindung mit den Verkaufskategorien auf Aufträgen oder bei Freitextrechnungen, wenn keine Artikel im Dokument enthalten sind. Die Auswahl, die Sie beim Einrichten von freigegebenen Produkten vornehmen, legt fest, wie der Umsatzerlös des Artikels erkannt wird. So bestimmt beispielsweise die Auswahl, ob der Umsatzerlöspreis zugeteilt und ob der Umsatz mittels Umsatzerlöszeitplan verzögert ist.

Die Einrichtung kann auf dem Inforegister **Umsatzerkennung** der Seite **Artikelgruppe** (**Umsatzerkennung \> Einstellungen \> Lager- und Produkteinrichtung \> Artikelgruppe**) begonnen werden. Diese Seite enthält mehrere Einstellungsfelder. Diese Felder werden verwendet, um neue Standardwerte ausschließlich für freigegebene Produkte festzulegen, die im System erstellt werden. Beim Erstellen neuer Produkte werden die hier festgelegten Werte standardmäßig für die Artikelgruppe eingegeben. Sie können die Standardwerte für freigegebene Produkte auf der Seite **Freigegebene Produkte** (**Umsatzerkennung \> Einstellungen \> Lager- und Produkteinrichtung \> Freigegebene Produkte**) überschreiben. Die für freigegebene Produkte festgelegten Standardwerte werden anschließend an den Auftrag übertragen.

## <a name="item-groups-and-released-products"></a>Artikelgruppen und freigegebene Produkte

### <a name="define-the-revenue-schedule"></a>Den Umsatzerlöszeitplan definieren

Der Umsatzerlös in einer Auftragsposition wird verzögert, wenn ein Umsatzerlöszeitplan für das freigegebene Produkt definiert und standardmäßig für die Auftragsposition verwendet wird. Wenn die Einstellung standardmäßig für das Fertigprodukt verwendet werden soll, können Sie den Umsatzerlöszeitplan auf dem Inforegister **Umsatzerkennung** der Seite **Artikelgruppe** (**Umsatzerkennung \> Einstellungen \> Lager- und Produkteinrichtung \> Artikelgruppe**) definieren. Sie können die Einstellungen für das freigegebene Produkt weiterhin auf dem Inforegister **Umsatzerkennung** der Seite **Freigegebene Produkte** (**Umsatzerkennung \> Einstellungen \> Lagereinrichtung \> Freigegebene Produkte**) definieren.

Wählen Sie im Feld **Umsatzerlöszeitplan** den Umsatzerlöszeitplan für die Periode aus, deren Umsatzerlös verzögert werden muss. Der Umsatzerlöszeitplan wird automatisch in der Auftragsposition eingegeben, und die Zeitplandetails werden erstellt, wenn die Auftragsrechnung gebucht wird.

### <a name="define-the-revenue-price"></a>Den Umsatzerlöspreis definieren

Sie können Artikelgruppen und freigegebene Produkte einrichten, indem Sie entweder die Medianpreismethode oder die Rabattzuordnungsmethode anwenden. Beide Methoden erfordern verschiedene Einstellungen auf der Seite **Freigegebene Produkte**:

- **Umsatzerlöszuteilung aktiv** – Legen Sie diese Option auf **Ja** fest, um das freigegebene Produkt in die Umsatzerlös-Zuteilungsberechnung einzubeziehen. Wenn diese Option auf **Nein** festgelegt wird, verwendet das freigegebene Produkt die Medianpreismethode, wenn der Durchschnittspreis definiert ist. Wenn der Medianpreis nicht definiert wurde, wird der Einheitenpreis in der Auftragsposition für Umsatzerlös- oder verzögerte Umsatzerlösbuchungen verwendet.
- **Umsatzerlöstyp** – Wählen Sie den Umsatzerlöstyp aus, der das freigegebene Produkt definiert:

    - **Wesentlich** – Der Artikel ist primäre Quelle des Umsatzerlöses einer Organisation. Dieser Wert ist die Standardeinstellung.
    - **Nicht wesentlich** – Der Artikel ist keine primäre Quelle des Umsatzerlöses einer Organisation. Wenn die Medianpreiseinstellungen verwendet werden, wird der Preis berechnet und dann zugewiesen. So verfügt beispielsweise ein wesentlicher Artikel über einen Festpreis, der für den Umsatz erkannt werden muss. Liegt ein Rabatt vor, wird der Rabatt aus dem Umsatz des wesentlichen Artikels berechnet, jedoch **nur** bis zum Festpreisbetrag. Der Restbetrag des Rabatts wird aus dem Umsatzerlös für unwesentliche Artikel entnommen. Alternativ dazu kann der Rabatt auch nicht aus dem Umsatzerlös des wesentlichen Artikels berechnet werden.
    - **Unterstützung nach Vertragsabschluss** – Der Artikel unterstützt andere Elemente, die im Verkauf an den Debitor enthalten sind. Der Umsatzerlöspreis wird auf die wesentlichen nicht-wesentlichen Produkte verteilt, die im Verkauf enthalten sind. Je nach Einstellung erfordern PCS-Artikel ggf. nicht, dass Vertragsstart- und -enddatum für die Auftragsposition definiert sind.

- **Vom Carve-Out ausschließen** – Legen Sie diese Option auf **Ja** fest, um anzugeben, dass der Medianpreis des Artikels nicht unterhalb des Mindestprozentsatzes oder oberhalb des Höchstprozentsatzes angepasst werden kann. Jeder Umsatzerlöspreis wird aus dem Umsatzerlöspreis eines anderen freigegebenen Produkts abgeleitet, das im Auftrag enthalten ist. Wenn die Option auf **Nein** festgelegt ist, kann der Medianpreis des Artikels nicht angepasst oder abgetrennt werden. Beachten Sie, dass Sie beim Verkauf von mehr als einem Artikel, der als Medianpreis eingerichtet wurde, mindestens ein freigegebenes Produkt festgelegt werden muss, bei dem die Option **Vom Carve-Out ausschließen** auf **Nein** eingestellt ist. Auf diese Weise gibt es mindestens einen Artikel, dem sämtliche Abweichungen im Umsatzerlöspreis zugewiesen werden können.
- **Medianpreis** – Legen Sie diese Option auf **Ja** fest, um anzugeben, dass der Umsatzerlöspreis des Artikels angepasst werden soll, sodass er dem Medianpreis entspricht, wenn er unter der angegebenen Mindest- bzw. über der Höchsttoleranz liegt, und dass der Carve-Out-Betrag den Positionen zugewiesen wird, die über Produkte verfügen, bei denen **Vom Carve-Out ausschließen** auf **Nein** festgelegt ist.

    - **Höchsttoleranz** – Geben Sie hier den prozentualen Anteil ein, der über dem Medianpreis zulässig ist.
    - **Mindesttoleranz** – Geben Sie hier den prozentualen Anteil ein, der unter dem Medianpreis zulässig ist.

Nachdem Sie alle Einstellungen für das freigegebene Produkt konfiguriert haben, müssen Sie den Umsatzerlöspreis manuell definieren, indem Sie den Zeitwertpreis oder den Medianpreis (wenn Sie die Medianpreismethode anwenden) auf der Seite **Umsatzerlöspreise** (**Umsatzerlöserkennung \> Einstellungen \> Lagereinrichtung \> Freigegebene Produkte** angeben und dann im Aktionsbereich auf der Registerkarte **Verkaufen** in der Gruppe **Umsatzerlöserkennung** die Option **Umsatzerlöspreise** auswählen).

[![Umsatzerlöspreise.](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Der Umsatzerlöspreis, der manuell auf dieser Registerkarte definiert wurde, wird verwendet, um die Umsatzerlös-Preiszuteilung für jeden Auftrag auf Basis der definierten Kriterien zu bestimmen. Jedes Kriterium wird mit der Auftragsposition abgeglichen, um den Umsatzerlöspreis festzulegen, der im Zuteilungsprozess verwendet werden soll.

- **Artikelcode** und **Artikelrelation** – Ein Umsatzerlöspreis kann für ein Einzelprodukt oder eine Gruppe von Produkten definiert werden. Wenn Sie im Feld **Artikelcode** die Option **Tabelle** auswählen, wählen Sie das freigegebene Produkt im Feld **Artikelrelation** aus. Wenn Sie im Feld **Artikelcode** die Option **Gruppe** auswählen, wählen Sie die Artikelgruppe im Feld **Artikelrelation** aus.
- **Kontocode** und **Konto-/Gruppennummer** – Ein Umsatzerlöspreis kann für alle Debitoren, einen bestimmten Debitor oder eine Debitorengruppe festgelegt werden. Wenn Sie im Feld **Kontocode** die Option **Alle** auswählen, wird der Preis für alle Debitoren verwendet. Wenn Sie im Feld **Kontocode** die Option **Tabelle** auswählen, wählen Sie den Debitoren im Feld **Konto-/Gruppennummer** aus. Wenn Sie im Feld **Kontocode** die Option **Gruppe** auswählen, wählen Sie die Debitorengruppe im Feld **Konto-/Gruppennummer** aus.
- **Währung** – Sie müssen einen separaten Umsatzerlöspreis für jede Währung eingeben, die Sie für einen Auftrag verwenden. Wenn Sie derzeit beispielsweise in US-Dollar, in kanadischen Dollar und in Euro verkaufen, müssen Sie einen Umsatzerlöspreis für alle drei Währungen definieren. Der Umsatzerlöspreis wird nicht von einer Währung, wie der Buchhaltungswährung, in eine andere Transaktionswährung übersetzt, die Sie verwenden.
- **Betrag oder Prozentsatz des Listenpreises** – Gibt an, ob der Umsatzerlöspreis als Betrag oder als Prozentsatz des Listenpreises eingerichtet wird. Wenn Sie **Prozentsatz des Listenpreises** auswählen, können Benutzer den Medianpreis als Prozentsatz des Listenpreises anstelle eines Betrags eingeben. Der Wert **Prozentsatz des Listenpreises** wird nur für freigegebene Produkte verwendet, die als PCS-Artikel eingerichtet wurden.
- **Umsatzerlöszuteilungspreis** – In Abhängigkeit vom im Feld **Betrag oder Prozentsatz des Listenpreises** ausgewählten Wert geben Sie entweder einen Betrag oder einen Prozentsatz ein, um den Umsatzerlöspreis anzugeben, der verwendet wird, um den Artikeln im Auftrag den Umsatzerlös zuzuordnen.
- **Startdatum** und **Enddatum** – Geben Sie den Datumsbereich ein, in dem der Umsatzerlöspreis aktiv ist. Diese Felder sind optional.

Wenn die Option **Rabattzuordnungsmethode aktivieren** auf der Seite **Hauptbuchparameter** auf **Ja** festgelegt ist und wenn das Feld **Umsatzerlöstyp** für Ihr freigegebenes Produkt auf **Unterstützung nach Vertragsabschluss** eingestellt ist, müssen Sie auch die Artikel angeben, die durch das freigegebene Produkt unterstützt werden. Diese Einstellung wird auf der Seite **Einstellungsgrundlage** festgelegt. (Navigieren Sie zu **Umsatzerkennung \> Einstellungen \> Bestandseinrichtung \> Freigegebene Produkte**, und wählen Sie dann im Aktionsbereich auf der Registerkarte **Verkaufen** in der Gruppe **Umsatzerkennung** die Option **Einstellungsgrundlage** aus.)

Auf der Seite **Einstellungsgrundlage** können Sie einen Datensatz für jede Artikelgruppe hinzufügen, die der Artikel unterstützt. Während der Umsatzerlöszuteilung wird der Umsatzerlöspreis auf die wesentlichen und nicht-wesentlichen Teile für den PCS-Artikel verteilt.

### <a name="posting-profiles"></a>Buchungsprofile

Drei weitere Buchungstypen bieten Unterstützung für die Umsatzerlösverzögerung. Diese Typen werden auf der Registerkarte **Auftrag** der Seite **Buchung** (**Umsatzerkennung \> Einstellungen \> Lager- und Produkteinrichtung \> Buchung**) festgelegt.

- **Verzögerter Umsatzerlös** – Geben Sie das Hauptkonto für den Umsatzerlöspreis ein, der für den verzögerten Umsatzerlös (anstelle des Umsatzerlöses) gebucht wird. Der Umsatzerlöspreis wird verzögert, wenn die Auftragsposition einen Umsatzerlöszeitplan hat.
- **Verzögerter Wareneinsatz** – Geben Sie das Hauptkonto für den Wareneinsatzbetrag ein, der für den verzögerten Wareneinsatz gebucht wird, wenn der Umsatzerlös auch verzögert wird.
- **Teilweisen Rechnungsumsatz verrechnen** – Geben Sie das Hauptkonto für das Verrechnungskonto ein, das verwendet wird, wenn der Auftrag teilweise fakturiert wird oder wenn eine Neuzuordnung erfolgt. Der Saldo dieses Kontos wird auf 0 (null) zurückgesetzt, wenn die Aufträge vollständig fakturiert wurden.

### <a name="bundles"></a>Bündel

Bündelartikel sind eindeutige freigegebene Produkte, die so eingerichtet werden, dass sie Komponenten umfassen. Die Einrichtung erfolgt mithilfe von Stücklisten (BOM)-Funktionen. Wenn ein Bündelartikel in einem Auftrag eingegeben wird, werden die einzelnen Komponenten verwendet, um die Umsatzerlöspreise und die Umsatzerlöszeitpläne zu bestimmen. Die gedruckten Dokumente für die Debitoren, wie Aufträge und Rechnungen, geben jedoch den Bündelartikel wieder.

#### <a name="bundle-components"></a>Bündelkomponenten

Die Komponenten, die im Bündel enthalten sind, müssen auf der Seite **Freigegebene Produkte** (**Umsatzerkennung \> Einstellungen \> Lager- und Produkteinrichtung \> Freigegebene Produkte**) eingerichtet werden. Diese Komponenten sind freigegebene Produkte, die auf die gleiche Weise wie Produkte eingerichtet werden müssen, die in einer Stückliste enthalten sind. So kann ein freigegebenes Produkt ein Artikel des Typs **Artikel** oder **Dienstleistung** sein. Es muss allerdings einer Artikelmodellgruppe zugewiesen werden, bei der die Option **Produkt auf Lager** auf **Ja** festgelegt ist. Weitere Informationen finden Sie in der Dokumentation zur Einrichtung von Stücklistenartikeln.

Die Komponenten müssen außerdem für die Umsatzerkennung wie Produkte eingerichtet werden, die in einem Auftrag einzeln verkauft werden können. So sollten Sie beispielsweise sicherstellen, dass der korrekte Umsatzerlöspreis für jede Komponente definiert wurde und ob dass die Preisgrundlage für PCS-Artikel eingerichtet ist.

#### <a name="bundle-items"></a>Bündelartikel

Wenn Sie einen Bündelartikel einrichten, müssen Sie zwei Felder auf der Seite **Freigegebene Produkte** (**Umsatzerkennung \> Einstellungen \> Lager- und Produkteinrichtung \> Freigegebene Produkte**) festlegen:

- Der Artikel muss im Inforegister **Entwickler** im Feld **Produktionstyp** als Stücklistenartikel eingerichtet werden.
- Der Artikel muss im Inforegister **Allgemein** im Feld **Bündel** als Bündelartikel gekennzeichnet werden.

Die Komponenten müssen dem übergeordneten Bündel-/Stücklistenartikel auf der Seite **Stücklistenversionen** zugewiesen werden. (Navigieren Sie zu **Umsatzerkennung \> Einstellungen \> Lager- und Produkteinrichtung \> Freigegebene Produkte**, und wählen Sie dann im Aktionsbereich auf der Registerkarte **Entwickler** in der Gruppe **Stückliste** die Option **Stücklistenversionen** aus.) Weitere Informationen finden Sie in der Dokumentation zur Einrichtung von Stücklisten.

[![Freigegebene Produkte, Stücklistenzeitpläne.](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Wenn der übergeordnete Bündelartikel und die Bündelkomponenten für die Zuteilung festgelegt wurden, wird der Bündelumsatzerlöspreis basierend auf den Umsatzerlös-Beitragsprozentsätzen auf die Komponenten verteilt.

## <a name="project-setup"></a>Projekteinstellungen

Die Umsatzerkennung kann auch für Aufträge verwendet werden, die durch ein Aufwandsprojekt erstellt wurden. Für Aufträge, die aus Projekten stammen, müssen Sie nur die Hauptkonten in den Projektbuchungsprofilen definieren, die verwendet werden, um Projektrechnungen zu buchen. Die Hauptkonten werden auf der Seite **Sachkontobuchungseinstellungen** (**Umsatzerkennung \> Einstellungen \> Projekteinstellungen \> Sachkontobuchungseinstellungen**) definiert.

- **Verzögerter Rechnungsumsatz** (unter **Umsatzerlöskonten**) – Geben Sie das Hauptkonto für den Umsatzerlöspreis ein, der für den verzögerten Umsatzerlös (anstelle des Umsatzerlöses) gebucht wird. Der Umsatzerlöspreis wird verzögert, wenn die Auftragsposition einen Umsatzerlöszeitplan hat.
- **Verzögerte Kosten** (unter **Kostenkonten**) – Geben Sie das Hauptkonto für den Wareneinsatzbetrag ein, der für den verzögerten Wareneinsatz gebucht wird, wenn der Umsatzerlös auch verzögert wird.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
