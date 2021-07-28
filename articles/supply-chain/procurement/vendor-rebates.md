---
title: Kreditorenrückvergütungen
description: Dieses Thema bietet einen Überblick die gebräuchlichsten Aufgaben, die Sie möglicherweise ausführen möchten, wenn Sie mit Kreditorenrückvergütungen arbeiten. Mithilfe von Kreditorenrückvergütungen können Unternehmen ihre Lieferantenrückvergütungsprogramme anhand automatisierter Aufgaben besser verwalten, die erforderlich sind, um Rückvergütungen, die verdient wurden, zu verwalten, nachzuverfolgen und zu fordern.
author: omulvad
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.openlocfilehash: 42c35fcca90b7dc55c8ef2985283d2ce92c4c8bc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344219"
---
# <a name="vendor-rebates"></a>Kreditorenrückvergütungen

[!include [banner](../includes/banner.md)]

Mithilfe von Kreditorenrückvergütungen können Unternehmen ihre Lieferantenrückvergütungsprogramme anhand automatisierter Aufgaben besser verwalten, die erforderlich sind, um Rückvergütungen, die verdient wurden, zu verwalten, nachzuverfolgen und zu fordern.

Dieses Thema bietet einen Überblick die gebräuchlichsten Aufgaben, die Sie möglicherweise ausführen möchten, wenn Sie mit Kreditorenrückvergütungen arbeiten. Der Überblick umfasst die folgenden Aufgaben:

- Überprüfen von Details einer Rückvergütungsvereinbarung.
- Identifizierung von Aufträgen, bei denen eine Berechtigung zu Rückvergütungen besteht und Generieren von Rückvergütungsforderungen.
- Prüfen und Genehmigen von Forderungen.

## <a name="audience-and-purpose"></a>Zielgruppe und Zweck

Die Informationen in diesem Thema sind für geschäftliche Entscheidungsträger in Unternehmen bestimmt, in Positionen wie Einkaufsleiter, Leiter der Finanzabteilung und Buchhaltungsleiter, die für Folgendes verantwortlich sind:

- Kreditorenpreis, Rabatt und Rückvergütungsvereinbarungen verwalten.
- Personal verwalten, das Rückvergütungsforderungen bearbeitet und Zahlungen eintreibt.
- Bestand zu den bestmöglichen Preisen bestellen.

Personen in diesen Positionen suchen nach Möglichkeiten, verschiedene Ziele zu erreichen. Nachfolgend finden Sie einige Beispiele:

- Flexibel verschiedene Typen von Verkaufsförderungskampagnen für Kreditoren sowie Rückvergütungsbedingungen berücksichtigen.
- Reduzieren der Verwaltungsbelastung und von Fehlern, die mit dem Überwachen der Wirkung verkaufsfördernder Maßnahmen und dem Bearbeiten von Forderungen zusammenhängen.
- Verbessern von Cashflowplanungen durch das Antizipieren zukünftiger Forderungen.
- Arbeiten mit einer quantifizierten Basis für laufende und zukünftige Verhandlungen mit Kreditoren über Rückvergütungen.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>Überprüfen von Details einer Kreditorenrückvergütungsvereinbarung

Eine Kreditorenrückvergütungsvereinbarung ist ein Datensatz eines Vertrags mit einem Kreditor, der die verhandelten Bedingungen angibt, unter denen das Unternehmen sich für eine monetäre Belohnung für das Erreichen vorher festgelegter Einkaufsziele qualifiziert. Kreditorenrückvergütungsvereinbarungen werden auf der Seite **Rückvergütungsvereinbarungen** erfasst.

Um die Seite **Kreditorenrückvergütungsvereinbarungen** zu öffnen, wählen Sie **Beschaffung** &gt; **Kreditorenrückvergütungen** &gt; **Rückvergütungsvereinbarungen** aus.

![Rahmenbestellung.](media/purchase-agreement.PNG)

Auf der Seite **Kreditorenrückvergütungsvereinbarungen** können Sie Details über die verhandelten Bedingungen einer Kreditorenvereinbarung anzeigen.

Der Kopf der Vereinbarung gibt die allgemeinen Bedingungen an, die ein Unternehmen für Rückvergütungen qualifizieren. Im Endeffekt geben Kopfzeileninformationen an, dass ein Kreditor eine Rückvergütung gewährt, wenn ein bestimmtes Produkt in einer bestimmten Menge gekauft wird. In der Kopfzeile geben Sie auch die Maßeinheits-Rückvergütungsoption an und den Berechnungsdatentyp.

