---
title: EB-Konfigurationen mit Excel-Vorlagen wiederverwenden, um Berichte im Word-Format zu erstellen
description: In diesem Thema wird beschrieben, wie Berichtsformate, die zum Generieren von Berichten als Excel-Arbeitsmappen entwickelt wurden, so konfiguriert werden können, dass Berichte als Word-Dokumente generiert werden.
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769913fd0344eb276b3b1bd055255272ca5dfffd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092715"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>EB-Konfigurationen mit Excel-Vorlagen wiederverwenden, um Berichte im Word-Format zu erstellen

[!include [banner](../../includes/banner.md)]

Um Berichte als Microsoft Word-Dokumente zu generieren, können Sie ein neues [EB-](../general-electronic-reporting.md)[Format](../general-electronic-reporting.md#FormatComponentOutbound) (elektronische Berichterstellung) [konfigurieren](../er-design-configuration-word.md). Alternativ können Sie ein EB-Format wiederverwenden, das ursprünglich zum Generieren von Berichten als Excel-Arbeitsmappen entwickelt wurde. In diesem Fall müssen Sie die Excel-Vorlage durch eine Word-Vorlage ersetzen.

Die folgenden Verfahren zeigen, wie ein Benutzer in der Rolle des Systemadministrators oder des Entwicklers für elektronische Berichterstellung ein EB-Format konfigurieren kann, um Berichte als Word-Dateien zu generieren, indem er ein EB-Format wiederverwendet, das zum Generieren von Berichten als Excel-Dateien entwickelt wurde.

Diese Prozeduren können im Unternehmen GBSI ausgeführt werden.

## <a name="prerequisites"></a>Voraussetzungen

Um diese Prozeduren abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden [Entwerfen einer Konfiguration für das Generieren von Berichten im OPENXML-Format](er-design-reports-openxml-2016-11.md) abschließen.

Sie müssen auch die folgenden Vorlagen für den Beispielbericht herunterladen und lokal speichern:

- [Vorlage eines Zahlungsberichtes (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=862266)
- [Begrenzte Vorlage eines Zahlungsberichtes (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=862266)

Diese Prozeduren gelten für eine Funktion, die Dynamics 365 for Operations Version 1611 (November 2016) hinzugefügt wurde.

## <a name="select-the-existing-er-report-configuration"></a>Wählen Sie die vorhandene ER-Berichtskonfiguration aus

1. Wechseln Sie in Dynamics 365 Finance zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Stellen Sie sicher, dass der Konfigurationsanbieter **Litware, Inc.** als **Aktiv** ausgewählt ist. Wenn dies nicht der Fall ist, befolgen Sie die Schritte im Aufgabenleitfaden [Erstellen von Konfigurationsanbietern und Markieren als aktiv](er-configuration-provider-mark-it-active-2016-11.md).
3. Wählen Sie **Berichterstellungskonfigurationen** aus. Sie verwenden die vorhandene EB-Koniguration erneut, die entworfen wurde, um die Berichtsausgabe im OPENXML-Format zu generieren.
4. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **Beispiel-Arbeitsblattbericht** aus.

    > [!NOTE]
    > Die Entwurfsversion des ausgewählten EB-Formats kann im Inforegister **Versionen** bearbeitet werden.

5. Wählen Sie **Designer** aus.
6. Beachten Sie auf der Seite **Format-Designer**, dass der Titel des Stammformatelements angibt, dass derzeit eine Excel-Vorlage verwendet wird.

![Auswählen der vorhandenen Konfiguration](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Überprüfen der heruntergeladenen Word-Vorlage

1. Öffnen Sie in der Word-Desktopanwendung die Vorlagendatei **SampleVendPaymDocReport.docx**, die Sie zuvor heruntergeladen haben.
2. Stellen Sie sicher, dass diese Vorlage nur das Layout des Dokuments beinhaltet, das Sie als EB-Ausgabe generieren möchten.

![Das Layout der Word-Vorlage in der Desktop-Anwendung](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Ersetzen Sie die Excel-Vorlage durch die Word-Vorlage, und fügen Sie einen benutzerdefinierten XML-Teil hinzu

Aktuell wird das Excel-Dokument als Vorlage verwendet, um die Ausgabe im OPENXML-Format zu generieren. Ersetzen Sie diese Vorlage durch die Word-Vorlagendatei SampleVendPaymDocReport.docx, die Sie zuvor heruntergeladen haben. Sie erweitern die Word-Vorlage auch durch Hinzufügen eines benutzerdefinierten XML-Teils.

1. Wählen Sie in Finance auf der Seite **Format-Designer** auf der Registerkarte **Format** die Option **Anhänge** aus.
2. Auf der Seite **Anhänge** wählen Sie **Löschen** aus, um die vorhandene Excel-Vorlage zu entfernen. Wählen Sie **Ja** aus, um die Änderung zu bestätigen.
3. Wählen Sie **Neu** \> **Datei** aus.

    > [!NOTE]
    > Sie müssen einen Dokumenttyp auswählen, der in den EB-Parametern [konfiguriert wurde](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), um die Vorlagen von EB-Formatvorlagen zu speichern.

4. Wählen Sie **Durchsuchen** aus, und navigieren Sie dann zu der Datei **SampleVendPaymDocReport.docx**, die Sie zuvor heruntergeladen haben, und wählen Sie sie aus.
5. Wählen Sie **OK**.
6. Schließen Sie die Seite **Anhänge**.
7. Auf der Seite **Format-Designer** im Feld **Vorlage** geben Sie die Datei **SampleVendPaymDocReport.docx** ein oder wählen sie aus, um diese Word-Vorlage anstelle der zuvor verwendeten Excel-Vorlage zu verwenden.
8. Wählen Sie **Speichern** aus.

    Zusätzlich zum Speichern von Konfigurationsänderungen, wird durch die Aktivität **Speichern** auch die angehängte Word-Vorlage aktualisiert. Die hierarchische Struktur des entworfenen Formats wird dem zugeordneten Word-Dokument als neuer benutzerdefinierter XML-Abschnitt mit dem Namen **Bericht** angehängt. Die angefügte Word-Vorlage enthält das Layout des Dokuments, das als EB-Ausgabe generiert wird, und auch die Struktur von Daten, die EB in diese Vorlage zur Laufzeit eingibt.

9. Beachten Sie, dass der Titel des Stammformatelements angibt, dass derzeit eine Word-Vorlage verwendet wird.

    ![Ersetzen der Excel-Vorlage durch die Word-Vorlage und Hinzufügen eines benutzerdefinierten XML-Teils](../media/er-design-configuration-word-2016-11-image03.gif)

10. Auf der Registerkarte **Formate** wählen Sie **Anhänge** aus.

Sie können jetzt die Elemente des ausgewählten benutzerdefinierten XML-Teils **Bericht** den Inhaltssteuerelementen des Word-Dokuments zuordnen.

Wenn Sie mit dem Entwurf von Word-Dokumenten als Formulare vertraut sind, die [Inhaltssteuerelemente](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) enthalten, die den Elementen von [benutzerdefinierten XML-Teilen](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) zugeordnet sind, führen Sie alle Schritte in der nächsten Prozedur aus, um das Dokument zu erstellen. Weitere Informationen finden Sie unter [Erstellen von Formularen, die in Word ausgefüllt oder gedruckt werden können](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Überspringen Sie anderenfalls die nächste Prozedur.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Ein Word-Dokument mit einem benutzerdefinierten XML-Teil erstellen und eine Datenzuordnung durchführen

1. In Finance wählen Sie auf der Seite **Anhänge** die Option **Öffnen** aus, um die ausgewählte Vorlage von Finance herunterzuladen und lokal als Word-Dokument zu speichern.
3. Öffnen Sie in der Word-Desktopanwendung das gerade heruntergeladene Dokument.
4. Auf der Registerkarte **Entwickler** wählen Sie **XML-Zuordnungsbereich** aus.

    > [!NOTE]
    > Wenn die Registerkarte **Entwickler** nicht in der Menüleiste angezeigt wird, passen Sie die Menüleiste an, um sie hinzuzufügen.

5. Im Bereich **XML-Zuordnung** im Feld **Benutzerdefinierter XML-Teil** wählen Sie den benutzerdefinierten XML-Teil **Bericht** aus.
6. Sie können jetzt die Elemente des ausgewählten benutzerdefinierten XML-Teils **Bericht** und die Inhaltssteuerelemente des Word-Dokuments zuordnen.
7. Speichern Sie das aktualisierte Word-Dokument lokal unter **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Überprüfen der Word-Vorlage, in der der benutzerdefinierte XML-Teil Inhaltssteuerelementen zugeordnet ist

1. Öffnen Sie in der Word-Desktopanwendung die Vorlagendatei **SampleVendPaymDocReportBounded.docx**.
2. Stellen Sie sicher, dass diese Vorlage das Layout des Dokuments beinhaltet, das Sie als EB-Ausgabe generieren möchten. Die Inhaltssteuerelemente, die als Platzhalter für Daten verwendet werden, die EB zur Laufzeit in diese Vorlage eingibt, basieren auf den Zuordnungen, die zwischen Elementen des benutzerdefinierten XML-Teils **Bericht** und den Inhaltssteuerelemente des Word-Dokuments konfiguriert werden.

![Vorschau der Word-Vorlage in der Desktop-Anwendung](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Hochladen der Word-Vorlage, in der der benutzerdefinierte XML-Teil Inhaltssteuerelementen zugeordnet ist

1. Wählen Sie in Finance auf der Seite **Anhänge** die Option **Löschen** aus, um die Word-Vorlage zu entfernen, die keine Zuordnungen zwischen Elementen des benutzerdefinierten XML-Teils **Bericht** und Inhaltssteuerelementen enthält. Wählen Sie **Ja** aus, um die Änderung zu bestätigen.
2. Wählen Sie **Neu** \> **Datei** aus, um eine neue Vorlagendatei hinzuzufügen, die Zuordnungen zwischen Elementen des benutzerdefinierten XML-Teils **Bericht** und Inhaltssteuerelementen enthält.

    > [!NOTE]
    > Sie müssen einen Dokumenttyp auswählen, der in den EB-Parametern [konfiguriert wurde](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), um die Vorlagen von EB-Formatvorlagen zu speichern.

3. Wählen Sie **Durchsuchen** aus, und navigieren Sie dann zu der Datei **SampleVendPaymDocReportBounded.docx**, die Sie heruntergeladen oder vorbereitet haben, indem Sie den Vorgang im Abschnitt [Ein Word-Dokument mit einem benutzerdefinierten XML-Teil erstellen und eine Datenzuordnung durchführen](#get-word-doc) abgeschlossen haben, und wählen Sie sie aus.
4. Wählen Sie **OK**.
5. Schließen Sie die Seite **Anhänge**.
6. Auf der Seite **Format-Designer** im Feld **Vorlage** wählen Sie das Dokument aus, das Sie gerade heruntergeladen haben.
7. Wählen Sie **Speichern** aus.
8. Seite **Format-Designer** schließen.

## <a name="mark-the-configured-format-as-runnable"></a>Markieren des konfigurierten Formats als ausführbar

Um die Entwurfsversion des bearbeitbaren Formats auszuführen, müssen Sie sie [ausführbar](../er-quick-start2-customize-report.md#MarkFormatRunnable) machen.

1. In Finance wählen Sie auf der Seite **Konfigurationen** im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** die Option **Benutzerparameter** aus.
2. Legen Sie im Dialogfeld **Benutzerparameter** die Option **Testlaufeinstellungen** auf **Ja** fest und wählen Sie dann **OK** aus.
3. Wählen Sie **Bearbeiten** aus, um die aktuelle Seite bei Bedarf bearbeiten zu können.
4. Für die aktuell ausgewählte Konfiguration **Beispiel-Arbeitsblattbericht** setzen Sie die Option **Entwurf ausführen** auf **Ja**.
5. Wählen Sie **Speichern** aus.

## <a name="run-the-format-to-create-output-in-word-format"></a>Das Format ausführen, um eine Ausgabe im Word-Format zu erstellen

1. Wechseln Sie in Finance zu **Kreditorenkonten** \> **Zahlungen** \> **Zahlungserfassung**.
2. Wählen Sie in einer zuvor eingegebenen Zahlungserfassung die Option aus **Positionen** aus.
3. Auf der Seite **Kreditorenzahlungen** wählen Sie alle Zeilen im Raster aus.
4. Wählen Sie **Zahlungsstatus** \> **Keiner** aus.

    ![Zahlrungen zur Verarbeitung auf der Seite „Kreditorenzahlungen“](../media/er-design-configuration-word-2016-11-image05.png)

5. Wählen Sie im Aktivitätsbereich **Zahlungen generieren** aus.
6. Führen Sie im angezeigten Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.
    2. Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.
    3. Wählen Sie **OK**.

7. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **OK** aus.
8. Die erstellte Ausgabe wird im Word-Format dargestellt und enthält die Details der verarbeiteten Zahlungen. Analysieren Sie das generierte Ergebnis.

    ![Generierte Ausgabe im Word-Format](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Eine neue EB-Konfiguration zum Generieren von Berichten im Word-Format erstellen](../er-design-configuration-word.md)
- [Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von ER](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]