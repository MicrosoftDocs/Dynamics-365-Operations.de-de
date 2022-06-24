---
title: Eine Konfiguration zur Generierung von Dokumenten im Excel-Format entwerfen
description: Dieser Artikel enthält Informationen zum Entwerfen eines Formats für die elektronische Berichterstellung (EB), um eine Excel-Vorlage auszufüllen und ausgehende Dokumente im Excel-Format zu generieren.
author: NickSelin
ms.date: 05/09/2022
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
ms.openlocfilehash: 4660aaf438ee091eed30387d984746ac2c3b4bd7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854813"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Eine Konfiguration zur Generierung von Dokumenten im Excel-Format entwerfen

[!include[banner](../includes/banner.md)]

Sie können eine Formatkonfiguration für die [elektronische Berichtersterstellung (EB)](general-electronic-reporting.md) mit einer EB-Formatkomponente entwerfen, die Sie konfigurieren können, um ein ausgehendes Dokument in einem Microsoft Excel-Arbeitsmappenformat zu generieren. Zu diesem Zweck müssen bestimmte Komponenten des EB-Formats verwendet werden.

Führen Sie die folgenden Schritte im Artikel [Konfiguration zum Generieren von Berichten im OPENXML-Format entwerfen](tasks/er-design-reports-openxml-2016-11.md) aus, um weitere Informationen zu dieser Funktion zu erhalten.

## <a name="add-a-new-er-format"></a>Neues ER-Format hinzufügen

Wenn Sie eine neue EB-Formatkonfiguration hinzufügen, um ein ausgehendes Dokument in einem Excel-Arbeitsmappenformat zu generieren, müssen Sie den **Excel**-Wert das Attribut **Formattyp** des Formats auswählen oder das Attribut **Formattyp** leer lassen.

- Wenn Sie **Excel** auswählen, können Sie das Format so konfigurieren, dass ein ausgehendes Dokument nur im Excel-Format generiert wird.
- Wenn Sie das Attribut leer lassen, können Sie das Format so konfigurieren, dass ein ausgehendes Dokument in einem beliebigen Format generiert wird, das vom EB-Framework unterstützt wird.

Wählen Sie im Aktionsbereich **Designer** aus, und öffnen Sie die EB-Formatkomponente zur Bearbeitung im EB-Vorgangs-Designer aus, um die EB-Formatkomponente der Konfiguration zu konfigurieren.