- Wenn Sie auf der **Überblick**-Registerkarte Positionen haben, bei denen **Artikelcode** auf *Tabelle* festgelegt ist, um den Artikel anzugeben, gilt die Vereinbarung für diesen bestimmten Artikel. Wenn Sie Positionen haben, bei denen der **Artikelcode** auf *Gruppe* oder *Alles* festgelegt ist, um die Artikel anzugeben, wird die Lieferantenrabattvereinbarung individuell für jeden Artikel verarbeitet, der für den Artikelcode qualifiziert ist, und nicht für alle Artikel, die für den Artikelcode qualifiziert sind.

- Auf der Registerkarte **Allgemein** im Feld **Rückvergütungsoption für Maßeinheit** können Sie definieren, ob eine Maßeinheit eine Bedingung dafür sein soll, dass für eine Bestellposition eine Rückvergütung in Anspruch genommen werden kann.

    - **Konvertieren** – Eine Bestellposition qualifiziert zu einer Kreditorenrückvergütung mittels der Rückvergütungsvereinbarung. Sie erhalten eine Rückvergütung ungeachtet der Maßeinheit, die für die Position angewendet wird.
    - **Genaue Übereinstimmung** – Um sich für eine Rückvergütung zu qualifizieren, muss eine Bestellposition dieselbe Maßeinheit aufweisen, die in der Vereinbarung angegeben ist.

- Wählen Sie auf der Registerkarte **Allgemein** im Feld **Berechnungsdatumstyp** das Datum aus, dass verwendet wird, um zu ermitteln, ob der Einkauf in der Gültigkeitsperiode der Rückvergütungsvereinbarung erfolgt.

    - **Erstellt** – Verwenden Sie das Erstellungsdatum der Bestellung.
    - **Angeforderte Lieferung** – Verwenden Sie das angeforderte Lieferdatum.

In den Vereinbarungspositionen können Sie die Kreditoren-Rückvergütungsvereinbarung näher im Detail angeben.

- Im Feld **Kumulieren von Einkauf nach** können Sie die Berechnung der Rückvergütungsforderung festlegen. Der Betrag kann so festgelegt werden, dass er von einer Periode abhängt (Woche, Monat, Jahr, Lebenszeit oder eine benutzerdefinierte Periode). Der Wert **Rechnung** gibt an, dass eine Rückvergütungsforderung jedes Mal bestimmt wird, wenn eine Bestellposition in Rechnung gestellt wird.
- Im Feld **Entnommen von** können Sie die Basis zum Berechnen der Rückvergütung angeben.

    - **Brutto** – Die Rückvergütung wird basierend auf dem Bruttopreis des Artikels berechnet.
    - **Netto** – Die Rückvergütung wird basierend auf dem Nettopreis des Artikels berechnet (das heißt, der Preis, nachdem andere Rabatte angewendet wurden).

- Die Felder **Abgrenzungskonto für Rückvergütungsprogramm** und **Ausgabenkonto für Rückvergütungsprogramm** geben die Nummern von Konten an, die antizipierte Rückvergütungsbeträge während der unmittelbaren Phase zwischen Genehmigung und Bearbeitung empfangen.
- Wenn die Option **Genehmigung erforderlich** auf **Ja** festgelegt ist, muss die Rückvergütungsforderung genehmigt werden, bevor sie antizipiert oder gezahlt werden kann.
- Das Feld **Typ des Rückvergütungszeilenumbruchs** gibt die Basis für die Rückvergütungen an.

    - **Menge** – Die Rückvergütungen basieren auf Volumen.
    - **Betrag** – Die Rückvergütungen basieren auf Betrag.

- Im Inforegister **Positionen** können Sie sehen, wie verschiedene Mengenebenen eingerichtet werden können, um unterschiedliche Rückvergütungen zu gewähren. Beispielsweise geben in der vorherigen Illustration die Felder **Wert „Von”** und **Wert „An”** an, dass eine Produktmenge zwischen 10 und 19 Einheiten zu einer Rückvergütung von 15 USD pro Einheit qualifizieren.

    > [!NOTE]
    > Der Wert **Wert „Von”** ist inklusiv, wohingegen der Wert **Wert „Bis”** exklusiv ist. Das Feld **Typ des Rückvergütungszeilenumbruchs** wird beispielsweise auf **Menge** festgelegt, und Sie geben **1** im Feld **Wert „Ab”** ein und **3** im Feld **Wert „Bis”** ein. In diesem Fall gilt der Rückvergütungsbetrag, wenn Sie einen oder zwei Artikel kaufen, aber nicht, wenn Sie drei Artikel kaufen.

- Im Feld **Genehmigungsstatus für Workflow** gibt der Wert **Genehmigt** an, dass die Vereinbarung auf Bestellungen angewendet werden kann, die die Bedingungen der Vereinbarung erfüllen.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>Identifizierung von Aufträgen, bei denen eine Berechtigung zu Rückvergütungen besteht und Generieren von Rückvergütungsforderungen

