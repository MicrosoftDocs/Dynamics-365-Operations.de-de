---
title: Umsatzerlös- und Ausgabenstundungen in der Abonnementabrechnung
description: In diesem Thema wird erklärt, wie Sie Umsatzerlös- und Ausgabenstundungen in der Abonnementabrechnung einrichten.
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
ms.openlocfilehash: 9a12cf52d904db0396aa9914b8e324060289710f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690947"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Umsatzerlös- und Ausgabenstundungen in der Abonnementabrechnung

In diesem Thema wird erklärt, wie Sie Umsatzerlös- und Ausgabenstundungen in der Abonnementabrechnung einrichten und verwenden. Stundungszeitpläne basieren immer auf einem zugrunde liegenden Ursprungsbeleg oder Abrechnungszeitplan und sind auch davon abhängig. Da sie basierend auf Standardwerten erstellt werden, können sie nicht separat eingegeben oder erstellt werden.

Der Vorgang zum Einrichten und Verwenden von Umsatzerlös- und Ausgabenstundungen findet auf mehreren Seiten statt:

- Auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** können Sie die Firmenpräferenzen definieren.
- Auf der Seite **Standardstundungseinstellungen** können Sie die Standardkonten und -vorlagen einrichten, die für die Stundungszeitpläne verwendet werden.
- Auf der Seite **Stundungsvorlagen** und **Ereignisbasierte Stundungsvorlagen** können Sie die Vorlagen definieren, die für die Stundungszeitpläne verwendet werden.
- Auf der Seite **Alle Stundungszeitpläne** können Sie jeden Stundungszeitplan anzeigen und bearbeiten.

Umsatzerlös- und Ausgabenstundungen können zusammen mit der wiederkehrenden Vertragsabrechnung verwendet werden.

## <a name="revenue-and-expense-deferral-parameters"></a>Parameter für Umsatzerlös- und Ausgabenstundung

Die Seite **Parameter für Umsatzerlös- und Ausgabenstundung** enthält die folgenden Felder.

