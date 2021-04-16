---
title: Rückvergütungsverwaltungsdeals
description: In diesem Thema wird beschrieben, wie Rückvergütungsverwaltungsdeal angelegt werden. Deals werden verwendet, um verschiedene Methoden und Grundlagen für die Berechnung von Rückvergütungen und Lizenzgebühren zu steuern. Dazu gehören Regeln für Ein- und Ausschlüsse.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b75743a64fef53f79159a1476c99a7035b7e4f3b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839172"
---
# <a name="rebate-management-deals"></a>Rückvergütungsverwaltungsdeals

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Rückvergütungsverwaltungsdeals werden verwendet, um verschiedene Methoden und Grundlagen für die Berechnung von Rückvergütungen und Lizenzgebühren zu steuern. Dazu gehören Regeln für Ein- und Ausschlüsse. Es gibt drei Arten von Rückvergütungsverwaltungsdeals: Debitorenrückvergütungen, Debitorenlizenzgebühren und Kreditorenrückvergütungen. Alle drei Arten verwenden ähnliche Einstellungen. Dieses Thema befasst sich mit den bestehenden Unterschieden.

## <a name="create-a-deal"></a>Einen Deal erstellen

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Alle Rückvergütungsverwaltungsdeals**. Auf der Listenseite **Alle Rückvergütungsverwaltungsdeals** können Sie Deals aller drei Arten erstellen und damit arbeiten.

    Folgen Sie alternativ einem dieser Schritte: In jedem Fall enthält die angezeigte Listenseite dieselben Einstellungen wie die Listenseite **Alle Rückvergütungsverwaltungsdeals**, ist aber nach Deals nur eines Typs gefiltert.

    - Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Debitorenrückvergütungsdeals**, um nur Debitorenrückvergütungsdeals zu erstellen.
    - Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Debitorenlizenzgebührendeals**, um nur Debitorenlizenzgebührendeals zu erstellen.
    - Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Kreditorenrückvergütungsdeals**, um nur Kreditorenrückvergütungsdeals zu erstellen.

1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Neuen Deal erstellen** die folgenden Felder fest:

    - **Rückvergütungsverwaltungsdeals** – Wenn Sie für Rückvergütungsdeals [einen Nummernkreis einrichten](rebate-management-parameters.md), wird für dieses Feld automatisch eine eindeutige, vom System generierte Kennung festgelegt. Geben Sie andernfalls eine eindeutige Kennung ein.
    - **Beschreibung** – Geben Sie eine Beschreibung für den Deal ein.
    - **Modul** – Wählen Sie den Partnertyp aus, für den der Deal gilt (*Debitor* oder *Kreditor*). Abhängig von welcher Seite aus Sie begonnen haben, wird dieses Feld möglicherweise automatisch basierend auf dem ausgewählten Deal festgelegt. In diesem Fall ist das Feld schreibgeschützt.
    - **Typ** – Wählen Sie die Art des Deals aus (*Rückvergütung* oder *Lizenzgebühr*). Abhängig von welcher Seite aus Sie begonnen haben, wird dieses Feld möglicherweise automatisch basierend auf dem ausgewählten Deal festgelegt. In diesem Fall ist das Feld schreibgeschützt.
    - **Abstimmen nach** – Wählen Sie aus, wie der Deal berechnet und abgestimmt werden soll:

        - *Deal* – Für alle Rückvergütungen und Abzüge im Deal sollte eine einzige Rückvergütung verarbeitet werden.
        - *Position* – Rückvergütungen sollten für jede Position in einem Deal verarbeitet werden.

    - **Buchungsprofil** – Wählen Sie das [Buchungsprofil](rebate-management-posting.md) aus, das für Transaktionen verwendet werden soll, bei denen der Deal gilt. Dieses Feld ist nur verfügbar, wenn das Feld **Abstimmen nach** auf *Deal* gesetzt wird. Wenn es auf *Position* eingestellt ist, weisen Sie später jeder Position, die Sie dem Deal hinzufügen, ein Profil hinzu.
    - **Buchungsprofil für Garantie** – Wählen Sie das [Buchungsprofil](rebate-management-posting.md) aus, das für Garantietransaktionen verwendet werden soll. Buchungsprofile sind für Garantietransaktionen nur erforderlich, wenn die Garantie für eine Lizenzgebühr gilt. Andernfalls wird, obwohl kein Buchungsprofil vorgeschrieben ist, wenn kein Buchungsprofil angegeben wird, ein Fehler angezeigt, wenn Garantien gebucht werden. Dieses Feld ist nur verfügbar, wenn das Feld **Typ** auf *Lizenzgebühr* gesetzt wird. 
    - **Rückvergütungsausgabe** – Wählen Sie aus, wie die Rückvergütung oder die Lizenzgebühr gezahlt werden soll:

        - *Finanziell* – Erstellen Sie eine Freitextgutschrift oder eine Kreditorenlastschrift, damit Gelder später gezahlt oder empfangen werden können. Beachten Sie, dass Rückstellungen mit Rückvergütungen verwendet werden **können**, wenn diese Option ausgewählt ist. Diese Option ist die einzig verfügbare, wenn das Feld **Typ** auf *Lizenzgebühr* gesetzt wird.
        - *Artikel* – Generieren Sie einen Auftrag für Artikel je nachdem, wie der Deal eingerichtet wurde. In diesem Auftrag wird jedem Artikel ein Preis von 0 (null) zugewiesen. Beachten Sie, dass Rückstellungen **nicht** mit Rückvergütungen verwendet werden können, wenn diese Option ausgewählt ist.

    - **Rückvergütungswährung** – Wählen Sie die Währung aus, die verwendet werden soll, wenn die Rückvergütung, der Abzug oder die Lizenzgebühr gezahlt wird.
    - **Dokumentnotizen** – Geben Sie bei Bedarf Notizen zum Deal ein.
    - **Kumulative Garantie** – Sie können diese Option nur auf *Ja* festlegen, wenn das Feld **Typ** auf *Lizenzgebühr* festgelegt ist. Diese Option wirkt sich auf die Berechnung der garantierten Abzugszahlungen aus. Hier ist ein Beispiel:

        - Die Garantie für den Deal lautet, dass ein Wert verkauft wird, der zu einer Zahlung von 10.000 EUR pro Quartal führt.
        - Die Organisation, die die Waren verkauft, verkauft einen Wert, der im ersten Quartal eine Abzugszahlung von 12.000 EUR verursacht. Das Ergebnis ist eine Lizenzgebühr für 12.000 EUR, die abzüglich der Garantie von 10.000 EUR gezahlt wird.
        - Wenn die Option **kumulative Garantie** auf *Ja* gesetzt ist, gelten die zusätzlichen Lizenzgebühren von 2.000 EUR, die im ersten Quartal gezahlt wurden, für das zweite Quartal. Daher werden dem Debitor 8.000 EUR garantiert (die Garantie von 10.000 EUR abzüglich der zusätzlichen Zahlung von 2.000 EUR).
        - In zweiten Quartal erfassen Sie Verkäufe, die eine Lizenzgebühr in Höhe von 5.000 EUR auslösen.
        - Das System identifiziert eine Zahlung in Höhe von 3.000 EUR (die Garantie in Höhe von 8.000 EUR abzüglich der 5.000 EUR gezahlter Lizenzgebühren).
        - Wenn die Option **kumulative Garantie** auf *Nein* gesetzt ist, werden jedes Quartal die vollen 10.000 EUR garantiert. Diese Garantie entspricht einer empfohlenen Zahlung von 5.000 EUR im zweiten Quartal (die Garantie in Höhe von 10.000 EUR abzüglich der gezahlten Lizenzgebühren in Höhe von 5.000 EUR).

