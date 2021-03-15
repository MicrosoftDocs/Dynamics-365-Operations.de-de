---
title: Entwerfen von EB-Konfigurationen, um Zeichen von Bytereihenfolge-Marken in generierten Dateien zu unterdrücken
description: In diesem Thema wird erläutert, wie Sie ein EB-Format (elektronische Berichterstellung) konfigurieren, um Berichte zu generieren, die Zeichen von Bytereihenfolge-Marken unterdrücken.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19fbbdea4bfdf30b1313a47e65056b536ed73dbe
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060818"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>Entwerfen von EB-Konfigurationen, um Zeichen von Bytereihenfolge-Marken in generierten Dateien zu unterdrücken

[!include [banner](../includes/banner.md)]

Sie können eine [EB-](general-electronic-reporting.md)[Lösung](er-quick-start1-new-solution.md) entwerfen, um ausgehende Dokumente zu generieren. Um die Dokumente als Text- oder XML-Dateien zu generieren, muss die Lösung eine EB-[Konfiguration](general-electronic-reporting.md#Configuration) enthalten, die eine EB-[Format-](general-electronic-reporting.md#FormatComponentOutbound)-Komponente enthält. Um die [Zeichencodierung](https://docs.microsoft.com/windows/win32/intl/character-sets) anzugeben, die den Zeichensatz in generierten Dateien darstellt, muss das EB-Format das Formatelement **Allgemein\\Datei** enthalten. Um die EB-Formatkomponente zu konfigurieren, öffnen Sie die [Entwurfs](general-electronic-reporting.md#component-versioning)version der erstellten EB-Konfiguration im EB-Format-Designer, und fügen Sie das Element **Allgemein\\Datei** hinzu. Geben Sie im Feld **Codierung** die Codierung ausgehender Dateien an, die zur Laufzeit mithilfe dieser Komponente generiert werden.

> [!NOTE]
> Wenn das Format einen falschen Codierungsnamen enthält, wird ein Fehler ausgegeben, wenn Sie Ihre Änderungen an den Einstellungen des Formats speichern.

![Hinzufügen eines Stammelements auf der Seite „Formatdesigner“](./media/er-suppress-bom-characters-image1.gif)

Wenn Sie **UTF-8**, **UTF-16** oder **UTF-32** als Codierung angeben, wird die Option **Zeichen von Bytereihenfolge-Marken unterdrücken** verfügbar. Setzen Sie diese Option auf **Ja**, um [Zeichen von Bytereihenfolge-Marken](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in ausgehenden Dateien zu unterdrücken, die zur Laufzeit generiert werden, wenn das bearbeitbare ER-Format ausgeführt wird.

> [!NOTE]
> Wenn Sie das Feld **Codierung** leer lassen, wird die Standardcodierung **UTF-8** verwendet.

![Festlegen der Option „Zeichen von Bytereihenfolge-Marken unterdrücken“ auf der Seite „Format-Designer“](./media/er-suppress-bom-characters-image2.gif)

Führen Sie die entsprechenden Schritte aus, um die Funktionalität zur Laufzeit zu überprüfen. Führen Sie beispielsweise die Schritte im Thema [Ausführung von XML-Elementen in ER-Formaten verzögern](er-defer-xml-element.md) aus. Nachdem Sie die Schritte im Abschnitt [Ändern des Formats, sodass die Berechnung auf der generierten Ausgabe basiert](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) dieses Themas abgeschlossen haben, befolgen Sie diese zusätzlichen Schritte.

1. Geben Sie die UTF-Codierung an:

    1. Wählen Sie das Element **Bericht** des Typs **Allgemein\\Datei** aus.
    2. Geben Sie im Feld **Codierung** die **UTF-8**-Codierung an.

2. Generieren Sie eine XML-Datei mit einem Zeichen von Bytereihenfolge-Marken:

    1. Stellen Sie die Option **Zeichen von Bytereihenfolge-Marken unterdrücken** auf **Nein**, Zeichen von Bytereihenfolge-Marken in generierte XML-Dateien aufzunehmen.
    2. Führen Sie die Schritte im Abschnitt [Verzögern der Ausführung des XML-Elements „Zusammenfassung“, sodass die berechnete Gesamtsumme verwendet wird](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) des Themas [Ausführung von XML-Elementen in ER-Formaten verzögern](er-defer-xml-element.md), und speichern Sie die generierte Datei als **SampleXmlReport.xml**.

3. Generieren Sie eine XML-Datei, die kein Zeichen von Bytereihenfolge-Marken enthält:

    1. Stellen Sie die Option **Zeichen von Bytereihenfolge-Marken unterdrücken** auf **Ja**, um Zeichen von Bytereihenfolge-Marken in generierten XML-Dateien zu unterdrücken.
    2. Führen Sie die Schritte im Abschnitt [Verzögern der Ausführung des XML-Elements „Zusammenfassung“, sodass die berechnete Gesamtsumme verwendet wird](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) des Themas [Ausführung von XML-Elementen in ER-Formaten verzögern](er-defer-xml-element.md) aus, und speichern Sie die generierte Datei als **SampleXmlReport (1).xml**.

4. Vergleichen Sie in einem Dienstprogramm zum Dateivergleich die generierten Dateien.

    Der erste Unterschied, den Sie bemerken werden, liegt in der Dateikopfzeile. Die Datei „SampleXmlReport.xml“ enthält ein Zeichen von Bytereihenfolge-Marke, die Datei „SampleXmlReport(1).xml“ nicht.

    ![Vergleichen der generierten Dateien in einem Dienstprogramm zum Dateivergleich](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Siehe auch

- [Ausführung von XML-Elementen in ER-Formaten verzögern](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]