| Feld | Description |
|---|---| 
| Registerkarte **Zeitplan** | |
| Pro Zeitraum angleichen | <p>Geben Sie an, ob die Anzahl der Tage in einem Zeitraum verwendet wird, wenn der Betrag pro Zeitraum für einen Stundungszeitplan berechnet wird:</p><ul><li>**Ja** – Der Betrag für jeden Zeitraum ist gleich, unabhängig von der Anzahl der Tage im Zeitraum. Teilzeiträume (z. B. Zeiträume zu Beginn oder am Ende eines Stundungszeitplans) werden anteilig berechnet.</li><li>**Nein** – Der Betrag wird basierend auf der Anzahl der Tage in jedem Zeitraum berechnet.</li></ul><p>Sie können diese Einstellung auf Transaktionsebene überschreiben.</p> |
| Stundungsoption für Verkaufsrabatt | <p>Geben Sie an, ob separate Stundungszeitpläne für den Rabatt und die Auftragsbeträge erstellt werden:</p><ul><li>**Separater Zeitplan für Rabatt** – Der Rabattbetrag wird vom Umsatzerlösbetrag getrennt gehalten.<p>In diesem Fall werden beim Anlegen eines Auftrags zwei Stundungszeitpläne erstellt und dann gebucht. Die Rabatt- und Umsatzerlösbeträge werden auf verschiedene Stundungskonten gebucht.</p></li><li>**Rabatt mit Umsatzerlös zusammenführen** – Der Rabattbetrag wird mit dem Umsatzerlösbetrag kombiniert. Ein Stundungszeitplan wird erstellt, und sowohl der Rabattbetrag als auch der Umsatzerlösbetrag werden auf dasselbe Stundungskonto gebucht.<p>In diesem Fall wird beim Anlegen eines Auftrags ein Stundungszeitplan erstellt und dann gebucht. Sowohl der Rabattbetrag als auch der Umsatzerlösbetrag werden auf dasselbe Stundungskonto gebucht.</p></li></ul><p>**Hinweis:** Um Rabatte auf Artikel anzuwenden, die die Funktion für nicht abgerechnete Umsatzerlöse verwenden, wählen Sie die Option **Separater Zeitplan für Rabatt** aus. Rabatte können dann auf alle Artikel angewendet werden, unabhängig davon, ob die Funktion für nicht abgerechnete Umsatzerlöse verwendet wird. Wenn die Option **Rabatt mit Umsatzerlös zusammenführen** ausgewählt ist, können Rabatte nicht auf Artikel angewendet werden, die die Funktion für nicht abgerechnete Umsatzerlöse verwenden.</p> |
| Stundungsoption für Einkaufsrabatt | <p>Geben Sie an, ob separate Stundungszeitpläne für den Rabatt und die Bestellbeträge erstellt werden:</p><ul><li>**Separater Zeitplan für Rabatt** – Der Rabattbetrag wird vom Ausgabenbetrag getrennt gehalten.<p>In diesem Fall werden beim Anlegen einer Bestellung zwei Stundungszeitpläne erstellt und dann gebucht. Die Rabatt- und Ausgabenbeträge werden auf verschiedene Stundungskonten gebucht.</p></li><li>**Rabatt mit Umsatzerlös zusammenführen** – Der Rabattbetrag wird mit dem Ausgabenbetrag kombiniert. Ein Stundungszeitplan wird erstellt, und sowohl der Rabattbetrag als auch der Ausgabenbetrag werden auf dasselbe Stundungskonto gebucht.<p>In diesem Fall wird beim Anlegen einer Bestellung ein Stundungszeitplan erstellt und dann gebucht. Sowohl der Rabattbetrag als auch der Ausgabenbetrag werden auf dasselbe Stundungskonto gebucht.</p></li></ul> |
| Vorangegangene Zeiträume konsolidieren | <p>Legen Sie fest, ob Stundungszeitplanpositionen für Vorperioden konsolidiert werden:</p><ul><li>**Ja** – Wenn das Anfangsdatum der Stundung in einem Zeitraum vor dem Transaktionsdatum liegt, werden alle Beträge bis zum Zeitraum des Transaktionsdatums in einer einzigen Stundungszeitplanposition zusammengefasst.</li><li>**Nein** – Die Beträge aller Zeiträume werden in separaten Stundungszeitplanpositionen geführt.<p>Liegt das Startdatum der Stundung im selben oder in einem späteren Zeitraum als das Transaktionsdatum, hat diese Option keine Auswirkung.</p></li></ul><p>Diese Einstellung kann auf Transaktionsebene aktualisiert werden.</p> |
| Startdatum der Standardstundung | <p>Wählen Sie die Regel aus, die verwendet wird, um das Startdatum des Stundungszeitplans zu bestimmen:</p><ul><li>**Transaktionsdatum** – Das Transaktionsdatum wird als Startdatum verwendet.</li><li>**Beginn des aktuellen Monats** – Der Erste des aktuellen Monats wird als Startdatum verwendet. Wenn das Transaktionsdatum der Erste eines beliebigen Monats ist, ist der Erste des aktuellen Monats das Startdatum.</li><li>**Beginn des nächsten Monats** – Der Erste des nächsten Monats wird als Startdatum verwendet. Wenn das Transaktionsdatum auf den Ersten fällt, wird das Transaktionsdatum verwendet. Andernfalls wird der Erste des nächsten Monats verwendet.</li><li>**15er-Regel** – Wenn das Transaktionsdatum zwischen dem 1. und 15. liegt, verwenden Sie den 1. des aktuellen Monats als Startdatum. Wenn das Transaktionsdatum der 16. oder später ist, verwenden Sie den Ersten des nächsten Monats als Startdatum.</li></ul><p>Diese Einstellung kann auf Transaktionsebene aktualisiert werden.</p> |
| Kurzfristige Stundungsmethode | <p>Wählen Sie die kurzfristige Stundungsmethode aus: **Keine**, **Rollierende Zeiträume** oder **Festes Jahr**.</p><p>|
| Buchungsmethode für Stundung | <p>Wählen Sie die Methode, die zum Erstellen von Stundungsbuchungen verwendet wird.</p><ul><li>**Bilanz** – Es wird die Bilanzbuchungsmethode verwendet, um Stundungsbuchungen zu erstellen.</li><li>**Gewinn und Verlust** – Es wird die Gewinn- und Verlustbuchungsmethode verwendet, um Stundungsbuchungen zu erstellen. Wenn Transaktionen gebucht werden, können Sie den Rechnungsbeleg überprüfen, um die zusätzlichen Einträge anzuzeigen, die die anfängliche Erkennung und die Erkennungsgegenbeträge ausgleichen.</li></ul> |
| Gewinn und Verlust auf Kredit zurückbuchen | <p>**Hinweis:** Dieses Feld ist nur verfügbar, wenn das Feld **Buchungsmethode für Stundung** auf **Gewinn und Verlust** festgelegt ist.</p><p>Geben Sie an, ob die Gewinn- und Verlustbeträge storniert werden, wenn eine Stornierung, Kündigung oder Rückerstattung auf einen Abrechnungsplan oder Auftrag angewendet wird:</p><ul><li>**Ja** – Die Gewinn- und Verlustbeträge werden storniert. Es wird ein Kreditanpassungsbetrag auf den Stundungszeitplan angewendet.<p>Erfolgt die Stornierung in der Mitte eines Abrechnungszeitraums, werden die Beträge anteilig berechnet.</p></li><li>**Nein** – Für die Gewinn- und Verlustbeträge wird keine Stornobuchung erstellt, wenn eine Stornierung, Kündigung oder Rückerstattung auf einen Abrechnungsplan oder Auftrag angewendet wird.</li></ul> |
| Registerkarte **Erkennung** | |
| Allgemeine Erfassungen automatisch buchen | <p>Legen Sie fest, ob Journalbuchungen, die durch Umsatzerlös- und Ausgabenstundungen erstellt werden, automatisch gebucht werden sollen:</p><ul><li>**Ja** – Journaleinträge, die durch Umsatzerlös- und Ausgabenstundungen erstellt werden, sollen automatisch gebucht werden.<p>**Tipp:** Durch die Auswahl von **Ja** können Sie dazu beitragen, Buchhaltungsinkonsistenzen zu vermeiden, die durch manuelle Änderungen an Belegen verursacht werden.</p></li><li>**Nein** – Journaleinträge, die durch Umsatzerlös- und Ausgabenstundungen erstellt werden, sollen nicht automatisch gebucht werden. Sie müssen Journaleinträge manuell buchen.</li></ul> |
| Erkennungsjournal zusammenfassen | <p>Geben Sie an, ob Erkennungsbelege standardmäßig konsolidiert werden:</p><ul><li>**Ja** – Es wird ein einziger Beleg für alle Erkennungspositionen mit demselben Datum erstellt. Alle Positionen in einem Beleg, die dasselbe Konto haben, werden in einer einzigen Position zusammengefasst.</li><li>**Nein** – Es wird ein Beleg für jede Erkennungsposition erstellt.</li></ul><p>Sie können diese Einstellung auf der Seite **Erkennungsverarbeitung** aktualisieren.</p> |
| Standardjournal | Wählen Sie den Journalnamen für Journale aus, die aus Umsatzerlös- und Ausgabenstundungsprozessen erstellt werden, wie z. B. der Erfassungsverarbeitung. |
| Beschreibung der Erkennungsjournalposition. | <p>Wählen Sie die Beschreibung aus, die in der Beschreibung der Erfassungsbelegposition angezeigt wird:</p><ul><li>**Datumsangaben der Zeitplanposition** – Die Datumsangaben der Zeitplanposition werden in der Erfassungspositionsbeschreibung angezeigt.</li><li>**Details der ursprünglichen Transaktion** – Die ursprünglichen Transaktionsinformationen werden in der Erfassungspositionsbeschreibung angezeigt.<p>**Beispiel:** USMF-0001, CIV-00839, Umsatzerlös aus Software</p></li></ul> |
| Registerkarte **Nummernkreise** | Verwenden Sie diese Registerkarte, um die Standardwerte für Leasingnummernkreise festzulegen. Der Assistent zur Generierung von Nummernkreisen dient zum automatischen Generieren und Zuweisen von Nummernkreisen. Sie müssen den Nummernkreis nicht ändern. Es sei denn, Sie möchten manuelle Änderungen an den generierten Nummernkreisen vornehmen. |
| Zeitplannummer | Die für Stundungszeitpläne verwendete Nummer im Nummernkreis. |

