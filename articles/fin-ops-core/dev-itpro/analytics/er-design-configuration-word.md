---
title: EB-Konfigurationen zur Anfertigung von Berichten im Word-Format entwerfen
description: In diesem Artikel wird erläutert, wie Benutzer ein neues EB-Format (elektronische Berichterstellung) konfigurieren können, um Berichte als Microsoft Word-Dokumente zu generieren.
author: kfend
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.search.form:
- ERWorkspace, ERSolutionTable, EROperationDesigner
- LedgerJournalTable, LedgerJournalTransVendPaym
ms.openlocfilehash: b56b328aa2a2b53dc177a02a4d453e5dbcb8340c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273337"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Eine neue EB-Konfiguration zum Generieren von Berichten im Word-Format erstellen

[!include [banner](../includes/banner.md)]

Um Berichte als Microsoft Word-Dokumente zu generieren, müssen Sie eine Vorlage für die Berichte entwerfen, indem Sie beispielsweise die Word-Desktopanwendung verwenden. Die folgende Abbildung zeigt die Beispielvorlage für den Kontrollbericht, der generiert werden kann, um Details zu verarbeiteten Lieferantenzahlungen anzuzeigen.

![Beispielvorlage für den Kontrollbericht in der Word-Desktopanwendung.](./media/er-design-configuration-word-image1.png)

