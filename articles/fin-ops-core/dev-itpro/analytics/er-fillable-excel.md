---
title: Eine Konfiguration zur Generierung von Dokumenten im Excel-Format entwerfen
description: Dieses Thema enthält Informationen zum Entwerfen eines Formats für die elektronische Berichterstellung (EB), um eine Excel-Vorlage auszufüllen und ausgehende Dokumente im Excel-Format zu generieren.
author: NickSelin
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c8d939fef4fd0f9e189ca37318c2c0306511785
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893907"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Eine Konfiguration zur Generierung von Dokumenten im Excel-Format entwerfen

[!include[banner](../includes/banner.md)]

Sie können eine Formatkonfiguration für die [elektronische Berichtersterstellung (EB)](general-electronic-reporting.md) mit einer EB-[Formatkomponente](general-electronic-reporting.md#FormatComponentOutbound) entwerfen, die Sie konfigurieren können, um ein ausgehendes Dokument in einem Microsoft Excel-Arbeitsmappenformat zu generieren. Zu diesem Zweck müssen bestimmte Komponenten des EB-Formats verwendet werden.

Führen Sie die folgenden Schritte im Thema [Konfiguration zum Generieren von Berichten im OPENXML-Format entwerfen](tasks/er-design-reports-openxml-2016-11.md) aus, um weitere Informationen zu dieser Funktion zu erhalten.

## <a name="add-a-new-er-format"></a>Neues ER-Format hinzufügen

Wenn Sie eine neue EB-Formatkonfiguration hinzufügen, um ein ausgehendes Dokument in einem Excel-Arbeitsmappenformat zu generieren, müssen Sie den **Excel**-Wert das Attribut **Formattyp** des Formats auswählen oder das Attribut **Formattyp** leer lassen.

- Wenn Sie **Excel** auswählen, können Sie das Format so konfigurieren, dass ein ausgehendes Dokument nur im Excel-Format generiert wird.
- Wenn Sie das Attribut leer lassen, können Sie das Format so konfigurieren, dass ein ausgehendes Dokument in einem beliebigen Format generiert wird, das vom EB-Framework unterstützt wird.

Wählen Sie im Aktionsbereich **Designer** aus, und öffnen Sie die EB-Formatkomponente zur Bearbeitung im EB-Vorgangs-Designer aus, um die EB-Formatkomponente der Konfiguration zu konfigurieren.

![Konfigurationsseite](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Komponente „Excel-Datei“

### <a name="manual-entry"></a>Manuelle Eingabe

Sie müssen dem konfigurierten EB-Format eine **Excel\\Datei-Komponente** hinzufügen, um ein ausgehendes Dokument im Excel-Format zu generieren.

![Komponente „Excel\Datei“](./media/er-excel-format-add-file-component.png)

Hängen Sie eine Excel-Arbeitsmappe mit der .xlsx-Erweiterung als Vorlage für ausgehende Dokumente an die **Excel\\Datei**-Komponente an, um das Layout des ausgehenden Dokuments festzulegen.

> [!NOTE]
> Wenn Sie eine Vorlage manuell anhängen, müssen Sie einen [Dokumententyp](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) verwenden, der zu diesem Zweck im [EB-Parameter ](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) konfiguriert wurde.

![Hinzufügen eines Anhangs zur Excel\Datei-Komponente](./media/er-excel-format-add-file-component2.png)

Wenn Sie das konfigurierte ER-Format ausführen, müssen Sie der **Excel\\Datei**-Komponente die Komponenten **Blatt**-, **Angebot** und **Zelle** hinzufügen, um festzulegen, wie die angehängte Vorlage ausgefüllt wird. Jede verschachtelte Komponente muss mit einem Excel-benannten Element verknüpft sein.

### <a name="template-import"></a>Vorlagenimport

Sie können auf der Registerkarte **Importieren** des Aktionsbereichs die Option **Aus Excel importieren** auswählen, um eine neue Vorlage in ein leeres EB-Format zu importieren. In diesem Beispiel wird automatisch eine **Excel\\Datei**-Komponente erstellt und die importierte Vorlage daran angehängt. Alle erforderlichen EB-Komponenten werden ebenfalls automatisch erstellt, basierend auf der Liste der erkannten Excel-benannten Elemente.

![Auswählen von „Aus Excel importieren“](./media/er-excel-format-import-template.png)

> [!NOTE]
> Wenn Sie das optionale **Blatt**-Element im bearbeitbaren EB-Format erstellen möchten, legen Sie die Option **Excel-Arbeitsblattformat-Element erstellen** auf **Ja** fest.

## <a name="sheet-component"></a>Komponente „Blatt“

Die **Blatt**-Komponente gibt ein Arbeitsblatt der angehängten Excel-Arbeitsmappe an, das ausgefüllt werden muss. Der Name des Arbeitsblatts in einer Excel-Vorlage ist in der **Blatt**-Eigenschaft dieser Komponente definiert.

> [!NOTE]
> Diese Komponente ist für Excel-Arbeitsmappen, die ein einzelnes Arbeitsblatt enthalten, optional.

Auf der Registerkarte **Zuordnung** des EB-Vorgangs-Designers können Sie die Eigenschaft **Aktiviert** für eine **Blatt**-Komponente konfigurieren, um anzugeben, ob die Komponente in ein generiertes Dokument eingefügt werden muss:

- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Wahr** zur Laufzeit oder wenn überhaupt kein Ausdruck konfiguriert ist, wird das entsprechende Arbeitsblatt im generierten Dokument ausgefüllt.
- Wenn ein Ausdruck der Eigenschaft **Aktiviert** ist für die Rückgabe von **Falsch** zur Laufzeit konfiguriert ist, enthält das generierte Dokument kein Arbeitsblatt.

![Beispiel einer Blatt-Komponente](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Komponente „Bereich“

Die Komponente **Bereich** gibt einen Excel-Bereich an, der von dieser EB-Komponente gesteuert werden muss. Der Name des Bereichs ist in der Eigenschaft **Excel-Bereich** dieser Komponente definiert.

Die Eigenschaft **Replikationsrichtung** gibt an, ob und wie der Bereich in einem generierten Dokument wiederholt wird:

- Wenn die Eigenschaft **Replikationsrichtung** auf **Keine Replikation** festgelegt ist, wird der entsprechende Excel-Bereich nicht im generierten Dokument wiederholt.
- Wenn die Eigenschaft **Replikationsrichtung** auf **Vertikal** festgelegt ist, wird der entsprechende Excel-Bereich im generierten Dokument wiederholt. Jeder replizierte Bereich wird in einer Excel-Vorlage unter den ursprünglichen Bereich eingefügt. Die Anzahl der Wiederholungen wird durch die Anzahl der Datensätze in einer Datenquelle des Typs **Datensatzliste** definiert, der an diese EB-Komponente gebunden ist.
- Wenn die Eigenschaft **Replikationsrichtung** auf **Horizontal** festgelegt ist, wird der entsprechende Excel-Bereich im generierten Dokument wiederholt. Jeder replizierte Bereich wird in einer Excel-Vorlage rechts neben dem ursprünglichen Bereich eingefügt. Die Anzahl der Wiederholungen wird durch die Anzahl der Datensätze in einer Datenquelle des Typs **Datensatzliste** definiert, der an diese EB-Komponente gebunden ist.

Führen Sie die Schritte unter [Horizontal erweiterbare Bereiche verwenden, um Spalten in Excel-Berichten dynamisch hinzuzufügen](tasks/er-horizontal-1.md) aus, um weitere Informationen zu erhalten.

Die Komponente **Bereich** kann andere verschachtelte EB-Komponenten aufweisen, die zur Eingabe von Werten in die entsprechenden benannten Excel-Bereiche verwendet werden.

- Wenn eine Komponente der Gruppe **Text** für die Eingabe von Werten verwendet wird, erfolgt die Eingabe des Werts in einem Excel-Bereich als Textwert.

    > [!NOTE]
    > Verwenden Sie dieses Muster, um eingegebene Werte basierend auf dem in der Anwendung definierten Gebietsschema zu formatieren.

- Wenn die Komponente **Zelle** der Gruppe **Excel** verwendet wird, um Werte einzugeben, wird der Wert in einem Excel-Bereich als Wert des Datentyps eingegeben, der durch die Bindung dieser Komponente **Zelle** (z. B. **Zeichenfolge**, **Gleitkommazahl**, oder **Ganzzahl**) definiert ist.

    > [!NOTE]
    > Verwenden Sie dieses Muster, damit die Excel-Anwendung eingegebene Werte basierend auf dem Gebietsschema des lokalen Computers formatieren kann, der das ausgehende Dokument öffnet.

Auf der Registerkarte **Zuordnung** des EB-Vorgangs-Designers können Sie die Eigenschaft **Aktiviert** für eine **Bereich**-Komponente konfigurieren, um anzugeben, ob die Komponente in ein generiertes Dokument eingefügt werden muss:

- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Wahr** zur Laufzeit oder wenn überhaupt kein Ausdruck konfiguriert ist, wird der entsprechende Bereich im generierten Dokument ausgefüllt.
- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Falsch** zur Laufzeit konfiguriert ist und dieser Bereich nicht sämtliche Zeilen oder Spalten darstellt, wird der entsprechende Bereich nicht im generierten Dokument ausgefüllt.
- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Falsch** zur Laufzeit konfiguriert ist und dieser Bereich sämtliche Zeilen oder Spalten darstellt, enthält das Dokument diese Zeilen und Spalten als ausgeblendete Zeilen und Spalten.

## <a name="cell-component"></a>Komponente „Zelle“

Die Komponente **Zelle** wird verwendet, um Excel-benannte Zellen, Formen und Bilder auszufüllen. Wenn Sie ein Excel-benannte Objekt, das von einer EB-Komponente vom Typ **Zelle** ausgefüllt werden muss, angeben möchten, müssen Sie den Namen dieses Objekts in der Eigenschaft **Excel-Bereich** der Komponente **Zelle** festlegen.

Auf der Registerkarte **Zuordnung** des EB-Vorgangs-Designers können Sie die Eigenschaft **Aktiviert** für eine **Bereich**-Komponente konfigurieren, um festzulegen, ob das Objekt in einem generierten Dokument ausgefüllt werden muss:

- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Wahr** zur Laufzeit oder wenn überhaupt kein Ausdruck konfiguriert ist, wird das entsprechende Objekt im generierten Dokument ausgefüllt. Die Bindung dieser Komponente vom Typ **Zelle** gibt einen Wert an, der in das entsprechende Objekt eingefügt wird.
- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Falsch** zur Laufzeit konfiguriert ist, wird das entsprechende Objekt nicht im generierten Dokument ausgefüllt.

Wenn eine Komponente vom Typ **Zelle** für die Eingabe eines Werts in eine Zelle konfiguriert ist, kann sie an eine Datenquelle gebunden werden, die den Wert eines primitiven Datentyps zurückgibt (z. B. **Zeichenfolge**, **Gleitkommazahl** oder **Ganzzahl**). In diesem Fall wird der Wert als Wert desselben Datentyps in die Zelle eingegeben.

Wenn eine Komponente vom Typ **Zelle** für die Eingabe eines Werts in ein Excel-Shape konfiguriert ist, kann sie an eine Datenquelle gebunden werden, die einen Wert eines primitiven Datentyps zurückgibt (z. B. **Zeichenfolge**, **Gleitkommazahl** oder **Ganzzahl**). In diesem Fall wird der Wert als Text dieses Shapes in das Excel-Shape eingegeben. Für Werte von anderen Datentypen als **Zeichenfolge** erfolgt die Konvertierung in Text automatisch.

> [!NOTE]
> Sie können eine Komponente vom Typ **Zelle** so konfigurieren, dass ein Shape nur in den Fällen ausgefüllt wird, in denen eine Shape-Text-Eigenschaft unterstützt wird.

Wenn eine Komponente vom Typ **Zelle** für die Eingabe eines Werts in ein Excel-Bild konfiguriert ist, kann sie an eine Datenquelle gebunden werden, die einen Wert des Datentyps **Container** zurückgibt, der ein Bild im Binärformat darstellt. In diesem Fall wird der Wert als Bild in das Excel-Bild eingegeben.

> [!NOTE]
> Jedes Excel-Bild und -Shape gilt als durch die obere linke Ecke in einer bestimmten Excel-Zelle oder einem bestimmten Excel-Bereich verankert. Wenn Sie ein Excel-Bild oder Excel-Shape replizieren möchten, müssen Sie die Zelle oder den Bereich, in dem es verankert ist, als replizierte Zelle oder Bereich konfigurieren.

Weitere Informationen zum Einbetten von Bildern und Shapes finden Sie unter [Bilder und Shapes in Dokumente einbetten, die mit EB generiert werden](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Komponente „Seitenumbruch“

Die Komponente **PageBreak** erzwingt das Starten einer neuen Seite in Excel. Diese Komponente ist nicht erforderlich, wenn Sie das Standard-Paging von Excel verwenden möchten, aber Sie sollten sie verwenden, wenn Sie möchten, dass Excel Ihrem ER-Format folgt, um das Paging zu strukturieren.

## <a name="footer-component"></a>Fußzeilenkomponente

Die **Fußzeile**-Komponente wird verwendet, um Fußzeilen am unteren Rand eines generierten Arbeitsblatts in einer Excel-Arbeitsmappe auszufüllen.

> [!NOTE]
> Sie können diese Komponente für jede **Blatt**-Komponente zum Angeben verschiedener Fußzeilen für verschiedene Arbeitsblätter in einer generierten Excel-Arbeitsmappe hinzufügen.

Wenn Sie eine individuelle **Fußzeile**-Komponente konfigurieren, können Sie die Eigenschaft **Kopf-/Fußzeilendarstellung** zum Angeben der Seiten verwenden, für die die Komponente verwendet werden soll. Folgende Werte sind verfügbar:

- **Beliebig** – Führt die konfigurierte **Fußzeile**-Komponente für eine beliebige Seite des übergeordneten Excel-Arbeitsblatts aus.
- **Zuerst** – Führt die konfigurierte **Fußzeile**-Komponente nur für die erste Seite des übergeordneten Excel-Arbeitsblatts aus.
- **Gerade** – Führt die konfigurierte **Fußzeile**-Komponente nur für die geraden Seiten des übergeordneten Excel-Arbeitsblatts aus.
- **Ungerade** – Führt die konfigurierte **Fußzeile**-Komponente nur für die ungeraden Seiten des übergeordneten Excel-Arbeitsblatts aus.

Einer einzelnen **Blatt**-Komponente können Sie mehrere **Fußzeile**-Komponenten hinzufügen, von denen jede einen anderen Wert in der Eigenschaft **Kopf-/Fußzeilendarstellung** besitzt. Auf diese Weise können Sie verschiedene Fußzeilen für verschiedene Seitentypen in einem Excel-Arbeitsblatt generieren.

> [!NOTE]
> Vergewissern Sie sich, dass jede **Fußzeile**-Komponente, die Sie einer einzelnen **Blatt**-Komponenten hinzufügen, einen anderen Wert in der Eigenschaft **Kopf-/Fußzeilendarstellung** besitzt. Ansonsten tritt [Prüfungsfehler](er-components-inspections.md#i16) auf. Die Fehlermeldung, die Sie erhalten, benachrichtigt Sie über die Inkonsistenz.

Fügen Sie unter der hinzugefügten **Fußzeile**-Komponente die erforderlichen verschachtelten Komponenten der Typen **Text\\String**, **Text\\DateTime** oder eines anderen Typs hinzu. Konfigurieren Sie die Bindungen für diese Komponenten, um anzugeben, wie Ihre Seitenfußzeile ausgefüllt werden soll.

Sie können auch spezielle [Formatierungscodes](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) verwenden, um den Inhalt einer generierten Fußzeile korrekt zu formatieren. Befolgen Sie die Schritte in [Beispiel 1](#example-1) im weiteren Verlauf des Themas, um zu erfahren, wie Sie diesen Ansatz verwenden.

> [!NOTE]
> Berücksichtigen Sie beim Konfigurieren von EB-Formaten unbedingt die [Spezifikationen und Beschränkungen in Excel](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) sowie die maximale Zeichenanzahl für eine einzelne Kopf- oder Fußzeile.

## <a name="header-component"></a>Kopfzeilenkomponente

Die **Kopfzeile**-Komponente wird verwendet, um Kopfzeilen am oberen Rand eines generierten Arbeitsblatts in einer Excel-Arbeitsmappe auszufüllen. Sie wird wie die **Fußzeile**-Komponente verwendet.

## <a name="edit-an-added-er-format"></a>Hinzugefügtes EB-Format bearbeiten

### <a name="update-a-template"></a>Vorlage aktualisieren

Sie können auf der Registerkarte **Importieren** des Aktionsbereichs die Option **Aus Excel importieren** auswählen, um eine aktualisierte Vorlage in ein bearbeitbares EB-Format zu importieren. Während dieses Vorgangs wird eine Vorlage der ausgewählten **Excel\\Datei**-Komponente durch eine neue Vorlage ersetzt. Der Inhalt des bearbeitbaren EB-Formats wird mit dem Inhalt der aktualisierten EB-Vorlage synchronisiert.

- Für jeden Excel-Namen wird automatisch eine neue EB-Format-Komponente erstellt, wenn die EB-Format-Komponente nicht im bearbeitbaren Format gefunden wird.
- Jede EB-Format-Komponente wird aus dem bearbeitbaren EB-Format gelöscht, wenn kein entsprechender Excel-Name dafür gefunden wird.

> [!NOTE]
> Legen Sie die Option **Excel-Arbeitsblattformat-Element erstellen** auf **Ja** fest, wenn Sie das optionale **Blatt**-Element im bearbeitbaren EB-Format erstellen möchten.
>
> Wenn das bearbeitbare EB-Format ursprünglich **Blatt**-Elemente enthielt, wird empfohlen, dass Sie die Option **Excel-Arbeitsblattformat-Element erstellen** auf **Ja** festlegen, wenn Sie eine aktualisierte Vorlage importieren. Anderfalls werden alle verschachtelten Elemente des ursprünglichen **Blatt**-Elements von Grund auf neu erstellt. Daher gehen alle Bindungen der neu erstellten Formatelemente im aktualisierten EB-Format verloren.

![Option „Excel-Arbeitsblattformat-Element erstellen“ im Dialogfeld „Aus Excel aktualisieren“](./media/er-excel-format-update-template.png)

Führen Sie die Schritte unter [Elektronische Berichterstellungsformate ändern, indem Microsoft Excel-Vorlagen erneut angewendet werden](modify-electronic-reporting-format-reapply-excel-template.md), um weitere Informationen zu dieser Funktion zu erhalten.

## <a name="validate-an-er-format"></a>EB-Format überprüfen

Wenn Sie ein bearbeitbares EB-Format überprüfen, wird eine Konsistenzprüfung durchgeführt, um sicherzustellen, dass der Excel-Name in der aktuell verwendeten Excel-Vorlage vorhanden ist. Sie werden über etwaige Inkonsistenzen informiert. Bei einigen Inkonsistenzen ist die Option zur automatischen Behebung von Problemen verfügbar.

![Meldung „Überprüfungsfehler“](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Berechnung von Excel-Formeln steuern

Wenn ein ausgehendes Dokument in einem Microsoft Excel-Arbeitsmappenformat generiert wird, enthalten einige Zellen dieses Dokuments möglicherweise Excel-Formeln. Wenn die Funktion **Aktivieren Sie die Verwendung der EPPlus-Bibliothek im Rahmen für elektronische Berichte** aktiviert ist, können Sie steuern, wann die Formeln berechnet werden, indem Sie den Wert des [Parameters](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Berechnungsoptionen** in der verwendeten Excel-Vorlage ändern:

- Wählen Sie **Automatisch** aus, um alle abhängigen Formeln jedes Mal neu zu berechnen, wenn ein generiertes Dokument an neue Bereiche, Zellen usw. angehängt wird.
    >[!NOTE]
    > Dies kann zu Leistungsproblemen bei Excel-Vorlagen führen, die mehrere verwandte Formeln enthalten.
- Wählen Sie **Manuell** aus, um eine Neuberechnung der Formel beim Generieren eines Dokuments zu vermeiden.
    >[!NOTE]
    > Die Neuberechnung der Formel wird manuell erzwungen, wenn ein generiertes Dokument in Excel zur Vorschau geöffnet wird.
    > Verwenden Sie diese Option nicht, wenn Sie ein EB-Ziel konfigurieren, das die Verwendung eines generierten Dokuments ohne Vorschau in Excel (PDF-Konvertierung, E-Mail usw.) voraussetzt, da das generierte Dokument möglicherweise keine Werte in Zellen enthält, die Formeln enthalten.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Beispiel 1: Fußzeileninhalt formatieren

1. Verwenden Sie die bereitgestellten EB-Konfigurationen, um ein druckbares Freitext-Dokument (Free Text Invoice, FTI) zu [generieren](er-generate-printable-fti-forms.md) .
2. Überprüfen Sie die Fußzeile des generierten Dokuments. Beachten Sie, dass es Informationen zur aktuellen Seitenzahl und zur Gesamtzahl der Seiten im Dokument enthält.

    ![Die Fußzeile eines generierten Dokuments im Excel-Format überprüfen](./media/er-fillable-excel-footer-1.gif)

3. [Öffnen](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) Sie im EB-Formatdesigner das Beispiel-EB-Format zur Überprüfung.

    Die Fußzeile des Arbeitsblattes **Rechnung** wird basierend auf den Einstellungen von zwei **String**-Komponenten generiert, die sich unter der **Fußzeile**-Komponente befinden:

    - Die erste **String**-Komponente füllt die folgenden speziellen Formatierungscodes aus, um Excel zu zwingen, bestimmte Formatierungen anzuwenden:

        - **&C** – Mittiges Ausrichten des Fußzeilentextes.
        - **&"Segoe UI,Regular"&8** – Darstellen des Fußzeilentextes in der Schrift "Segoe UI Regular" und in einer Größe von 8-Punkt.

    - Die zweite **String**-Komponente füllt den Text aus, der die aktuelle Seitenzahl und die Gesamtzahl der Seiten im aktuellen Dokument enthält.

    ![Die EB-Formatkomponente der Fußzeile auf der Seite „Formatdesigner“ überprüfen](./media/er-fillable-excel-footer-2.png)

4. Passen Sie das Beispiel-EB-Format an, um die aktuelle Seitenfußzeile zu ändern:

    1. [Erstellen](er-quick-start2-customize-report.md#DeriveProvidedFormat) Sie ein abgeleitetes **Freitextrechnung (Excel) benutzerdefiniert**-EB-Format, das auf dem Beispiel-EB-Format basiert.
    2. Fügen Sie das erste neue Paar an **String**-Komponenten für die **Fußzeile**-Komponente des Arbeitsblattes **Rechnung** hinzu:

        1. Fügen Sie eine **String**-Komponente hinzu, die den Firmennamen links ausrichtet und in der Größe 8-Punkt in der Schriftart "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**) darstellt.
        2. Fügen Sie eine **String**-Komponente hinzu, die den Firmennamen ausfüllt (**model.InvoiceBase.CompanyInfo.Name**).

    3. Fügen Sie das zweite neue Paar an **String**-Komponenten für die **Fußzeile**-Komponente des Arbeitsblattes **Rechnung** hinzu:

        1. Fügen Sie eine **String**-Komponente hinzu, die das Verarbeitungsdatum rechts ausrichtet und in der Größe 8-Punkt in der Schriftart "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**) darstellt.
        2. Fügen Sie eine **String**-Komponente hinzu, die das Verarbeitungsdatum in einem benutzerdefinierten Format ausfüllt (**""&nbsp;"&DATEFORMAT(SESSIONTODAY(), "JJJJ-MM-TT")**).

        ![Überprüfen der EB-Formatkomponente der Fußzeile auf der Seite „Formatdesigner“](./media/er-fillable-excel-footer-3.png)

    4. [Vervollständigen](er-quick-start2-customize-report.md#CompleteDerivedFormat) Sie die Entwurfsversion des abgeleiteten **Freitextrechnung (Excel) benutzerdefiniert**-EB-Formats.

5. [Konfigurieren](er-generate-printable-fti-forms.md#configure-print-management) Sie die Druckverwaltung zur Verwendung des abgeleiteten **Freitextrechnung (Excel) benutzerdefiniert**-EB-Formats anstelle des Beispiel-EB-Formats.
6. Generieren Sie ein druckbares FTI-Dokument, und überprüfen Sie die Fußzeile des generierten Dokuments.

    ![Überprüfen der Fußzeile eines generierten Dokuments im Excel-Format](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Entwerfen einer Konfiguration für das Erstellen von Berichten im OPENXML-Format](tasks\er-design-reports-openxml-2016-11.md)

[Ändern von elektronisches Berichterstellungsformaten, indem Excel-Vorlagen erneut angewendet werden](modify-electronic-reporting-format-reapply-excel-template.md)

[Horizontal erweiterbare Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten verwenden](tasks/er-horizontal-1.md)

[Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von ER](electronic-reporting-embed-images-shapes.md)

[Konfigurieren Sie die elektronische Berichterstattung (ER), um Daten in Power BI zu ziehen.](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]