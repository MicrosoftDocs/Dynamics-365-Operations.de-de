---
title: Zielorte für elektronische Berichterstellung (ER)
description: Dieser Artikel enthält Informationen zur Verwaltung von EB-Zielen (Elektronische Berichterstellung), zu den unterstützten Zieltypen und zu Sicherheitsaspekten.
author: nselin
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: bc8ef4a5299e6daba79702fadd37284f752a54a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851076"
---
# <a name="electronic-reporting-er-destinations"></a>Zielorte für elektronische Berichterstellung (ER)

[!include [banner](../includes/banner.md)]

Sie können ein Ziel für jede Formatvariante zur "Elektronischen Berichterstellung" (ER) und die Ausgabenkomponente (einen Ordner oder eine Datei) konfigurieren. Benutzer, die entsprechende Zugriffsrechte haben, können auch Zieleinstellungen zur Laufzeit ändern. Dieser Artikel beschreibt die ER Zielverwaltung, die unterstützten Zieltypen und die Sicherheitsaspekte.

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

Außerdem gibt es einen [Drucken](er-destination-type-print.md)-Zieltyp. Um ihn zu verwenden, müssen Sie Microsoft Microsoft Dynamics 365 Finance Version 10.0.9 (April 2020) installieren.

## <a name="overview"></a>Übersicht

Sie können Ziele nur für ER-Konfigurationen einrichten, die in die aktuelle Finance-Instanz [importiert](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) wurden und für die Formate auf der Seite **Konfigurationen für die elektronische Berichterstellung**. Die ER-Zielverwaltungsfunktionalität steht unter **Organisationsverwaltung** \> **Elektronische Berichterstattung** \> **Zielort für elektronische Berichterstellung** bereit.

### <a name="default-behavior"></a>Standardmäßiges Verhalten

Das Standardverhalten für eine EB-Formatkonfiguration hängt vom Ausführungstyp ab, den Sie beim Start eines EB-Formats angeben.

Im Dialogfeld **Intrastat-Bericht** im Inforegister **Im Hintergrund ausführen**, wenn Sie die Option **Stapelverarbeitung** auf **Nein** festlegen, wird ein EB-Format sofort im interaktiven Modus ausgeführt. Wenn diese Ausführung erfolgreich abgeschlossen wurde, wird ein generiertes ausgehendes Dokument zum Download bereitgestellt.

Wenn Sie die Option **Stapelverarbeitung** auf **Ja** festlegen, wird ein EB-Format im Modus [Charge](../sysadmin/batch-processing-overview.md) ausgeführt. Der entsprechende Stapelverarbeitungsauftrag wird basierend auf den Parametern erstellt, die Sie in der Registerkarte **Im Hintergrund ausführen** des Dialogfelds **EB-Parameter** angeben.

> [!NOTE]
> Die Einzelvorgangsbeschreibung informiert Sie über die Ausführung einer EB-Formatzuordnung. Sie enthält auch den Namen der ausgeführten EB-Komponente.

