---
title: Zielorte für elektronische Berichterstellung (ER)
description: Dieses Thema enthält Informationen zur Verwaltung von ER-Zielen (Electronic Reporting), zu den unterstützten Zieltypen und zu Sicherheitsaspekten.
author: nselin
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2e4c6951afbff367dc93072d20395c3a37fffbcb
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030772"
---
# <a name="electronic-reporting-er-destinations"></a>Ziele für elektronische Berichterstellung (EB)

[!include [banner](../includes/banner.md)]

Sie können ein Ziel für jede Formatvariante zur "Elektronischen Berichterstellung" (ER) und die Ausgabenkomponente (einen Ordner oder eine Datei) konfigurieren. Benutzer, die entsprechende Zugriffsrechte haben, können auch Zieleinstellungen zur Laufzeit ändern. Dieses Thema beschreibt die ER Zielverwaltung, die unterstützten Zieltypen und die Sicherheitsaspekte.

Die ER-Formatkonfiguration umfasst in der Regel mindestens eine Ausgabekomponente: eine Datei. Konfigurationen enthalten in der Regel mehrere Ausgabedatei-Komponenten verschiedener Typen (zum Beispiel XML, TXT, XLSX, DOCX oder PDF), die entweder in einen einzelnen Ordner oder mehrere Ordner gruppiert sind. Die ER-Zielverwaltung ermöglicht die Vorkonfiguration der Ausführung jeder Komponente. Standardmäßig werden Ihnen bei der Ausführung einer Konfiguration ein Dialogfeld angezeigt, das zum Speichern oder Öffnen der Datei verwendet wird. Dasselbe Verhalten wird auch beim Importieren einer ER-Konfiguration ohne spezifische Ziele für diese verwendet. Nachdem ein Ziel für eine Hauptausgabekomponente erstellt wurde, überschreibt das Ziel das Standardverhalten und der Ordner oder die Datei wird entsprechend dem Ziel gesendet.

## <a name="availability-and-general-prerequisites"></a>Verfügbarkeit und allgemeine Voraussetzungen

Die Funktionalität für die EB-Ziele ist nicht in Microsoft Dynamics AX 7.0 (Februar 2016) verfügbar. Daher müssen Sie Microsoft Dynamics 365 for Operations Version 1611 (November 2016) oder höher zur Verwendung der folgenden Zieltypen installieren:

- [E-Mail](er-destination-type-email.md)
- [Archiv](er-destination-type-archive.md)
- [Datei](er-destination-type-file.md)
- [Bildschirm](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Alternativ können Sie eine der folgenden Komponenten installieren. Beachten Sie jedoch, dass diese Alternativen eine eher begrenzte ER-Zielerfahrung bieten.

- Microsoft Dynamics AX-Anwendungsversion 7.0.1 (Mai 2016)
- [Hotfix für die Verwaltung elektronischer Berichtsziele](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Außerdem gibt es einen [Drucken](er-destination-type-print.md)-Zieltyp. Um ihn zu verwenden, müssen Sie Microsoft Dynamics 365 Finance Version 10.0.9 (April 2020) installieren.

## <a name="overview"></a>Übersicht

Sie können Ziele nur für ER-Konfigurationen einrichten, die in die aktuelle Finance-Instanz [importiert](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) wurden und für die Formate auf der Seite **Konfigurationen für die elektronische Berichterstellung**. Die ER-Zielverwaltungsfunktionalität steht unter **Organisationsverwaltung** \> **Elektronische Berichterstattung** \> **Zielort für elektronische Berichterstellung** bereit. Auf der Seite **Zielort für elektronische Berichterstellung** können Sie das Standardverhalten für eine Konfiguration überschreiben. Importierte Konfigurationen werden auf dieser Seite nicht angezeigt, bis Sie auf **Neu** klicken und dann im Feld **Verweis** eine Konfiguration für die Zieleinstellungen wählen.

[![Wählen Sie im Feld eine Konfigurationstechnologie aus](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Nachdem Sie eine Referenz erstellt haben, können Sie ein Dateiziel für jede **Mappe** oder **Datei**-Ausgabekomponente des referenzierten ER-Formats erstellen.

[![Erstellen Sie die Zieldatei.](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Als nächstes können Sie im Dialogfeld **Zieleinstellungen** die einzelnen Ziele für die Dateiziele aktivieren und deaktivieren. Die **Einstellungen**-Schaltfläche wird verwendet, um alle Ziele für eine ausgewählte Dateiziel steuern. Im **Zieleinstellungen**-Dialogfeld Sie können jedes Ziel separat steuern, indem Sie die **Aktiviert**-Option nutzen.

In den Versionen von Finance **vor Version 10.0.9** können Sie **ein Dateiziel** für jede Ausgabekomponente des gleichen Formats im Feld Dateiname erstellen, z. B. einen Ordner oder eine Datei, die im Feld **Dateiname** ausgewählt ist. In **Version 10.0.9 und höher** können Sie **mehrere Dateiziele** für jede Ausgabekomponente desselben Formats erstellen.

Mit dieser Funktion können Sie beispielsweise Dateiziele für eine Dateikomponente konfigurieren, die zum Generieren eines ausgehenden Dokuments im Excel-Format verwendet wird. Ein Ziel ([Archiv](er-destination-type-archive.md)) kann so konfiguriert werden, dass die ursprüngliche Excel-Datei im ER-Auftragsarchiv gespeichert wird und ein anderes Ziel ([E-Mail ](er-destination-type-email.md)) kann konfiguriert werden, um die Excel-Datei gleichzeitig ins PDF-Format zu [konvertieren](#OutputConversionToPDF) und die PDF-Datei per E-Mail zu senden.

[![Mehrere Ziele für ein einzelnes Formatelement konfigurieren](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

## <a name="destination-types"></a>Zieltypen

Die folgenden Ziele werden derzeit für ER-Formate unterstützt. Sie können alle gleichzeitig aktivieren oder deaktivieren. Auf diese Weise können Sie entweder nichts machen, oder die Komponente an alle konfigurierten Ziele senden.

- [E-Mail](er-destination-type-email.md)
- [Archiv](er-destination-type-archive.md)
- [Datei](er-destination-type-file.md)
- [Bildschirm](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Drucken](er-destination-type-print.md)

## <a name="applicability"></a>Anwendbarkeit

Sie können Ziele nur für ER-Konfigurationen einrichten, die importiert wurden und für die Formate auf der Seite **Konfigurationen für die elektronische Berichterstellung** verfügbar sind.

> [!NOTE]
> Konfigurierte Ziele sind firmenspezifisch. Wenn Sie ein ER-Format in verschiedenen Unternehmen der aktuellen Finance-Instanz verwenden möchten, müssen Sie für jedes dieser Unternehmen Ziele für dieses ER-Format konfigurieren.

Wenn Sie Dateiziele für ein ausgewähltes Format konfigurieren, konfigurieren Sie sie für das gesamte Format.

[![Konfigurationslink](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Zur gleichen Zeit haben Sie möglicherweise mehrere [Versionen](general-electronic-reporting.md#component-versioning)des Formats, das in die aktuelle Finance-Instanz importiert wurde. Sie können diese anzeigen, wenn Sie den Link **Konfiguration** auswählen, der angeboten wird, wenn Sie das Feld **Referenz** auswählen.

[![Konfigurationsversionen](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Standardmäßig werden konfigurierte Ziele nur angewendet, wenn Sie eine Version im ER-Format ausführen, die entweder den Status **Abgeschlossen**oder **Geteilt** haben. Sie müssen jedoch manchmal konfigurierte Ziele verwenden, wenn die Entwurfsversion eines ER-Formats ausgeführt wird. Sie ändern beispielsweise eine Entwurfsversion Ihres Formats und möchten anhand konfigurierter Ziele testen, wie die generierte Ausgabe geliefert wird. Befolgen Sie diese Schritte, um Ziele für ein ER-Format anzuwenden, wenn die Entwurfsversion ausgeführt wird.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Stellen Sie die Option **Ziele für Entwurfsstatus verwenden** auf **Ja**.

[![Ziele für Option Entwurfsstatus verwenden](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Um die Entwurfsversion eines ER-Formats zu verwenden, müssen Sie das ER-Format entsprechend markieren.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Legen Sie die Option **Einstellung ausführen** auf **Ja** fest.

[![Option „Einstellung ausführen”](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Nachdem Sie dieses Setup abgeschlossen haben, wird die **Entwurf ausführen** für ER-Formate verfügbar, die Sie ändern. Setzen Sie diese Option auf **Ja**, um die Entwurfsversion des Formats zu verwenden, wenn das Format ausgeführt wird.

[![Entwurfsoption ausführen](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="DestinationFailure"></a>Behandlung von Zielfehlern

Normalerweise wird ein ER-Format im Rahmen eines bestimmten Geschäftsprozesses ausgeführt. Die Zustellung eines ausgehenden Dokuments, das während der Ausführung eines ER-Formats generiert wird, muss jedoch manchmal als Teil dieses Geschäftsprozesses betrachtet werden. In diesem Fall muss die Ausführung des Geschäftsprozesses abgebrochen werden, wenn die Zustellung eines generierten ausgehenden Dokuments an ein konfiguriertes Ziel nicht erfolgreich ist. Um das entsprechende ER-Ziel zu konfigurieren, wählen Sie die Option **Verarbeitung bei Fehler beenden**.

Beispielsweise konfigurieren Sie die Kreditorenzahlungsverarbeitung so, dass das ER-Format **ISO20022-Kreditübertragung** ausgeführt wird, um die Zahlungsdatei und die zusätzlichen Dokumente (z. B. Anschreiben und Kontrollbericht) zu generieren. Soll eine Zahlung erst dann als erfolgreich abgewickelt gelten, wenn das Anschreiben erfolgreich per E-Mail zugestellt wurde, müssen Sie das Kontrollkästchen **Verarbeitung bei Fehler beenden** für die Komponente **Anschreiben** in der entsprechenden Dateiziel, wie in der folgenden Abbildung dargestellt, auswählen. In diesem Fall wird der Status der Zahlung, die zur Verarbeitung ausgewählt wurde, von **Keine**zu **Geschickt** nur dann geändert, wenn das generierte Anschreiben von einem in der Finance-Instanz konfigurierten E-Mail-Anbieter erfolgreich zur Zustellung angenommen wurde.

[![Konfigurieren der Prozessbehandlung für Dateizielfehler](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Wenn Sie das Kontrollkästchen **Verarbeitung bei Fehler beenden** für die Komponente **Anschreiben** in der entsprechenden Dateiziel löschen, gilt eine Zahlung als erfolgreich verarbeitet, auch wenn das Anschreiben nicht erfolgreich per E-Mail zugestellt wurde. Der Status der Zahlung wird von **Keine**zu **Gesendet** geändert, auch wenn das Anschreiben nicht gesendet werden kann, weil beispielsweise die E-Mail-Adresse des Empfängers oder Absenders fehlt oder falsch ist.

## <a name="OutputConversionToPDF"></a>Ausgabeumwandlung in PDF

Sie können die PDF-Konvertierungsoption verwenden, um die Ausgabe in Microsoft Office Format (Excel/Word) in PDF-Format zu konvertieren.

### <a name="make-pdf-conversion-available"></a>PDF-Konvertierung verfügbar machen

Um die PDF-Konvertierungsoption in der aktuellen Finance-Instanz verfügbar zu machen, öffnen Sie den Arbeitsbereich **Funktionsverwaltung**, und aktivieren Sie die Funktion **Ausgehende Dokumente für die elektronische Berichterstellung von Microsoft Office Formaten in PDF konvertieren**.

[![Aktivieren der PDF-Konvertierung ausgehender Dokumente in der Funktionsverwaltung](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Anwendbarkeit

Die PDF-Konvertierungsoption kann nur für Dateikomponenten aktiviert werden, in denen die Ausgabe in Microsoft Office Exceloder Word-Format (**Excel-Datei**) generiert wird. Wenn diese Option aktiviert ist, wird die im Office-Format generierte Ausgabe automatisch in PDF-Format konvertiert.

### <a name="limitations"></a>Einschränkungen

> [!NOTE]
> Diese Funktion ist eine Vorschau-Funktion und unterliegt den angegebenen Nutzungsbedingungen, die in [Ergänzende Nutzungsbedingungen für Microsoft Dynamics 365-Vorschauen](https://go.microsoft.com/fwlink/?linkid=2105274) beschrieben sind.

> [!NOTE]
> Die PDF-Konvertierungsoption ist nur für Cloud-Bereitstellungen verfügbar.
>
> Das erstellte PDF ist auf maximal 300 Seiten beschränkt.
>
> Derzeit wird im PDF-Dokument, das aus einer Excel-Ausgabe erstellt wird, nur die Querformat-Seitenausrichtung unterstützt.
>
> Für die Konvertierung einer Ausgabe, die keine eingebetteten Schriftarten enthält, werden nur die allgemeinen Systemschriftarten des Windows-Betriebssystems verwendet.

### <a name="use-the-pdf-conversion-option"></a>Die PDF-Konvertierungsoption verwenden

Um die PDF-Konvertierung für ein Dateiziel zu aktivieren, aktivieren Sie das Kontrollkästchen **In PDF konvertieren**.

[![Aktivieren der PDF-Konvertierung für ein Dateiziel](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

## <a name="security-considerations"></a>Sicherheitsaspekte

Für ER Ziele werden zwei Arten von Rechte und Pflichten verwendet. Ein Typ steuert die allgemeine Fähigkeit eines Benutzers zur Pflege aller Ziele, die für eine juristische Person konfiguriert sind (steuert den Zugriff auf die **Elektronische Berichterstellung**-Seite). Der andere Typ steuert die Möglichkeit eines Benutzers der Anwendung, zur Laufzeit die Zieleinstellung zu überschreiben, die von einem ER-Entwickler oder vom funktionaler Berater konfiguriert wurden.

| Rolle (Name der AOT/Entwicklungsumgebung)                     | Rollenname                                  | Berechtigungen (Name der AOT/Entwicklungsumgebung)                     | Aufgabenname                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Entwickler für elektronische Berichterstellung             | ERFormatDestinationConfigure        | Zielort für elektronisches Berichtsformat konfigurieren                |
| ERFunctionalConsultant              | Funktionaler Berater für elektronische Berichterstellung | ERFormatDestinationConfigure        | Zielort für elektronisches Berichtsformat konfigurieren                |
| PaymAccountsPayablePaymentsClerk    | Sachbearbeiter Kreditorenkontozahlungen            | ERFormatDestinationRuntimeConfigure | Zielort für elektronisches Berichtsformat zur Laufzeit konfigurieren |
| PaymAccountsReceivablePaymentsClerk | Sachbearbeiter Debitorenkontenzahlungen         | ERFormatDestinationRuntimeConfigure | Zielort für elektronisches Berichtsformat zur Laufzeit konfigurieren |

> [!NOTE]
> In der vorherigen Aufgaben werden zwei Rechte verwendet. Diese Berechtigungen haben dieselben Namen wie die entsprechenden Aufgaben: **ERFormatDestinationConfigure** und **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Ich habe elektronische Konfigurationen importiert und sehe sie auf der Seite "Elektronische Berichterstellung". Aber warum sehe ich sie nicht auf der Seite "Ziele für die elektronische Berichterstellung"?

Stellen Sie sicher, dass Sie **Neu** und dann eine Konfiguration im Feld **Referenz** wählen. Auf der Seite **Zielorte für elektronische Berichterstellung** stehen nur die Konfigurationen, für die Ziele konfiguriert wurden.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Gibt es eine Möglichkeit zur Definition des verwendeten Microsoft Azure Storage-Kontos und des Azure Blob-Speichers?

Nr. Nein. Der standardmäßige Microsoft Azure Blob-Speicher, der definiert ist und für das Dokumentenmanagement-System verwendet wird, wird verwendet.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Wozu dient die Datei in den Zieleinstellungen? Was bewirkt diese Einstellung?

Das **Datei**-ziel dient zur Steuerung eines Dialogfelds. Wenn Sie dieses Ziel aktivieren oder wenn kein Ziel für eine Konfiguration definiert ist, erscheint ein Speichern- oder Öffnen-Dialogfeld, nachdem eine Ausgabedatei erstellt wurde.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Bitte geben Sie ein Beispiel für eine Formel, die auf ein Kreditorenkonto verweist, an das ich E-Mail senden kann.

Die Formel ist für die ER-Konfiguration spezifisch. Wenn Sie beispielsweise die ISO 20022-Kreditübertragunskonfiguration verwenden, dann können Sie **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** oder **Modell. Payments.Creditor.Identification.SourceID** verwenden, um das zugeordnete Kreditorenkonto zu erhalten.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Eine meiner Formatkonfigurationen enthält mehrere Dateien, die in einem Ordner gruppiert sind (z. B. Ordner1, der Datei1, Datei2 und Datei3 enthält). Wie richte ich Ziele ein, damit Ordner1.zip nicht erstellt wird, Datei1 per E-Mail gesendet wird, Datei2 an SharePoint gesendet wird und ich Datei3 direkt nach der Ausführung der Konfiguration öffnen kann?

Ihr Format muss erst in der ER-Konfigurationen verfügbar sein. Wenn diese Voraussetzung erfüllt ist, öffnen Sie die Seite **Ziel für elektronische Berichterstellung**, und erstellen Sie eine neue Referenz zu der Konfiguration. Sie müssen dann über vier Dateiziele verfügen – eine für jede Komponente. Erstellen Sie das erste Ziel, geben sie ihm einen Namen (z. B. **Ordner**), und wählen Sie einen Dateinamen, die einen Ordner in Ihrer Konfiguration darstellt. Wählen Sie dann **Einstellungen**, und stellen Sie sicher, dass alle Ziele deaktiviert sind. Für dieses Dateiziel wird kein Ordner erstellt. Aufgrund der hierarchischen Abhängigkeiten zwischen Dateien und übergeordneten Ordner verhalten sich die Dateien genauso. Sie werden also auch nicht gesendet. Um dieses Standardverhalten zu überschreiben, müssen Sie drei weitere Datei Ziele für jede Datei erstellen. In jeder Zieleinstellungen müssen Sie das Ziel aktivieren, an das die Datei gesendet werden soll.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung (Electronic reporting, ER)](general-electronic-reporting.md)
