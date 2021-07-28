---
title: Zeilendefinitionen im Finanzberichtdesigner
description: Eine Zeilendefinition ist eine Berichtkomponente oder ein Baustein, die den Inhalt jeder Zeile eines Finanzberichts angibt.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e84f882f69fbc7fceae8a6e0332716a82830dfdc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344047"
---
# <a name="row-definitions-in-financial-report-designer"></a>Zeilendefinitionen im Finanzberichtdesigner

[!include [banner](../includes/banner.md)]

Eine Zeilendefinition ist eine Berichtkomponente oder ein Baustein, die den Inhalt jeder Zeile eines Finanzberichts angibt. Zeilendefinitionen können mit Spaltendefinitionen, Berichtsstruktur-Definitionen und Berichtsdefinitionen kombiniert werden, um eine Bausteingruppe zu erstellen, die von mehreren Unternehmen verwendet werden kann.

## <a name="create-a-row-definition"></a>Erstellen einer Zeilendefinition

1. Klicken Sie im Berichts-Designer im Navigationsbereich auf **Zeilendefinitionen** .
2. Wählen Sie im Menü **Datei** die Option **Neu**, und klicken Sie dann auf **Zeilendefinitionen**. Weitere Informationen zum Inhalt jeder Zelle finden Sie unter [Zeilendefinitionszellen ändern](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Öffnen Sie eine Zeilendefinition.
1. Klicken Sie im Berichts-Designer im Navigationsbereich auf **Zeilendefinitionen** .
2. Doppelklicken Sie auf den Namen der Zeilendefinition.
3. Um alle Bausteine anzuzeigen, die der Zeilendefinition zugeordnet sind, klicken Sie mit der rechten Maustaste auf die Zeilendefinition, und wählen Sie dann **Zuordnungen** aus.

## <a name="contents-of-a-row-definition"></a>Inhalt einer Zeilendefinition
Eine Zeilendefinition kann bis zu 20,000 Finanzdimensionszeilen und die folgenden Informationen enthalten:

- Beschreibender Text, der dem Bericht Bedeutung verleiht, indem Abschnittsüberschriften, Positionen und Leerzeichen hinzugefügt werden, wie z. B. **Bargeld** oder **Gesamtumsatz**
- Links zu Finanzdaten, die Dimensionswerte in Microsoft Dynamics 365 Finance enthalten können

    > [!NOTE]
    > Sie können eine Zeilendefinition so einrichten, dass bei jeder Berichtsgenerierung Daten aus dem Finanzdimensionssystem abgerufen werden.

- Zeilensummen und -formeln, die auf den verknüpften Finanzdaten basieren

Normalerweise enthält jede Zeile in einer Zeilendefinition eine der folgenden Arten von Informationen:

- Verweise auf das Finanzdimensionssystem
- Summen oder Berechnungen basierend auf den Daten
- Formatierung

Es gibt zwei Methoden zur Eingabe von Informationen in einer Zeilendefinition:

- Geben Sie Zeileninformationen manuell in die neue Zeilendefinition ein. Weitere Informationen finden Sie unter [Ändern von Zeilendefinitionszellen](modify-row-definition-cells-financial-reporting.md).
- Verwenden Sie den Berichts-Designer, um Zeileninformationen direkt aus den Finanzdimensionen abzurufen. Weitere Informationen finden Sie im Abschnitt "Verwandte Formeln/Zeilen/Einheiten" in [Ändern von Zeilendefinitionszellen](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a>Hinzufügen einer Dimensionen zu einer Zeilendefinizion
Eine Dimension stellt eine Schnittstelle von Daten und Werten dar. Sie können Daten und Werte im Berichtsdesigner gruppieren. Sie können dann Transaktionen klassifizieren und genauer analysieren. Sie können das **Dimensionen aus Zeilen einfügen**- Dialogfeld verwenden, um gleichzeitig mehrere Zeilen einer Zeilendefinition hinzuzufügen. Im Dialogfeld wird eine Spalte für jede Dimension angezeigt. In der folgenden Tabelle werden Informationen beschrieben, die Sie für die einzelnen Dimensionen angeben können.

| Mit der folgenden Option...                | Beschreibung |
|-----------------------|-------------|
| Dimensionen             | Das Muster, das die Dimension identifiziert, die der Zeilendefinition hinzugefügt wird. Dieses Muster enthält ein kaufmännisches Und-Zeichen (\#) oder Nummernzeichen (#) für jede Position in den Dimensionen. Verwenden Sie im Allgemeinen immer kaufmännische Und-Zeichen für die Kontodimension und immer Nummernzeichen für andere Dimensionen. |
| Anfang des Dimensionsbereichs | Der erste Wert für diese Dimension, der der Zeilendefinition hinzugefügt werden soll. |
| Ende des Dimensionsbereichs   | Der letzte Wert, der von dieser Dimension der Zeilendefinition hinzugefügt wird. |

Um Dimensionen einer Zeilendefinition hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Klicken Sie im Berichts-Designer auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Klicken Sie im Menü **Bearbeiten** auf **Zeilen aus Dimensionen einfügen**...
3. Wählen Sie im Dialogfeld **Zeilen aus Dimensionen einfügen** in der Zeile **Dimensionen** die Zelle aus, damit die Dimension der Zeilendefinition übertragen werden kann, und klicken Sie anschließend auf **Alle &&&**.
4. Um die Zeilendefinition auf einen bestimmten Bereich von Dimensionswerten einzuschränken, geben Sie den Dimensionsstartwert in der Zelle **Dimensionsbereichsanfang** ein, und geben Sie dann den Enddimensionswert in der Zelle **Dimensionssbereichsende** ein. Wenn Sie alle Werte für die ausgewählte Dimension einschließen möchten, lassen Sie diese Zellen leer.

    > [!NOTE]
    > Wenn Sie Platzhalterzeichen (\* oder ?) zur Angabe von Dimensionsbereichen verwenden, werden möglicherweise nicht alle gewünschten Ergebnisse zurückgegeben. Dies hängt von der Sortierung der Daten in der ERP-Datenbank ab.

5. Wählen Sie einen Wert im Feld **Anfangszeilencode** aus, um den Zeilencode für den ersten Dimensionswert anzugeben, der der Zeilendefinition hinzugefügt wird.
6. Geben Sie im Feld **Jede Zeile inkrementieren um** die Lücke zwischen aufeinanderfolgenden Zeilencodes an. Wenn beispielsweise der erste Zeilencode ist 100, und der Inkrementwert ist 30, die ersten neuen Zeilen weisen die Codes 100,130,160,190 und 220. Verwenden Sie einen Inkrementwert, der genügend Platz enthält, der Anwerbung neuer Format- und Formelzeilen einzufügen.
7. Klicken Sie auf **OK**. Für jeden der ausgewählten Dimensionswerte wird der Zeilendefinition eine Position hinzugefügt.

## <a name="adjust-rounding-in-a-row-definition"></a>Anpassen der Rundung in einer Zeilendefinition
Wenn Sie eine Bilanz haben, in der die Beträge gerundet werden, sind die Summen ggf. nicht gleich. Dieses Problem kann auftreten, wenn Sie beispielsweise die Rundungsoption in einem Bilanzbericht verwenden und die Berichtsdefinition ebenfalls Rundung angibt. Verwenden Sie die Option **Rundungsregulierung** in der Zeilendefinition, um die Beträge in der Bilanz auszugleichen. Sie können Rundung auf der Registerkarte **Einstellungen** der Berichtsdefinition deaktivieren oder ändern. Die folgende Tabelle zeigt, wie Beträge gerundet werden. In dieser Tabelle weichen die Summen der Zeilen 100 und 200 ab, wenn "Runden" aktiviert ist.

| Zeilencode | Nicht gerundete Beträge | Auf ganze Tausend gerundeter Betrag |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Summe    | 7,300                    | 8                                       |

Um Rundung in einer Bilanz anzupassen, führen Sie die folgenden Schritte aus.

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Klicken Sie im Menü **Bearbeiten** auf **Rundungsausgleich**.
3. Im Dialogfeld **Rundungsregulierungen** können Sie die folgenden Werte eingeben:

    - **Rundungsausgleichszeile** - Der Zeilencode für die Zeile, die angepasst werden soll, um die Bilanz auszugleichen.
    - **Anlagensummenzeile** - Der Zeilencode für die Zeile in der Bilanz, die die Anlagesummen beinhaltet.
    - **Summenzeile der Verbindlichkeiten und des Eigenkapitals** - Der Zeilencode für die Zeile in der Bilanz, die die Summe der Verbindlichkeiten und des Eigenkapitals beinhaltet.
    - **Ausgleichsbetraggrenze** - Eine positive Ganzzahl, die bei automatischen Regulierungen die Grenze angibt. Dieser Betrag wird mit dem absoluten Wert der tatsächlichen Rundungsdifferenz verglichen.

    > [!NOTE]
    > Diese Zeilencodes müssen direkt mit den Finanzdaten verknüpft werden. In der Zelle **Verknüpfen mit Finanzdatenquelle** muss sich also ein Segment- oder Dimensionswert befinden. Verweisen Sie **keine** Beschreibungs- (**DESC**) , Berechnet- (**CALC**) oder Gesamt- (**KNIRPS**) zeile.

Die Beträge in der Bilanz werden jetzt gleichmäßig ausgeglichen, wenn Runden aktiviert ist.

> [!NOTE]
> Die Regulierungsgrenze auf Grundlage der Option an, die für die Berichtsdefinition unter **Rundungsgenauigkeit** angegeben ist. Wenn Sie beispielsweise Ihren Bericht auf Tausend runden und **2** im Feld **Ausgleichsbetraggrenze** eingeben, wird eine Warnmeldung angezeigt, wenn der Wert im Feld **Rundungsausgleichszeile** um mehr als 2.000 Dollar steigt oder reduziert wird.

## <a name="format-row-and-column-text"></a>Formatieren von Zeilen- und Spaltentext
Sie können die Darstellung Ihrer Berichte anpassen, indem Sie Schriftarten ändern und Text formatieren. In den folgenden Abschnitten wird erklärt, wie die Darstellung der Zeilen und der Spalten in Berichten formatiert wird.

### <a name="manage-font-styles"></a>Verwalten von Schriftschnitten

Sie können Schriftarten für Ihren Bericht erstellen und ändern. Sie können diese Stile dann auf das Dokument, eine bestimmten Zeile oder Spalte in einem Bericht anwenden.

<table>
<tbody>
<tr>
<td><strong>Erstellen eines Schriftschnitts</strong></td>
<td>
<ol>
<li>Im Berichts-Designer im Menü <strong>Format</strong> klicken Sie auf <strong>Formate und Formatierung</strong>.</li>
<li>Klicken Sie im Dialogfeld <strong>Formatvorlagen und Formatierung</strong> auf <strong>Neu</strong>, und geben Sie einen eindeutigen Namen für den neuen Stil ein.</li>
<li>Wählen Sie die gewünschten Schriftoptionen aus, und klicken Sie dann auf <strong>OK</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Ändern eines Schriftschnitts</strong></td>
<td>
<ol>
<li>Im Berichts-Designer im Menü <strong>Format</strong> klicken Sie auf <strong>Formate und Formatierung</strong>.</li>
<li>Wählen Sie im Dialogfeld <strong>Formatvorlagen und Formatierung</strong> eine zu ändernde Formatvorlage aus, und klicken Sie dann auf <strong>Ändern</strong>.</li>
<li>Wählen Sie die gewünschten Schriftoptionen aus, und klicken Sie dann auf <strong>OK</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Anwenden eines Schriftschnitts</strong></td>
<td>
<ol>
<li>Wählen Sie im Berichts-Designer eine oder mehrere Zellen in einer Definition, einer Spaltendefinition oder in den Kopf- und Fußzeilen aus.</li>
<li>Wählen Sie auf der Symbolleiste in der Liste <strong>Formatvorlage</strong> einen Schriftschnitt aus.</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Formatieren von Zeilentext

Die Formatierung, die in der Zeilendefinition angegeben wird, überschreibt jede Formatierung, die in der Spaltendefinition und der Berichtsdefinition angegeben ist. Sie können das Textformat mit den Steuerelementen auf der Formatierungssymbolleiste ändern. Diese Steuerelemente sind Microsoft Windows-Standardsteuerelemente.

1. Öffnen Sie im Berichts-Designer die zu bearbeitende Zeilendefinition.
2. Wählen Sie die Zellen aus, die formatiert werden sollen. Um mehrere Zellen auszuwählen, halten Sie die STRG-Taste gedrückt, während Sie die Zelle auswählen.
3. Klicken Sie auf die Symbolleistenschaltfläche des Formats, das übernommen werden soll. Um beispielsweise eine Zeile einzurücken, wählen Sie die Zeile aus und klicken Sie anschließend auf **Einrückung erhöhen** ![Einrückung erhöhen](media/indent.gif "Einzug vergrößern") auf der Symbolleiste.

### <a name="adjust-columns-while-you-design-reports"></a>Anpassen der Spalten, während des Berichtentwurfs

Um die Ansicht der Spalten, an denen Sie in der Zeilendefinition arbeiten, zu vereinfachen, können Sie die Breite einer Spalte anpassen und Spalten im Ansichtsbereich ausblenden (minimieren) oder anzeigen. Änderungen, die Sie vornehmen, betreffen nur die Bildschirmdarstellung der Spalten. Sie betreffen nicht die Spaltenformatierung eines Berichts.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Ändern der Breite einer Spalte im Ansichtsbereich

1. Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2. Wählen Sie im Menü **Format** die Option **Spaltenbreite**.
3. Geben Sie im Dialogfeld **Spaltenbreite** einen Wert ein, und klicken Sie anschließend auf **OK**. Alternativ können Sie die rechte Begrenzung einer Spaltenüberschriftszelle ziehen, um die Spaltenbreite zu ändern.

### <a name="hide-columns-in-the-view-pane"></a>Ausblenden von Spalten im Ansichtsbereich

1. Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2. Wählen Sie die Spalte oder Spalten aus, die Sie minimieren möchten.
3. Klicken Sie mit der rechten Maustaste, und klicken Sie dann auf **Ausblenden**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Anzeigen aller ausgeblendeten Spalten im Ansichtsbereich

1. Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2. Klicken Sie mit der rechten Maustaste auf die minimierte Spalte, die Sie anzeigen möchten, und klicken Sie anschließend auf **Einblenden**.


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Finanzberichterstellung](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]