1. Wählen Sie **OK** aus, um den Deal zu erstellen und das Dialogfeld zu schließen.

Mit dieser Prozedur wird die Kopfzeilenebene des neuen Deals erstellt. Als Nächstes fügen Sie dem Deal Positionen hinzu.

## <a name="add-lines-to-a-deal"></a>Dem Deal Positionen hinzufügen

Nachdem Sie einen Deal wie im vorherigen Abschnitt beschrieben erstellt haben, können Sie ihn auf der Listenseite öffnen. Anschließend können Sie Positionen hinzufügen, um Debitoren oder Kreditoren, Artikel, Zeitrahmen, eine Basis und Berechnungsmethoden für den Deal festzulegen. Ein Deal kann eine oder mehrere Positionen haben. Wenn ein Deal mehrere Positionen hat, haben sie im Allgemeinen den gleichen Typ oder ihnen sind dieselben Parameter zugeordnet. Der Deal hat tatsächlich keine Folgen, bis Sie ihm Positionen hinzufügen.

1. Öffnen Sie die entsprechende Listenseite mit dem Rückvergütungsdeals, wie im vorherigen Abschnitt beschrieben.
1. Suchen und öffnen Sie den Deal, an dem Sie arbeiten möchten.
1. Wählen Sie im Inforegister **Rückvergütungsverwaltung** eine der folgenden Schaltflächen aus, um dem Raster eine Deal-Position hinzuzufügen:

    - **Position hinzufügen** – Fügen Sie eine neue, leere Deal-Position hinzu.
    - **Position kopieren** – Wenn eine vorhandene Deal-Position der Deal-Position ähnelt, die Sie hinzufügen möchten, können Sie diese Schaltfläche zum Kopieren auswählen, um eine Kopie davon hinzuzufügen. Die neue Deal-Position enthält alle Einstellungen aus den zugehörigen Details zur Rückvergütungsverwaltung. Sie können dann die Einstellungen bearbeiten. Beispielsweise aktualisieren Sie normalerweise die Artikelrelation und den Rückvergütungsprozentsatz.