## <a name="deferral-templates"></a>Stundungsvorlagen

Auf der Seite **Stundungsvorlagen** können Sie einfache Vorlagen definieren, die für Stundungszeitpläne verwendet werden.

Hier einige der Vorteile der Verwendung einer Vorlage:

* Die Dauer der Stundung wird automatisch berechnet.
* Sie lassen Stundungszeitpläne zu, die über Zeiträume verfügen, in denen die Erkennung übersprungen wird.
* Sie können Stundungen automatisieren, indem Sie die Vorlage einem Produkt, einer Produktgruppe, einer Produktkategorie, Kund\*innen oder einer Kund\*innengruppe zuweisen. Die Vorlagenzuweisung erfolgt über die Seite **Standardstundungseinstellungen**.

Für Vorlagen stehen mehrere Periodenhäufigkeiten zur Verfügung: tägliche, monatliche oder steuerliche Finanzzeiträume.

Die Vorlagenzeilen bestehen aus einem Typ (**Erkannt** oder **Übersprungen**) und der Periodendauer. Übersprungene Zeilen weisen in den Stundungszeitplanpositionen einen Betrag von 0 (null) auf. Dieses Verhalten kann nützlich sein, wenn Sie Umsätze nicht in allen Perioden erfassen möchten.

### <a name="create-a-deferral-template"></a>Stundungsvorlage erstellen

