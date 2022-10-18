---
title: Wiederkehrende Abrechnungsparameter für Vertrag
description: In diesem Artikel wird erläutert, wie Sie die Standardwerte für Abrechnungszeitpläne einrichten, die in der wiederkehrenden Vertragsabrechnung erstellt werden. Außerdem wird erläutert, wie Abrechnungszeitplangruppen erstellt werden.
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
ms.openlocfilehash: 64d6e21c2d8c588a64f0f4cf8b7a0bafc853bcab
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644002"
---
# <a name="recurring-contract-billing-parameters"></a>Wiederkehrende Abrechnungsparameter für Vertrag

Verwenden Sie die Seite **Wiederkehrende Abrechnungsparameter für Vertrag** zum Einrichten der Standardwerte für Abrechnungszeitpläne, die in der wiederkehrenden Vertragsabrechnung erstellt werden. Alle Abrechnungszeitpläne, die Sie erstellen, verwenden zunächst diese Standardwerte. Sie können die Werte für jeden Abrechnungszeitplan jedoch nach Bedarf ändern.

## <a name="general-tab"></a>Registerkarte „Allgemeines“

1. Wählen Sie auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** auf der Registerkarte **Allgemein** im Feld **Abrechnungszeitplangruppe** eine Abrechnungszeitplangruppe aus. Informationen zum Einrichten von Abrechnungszeitplangruppen finden Sie im Abschnitt [Abrechnungszeitplangruppen](#set-up-billing-schedule-groups) weiter unten in diesem Artikel.
2. Wählen Sie im Feld **Kündigungsart** aus, wie die Schlussrechnung berechnet wird, wenn ein Abrechnungszeitplan beendet wird:

    - **Zeitplan anpassen** – Beendet den Abrechnungszeitplan am Kündigungsdatum, ändert den Status des Zeitplans zu **Letzte Abrechnung**, und passt den zugehörigen Stundungszeitplan an, indem der nicht mehr zu erfassende Betrag storniert wird. Wenn das Startdatum der Abrechnung nach dem Kündigungsdatum liegt, werden die verbleibenden Abrechnungszeiträume entfernt.
    - **Restliche Rechnung** - Addiert die verbleibenden Beträge im Abrechnungszeitplan zur Kündigungsfrist und ändert den Status des Zeitplans in **Letzte Rechnung** und aktualisiert den Stundungszeitplan. Liegt das Startdatum der Abrechnung nach dem Kündigungsdatum, wird der Gesamtbetrag aller verbleibenden Abrechnungszeiträume zum Abrechnungszeitraum addiert und die verbleibenden Abrechnungszeiträume werden entfernt.
    - **Keine Anpassung** – Beendet den Abrechnungszeitraum zum Beendigungsdatum. Es werden keine Anpassungen am Abrechnungszeitplan vorgenommen.

3. Wählen Sie im Feld **Eindeutiger Zeitplantyp** die Option **Keiner**, um anzugeben, dass Kunden auf einen einzigen Abrechnungszeitplan beschränkt sind. Wählen Sie **Pro Kunde** oder **Pro Endbenutzer** aus, um anzugeben, dass Kunden auf einen eindeutigen Zeitplan beschränkt sind.
4. Setzen Sie die Option **An Monat ausrichten** auf **Ja**, um die Detailpositionen des Abrechnungszeitplans am Monatsende auszurichten, wenn ein Abrechnungszeitplan erstellt oder aktualisiert wird. Setzen Sie es auf **Nein**, um inkrementelle Daten zu verwenden.
5. Stellen Sie die Option **Anteilige Teilzeiträume** auf **Ja**, um Rechnungsbeträge basierend auf der Anzahl der Tage im Zeitraum zuzuweisen. Stellen Sie es auf **Nein**, um in jedem Abrechnungszeitraum den gleichen Betrag zu haben, unabhängig von der Anzahl der Tage.
6. Wenn Sie die Option **Anteilige Teilzeiträume** auf **Ja** setzen, setzen Sie das Feld **Methode der anteiligen Verrechnung** auf **Täglich**, um die Beträge basierend auf der Anzahl der Tage im Zeitraum zu verteilen. Stellen Sie es auf **Monatlich**, um jeden Monat den gleichen Betrag zu haben.
7. Geben Sie an, ob neu erstellte Abrechnungszeitpläne standardmäßig gesperrt sind.

    > [!NOTE]
    > Um die Sperrung eines Abrechnungszeitplans aufzuheben, muss der Benutzer Teil einer Benutzergruppe sein. Wählen Sie **Benutzergruppenüberschreibung zum Entfernen der Sperre** aus, um eine Benutzergruppe einzurichten, wo die Option **Entfernen der Sperre zulassen** aktiviert ist.

8. Wählen Sie im Feld **Rechnungstransaktionstyp** den Standard-Rechnungstransaktionstyp für neue Abrechnungszeitpläne aus.
9. Stellen Sie die Option **Stundung an Abrechnung ausrichten** auf **Ja**, um den entsprechenden Stundungszeitplan so auszurichten, dass er die gleichen Daten wie der Abrechnungszeitplan verwendet. Setzen Sie es auf **Nein**, um verschiedene Daten zu verwenden.
10. Wenn Sie die Umsatzerlösverteilungsfunktion verwenden, legen Sie die Option **Umsatzerlösverteilung automatisch erstellen** auf **Ja**, wenn Artikel zu einem Abrechnungszeitplan hinzugefügt werden. Das Kontrollkästchen **Umsatzerlösverteilung** wird automatisch in der Abrechnungszeitplanposition aktiviert, wenn der Artikel als Artikel für Umsatzerlösverteilung eingerichtet ist. Stellen Sie die Option auf **Nein**, wenn Sie das Kontrollkästchen **Umsatzerlösverteilung** manuell auswählen möchten.
11. Stellen Sie die Option **Kundenaufteilung** auf **Ja**, um zu ermöglichen, dass ein Abrechnungszeitplan verschiedenen Kunden in Rechnung gestellt wird. Bei der Einstellung auf **Ja** ist die Option **Kundenaufteilung** in der Kopfzeile des Abrechnungszeitplans und in der Zeile des Abrechnungszeitplans verfügbar. 
12. Legen Sie die Felder für die Auftragserstellung fest:

    - Rechnungen können nach Zeitraum, Kunde oder Artikel konsolidiert werden. Jede Kombination der Werte **Ja** und **Nein** kann eingestellt werden. Rechnungen können auch nach Artikelgruppen aufgeteilt werden.
    - Für Rechnungen sind die folgenden Buchungsoptionen verfügbar:

        - **Auftrag erstellen** – Erstellt nur den Auftrag.
        - **Rechnungsbuchung anzeigen** – Fakturiert den Auftrag und öffnet eine Seite, auf der Sie die Rechnung manuell buchen können.
        - **Freitextrechnung erstellen** – Wählen Sie diese Option, wenn Sie Freitextrechnungen verwenden.
        - **Rechnung automatisch buchen** – Fakturiert den Auftrag und bucht ihn automatisch.

    - Stellen Sie die Option **Abrechnungsdatumsangaben einer Artikelbeschreibung hinzufügen** auf **Ja**, um eine Beschreibung hinzuzufügen, die das Start- und Enddatum der Abrechnung enthält.
    - Stellen Sie die Option **Nullverbrauch ausschließen** auf **Ja**, um Abrechnungszeitplanpositionen auszuschließen, die keinen Verbrauch haben. Stellen Sie sie auf **Nein**, um diese Positionen in den Auftrag aufzunehmen.
    - Stellen Sie die Option **Untergeordnete Artikel nicht ausdrucken** auf **Ja**, wenn Sie die untergeordneten Artikel einer Umsatzerlösverteilung nicht auf dem Auftrag drucken möchten. Auf der Rechnung steht nur der übergeordnete Artikel. Wenn der Nettobetrag der (ausgeblendeten) untergeordneten Positionen eine Summe ungleich Null ist, zeigt der Nettobetrag der übergeordneten Position eine Zusammenfassung der untergeordneten Positionen. Stellen Sie die Option auf **Nein**, um alle untergeordneten Artikel unter dem übergeordneten Artikel auf der Verkaufsrechnung zu drucken.

12. Legen Sie die Felder für Support und Verlängerungen fest:

    - Stellen Sie die Option **Support und Verlängerung automatisch aktivieren** auf **Ja**, um die Support- und Verlängerungsfunktion für einen Auftrag automatisch zu verwenden.
    - Wählen Sie im Feld **Support- und Verlängerungsstufe** die standardmäßige Support- und Verlängerungsstufe aus.
    - Geben Sie im Feld **Support- und Verlängerungsmenge** die standardmäßige Support- und Verlängerungsmenge an.
    - Geben Sie im Feld **Standardstartdatum für Support und Verlängerung** das Datum an, das als Standardstartdatum für Support und Verlängerungen verwendet werden soll:

        - **Transaktionsdatum** – Das Transaktionsdatum wird als Startdatum verwendet.
        - **Beginn des aktuellen Monats** – Der Erste des aktuellen Monats wird als Startdatum verwendet.
        - **Beginn des nächsten Monats** – Der Erste des nächsten Monats wird als Startdatum verwendet. Wenn das Transaktionsdatum auf den Ersten fällt, wird der Erste des aktuellen Monats verwendet.
        - **15er-Regel** – Verwendet den Ersten des aktuellen Monats als Startdatum, wenn das Transaktionsdatum zwischen dem Ersten und Fünfzehnten des Monats liegt. Wenn das Transaktionsdatum der 16. oder später ist, verwenden Sie den Ersten des nächsten Monats als Startdatum.

    - Stellen Sie die Option **Rabatt in Berechnung einbeziehen** auf **Ja**, um den Rabattbetrag in den Support- oder Verlängerungsbetrag aufzunehmen. Stellen Sie sie auf **Nein**, um den Rabattbetrag auszuschließen.
    - Wählen Sie in den Feldern **Supportfrequenz** und **Verlängerungsfrequenz** die Frequenz aus, die verwendet werden soll, wenn Support- und Verlängerungsartikel zu einem Abrechnungszeitplan hinzugefügt werden: **Täglich**, **Monatlich**, **Vierteljährlich**, **Halbjährlich** oder **Jährlich**.
    - Stellen Sie die Option **An Artikelgruppe ausrichten** auf **Ja**, um das Start- und Enddatum neuer Artikel basierend auf der Artikelgruppe an bestehenden Artikeln auszurichten.
    - Stellen Sie die Option **An nächster nicht abgerechneter Periode ausrichten** auf **Ja**, um das Anpassungsdatum für einen Verlängerungsartikel basierend auf dem Datum des nächsten nicht abgerechneten Zeitraums nach Beginn der Verlängerung zu bestimmen.
    - Stellen Sie die Option **Seriennummer kopieren** auf **Ja**, um die Artikelseriennummer aus der ursprünglichen Auftragsposition in die entsprechende Abrechnungszeitplanposition zu kopieren.

13. Wenn Sie die Eskalation für den Abrechnungszeitplan verwenden, wählen Sie die Methode aus, die für die Berechnung des Verbraucherpreisindex verwendet wird.
14. Stellen Sie die Option **Preisänderung verfolgen** auf **Ja**, wenn Sie eine Aufzeichnung von Preisänderungen in Abrechnungszeitplanpositionen wünschen. Wenn eine Abrechnungszeitplanposition manuell von „Standard“ auf „Pauschal“ geändert und ein neuer Preis eingegeben wird, werden Prüfungsinformationen in der Abrechnungszeitplanposition nachverfolgt. Legen Sie die Option auf **Nein** fest, wenn Sie diese Änderungen nicht nachverfolgen möchten.
15. Geben Sie an, ob Datensätze auf der Seite **Rechnung generieren** standardmäßig nach Start- oder Enddatum gefiltert werden.
16. Wenn Sie die Funktion **Nicht abgerechneter Umsatzerlös** verwenden, geben Sie die verwendeten Optionen an:

    - Stellen Sie die Option **Allgemeine Erfassung automatisch buchen** auf **Ja**, wenn Sie möchten, dass die allgemeine Erfassung gleichzeitig erstellt und gebucht wird. Stellen Sie sie auf **Nein**, wenn Sie die allgemeine Erfassung erstellen und dann manuell buchen möchten.
    - Wählen Sie im Feld **Standarderfassungsname** den standardmäßigen Erfassungsnamen aus, der verwendet werden soll, wenn die allgemeine Erfassung erstellt wird.
    - Wählen Sie im Feld **Kurzfristige nicht abgerechnete Methode** die kurzfristige nicht abgerechnete Methode aus, falls Sie eine verwenden. Wenn Sie **Keine** auswählen, wird die kurzfristige Funktion nicht mit nicht abgerechnetem Umsatz verwendet. Wählen Sie **Rollierende Zeiträume** aus, um immer 12 Monate zu verwenden bzw. **Festes Jahr**, um das verbleibende Geschäftsjahr zu nutzen.

17. Geben Sie die Optionen an, die verwendet werden, wenn ein Abrechnungszeitplan und seine Positionen beendet werden:

    - **Gutschrift erstellen** - Erzeugt eine Gutschrift, wenn eine Rechnungseinteilung oder eine Rechnungseinteilungszeile beendet wird.
    - **Gutschriftsanpassung** - Erzeugt eine Gutschriftsanpassung für einen Abrechnungsplan, wenn eine Zeile beendet wird. Die Gutschriftsanpassung erscheint in einem zukünftigen Abrechnungszeitraum für den Abrechnungsplan. Die Kreditanpassung passt automatisch den Rechnungsbetrag für den nächsten Abrechnungszeitraum an, bis das Guthaben im Abrechnungszeitplan fertiggestellt ist.
    - **Keine Gutschrift** - Erzeugt keine Gutschriftsanpassung oder eine Gutschrift, wenn ein Abrechnungsschema oder eine Abrechnungseinteilung beendet wird. Diese Option ist nur verfügbar, wenn die Option **Keine Anpassung** verwendet wird, um einen Abrechnungszeitplan zu beenden.
18. Wenn die Option **Einmalig kann mit Rückerstattung beenden** auf **Nein** und einen Abrechnungszeitplan mit einer Abrechnungshäufigkeit von **Einmal** eingestellt ist, ändert sich der Status der Abrechnungsplanszeile auf **Beendet**, sobald der Abrechnungsplan in Rechnung gestellt wird. Dieser Abrechnungsplan kann nicht beendet werden und es kann kein Guthaben ausgestellt werden. Wenn die Option **Einmalig kann mit Rückerstattung beenden** auf **Ja** eingestellt ist, hat der Abrechnungsplan mit einer Abrechnungshäufigkeit von **Einmal** einen **Aktiv**-Status, nachdem der Abrechnungsplan fakturiert wird. Die Abrechnungsplanposition kann beendet und eine Rückerstattung bearbeitet werden. 
19. Die in den Parametern festgelegte Option **Täglich anteilig verrechnen** wird standardmäßig auf die Massenkündigungsseite und die Beendigungsdialoge für Abrechnungsplankopfzeile sowie -position festgelegt. Sie kann während des Beendigungsprozesses geändert werden. Bei Einstellung auf **Ja** wird jeder Rückerstattungsbetrag anhand eines Tagessatzes berechnet. Bei Einstellung auf **Nein** erfolgt die Gutschrift basierend auf dem Beendigungsdatum und der Abrechnungshäufigkeit. Wenn Sie beispielsweise die monatliche Häufigkeit verwenden und der Rechnungsbetrag 100 US-Dollar pro Monat beträgt, wird der Guthabenbetrag in Schritten von 100 US-Dollar angegeben. Wenn die Abrechnungshäufigkeit einmalig ist, beträgt der Guthabenbetrag 0,00 US-Dollar. Sie müssen „Anteil täglich“ auf „Ja“ setzen, um eine Rückerstattung für die einmalige Abrechnungshäufigkeit zu erhalten. 
20. Legen Sie die Option **Kreditstundung erstellen** auf **Ja** fest, um einen neuen Stundungsplan zu erstellen, wenn ein bestehender Stundungsplan gutgeschrieben wird. Lassen Sie die Option auf **Nein**, um die Gutschrift auf dem bestehenden Stundungsplan zu erstellen.

## <a name="sequence-number-tab"></a>Registerkarte „Laufende Nummer“

Verwenden Sie die Registerkarte **Laufende Nummer** auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag**, um den Standardwert für Abrechnungszeitplannummern festzulegen. Die Standardwerte werden auf der Seite **Nummernkreise** eingestellt (**Organisationsverwaltung \> Nummernkreise \> Nummernkreise**).

## <a name="set-up-billing-schedule-groups"></a>Abrechnungszeitplangruppen einrichten

Verwenden Sie die Seite **Abrechnungszeitplangruppe**, um eine Abrechnungszeitplangruppe für die wiederkehrende Vertragsabrechnung zu erstellen. Wenn ein neuer Abrechnungszeitplan erstellt und eine Abrechnungszeitplangruppe darauf angewendet wird, werden die Werte, die auf der Seite **Abrechnungszeitplangruppe** definiert sind, als Standardwerte für den Abrechnungszeitplan eingetragen. Sie können jeden der Standardwerte für den von Ihnen erstellten Abrechnungszeitplan ändern. Sie können mehrere Abrechnungszeitplangruppen einrichten und dann eine davon als Standard-Abrechnungszeitplangruppe auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** zuweisen.

Gehen Sie folgendermaßen vor, um eine Abrechnungszeitplangruppe für die wiederkehrende Vertragsabrechnung zu erstellen.

1. Wählen Sie auf der Seite **Abrechnungszeitplangruppe** die Option **Neu**, um eine Abrechnungszeitplangruppe zu erstellen.
2. Geben Sie im Feld **Abrechnungszeitplangruppe** eine eindeutige Kennung ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Geben Sie im Feld **Abrechnungsfrequenz** an, wie oft der Abrechnungszeitplan einem Kunden in Rechnung gestellt wird: **Einmal**, **Täglich**, **Monatlich**, **Vierteljährlich**, **Halbjährlich** oder **Jährlich**.
5. Geben Sie im Feld **Abrechnungsintervall** einen Abrechnungsintervall ein. Setzen Sie zum Beispiel das Feld **Abrechnungsfrequenz** auf **Monatlich** und das Feld **Abrechnungsintervall** auf **2**, um jeden zweiten Monat abzurechnen.
6. Wählen Sie im Feld **Preisberechnungsmethode** die Standard-Preisberechnungsmethode für Artikel in diesem Abrechnungszeitplan aus:

    - **Standard** – Berechnet den Einheitspreis basierend auf der eingegebenen Gesamtmenge und verwendet die Standardpreise aus der Seite **Freigegebene Produkte** in der Produktinformationsverwaltung.
    - **Pauschal** – Wendet einen Pauschalpreis an, der in der Abrechnungszeitplanposition eingegeben wird.
    - **Ebene** – Berechnet den Einheitspreis, indem eine feste Menge in verschiedenen Preisstufen verwendet wird. Jede Ebene muss ausgefüllt werden, bevor zur nächsten Preisstufe übergegangen wird.
    - **Pauschaltarif** – Berechnet den Einheitspreis, indem eine feste Menge und erweiterte Preise für verschiedene Preisstufen verwendet wird. Der Preis, der in einem Abrechnungszeitraum berechnet wird, verwendet den erweiterten Preis, der der Eben entspricht, in der die Abrechnungsmenge vorhanden ist.

7. Wählen Sie im Feld **Positionstyp** die Artikelart für die Abrechnungsgruppe aus:

    - **Standard** – Wählen Sie diesen Wert, wenn die Menge statisch ist.
    - **Verbrauch** – Wählen Sie diesen Wert für gemessene oder Verbrauchsartikel. Wenn Sie diesen Wert auswählen, legen Sie das Feld **Nutzungsleseoption** auf **Lesen** fest, um den Wert (Ablesung) für einen Abrechnungszeitraum auf einem Zähler oder Gerät einzugeben. Der verbrauchte Wert wird auf Grundlage des vorherigen Abrechnungszeitraums und des von Ihnen eingegebenen aktuellen Messwerts berechnet.
    - **Meilenstein** – Wählen Sie diesen Wert aus, um die Funktion der Abrechnung nach Meilenstein zu verwenden. Wenn Sie diesen Wert auswählen, wählen Sie im Feld **Meilensteinvorlage** die Meilensteinvorlage aus, falls Sie eine verwenden.
    - **Verbrauch** – Wählen Sie diesen Wert aus, um den Wert einzugeben, der für einen Abrechnungszeitraum verbraucht wird.

8. Stellen Sie die Option **Separat abrechnen** auf **Ja**, um eine Kombination aus konsolidierten Rechnungen und separaten Rechnungen für denselben Kunden zu erstellen. Beispiel: Ein Kunde hat fünf Abrechnungszeitpläne. Drei davon werden auf einer einzigen Rechnung zusammengefasst, die anderen beiden erfordern jedoch jeweils eine separate Rechnung. Stellen Sie die Option auf **Nein**, um nur eine konsolidierte Rechnung für den Kunden zu erstellen.
9. Legen Sie die Option **Automatisch verlängern** auf **Ja** fest, um einen wiederkehrenden Abrechnungszeitplan nach Erstellen der Rechnung automatisch für den nächsten Abrechnungszeitraum zu verlängern. Legen Sie sie auf **Nein** fest, um den Abrechnungszeitplan manuell zu verlängern. Geben Sie im Feld **Pro Verlängerung hinzuzufügende Positionen** an, wie viele Positionen für jede Verlängerung hinzugefügt werden sollen.
10. Stellen Sie die Option **Eskalation** auf **Ja**, um *Eskalationen* (Preiserhöhungen) für die Abrechnungszeitpläne zu übernehmen, die dieser Abrechnungszeitplangruppe zugeordnet sind.
