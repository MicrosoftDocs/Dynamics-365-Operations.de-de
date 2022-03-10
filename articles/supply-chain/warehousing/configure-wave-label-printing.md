---
title: Zyklusbeschriftungsdruck
description: In diesem Thema wird das Drucken von Wellenetiketten beschrieben und die Einrichtung erläutert.
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 59c4c100275917f3f9bf489c7d64b276275f1872
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778082"
---
# <a name="wave-label-printing"></a>Zyklusbeschriftungsdruck

[!include [banner](../includes/banner.md)]

Das Drucken von Wellenetiketten bietet einen alternativen Ansatz zum Drucken von Etiketten, indem eine neue Wellenschrittmethode eingeführt wird, mit der Sie während der Wellenausführung Etikette direkt aus der Wellenvorlage erstellen und drucken können. Daher sind die Etikette bereits verfügbar, bevor Mitarbeiter den Arbeitsauftrag auf einem mobilen Gerät ausführen. Die Arbeiter können dann die erforderlichen Etikette während der Kommissionierung anstatt nach der Kommissionierung anbringen.

Beim Drucken von Wellenetiketten wird die Zebra-Programmiersprache (ZPL) zum Erstellen von Etikettenlayouts verwendet. Ein Etikettenlayout ist in drei Abschnitte (Kopfzeile, Text und Fußzeile) unterteilt, um Etikette mit sich wiederholender Struktur zu ermöglichen. Wellenetikettenvorlagen teilen dem System mit, welches Etikettenlayout verwendet werden soll. Benutzer können angeben, welcher Drucker verwendet wird. Sie können bei Bedarf auch Etikette auf mehreren Druckern gleichzeitig drucken. Die Seite **Wellenetikettverlauf** zeigt die Erfassung aller Etikette an, die mit diesem Setup erstellt wurden.

Sie können Etikette basierend auf Arbeitsüberschriften drucken und sortieren, Sie können Unterbrechungsetikette pro Arbeitsüberschrift drucken und Sie können Etikette für Containerinhalte, Falletikette und andere ähnliche Etikette drucken.

> [!NOTE]
> Diese Funktion ersetzt nicht die vorhandene Etikettendruckfunktion, die auf dem Routing von Dokumenten basiert.

Der Wellenetikettendruck bietet die folgenden Verbesserungen:

- Drucken Sie Etikette entsprechend der Anzahl der Kartons in einer einzelnen Arbeitsposition, ohne Containerisierung zu verwenden. (Ein „Karton“ ist eine Einheit, die in Einheitennummernkreis-Positionen angegeben ist.)
- Drucken Sie verschiedene Etikettsequenzen (z. B. Karton- und Palettenetikette).
- Schließen Sie die Etikettaufzählung ein (z. B. 1/124, 2/124, ... 124/124) und definieren Sie den Enumerationsbereich (z. B. Arbeitspostion, Ladungsposition oder Lieferung).
- Erstellen und drucken Sie eine Frachtbrief-ID auf Etiketten, bevor der Frachtbrief generiert wird.
- Erstellen Sie für jeden Karton eine eindeutige Nummer der Versandeinheit (SSCC) und fügen Sie diese auf jedem Etikett ein.
- Erstellen Sie GS1-konforme Nummernkreise für Frachtbrief-IDs und SSCCs.
- Drucken Sie erneut Etikette sowohl von Mobilgeräten als auch vom Rich-Client.
- Stornieren Sie Etikette (z. B. in Szenarien von Entnahme mit unzureichender Menge) und drucken Sie sie erneut.
- Serienetikettenverlauf löschen.
- Verbesserungen an Dokumentrouting-Layouts werden zwischen Dokumentrouting-Layouts und Wellenetikettenlayouts geteilt. (Weitere Informationen finden Sie unter [Dokumentrouting-Layout für Kennzeichen](../warehousing/document-routing-layout-for-license-plates.md) .)

Diese Verbesserungen machen es effizienter, Kartons zu etikettieren, bevor sie auf Paletten geladen werden. Sie kommen insbesondere Unternehmen zugute, die an große Einzelhändler liefern, die automatisch Auftragseingänge bestätigen, indem sie jeden Karton separat scannen.

> [!NOTE]
> Sie können die in diesem Thema beschriebenen Konfigurationsszenarien je nach Ihren Geschäftsanforderungen entweder separat oder in Kombination implementieren. Sie können mehrere Wellenetikettenvorlagen entwerfen, die nacheinander arbeiten (wie in Szenario 3 dargestellt). Sie können beispielsweise Szenario 1 zum Drucken von Kartonetiketten und Szenario 2 zum Drucken von Palettenetiketten verwenden (wenn die vorrätigen Paletten in Größe und Anordnung variieren).

## <a name="turn-on-the-wave-label-printing-feature"></a>Funktion für Wellenetikettendruck aktivieren

Ab Supply Chain Management Version 10.0.21 ist diese Funktion obligatorisch, daher ist sie standardmäßig aktiviert und kann nicht wieder deaktiviert werden. Die Funktion ist jedoch immer noch in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Wellenetikettendruck*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Szenario 1: Drucken von Wellenetiketten, bei dem ein einzelnes Wellenetikett generiert wird

Dieses Szenario zeigt, wie ein Unternehmen Adressetikett für einen großen Einzelhändler drucken kann, der Auftragseingänge automatisch bestätigt, indem jeder Karton separat gescannt wird.

Dieses Szenario zeigt den End-to-End-Flow.

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Um diesem Szenario zu folgen, müssen Demodaten installiert sein, und Sie müssen die juristische Person **USMF** auswählen.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Stellen Sie sicher, dass die Wellenetikettmethode verfügbar ist

Möglicherweise müssen Sie die Wellenprozessmethoden erneut generieren, um die Wellenetiketdruck-Methode verfügbar zu machen.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.
1. Bestätigen Sie, dass **waveLabelPrinting** in der Liste ist. Wenn nicht, wählen Sie im Aktionsbereich **Methoden erneut generieren** aus, um es hinzuzufügen.

### <a name="configure-a-wave-template"></a>Eine Wellenvorlage konfigurieren

