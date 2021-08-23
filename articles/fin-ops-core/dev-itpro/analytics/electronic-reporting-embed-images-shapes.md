---
title: Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von ER
description: In diesem Thema wird erläutert, wie Sie mithilfe des elektronischen Berichterstellungstools (EB) Geschäftsdokumente mit eingebetteten Bildern und Formen generieren.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550ecca31af48e624e292b342d909abd6eb3e87af122f736eb388524b42f1e05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730634"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von ER

[!include [banner](../includes/banner.md)]

Sie können das elektronische Berichterstellungstool (EB) verwenden, um Berichte zu entwerfen, die Sie ausführen können, um erforderliche elektronische Dokumente zu generieren. Sie können Microsoft Excel- oder Microsoft Word-Dokumente verwenden, um das Layout eines Berichts festzulegen. Mit dem EB-Vorgangsdesigner können Sie das Excel- oder Word-Dokument als Vorlage für den Bericht anhängen. Die benannten Elemente in der angehängten Vorlage sind den Formatelementen des EB-Berichts zugeordnet: Formatelemente des Berichts sind an Datenquellen gebunden. Diese Elemente geben die Daten an, die zur Laufzeit in die generierten Dokumente eingegeben werden.

Diese neue Funktionalität geht über die bestehenden EB-Funktionen zum Erstellen von Dokumenten in Microsoft Office-Formaten hinaus. Weitere Informationen finden Sie in folgenden Aufgabenleitfäden: Sie finden diese Aufgabenleitfäden unter dem Geschäftsprozess „7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)“.

- ER Entwerfen einer Konfiguration für das Erstellen von Berichten im OPENXML-Format
- Eine EB-Konfigurationen zum Generieren von Berichten im Microsoft Word-Format erstellen

## <a name="embed-an-image-in-an-excel-document"></a>Ein Bild in ein Excel-Dokument einbetten

### <a name="embed-an-image-in-an-excel-worksheet"></a>Ein Bild in ein Excel-Arbeitsblatt einbetten

Zuerst müssen Sie einen Platzhalter für das Bild in einem Excel-Dokument hinzufügen. Öffnen Sie eine Excel-Arbeitsmappe, und fügen Sie ein Bild als Platzhalter für das Bild hinzu, das Sie später hinzufügen. Verwenden Sie dann das EB-Tool, um eine neue EB-Formatkonfiguration hinzuzufügen, um den von Ihnen entworfenen Bericht aufzunehmen. Hängen Sie die Excel-Arbeitsmappe als Vorlage für das Format des Berichts an und importieren Sie dann den Inhalt der Arbeitsmappe in das EB-Format. Die Formatdefinition wird automatisch erstellt. Der von Ihnen hinzugefügte Bildplatzhalter wird in die EB-Formatdefinition als ein **ZELLEN**-Element aufgenommen.

> [!NOTE]
> Sie können die Formatdefinition manuell festlegen, anstatt sie zu importieren. Wenn Sie Ihre Änderungen speichern, wird das Format überprüft.