Um eine Stundungsvorlage zu erstellen, befolgen Sie diese Schritte.

1. Wählen Sie auf der Seite **Stundungsvorlagen** die Option **Neu** aus.
2. Geben Sie im Feld **Vorlage** einen Namen ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Wählen Sie im Feld **Periodenhäufigkeit** die Periodenhäufigkeit aus.
5. Wählen Sie **Hinzufügen** aus, um eine Zeile oben in der Liste der Zeilen hinzuzufügen, oder wählen Sie **Anhängen** aus, um eine Zeile am Ende der Liste hinzuzufügen.
6. Wählen Sie im Feld **Typ** die Art des Zeitraums aus.
7. Geben Sie im Feld **Länge des Zeitraums** die Länge des Zeitraums ein.
8. Wiederholen Sie die Schritte 5 bis 7 für jede zusätzliche Zeile, die Sie benötigen.
9. Wählen Sie **Speichern** aus.

## <a name="deferral-defaults"></a>Standardstundungseinstellungen

Verwenden Sie die Seite **Standardstundungseinstellungen** zum Einrichten von Standardstundungskonten für Artikel sowie zum Zuweisen von Standardvorlagen zu stundbaren Artikeln. Sie können auch Stundungskonten für Gebühren einrichten und den stundbaren Gebühren Vorlagen zuweisen.

**Nach Artikel stunden**

Bei Buchungen mit einem Artikel (z. B. Aufträgen) können Sie Konten und Vorlagen bestimmten Artikeln und Kund\*innen zuweisen. Diese Einstellungen werden als Standardwerte verwendet, wenn eine Buchung gestundet wird. Um die Buchung standardmäßig stundbar zu machen, müssen Sie die Artikel auf der Seite **Stundbare Artikel** einrichten.

**Nach Konto stunden**

Bei Buchungen ohne Artikel (z. B. allgemeinen Erfassungen) können Sie die Stundungskonten angeben. Wenn diese Konten in einer Buchungsposition verwendet werden, wird die Buchung automatisch als gestundet markiert. Die entsprechende Vorlage und das Erkennungskonto werden der Buchungsposition zugewiesen.

**Alle Buchungsarten (z. B. auf den Registerkarten „Auftrag“, „Einkauf“ und „Allgemeine Erfassung“)**

Die Konten auf der Seite sind die Hauptkonten, die keine Finanzdimensionen haben. Die Finanzdimensionen des Erkennungskontos stammen von Kund\*innen bzw. dem Artikel basierend auf Ihrer Organisation.

Jede Vorlagenzeile muss entweder über eine lineare Vorlage oder eine ereignisbasierte Vorlage verfügen. Sie kann nicht beides haben.

### <a name="for-sales-orders"></a>Für Aufträge gilt:

Führen Sie die folgenden Schritte aus, um die Stundungsstandardwerte für Aufträge anzugeben.

1. Wählen Sie auf der Registerkarte **Auftrag** die Stundungsart aus.
2. Wählen Sie **Hinzufügen** aus, um eine Position hinzuzufügen.
3. Wählen Sie im Feld **Artikelcode** den Artikelcode aus. Der Artikelcode bestimmt, wie die Stundungsstandardwerte angewendet werden.
4. Geben Sie an, wie der Artikelcode angewendet wird:

    * Wenn das Feld **Artikelcode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Artikelrelation im Feld **Artikelrelation** aus.
    * Wenn das Feld **Artikelcode** auf **Kategorie** festgelegt ist, wählen Sie die Kategorierelation im Feld **Kategorierelation** aus.
    * Wenn das Feld **Artikelcode** auf **Alle** festgelegt ist, gelten die Standardwerte für alle zutreffenden Datensätze.