[![Ausführen eines EB-Formats.](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Informationen zu diesen Einzelvorgang finden Sie an mehreren Stellen:

- Gehen Sie zu **Allgemein** \> **Abfragen** \> **Stapelverarbeitungsaufträge** \> **Meine Stapelverarbeitugnsaufträge,** um den Status des geplanten Einzelvorgangs zu überprüfen.
- Gehen Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Einzelvorgänge der elektronischen Berichterstellung,** um den Status des geplanten Einzelvorgangs und die Ausführungsergebnisse des abgeschlossenen Einzelvorgangs zu überprüfen. Wenn die Einzelvorgangsausführung erfolgreich abgeschlossen wurde, wählen Sie **Dateien anzeigen** auf der Seite **Einzelvorgänge der elektronischen Berichterstellung** aus, um ein generiertes ausgehendes Dokument abzurufen.

    > [!NOTE]
    > Dieses Dokument wird als Anhang des aktuellen Einzelvorgangsdatensatzes gespeichert und vom [Dokumentverwaltung](../../fin-ops/organization-administration/configure-document-management.md)-Framework gesteuert. Der [Dokumententyp](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), der verwendet wird, um EB-Artefakte dieses Typs zu speichern, wird in den [EB-Parametern](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) konfiguriert.

- Auf der Seite **Einzelvorgänge der elektronischen Berichterstellung** wählen Sie **Dateien anzeigen** aus, um die Liste aller Fehler und Warnungen anzuzeigen, die während der Einzelvorgangsausführung generiert wurden.

    [![Überprüfen der EB-Einzelvorgangsliste.](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Vom Benutzer konfiguriertes Verhalten

Auf der Seite **Zielort für elektronische Berichterstellung** können Sie das Standardverhalten für eine Konfiguration überschreiben. Importierte Konfigurationen werden auf dieser Seite nicht angezeigt, bis Sie auf **Neu** klicken und dann im Feld **Verweis** eine Konfiguration für die Zieleinstellungen wählen.

[![Im Verweisfeld eine Konfiguration auswählen.](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Nachdem Sie eine Referenz erstellt haben, können Sie ein Dateiziel für jede **Mappe** oder **Datei**-Ausgabekomponente des referenzierten ER-Formats erstellen.

[![Eine Zieldatei erstellen.](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Als nächstes können Sie im Dialogfeld **Zieleinstellungen** die einzelnen Ziele für die Dateiziele aktivieren und deaktivieren. Die **Einstellungen**-Schaltfläche wird verwendet, um alle Ziele für eine ausgewählte Dateiziel steuern. Im **Zieleinstellungen**-Dialogfeld Sie können jedes Ziel separat steuern, indem Sie die **Aktiviert**-Option nutzen.

In den Versionen von Finance **vor Version 10.0.9** können Sie **ein Dateiziel** für jede Ausgabekomponente des gleichen Formats im Feld Dateiname erstellen, z. B. einen Ordner oder eine Datei, die im Feld **Dateiname** ausgewählt ist. In **Version 10.0.9 und höher** können Sie **mehrere Dateiziele** für jede Ausgabekomponente desselben Formats erstellen.

Mit dieser Funktion können Sie beispielsweise Dateiziele für eine Dateikomponente konfigurieren, die zum Generieren eines ausgehenden Dokuments im Excel-Format verwendet wird. Ein Ziel ([Archiv](er-destination-type-archive.md)) kann so konfiguriert werden, dass die ursprüngliche Excel-Datei im ER-Auftragsarchiv gespeichert wird und ein anderes Ziel ([E-Mail](er-destination-type-email.md)) kann konfiguriert werden, um die Excel-Datei gleichzeitig ins PDF-Format zu [konvertieren](#OutputConversionToPDF) und die PDF-Datei per E-Mail zu senden.

[![Mehrere Ziele für ein einzelnes Formatelement konfigurieren.](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Wenn Sie ein EB-Format ausführen, werden immer alle Ziele ausgeführt, die für Komponenten des Formats konfiguriert wurden. Darüber hinaus wurde die Funktionalität für EB-Ziele in Finance **Version 10.0.17 und höher** verbessert. Jetzt können Sie verschiedene Zielgruppen für ein einzelnes EB-Format konfigurieren. Diese Konfiguration markiert jeden Satz als für eine bestimmte Benutzeraktion konfiguriert. Die EB-API wurde [erweitert](er-apis-app10-0-17.md), sodass eine Aktion bereitgestellt werden kann, die der Benutzer durch Ausführen eines EB-Formats ausführt. Der bereitgestellte Aktionscode wird an EB-Ziele übergeben. Abhängig vom bereitgestellten Aktionscode können Sie verschiedene Ziele eines EB-Formats ausführen. Weitere Informationen finden Sie unter [Aktivitätsabhängige EB-Ziele konfigurieren](er-action-dependent-destinations.md).

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

[![Konfigurationslink.](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Zur gleichen Zeit haben Sie möglicherweise mehrere [Versionen](general-electronic-reporting.md#component-versioning) des Formats, das in die aktuelle Finance-Instanz importiert wurde. Sie können diese anzeigen, wenn Sie den Link **Konfiguration** auswählen, der angeboten wird, wenn Sie das Feld **Referenz** auswählen.

[![Konfigurationsversionen.](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Standardmäßig werden konfigurierte Ziele nur angewendet, wenn Sie eine Version im ER-Format ausführen, die entweder den Status **Abgeschlossen** oder **Geteilt** haben. Sie müssen jedoch manchmal konfigurierte Ziele verwenden, wenn die Entwurfsversion eines ER-Formats ausgeführt wird. Sie ändern beispielsweise eine Entwurfsversion Ihres Formats und möchten anhand konfigurierter Ziele testen, wie die generierte Ausgabe geliefert wird. Befolgen Sie diese Schritte, um Ziele für ein ER-Format anzuwenden, wenn die Entwurfsversion ausgeführt wird.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Stellen Sie die Option **Ziele für Entwurfsstatus verwenden** auf **Ja**.

[![Ziele für Option Entwurfsstatus verwenden.](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Um die Entwurfsversion eines ER-Formats zu verwenden, müssen Sie das ER-Format entsprechend markieren.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Legen Sie die Option **Einstellung ausführen** auf **Ja** fest.

[![Option „Einstellung ausführen“.](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Nachdem Sie dieses Setup abgeschlossen haben, wird die **Entwurf ausführen** für ER-Formate verfügbar, die Sie ändern. Setzen Sie diese Option auf **Ja**, um die Entwurfsversion des Formats zu verwenden, wenn das Format ausgeführt wird.

[![Entwurfsoption ausführen.](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Behandlung von Zielfehlern

Normalerweise wird ein ER-Format im Rahmen eines bestimmten Geschäftsprozesses ausgeführt. Die Zustellung eines ausgehenden Dokuments, das während der Ausführung eines ER-Formats generiert wird, muss jedoch manchmal als Teil dieses Geschäftsprozesses betrachtet werden. In diesem Fall muss die Ausführung des Geschäftsprozesses abgebrochen werden, wenn die Zustellung eines generierten ausgehenden Dokuments an ein konfiguriertes Ziel nicht erfolgreich ist. Um das entsprechende ER-Ziel zu konfigurieren, wählen Sie die Option **Verarbeitung bei Fehler beenden**.

Beispielsweise konfigurieren Sie die Kreditorenzahlungsverarbeitung so, dass das ER-Format **ISO20022-Kreditübertragung** ausgeführt wird, um die Zahlungsdatei und die zusätzlichen Dokumente (z. B. Anschreiben und Kontrollbericht) zu generieren. Soll eine Zahlung erst dann als erfolgreich abgewickelt gelten, wenn das Anschreiben erfolgreich per E-Mail zugestellt wurde, müssen Sie das Kontrollkästchen **Verarbeitung bei Fehler beenden** für die Komponente **Anschreiben** in der entsprechenden Dateiziel, wie in der folgenden Abbildung dargestellt, auswählen. In diesem Fall wird der Status der Zahlung, die zur Verarbeitung ausgewählt wurde, von **Keine** zu **Geschickt** nur dann geändert, wenn das generierte Anschreiben von einem in der Finance-Instanz konfigurierten E-Mail-Anbieter erfolgreich zur Zustellung angenommen wurde.

[![Konfigurieren der Prozessbehandlung für Dateizielfehler.](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Wenn Sie das Kontrollkästchen **Verarbeitung bei Fehler beenden** für die Komponente **Anschreiben** in der entsprechenden Dateiziel löschen, gilt eine Zahlung als erfolgreich verarbeitet, auch wenn das Anschreiben nicht erfolgreich per E-Mail zugestellt wurde. Der Status der Zahlung wird von **Keine** zu **Gesendet** geändert, auch wenn das Anschreiben nicht gesendet werden kann, weil beispielsweise die E-Mail-Adresse des Empfängers oder Absenders fehlt oder falsch ist.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Ausgabeumwandlung in PDF

Sie können die PDF-Konvertierungsoption verwenden, um die Ausgabe im Microsoft Office-Format (Excel oder Word) in das PDF-Format zu konvertieren.

### <a name="make-pdf-conversion-available"></a>PDF-Konvertierung verfügbar machen

Um die PDF-Konvertierungsoption in der aktuellen Finance-Instanz verfügbar zu machen, öffnen Sie den Arbeitsbereich **Funktionsverwaltung**, und aktivieren Sie die Funktion **Ausgehende Dokumente für die elektronische Berichterstellung von Microsoft Office Formaten in PDF konvertieren**.

[![Aktivieren der PDF-Konvertierung ausgehender Dokumente in der Funktionsverwaltung.](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Anwendbarkeit

In Versionen von Finance **vor der Version 10.0.18** kann die PDF-Konvertierungsoption nur für Komponenten **Excel \\ Datei** aktiviert werden, die zum Generieren der Ausgabe in Office-Format (Excel oder Word)verwendet werden. Wenn diese Option aktiviert ist, wird die im Office-Format generierte Ausgabe automatisch in PDF-Format konvertiert. In **Version 10.0.18 und höher** können Sie diese Option jedoch auch für Komponenten des Typs **Allgemein\\Datei** aktivieren.

> [!NOTE]
> Beachten Sie die Warnmeldung, die Sie erhalten, wenn Sie die PDF-Konvertierungsoption für eine ER-Komponente des Typs **Allgemein\\Datei** aktivieren. Diese Meldung informiert Sie darüber, dass zur Entwurfszeit nicht garantiert werden kann, dass die ausgewählte Dateikomponente den Inhalt im PDF-Format oder den PDF-konvertierbaren Inhalt zur Laufzeit verfügbar macht. Daher sollten Sie die Option nur aktivieren, wenn Sie sicher sind, dass die ausgewählte Dateikomponente so konfiguriert wurde, dass der Inhalt im PDF-Format oder der PDF-konvertierbare Inhalt zur Laufzeit verfügbar gemacht wird.
> 
> Wenn Sie die PDF-Konvertierungsoption für eine Formatkomponente aktivieren: Wenn diese Komponente Inhalte in einem anderen Format als PDF verfügbar macht und der exponierte Inhalt nicht in das PDF-Format konvertiert werden kann, tritt zur Laufzeit eine Ausnahme auf. Die Nachricht, die Sie erhalten, informiert Sie darüber, dass der generierte Inhalt nicht in das PDF-Format konvertiert werden kann.

### <a name="limitations"></a>Einschränkungen

Ab Finance **Version 10.0.9** ist die PDF-Konvertierungsoption nur für Cloud-Bereitstellungen verfügbar. Ab Finance-Version **10.0.27** ist die PDF-Konvertierungsoption für jede lokale Bereitstellung verfügbar, bei der [Internetverbindung](../user-interface/client-disconnected.md) aktiviert ist.

Das erstellte PDF ist auf maximal 300 Seiten beschränkt.

Ab Finance **Version 10.0.9** wird im PDF-Dokument, das aus einer Excel-Ausgabe erstellt wird, nur die Querformat-Seitenausrichtung unterstützt. Ab Finance **Version 10.0.10** können Sie im PDF-Dokument, das aus einer Excel-Ausgabe erstellt wird, [die Seitenausrichtung angeben](#SelectPdfPageOrientation), während Sie ein ER-Ziel konfigurieren.

Für die Konvertierung einer Ausgabe, die keine eingebetteten Schriftarten enthält, werden nur die allgemeinen Systemschriftarten des Windows-Betriebssystems verwendet.

### <a name="use-the-pdf-conversion-option"></a>Die PDF-Konvertierungsoption verwenden

Um die PDF-Konvertierung für ein Dateiziel zu aktivieren, aktivieren Sie das Kontrollkästchen **In PDF konvertieren**.

[![Aktivieren der PDF-Konvertierung für ein Dateiziel.](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Wählen Sie eine Seitenausrichtung für die PDF-Konvertierung</a>

Wenn Sie eine EB-Konfiguration im Excel-Format generieren und in das PDF-Format konvertieren möchten, können Sie die Seitenausrichtung der PDF-Datei explizit angeben. Wenn Sie **In PDF konvertieren** auswählen, aktivieren Sie das Kontrollkästchen, um die PDF-Konvertierung für ein Dateiziel zu aktivieren, das eine Ausgabedatei im Excel-Format erstellt. Das Feld **Seitenausrichtung** wird auf dem Inforegister **PDF-Konvertierungseinstellungen** verfügbar. In dem Feld **Seitenausrichtung** können Sie eine bevorzugte Seitenausrichtung auswählen.

[![Wählen Sie eine Seitenausrichtung für die PDF-Konvertierung.](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

Um die PDF-Seitenausrichtung auswählen zu können, installieren Sie Finance Version 10.0.10 oder höher. In Versionen von Finance **vor Version 10.0.23** bietet diese Option die folgenden Seitenausrichtungsoptionen:

- Hochformat
- Querformat

Die ausgewählte Seitenausrichtung wird auf alle Seite eines ausgehenden Dokuments angewendet, das im Excel-Format generiert und dann in das PDF-Format konvertiert wird.

Allerdings wurde die Liste der Seitenausrichtungsoptionen in **Version 10.0.23 und höher** wie folgt erweitert:

- Hochformat
- Querformat
- Arbeitsblattspezifisch

Wenn Sie die Option **Arbeitsblattspezifisch** auswählen, wird jedes Arbeitsblatt einer generierten Excel-Arbeitsmappe in PDF konvertiert, indem die Seitenausrichtung verwendet wird, die für dieses Arbeitsblatt in der verwendeten Excel-Vorlage konfiguriert wurde. Möglicherweise haben Sie also ein endgültiges PDF-Dokument mit Seiten im Hoch- und Querformat. 

Wenn eine ER-Konfiguration im Word-Format in das PDF-Format konvertiert wird, wird die Seitenausrichtung der PDF-Datei aus dem Word-Dokument immer übernommen.

## <a name="output-unfolding"></a>Ausgabe entfaltet sich

Wenn Sie ein Ziel für die Komponente **Ordner** Ihres ER-Formats erstellen, können Sie angeben, wie die Ausgabe dieser Komponente an das konfigurierte Ziel geliefert wird.

### <a name="make-output-unfolding-available"></a>Stellen Sie die Entfaltung der Ausgabe zur Verfügung

Damit die Option zum Entfalten der Ausgabe in der aktuellen Finanzinstanz verfügbar ist, öffnen Sie den Arbeitsbereich **Funktionsverwaltung** und schalten Sie die Funktion **Ermöglichen Sie das Konfigurieren von ER-Zielen, Ordnerinhalte als separate Dateien zu senden** ein.

### <a name="applicability"></a>Anwendbarkeit

Die Option zum Entfalten der Ausgabe kann nur für die Formatkomponenten des Typs **Ordner** konfiguriert werden. Wenn Sie mit der Konfiguration von einer Komponente **Ordner** beginnen, wird das Inforegister **Allgemeines** auf der Seite **Ziel der elektronischen Berichterstattung** verfügbar. 

### <a name="use-the-output-unfolding-option"></a>Verwenden Sie die Option zum Entfalten der Ausgabe

Auf dem Inforegister **Allgemeines** im **Ordner senden als** wählen Sie im Feld einen der folgenden Werte aus:

- **ZIP-Archiv** – Liefern Sie eine generierte Datei als Zip-Datei.
- **Separate Dateien** – Liefern Sie jede Datei einer generierten Zip-Datei als einzelne Datei.

    > [!NOTE]
    > Wenn Sie **Separate Dateien** auswählen, wird die generierte Ausgabe in einem komprimierten Zustand im Speicher gesammelt. Daher wird die maximale [Dateigrößenbeschränkung](er-compress-outbound-files.md) für die komprimierte Ausgabe angewendet, wenn die tatsächliche Dateigröße diese Grenze möglicherweise überschreitet. Wir empfehlen, diesen Wert auszuwählen, wenn Sie erwarten, dass die Größe der generierten Ausgabe zu groß ist.

[![Konfigurieren eines Ziels für eine Komponente im Ordnerformat.](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>Einschränkungen

Wenn Sie das Feld **Ordner senden als** auf **Separate Dateien** für eine Komponente **Ordner** festlegen, die andere eingebetteten Komponenten **Ordner** enthält, wird die Einstellung nicht rekursiv auf die verschachtelten Komponenten **Ordner** angewendet.

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

Das Ziel der **Datei** wird verwendet, um ein Dialogfeld Ihres Webbrowsers zu steuern, wenn Sie ein EB-Format im interaktiven Modus ausführen. Wenn Sie dieses Ziel aktivieren oder wenn kein Ziel für eine Konfiguration definiert ist, erscheint ein Speichern- oder Öffnen-Dialogfeld im Webbrowser.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Bitte geben Sie ein Beispiel für eine Formel, die auf ein Kreditorenkonto verweist, an das ich E-Mail senden kann.

Die Formel ist für die ER-Konfiguration spezifisch. Wenn Sie beispielsweise die ISO 20022-Kreditübertragunskonfiguration verwenden, dann können Sie **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** oder **Modell. Payments.Creditor.Identification.SourceID** verwenden, um das zugeordnete Kreditorenkonto zu erhalten.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Eine meiner Formatkonfigurationen enthält mehrere Dateien, die in einem Ordner gruppiert sind (z. B. Ordner1, der Datei1, Datei2 und Datei3 enthält). Wie richte ich Ziele ein, damit Ordner1.zip nicht erstellt wird, Datei1 per E-Mail gesendet wird, Datei2 an SharePoint gesendet wird und ich Datei3 direkt nach der Ausführung der Konfiguration öffnen kann?

Ihr Format muss erst in der ER-Konfigurationen verfügbar sein. Wenn diese Voraussetzung erfüllt ist, öffnen Sie die Seite **Ziel für elektronische Berichterstellung**, und erstellen Sie eine neue Referenz zu der Konfiguration. Sie müssen dann über vier Dateiziele verfügen – eine für jede Komponente. Erstellen Sie das erste Ziel, geben sie ihm einen Namen (z. B. **Ordner**), und wählen Sie einen Dateinamen, die einen Ordner in Ihrer Konfiguration darstellt. Wählen Sie dann **Einstellungen**, und stellen Sie sicher, dass alle Ziele deaktiviert sind. Für dieses Dateiziel wird kein Ordner erstellt. Aufgrund der hierarchischen Abhängigkeiten zwischen Dateien und übergeordneten Ordner verhalten sich die Dateien genauso. Sie werden also auch nicht gesendet. Um dieses Standardverhalten zu überschreiben, müssen Sie drei weitere Datei Ziele für jede Datei erstellen. In jeder Zieleinstellungen müssen Sie das Ziel aktivieren, an das die Datei gesendet werden soll.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)

[Aktivitätsabhängige EB-Ziele konfigurieren](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