Als Nächstes binden Sie das **ZELLEN**-Element des EB-Formats in das Feld aus der Datenquelle des Formats ein, das die Bilddaten zur Runtime im Binärformat bereitstellt. Wenn ein EB-Datenmodell als Datenquelle eines Formats verwendet wird, muss der Datentyp des Felds [Container](er-formula-supported-data-types-composite.md#container) lauten. Derzeit kann ein EB-Datenmodellfeld mit dem Datentyp [Container](er-formula-supported-data-types-composite.md#container) an verschiedene Datenquellentypen gebunden werden, die Bilder im Binärformat zurückgeben. Sie können auf ein Feld in einer Datentabelle und eine Datei zugreifen, die an den Datensatz der Datentabelle angehängt ist, indem Sie das Dokumentverwaltungs-Framework verwenden.

> [!IMPORTANT]
> - Wenn Sie den Bildplatzhalter in dem Dokument füllen möchten, den Sie mithilfe der Excel-Vorlage erstellen, muss das EB-Format das **ZELLEN**-Element enthalten, das auf das benannte Bildelement in der Excel-Vorlage verweist. Sonst wird kein Bildplatzhalter in der Ausgabe des Berichts angezeigt. Wenn die Bindung von ein **ZELLEN**-Element zur Runtime keine Daten zurückgibt, zeigt das generierte Dokument den Bildplatzhalter aus der Vorlage. Um ein Bild in dem von Ihnen erstellten Dokument auszublenden, definieren Sie ein **ZELLEN**-Element und geben Sie an, dass der Ausdruck **Aktivieren** den Wert **FALSCH** zurückgeben soll.
> - Verwenden Sie in der Excel-Vorlage für jedes Element einen eindeutigen Namen. Zu diesen Elementen gehören auch Bilder und Zellen. Wenn Sie einen Elementnamen doppelt verwenden, wird der Inhalt des generierten Berichts mehrdeutig und verwirrend.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Bilder in die Kopf- und Fußzeile eines Excel-Arbeitsblatts einbetten

Verwenden Sie das Excel-Arbeitsmappendokument als Vorlage, um das Layout eines Berichts anzugeben. Die Arbeitsmappe kann mehrere Arbeitsblätter enthalten, von denen jedes so eingerichtet werden kann, dass es eine Kopf- und eine Fußzeile hat. Excel unterstützt bis zu drei Bilder in der Kopf- und Fußzeile jedes Arbeitsblatts. Die Bilder können links, rechts oder mittig ausgerichtet werden.

In der Finance-Release 10.0.21 können Sie die Kopf- und Fußzeilenbilder verwalten, die von einer EB-Lösung mit einer Excel-Vorlage generiert werden.

Wenn in der Kopf- oder Fußzeile eines generierten Dokuments ein Standardbild angezeigt werden soll, können Sie der Kopf- oder Fußzeile eines Arbeitsblatts einer EB-Vorlage ein Bild hinzufügen. Um auf dieses Bild in Ihrem EB-Format zuzugreifen, müssen Sie die Komponente **Bild** unter der Komponente [Kopfzeile](er-fillable-excel.md#header-component) oder [Fußzeile](er-fillable-excel.md#footer-component) des Formats hinzufügen. Konfigurieren Sie die Ausrichtung der Komponente **Bild** entsprechend. 

Sie können auch die Komponente **Bild** verwenden, um zur Runtime ein Bild in die Kopf- oder Fußzeile eines generierten Dokuments einzufügen, auch wenn die Vorlage kein Standardbild enthält. Um den Medieninhalt anzugeben, der entweder als neues Bild oder als Ersatz für ein Standardbild in die Kopf- oder Fußzeile eines generierten Dokuments eingefügt werden soll, müssen Sie die Komponente **Bild** an eine Datenquelle vom Typ [Container](er-formula-supported-data-types-composite.md#container) binden, der ein Bild im Binärformat darstellt.

Jede **Kopfzeilen**- oder **Fußzeilen**-Komponente kann eine **Bild**-Komponente für jede unterstützte Ausrichtung enthalten: **Links**, **Mitte** und **Rechts**.

Mit der Eigenschaft **Höhe skalieren** der Komponente **Bild** können Sie die konfigurierte Bindung verwenden, um die Größe eines Bildes zu steuern:

- Wählen Sie **Original**, um die ursprüngliche Größe des Bildes beizubehalten.
- Wählen Sie **Relativ**, um die Höhe des Bildes proportional zur Höhe der Kopf- oder Fußzeile, die das Bild enthält, zu skalieren.

    - In diesem Fall muss die Höhe des Bildes als Prozentsatz der übergeordneten Kopf- oder Fußzeile definiert werden.
    - Wenn der Skalierungswert 100 % überschreitet, überlappt das Bild möglicherweise den Datenbereich des entsprechenden Arbeitsblatts.
    - Wenn die Höhe des Bildes beim Anwenden der Skalierung geändert wird, wird auch die Breite geändert, um das ursprüngliche Seitenverhältnis des Bildes beizubehalten.

- Wählen Sie **Absolut**, um die Größe des Bildes entsprechend den Höhen- und Breitenwerten (in Pixeln) zu ändern, die zur Entwurfszeit bereitgestellt werden.

    - Wenn die angegebene Höhe die Höhe der übergeordneten Kopf- oder Fußzeile überschreitet, überlappt das Bild möglicherweise den Datenbereich des entsprechenden Arbeitsblatts.

Sie können auch die Eigenschaft **Aktiviert** der Komponente **Bild** verwenden, um die Sichtbarkeit eines Bildes zu steuern, das mit dieser Komponente in ein generiertes Dokument eingefügt wird.

> [!NOTE]
> Sie müssen den EB-Formatdesigner verwenden, um eine Komponente **Bild** in das bearbeitbare EB-Format hinzuzufügen. Sie können die Komponente nicht hinzufügen, wenn Sie den Arbeitsbereich [Geschäftsdokumentverwaltung](er-business-document-management.md) verwenden, um die Vorlage eines Geschäftsdokuments zu bearbeiten.

Um mehr über diese Funktion zu erfahren, befolgen Sie die Schritte in [Ein EB-Format entwerfen, um einen Bericht im Excel-Format mit eingebetteten Bildern in den Kopf- oder Fußzeilen einer Seite zu erstellen](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Eine Form in ein Excel-Dokument einbetten

Zuerst müssen Sie einen Platzhalter für die Form in einem Excel-Dokument hinzufügen. Öffnen Sie eine Excel-Arbeitsmappe und wählen Sie **Form**, **Textfeld** oder **WordArt** als Platzhalter für die Form. Verwenden Sie dann das EB-Tool, um eine neue EB-Formatkonfiguration hinzuzufügen, um den von Ihnen entworfenen Bericht aufzunehmen. Hängen Sie die Excel-Arbeitsmappe als Vorlage für das Format des Berichts an und importieren Sie dann den Inhalt der Arbeitsmappe in das EB-Format. Die Formatdefinition wird automatisch erstellt. Der von Ihnen hinzugefügte Formplatzhalter wird in die EB-Formatdefinition als **ZELLEN**-Element aufgenommen, das auf das benannte Excel-Formelement verweist.

> [!NOTE]
> Sie können die Formatdefinition manuell festlegen, anstatt sie zu importieren. Wenn Sie Ihre Änderungen speichern, wird das Format überprüft.

Als Nächstes binden Sie das **ZELLEN**-Element in das EB-Format an das Feld aus der Datenquelle des Formats, das die Daten zur Runtime bereitstellt. Diese Daten können in eine Textzeichenfolge umgewandelt werden. Wenn das **ZELLEN**-Element im EB-Format auf ein Format-Element in der Excel-Vorlage verweist, das Text unterstützt, wird der Text, der über diese Bindung zur Runtime bereitgestellt wird, in einer Form im generierten Dokument angezeigt.

> [!IMPORTANT]
> - Wenn Sie die Excel-Vorlage verwenden möchten, die den Platzhalter für die Form enthält, um ein neues Dokument zu generieren, muss das EB-Format ein **ZELLEN**-Element enthalten, das auf das Excel-Formelement verweist. Sonst wird kein Formplatzhalter in der Ausgabe des Berichts angezeigt. Wenn die Bindung eines **ZELLEN**-Elements, das auf das benannte Excel-Formelement verweist, zur Runtime keine Daten zurückgibt, zeigt das generierte Dokument den Text des Formplatzhalters aus der Excel-Vorlage an. Um eine Form in dem von Ihnen erstellten Dokument auszublenden, definieren Sie ein **ZELLEN**-Element, das auf das benannte Excel-Formelement verweist, und geben Sie an, dass der Ausdruck **Aktivieren** den Wert **FALSCH** zurückgeben soll.
> - Verwenden Sie in der Excel-Vorlage für jedes Element einen eindeutigen Namen. Zu diesen Elementen gehören auch Formen und Zellen. Wenn Sie einen Elementnamen doppelt verwenden, wird der Inhalt des generierten Berichts mehrdeutig und verwirrend.

## <a name="embed-an-image-in-a-word-document"></a>Ein Bild in ein Word-Dokument einbetten
> [!IMPORTANT]
> Sie können das EB-Format wiederverwenden, das eine Excel-Vorlage verwendet, um Dokumente zu erstellen, die eingebettete Bilder enthalten. Stellen Sie im EB-Format sicher, dass ein Name für das **ZELLEN**-Element angegeben ist, das auf ein benanntes Bildelement in Excel verweist und an eine Datenquelle gebunden ist, die zur Runtime ein Bild zurückgibt.

Zuerst müssen Sie das Layout des Word-Dokuments konfigurieren. Verwenden Sie das Steuerelement **Bildinhalt**, um einen Platzhalter für das eingebettete Bild zu erstellen. Um auf dieses Steuerelement zugreifen zu können, müssen Sie zuerst die Registerkarte **Entwickler** in der Word-Menüband sichtbar.

Löschen Sie als Nächstes die Excel-Vorlage aus dem EB-Format und hängen Sie das Word-Vorlagendokument an. Aktualisieren Sie den Verweis auf die Vorlage und speichern Sie Ihre Änderungen. Die Struktur des gespeicherten AB-Formats wird der Word-Vorlage als neuer benutzerdefinierter XML-Abschnitt mit dem Namen **Bericht** angehängt.

Speichern Sie als Nächstes die Word-Vorlage für das aktuelle EB-Format auf Ihrem lokalen Computer. Öffnen Sie die Vorlage und öffnen Sie den Bereich **XML-Zuordnung**. Suchen Sie den benutzerdefinierten XML-Teil mit dem Namen **Bericht** und gehen Sie dann im EB-Bericht auf das **ZELLEN**-Element, das an eine Datenquelle gebunden ist, die ein Bild im Binärformat zurückgibt. Ordnen Sie das Element dieses XML-Teils dem ausgewählten Steuerelement **Bildinhalt** zu und speichern Sie Ihre Änderungen.

[![Bilder einbetten.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Löschen Sie abschließend die Word-Vorlage aus dem EB-Format und hängen Sie das Word-Dokument an, das die zugeordneten benutzerdefinierten XML-Teile enthält. Aktualisieren Sie den Formatverweis auf die Vorlage, und speichern Sie die Änderungen, die Sie an diesem EB-Format vorgenommen haben.

## <a name="more-information"></a>Weitere Informationen
Um sich mit den Details dieser Funktion vertraut zu machen, sehen Sie sich die Aufgabenleitfäden **EB – Berichte in MS Office-Formaten mit eingebettete Bildern erstellen** an. Diese Aufgabenleitfäden zeigen, wie Sie die Bilder eines Firmenlogos und der Unterschrift einer autorisierten Person in die Zahlungsschecks einbetten, die mit dem EB-Tool in Excel- und Word-Dokumenten generiert werden.

In der folgenden Tabelle sind die Dateien aufgeführt, die zur Erledigung des Aufgabenleitfäden **EB – Berichte in MS Office-Formaten mit eingebettete Bildern erstellen**. Laden Sie die Dateien auf Ihren lokalen Computer herunter und speichern Sie sie.

| Beschreibung                                          | Dateiname                   |
|------------------------------------------------------|-----------------------------|
| ER-Datenmodell-Konfiguration                          | [Modell für cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER-Formatkonfiguration                              | [Überprüft das Drucken von Format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Firmenlogo-Bild                                   | [Firmenlogo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Bild unterschreiben                                      | [Signatur image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternatives Signaturbild                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word Vorlage für den Druck von Zahlungsschecks  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Microsoft Excel Vorlage für den Druck von Zahlungsschecks | [Scheckvorlage.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Die folgende Grafik zeigt beispielhaft den Testausdruck für einen Zahlungsscheck, der aus der Excel-Vorlage generiert wird.

[![Testausdruck des Zahlungsschecks.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