5. Geben Sie an, wie der Kontocode angewendet wird:

    * Wenn das Feld **Kontocode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Kontobeziehung im Feld **Kontobeziehung** aus.
    * Wenn das Feld **Kontocode** auf **Alle** festgelegt ist, gilt das Konto für alle Datensätze.

6. Wählen Sie im Feld **Hauptkonto** das Hauptkonto für die Stundung aus.
7. Wenn das Feld **Buchungsmethode für Stundung** auf **Gewinn und Verlust** festgelegt ist, wählen Sie das anfängliche Umsatzerlöskonto im Feld **Anfängliches Umsatzerlöskonto** und das Erlösgegenkonto im Feld **Erlösgegenkonto** aus.
8. Wenn das Feld **Kurzfristige Stundungsmethode** auf **Rollierende Zeiträume** oder **Festes Jahr** festgelegt ist, wählen Sie das kurzfristige Stundungskonto im Feld **Kurzfristiges Stundungskonto** aus.
9. Bei einer Vorlage können Sie **Hinzufügen** auswählen, um eine Zeile hinzuzufügen.
10. Wählen Sie im Feld **Artikelcode** den Artikelcode aus.
11. Geben Sie an, wie der Artikelcode angewendet wird:

    * Wenn das Feld **Artikelcode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Artikelrelation im Feld **Artikelrelation** aus.
    * Wenn das Feld **Artikelcode** auf **Kategorie** festgelegt ist, wählen Sie die Kategorierelation im Feld **Kategorierelation** aus.
    * Wenn das Feld **Artikelcode** auf **Alle** festgelegt ist, gelten die Standardwerte für alle zutreffenden Datensätze.

12. Geben Sie an, wie der Kontocode angewendet wird:

    * Wenn das Feld **Kontocode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Kontobeziehung im Feld **Kontobeziehung** aus.
    * Wenn das Feld **Kontocode** auf **Alle** festgelegt ist, gilt das Konto für alle betreffenden Datensätze.
    * Wählen Sie die lineare Vorlage im Feld **Lineare Vorlage** oder die ereignisbasierte Vorlage im Feld **Ereignisbasierte Vorlage** aus.

13. Wählen Sie **Speichern** aus.

### <a name="for-purchase-orders"></a>Bei Bestellungen

Führen Sie die folgenden Schritte aus, um die Stundungsstandardwerte für Bestellungen anzugeben.

1. Wählen Sie auf der Registerkarte **Einkauf** die Stundungsart aus.
2. Wählen Sie **Hinzufügen** aus, um eine Position hinzuzufügen.
3. Wählen Sie im Feld **Artikelcode** den Artikelcode aus.
4. Geben Sie an, wie der Artikelcode angewendet wird:

    * Wenn das Feld **Artikelcode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Artikelrelation im Feld **Artikelrelation** aus.
    * Wenn das Feld **Artikelcode** auf **Kategorie** festgelegt ist, wählen Sie die Kategorierelation im Feld **Kategorierelation** aus.
    * Wenn das Feld **Artikelcode** auf **Alle** festgelegt ist, gelten die Standardwerte für alle zutreffenden Datensätze.

5. Geben Sie an, wie der Kontocode angewendet wird:

    * Wenn das Feld **Kontocode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Kontobeziehung im Feld **Kontobeziehung** aus.
    * Wenn das Feld **Kontocode** auf **Alle** festgelegt ist, gilt das Konto für alle betreffenden Datensätze.

6. Wählen Sie im Feld **Hauptkonto** das Hauptkonto für die Stundung aus.
7. Wenn das Feld **Buchungsmethode für Stundung** auf **Gewinn und Verlust** festgelegt ist, wählen Sie das anfängliche Umsatzerlöskonto im Feld **Anfängliches Umsatzerlöskonto** und das Erlösgegenkonto im Feld **Erlösgegenkonto** aus.
8. Wenn das Feld **Kurzfristige Stundungsmethode** auf **Rollierende Zeiträume** oder **Festes Jahr** festgelegt ist, wählen Sie das kurzfristige Stundungskonto im Feld **Kurzfristiges Stundungskonto** aus.
9. Bei einer Vorlage können Sie **Hinzufügen** auswählen, um eine Zeile hinzuzufügen. 
10. Wählen Sie im Feld **Artikelcode** den Artikelcode aus.
11. Geben Sie an, wie der Artikelcode angewendet wird:

    * Wenn das Feld **Artikelcode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Artikelrelation im Feld **Artikelrelation** aus.
    * Wenn das Feld **Artikelcode** auf **Kategorie** festgelegt ist, wählen Sie die Kategorierelation im Feld **Kategorierelation** aus.
    * Wenn das Feld **Artikelcode** auf **Alle** festgelegt ist, gelten die Standardwerte für alle zutreffenden Datensätze.