Wenn Bestellungen einem Kreditor erteilt werden, mit dem das Unternehmen eine Rückvergütungsvereinbarung hat, identifiziert das Programm sämtliche zukünftigen Kreditorenkreditzahlungen. Wenn die Bestellungen für eine Rückvergütung qualifizieren, wird eine Rückvergütungsforderung für jede Bestellposition generiert, sobald eine Einkaufsrechnung gebucht wurde. Dieser Prozess ist automatisch. Später können Sie die voraussichtlichen Rückvergütungen überprüfen und die Auswirkung dieser Rückvergütungen auf die Kosten des Produkts und die Gewinnspanne anzeigen.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Details von Rückvergütungen anzeigen, die auf eine Bestellposition durch die Kreditoren-Rückvergütungsvereinbarung angewendet werden

1. Wählen Sie auf der Seite **Bestellung** eine Bestellposition aus, und wählen Sie dann **Bestellposition** &gt; **Ansicht** &gt; **Preisdetails** aus.
2. Wählen Sie auf der Seite **Preisdetails** das Inforegister **Rückvergütungen** aus.

Die Rückvergütungsinformationen werden auch im Feld **Kreditorenrückvergütung** im Abschnitt **Gewinnspannenvorkalkulation** der Seite **Preisdetails** angezeigt.

> [!NOTE]
> Überprüfen Sie auf der Seite **Beschaffungsparameter** auf der Registerkarte **Preise**, dass die Option **Preisdetails aktivieren** auf **Ja** festgelegt ist. Wenn die Option auf **Nein** festgelegt ist, sind Sie dann nicht in der Lage, die Rückvergütungen anzuzeigen.

## <a name="review-and-approve-claims"></a>Prüfen und Genehmigen von Forderungen

Rückvergütungsforderungen, die generiert werden, stellen die zukünftigen Zahlungen dar, die vom Kreditor erwartet werden können. Bevor eine Gutschrift für den Kreditor ausgestellt wird, möchte der Vereinbarungsbesitzer normalerweise die Forderungen überprüfen und genehmigen. Beachten Sie jedoch, dass der Status eines Anspruchs bestimmt, ob der Anspruch bereit ist, den Genehmigungsprozess zu durchlaufen.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>Der Status von Forderungen und die Auswirkung auf den Genehmigungsprozess

Wenn eine Forderung generiert wird, wird deren Status auf **Zu berechnen** festgelegt, wenn die Rückvergütung auf kumulativer Basis gewährt wird, oder auf **Berechnet**, wenn die Rückvergütung pro Rechnung gewährt wird. Wenn der Status einer Forderung **Zu berechnen** ist, muss die Forderung einen Berechnungsprozess durchlaufen, der durch die Funktion „Kumulieren” behandelt wird. Nur Forderungen, die den Status **Berechnet** aufweisen, können in den Genehmigungsprozess einbezogen werden.

> [!NOTE]
> Wenn die Option **Genehmigung erforderlich** auf einer Kreditoren-Rückvergütungsvereinbarung auf **Nein** festgelegt wird, haben sämtliche Ansprüche, die generiert werden, den Status **Genehmigt** Die Genehmigung ist für Forderungen verbindlich, die auf kumulativer Basis gewährt werden.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Forderungen genehmigen und Buchungen sowie Rechnungsdetails anzeigen

Wenn Ansprüche genehmigt wurden, können sie nach Kreditorenkonten bearbeitet werden. Eine Gutschrift (Kreditorenrechnung) für den Rückvergütungs-Forderungsbetrag wird automatisch generiert. Der Kredit kann dann dem Kreditorensaldo hinzugefügt werden und das Kreditorenkontenteam kann es in den regulären Begleichungsprozess einbeziehen.

1. Wählen Sie **Beschaffung** &gt; **Kreditorenrückvergütungen** &gt; **Rückvergütungsforderungen** aus, um eine Rückvergütungsforderung zu öffnen.
2. Schließen Sie die Rückvergütungsforderung.
3. Markieren Sie die Forderung, und wählen Sie dann im Aktionsbereich **Genehmigen** aus.
4. Auf der Anforderungsseite im Feld **Kreditor** wählen Sie den Kreditor aus, bezüglich dem sie autorisiert sind, eine Rückvergütung von diesem zu empfangen, und wählen Sie dann **OK**.

    Eine Rückvergütungs-Abgrenzungserfassung wird für den Forderungsbetrag gebucht. Diese Buchung belastet das Konto der antizipierten Kreditorenrückvergütungsforderungen mit dem erwarteten Kreditorenkredit und schreibt dem Interimskonto für antizipierten Kreditorenrückvergütungsforderungen den erwarteten Gewinn gut.

    ![Meldung.](media/message.png)

