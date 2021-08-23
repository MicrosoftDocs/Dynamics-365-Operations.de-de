---
title: Steuerelemente für Word-Inhalte in generierten Berichten unterdrücken
description: In diesem Thema wird erläutert, wie Sie ein EB-Format (elektronische Berichterstellung) konfigurieren, um Berichte als Microsoft Word-Dateien zu generieren, in denen Inhaltssteuerelemente unterdrückt sind.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: cfabd6f544dca6f48448da4ef9ff8383c6583f8488a718a7c971ff7b39c1f2cb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737974"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Steuerelemente für Word-Inhalte in generierten Berichten unterdrücken

[!include [banner](../includes/banner.md)]

Um Berichte als Microsoft Word-Dokumente zu generieren, müssen Sie für diese eine Vorlage als Word-Dokument entwerfen. Diese Vorlage muss Steuerelemente für Word-Inhalte als Platzhalter für Daten enthalten, die während der Laufzeit ausgefüllt werden. Um das für Ihre Berichte als Vorlage erstellte Word-Dokument zu verwenden, können Sie eine neue [Lösung](er-quick-start1-new-solution.md) für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) [konfigurieren](er-design-configuration-word.md). Die Lösung muss eine EB-[Konfiguration](general-electronic-reporting.md#Configuration) enthalten, die eine Komponente im EB-[Format](general-electronic-reporting.md#FormatComponentOutbound) aufweist. Dieses EB-Format muss so konfiguriert sein, dass die entworfene Vorlage für die Berichtsgenerierung verwendet wird.

In Dynamics 365 Finance Version 10.0.6 und höher können Sie Formeln in Ihrem EB-Format konfigurieren, um einige Word-Inhaltssteuerelemente in generierten Dokumenten zu unterdrücken.

Die folgenden Schritten erläutern, wie ein Benutzer, der dem Systemadministrator oder der Rolle als funktionaler Berater für die elektronische Berichterstellung zugewiesen ist, ein EB-Format konfigurieren kann, das Berichte als Word-Dateien generiert und einige Inhaltssteuerelemente in den generierten Berichten unterdrückt, die mithilfe einer Word-Vorlage konfiguriert wurden.

Diese Schritte können im Unternehmen GBSI ausgeführt werden.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie diese Schritte ausführen können, müssen Sie zuerst diejenigen in diesen Aufgabenleitfäden ausführen:

- [Entwerfen einer Konfiguration für das Erstellen von Berichten im OPENXML-Format](./tasks/er-design-reports-openxml-2016-11.md)
- [EB-Konfigurationen mit Excel-Vorlagen erneut verwenden, um Berichte im Word-Format zu generieren](./tasks/er-design-configuration-word-2016-11.md)

Wenn Sie die Schritte dieser Aufgabenleitfäden ausführen, werden die folgenden Elemente vorbereitet:

- ein EB-Format **Beispiel-Arbeitsblattbericht**, das zum Generieren eines Dokuments im Word-Format konfiguriert ist
- eine [Entwurfsversion](general-electronic-reporting.md#component-versioning) des EB-Formats **Beispiel-Arbeitsblattbericht**, das als **Ausführbar** gekennzeichnet ist
- eine **elektronische** Zahlungsmethode, die für die Verwendung des EB-Formats **Beispiel-Arbeitsblattbericht** zur Verarbeitung von Kreditorenzahlungen konfiguriert ist

Außerdem müssen Sie die folgende Vorlage für den Beispielbericht herunterladen und speichern:

- [Begrenzte Vorlage 2 eines Zahlungsberichtes (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Überprüfen der heruntergeladenen Word-Vorlage

1. Öffnen Sie in der Word-Desktopanwendung die Vorlagendatei **SampleVendPaymDocReportBounded2.docx**, die Sie zuvor heruntergeladen haben.
2. Stellen Sie sicher, dass die Vorlagendatei einen Zusammenfassungsabschnitt enthält, in dem die gesamten Zahlungsbeträge für jeden Währungscode angezeigt werden, der in den verarbeiteten Zahlungen erfüllt wurde.

    - Der Zusammenfassungsabschnitt befindet sich in einer separaten Tabelle des Word-Dokuments.
    - Die erste Zeile dieser Tabelle enthält die Überschriften der Tabellenspalten als Abschnittsüberschrift.
    - Die zweite Zeile dieser Tabelle enthält das Steuerelement für sich wiederholende Inhalte als Abschnittsdetails.
    - Dieses Inhaltssteuerelement ist dem Feld **SummaryLines** im benutzerdefinierten XML-Teil **Bericht** zugeordnet.
    - Basierend auf dieser Zuordnung ist das Inhaltssteuerelement dem Element **SummaryLines** des bearbeitbaren EB-Formats zugeordnet.

    > [!NOTE]
    > Das sich wiederholende Inhaltssteuerelement wird durch den Schlüssel **SummaryLines** gekennzeichnet, der dem Feld des benutzerdefinierten XML-Teils entspricht, dem es zugeordnet wurde.

    ![Layout der Word-Vorlage.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Wählen Sie die vorhandene ER-Berichtskonfiguration aus

Für die folgenden Schritte werden Sie die vorhandene EB-Konfiguration nutzen, die Sie konfiguriert haben, als Sie die Schritte in den zuvor genannten Aufgabenleitfäden ausgeführt haben.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur den Punkt **Zahlungsmodell**, und wählen Sie dann **Beispiel-Arbeitsblattbericht** aus.
4. Wählen Sie **Designer** aus, um die Entwurfsversion des ausgewählten EB-Formats zu bearbeiten.

## <a name="replace-the-current-template-with-the-new-template"></a>Die aktuelle Vorlage durch die neue Vorlage ersetzen

Aktuell wird die Datei „SampleVendPaymDocReportBounded.docx“ als Vorlage verwendet, um die Ausgabe im Word-Format zu generieren. In den folgenden Schritten werden Sie diese Word-Vorlage durch die neue Word-Vorlage „SampleVendPaymDocReportBounded2.docx“ ersetzen, die Sie zuvor heruntergeladen haben.

1. Wählen Sie auf der Seite **Formatdesigner** die Option **Anhänge** aus.
2. Wählen Sie auf der Seite **Anhänge** die Option **Löschen** aus, um die vorhandene Vorlage zu entfernen.
3. Wählen Sie **Ja** aus, um das Löschen zu bestätigen.
4. Wählen Sie **Neu** \> **Datei** aus.
5. Wählen Sie **Durchsuchen** aus, navigieren Sie zu der Datei **SampleVendPaymDocReportBounded2.docx**, die Sie zuvor heruntergeladen haben, und wählen Sie sie aus.
6. Wählen Sie **OK**.
7. Schließen Sie die Seite **Anhänge**.
8. Geben Sie auf der Seite **Formatdesigner** im Feld **Vorlage** die Datei **SampleVendPaymDocReportBounded2.docx** ein, oder wählen Sie diese aus.

## <a name="run-the-format-to-create-word-output"></a>Das Format zum Erstellen der Word-Ausgabe ausführen

1. Rufen Sie **Kreditorenkonten** \> **Zahlungen** \> **Zahlungserfassung** aus.
2. Wählen Sie auf der Registerkarte **Liste** der Seite **Kreditorenzahlungen** alle Zahlungen aus.
3. Wählen Sie **Zahlungsstatus** \> **Keiner** aus.
4. Wählen Sie **Zahlungen generieren** aus.
5. Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.
6. Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.
7. Wählen Sie **OK**.
8. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **OK** aus, und analysieren Sie die generierte Ausgabe.

    ![Zahlungen zur Verarbeitung auf der Seite „Kreditorenzahlungen“.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Die Ausgabe wird im Word-Format dargestellt und enthält den Zusammenfassungsabschnitt.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Das bearbeitbare Format konfigurieren, um den Zusammenfassungsabschnitt zu unterdrücken

Wenn Sie den Zusammenfassungsabschnitt in einem generierten Dokument auf Anforderung eines Benutzers, der dieses EB-Format ausführt, unterdrücken möchten, müssen Sie das bearbeitbare EB-Format modifizieren.

1. Rufen Sie **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung** aus, und öffnen Sie zum Bearbeiten die Entwurfsversion des EB-Formats.
2. Wählen Sie **Berichterstellungskonfigurationen** aus. 
3. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur den Punkt **Zahlungsmodell** \> **Beispiel-Arbeitsblattbericht**.
4. Wählen Sie **Designer** aus.
5. Erweitern Sie auf der Seite **Formatdesigner** den Punkt **Word**, und wählen Sie **SummaryLines** aus.
6. Fügen Sie der Registerkarte **Zuordnung** eine neue Datenquelle hinzu, um den Benutzer während der Laufzeit zu fragen, ob der Zusammenfassungsabschnitt unterdrückt werden soll:

    1. Wählen Sie **Stamm hinzufügen** aus.
    2. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** die Option **Allgemein\Benutzereingabeparameter** aus, um das Dialogfeld **Datenquelleneigenschaften ‚Benutzereingabeparameter‛** zu öffnen.
    3. Geben Sie im Feld **Name** **uipSuppress** ein.
    4. Geben Sie im Feld **Beschriftung** **Zusammenfassungsabschnitt unterdrücken** ein.
    5. Geben Sie im Feld **Name des Betriebsdatentyps** **NoYes** ein, oder wählen Sie dies aus.
    6. Wählen Sie **OK**.

7. Fügen Sie eine neue Datenquelle des Anwendungsenumerationstyps **NoYes** hinzu:

    1. Wählen Sie **Stamm hinzufügen** aus.
    2. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** die Option **Dynamics 365 for Operations\Enumeration** aus, um das Dialogfeld **Datenquelleneigenschaften ‚Enumeration‛** zu öffnen.
    3. Geben Sie im Feld **Name** die Bezeichnung **enumNoYes** ein.
    4. Geben Sie im Feld **Beschriftung** **Optionen unterdrücken** ein.
    5. Geben Sie im Feld **Name des Betriebsdatentyps** **NoYes** ein, oder wählen Sie dies aus.
    6. Wählen Sie **OK**.

8. Konfigurieren Sie die Formel für das ausgewählte Formatelement **SummaryLines** so, dass angegeben wird, wann das dem ausgewählten Formatelement zugeordnete Word-Inhaltssteuerelement unterdrückt werden soll:

    1. Wählen Sie auf der Registerkarte **Zuordnung** im Abschnitt **Entfernt** die Option **Bearbeiten** aus, um die Seite **[Formeldesigner](general-electronic-reporting-formula-designer.md)** zu öffnen.
    2. Geben Sie im Feld **Formel** die Formel `uipSuppress = enumNoYes.Yes` ein.
    3. Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.

        > [!NOTE]
        > Diese Formel wird auf ein generiertes Dokument angewendet, **nachdem alle anderen Formatelemente ausgeführt wurden**. Zur Anwendung dieser Formel gibt es ein Word-Inhaltssteuerelement, das als für die Formel konfiguriertes Formatelement gekennzeichnet ist (**SummaryLines** in diesem Fall), in einem generierten Dokument. Dieses Inhaltssteuerelement wird dann zusammen mit der Zeile in der Word-Tabelle, in der es enthalten ist, vollständig entfernt. Die Detailzeile des Zusammenfassungsabschnitts wird aus dem generierten Dokument entfernt.
        >
        > In der Entwurfsphase können Sie die **Entfernt**-Formel für ein Formatelement konfigurieren, obwohl kein Inhaltssteuerelement in der von Ihnen verwendeten Word-Vorlage eine Markierung enthält, die dem Namen eines Formatelements entspricht, für das die **Entfernt**-Eigenschaft konfiguriert wurde. Wenn Sie das Format in der Entwurfsphase validieren, erhalten Sie eine [Warnung](er-components-inspections.md#i14) hinsichtlich dieser Inkonsistenz.
        >
        > Während der Laufzeit wird eine Ausnahme ausgelöst, wenn kein Inhaltssteuerelement in der von Ihnen verwendeten Word-Vorlage eine Markierung enthält, die dem Namen eines Formatelements entspricht, für das die **Entfernt**-Eigenschaft konfiguriert wurde.

    4. Setzen Sie auf der Registerkarte **Zuordnung** im Abschnitt **Entfernt** die Option **Mit übergeordnetem Element** auf **Ja**.

        > [!NOTE]
        > Sie müssen diese Option auf **Ja** setzen, um die gesamte Word-Tabelle als übergeordnetes Objekt der Zeile, die die Details des Zusammenfassungsabschnitts enthält, zu entfernen. Wenn Sie diese Option auf **Nein** setzen, verbleibt die Abschnittsüberschriftenzeile im generierten Dokument.

9. Wählen Sie **Speichern** aus, um Ihre Änderungen im bearbeitbaren Format zu speichern.

    ![Die generierte Ausgabe im Word-Format.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Das geänderte Format zum Erstellen der Word-Ausgabe ausführen

1. Rufen Sie **Kreditorenkonten** \> **Zahlungen** \> **Zahlungserfassung** aus.
2. Wählen Sie die erstellte Zahlungserfassung aus, und wählen Sie anschließend **Positionen** aus.
3. Wählen Sie auf der Seite **Kreditorenzahlungen** alle Zeilen und anschließend **Zahlungsstatus** \> **Keiner** aus.
4. Wählen Sie **Zahlungen generieren** aus.
5. Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.
6. Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.
7. Wählen Sie **OK**.
8. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** im Feld **Zusammenfassungsabschnitt unterdrücken** die Option **Ja** aus.
9. Wählen Sie **OK** aus, und analysieren Sie die generierte Ausgabe.

    ![Generierte Ausgabe im Word-Format.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Beachten Sie, dass die Ausgabe den Zusammenfassungsabschnitt nicht enthält, da er unterdrückt wurde.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Entwerfen einer Konfiguration für das Erstellen von Berichten im OPENXML-Format](./tasks/er-design-reports-openxml-2016-11.md)
- [ER-Konfigurationen zum Generieren von Berichten im Word-Format entwerfen](er-design-configuration-word.md)
- [EB-Konfigurationen mit Excel-Vorlagen erneut verwenden, um Berichte im Word-Format zu generieren](./tasks/er-design-configuration-word-2016-11.md)
- [Konfigurierte EB-Komponente überprüfen, um Laufzeitprobleme zu vermeiden](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]