12. Geben Sie an, wie der Kontocode angewendet wird:

    * Wenn das Feld **Kontocode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Kontobeziehung im Feld **Kontobeziehung** aus.
    * Wenn das Feld **Kontocode** auf **Alle** festgelegt ist, gilt das Konto für alle betreffenden Datensätze.
    * Wählen Sie die lineare Vorlage im Feld **Lineare Vorlage** oder die ereignisbasierte Vorlage im Feld **Ereignisbasierte Vorlage** aus.

13. Wählen Sie **Speichern** aus.

### <a name="for-general-journals"></a>Bei allgemeinen Erfassungen

Führen Sie die folgenden Schritte aus, um die Stundungsstandardwerte für Einträge der allgemeinen Erfassung anzugeben.

1. Wählen Sie die Registerkarte **Allgemeine Erfassung**.
2. Wählen Sie bei einer Stundung **Hinzufügen** aus, um eine Zeile hinzuzufügen.
3. Wenn das Feld **Kurzfristige Stundungsmethode** auf **Rollierende Zeiträume** oder **Festes Jahr** festgelegt ist, wählen Sie das kurzfristige Stundungskonto im Feld **Kurzfristiges Stundungskonto** aus.
4. Wählen Sie im Feld **Stundungskonto** das Stundungskonto aus.
5. Wählen Sie im Feld **Erkennungskonto** das Erkennungskonto aus.
6. Wenn das Feld **Buchungsmethode für Stundung** auf **Gewinn und Verlust** festgelegt ist, wählen Sie das anfängliche Umsatzerlöskonto im Feld **Anfängliches Umsatzerlöskonto** und das Erlösgegenkonto im Feld **Erlösgegenkonto** aus.
7. Wählen Sie die lineare Vorlage im Feld **Lineare Vorlage** oder die ereignisbasierte Vorlage im Feld **Ereignisbasierte Vorlage** aus.
8. Wählen Sie **Speichern** aus.

### <a name="for-free-text-invoices"></a>Bei Freitextrechnungen

Führen Sie die folgenden Schritte aus, um die Stundungsstandardwerte für Freitextrechnungen anzugeben.

1. Wählen Sie die Registerkarte **Freitextrechnung**.
2. Wählen Sie bei einer Stundung **Hinzufügen** aus, um eine Zeile hinzuzufügen.
3. Geben Sie an, wie der Kontocode angewendet wird:

    * Wenn das Feld **Kontocode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Kontobeziehung im Feld **Kontobeziehung** aus.
    * Wenn das Feld **Kontocode** auf **Alle** festgelegt ist, gilt der Kontocode für alle betreffenden Datensätze.

4. Wählen Sie im Feld **Stundungskonto** das Stundungskonto aus.
5. Wenn das Feld **Kurzfristige Stundungsmethode** auf **Rollierende Zeiträume** oder **Festes Jahr** festgelegt ist, wählen Sie das kurzfristige Stundungskonto im Feld **Kurzfristiges Stundungskonto** aus.
6. Wählen Sie im Feld **Erkennungskonto** das Erkennungskonto aus.
7. Wenn das Feld **Buchungsmethode für Stundung** auf **Gewinn und Verlust** festgelegt ist, wählen Sie das anfängliche Umsatzerlöskonto im Feld **Anfängliches Umsatzerlöskonto** und das Erlösgegenkonto im Feld **Erlösgegenkonto** aus.
8. Wählen Sie die lineare Vorlage im Feld **Lineare Vorlage** oder die ereignisbasierte Vorlage im Feld **Ereignisbasierte Vorlage** aus.
9. Wählen Sie **Speichern** aus.

### <a name="for-invoice-journals"></a>Bei Rechnungserfassungen

Führen Sie die folgenden Schritte aus, um die Stundungsstandardwerte für Rechnungserfassungen anzugeben.

1. Wählen Sie die Registerkarte **Rechnungserfassung** aus.
2. Wählen Sie bei einer Stundung **Hinzufügen** aus, um eine Zeile hinzuzufügen.
3. Geben Sie an, wie der Kontocode angewendet wird:

    * Wenn das Feld **Kontocode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Kontobeziehung im Feld **Kontobeziehung** aus.
    * Wenn das Feld **Kontocode** auf **Alle** festgelegt ist, gilt der Kontocode für alle betreffenden Datensätze.

