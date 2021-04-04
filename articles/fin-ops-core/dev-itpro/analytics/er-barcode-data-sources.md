---
title: Verwenden Sie Barcode-Datenquellen, um Barcode-Bilder zu generieren
description: In diesem Thema wird erläutert, wie Sie Barcode-Datenquellen zum Generieren von Barcode-Bildern verwenden.
author: NickSelin
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: bf71caf2ff14fb815999e63d6b7ee91afccbdd1b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563678"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Verwenden Sie Barcode-Datenquellen, um Barcode-Bilder zu generieren

[!include[banner](../includes/banner.md)]

Sie können das [Elektronische Berichterstattung (ER)](general-electronic-reporting.md) Framework nutzen, um [Komponenten im ER-Format](general-electronic-reporting.md#FormatComponentOutbound) zu entwerfen, die Sie ausführen können, um elektronische und druckbare ausgehende Dokumente zu generieren, die Sie benötigen. So generieren Sie ein ausgehendes Dokument im Microsoft Office Format; Sie müssen das Layout des Berichts angeben, indem Sie entweder ein Microsoft Excel Dokument oder ein Microsoft Word Dokument als Berichtsvorlage verwenden. Mit dem [EB-Vorgangs-Designer](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) können Sie ein Excel- oder Word-Dokument als Vorlage für ein EB-Format anhängen. Die folgenden benannten Elemente in der angehängten Vorlage sind den Elementen der konfigurierten Formatkomponente zugeordnet:

- Inhaltssteuerelemente in Word
- Benannte Blätter, Bereiche, Zellen, Formen und Bilder in Excel

Diese benannten Elemente werden als Platzhalter für Daten verwendet, die in ein generiertes Dokument eingegeben werden, wenn ein EB-Format ausgeführt wird. Zuweisen von EB-Formatkomponenten zu Datenquellen. Diese Datenquellen geben die Daten an, die zur Laufzeit in die generierten Dokumente eingegeben werden. Weitere Informationen erhalten Sie unter [Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von EB](electronic-reporting-embed-images-shapes.md).

EB unterstützt jetzt den **Barcode** Datenquellentyp. Daher können Sie jetzt ein Bild generieren, das den Barcode für den angegebenen Text darstellt. Wenn Sie ein EB-Format konfigurieren, können Sie Datenquellen des **Barcodes** angeben; tippen Sie, um Barcode-Bilder zu generieren. Sie können diese Bilder dann generierten Geschäftsdokumenten wie Bestellungen, Rechnungen, Packzetteln und Belegen hinzufügen. Sie können sie auch verschiedenen Arten von Etiketten hinzufügen, z. B. Produkt- und Regaletiketten sowie Verpackungs- und Versandetiketten.

Die folgenden Platzhalter können in Berichtsvorlagen zur Eingabe von Barcode-Bildern verwendet werden:

- [Bild](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) Inhaltskontrolle für Word
- [Bild](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) Objekt in Excel

Durch die Verwendung einer Datenquelle des **Barcode** Typs können Sie Barcodes in den folgenden Formaten generieren:

- Eindimensionale Barcodes:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Intelligent Mail
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Zweidimensionale Barcodes:

    - Aztec
    - Data Matrix
    - QR-Code

Wenn Sie eine **Barcode** Datenquelle konfigurieren, können Sie bestimmte Rendering-Parameter definieren, die zum Generieren eines Bildes verwendet werden:

- **Breite** – Geben Sie die Breite des Barcodes in Pixel an. Ein Wert von **0** (Null) gibt an, dass die Standardbreite verwendet wird. Die Bedeutung kann für verschiedene Formate variieren.
- **Höhe** – Geben Sie die Höhe des Barcodes in Pixel an. Ein Wert von **0** (Null) gibt an, dass die Standardhöhe verwendet wird. Die Bedeutung kann für verschiedene Formate variieren.
- **Rand** – Geben Sie die Größe des Barcode-Randes in Pixel an. Der Rand ist der Bereich auf jeder Seite eines Strichcodes, der frei gehalten werden muss (Ruhezone). Ein Wert von **0** (Null) gibt an, dass der Standardrand verwendet wird. Die Bedeutung kann für verschiedene Formate variieren.
- **Inhalt ausgeben** – Stellen Sie den Wert auf **Ja** um ein Barcode-Bild zu generieren, das die codierten Informationen als Text enthält. Standardwert ist **Keiner**.
- **Codierung** – Geben Sie die Art der Zeichen an, die im generierten Barcode-Bild codiert sind. Standardmäßig wird die **UTF-8** Codierung verwendet.

> [!IMPORTANT]
> Wenn Sie eine neue **Barcode** Datenquelle hinzufügen, müssen Sie sie als verschachteltes Element unter einem anderen Element (Container) platzieren.
>
> Wenn Sie eine **Barcode** Datenquelle an ein Zellenelement in einem Format binden, und das Zellenelement repräsentiert entweder ein Word-Inhaltssteuerelement oder ein Excel-Bild, wird die Datenquelle in dieser Bindung als eine Funktion dargestellt, die einen einzelnen Parameter des **Zeichenfolgentyps** hat. Mit diesem Parameter müssen Sie den Text angeben, der in ein Barcode-Bild umgewandelt und beim Scannen eines generierten Barcodes gelesen werden soll.

Weitere Informationen zu dieser Funktion erhalten Sie, wenn Sie das Beispiel in diesem Thema abschließen.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Beispiel: Generieren Sie einen Zahlungsscheck, der einen Barcode enthält, der den zu zahlenden Betrag codiert

Dieses Beispiel zeigt, wie ein Benutzer in der Rolle **Systemadministrator** oder **Funktionsberater für elektronische Berichterstattung** ein EB-Format konfigurieren kann, das eine Vorlage enthält, mit der ein ausgehendes Dokument im Excel-Format generiert wird, das einen Barcode enthält. Hier finden Sie eine Übersicht über die beteiligten Schritte.

1. [Vervollständigen Sie die Voraussetzungen](#ExamplePrerequisites).
2. [Aktivieren eines Konfigurationsanbieters](#ExampleProvider).
3. [Überprüfen der bereitgestellten EB-Lösung](#ExampleImportSolution).
4. [Zahlungsscheck generieren](#ExampleGenerateCheque).
5. [Prüfen sie den generierten Zahlungscheck](#ExampleReviewGeneratedCheque).
6. [Ändern Sie das Format der bereitgestellten EB-Lösung](#ExampleModifyFormat).

    1. [Wenden Sie eine neue Scheckvorlage an](#ExampleModifyFormatApplyTemplate).
    2. [Hinzufügen einer neuen Barcode-Datenquelle](#ExampleModifyFormatAddDataSource).
    3. [Binden Sie ein neues Formatelement](#ExampleModifyFormatBindFormatElement).
    4. [Stellen Sie die geänderte Version für Testläufe zur Verfügung](#ExampleModifyFormatMakeVersionAvailable).

        1. [Vervollständigen Sie die geänderte Formatversion](#CompleteToRun).
        2. [Stellen Sie die Entwurfsversion zur Verwendung bereit](#MarkToRun).

7. [Zahlungsscheck generieren](#ExampleGenerateCheque2).
8. [Konvertieren Sie den generierten Scheck in ein PDF](#ExampleConvertToPDF).

In diesem Beispiel verwenden Sie die bereitgestellte EB-Lösung, die zum Generieren von Zahlungsschecks konfiguriert wurde. Diese Lösung generiert Zahlungsschecks, bei denen der zu zahlende Betrag sowohl als Zahl als auch als Text geschrieben wird. Sie werden diese EB-Lösung so ändern, dass der Scheck auch einen generierten Barcode enthält, in dem der zu zahlende Betrag verschlüsselt ist und mit einem Barcode-Scanner gelesen werden kann.

Diese Schritte können im **USMF**-Unternehmen in Microsoft Dynamics 365 Finance abgeschlossen werden.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Vervollständigen Sie die Voraussetzungen

Um das Beispiel in diesem Thema abzuschließen, müssen Sie für eine der folgenden Rollen Zugriff auf das USMF-Unternehmen in Finance haben:

- Funktionaler Berater für elektronische Berichterstellung
- Systemadministrator

Wenn Sie das Beispiel im Thema [Einbetten von Bildern und Formen in Dokumenten, die Sie mithilfe von EB generiert haben](electronic-reporting-embed-images-shapes.md) nocht nicht abgeschlossen haben, laden Sie die folgende Konfiguration in der Beispiel-EB-Lösung herunter.

| Inhaltsbeschreibung         | Dateiname                   |
|-----------------------------|-----------------------------|
| ER-Datenmodell-Konfiguration | Modell für cheques.xml       |
| ER-Formatkonfiguration     | Überprüft das Drucken von Format.xml |

Laden Sie außerdem die folgende Excel-Datei herunter, die die geänderte Vorlage für die bereitgestellte EB-Lösung enthält.

| Inhaltsbeschreibung | Dateiname                 |
|---------------------|---------------------------|
| Berichtsvorlage     | Überprüfen Sie die Vorlage Excel.xlsx |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Aktivieren eines Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Überprüfen Sie auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationsanbieter**, ob der [Konfigurationsanbieter](general-electronic-reporting.md#Provider) für das Beispielunternehmen **Litware, Inc.** aufgeführt und als Aktiv markiert ist. Wenn dieser Konfigurationsanbieter nicht aufgeführt oder nicht als Aktiv markiert ist, befolgen Sie die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Einstellungen der Beispielfirma auf aktiv setzen auf der Seite „Lokalisierungskonfigurationen“](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Überprüfen der bereitgestellten EB-Lösung

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Wenn auf der Seite **Konfigurationen** die Konfiguration für **Model zum Erlernen verzögerter Elemente** nicht im Konfigurationsbaum verfügbar ist, importieren Sie die EB-Datenmodellkonfiguration.

    1. Wählen Sie im Aktivitätsbereich **Austausch** \> **Aus XML-Datei laden** aus.
    2. Wählen Sie im Dialogfeld **Durchsuchen** aus, um die Datei **Modell für cheques.xml** zu finden und auszuwählen und klicken Sie dann auf **OK**.

4. Wenn auf der Seite Konfigurationen die Konfiguration für **Scheckdruckformat** nicht verfügbar ist, folgen Sie diesen Schritten, um die EB-Format-Konfiguration zu importieren:

    1. Wählen Sie im Aktivitätsbereich **Austausch** \> **Aus XML-Datei laden** aus.
    2. Wählen Sie im Dialogfeld **Durchsuchen** und wählen Sie die Datei **Scheckdruckformat.xml** und wählen Sie **OK**.

5. Erweitern Sie im Konfigurationsbaum **Modell für Schecks**.
6. Überprüfen Sie die Liste der importierten ER-Konfigurationen in der Konfigurationsstruktur.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Zahlungsscheck generieren

1. Gehen Sie zu **Bargeld- und Bankverwaltung** \> **Bankkonten** \> **Bankkonten**.
2. Auf der Seite **Bankkonten** wählen Sie das **USMF OPER** Konto.
3. Auf der Seite Bankkontodetails im Aktivitätsbereich auf der Registerkarte **Einrichten** in der Gruppe **Layout** wählen Sie **Scheck**.
4. Wählen Sie auf der Seite **Scheck-Layout** **Bearbeiten** aus.
5. Legen Sie im Inforegister **Allgemein** die Option **Generisches elektronisches Exportformat** auf **Ja** fest.
6. In dem Feld **Formatkonfiguration exportieren** wählen Sie das EB-Format **Überprüft das Druckformat**, das Sie zuvor importiert haben.
7. Klicken Sie im Aktivitätsbereich auf **Drucktest**.
8. Stellen Sie im Dialogfeld die Option **Verhandelbares Scheckformat** auf **Ja** und wählen dann **OK**.

    ![Überprüfen Sie das Dialogfeld Layout – Drucktest](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Prüfen Sie den generierten Zahlungscheck

- Öffnen Sie den generierten Scheck in Excel.
2. Generierten Scheck überprüfen.

    ![Öffnen Sie den generierten Scheck in Excel](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Ändern Sie das Format der bereitgestellten EB-Lösung

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Wenden Sie eine neue Scheckvorlage an

Sie können die Excel-Desktopanwendung verwenden, um die Datei **Scheck-Vorlage Excel.xlsx** zu öffnen, die Sie zuvor importiert haben. Beachten Sie, dass sich diese Vorlage von der Vorlage unterscheidet, mit der Sie in der bereitgestellten EB-Lösung einen Zahlungsscheck erstellt haben. Darüber hinaus enthält es ein Element **AmountBarcode** für das Barcode-Bild.

![AmountBarcode-Element in der Excel-Vorlage](./media/er-barcode-data-source-cheque2.png)

Sie müssen jetzt die EB-Lösung ändern und dann die geänderte Vorlage [erneut anwenden](modify-electronic-reporting-format-reapply-excel-template.md).

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen**.
3. Auf der Seite **Konfigurationen** im Konfigurationsbaum erweitern Sie **Modell für Scheck** und wählen **Überprüft das Druckformat**.
4. Wählen Sie im Aktivitätsbereich **Designer** aus.
5. Wählen Sie im EB Vorgangs-Designer die Registerkarte **Zuordnung**. Wählen Sie die Registerkarte auf der rechten Seite der Seite aus, und wählen Sie dann im Formatbaumbereich auf der linken Seite die Option **Aufklappen/reduzieren**.
6. Beachten Sie, dass alle Zellenformatelemente an die entsprechenden Datenquellen gebunden sind.

    ![Binden von Zellenformatelementen an Datenquellen im EB Vorgangs-Designer](./media/er-barcode-data-source-cells-bound.png)

7. Wählen Sie die Registerkarte **Format** auf der rechten Seite.
8. Wählen Sie im Aktionsbereich die Auslassungspunkte aus (**...**) und wählen Sie dann **Importieren**.
9. In der Gruppe **Importieren** wählen Sie **Aus Excel aktualisieren** und dann **Vorlage aktualisieren**.
10. Navigieren Sie im Dialogfeld zu **Überprüfen Sie die Vorlage Excel.xlsx** Datei, die auf Ihrem Computer gespeichert ist, wählen Sie sie aus und wählen Sie dann **OK** um zu bestätigen, dass die ausgewählte Vorlage angewendet werden soll.
11. Wählen Sie im EB Vorgangs-Designer die Registerkarte **Zuordnung**, wählen Sie die Registerkarte auf der rechten Seite der Seite aus, und wählen Sie dann im Formatbaumbereich auf der linken Seite die Option **Aufklappen/reduzieren**.
12. Beachten Sie, dass das **AmountBarcode** Zellenelement dem Format hinzugefügt wurde. Dieses Element ist dem Element **AmountBarcode** zugeordnet, das der geänderten Excel-Vorlage als Platzhalter für ein Barcode-Bild hinzugefügt wurde.

    ![AmountBarcode-Zellenelement, das dem Format im EB Vorgangs-Designer hinzugefügt wurde](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Hinzufügen einer neuen Barcode-Datenquelle

Als nächstes müssen Sie eine neue Datenquelle des Typs **Barcode** hinzufügen.

1. Im EB Vorgangs-Designer auf der Registerkarte **Zuordnung** wählen Sie auf der rechten Seite der Seite die Datenquelle **drucken** aus.
2. Wählen Sie **Hinzufügen** und dann in der Gruppe **Funktionen** wählen Sie den Datenquellentyp **Barcode**.

    ![Auswahl des Barcode-Datenquellentyps](./media/er-barcode-data-source-add.png)

3. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** den **Barcode** ein.
4. Wählen Sie im **Barcode-Format** **Code 128** aus.
5. Geben Sie im Feld **Breite** den Wert **500** ein.
6. Wählen Sie **OK**.

    ![Dialogfeld „Datenquelleneigenschaften“](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Binden Sie ein neues Formatelement

Als Nächstes müssen Sie das neue Formatelement an die gerade hinzugefügte Datenquelle binden.

1. Im EB Vorgangs-Designer auf der Registerkarte **Zuordnung** wählen Sie auf der rechten Seite der Seite die Datenquelle **drucken\\Barcode** aus.
2. Wählen Sie im Formatbaumbereich links die Option **AmountBarcode** Zellenelement, und wählen Sie dann **Binden**.
3. Wählen Sie im Aktivitätsbereich **Details anzeigen** aus.
4. Beachten Sie, dass, weil die **Barcode** Datenquelle in der Bindung als eine Funktion dargestellt wird, die einen einzelnen Parameter enthält, der Name des gebundenen Formatelements automatisch als Argument für diesen Parameter verwendet wird.

    ![Details zur Barcode-Datenquelle im EB Vorgangs-Designer](./media/er-barcode-data-source-bind1.png)

5. Wählen Sie **Formel bearbeiten**, um die Bindung anzupassen.

    Sie möchten nicht, dass der Name des Zellenelements zurückgegeben wird. Daher müssen Sie einen Ausdruck konfigurieren, der Text zurückgibt, der den zu zahlenden Betrag des aktuellen Schecks enthält. Weil der übergeordnete Bereich **ChequeLines** an die Datenquelle **model.cheques** gebunden ist, ist der zu zahlende Betrag des aktuellen Schecks im Feld **model.cheques.attributes.amount** des Datentyps **Echt** verfügbar.

6. Im Feld **Formel** geben Sie **print.barcode (NUMBERFORMAT(@.attributes.amount, „F2“))** ein.
7. Schließen Sie die Seite **EB Formulardesigner** und wählen Sie [Speichern](general-electronic-reporting-formula-designer.md) aus.
8. Beachten Sie, dass die Bindung angepasst wurde.

    ![Angepasste Bindung im EB Vorgangs-Designer](./media/er-barcode-data-source-bind2.png)

9. Schließen Sie die Seite EB Vorgangsdesigner und wählen Sie **Speichern** aus.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Stellen Sie die geänderte Version für Testläufe zur Verfügung

Standardmäßig sind dies die einzigen Versionen mit dem Status **Abgeschlossen** und **Geteilt**, die verwendet werden, wenn Sie ein EB-Format ausführen.

Wenn Sie Ihre Änderungen abgeschlossen haben, können Sie Ihre Arbeit mit der aktuellen Entwurfsversion abschließen und Ihre Änderungen zur Verwendung bereitstellen. Anweisungen finden Sie im Abschnitt [Vervollständigen Sie die geänderte Formatversion](#CompleteToRun).

Wenn Sie weiterhin mit der aktuellen Entwurfsversion arbeiten möchten, diese jedoch zum Generieren von Überprüfungen verwenden müssen, müssen Sie explizit angeben, dass Sie die Entwurfsversion des Formats für die Ausführung verwenden möchten. Anweisungen finden Sie im Abschnitt [Stellen Sie die Entwurfsversion zur Verwendung bereit](#MarkToRun).

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Vervollständigen Sie die geänderte Formatversion

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen**.
3. Auf der Seite **Konfigurationen** im Konfigurationsbaum erweitern Sie **Modell für Scheck** und wählen **Überprüft das Druckformat**.
4. Wählen Sie im Inforegister **Versionen**, wählen Sie den Datensatz mit dem Status **Entwurf** aus.
5. Wählen Sie **Status ändern** und dann **Abgeschlossen**.
6. Klicken Sie im Dialogfeld auf **OK**.

Der Status der aktuellen Version wird von **Entwurf** zu **Abgeschlossen** geändert und eine neue Version mit dem Status **Entwurf** wird geschaffen. Mit dieser neuen Entwurfsversion können Sie zusätzliche Änderungen anwenden.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Stellen Sie die Entwurfsversion zur Verwendung bereit

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen**.
3. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
4. Stellen Sie im Dialogfeld die Option **Einstellungen ausführen** auf **Ja** und wählen dann **OK**.
5. Auf der Seite Konfigurationen im Konfigurationsbaum erweitern Sie **Modell für Scheck** und wählen **Scheckdruckformat** aus.
6. Legen Sie die Option **Entwurf ausführen** auf **Ja** fest.
7. Wählen Sie **Speichern** aus.

Die Entwurfsversion des ausgewählten Formats wird als verfügbar markiert, wenn das ausgewählte Format ausgeführt wird.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Zahlungsscheck generieren

1. Gehen Sie zu **Bargeld- und Bankverwaltung** \> **Bankkonten** \> **Bankkonten**.
2. Auf der Seite **Bankkonten** wählen Sie das **USMF OPER** Konto.
3. Auf der Seite Bankkontodetails im Aktivitätsbereich auf der Registerkarte **Einrichten** in der Gruppe **Layout** wählen Sie **Scheck**.
4. Auf der Seite **Überprüfen Sie das Layout** wählen Sie im Aktionsbereich die Option **Test drucken**.
5. Stellen Sie im Dialogfeld die Option **Verhandelbares Scheckformat** auf **Ja** und wählen dann OK.
6. Wählen Sie **OK**.
7. Generierten Scheck überprüfen. Beachten Sie, dass ein Barcode generiert wurde, um den zu zahlenden Betrag des Schecks zu codieren.

    ![Generierter Zahlungsscheck mit Barcode in Excel](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Eine Ausnahme wird ausgelöst, wenn das Argument von einer **Barcode** Datenquelle nicht den entsprechenden Anforderungen entspricht, die für das Barcode-Format spezifisch sind. Zum Beispiel, wenn die **Barcode** Datenquelle aufgerufen wird, um einen Barcode [EAN-8](https://wikipedia.org/wiki/EAN-8) für den bereitgestellten Text zu erstellen, wird eine Ausnahme ausgelöst, wenn die Länge des Textes sieben Zeichen überschreitet.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Konvertieren Sie den generierten Scheck in ein PDF

Wie im Thema [Generieren Sie druckbare FTI-Formulare](er-generate-printable-fti-forms.md#finland) beschrieben können Sie eine spezielle Schriftart verwenden, um Barcodes in einem generierten Dokument zu erstellen. In diesem Fall hängen zusätzliche Transformationen des generierten Dokuments möglicherweise von der Verfügbarkeit dieser Schriftart in der Transformationsumgebung ab. Wenn Sie beispielsweise versuchen, ein Dokument in das PDF-Format zu konvertieren oder eine Vorschau in einer Umgebung anzuzeigen, in der die Schriftart fehlt, werden Barcodes nicht korrekt gerendert.

Wenn Sie jedoch die Datenquelle **Barcode** verwenden, um Barcodes zu erstellen, hängt das Rendern dieser Barcodes von keiner Schriftart ab. Daher können Sie Dokumente, die Barcodes enthalten, problemlos in das PDF-Format konvertieren. Die folgende Abbildung zeigt die Vorschau eines generierten Zahlungsschecks [umgewandelt](electronic-reporting-destinations.md#OutputConversionToPDF) zu einem PDF, basierend auf der Einstellung der konfigurierten EB [Ziel](electronic-reporting-destinations.md).

![Vorschau des PDF eines Zahlungsschecks](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Einschränkungen

> [!NOTE]
> Einige Arten von Barcodes, die generiert werden, haben ein festes Seitenverhältnis. Dieses Verhalten ist sinnvoll, wenn Sie die Funktion **Aktivieren Sie die Verwendung der EPPlus-Bibliothek im Rahmen für elektronische Berichte** zum Arbeiten mit Excel-Dokumenten in EB aktiviert haben. In diesem Fall wird ein Bild in einen Platzhalter mit einem gesperrten Seitenverhältnis eingegeben. Wenn daher die Abmessungen eines Platzhalters in einer Vorlage dem Verhältnis eines eingegebenen Bildes entsprechen, kann die Größe eines realen Bilds in einem generierten Dokument geändert werden, um das erforderliche Seitenverhältnis beizubehalten. Verwenden Sie einen Platzhalter mit einem erwarteten Seitenverhältnis, um die Größenänderung von Bildern zu verhindern.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Zielorte für die elektronische Berichterstellung](electronic-reporting-destinations.md)
- [Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)
- [NUMBERFORMAT Funktion](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]