5. In der Rückvergütungsliste wählen Sie die Position aus, und wählen Sie dann im Aktionsbereich die Option **Rückvergütungsbuchungen** aus, um die Nummer der Stapelverarbeitungserfassung für diese Rückvergütungs-Abgrenzungsbuchung anzuzeigen und zu ihr zu navigieren.

    Um die Forderungen zum regulären Kreditorenkontenprozess zu verschieben, muss der Kreditorenkontensachbearbeiter jetzt die Bearbeitung der Rückvergütungsforderung abschließen, indem die Prozessfunktion ausgeführt wird.

6. Wählen Sie im Aktionsbereich **Prozess** aus, und wählen Sie dann **Filter** aus. Wählen Sie im Feld **Kriterien** für das Feld **Kreditorenkonto** den Kreditor aus, für den Rückvergütungsforderungen zu bearbeiten sind, wählen Sie andere relevante Filte aus, und wählen Sie dann **OK** aus.

    Die Meldungsleisten und die Tatsache, dass der Status zu **Abgeschlossen** geändert wurde, zeigen an, dass die folgenden Ereignisse erfolgt sind:

    - Eine Rückvergütungs-Abgrenzungserfassungsbuchung hat die vorherigen Zwischenbeträge in den Abgrenzungsforderungs- und Ausgabenkonten zurückgesetzt.
    - Eine Kreditorenrechnung (Gutschrift) für den Rückvergütungsbetrag wurde erstellt.

        > [!NOTE]
        > Die Einstellung der Option **Manuelle Rechnungsbuchung** auf der Registerkarte **Rückvergütungsprogramm** der Seite **Beschaffungsparameter** bestimmt, ob eine Kreditorenrechnung manuell oder automatisch als Teil der Forderungsbearbeitung gebucht wird.

    - Wenn die Kreditorenrechnung entweder manuell oder automatisch gebucht wird, wurde das Verbindlichkeitskonto des Kreditors belastet, und das Konto für Erhaltene Rabatte und Vergütungen hat eine Gutschrift erhalten.

        > [!NOTE] 
        > Die Nummer des Kontos für erhaltene Rabatte und Vergütungen wird für die Beschaffungskategorie angegeben, die in der Einkaufsrechnungsposition für die Rückvergütung verwendet wird. Die Beschaffungskategorie wird wiederum auf der Registerkarte **Rückvergütungsprogramm** der Seite **Beschaffungsparameter** festgelegt.

7. In der Rückvergütungsliste wählen Sie die Position aus, und wählen Sie dann im Aktionsbereich die Option **Rückvergütungsbuchungen** aus, um die Nummer der Stapelverarbeitungserfassung für diese Rückvergütungs-Abgrenzungsbuchung sowie die Kreditorenrechnungsnummer anzuzeigen und zu ihr zu navigieren.
8. Wählen Sie die Position für die Kreditorenrechnungstransaktion aus, und wählen Sie dann im Aktionsbereich **Kreditorenrechnung** aus. Wenn die Kreditorenrechnung gebucht wurde, wird Ihnen die Rechnungserfassung angezeigt. Andernfalls wird Ihnen die Kreditorenrechnung als ausstehende Kreditorenrechnung angezeigt, die eine manuelle Buchung erfordert.

    Die Rechnungsposition gibt die Details zur Kreditorenrechnung für die Beschaffungskategorie **Provisionen und Rückerstattungen** an.

9. Auf der Seite **Alle Kreditoren** wählen Sie den Kreditor aus, von dem Sie die Rückvergütung erhalten, und wählen Sie dann im Aktionsbereich **Buchungen** aus. Finden Sie die Position für die Rechnung. Der Rückvergütungsbetrag wurde nun zum Kreditorensaldo hinzuaddiert.

## <a name="summary"></a>Summe

Der Prozess für die Bearbeitung von Kreditorenrückvergütungen beinhaltet mehrere manuelle Nachverfolgungsaufgaben, die oft lästig sind. Indem diese Aufgaben automatisiert werden, kann die Kreditorenrückvergütungs-Verwaltungsfunktion Ihnen dabei helfen, die folgenden Prozesse zu durchlaufen:

- Generieren von genauen Rückvergütungsansprüchen
- Die erwarteten Forderungen und Zwischengewinne im Hauptbuch antizipieren
- Den Kreditorensaldo und die Gewinn- & Verlustrechnung mit der fälligen Vergütung aktualisieren


[!INCLUDE[footer-include](../../includes/footer-banner.md)]