4. Wählen Sie im Feld **Stundungskonto** das Stundungskonto aus.
5. Wenn das Feld **Kurzfristige Stundungsmethode** auf **Rollierende Zeiträume** oder **Festes Jahr** festgelegt ist, wählen Sie das kurzfristige Stundungskonto im Feld **Kurzfristiges Stundungskonto** aus.
6. Wählen Sie im Feld **Erkennungskonto** das Erkennungskonto aus.
7. Wenn das Feld **Buchungsmethode für Stundung** auf **Gewinn und Verlust** festgelegt ist, wählen Sie das anfängliche Umsatzerlöskonto im Feld **Anfängliches Umsatzerlöskonto** und das Erlösgegenkonto im Feld **Erlösgegenkonto** aus.
8. Wählen Sie die lineare Vorlage im Feld **Lineare Vorlage** oder die ereignisbasierte Vorlage im Feld **Ereignisbasierte Vorlage** aus.
9. Wählen Sie **Speichern** aus.

### <a name="items-that-are-deferred-by-default"></a>Standardmäßig gestundete Artikel

Verwenden Sie die Seite **Standardmäßig verzögerte Artikel**, um festzulegen, welche Artikel standardmäßig gestundet werden. Sie können die Arten der Transaktionen festlegen, für die die Artikel gestundet werden. Sie können angeben, ob ein einzelner Artikel gestundet wird oder eine ganze Artikelgruppe oder -kategorie.

Wenn Sie Artikel als gestundet festlegen, wählen Sie die Standardkonten und -vorlagen auf der Seite **Standardstundungseinstellungen** aus. Wenn die Konten und Vorlagen nicht ausgewählt sind, werden Buchungspositionen, die die diese Artikel eingegeben werden, nicht gestundet.

Für Artikel, die basierend auf der Verkaufs- oder Einkaufskategorie gestundet werden, der sie zugeordnet sind, basieren die Stundungseinstellungen auf der Kategorie. Wenn die Kategorie jedoch nicht im Feld **Kategorierelation** ausgewählt ist, werden die Stundungseinstellungen der höherrangigen Kategorie verwendet. Beispiel: Sie fügen die Verkaufskategorie **Heimvideo**, aber keine Verkaufskategorie **Fernsehen** hinzu. Wenn Sie eine Stundungsposition hinzufügen, die der Kategorie **Fernsehen** zugeordnet ist, werden die Stundungseinstellungen von **Heimvideo** für die Position verwendet.

### <a name="set-up-deferred-items"></a>Gestundete Artikel einrichten

Gehen Sie wie folgt vor, um standardmäßig gestundete Artikel einzurichten.

1. Wählen Sie auf der Seite **Standardmäßig verzögerte Artikel** die gewünschte Registerkarte aus: **Auftrag** oder **Einkauf**.
2. Wählen Sie **Hinzufügen** aus, um eine Position hinzuzufügen.
3. Wählen Sie im Feld **Artikelcode** den Artikelcode aus.
4. Geben Sie an, wie der Artikelcode angewendet wird:

    * Wenn das Feld **Artikelcode** auf **Tabelle** oder **Gruppe** festgelegt ist, wählen Sie die Artikelrelation im Feld **Artikelrelation** aus.
    * Wenn das Feld **Artikelcode** auf **Kategorie** festgelegt ist, wählen Sie die Kategorierelation im Feld **Kategorierelation** aus.

5. Wiederholen Sie die Schritte 2 bis 4 für jede zusätzliche Zeile, die Sie benötigen.
6. Wählen Sie **Speichern** aus.

## <a name="deferred-charges"></a>Gestundete Belastungen

Verwenden Sie die Seite **Stundbare Belastungen**, um festzulegen, welche Gebühren standardmäßig gestundet werden.

> [!NOTE]
> * Derzeit sind stundbare Belastungen nur für Aufträge (Verkauf) verfügbar.
> * Belastungen können nur auf Positionsebene gestundet werden. Um eine Belastung auf Auftragskopfebene zu stunden, können Sie die Belastung als gestundeten Artikel in einer separaten Position im Auftrag einrichten.
> * Um eine Belastung für eine Freitextrechnung zu stunden, müssen Sie die Belastung als separate gestundete Rechnungsposition eingeben.
> * Diese Funktion ist für Supportgebühren und die Umsatzerlösverteilung nicht verfügbar.