Um ein Word-Dokument als Vorlage für Berichte im Word-Format zu verwenden, können Sie eine neue [EB-](general-electronic-reporting.md)[Lösung](er-quick-start1-new-solution.md) (elektronische Berichterstellung) konfigurieren. Diese Lösung muss eine EB-[Konfiguration](general-electronic-reporting.md#Configuration) enthalten, die eine Komponente im EB-Format aufweist.

> [!NOTE]
> Wenn Sie eine neue Konfiguration im EB-Format erstellen, um Berichte im Word-Format zu generieren, müssen Sie entweder **Word** als Formattyp im Dropdown-Dialogfeld **Konfiguration erstellen** auswählen oder das Feld **Formattyp** leer lassen.

![Eine Formatkonfiguration auf der Konfigurationsseite erstellen.](./media/er-design-configuration-word-image2.gif)

Die EB-Formatkomponente der Lösung muss das Formatelement **Excel\\Datei** enthalten, und dieses Formatelement muss mit dem Word-Dokument verknüpft sein, das zur Laufzeit als Vorlage für generierte Berichte verwendet wird. Um die EB-Formatkomponente zu konfigurieren, müssen Sie die Entwurfsversion der erstellten EB-Konfiguration im EB-Format-Designer öffnen. Dann fügen Sie das Element **Excel\\Datei** hinzu, hängen Ihre Word-Vorlage an das bearbeitbare EB-Format an, und verknüpfen diese Vorlage mit dem Element **Excel\\Datei**, das Sie hinzugefügt haben.

> [!NOTE]
> Wenn Sie eine Vorlage manuell anhängen, müssen Sie einen [Dokumenttyp](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) verwenden, der zuvor in den EB-Parametern zum Speichern von Vorlagen von EB-Formaten [konfiguriert](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) wurde.

![Anhängen einer Vorlage auf der Seite „Formatdesigner“.](./media/er-design-configuration-word-image3.gif)

Sie können verschachtelte **Excel\\Bereich**- und **Excel\\Zelle**-Elemente für das Element **Excel\\Datei** hinzufügen, um die Struktur von Daten anzugeben, die zur Laufzeit in generierte Berichte eingegeben werden. Anschließend müssen Sie diese Elemente an Datenquellen im bearbeitbaren EB-Format binden, um die tatsächlichen Daten anzugeben, die zur Laufzeit in generierte Berichte eingegeben werden.

![Hinzufügen der verschachtelten Elemente auf der Seite „Formatdesigner“.](./media/er-design-configuration-word-image4.gif)

Wenn Sie Ihre Änderungen am EB-Format zur Entwurfszeit speichern, wird die hierarchische Formatstruktur in der angehängten Word-Vorlage als [benutzerdefinierter XML-Teil](/visualstudio/vsto/custom-xml-parts-overview) gespeichert, der **Bericht** heißt. Sie müssen auf die geänderte Vorlage zugreifen, sie von Finance herunterladen, lokal speichern und in der Word-Desktopanwendung öffnen. Die folgende Abbildung zeigt die lokal gespeicherte Beispielvorlage für den Kontrollbericht, der den benutzerdefinierten XML-Teil **Bericht** enthält.

![Anzeige der Beispielberichtsvorlage in der Word-Desktopanwendung.](./media/er-design-configuration-word-image5.gif)

Wenn Bindungen der Formatelemente **Excel\\Bereich** und **Excel\\Zelle** zur Laufzeit ausgeführt werden, werden die Daten, die jede Bindung liefert, als einzelnes Feld des benutzerdefinierten XML-Teils **Berichts** in das generierte Word-Dokument eingegeben. Um die Werte aus den Feldern des benutzerdefinierten XML-Teils in ein generiertes Dokument einzugeben, müssen Sie die entsprechenden Word-[Inhaltssteuerelemente](/office/client-developer/word/content-controls-in-word) zu Ihrer Word-Vorlage hinzufügen, um als Platzhalter für Daten zu dienen, die zur Laufzeit aufgefüllt werden. Um festzulegen, wie Inhaltssteuerelemente ausgefüllt werden, ordnen Sie jedes Inhaltssteuerelement dem entsprechenden Feld des benutzerdefinierten XML-Teils **Bericht** zu.

![Hinzufügen und Zuordnen von Inhaltssteuerelementen in der Word-Desktopanwendung.](./media/er-design-configuration-word-image6.gif)

Anschließend müssen Sie die ursprüngliche Word-Vorlage des bearbeitbaren ER-Formats durch die geänderte Vorlage ersetzen, die jetzt Word-Inhaltssteuerelemente enthält, die den Feldern des benutzerdefinierten XML-Teils **Bericht** zugeordnet wurden.

![Ersetzen der Vorlage auf der Seite „Formatdesigner“.](./media/er-design-configuration-word-image7.gif)

Wenn Sie das konfigurierte EB-Format ausführen, wird die angehängte Word-Vorlage verwendet, um einen neuen Bericht zu erstellen. Die tatsächlichen Daten werden im Word-Bericht als benutzerdefinierter XML-Teil mit dem Namen **Bericht** gespeichert. Wenn der generierte Bericht geöffnet wird, werden die Steuerelemente für den Word-Inhalt mit Daten aus dem benutzerdefinierten XML-Teil **Bericht** ausgefüllt.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Frage:** Ich habe ein EB-Format konfiguriert, um ein Word-Dokument zu drucken, das eine Firmenadresse enthält. In die Word-Vorlage für dieses EB-Format habe ich ein Rich-Text-Inhaltssteuerelement eingefügt, um eine Firmenadresse darzustellen. In Finance habe ich die Firmenadresse als mehrzeiligen Text eingegeben und **Eingeben** ausgewählt, um für jede von mir eingegebene Zeile einen Wagenrücklauf hinzuzufügen. Daher erwarte ich, dass die Firmenadresse in generierten Dokumenten als mehrzeiliger Text angezeigt wird. Die Adresse wird jedoch als einzelne Textzeile angezeigt, die anstelle von Zeilenumbrüchen spezielle Symbole enthält. Was ist in meinen Einstellungen falsch?

**Antwort:** Anstatt ein Rich-Text-Inhaltssteuerelement zu verwenden, müssen Sie ein Nur-Text-Inhaltssteuerelement verwenden und das Kontrollkästchen **Wagenrückläufe zulassen (mehrere Absätze)** in den Eigenschaften des Steuerelements aktivieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [EB-Konfigurationen mit Excel-Vorlagen wiederverwenden, um Berichte im Word-Format zu erstellen](./tasks/er-design-configuration-word-2016-11.md)
- [Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von ER](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