Mit Wellenvorlagen können Sie bestimmte Instanzen von Wellenmethoden mit einer entsprechenden Wellenetikettenvorlage verknüpfen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Wählen Sie eine Vorlage aus, wie beispielsweise **62 Lieferungsstandard**.
1. Im Inforegister **Methoden** verschieben Sie die Methode **Wellenetikettendruck** zur Spalte **Ausgewählte Methoden**.
1. Wählen Sie in der Spalte **Ausgewählte Methoden** die Methode **Wellenetikettendruck** aus, und legen Sie deren Feld **Wellenschrittcode** auf *PrintLabel* fest. Weitere Informationen über Wellenschrittcodes finden Sie unter [Wellenschrittcodes](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Ein Wellenetikettenlayout erstellen

Das Etikettenlayout steuert, welche Informationen auf dem Etikett gedruckt werden und wie sie angeordnet sind. Hier geben Sie den ZPL-Code ein, der an den Drucker gesendet wird.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenlayouts**.
1. Erstellen Sie einen Datensatz mit den folgenden Einstellungen:

    - **Etikettenlayout-ID:** *Karton*
    - **Beschreibung:** *Karton (SSCC)*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktionsbereich **Einstellungen für Wellenetikettzeile** aus.

    Die Seite **Einstellungen für Wellenetikettzeile** wird angezeigt. Hier können Sie den dynamischen Teil des Etiketts konfigurieren.

1. Fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:

    - **Zeilen-ID:** *WaveLabel*
    - **Zeilentabellenname:** *WHSWaveLabel*
    - **Zeilenstartposition:** *0*

        Dieses Feld definiert die vertikale Position, an der die Zeile im Etikett beginnt.

    - **Zeilenhöhe:** *0*

        Dieses Feld definiert die Höhe jeder Zeile (in Punkten) gemäß dem ZPL-Standard. Die Zeilenhöhe ist positiv für horizontale Etikette und negativ für vertikale Etikette. Da es in diesem Beispiel nur eine Zeile gibt, können Sie den Wert auf *0* (Null) festlegen.

    - **Zeilen pro Seite:** *1*

        Dieses Feld definiert die Anzahl der Zeilen, die auf jedes Etikett gedruckt werden können.

        > [!NOTE]
        > Durch dieses Setup wird für jeden Datensatz in der Wellenetikettentabelle ein separates ZPL-Etikett gedruckt.

1. Schließen Sie die Seite.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Arbeitstyp*
    - **Kriterien:** *Entnahme*

    Diese Abfrage stellt sicher, dass nur Arbeitspositionen vom Entnahmetyp auf dem Etikett gedruckt werden und nicht Arbeitspositionen vom Einlagerungstyp.

1. Wenn Sie die Frachtbrief-ID ausdrucken möchten, wählen Sie auf der Registerkarte **Verknüpfungen** die Tabelle **Arbeitspositionen** aus, und verknüpften Sie die Tabelle **Lieferungen** damit.
1. Schließen Sie das Abfrage-Editor-Dialogfeld.
1. Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**. Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie Code für die erforderliche Kopfzeile ein. Wenn Sie beispielsweise Zebra-Drucker verwenden, können Sie den folgenden Code verwenden.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Im Abschnitt **Textabschnitt** im Feld **Etikettentext** geben Sie ZPL-Code für den erforderlichen Text ein. Hier ist ein Beispiel.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Im Abschnitt **Textabschnitt** im Feld **Etikettenfußzeile** geben Sie ZPL-Code für die erforderlichen Fußzeile ein. Hier ist ein Beispiel.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Durch dieses Setup wird eine Kopie jedes Etiketts gedruckt. Wenn Sie mehr Kopien benötigen (z. B. eine Kopie für jede Seite der Palette), legen Sie den **n**-Wert für den Abschnitt **\^PQn** in der Fußzeile auf die erforderliche Anzahl von Kopien fest. Um vier Kopien jedes Etiketts zu drucken, geben Sie beispielsweise **\^PQ4** an.

Ihr Etikett kann jetzt verwendet werden.

### <a name="create-a-wave-label-type"></a>Einen Wellenetikettentyp erstellen

Wellenetikettentypen werden verwendet, um Wellenetikettenvorlagen mit einer Einheit in Einheitsnummernkreisgruppen-Positionen zu verknüpfen.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettentypen**.
1. Fügen Sie ein Wellenetikettentyp mit den folgenden Einstellungen hinzu:

    - **Etikettentyp:** *Karton*
    - **Beschreibung:** *Karton*

### <a name="set-up-unit-sequence-groups"></a>Einheitensequenzgruppen einrichten

Richten Sie als Nächstes die Einheitsnummernkreisgruppe für den Wellenetikettentyp ein.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Lagerort \> Einheitsnummernkreisgruppe**.
1. Wählen Sie die Gruppe **Ea Box PL** (Einzelstücke Kiste/Palette) aus.
1. Für die Position **Kiste** legen Sie das Feld **Wellenetikettentyp** auf *Karton* fest.

### <a name="create-a-wave-label-template"></a>Eine Wellenetikettenvorlage erstellen

Erstellen Sie als Nächstes die Wellenetikettenvorlage für den Wellenetikettentyp.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenvorlagen**.
1. Fügen Sie eine Wellenetikettenvorlage hinzu und legen Sie die folgenden Werte in der Kopfzeile fest:

    - **Etikettenvorlagenname:** *Kartonetikette*
    - **Beschreibung:** *Kartonetikette*
    - **Wellenschrittcode:** *PrintLabel*
    - **Lagerort:** *62*

1. Im Inforegister **Allgemein** legen Sie das Feld **Wellenetikettentyp** auf *Karton* fest.
1. Im Inforegister **Details zur Wellenetikettenvorlage** fügen Sie eine neue Zeile mit den folgenden Einstellungen hinzu:

    - **Etikettenlayout-ID:** *Karton*
    - **Druckername:** Wählen Sie einen geeigneten ZPL-Drucker aus.
    - **Abfrage ausführen:** *Ja* (Diese Einstellung ist optional, wird jedoch für eine optimale Leistung empfohlen.)

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Optional: Wenn Sie ein kundenspezifisches Etikettendesign einrichten, müssen Sie eine Abfrage erstellen, um das Kundenkonto zu finden. Im Inforegister **Details zur Wellenetikettenvorlage** wählen Sie **Abfrage bearbeiten** aus. Fügen Sie dann im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Lieferungen*
    - **Abgeleitete Tabelle:** *Lieferungen*
    - **Feld:** *Kontonummer*
    - **Kriterien:** Geben Sie die relevante Kundenkontonummer ein.

    Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.

1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus, um das Dialogfeld des Abfrage-Editors für die gesamte Etikettenvorlage zu öffnen.
1. Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Sortieren** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Referenzladungspositions-ID (Datensatz-ID)*
    - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.
1. In einem Meldungsfeld werden Sie aufgefordert, den Vorgang zum Zurücksetzen der Gruppierung zu bestätigen. Wählen Sie **Ja** aus, um fortzufahren.
1. Wählen Sie im Aktionsbereich **Wellenetikettenvorlagen-Gruppe** aus.
1. Im Dialogfeld **Wellenetikettenvorlagen-Gruppe** wählen Sie die Zeile aus, in der das Feld **Referenzfeldname** auf *Referenzladungspositions-ID* festgelegt ist und aktivieren Sie dann das Kontrollkästchen **Etiketten-Build-ID** für diese Zeile.

    > [!NOTE]
    > Dieses Setup erstellt eine Etikettensequenz („Karton 1 von X“) pro Ladeposition während der gesamten Welle, unabhängig vom Setup der Arbeitsgruppierung. Diese Etikettensequenz kann auf das Etikettenlayout gedruckt werden.

### <a name="configure-number-sequence-extensions"></a>Nummernkreiserweiterungen konfigurieren

Nummernkreiserweiterungen steuern die GS1-Konformität bestimmter Nummernkreise. Diese Konfiguration ist für das aktuelle Szenario optional. Weitere Informationen und Konfigurationsanweisungen finden Sie unter [Nummernkreiserweiterungen konfigurieren](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Einen Auftrag erstellen und ihn für den Lagerort freigeben

1. Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.
1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *62*

1. Fügen Sie zwei Auftragspositionen mit den folgenden Einstellungen hinzu:

    - Auftragsposition 1:

        - **Artikelnummer** *A001*
        - **Menge** *9024*
        - **Einheit:** *ea* (9024 Einzelstücke = 376 Kisten = 47 Paletten)

    - Auftragsposition 2:

        - **Artikelnummer:** *A0002*
        - **Menge** *9016*
        - **Einheit:** *ea* (9016 Einzelstücke = 322 Kisten = 46 Paletten)

    > [!NOTE]
    > Die hier angegebenen Artikel und Mengen sind nur Beispiele. Sie müssen die zuvor definierte Einheitsnummernkreisgruppe verwenden, für sie müssen entsprechende Einheitsumrechnungen von *ea* (Einzelstück) zu *Box* (Kiste) zu *PL* (Palette) definiert sein, und sie müssen Bestand im Lager haben *62*. Weitere Informationen finden Sie unter [Maßeinheit und Lagerhaltungsrichtlinien](unit-measure-stocking-policies.md).

1. Wählen Sie Auftragsposition 1 aus. Wählen Sie dann im Abschnitt **Auftragsposition** im Menü **Bestand** die Option **Reservierungen** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, und schließen Sie dann die Seite.
1. Wiederholen Sie die Schritte 4 und 5 für Auftragsposition 2.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Folgende Ereignisse treten auf:

    - Das System verarbeitet die erstellte Lieferung mithilfe der Vorlage, die den Etikettendruckschritt enthält. Das Etikettenlayout wird verwendet, um das Format des Etiketts zu definieren. Das Ergebnis ist ein Etikett, das auf dem in der Etikettenvorlage ausgewählten Drucker gedruckt wird.
    - Wellenetiketten werden generiert und gedruckt. Die Anzahl der Etikette entspricht der Anzahl der Kartons (in diesem Beispiel 376 Kartonetikette für Position 1 und 322 Kartonetikette für Position 2).
    - Für die Lieferung wird eine neue Frachtbrief-ID generiert. Wenn Sie die Nummernkreiserweiterungen konfiguriert haben, folgen die Wellenetikett-IDs dem Zahlenformat **SSCC-18**. 

Sie können Serienetiketten von den folgenden Seiten anzeigen und erneut drucken. Wählen Sie im Aktivitätsbereich jeder Seite, auf der Registerkarte **Lieferungen** in der Gruppe **Zugehörige Informationen** die Option **Serienetiketten**.

- Alle Lieferungen \> Lieferdetails
- Alle Ladungen \> Ladungsdetails
- Alle Wellen
- Serienetiketten
- Wellenbeschriftungsverlauf

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Szenario 2: Wellenetikettendruck zur Containerisierung (ohne Wellenetikettendatensätze)

In diesem Szenario können Sie Wellenetiketten drucken, wenn Sie die Containerisierung verwenden, um Artikel automatisch in Kartons aufzuteilen, und daher keinen Wellenetikettendatensatz benötigen. In diesem Fall fungiert die Container-ID als Platzhalter für den SSCC.

Hier sind die Hauptunterschiede zwischen diesem Szenario und Szenario 1:

- **Wellenetikettenvorlagen:** Sie wählen keinen Wellenetikettentyp in der Wellenetikettenvorlage aus und benötigen keine Etiketten-Build-Gruppierung. Andernfalls konfigurieren Sie die Wellenetikettenvorlage und verknüpfen sie mit der Wellenvorlage auf dieselbe Weise wie in Szenario 1 beschrieben. Sie müssen den Wellenetikettentyp leer lassen, um zu verhindern, dass Wellenetiketten generiert werden.
- **Wellenetikettenlayouts:** Sie konfigurieren die Zeileneinstellungen für das Wellenetikettenlayout für Arbeitspositionen anstelle von Wellenetikettendatensätzen. Sie müssen die Zeileneinstellung für das Etikettenlayout mithilfe der Tabelle **WHSWorkLine** anstelle der Tabelle **WHSWaveLabel** konfigurieren. Die Einstellung **Zeilen pro Seite** steuert die Anzahl der Zeilen, die der Textabschnitt haben wird. 

Diese Konfiguration eignet sich auch für Geschäftsszenarien, in denen mehrere verschiedene Artikel in eine etikettierte Schachtel oder auf einer Palette gepackt werden. Dieser Verpackungsprozess kann durch die Arbeitserstellung definiert werden (z. B. Arbeit, die nach Lieferung gruppiert wird).

Dieses Szenario zeigt den End-to-End-Flow.

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Um diesem Szenario zu folgen, müssen Demodaten installiert sein, und Sie müssen die juristische Person **USMF** auswählen.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Stellen Sie sicher, dass die Wellenetikettmethode verfügbar ist

Möglicherweise müssen Sie die Wellenprozessmethoden erneut generieren, um die Wellenetiketdruck-Methode verfügbar zu machen.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.
1. Bestätigen Sie, dass **waveLabelPrinting** in der Liste ist. Wenn nicht, wählen Sie im Aktionsbereich **Methoden erneut generieren** aus, um es hinzuzufügen.

### <a name="set-up-a-wave-template"></a>Richten Sie eine Wellenvorlage ein

Mit Wellenvorlagen können Sie bestimmte Instanzen von Wellenmethoden mit einer entsprechenden Wellenetikettenvorlage verknüpfen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Wählen Sie eine Vorlage aus, wie beispielsweise **63 Containerisierung**.
1. Im Inforegister **Methoden** verschieben Sie die Methode **Wellenetikettendruck** zur Spalte **Ausgewählte Methoden**.
1. Wählen Sie in der Spalte **Ausgewählte Methoden** die Methode **Wellenetikettendruck** aus, und legen Sie deren Feld **Wellenschrittcode** auf *PrintLabel* fest. Weitere Informationen über Wellenschrittcodes finden Sie unter [Wellenschrittcodes](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Ein Wellenetikettenlayout erstellen

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenlayouts**.
1. Erstellen Sie einen Datensatz mit den folgenden Einstellungen:

    - **Etikettenlayout-ID:** *Karton*
    - **Beschreibung:** *Karton (SSCC)*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktionsbereich **Einstellungen für Wellenetikettzeile** aus.

    Die Seite **Einstellungen für Wellenetikettzeile** wird angezeigt. Hier können Sie den dynamischen Teil des Etiketts konfigurieren.

1. Fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:

    - **Zeilen-ID:** *WorkLine*
    - **Zeilentabellenname:** *WHSWorkLine*
    - **Zeilenstartposition:** *500*

        Dieses Feld definiert die vertikale Position, an der die Zeile im Etikett beginnt.

    - **Zeilenhöhe:** *-50*

        Dieses Feld definiert die Höhe jeder Zeile. Die Zeilenhöhe ist positiv für horizontale Etikette und negativ für vertikale Etikette.

    - **Zeilen pro Seite:** *5*

        Dieses Feld definiert die Anzahl der Zeilen, die auf jedes Etikett gedruckt werden können.

        > [!NOTE]
        > Dieses Setup druckt mehrere ZPL-Etiketten pro Arbeit, wobei jede Seite bis zu fünf Arbeitspositionen enthalten kann. Wenn beispielsweise ein Etikett für einen Container mit 12 Positionen gedruckt wird, werden drei Etiketten gedruckt. Wenn Sie für jede Entnahmeposition ein separates Etikett drucken möchten, legen Sie diesen Wert auf *1* fest.

1. Schließen Sie die Seite.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Arbeitstyp*
    - **Kriterien:** *Entnahme*

1. Wenn Sie die Frachtbrief-ID ausdrucken möchten, wählen Sie auf der Registerkarte **Verknüpfungen** die Tabelle **Arbeitspositionen** aus, und verknüpften Sie die Tabelle **Lieferungen** damit.
1. Schließen Sie das Abfrage-Editor-Dialogfeld.
1. Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**. Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie Code für die erforderliche Kopfzeile ein. Wenn Sie beispielsweise Zebra-Drucker verwenden, können Sie den folgenden Code verwenden.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Im Abschnitt **Textabschnitt** im Feld **Etikettentext** geben Sie ZPL-Code für den erforderlichen Text ein. Hier ist ein Beispiel.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. Im Abschnitt **Textabschnitt** im Feld **Etikettenfußzeile** geben Sie ZPL-Code für die erforderlichen Fußzeile ein. Hier ist ein Beispiel.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Durch dieses Setup wird eine Kopie jedes Etiketts gedruckt. Wenn Sie mehr Kopien benötigen (z. B. eine Kopie für jede Seite der Palette), legen Sie den **n**-Wert für den Abschnitt **\^PQn** in der Fußzeile auf die erforderliche Anzahl von Kopien fest. Um vier Kopien jedes Etiketts zu drucken, geben Sie beispielsweise **\^PQ4** an.

Ihr Etikett kann jetzt verwendet werden.

### <a name="create-a-wave-label-template"></a>Eine Wellenetikettenvorlage erstellen

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenvorlagen**.
1. Fügen Sie eine Wellenetikettenvorlage hinzu und legen Sie die folgenden Werte in der Kopfzeile fest:

    - **Etikettenvorlagenname:** *Containeretikette*
    - **Beschreibung:** *Containeretikette*
    - **Wellenschrittcode:** *PrintLabel*
    - **Lagerort:** *63*

1. Im Inforegister **Details zur Wellenetikettenvorlage** fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:

    - **Etikettenlayout-ID:** *Container*
    - **Druckername:** Wählen Sie einen geeigneten ZPL-Drucker aus.
    - **Abfrage ausführen:** *Ja* (Diese Einstellung ist optional, wird jedoch für eine optimale Leistung empfohlen.)

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Optional: Wenn Sie ein kundenspezifisches Etikettendesign einrichten, müssen Sie eine Abfrage erstellen, um das Kundenkonto zu finden. Im Inforegister **Details zur Wellenetikettenvorlage** wählen Sie **Abfrage bearbeiten** aus. Fügen Sie dann im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Lieferungen*
    - **Abgeleitete Tabelle:** *Lieferungen*
    - **Feld:** *Kontonummer*
    - **Kriterien:** Geben Sie die relevante Kundenkontonummer ein.

    Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.

### <a name="configure-number-sequence-extensions"></a>Nummernkreiserweiterungen konfigurieren

Nummernkreiserweiterungen steuern die GS1-Konformität bestimmter Nummernkreise. Diese Konfiguration ist für das aktuelle Szenario optional. Weitere Informationen und Konfigurationsanweisungen finden Sie unter [Nummernkreiserweiterungen konfigurieren](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Einen Auftrag erstellen und ihn für den Lagerort freigeben

1. Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.
1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *63*

1. Fünf Auftragspositionen hinzufügen:

    - Auftragsposition 1:

        - **Artikelnummer** *A001*
        - **Menge** *10*

    - Auftragsposition 2:

        - **Artikelnummer:** *A0002*
        - **Menge** *20*

    - Auftragsposition 3:

        - **Artikelnummer:** *L0006*
        - **Menge** *20*

    - Auftragsposition 4:

        - **Artikelnummer:** *L0100*
        - **Menge** *40*

    - Auftragsposition 5:

        - **Artikelnummer:** *L0101*
        - **Menge** *50*

    > [!NOTE]
    > Die hier angegebenen Artikel und Mengen sind nur Beispiele. Sie müssen Lagerbestand im angegebenen Lager haben.

1. Wählen Sie Auftragsposition 1 aus. Wählen Sie dann im Abschnitt **Auftragsposition** im Menü **Bestand** die Option **Reservierungen** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, und schließen Sie dann die Seite.
1. Wiederholen Sie die Schritte 4 und 5 für jede zusätzliche Auftragsposition.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Folgende Ereignisse treten auf:

    - Das System verarbeitet die erstellte Lieferung mithilfe der Vorlage, die den Etikettendruckschritt enthält. Das Etikettenlayout wird verwendet, um das Format des Etiketts zu definieren. Das Endergebnis ist ein Etikett, das fünf Positionen hat und das auf dem in der Etikettenvorlage ausgewählten Drucker gedruckt wird.
    - Für die Lieferung wird eine neue Frachtbrief-ID generiert. Wenn Sie die Nummernkreiserweiterungen konfiguriert haben, folgen die Wellenetikett-IDs dem Zahlenformat **SSCC-18**. 

Sie können diese Wellenetiketten erneut drucken, indem Sie zu **Lagerortverwaltung \> Anfragen und Berichte \> Wellenetikettenverlauf** gehen.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Szenario 3: Wellenetikettendruck für mehrstufige Etiketten

Dieses Szenario zeigt, wie die Funktion zum Drucken von Wellenetiketten verwendet wird, wenn für die Lagerhaltungsprozesse mehrere Ebenen von Adressetiketten erforderlich sind. Beispielsweise müssen möglicherweise separate Etiketten für Kartons und Paletten gedruckt werden, und ein Unterbrechungsetikett muss möglicherweise für eine gesamte Lieferung gedruckt werden. Unterbrechungsetiketten sind ein separater Etikettentyp, der als Trenner zwischen Rollen und Containern verwendet werden kann, z. B. Etiketten für die Sendungs-ID und einen Barcode, so dass die Etiketten nach dem Druck leicht sortiert werden können.

Der Hauptunterschied zwischen der Konfiguration dieses Szenarios und der Konfiguration von Szenario 1 besteht neben der Tatsache, dass Unterbrechungsetiketten aktiviert sind, darin, dass mehrere Wellenetikettentypen den Wellenetikettenvorlagen und Einheitsnummernkreisgruppen-Positionen zugeordnet werden müssen. Um diese Konfiguration durchzuführen, richten Sie die folgenden Elemente für dieses Szenario ein:

- **Wellenverarbeitungsmethoden:** Sie markieren die Wellenetikettenmethode als „wiederholbar“, fügen sie zwei (oder mehrere) Male zur Wellenvorlage hinzu und legen verschiedene Wellenschrittcodes fest.
- **Wellenetikettenvorlagen:** Sie konfigurieren die Wellenetikettenvorlagen und verknüpfen sie mit der Wellenvorlage. Jede Wellenetikettenvorlage hat ihren eigenen Wellenetikettentyp.
- **Wellenetikettenlayouts:** Sie erstellen mehrere Wellenetikettenlayouts. Es wird ein separates Etikettenlayout für jede „Ebene“ von Etiketten geben, und es wird auch ein Unterbrechungsetikettenlayout geben.

Dieses Szenario zeigt den End-to-End-Flow.

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Um diesem Szenario zu folgen, müssen Demodaten installiert sein, und Sie müssen die juristische Person **USMF** auswählen.

### <a name="set-up-a-wave-process-method"></a>Eine Wellenverarbeitungsmethode einrichten

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.
1. Bestätigen Sie, dass **waveLabelPrinting** in der Liste ist. Wenn nicht, wählen Sie im Aktionsbereich **Methoden erneut generieren** aus, um es hinzuzufügen.
1. Für die Methode **waveLabelPrinting** aktivieren Sie das Kontrollkästchen **Methode wiederholbar machen**.

### <a name="set-up-a-wave-template"></a>Richten Sie eine Wellenvorlage ein

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
2. Wählen Sie eine Vorlage aus, wie beispielsweise **62 Lieferungsstandard**.
3. Im Inforegister **Methoden** verschieben Sie die Methode **Wellenetikettendruck** zur Spalte **Ausgewählte Methoden**.
4. In der Spalte **Ausgewählte Methoden** weisen Sie einen Wert **Wellenschrittcode**, wie z. B. *Karton*, der Methode **Wellenetikettendruck** zu. Weitere Informationen über Wellenschrittcodes finden Sie unter [Wellenschrittcodes](wave-step-codes.md).
5. Verschieben Sie die Methode **Wellenetikettendruck** ein zweites Mal zur Spalte **Ausgewählte Methoden**.
6. In der Spalte **Ausgewählte Methoden** weisen Sie einen anderen **Wellenschrittcode**-Wert, wie z. B. *Palette*, der zweiten **Wellenetikettendruck**-Methode zu. Weitere Informationen über Wellenschrittcodes finden Sie unter [Wellenschrittcodes](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Drei Wellenetikettenlayouts erstellen

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenlayouts**.
1. Erstellen Sie einen Datensatz mit den folgenden Einstellungen:

    - **Etikettenlayout-ID:** *Karton*
    - **Beschreibung:** *Karton (SSCC)*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktionsbereich **Einstellungen für Wellenetikettzeile** aus.

    Die Seite **Einstellungen für Wellenetikettzeile** wird angezeigt. Hier können Sie den dynamischen Teil des Etiketts konfigurieren.

1. Fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:

    - **Zeilen-ID:** *WaveLabel*
    - **Zeilentabellenname:** *WHSWaveLabel*
    - **Zeilenstartposition:** *0*

        Dieses Feld definiert die vertikale Position, an der die Zeile im Etikett beginnt.

    - **Zeilenhöhe:** *0*

        Dieses Feld definiert die Höhe jeder Zeile (in Punkten) gemäß dem ZPL-Standard. Die Zeilenhöhe ist positiv für horizontale Etikette und negativ für vertikale Etikette. Da es in diesem Beispiel nur eine Zeile gibt, können Sie den Wert auf *0* (Null) festlegen.

    - **Zeilen pro Seite:** *1*

        Dieses Feld definiert die Anzahl der Zeilen, die auf jedes Etikett gedruckt werden können.

        > [!NOTE]
        > Durch dieses Setup wird für jeden Datensatz in der Wellenetikettentabelle ein separates ZPL-Etikett gedruckt.

1. Schließen Sie die Seite.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Arbeitstyp*
    - **Kriterien:** *Entnahme*

    Diese Abfrage stellt sicher, dass nur Arbeitspositionen vom Entnahmetyp auf dem Etikett gedruckt werden und nicht Arbeitspositionen vom Einlagerungstyp.

1. Wenn Sie die Frachtbrief-ID ausdrucken möchten, wählen Sie auf der Registerkarte **Verknüpfungen** die Tabelle **Arbeitspositionen** aus, und verknüpften Sie die Tabelle **Lieferungen** damit. 
1. Schließen Sie das Abfrage-Editor-Dialogfeld.
1. Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**. Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie Code für die erforderliche Kopfzeile ein. Wenn Sie beispielsweise Zebra-Drucker verwenden, können Sie den folgenden Code verwenden.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Im Abschnitt **Textabschnitt** im Feld **Etikettentext** geben Sie ZPL-Code für den erforderlichen Text ein. Hier ist ein Beispiel.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Im Abschnitt **Textabschnitt** im Feld **Etikettenfußzeile** geben Sie ZPL-Code für die erforderlichen Fußzeile ein. Hier ist ein Beispiel.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Durch dieses Setup wird eine Kopie jedes Etiketts gedruckt. Wenn Sie mehr Kopien benötigen (z. B. eine Kopie für jede Seite der Palette), legen Sie den **n**-Wert für den Abschnitt **\^PQn** in der Fußzeile auf die erforderliche Anzahl von Kopien fest. Um vier Kopien jedes Etiketts zu drucken, geben Sie beispielsweise **\^PQ4** an.

1. Das erste Etikett kann jetzt verwendet werden.
1. Erstellen Sie einen zweiten Layoutdatensatz mit den folgenden Einstellungen:

    - **Etikettenlayout-ID:** *Palette*
    - **Beschreibung:** *Palette*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktionsbereich **Einstellungen für Wellenetikettzeile** aus.

    Die Seite **Einstellungen für Wellenetikettzeile** wird angezeigt. Hier können Sie den dynamischen Teil des Etiketts konfigurieren.

1. Fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:

    - **Zeilen-ID:** *WaveLabel*
    - **Zeilentabellenname:** *WHSWaveLabel*
    - **Zeilenstartposition:** *0*

        Dieses Feld definiert die vertikale Position, an der die Zeile im Etikett beginnt.

    - **Zeilenhöhe:** *0*

        Dieses Feld definiert die Höhe jeder Zeile (in Punkten) gemäß dem ZPL-Standard. Die Zeilenhöhe ist positiv für horizontale Etikette und negativ für vertikale Etikette. Da es in diesem Beispiel nur eine Zeile gibt, können Sie den Wert auf *0* (Null) festlegen.

    - **Zeilen pro Seite:** *1*

        Dieses Feld definiert die Anzahl der Zeilen, die auf jedes Etikett gedruckt werden können.

        > [!NOTE]
        > Durch dieses Setup wird für jeden Datensatz in der Wellenetikettentabelle ein separates ZPL-Etikett gedruckt.

1. Schließen Sie die Seite.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Arbeitstyp*
    - **Kriterien:** *Entnahme*

    Diese Abfrage stellt sicher, dass nur Arbeitspositionen vom Entnahmetyp auf dem Etikett gedruckt werden und nicht Arbeitspositionen vom Einlagerungstyp.

1. Wenn Sie die Frachtbrief-ID ausdrucken möchten, wählen Sie auf der Registerkarte **Verknüpfungen** die Tabelle **Arbeitspositionen** aus, und verknüpften Sie die Tabelle **Lieferungen** damit.
1. Schließen Sie das Abfrage-Editor-Dialogfeld.
1. Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**. Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie Code für die erforderliche Kopfzeile ein. Wenn Sie beispielsweise Zebra-Drucker verwenden, können Sie den folgenden Code verwenden.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Im Abschnitt **Textabschnitt** im Feld **Etikettentext** geben Sie ZPL-Code für den erforderlichen Text ein. Hier ist ein Beispiel.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. Im Abschnitt **Textabschnitt** im Feld **Etikettenfußzeile** geben Sie ZPL-Code für die erforderlichen Fußzeile ein. Hier ist ein Beispiel.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Durch dieses Setup wird eine Kopie jedes Etiketts gedruckt. Wenn Sie mehr Kopien benötigen (z. B. eine Kopie für jede Seite der Palette), legen Sie den **n**-Wert für den Abschnitt **\^PQn** in der Fußzeile auf die erforderliche Anzahl von Kopien fest. Um vier Kopien jedes Etiketts zu drucken, geben Sie beispielsweise **\^PQ4** an.

1. Das zweite Etikett kann jetzt verwendet werden.
1. Erstellen Sie einen dritten Layoutdatensatz mit den folgenden Einstellungen:

    - **Etikettenlayout-ID:** *Unterbrechung*
    - **Beschreibung:** *Unterbrechungsetikett*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**. Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie den ZPL-Code für die erforderliche Kopfzeile ein. Hier ist ein Beispiel.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Diesmal ist kein Textabschnitt erforderlich. Geben Sie daher einfach den gewünschten Text in den Abschnitt **Fußzeilenabschnitt** ein. Hier ist ein Beispiel.

    ```plaintext
    ^XZ
    ```

    Das dritte Etikett kann jetzt verwendet werden.

    > [!NOTE]
    > Dieses dritte Etikett ist ein Unterbrechungsetikett, das als Teiler zwischen Etikettenrollen verwendet wird.

### <a name="create-two-wave-label-types"></a>Zwei Wellenetikettentypen erstellen

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettentypen**.
1. Erstellen Sie einen Datensatz mit den folgenden Einstellungen:

    - **Etikettentyp:** *Karton*
    - **Beschreibung:** *Karton*

1. Erstellen Sie einen zweiten Datensatz mit den folgenden Einstellungen:

    - **Etikettentyp:** *Palette*
    - **Beschreibung:** *Palette*

### <a name="set-up-unit-sequence-groups"></a>Einheitensequenzgruppen einrichten

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Lagerort \> Einheitsnummernkreisgruppe**.
1. Wählen oder erstellen Sie eine Gruppe **Ea Box PL** (Einzelstücke Kiste/Palette).
1. Für die Position **Kiste** legen Sie das Feld **Wellenetikettentyp** auf *Karton* fest.
1. Für die Position **PL** (Palette) legen Sie das Feld **Wellenetikettentyp** auf *Palette* fest.

### <a name="create-wave-label-templates"></a>Wellenetikettenvorlagen erstellen

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenvorlagen**.
1. Erstellen Sie eine Etikettenvorlage mit den folgenden Einstellungen:

    - **Etikettenvorlagenname:** *Kartonetikette*
    - **Beschreibung:** *Kartonetikette*
    - **Wellenschrittcode:** *Karton*
    - **Lagerort:** *62*

1. Wählen Sie im Inforegister **Allgemein** im Feld **Wellenetikettentyp** einen Wert aus, wie z. B. *Karton*.
1. Im Inforegister **Details zur Wellenetikettenvorlage** fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:

    - **Etikettenlayout-ID:** *Karton*
    - **Druckername:** Wählen Sie einen geeigneten ZPL-Drucker aus.
    - **Abfrage ausführen:** *Ja* (Diese Einstellung ist optional, wird jedoch für eine optimale Leistung empfohlen.)

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Optional: Wenn Sie ein kundenspezifisches Etikettendesign einrichten, müssen Sie eine Abfrage erstellen, um das Kundenkonto zu finden. Im Inforegister **Details zur Wellenetikettenvorlage** wählen Sie **Abfrage bearbeiten** aus. Fügen Sie dann im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Lieferungen*
    - **Abgeleitete Tabelle:** *Lieferungen*
    - **Feld:** *Kontonummer*
    - **Kriterien:** Geben Sie die relevante Kundenkontonummer ein.

    Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.

1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus, um das Dialogfeld des Abfrage-Editors für die gesamte Etikettenvorlage zu öffnen.
1. Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Sortieren** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Referenzladungspositions-ID (Datensatz-ID)*
    - **Suchrichtigung:** *Aufsteigend*

1. Fügen Sie eine zweite Zeile mit den folgenden Einstellungen hinzu:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Lieferungs-ID*
    - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.
1. In einem Meldungsfeld werden Sie aufgefordert, den Vorgang zum Zurücksetzen der Gruppierung zu bestätigen. Wählen Sie **Ja** aus, um fortzufahren.
1. Wählen Sie im Aktionsbereich **Wellenetikettenvorlagen-Gruppe** aus.
1. Legen Sie im Dialogfeld **Wellenetiketten-Vorlagengruppe** für die Zeile, in der das Feld **Referenzfeldname** auf *Lieferungs-ID* festgelegt ist, die folgenden Werte fest:

    - **Unterbrechungsetikett drucken:** Aktivieren Sie dieses Kontrollkästchen.
    - **Etikettenlayout-ID:** Wählen Sie ein Unterbrechungsetikett aus. (Wählen Sie zum Beispiel das Etikettenlayout *Unterbrechung* aus, dass Sie zuvor in diesem Szenario erstellt haben.)
    - **Druckername:** Wählen Sie den Drucker für das Unterbrechungsetikett aus. (Normalerweise sollten Sie zum Teilen von Etikettenrollen denselben Drucker auswählen, der im Inforegister **Details zur Wellenetikettenvorlage** ausgewählt ist. Es sind jedoch andere Szenarien möglich.)

1. Für die Zeile, in der das Feld **Referenzfeldname** auf *Referenzladungspositions-ID* festgelegt ist, aktivieren Sie das Kontrollkästchen **Etiketten-Build-ID**.

    > [!NOTE]
    > Dieses Setup erstellt eine Etikettensequenz („Karton 1 von X“) pro Ladeposition während der gesamten Welle, unabhängig vom Setup der Arbeitsgruppierung. Diese Etikettensequenz kann auf ein Etikettenlayout gedruckt werden. Außerdem werden Etiketten für verschiedene Lieferungen durch das ausgewählte Unterbrechungsetikett getrennt.

1. Wählen Sie **OK** aus, um das Dialogfeld **Wellenetiketten-Vorlagengruppe** zu schließen.
1. Erstellen Sie eine zweite Etikettenvorlage mit den folgenden Einstellungen:

    - **Etikettenvorlagenname:** *Palettenetikette*
    - **Beschreibung:** *Palettenetikette*
    - **Wellenschrittcode:** *Palette*
    - **Lagerort:** *62*

1. Wählen Sie im Inforegister **Allgemein** im Feld **Wellenetikettentyp** einen Wert aus, wie z. B. *Palette*.
1. Im Inforegister **Details zur Wellenetikettenvorlage** fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:

    - **Etikettenlayout-ID:** *Palette*
    - **Druckername:** Wählen Sie einen geeigneten ZPL-Drucker aus.
    - **Abfrage ausführen:** *Ja* (Diese Einstellung ist optional, wird jedoch für eine optimale Leistung empfohlen.)

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Optional: Wenn Sie ein kundenspezifisches Etikettendesign einrichten, müssen Sie eine Abfrage erstellen, um das Kundenkonto zu finden. Im Inforegister **Details zur Wellenetikettenvorlage** wählen Sie **Abfrage bearbeiten** aus. Fügen Sie dann im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Lieferungen*
    - **Abgeleitete Tabelle:** *Lieferungen*
    - **Feld:** *Kontonummer*
    - **Kriterien:** Geben Sie die relevante Kundenkontonummer ein.

    Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen. 

1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus, um das Dialogfeld des Abfrage-Editors für die gesamte Etikettenvorlage zu öffnen.
1. Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Sortieren** eine Zeile mit den folgenden Einstellungen ein:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Referenzladungspositions-ID (Datensatz-ID)*
    - **Suchrichtigung:** *Aufsteigend*

1. Fügen Sie eine zweite Zeile mit den folgenden Einstellungen hinzu:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Lieferungs-ID*
    - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.
1. In einem Meldungsfeld werden Sie aufgefordert, den Vorgang zum Zurücksetzen der Gruppierung zu bestätigen. Wählen Sie **Ja** aus, um fortzufahren.
1. Wählen Sie im Aktionsbereich **Wellenetikettenvorlagen-Gruppe** aus.
1. Legen Sie im Dialogfeld **Wellenetiketten-Vorlagengruppe** für die Zeile, in der das Feld **Referenzfeldname** auf *Lieferungs-ID* festgelegt ist, die folgenden Werte fest:

    - **Unterbrechungsetikett drucken:** Aktivieren Sie dieses Kontrollkästchen.
    - **Etikettenlayout-ID:** Wählen Sie ein Unterbrechungsetikett aus. (Wählen Sie zum Beispiel das Etikettenlayout *Unterbrechung* aus, dass Sie zuvor in diesem Szenario erstellt haben.)
    - **Druckername:** Wählen Sie den Drucker für das Unterbrechungsetikett aus. (Normalerweise sollten Sie zum Teilen von Etikettenrollen denselben Drucker auswählen, der im Inforegister **Details zur Wellenetikettenvorlage** ausgewählt ist. Es sind jedoch andere Szenarien möglich.)

1. Für die Zeile, in der das Feld **Referenzfeldname** auf *Referenzladungspositions-ID* festgelegt ist, aktivieren Sie das Kontrollkästchen **Etiketten-Build-ID**.

    > [!NOTE]
    > Dieses Setup erstellt eine Etikettensequenz („Karton 1 von X“) pro Ladeposition während der gesamten Welle, unabhängig vom Setup der Arbeitsgruppierung. Diese Etikettensequenz kann auf ein Etikettenlayout gedruckt werden. Außerdem werden Etiketten für verschiedene Lieferungen durch das ausgewählte Unterbrechungsetikett getrennt.

### <a name="configure-number-sequence-extensions"></a>Nummernkreiserweiterungen konfigurieren

Nummernkreiserweiterungen steuern die GS1-Konformität bestimmter Nummernkreise. Diese Konfiguration ist für das aktuelle Szenario optional. Weitere Informationen und Konfigurationsanweisungen finden Sie unter [Nummernkreiserweiterungen konfigurieren](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Einen Auftrag erstellen und ihn für den Lagerort freigeben

1. Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.
1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *62*

1. Zwei Auftragspositionen hinzufügen:

    - Auftragsposition 1:

        - **Artikelnummer** *A001*
        - **Menge** *9024*
        - **Einheit:** *ea* (9024 Einzelstücke = 376 Kisten = 47 Paletten)

    - Auftragsposition 2:

        - **Artikelnummer:** *A0002*
        - **Menge** *9016*
        - **Einheit:** *ea* (9016 Einzelstücke = 322 Kisten = 46 Paletten)

    > [!NOTE]
    > Die hier angegebenen Artikel und Mengen sind nur Beispiele. Sie müssen die zuvor definierte Einheitsnummernkreisgruppe verwenden, für sie müssen entsprechende Einheitsumrechnungen von *ea* (Einzelstück) zu *Box* (Kiste) zu *PL* (Palette) definiert sein, und sie müssen Bestand im Lager haben *62*. Weitere Informationen finden Sie unter [Maßeinheit und Lagerhaltungsrichtlinien](unit-measure-stocking-policies.md).

1. Wählen Sie Auftragsposition 1 aus. Wählen Sie dann im Abschnitt **Auftragsposition** im Menü **Bestand** die Option **Reservierungen** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, und schließen Sie dann die Seite.
1. Wiederholen Sie die Schritte 4 und 5 für Auftragsposition 2.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Folgende Ereignisse treten auf: 

    - Das System verarbeitet die erstellte Lieferung mithilfe der Vorlage, die den Etikettendruckschritt enthält. Das Etikettenlayout wird verwendet, um das Format des Etiketts zu definieren. Das Ergebnis ist ein Etikett, das auf dem in der Etikettenvorlage ausgewählten Drucker gedruckt wird.
    - Wellenetiketten werden generiert und gedruckt. Die Anzahl der Etiketten entspricht der Anzahl der Kartons (in diesem Beispiel 376 Kistenetiketten für Position 1, 322 Kistenetiketten für Position 2, 47 PL-Etiketten für Position 1, 47 PL-Etiketten für Position 2 und zwei Unterbrechungsetiketten mit der Lieferungs-ID).
    - Für die Lieferung wird eine neue Frachtbrief-ID generiert. Wenn Sie die Nummernkreiserweiterungen konfiguriert haben, folgen die Wellenetikett-IDs dem Zahlenformat **SSCC-18**. 

Sie können Wellenetiketten von den folgenden Seiten anzeigen und erneut drucken:

- Alle Lieferungen \> Lieferdetails
- Alle Ladungen \> Ladungsdetails
- Alle Wellen
- Serienetiketten
- Wellenbeschriftungsverlauf

Für die meisten dieser Seiten finden Sie die relevante Funktion durch Auswahl der **Wellenetiketten** in der Gruppe **Zugehörige Informationen** auf der Registerkarte **Lieferungen** des Aktionsbereichs.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Serienetiketten neu drucken und Wellenbeschriftungen stornieren](reprint-and-void-wave-labels.md)
- [Wellenetikettendruck während der Welle einplanen](configure-task-based-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