### <a name="set-up-deferred-charges"></a>Gestundete Belastungen einrichten

Gehen Sie zum Einrichten von gestundeten Belastungen folgendermaßen vor:

1. Wählen Sie auf der Seite **Stundbare Belastungen** die Option **Hinzufügen** aus, um eine Zeile hinzuzufügen.
2. Wählen Sie im Feld **Belastungscode** den Belastungscode aus.
3. Wählen Sie im Feld **Belastungsrelation** die Belastungsrelation aus.
4. Wiederholen Sie die Schritte 1 bis 3 für jede zusätzliche Zeile, die Sie benötigen.
5. Wählen Sie **Speichern** aus.

## <a name="event-based-deferral-templates"></a>Ereignisbasierte Stundungsvorlagen

Verwenden Sie die Seite **Ereignisbasierte Stundungsvorlagen** zum Definieren ereignisbasierter Stundungsvorlagen, die Sie in Stundungsbuchungen verwenden und auf der Seite **Standardstundungseinstellungen** zuweisen können.

### <a name="create-an-event-based-template"></a>Ereignisbasierte Vorlage erstellen

Gehen Sie wie folgt vor, um eine ereignisbasierte Stundungsvorlage zu erstellen.

1. Wählen Sie auf der Seite **Ereignisbasierte Stundungsvorlagen** die Option **Neu** aus.
2. Geben Sie im Feld **Vorlage** einen eindeutigen Namen für die Vorlage ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Wählen Sie im Feld **Umlagetyp** den Umlagetyp aus:

    * **Variabler Betrag** – Weisen Sie jeder eingegebenen Position einen bestimmten Betrag zu.
    * **Betrag angleichen** – Weisen Sie jeder eingegebenen Position den gleichen Betrag zu. 
    * **Prozentsatz** – Weisen Sie einen Betrag zu, der auf dem Prozentwert basiert, der für jede Position eingegeben wird.
    * **Vollendungsgrad in Prozent** – Weisen Sie jeder eingegebenen Position einen kumulativen Fertigstellungswert zu.
    * **Variable Menge** – Weisen Sie jeder eingegebenen Position eine bestimmte Menge zu.

5. Legen Sie die Option **Separate Ereignisse pro Einheit erstellen** auf **Ja** fest, wenn Sie möchten, dass jede Ereignisposition gleichmäßig auf die Anzahl der Einheiten in der Rechnungsbuchung aufgeteilt wird. Legen Sie sie auf **Nein** fest, wenn Sie die Ereignispositionen nicht aufteilen möchten.
6. Wählen Sie im Feld **Ablaufkonto** das Ablaufkonto aus.
7. Wählen Sie **Hinzufügen** aus, um eine Zeile oben in der Liste der Zeilen hinzuzufügen, oder wählen Sie **Anhängen** aus, um eine Zeile am Ende der Liste hinzuzufügen.
8. Geben Sie im Feld **Beschreibung** eine Beschreibung des Ereignisses ein.
9. Wenn das Feld **Umlagetyp** auf **Prozentsatz** festgelegt ist, geben Sie den Umlageprozentsatz im Feld **Zuteilung in Prozent** ein. Der Prozentsatz muss zwischen 0 und 100 liegen. Wenn Sie das Feld **Zuteilung in Prozent** leer lassen, wird der Prozentsatz als 0 betrachtet. Die Summe aller Prozentsätze wird Feld **Gesamtprozentsatz** unten auf der Seite angezeigt und muss 100 ergeben.
10. Geben Sie im Feld **Monate bis Ablauf** die Anzahl der Monate ein, die das Ereignis gültig ist. Das Ablaufdatum der Buchungsstundung wird basierend auf diesem Wert automatisch eingegeben.
11. Aktivieren Sie das Kontrollkästchen **Erkennen, wenn gebucht**, um Umsatzerlöse automatisch zu erkennen, wenn die Transaktion gebucht wird. Wenn Sie das Kontrollkästchen deaktiviert lassen, muss der Umsatzerlös manuell erkannt werden.
12. Wählen Sie im Feld **Erkennungskonto** das Erkennungskonto für das Ereignis aus, wenn das Ereignis ein anderes Konto als der gesamte Stundungszeitplan verwendet. Dieses Feld wird zusammen mit dem Kontrollkästchen **Erkennen, wenn gebucht** verwendet.
13. Wiederholen Sie die Schritte 7 bis 12 für jede zusätzliche Zeile, die Sie benötigen.
14. Wählen Sie **Speichern** aus.