1. Stellen Sie die folgenden Felder für die neue Deal-Position ein:

    - **Rückvergütungsverwaltungsnummer** – Wenn Sie für Rückvergütungsverwaltungsnummern [einen Nummernkreis einrichten](rebate-management-parameters.md), wird für dieses Feld automatisch eine eindeutige, vom System generierte Kennung festgelegt. Geben Sie andernfalls eine eindeutige Kennung ein.
    - **Typ** – Der Dealtyp, für den die Position gilt (*Rückvergütung* oder *Lizenzgebühr*). Der Wert wird aus der Kopfzeile kopiert und kann nicht geändert werden.
    - **Beschreibung** – Geben Sie eine Beschreibung für die Position ein.
    - **Unternehmen** – Wählen Sie das Unternehmen (die juristische Person) aus, für das die Deal-Position gilt. Während der Verarbeitung können Benutzer nur Deal-Positionen verarbeiten, die dem Unternehmen zugeordnet sind, das sie gerade verwenden. Die Listenseite **Debitorenrückvergütungsdeals** bietet eine unternehmensübergreifende Ansicht, die auf dem Sicherheitszugriff des Benutzers basiert. Sie können Rückvergütungen jedoch nur für das Unternehmen bearbeiten und verarbeiten, das Sie gerade verwenden.
    - **Kontocode** – Wählen Sie aus, für welche Debitoren oder Kreditoren die Deal-Position gilt:

        - *Tabelle* – Die Deal-Position gilt für einen bestimmten Debitor oder Kreditor.
        - *Gruppe* – Die Deal-Position gilt für eine Gruppe von Debitoren oder Kreditoren. Weitere Informationen zum Einrichten von Gruppen finden Sie unter [Rückvergütungsverwaltungsgruppen](rebate-management-groups.md).
        - *Alle* – Die Deal-Position gilt für alle Debitoren oder Kreditoren.

    - **Kontorelation** – Wenn Sie *Tabelle* im Feld **Kontocode** gewählt haben, wählen Sie den Debitor oder Kreditor aus, für den der Deal gilt. Wenn Sie *Gruppe* ausgewählt haben, können Sie die Debitoren- oder Kreditorengruppe auswählen. Wenn Sie *Alle* ausgewählt haben, ist dieses Feld nicht verfügbar.
    - **Artikelcode** – Wählen Sie aus, für welche Artikel die Deal-Position gilt:

        - *Tabelle* – Die Deal-Position gilt für einen bestimmten Artikel.
        - *Gruppe* – Die Deal-Position gilt für eine Gruppe von Artikeln. Weitere Informationen zum Einrichten von Gruppen finden Sie unter [Rückvergütungsverwaltungsgruppen](rebate-management-groups.md).
        - *Alle* – Die Artikelposition gilt für alle Artikel.

    - **Artikelrelation** – Wenn Sie *Tabelle* im Feld **Artikelcode** gewählt haben, wählen Sie den Artikel aus, für den die Artikelposition gilt. Wenn Sie *Gruppe* ausgewählt haben, können Sie eine Artikelgruppe auswählen. Wenn Sie *Alle* ausgewählt haben, ist dieses Feld nicht verfügbar.
    - **(Lagerverwaltungsparameter)**  – Geben Sie in den verbleibenden Feldern in der Deal-Position Werte für die Lagerverwaltungsparameter an, die die im Deal enthaltenen Artikel definieren (z. B. Größe, Farbe, Stil, Standort und Lagerort des Artikels). Wählen Sie zum Hinzufügen oder Entfernen der Dimensionen im Aktivitätsbereich **Dimensionen anzeigen** aus.

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wenn Sie die Anzahl der Artikel, für die eine Deal-Position gilt, weiter einschränken möchten, wählen Sie die Position und dann das Inforegister **Rückvergütungsverwaltung** und **Filter** aus, um ein normales **Anfrage**-Dialogfeld zu öffnen.
1. Richten Sie für jede hinzugefügte Deal-Position die Berechnungsdetails und andere Details im Inforegister **Details zur Rückvergütungsverwaltung** ein, wie im nächsten Abschnitt beschrieben.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Einer Deal-Position Details zur Rückvergütungsverwaltung hinzufügen

Sie müssen für jede Position in Ihrem Deal Details im Inforegister **Details zur Rückvergütungsverwaltung** festlegen. Wählen Sie zuerst die Deal-Position im Inforegister **Rückvergütungsverwaltung** aus. Richten Sie dann die Werte für diese Deal-Position mithilfe der verschiedenen Registerkarten im Inforegister **Details zur Rückvergütungsverwaltung** ein. In den folgenden Unterabschnitten wird die Verwendung der einzelnen Registerkarten beschrieben.

### <a name="settings-on-the-general-tab"></a>Einstellungen auf der Registerkarte Allgemein

Die Registerkarte **Allgemein** im Inforegister **Details zur Rückvergütungsverwaltung** können Sie die Berechnungsmethode und die Basis für die ausgewählte Deal-Position einrichten. Diese Einstellungen steuern, ob ein Mindestkauf erforderlich ist, die einer Deal-Position zugeordneten Buchungsprofile und die Details der Berechnung. In der folgenden Tabelle werden die Felder beschrieben, die zur Verfügung stehen.