![Seite „Konfigurationen“.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Komponente „Excel-Datei“

### <a name="manual-entry"></a>Manuelle Eingabe

Sie müssen dem konfigurierten EB-Format eine **Excel\\Datei-Komponente** hinzufügen, um ein ausgehendes Dokument im Excel-Format zu generieren.

![Komponente „Excel\Datei“.](./media/er-excel-format-add-file-component.png)

Hängen Sie eine Excel-Arbeitsmappe mit der .xlsx-Erweiterung als Vorlage für ausgehende Dokumente an die **Excel\\Datei**-Komponente an, um das Layout des ausgehenden Dokuments festzulegen.

> [!NOTE]
> Wenn Sie eine Vorlage manuell anhängen, müssen Sie einen [Dokumententyp](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) verwenden, der zu diesem Zweck im [EB-Parameter](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) konfiguriert wurde.

![Hinzufügen eines Anhangs zur Excel-\Datei-Komponente.](./media/er-excel-format-add-file-component2.png)

Wenn Sie das konfigurierte ER-Format ausführen, müssen Sie der **Excel\\Datei**-Komponente die Komponenten **Blatt**-, **Angebot** und **Zelle** hinzufügen, um festzulegen, wie die angehängte Vorlage ausgefüllt wird. Jede verschachtelte Komponente muss mit einem Excel-benannten Element verknüpft sein.

### <a name="template-import"></a>Vorlagenimport

Sie können auf der Registerkarte **Importieren** des Aktionsbereichs die Option **Aus Excel importieren** auswählen, um eine neue Vorlage in ein leeres EB-Format zu importieren. In diesem Beispiel wird automatisch eine **Excel\\Datei**-Komponente erstellt und die importierte Vorlage daran angehängt. Alle erforderlichen EB-Komponenten werden ebenfalls automatisch erstellt, basierend auf der Liste der erkannten Excel-benannten Elemente.

![Auswählen von „Aus Excel importieren“.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Wenn Sie das optionale **Blatt**-Element im bearbeitbaren EB-Format erstellen möchten, legen Sie die Option **Excel-Arbeitsblattformat-Element erstellen** auf **Ja** fest.

## <a name="sheet-component"></a>Komponente „Blatt“

Die **Blatt**-Komponente gibt ein Arbeitsblatt der angehängten Excel-Arbeitsmappe an, das ausgefüllt werden muss. Der Name des Arbeitsblatts in einer Excel-Vorlage ist in der **Blatt**-Eigenschaft dieser Komponente definiert.

> [!NOTE]
> Diese Komponente ist für Excel-Arbeitsmappen, die ein einzelnes Arbeitsblatt enthalten, optional.

Auf der Registerkarte **Zuordnung** des EB-Vorgangs-Designers können Sie die Eigenschaft **Aktiviert** für eine **Blatt**-Komponente konfigurieren, um anzugeben, ob die Komponente in ein generiertes Dokument eingefügt werden muss:

- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Wahr** zur Laufzeit oder wenn überhaupt kein Ausdruck konfiguriert ist, wird das entsprechende Arbeitsblatt im generierten Dokument ausgefüllt.
- Wenn ein Ausdruck der Eigenschaft **Aktiviert** ist für die Rückgabe von **Falsch** zur Laufzeit konfiguriert ist, enthält das generierte Dokument kein Arbeitsblatt.

![Beispiel einer Blatt-Komponente.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Komponente „Bereich“

### <a name="nested-components"></a>Verschachtelte Komponenten

#### <a name="data-typing"></a>Daten-Typisierung

Die Komponente **Bereich** kann weitere verschachtelte ER-Komponenten enthalten, die zur Eingabe von Werten in die entsprechenden Bereiche verwendet werden.

- Wenn eine Komponente der Gruppe **Text** für die Eingabe von Werten verwendet wird, erfolgt die Eingabe des Werts in einem Excel-Bereich als Textwert.

    > [!NOTE]
    > Verwenden Sie dieses Muster, um eingegebene Werte basierend auf dem in der Anwendung definierten Gebietsschema zu formatieren.

- Wenn die **Zelle**-Komponente der **Excel**-Gruppe zur Eingabe von Werten verwendet wird, wird der Wert in einem Excel-Bereich als Wert des Datentyps eingegeben, der durch die Bindung dieser **Zelle**-Komponente definiert ist. Der Datentyp kann zum Beispiel **String**, **Real** oder **Integer** sein.

    > [!NOTE]
    > Verwenden Sie dieses Muster, damit die Excel-Anwendung eingegebene Werte basierend auf dem Gebietsschema des lokalen Computers formatieren kann, der das ausgehende Dokument öffnet.

#### <a name="row-handling"></a>Behandlung von Zeilen

Die Komponente **Bereich** kann als vertikal repliziert konfiguriert werden, so dass mehrere Zeilen in einem Excel-Arbeitsblatt erzeugt werden. Die Zeilen können von der übergeordneten **Bereich**-Komponente oder von deren verschachtelten **Bereich**-Komponenten erzeugt werden.

In Version 10.0.26 und später können Sie ein generiertes Arbeitsblatt dazu zwingen, die generierten Zeilen auf derselben Seite zu halten. Legen Sie im ER-Formatdesigner die Option **Zeilen zusammenhalten** auf **Ja** für die übergeordnete Komponente **Bereich** im bearbeitbaren ER-Format fest. ER wird dann versuchen, alle Inhalte, die von diesem Bereich generiert werden, auf derselben Seite zu halten. Wenn die Höhe des Inhalts den verbleibenden Platz auf der aktuellen Seite überschreitet, wird ein Seitenumbruch eingefügt, und der Inhalt beginnt am Anfang der nächsten neuen Seite.

> [!NOTE]
> Wir empfehlen Ihnen, die Option **Zeilen zusammenhalten** nur für Bereiche zu konfigurieren, die sich über die gesamte Breite eines generierten Dokuments erstrecken.
>
> Die Option **Zeilen zusammenhalten** gilt nur für **Excel \> Datei** Komponenten, die für die Verwendung einer Excel Arbeitsmappenvorlage konfiguriert sind.
>
> Die Option **Zeilen zusammenhalten** kann nur verwendet werden, wenn die Funktion **Verwendung der EPPlus-Bibliothek im Electronic Reporting Framework aktivieren** aktiviert ist.
>
> Diese Funktion kann für **Bereich**-Komponenten verwendet werden, die sich unter der **Seite**-Komponente befinden. Es gibt jedoch keine Garantie dafür, dass [Seitenfußsummen](er-paginate-excel-reports.md#add-data-sources-to-calculate-page-footer-totals) durch die Verwendung von [Datensammlung](er-data-collection-data-sources.md)-Datenquellen korrekt berechnet werden.

Um zu erfahren, wie Sie diese Option verwenden, folgen Sie den Beispielschritten in [Entwerfen Sie ein ER-Format, um Zeilen auf derselben Excel-Seite zusammenzuhalten](er-keep-excel-rows-together.md).

### <a name="replication"></a>Wiederholung

Die Eigenschaft **Replikationsrichtung** gibt an, ob und wie ein Bereich in einem generierten Dokument wiederholt wird:

- **Keine Replikation** - Der entsprechende Excel-Bereich wird in dem generierten Dokument nicht wiederholt.
- **Vertikal** - Der entsprechende Excel-Bereich wird im generierten Dokument vertikal wiederholt. Jeder replizierte Bereich wird in einer Excel-Vorlage unter den ursprünglichen Bereich gestellt. Die Anzahl der Wiederholungen wird durch die Anzahl der Datensätze in einer Datenquelle des Typs **Datensatzliste** definiert, der an diese EB-Komponente gebunden ist.
- **Horizontal** - Der entsprechende Excel-Bereich wird in dem generierten Dokument horizontal wiederholt. Jeder replizierte Bereich wird in einer Excel-Vorlage rechts neben dem Originalbereich eingefügt. Die Anzahl der Wiederholungen wird durch die Anzahl der Datensätze in einer Datenquelle des Typs **Datensatzliste** definiert, der an diese EB-Komponente gebunden ist.

    Führen Sie die Schritte unter [Horizontal erweiterbare Bereiche verwenden, um Spalten in Excel-Berichten dynamisch hinzuzufügen](tasks/er-horizontal-1.md) aus, um weitere Informationen zu erhalten.

### <a name="enabling"></a>Wird aktiviert

Auf der Registerkarte **Zuordnung** des EB-Vorgangs-Designers können Sie die Eigenschaft **Aktiviert** für eine **Bereich**-Komponente konfigurieren, um anzugeben, ob die Komponente in ein generiertes Dokument eingefügt werden muss:

- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Wahr** zur Laufzeit oder wenn überhaupt kein Ausdruck konfiguriert ist, wird der entsprechende Bereich im generierten Dokument ausgefüllt.
- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Falsch** zur Laufzeit konfiguriert ist und dieser Bereich nicht sämtliche Zeilen oder Spalten darstellt, wird der entsprechende Bereich nicht im generierten Dokument ausgefüllt.
- Wenn ein Ausdruck der Eigenschaft **Aktiviert** für die Rückgabe von **Falsch** zur Laufzeit konfiguriert ist und dieser Bereich sämtliche Zeilen oder Spalten darstellt, enthält das Dokument diese Zeilen und Spalten als ausgeblendete Zeilen und Spalten.

### <a name="resizing"></a>Ändern der Größe

Sie können Ihre Excel-Vorlage so konfigurieren, dass Zellen zur Darstellung von Textdaten verwendet werden. Um sicherzustellen, dass der gesamte Text in einer Zelle in einem generierten Dokument sichtbar ist, können Sie diese Zelle so konfigurieren, dass der Text darin automatisch umgebrochen wird. Sie können die Zeile, die diese Zelle enthält, auch so konfigurieren, dass ihre Höhe automatisch angepasst wird, wenn der umgebrochene Text nicht vollständig sichtbar ist. Weitere Informationen finden Sie im Abschnitt „Text in einer Zelle umbrechen“ in [Korrigieren von unvollständig angezeigten Daten in Zellen](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e).

> [!NOTE]
> Wegen einer bekannten [Excel-Einschränkung](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353), selbst wenn Sie Zellen so konfigurieren, dass Text umgebrochen wird, und Sie die Zeilen, die diese Zellen enthalten, so konfigurieren, dass ihre Höhe automatisch an den umgebrochenen Text angepasst wird, können Sie die Excel-Funktionen **AutoFit** und **Zeilenumbruch** für verbundene Zellen und die Zeilen, die sie enthalten, eventuell nicht verwenden. 

Ab Dynamics 365 Finance-Version 10.0.23 können Sie ER zwingen, beim Arbeiten in einem generierten Dokument die Höhe jeder Zeile zu berechnen, die so konfiguriert wurde, dass ihre Höhe automatisch an den Inhalt verschachtelter Zellen angepasst wird, wenn diese Zeile mindestens eine verbundene Zelle enthält, die zum Umbrechen des Texts in der Zelle konfiguriert war. Die berechnete Höhe wird dann verwendet, um die Größe der Zeile zu ändern, um sicherzustellen, dass alle Zellen in der Zeile im generierten Dokument sichtbar sind.

> [!NOTE]
> Beachten Sie, dass diese Funktion möglicherweise nicht wie erwartet funktioniert, wenn eine benutzerdefinierte Schriftart zum Formatieren einer verbundenen Zelle verwendet wird. Da Excel keine benutzerdefinierten Schriftarten einbettet, werden keine Informationen zur benutzerdefinierten Schriftgröße bereitgestellt. Daher kann die Größe der verbundenen Zelle falsch geschätzt werden.

Gehen Sie folgendermaßen vor, um diese Funktion beim Ausführen von EB-Formaten zu verwenden, die für die Verwendung von Excel-Vorlagen zum Generieren ausgehender Dokumente konfiguriert wurden.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Parameter für elektronische Berichterstellung** aus.
3. Auf der Seite **Parameter für elektronische Berichterstellung** legen Sie auf der Registerkarte **Runtime** die Option **Zeilenhöhe automatisch anpassen** auf **Ja** fest.

Wenn Sie diese Regel für ein einzelnes EB-Format ändern möchten, aktualisieren Sie die Entwurfsversion dieses Formats, indem Sie wie folgt vorgehen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen**.
3. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich eine EB-Konfiguration aus, die für die Verwendung einer Excel-Vorlage zum Generieren ausgehender Dokumente ausgelegt ist.
4. Wählen Sie im Inforegister **Versionen** die Konfigurationsversion mit dem Status **Entwurf** aus.
5. Wählen Sie im Aktivitätsbereich **Designer** aus.
6. Wählen Sie auf der Seite **Formatdesigner** in der Formatstruktur im linken Bereich die Excel-Komponente aus, die mit einer Excel-Vorlage verknüpft ist.
7. Wählen Sie auf der Registerkarte **Format** im Feld **Zeilenhöhe anpassen** einen Wert aus, um anzugeben, ob EB zur Runtime gezwungen werden soll, die Zeilenhöhe in einem ausgehenden Dokument zu ändern, das vom bearbeiteten EB-Format generiert wird:

    - **Standard**: Verwenden Sie die allgemeine Einstellung, die im Feld **Zeilenhöhe automatisch anpassen** auf der Seite **Parameter der elektronischen Berichterstellung**.
    - **Ja**: Die allgemeinen Einstellungen werden überschrieben und die Zeilenhöhe zur Runtime geändert.
    - **Nein**: Die allgemeinen Einstellungen werden überschrieben und die Zeilenhöhe zur Runtime nicht geändert.

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

## <a name="page-component"></a><a name="page-component"></a>Seitenkomponente

### <a name="overview"></a>Übersicht

Sie können die **Seiten**-Komponente verwenden, wenn Sie möchten, dass Excel Ihr ER-Format befolgt und die Paginierung in einem generierten ausgehenden Dokument strukturiert. Wenn ER-Formatkomponenten ausgeführt werden, die sich unter der **Seiten**-Komponente befinden, werden die erforderlichen Seitenumbrüche automatisch hinzugefügt. Dabei werden die Größe des generierten Inhalts, der Seitenaufbau der Excel-Vorlage und das in der Excel-Vorlage gewählte Papierformat berücksichtigt.

Wenn Sie ein generiertes Dokument in verschiedene Abschnitte aufteilen müssen, von denen jeder eine andere Paginierung besitzt, können Sie mehrere **Seiten**-Komponenten in jeder [Blatt](er-fillable-excel.md#sheet-component)-Komponente konfigurieren.

### <a name="structure"></a><a name="page-component-structure"></a>Struktur

Wenn die erste Komponente unter der Komponente **Seite** eine [Bereich](er-fillable-excel.md#range-component)-Komponente ist, bei der die Eigenschaft **Replikationsrichtung** auf **Keine Replikation** gesetzt ist, wird dieser Bereich als Seitenkopf für die Paginierung betrachtet, die auf den Einstellungen der aktuellen **Seiten**-Komponente basiert. Der dieser Formatkomponente zugeordnete Excel-Bereich wird oben auf jeder Seite wiederholt, die mit den Einstellungen der aktuellen **Seiten**-Komponente generiert wird.

> [!NOTE]
> Für eine korrekte Paginierung, wenn der Bereich [Oben zu wiederholenden Zeilen](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409) in Ihrer Excel-Vorlage konfiguriert ist, muss die Adresse dieses Excel-Bereichs mit der Adresse des Excel-Bereichs übereinstimmen, der mit der zuvor beschriebenen **Bereich**-Komponente verknüpft ist.

Wenn die letzte Komponente unter der Komponente **Seite** eine **Bereich**-Komponente ist, bei der die Eigenschaft **Replikationsrichtung** auf **Keine Replikation** gesetzt ist, wird dieser Bereich als Seitenfußzeile für die Paginierung betrachtet, die auf den Einstellungen der aktuellen **Seiten**-Komponente basiert. Der dieser Formatkomponente zugeordnete Excel-Bereich wird unten auf jeder Seite wiederholt, die mit den Einstellungen der aktuellen **Seiten**-Komponente generiert wird.

> [!NOTE]
> Für eine korrekte Paginierung darf die Größe der Excel-Bereiche, die den **Bereich**-Komponenten zugeordnet sind, während der Runtime nicht geändert werden. Es wird nicht empfohlen, Zellen dieses Bereichs mit den Optionen **Text in eine Zelle umbrechen** und **Zeilenhöhe automatisch anpassen** [in Excel](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84) zu formatieren.

Sie können mehrere andere **Bereich**-Komponenten zwischen den optionalen **Bereich**-Komponenten hinzufügen, um anzugeben, wie ein generiertes Dokument ausgefüllt wird.

Wenn der Satz der verschachtelten **Bereich**-Komponenten unter der **Seite**-Komponente nicht mit der zuvor beschriebenen Struktur übereinstimmt, tritt ein [Validierungsfehler](er-components-inspections.md#i17) zur Entwurfszeit im ER-Formatdesigner auf. Die Fehlermeldung weist Sie darauf hin, dass das Problem zur Runtime zu Problemen führen kann.

> [!NOTE]
> Um eine korrekte Ausgabe zu generieren, geben Sie keine Bindung für eine **Bereich**-Komponente unter der **Seite**-Komponente an, wenn die Eigenschaft **Replikationsrichtung** für diese **Bereich**-Komponente auf **Keine Replikation** festgelegt ist, und der Bereich so konfiguriert ist, um Seitenkopfzeilen oder Seitenfußzeilen zu generieren.

Wenn Sie eine paginierungsbezogene Summierung und Zählung wünschen, um laufende Summen und Summen pro Seite zu berechnen, empfehlen wir Ihnen, die erforderliche Datenquelle [Datensammlung](er-data-collection-data-sources.md) zu konfigurieren. Um zu lernen, wie man die **Seite**-Komponente verwendet, um ein generiertes Excel-Dokument zu paginieren, führen Sie die Verfahren in [Ein ER-Format verwenden, um ein generiertes Dokument im Excel-Format zu paginieren](er-paginate-excel-reports.md) aus.

### <a name="limitations"></a><a name="page-component-limitations"></a>Einschränkungen

Wenn Sie die **Seite**-Komponente für die Excel-Paginierung verwenden, wissen Sie die endgültige Seitenzahl in einem generierten Dokument erst, wenn die Paginierung abgeschlossen ist. Daher können Sie die Gesamtseitenzahl nicht mithilfe von ER-Formeln berechnen und die richtige Seitenzahl eines generierten Dokuments auf einer Seite vor der letzten Seite drucken.

> [!TIP]
> Um dieses Ergebnis in einer Excel-Kopf- oder Fußzeile zu erreichen, verwenden Sie die spezielle Excel-[Formatierung](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) für Kopf- und Fußzeilen.

Konfigurierte **Seite**-Komponenten werden nicht berücksichtigt, wenn Sie eine Excel-Vorlage im bearbeitbaren Format in der Dynamics 365 Finance-Version 10.0.22 aktualisieren. Diese Funktionalität wird für weitere Versionen von Finance in Betracht gezogen.

Wenn Sie Ihre Excel-Vorlage zur Verwendung der [bedingten Formatierung](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting) konfigurieren, funktioniert sie in manchen Fällen möglicherweise nicht wie erwartet.

### <a name="applicability"></a>Anwendbarkeit

Die **Seite**-Komponente funktioniert für das Format [Excel-Datei](er-fillable-excel.md#excel-file-component) nur, wenn diese Komponente zur Verwendung einer Vorlage in Excel konfiguriert ist. Wenn Sie die Excel-Vorlage durch eine Word-Vorlage [ersetzen](tasks/er-design-configuration-word-2016-11.md) und dann das bearbeitbare ER-Format ausführen, wir die **Seite**-Komponente ignoriert.

Die **Seite**-Komponente funktioniert nur, wenn die Funktion **Aktivieren Sie die Verwendung der EPPlus-Bibliothek im Rahmen für elektronische Berichte** aktiviert ist. Zur Laufzeit wird eine Ausnahme ausgelöst, wenn ER versucht, die **Seite**-Komponente zu verarbeiten, während diese Funktion deaktiviert ist.

> [!NOTE]
> Zur Laufzeit wird eine Ausnahme ausgelöst, wenn ein ER-Format die **Seite**-Komponente für eine Excel-Vorlage verarbeitet, die mindestens eine Formel enthält, die auf eine ungültige Zelle verweist. Um Laufzeitfehler zu vermeiden, korrigieren Sie die Excel-Vorlage wie in [So korrigieren Sie einen #REF!-Fehler beschrieben](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

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

Sie können auch spezielle [Formatierungscodes](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) verwenden, um den Inhalt einer generierten Fußzeile korrekt zu formatieren. Befolgen Sie die Schritte in [Beispiel 1](#example-1) im weiteren Verlauf des Artikels, um zu erfahren, wie Sie diesen Ansatz verwenden.

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

![Option „Excel-Arbeitsblattformat-Element erstellen“ im Dialogfeld „Aus Excel aktualisieren“.](./media/er-excel-format-update-template.png)

Ab Version 10.0.28 können Sie die Option **Excel-Kopfzeilen- und Excel-Fußzeilenformatelemente aktualisieren** verwenden.

- Wenn Sie diese Option auf **Nein** setzen, bleiben die Formatelemente Excel-Kopfzeile und Excel-Fußzeile unverändert, auch wenn die entsprechenden Kopf- oder Fußzeilen in den Arbeitsblättern der importierten Vorlage im Excel-Arbeitsmappenformat aktualisiert wurden.
- Wenn Sie diese Option auf **Ja** setzen, werden die Formatelemente Excel-Kopfzeile und Excel-Fußzeile verändert, wenn die entsprechenden Kopf- oder Fußzeilen in den Arbeitsblättern der importierten Vorlage im Excel-Arbeitsmappenformat aktualisiert werden.

    - Wenn die Struktur einer Kopf- oder Fußzeile eines Arbeitsblatts nicht geändert oder nur angehängt wurde, wird die Struktur des entsprechenden Formatelements Excel-Kopfzeile oder Excel-Fußzeile aktualisiert. Bindungen von Formatelementen, die unter diesem Formatelement Excel-Kopfzeile oder Excel-Fußzeile verschachtelt sind, bleiben erhalten.
    - Wenn die Struktur einer Kopf- oder Fußzeile eines Arbeitsblatts geändert wird, wird das entsprechende Formatelement der Excel-Kopfzeile oder Excel-Fußzeile neu erstellt. Bindungen von Formatelementen, die unter diesem Formatelement Excel-Kopfzeile oder Excel-Fußzeile verschachtelt sind, werden entfernt.

![Option „Excel-Kopfzeilen- und Excel-Fußzeilenformatelemente aktualisieren“ im Dialogfeld „Aus Excel aktualisieren“.](./media/er-excel-format-update-template2.png)

Führen Sie die Schritte unter [Elektronische Berichterstellungsformate ändern, indem Microsoft Excel-Vorlagen erneut angewendet werden](modify-electronic-reporting-format-reapply-excel-template.md), um weitere Informationen zu dieser Funktion zu erhalten.

## <a name="validate-an-er-format"></a>EB-Format überprüfen

Wenn Sie ein bearbeitbares EB-Format überprüfen, wird eine Konsistenzprüfung durchgeführt, um sicherzustellen, dass der Excel-Name in der aktuell verwendeten Excel-Vorlage vorhanden ist. Sie werden über etwaige Inkonsistenzen informiert. Bei einigen Inkonsistenzen ist die Option zur automatischen Behebung von Problemen verfügbar.

![Meldung „Überprüfungsfehler“.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Berechnung von Excel-Formeln steuern

Wenn ein ausgehendes Dokument in einem Microsoft Excel-Arbeitsmappenformat generiert wird, enthalten einige Zellen dieses Dokuments möglicherweise Excel-Formeln. Wenn die Funktion **Aktivieren Sie die Verwendung der EPPlus-Bibliothek im Rahmen für elektronische Berichte** aktiviert ist, können Sie steuern, wann die Formeln berechnet werden, indem Sie den Wert des [Parameters](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Berechnungsoptionen** in der verwendeten Excel-Vorlage ändern:

- Wählen Sie **Automatisch** aus, um alle abhängigen Formeln jedes Mal neu zu berechnen, wenn ein generiertes Dokument an neue Bereiche, Zellen usw. angehängt wird.

    > [!NOTE]
    > Dies kann zu Leistungsproblemen bei Excel-Vorlagen führen, die mehrere verwandte Formeln enthalten.

- Wählen Sie **Manuell** aus, um eine Neuberechnung der Formel beim Generieren eines Dokuments zu vermeiden.

    > [!NOTE]
    > Die Neuberechnung der Formel wird manuell erzwungen, wenn ein generiertes Dokument in Excel zur Vorschau geöffnet wird.
    > Verwenden Sie diese Option nicht, wenn Sie ein EB-Ziel konfigurieren, das die Verwendung eines generierten Dokuments ohne Vorschau in Excel (PDF-Konvertierung, E-Mail usw.) voraussetzt, da das generierte Dokument möglicherweise keine Werte in Zellen enthält, die Formeln enthalten.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Beispiel 1: Fußzeileninhalt formatieren

1. Verwenden Sie die bereitgestellten EB-Konfigurationen, um ein druckbares Freitext-Dokument (Free Text Invoice, FTI) zu [generieren](er-generate-printable-fti-forms.md) .
2. Überprüfen Sie die Fußzeile des generierten Dokuments. Beachten Sie, dass es Informationen zur aktuellen Seitenzahl und zur Gesamtzahl der Seiten im Dokument enthält.

    ![Die Fußzeile eines generierten Dokuments im Excel-Format überprüfen.](./media/er-fillable-excel-footer-1.gif)

3. [Öffnen](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) Sie im EB-Formatdesigner das Beispiel-EB-Format zur Überprüfung.

    Die Fußzeile des Arbeitsblattes **Rechnung** wird basierend auf den Einstellungen von zwei **String**-Komponenten generiert, die sich unter der **Fußzeile**-Komponente befinden:

    - Die erste **String**-Komponente füllt die folgenden speziellen Formatierungscodes aus, um Excel zu zwingen, bestimmte Formatierungen anzuwenden:

        - **&C** – Mittiges Ausrichten des Fußzeilentextes.
        - **&"Segoe UI,Regular"&8** – Darstellen des Fußzeilentextes in der Schrift "Segoe UI Regular" und in einer Größe von 8-Punkt.

    - Die zweite **String**-Komponente füllt den Text aus, der die aktuelle Seitenzahl und die Gesamtzahl der Seiten im aktuellen Dokument enthält.

    ![Die EB-Formatkomponente der Fußzeile auf der Seite „Formatdesigner“ überprüfen.](./media/er-fillable-excel-footer-2.png)

4. Passen Sie das Beispiel-EB-Format an, um die aktuelle Seitenfußzeile zu ändern:

    1. [Erstellen](er-quick-start2-customize-report.md#DeriveProvidedFormat) Sie ein abgeleitetes **Freitextrechnung (Excel) benutzerdefiniert**-EB-Format, das auf dem Beispiel-EB-Format basiert.
    2. Fügen Sie das erste neue Paar an **String**-Komponenten für die **Fußzeile**-Komponente des Arbeitsblattes **Rechnung** hinzu:

        1. Fügen Sie eine **String**-Komponente hinzu, die den Firmennamen links ausrichtet und in der Größe 8-Punkt in der Schriftart "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**) darstellt.
        2. Fügen Sie eine **String**-Komponente hinzu, die den Firmennamen ausfüllt (**model.InvoiceBase.CompanyInfo.Name**).

    3. Fügen Sie das zweite neue Paar an **String**-Komponenten für die **Fußzeile**-Komponente des Arbeitsblattes **Rechnung** hinzu:

        1. Fügen Sie eine **String**-Komponente hinzu, die das Verarbeitungsdatum rechts ausrichtet und in der Größe 8-Punkt in der Schriftart "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**) darstellt.
        2. Fügen Sie eine **String**-Komponente hinzu, die das Verarbeitungsdatum in einem benutzerdefinierten Format ausfüllt (**""&nbsp;"&DATEFORMAT(SESSIONTODAY(), "JJJJ-MM-TT")**).

        ![Überprüfen der EB-Formatkomponente der Fußzeile auf der Seite „Formatdesigner“.](./media/er-fillable-excel-footer-3.png)

    4. [Vervollständigen](er-quick-start2-customize-report.md#CompleteDerivedFormat) Sie die Entwurfsversion des abgeleiteten **Freitextrechnung (Excel) benutzerdefiniert**-EB-Formats.

5. [Konfigurieren](er-generate-printable-fti-forms.md#configure-print-management) Sie die Druckverwaltung zur Verwendung des abgeleiteten **Freitextrechnung (Excel) benutzerdefiniert**-EB-Formats anstelle des Beispiel-EB-Formats.
6. Generieren Sie ein druckbares FTI-Dokument, und überprüfen Sie die Fußzeile des generierten Dokuments.

    ![Überprüfen der Fußzeile eines generierten Dokuments im Excel-Format.](./media/er-fillable-excel-footer-4.gif)

## <a name="example-2-fixing-the-merged-cells-epplus-issue"></a><a name="example-2"></a>Beispiel 2: Behebung des EPPlus-Problems mit verbundenen Zellen

Sie können ein EB-Format ausführen, um ein ausgehendes Dokument in einem Excel-Arbeitsmappenformat zu generieren. Wenn die **Die Nutzung der EPPlus-Bibliothek im Rahmen der elektronische Berichterstellung aktivieren**-Funktion ist im **Funktionsverwaltung**-Arbeitsplatz aktiviert ist, wird die [EPPlus-Bibliothek](https://www.nuget.org/packages/epplus/4.5.2.1) verwendet, um eine Excel-Ausgabe zu erstellen. Allerdings können Sie wegen eines bekannten [Excel-Verhaltens](https://answers.microsoft.com/en-us/msoffice/forum/all/deleting-a-range-of-cells-that-includes-merged/8601462c-4e2c-48e0-bd23-848eecb872a9) und einer Einschränkung der EPPlus-Bibliothek auf die folgende Ausnahme stoßen: „Verbundene Zellen können nicht gelöscht/überschrieben werden. Ein Bereich wird teilweise mit einem anderen zusammengeführten Bereich zusammengeführt.“ Um zu erfahren, welche Art von Excel-Vorlagen diese Ausnahme verursachen können und wie Sie das Problem beheben können, führen Sie das folgende Beispiel durch.

1. Erstellen Sie in der Excel-Desktopanwendung eine neue Excel-Arbeitsmappe.
2. Fügen Sie auf Arbeitsblatt **Sheet1** den **ReportTitle**-Namen für Zelle **A2** hinzu.
3. Zellen **A1** und **A2** verbinden.

    ![Überprüfen der Ergebnisse vom Zusammenführen der Zellen A1 und A2 in der entworfenen Excel-Arbeitsmappe in der Excel-Desktopanwendung.](./media/er-fillable-excel-example2-1.png)

3. Auf der Seite **Konfigurationen** [ein neues EB-Format](er-fillable-excel.md#add-a-new-er-format) hinzufügen, um ein ausgehendes Dokument im Format einer Excel-Arbeitsmappe zu generieren.
4. Auf der **Formatdesigner**-Seite die gestaltete Excel-Arbeitsmappe als neue Vorlage für ausgehende Dokumente in das hinzugefügte ER-Format [importieren](er-fillable-excel.md#template-import).
5. Konfigurieren Sie auf der **Zuordnung**-Registerkarte die Bindung für die **ReportTitle**-Komponente des Typs [Zelle](er-fillable-excel.md#cell-component).
6. Führen Sie as konfigurierte EB-Format aus. Beachten Sie, dass die folgende Ausnahme ausgelöst wird: „Verbundene Zellen können nicht gelöscht/überschrieben werden. Ein Bereich wird teilweise mit einem anderen zusammengeführten Bereich zusammengeführt.“

    ![Überprüfen der Ergebnisse der Ausführung des konfigurierten EB-Formats auf der Seite Format-Designer.](./media/er-fillable-excel-example2-2.png)

Sie können das Problem auf eine der folgenden Arten beheben:

- **Einfacher, aber nicht zu empfehlen:** Aktivieren Sie im **Funktionsverwaltung**-Arbeitsbereich die Funktion **Die Nutzung der EPPlus-Bibliothek im Rahmen der elektronischen Berichterstellung aktivieren**. Obwohl dieser Ansatz einfacher ist, können bei seiner Verwendung andere Probleme auftreten, da einige EB-Funktionen nur unterstützt werden, wenn die **Die Nutzung der EPPlus-Bibliothek im Rahmen der elektronischen Berichterstellung aktivieren**-Funktion aktiviert ist.
- **Empfohlen:** Führen Sie die folgenden Schritte aus:

    1. Ändern Sie in der Excel-Desktop-Anwendung die Excel-Arbeitsmappe auf eine der folgenden Weisen:

        - Haben Sie Auf Arbeitsblatt **Blatt1** die Zusammenführung der Zellen **A1** und **A2** auf.
        - Ändern Sie die Referenz für den **ReportTitle**-Namen von **=Sheet1!$A$2** auf **=Sheet1!$A$1**.

        ![Überprüfen der Ergebnisse der Änderung der Referenz in der designierten Excel-Arbeitsmappe in der Excel-Desktop-Anwendung.](./media/er-fillable-excel-example2-3.png)

    2. Auf der **Formatdesigner**-Seite die modifizierte Excel-Arbeitsmappe in das bearbeitbare EB-Format [importieren](er-fillable-excel.md#template-import), um die vorhandene Vorlage zu aktualisieren.
    3. Führen Sie das geänderte EB-Format aus.

        ![Überprüfen des generierten Excel-Dokuments in der Excel-Desktop-Anwendung.](./media/er-fillable-excel-example2-4.png)

## <a name="limitations"></a>Einschränkungen

### <a name="known-epplus-library-limitations"></a>Bekannte Einschränkungen der EPPlus Bibliothek

#### <a name="external-data-sources"></a>Externe Datenquellen

Wenn eine Ihrer Vorlagen eine PivotTable enthält, die auf einem PowerPivot-Modell basiert, das auf eine [externe Datenquelle](https://support.microsoft.com/office/create-a-pivottable-with-an-external-data-source-db50d01d-2e1c-43bd-bfb5-b76a818a927b) verweist, und die Funktion **Verwendung der EPPlus-Bibliothek im Electronic Reporting Framework aktivieren** aktiviert ist, erhalten Sie die folgende Fehlermeldung, wenn Sie ein ER-Format ausführen, das diese Vorlage verwendet, um einen ausgehenden Beleg im Excel-Format zu erzeugen: „The cachesource is not a worksheet“. Um dieses Problem zu beheben, haben Sie die folgenden Möglichkeiten:

- **Empfohlen:** Überarbeiten Sie die Excel-Lösung, die Sie verwenden:

    1. Isolieren Sie den Teil, der Pivots enthält, in einer separaten Excel-Arbeitsmappe (Arbeitsmappe A). 
    2. Verwenden Sie ER, um eine zweite Excel-Arbeitsmappe (Arbeitsmappe B) aus Finance zu erstellen, die die erforderlichen Details enthält. 
    3. Verweisen Sie in Arbeitsmappe A auf Arbeitsmappe B, sobald Arbeitsmappe B erstellt wird.

- Deaktivieren Sie die Funktion **Die Nutzung der EPPlus-Bibliothek im Rahmen der elektronische Berichterstellung aktivieren**, um eine andere Option als EPPlus zu verwenden. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Eine Konfiguration zum Generieren von Berichten im OpenXML-Format entwerfen](tasks\er-design-reports-openxml-2016-11.md)

[Ändern von elektronisches Berichterstellungsformaten, indem Excel-Vorlagen erneut angewendet werden](modify-electronic-reporting-format-reapply-excel-template.md)

[Horizontal erweiterbare Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten verwenden](tasks/er-horizontal-1.md)

[Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von ER](electronic-reporting-embed-images-shapes.md)

[Konfigurieren Sie die elektronische Berichterstattung (ER), um Daten in Power BI zu ziehen.](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