| Feld | Beschreibung |
|---|---|
| Berechnungsmethode | Wählen Sie die Methode aus, die verwendet werden soll, wenn die ausgewählte Deal-Position mit anderen Deal-Positionen kombiniert wird (*Abgestuft*, *Kumulativ*, *Rollierend* oder *Gesamt*). Der Wert dieses Felds kann das Ergebnis Ihrer Rückvergütungsberechnungen erheblich beeinflussen. Eine vollständige Beschreibung der einzelnen Methoden und Beispiele einschließlich der Auswirkungen auf die Rückvergütungsberechnung finden Sie weiter unten in diesem Thema im Abschnitt [Berechnungsmethoden für Deal-Positionen](#calc-methods). |
| Basis | Wählen Sie aus, ob die Rückvergütung basierend auf der Menge (d. h. der Gesamtzahl der gekauften oder verkauften Einheiten) oder dem Wert (d. h. dem Gesamtpreis der gekauften oder verkauften Waren) angewendet wird. |
| Transaktionstyp | <p>Wählen Sie den Punkt im Prozess aus, an dem die Berechnung erfolgen soll:</p><ul><li>*Bestellung* – Verwenden Sie die bestellte Menge oder den bestellten Wert als Grundlage für die Berechnung.</li><li>*Geliefert* – Verwenden Sie die gelieferte Menge oder den gelieferten Wert als Grundlage für die Berechnung.</li><li>*Rechnung* – Verwenden Sie die in Rechnung gestellte Menge oder den in Rechnung gestellten Wert als Grundlage für die Berechnung.</li></ul> |
| Einheit | Wenn Sie *Menge* im Feld **Basis** ausgewählt haben, wählen Sie die Einheit aus, in der die Menge angegeben werden muss. |
| Mindestbetrag | Geben Sie den Mindestbetrag ein, der pro Periode gezahlt werden muss. Sie können einen negativen Wert eingeben, um negative Rückvergütungsmengen zu berücksichtigen, wenn die Gutschriften den Umsatz der Periode übersteigen. |
| Prinzip der Rückvergütungsminderung | Wählen Sie das [Prinzip der Rückvergütungsminderung](rebate-reduction-principle.md) aus, das für die Deal-Position gilt. |
| Variantennummer | Wenn die Deal-Position für einen Artikel mit Varianten gilt, wählen Sie die Variante aus, für die die Deal-Position gilt. |
| Basis für Kreditorenrückvergütung | <p>Dieses Feld wird nur für Kreditorenrückvergütungen angezeigt (d. h. Deals bei denen das Feld **Modul** auf *Kreditor* gesetzt ist). Wählen Sie die Basis für die Kreditorenrückvergütung aus:</p><ul><li>*Bestellung* – Die Rückvergütung, die der Kreditor erhält, basiert auf der Menge oder dem Wert der Bestellung.</li><li>*Auftrag* – Der Kreditor erhält erst nach dem Verkauf der Ware eine Rückvergütung. Die Rückvergütung basiert auf der Menge oder dem Wert des Auftrags.</li></ul> |
| Preisgrundlage | <p>Dieses Feld wird nur für Kreditorenrückvergütungen angezeigt (Deals bei denen das Feld **Modul** auf *Kreditor* gesetzt ist). Wenn Sie *Auftrag* im Feld **Kreditorenrückvergütungsbasis** ausgewählt haben, wählen Sie die zutreffende Preisbasis aus:</p><ul><li><p>*FIFO* – Die periodische Aufgabe **FIFO-Einkaufpreis berechnen** muss ausgeführt werden, um die Rückvergütung zu berechnen. (Um die Aufgabe auszuführen, gehen Sie zu **Rückvergütungsverwaltung \> periodische Aufgaben \> FIFO-Einkaufpreis berechnen**.) Eine First-in-first-out-Regel (FIFO-Regel) wird verwendet, um den Wert des verkauften Bestands zu berechnen. Dieser Wert wird dann zur Berechnung der Kreditorenrückvergütungen verwendet. Hier ist ein Beispiel:</p><ul><li>**Verkaufter Bestand:** 1.000 Einheiten zu jeweils 3,00 EUR = 3.000 EUR</li><li>**Aktueller Einkaufspreis, basierend auf FIFO:** 2,00 EUR</li><li>**Durchgeführte Berechnung:** *Verkaufte Einheiten* × *Aktueller Einkaufspreis* = 1.000 × 2,00 EUR = 2.000 EUR</li></ul></li><li><p>*Letzter Einkaufpreis* – Der Wert aus der letzten Kauftransaktion wird zur Berechnung der Kreditorenrückvergütungen verwendet. Hier ist ein Beispiel:</p><ul><li>**Verkaufter Bestand:** 1.000 Einheiten zu jeweils 3,00 EUR = 3.000 EUR</li><li>**Letzter Einkaufspreis:** 2,00 EUR</li><li>**Durchgeführte Berechnung:** *Verkaufte Einheiten* × *Letzter Einkaufspreis* = 1.000 × 2,00 EUR = 2.000 EUR</li></ul></li><li><p>*Durchschnittlicher Einkaufspreis* – Der gewichtete Durchschnittswert für die letzten *x* Monate wird verwendet, um die Kreditorenrückvergütung zu berechnen. Wenn Sie diese Option auswählen, müssen Sie die Anzahl der Monate in das Feld **Anzahl der Monate** eingeben (das Feld ist nur verfügbar, wenn das Feld **Preisbasis** auf *Durchschnittlicher Einkaufpreis* gesetzt ist). Hier ist ein Beispiel:</p><ul><li>**Verkaufter Bestand:** 1.000 Einheiten zu jeweils 3,00 EUR = 3.000 EUR</li><li>**Durchschnittlicher Einkaufspreis:** 2,00 EUR</li><li>**Durchgeführte Berechnung:** *Verkaufte Einheiten* × *Durchschnittlicher Einkaufspreis* = 1.000 × 2,00 EUR = 2.000 EUR</li></ul></li><li><p>*Verkaufspreis* – Der Verkaufspreis wird zur Berechnung der Kreditorenrückvergütung verwendet. Hier ist ein Beispiel:</p><ul><li>**Verkaufter Bestand:** 1.000 Einheiten zu jeweils 3,00 EUR = 3.000 EUR</li><li>**Durchschnittlicher Einkaufspreis:** 2,00 EUR</li><li>**Durchgeführte Berechnung:** *Verkaufte Einheiten* × *Verkaufspreis* = 1.000 × 3,00 EUR = 3.000 EUR</li></ul></li></ul> |
| Anzahl Monate | Dieses Feld wird nur für Kreditorenrückvergütungen angezeigt (Deals bei denen das Feld **Modul** auf *Kreditor* gesetzt ist). Wenn Sie *Durchschnittlicher Einkaufspreis* im Feld **Preisbasis** ausgewählt haben, geben Sie die Anzahl der Monate ein, die verwendet werden sollen. |
| Buchungsprofil | Wählen Sie das [Buchungsprofil](rebate-management-posting.md) aus, das für die ausgewählte Deal-Position gilt. Dieses Profil wird nur verwendet, wenn das Feld **Abstimmen nach** in der Deal-Kopfzeile auf *Position* gesetzt ist. Ist das Feld **Abstimmen nach** auf *Deal* gesetzt, wird immer das Buchungsprofil verwendet, das in der Deal-Kopfzeile festgelegt ist. Ist für die Deal-Position kein Buchungsprofil festgelegt, wird immer das Buchungsprofil verwendet, das in der Deal-Kopfzeile festgelegt ist. |
| Buchungsprofil für Garantie | Dieses Feld funktioniert wie das Feld **Buchungsprofil**, gilt aber nur für Lizenzgebühren. |
| Zahlungstyp | Die Zahlungsart für das Buchungsprofil, das für den Deal ausgewählt wurde. |
| Mehrwertsteuer enthalten | Wählen Sie aus, ob in der Transaktion die Steuer enthalten ist. Die Frage, ob die Steuer enthalten ist, ist nur relevant, wenn das Feld **Basis** auf *Wert* gesetzt ist. Der Rechnungsbetrag wird als Betrag inklusive Steuer verwendet. Wenn die Rückvergütungsberechnung auf einem Prozentsatz basiert, multipliziert das System den Rückvergütungsprozentsatz mit dem Betrag inklusive Steuer. Beachten Sie, dass für die Berechnung der Mehrwertsteuersatz aus der Deal-Position verwendet wird. |
| Gutschriften einbeziehen | <p>Setzen Sie diese Option auf *Ja*, um Gutschriften in die Rückvergütungsberechnung einzubeziehen.</p><p>Wenn Sie diese Option auf *Ja* setzen, variiert der Effekt je nach Wert des Feld **Transaktionstyp**:</p><ul><li>Wenn das Feld **Transaktionstyp** auf *Rechnung* gesetzt ist, werden bei der Berechnung Gutschriften berücksichtigt. Diese ist die übliche Konfiguration.</li><li>Ist das Feld **Transaktionstyp** auf *Auftrag* gesetzt, werden bei der Berechnung sowohl Aufträge mit negativen Werten als auch offene zurückgegebene Aufträge berücksichtigt.</li></ul> |
| Rabattbetrag | Setzen Sie diese Option auf *Ja*, um die Berechnung auf den reduzierten Betrag des Artikels oder der Artikel in Fällen zu stützen, in denen Deal-Positionsrabatte gewährt werden. |
| Nur bezahlte Rechnungen | Setzen Sie diese Option auf *Ja*, wenn bei der Berechnung nur vollständig bezahlte Rechnungen berücksichtigt werden sollen. (Mit anderen Worten: Für teilweise bezahlte Rechnungen werden keine Rückvergütungen berechnet.) Diese Option ist nur verfügbar, wenn das Feld **Transaktionstyp** auf *Rechnung* gesetzt ist. |
| Freitext aufnehmen | Setzen Sie diese Option auf *Ja*, um Freitextrechnungen in die Rückvergütungsberechnung einzubeziehen. Freitextrechnungen können nur für Deal-Positionen aufgenommen werden, in denen das Feld **Artikelcode** auf *Alle* gesetzt ist. |
| Ausgleichsrabatt einbeziehen | Setzen Sie diese Option auf *Ja*, um die Rückvergütung um den ersten Ausgleichsrabatt zu reduzieren. Es wird davon ausgegangen, dass die Organisation den ersten Ausgleichsrabatt gewährt. Setzen Sie diese Option auf *Nein*, damit der Ausgleichsrabatt später verwendet werden kann. |
| Dokumentnotizen | Geben Sie Notizen ein, die als Transaktionstext in den Erfassungspositionen der Rückvergütungstransaktion verwendet werden sollen. |

### <a name="settings-on-the-dates-tab"></a>Einstellungen auf der Registerkarte „Datum“

Die Einstellungen auf der Registerkarte **Datum** des Inforegisters **Details zur Rückvergütungsverwaltung** definiert die Häufigkeit und das Timing der Berechnungen, die in der Registerkarte **Allgemein** festgelegt sind. Sie bestimmen, wie Berechnungen zur Verarbeitungszeit erfolgen.

Auf dieser Registerkarte können Sie den Datumsbereich angeben, für den die ausgewählte Deal-Position gilt, sowie die Häufigkeit der Berechnung. Sie können auch angeben, ob und wann die Garantie gebucht werden soll.

Sie können die Schaltflächen in der Symbolleiste verwenden, um Datumspositionen zum Raster hinzuzufügen oder zu entfernen. Wenn mehrere Datumspositionen vorhanden sind, dürfen sich die gültigen Datumsbereiche nicht überlappen. Andernfalls erhalten Sie eine Fehlermeldung, wenn Sie versuchen, den Deal zu speichern.

Die folgende Tabelle beschreibt die Felder, die für jede Datumsposition verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Anfangsdatum | Geben Sie das erste Datum ein, für das die Datumsposition gilt. Wenn in der Kopfzeile des Deals Von- und Bis-Daten angegeben sind, werden diese als Standardwerte für jede neue Datumsposition verwendet. |
| Bis-Datum | Geben Sie das letzte Datum ein, für das die Datumsposition gilt. Wenn in der Kopfzeile des Deals Von- und Bis-Daten angegeben sind, werden diese als Standardwerte für jede neue Datumsposition verwendet. |
| Pro | Geben Sie an, wie oft die Deal-Position berechnet werden soll. Geben Sie hier eine Ganzzahl ein und wählen Sie dann im Feld **Kumulieren nach** eine Einheit aus. Um die Berechnung beispielsweise jede zweite Woche durchzuführen, legen Sie das Feld **Pro** auf *2* und das Feld **Kumulieren nach** auf *Wochen* fest. |
| Kumulieren nach | Wählen Sie die Einheit aus, die für die **Pro**-Einstellung gilt. Wählen Sie *Lebensdauer* aus, um die Berechnung über die ganze Lebensdauer der Deal-Position durchzuführen. Wählen Sie *Angepasste Periode* aus, um einen Zeitraum auszuwählen, der im Hauptbuch festgelegt ist. In diesem Fall müssen Sie auch das Feld **Periodentyp** festlegen. |
| Periodentyp | Dieses Feld ist nur verfügbar, wenn das Feld **Kumulieren nach** auf *Angepasste Periode* gesetzt wird. Die zur Auswahl stehenden Werte stammen von den im Hauptbuch definierten Periodentyp. |
| Erster Wochentag | Geben Sie an, wie die Wochen für die Periode identifiziert werden. Dieses Feld ist nur verfügbar, wenn das Feld **Kumulieren nach** auf *Wochen* gesetzt wird. |
| Beanspruchen pro | Geben Sie an, wie oft Rückvergütungen für die Deal-Position in Anspruch genommen werden können. Geben Sie hier ein Integer ein und wählen Sie dann im Feld **Beanspruchen nach** eine Einheit aus. |
| Beanspruchen nach | Wählen Sie die Einheit aus, die für die Einstellung **Beanspruchen nach** gilt. Wählen Sie *Lebensdauer*, um eine Beanspruchung nur einmal während der gesamten Lebensdauer der Deal-Position zu erlauben. Wählen Sie *Angepasste Periode* aus, um einen Zeitraum auszuwählen, der im Hauptbuch festgelegt ist. In diesem Fall müssen Sie auch das Feld **Periodentyp für Beanspruchung** festlegen. |
| Periodentyp für Beanspruchung | Dieses Feld ist nur verfügbar, wenn das Feld **Beanspruchen nach** auf *Angepasste Periode* gesetzt wird. Die zur Auswahl stehenden Werte stammen von den im Hauptbuch definierten Periodentyp. |
| Bei Buchung verarbeiten | Aktivieren Sie dieses Kontrollkästchen, wenn die Beanspruchungsposition bei der Buchung verarbeitet werden soll. Diese Option ist nur für Deal-Positionen verfügbar, bei denen das Feld **Transaktionstyp** der Registerkarte **Allgemein** auf *Geliefert* oder *Rechnung* festgelegt ist. Für Rückstellungen wird die Bereitstellung gebucht, wenn der Lieferschein oder die Rechnung erstellt wird. |
| Garantie pro | Dieses Feld gilt nur für Lizenzgebührendeals. Geben Sie an, wie oft die Garantie der Lizenzgebühr während der durch **Kumulieren nach** festgelegten Periode berechnet werden soll. Geben Sie hier eine Ganzzahl ein und wählen Sie dann im Feld **Garantie bezahlt** die Zahlungszeit aus. |
| Garantie bezahlt | <p>Dieses Feld gilt nur für Lizenzgebührendeals. Damit wird in Verbindung mit dem Feld **Garantie pro** festgelegt, wie häufig die Garantie berechnet wird. Wählen Sie einen der folgenden Werte aus:</p><ul><li><p>*Anfang der Periode* – Die Garantie wird am Anfang des für die Datumsposition festgelegten Vereinbarungszeitraums gezahlt. Die volle Garantie wird zuerst verarbeitet. Nur der Wert der Lizenzgebühren über dem garantierten Betrag wird als Lizenzgebühr gebucht. Hier ist ein Beispiel:</p><ul><li>**Garantieminimum:** 10.000 EUR über zwei Monate.</li><li>**Monat 1:** 10.000 EUR wurden als Garantie und 0 EUR an Lizenzgebühren gebucht.</li><li>**Monat 2:** 2.000 EUR wurden als Lizenzgebühren und 0 EUR als Garantien gebucht.</li><li>**Durchgeführte Berechnung:** *Verbleibende Garantie* – *Gebuchte Lizenzgebühren* = 0 EUR – 2.000 EUR = -2.000 EUR.</li></ul><p>Da eine Lizenzgebührzahlung von 2.000 EUR erforderlich ist, wird eine Erfassung für 2.000 EUR erstellt.</p><p>**Hinweis:** Die Garantie sollte zusammen mit der Abzugsbereitstellung für die erste Periode berechnet und gebucht werden.</p></li><li><p>*Ende der Periode* – Die Garantie wird erst nach Ablauf der in der Datumsposition festgelegten Abzugsvereinbarung ausgezahlt. Hier ist ein Beispiel:</p><ul><li>**Garantieminimum:** 10.000 EUR über zwei Monate.</li><li>**Monat 1:** 5.000 EUR wurden als Lizenzgebühr gebucht und eine Erfassung erstellt.</li><li>**Monat 2:** 7.000 EUR wurden als Lizenzgebühr gebucht und eine Erfassung erstellt.</li><li>**Durchgeführte Berechnung:** Da die Lizenzgebühren den Garantiebetrag überschreiten, werden 0 EUR auf die Garantie gebucht.</li></ul><p>**Hinweis:** Die Garantie sollte nur zusammen mit der Abzugsbereitstellung und der Rückvergütungstransaktion für die letzte Periode berechnet und gebucht werden.</p></li></ul> |
| Garantieminimum | Dieses Feld gilt nur für Lizenzgebührendeals. Geben Sie den Mindestbetrag der Garantie für eine Lizenzgebühr in der Währung ein, die in der Deal-Kopfzeile festgelegt ist. |

### <a name="settings-on-the-lines-tab"></a>Einstellungen auf der Registerkarte Positionen

In der Registerkarte **Positionen** im Inforegister **Details zur Rückvergütungsverwaltung** können Sie die Berechnungspositionen für die ausgewählte Deal-Position festlegen. Jede Berechnungsposition legt einen Mengen- oder Werteschwellenwert und einen zugehörigen Vergütungsbetrag oder Artikel fest. Das Feld **Basis** unter **Allgemein** gibt an, ob die einzelnen Berechnungspositionen auf einer Menge oder einem Wert basieren.

Sie können die Schaltflächen in der Symbolleiste verwenden, um Berechnungspositionen zum Raster hinzuzufügen oder daraus zu entfernen. Sie können beliebig viele Berechnungspositionen haben. Wenn jedoch mehrere Berechnungspositionen vorhanden sind, dürfen sich die Mengen- oder Wertebereiche für „bis“ und „von“ nicht überlappen.

Die folgende Tabelle beschreibt die Felder, die für jede Berechnungsposition verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Ab Menge/Wert | Geben Sie die Mindestmenge oder den Mindestwert ein, für den die Berechnungsposition gilt. |
| Bis Menge/Wert | Geben Sie die Höchstmenge oder den Höchstwert ein, für den die Berechnungsposition gilt. |
| Rückvergütungsverwaltungsmethode | <p>Dieses Feld ist nur für Deals verfügbar, bei denen das Feld **Rückvergütungsausgabe** in der Kopfzeile auf *Finanziell* gesetzt ist. Wählen Sie die Methode zum Berechnen der Rückvergütung aus.</p><ul><li>*Fest* – Für die Position wird ein fester Preis verwendet.</li><li>*Prozent* – Ein prozentualer Anteil des Verkaufsbetrags verwendet.</li><li>*Satz* – Es wird ein fester Preis pro Bestellung verwendet.</li></ul><p>**Wichtig:** Wir empfehlen dringend, dass Sie für jede Berechnungsposition in der Registerkarte **Positionen** die gleiche Methode verwenden. Wenn eine neue Methode erforderlich ist, erstellen Sie eine neue Deal-Position. Denken Sie daran, dass Sie die Schaltfläche **Position kopieren** auf dem Inforegister **Rückvergütungsverwaltung** verwenden können, um aus einer bestehenden Deal-Position heraus eine neue Deal-Position zu erstellen.</p><p>**Hinweis:** Wenn das Feld **Rückvergütungsausgabe** auf *Artikel* festgelegt ist, ist dieses Feld immer auf *Fest* gesetzt. Weitere Informationen zum Angeben der Artikel finden Sie im Text, der dieser Tabelle folgt. |
| Rückvergütungsverwaltungsbetrag | Dieses Feld ist nur für Deals verfügbar, bei denen die **Rückvergütungsausgabe** in der Kopfzeile auf *Finanziell* gesetzt ist. Geben Sie den Betrag ein, der zur Berechnung der Rückvergütung verwendet werden soll, basierend auf der Methode, die Sie im Feld **Rückvergütungsverwaltungsmethode** ausgewählt haben. |

Wie in der vorherigen Tabelle erwähnt, müssen Sie bei Deals, bei denen das Feld **Rückvergütungsausgabe** in der Kopfzeile auf *Artikel* gesetzt ist, die Artikel angeben, die für jede Berechnungsposition in der Registerkarte **Positionen** bereitgestellt wird. Gehen Sie wie folgt vor, um die Artikel festzulegen.

1. Erstellen Sie in der Registerkarte **Positionen** die gewünschte Berechnungsposition, falls diese nicht vorhanden ist, und wählen Sie sie aus.
1. Wenn der Deal seit dem Erstellen der Berechnungsposition nicht gespeichert wurde, wählen Sie im Aktivitätsbereich **Speichern** aus.
1. Wählen Sie in der Registerkarte **Positionen** **Artikel** aus.
1. Fügen Sie auf der Seite **Artikel** mit den Schaltflächen im Aktivitätsbereich Artikel nach Bedarf zum Raster hinzu oder entfernen Sie sie. Legen Sie für jede Position die folgenden Felder fest:

    - **Artikelnummer** – Wählen Sie den Artikel aus, der bereitgestellt werden soll.
    - **(Andere Dimensionen)**  – Wenn Sie zum Definieren des Artikels mehr Dimensionen verwenden müssen (z. B. Konfiguration, Größe, Farbe, Stil, Standort oder Lager des Artikels), geben Sie diese an. Wählen Sie zum Hinzufügen oder Entfernen verfügbarer Dimensionen im Aktivitätsbereich **Dimensionen anzeigen** aus.
    - **Menge** – Geben Sie die Menge ein, die bereitgestellt wird, nachdem der Schwellenwert für die ausgewählte Berechnungsposition erreicht wurde.
    - **Einheit** – Wählen Sie die Einheit aus, in der der Wert **Menge** angegeben in.
    - **Mehrere** – Dieses Feld wird in Verbindung mit dem Feld **Menge** verwendet. Legen Sie zum Beispiel für eine Artikelposition das Feld **Menge** auf *2* und das Feld **Mehrere** auf *100* fest. Wenn Sie dann eine Gesamtauftragsmenge von 150 haben, sind zwei der Artikel kostenlos (zwei pro 100).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Einstellungen auf der Registerkarte „Bestandsdimensionen“

Die Registerkarte **Bestandsdimensionen** im Inforegister **Details zur Rückvergütungsverwaltung** zeigt alle verfügbaren Dimensionswerte für das Produkt an, die für die ausgewählte Deal-Position angegeben sind. Sie enthält Dimensionen, die nicht im Inforegister **Rückvergütungsverwaltung** angezeigt werden. Sie können Werte nur für die Dimensionen bearbeiten, die für das ausgewählte Produkt gelten.

Sie können dem Raster im Inforegister **Rückvergütungsverwaltung** durch Auswahl von **Dimensionen anzeigen** im Aktivitätsbereich weitere Dimensionen hinzufügen.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Berechnungsmethoden für Deal-Positionen

Jedes Mal, wenn Sie Details für eine Ihrer Deal-Positionen einrichten, wie im vorherigen Abschnitt beschrieben, müssen Sie die Berechnungsmethode für diese Position auswählen. In diesem Abschnitt werden die einzelnen Berechnungsmethoden erläutert und Beispiele bereitgestellt, die zeigen, wie jede Methode die Gesamtrückvergütung für Bestellungen und Deal-Positionen berechnet. In diesen Beispielen sind die Bestellungen und Deal-Positionen identisch. Nur die Berechnungsmethoden unterscheiden sich.

### <a name="stepped-calculation-method"></a>Abgestufte Berechnungsmethode

Die abgestufte Berechnungsmethode berechnet Schritt für Schritt, wobei jede Deal-Position ein Stück zur Rückvergütung beiträgt, bis die Verkaufsmenge oder der Verkaufswert erreicht ist. Die Schritte können entweder auf der Menge oder dem Wert der verkauften Waren basieren, abhängig von der Einstellung im Feld **Basis** in der Registerkarte **Allgemein** im Inforegister **Details zur Rückvergütungsverwaltung**.

Zum Beispiel wird eine Deal-Position eingerichtet, sodass das Feld **Berechnungsmethode** auf *Abgestuft* und das Feld **Basis** auf *Wert* festgelegt ist. Sie enthält Berechnungspositionen mit folgenden Rückvergütungen:

- **Position A:** 10 % bis zu 1.000 EUR
- **Position B:** 25 % bis zu 2.500 EUR

Wenn der Wert der gekauften oder verkauften Waren 2.000 EUR erreicht, wird die resultierende Rückvergütung wie folgt auf 350 EUR berechnet:

- **Rückvergütung (A):** *Schwelle (A)* × *Prozentsatz (A)* = 1.000 EUR x 10 % = 100 EUR
- **Rückvergütung (B):** (*Wert verkauft* – *Schwelle (A)*) × *Prozentsatz (B)* = (2.000 – 1.000 EUR) × 25 % = 250 EUR
- **Gesamtrückvergütung** *Rückvergütung (A)* + *Rückvergütung (B)*  = 100 EUR + 250 EUR = 350 EUR

Wenn das Feld **Basis** auf *Menge* und nicht auf *Wert* festgelegt ist, funktioniert die schrittweise Berechnungsmethode auf ähnliche Weise. Der erste Schritt wird für die identifizierte Menge verwendet, bis der zweite Schritt erreicht ist. Der zweite Schritt wird für alle Mengen über dem ersten Schritt verwendet, bis der dritte Schritt erreicht ist. Dieser Prozess wird dann durch alle nachfolgenden Schritte fortgesetzt.

### <a name="cumulative-calculation-method"></a>Kumulative Berechnungsmethode

Die kumulative Berechnungsmethode verwendet nur eine Berechnungsposition, um die Rückvergütung zu berechnen. Wenn für die Deal-Position mehrere Berechnungspositionen verfügbar sind, wird die Berechnungszeile mit dem höchsten Wert oder der höchsten Menge für die gesamte Menge oder den gesamten Wert verwendet. Wie die anderen Berechnungsmethoden verwendet auch die kumulative Methode die Einstellung des Felds **Basis** in der Registerkarte **Allgemein** des Inforegister **Details zur Rückvergütungsverwaltung**, um zu bestimmen, ob die Verkaufsmenge oder der Verkaufswert zur Berechnung der Rückvergütungen verwendet wird.

Zum Beispiel wird eine Deal-Position eingerichtet, sodass das Feld **Berechnungsmethode** auf *Kumulativ* und das Feld **Basis** auf *Wert* festgelegt ist. Sie enthält Berechnungspositionen mit folgenden Rückvergütungen:

- **Position A:** 10 % bis zu 1.000 EUR
- **Position B:** 25 % bis zu 2.500 EUR

Wenn der Wert der gekauften oder verkauften Waren 2.000 EUR erreicht, verwendet die Berechnung nur Position B. Die resultierende Rückvergütung wird wie folgt auf 500 EUR berechnet:

- **Gesamtrückvergütung:** *Verkaufter Wert* × *Rückvergütung (B)*  = 2.000 EUR x 25 % = 500 EUR

### <a name="rolling-calculation-method"></a>Rollierende Berechnungsmethode

Die rollierende Berechnungsmethode berechnet alle möglichen Berechnungspositionen für den Deal. Wenn mehrere Berechnungspositionen vorhanden sind und mehr als eine davon erreicht wird, werden alle erreichten Berechnungspositionen verwendet, die oberen Schwellenwerte gelten jedoch für jeden Prozentsatz. Wie die anderen Berechnungsmethoden verwendet auch die rollierende Methode die Einstellung des Felds **Basis** in der Registerkarte **Allgemein** des Inforegister **Details zur Rückvergütungsverwaltung**, um zu bestimmen, ob die Verkaufsmenge oder der Verkaufswert zur Berechnung der Rückvergütungen verwendet wird.

Zum Beispiel wird eine Deal-Position eingerichtet, sodass das Feld **Berechnungsmethode** auf *Rollierend* und das Feld **Basis** auf *Wert* festgelegt ist. Sie enthält Berechnungspositionen mit folgenden Rückvergütungen:

- **Position A:** 10 % bis zu 1.000 EUR
- **Position B:** 25 % bis zu 2.500 EUR

Wenn der Wert der gekauften oder verkauften Waren 2.000 EUR erreicht, wird die resultierende Rückvergütung wie folgt auf 600 EUR berechnet:

- **Rückvergütung (A):** *Schwelle (A)* × *Prozentsatz (A)* = 1.000 EUR x 10 % = 100 EUR
- **Rückvergütung (B):** *Verkaufter Wert* × *Prozentsatz (B)* =2.000 EUR x 25 % = 500 EUR
- **Gesamtrückvergütung** *Rückvergütung (A)* + *Rückvergütung (B)*  = 100 EUR + 500 EUR = 600 EUR

### <a name="total-calculation-method"></a>Gesamtberechnungsmethode

Die Gesamtberechnungsmethode verwendet alle Berechnungspositionen, um die Rückvergütung zu berechnen. Sie wendet die Gesamtmenge an, um die Rückvergütung für jede erreichte Berechnungsposition zu berechnen, und jede Berechnungsposition wendet ihren Prozentsatz auf den vollen Betrag an. Wie die anderen Berechnungsmethoden verwendet auch die Gesamtmethode die Einstellung des Felds **Basis** in der Registerkarte **Allgemein** des Inforegisters **Details zur Rückvergütungsverwaltung**, um zu bestimmen, ob die Verkaufsmenge oder der Verkaufswert zur Berechnung der Rückvergütungen verwendet wird.

Zum Beispiel wird eine Deal-Position eingerichtet, sodass das Feld **Berechnungsmethode** auf *Gesamt* und das Feld **Basis** auf *Wert* festgelegt ist. Sie enthält Berechnungspositionen mit folgenden Rückvergütungen:

- **Position A:** 10 % bis zu 1.000 EUR
- **Position B:** 25 % bis zu 2.500 EUR

Wenn der Wert der gekauften oder verkauften Waren 2.000 EUR erreicht, wird die resultierende Rückvergütung wie folgt auf 700 EUR berechnet:

- **Rückvergütung (A):** *Verkaufter Wert* × *Prozentsatz (A)* =2.000 EUR x 10 % = 200 EUR
- **Rückvergütung (B):** *Verkaufter Wert* × *Prozentsatz (B)* =2.000 EUR x 25 % = 500 EUR
- **Gesamtrückvergütung** *Rückvergütung (A)* + *Rückvergütung (B)*  = 200 EUR + 500 EUR = 700 EUR
