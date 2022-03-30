---
title: Entwerfen einer neuen ER-Lösung zum Drucken von ZPL-Labels
description: Dieses Thema erklärt, wie Sie eine neue Lösung für die elektronische Rechnungsstellung (ER) entwerfen, um Zebra Programming Language (ZPL) Etiketten zu drucken.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 4fb89f4b56ce8189482bf1a86582ef7e3684b15a
ms.sourcegitcommit: 411874545d7c326fc4aa877948a059371f0ccb3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392962"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Entwerfen einer neuen ER-Lösung zum Drucken von ZPL-Labels

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie ein Benutzer in der Rolle Systemadministrator, Entwickler für elektronische Berichterstellung oder Funktionsberater für elektronische Berichterstellung die Parameter des [Frameworks für elektronische Berichterstellung (ER)](general-electronic-reporting.md) konfigurieren, die erforderlichen ER [Konfigurationen](general-electronic-reporting.md#Configuration) einer neuen ER-Lösung entwerfen kann, um auf die Daten des Lagerortverwaltungssystems zuzugreifen und angepasste Lagerort-Etiketten im Format Zebra Programming Language (ZPL) II zu erzeugen. Diese Schritte können im Unternehmen **USRT** ausgeführt werden.

## <a name="business-scenario"></a>Geschäftsszenario

Sie vertreten eine Firma, die die Lagerortverwaltung in Microsoft Dynamics 365 Finance implementiert hat. Jedes Lager muss mit einem selbstklebenden Label mit einem Strichcode versehen werden. Die Arbeitskräfte im Lager verwenden tragbare Barcode-Lesegeräte, um die Barcodes zu scannen.

Alle Lagerstandorte wurden im Rahmen der Pre-Go-Live-Aktivitäten etikettiert. Sie müssen jedoch auch in der Lage sein, bei Bedarf Lagerort-Etiketten zu drucken, wenn vorhandene Etiketten beschädigt werden oder die Lagerregale neu konfiguriert werden. Mithilfe der kürzlich freigegebenen ER-Funktionalität können Sie eine neue ER-Lösung konfigurieren, mit der ein Lagerverwalter Etiketten direkt auf einem Thermo-Etikettendrucker ausdrucken kann.

## <a name="configure-the-er-framework"></a>Konfigurieren des EB-Frameworks

Befolgen Sie die Schritte in [ER-Framework konfigurieren](er-quick-start2-customize-report.md#ConfigureFramework), um den minimalen Satz von ER-Parametern einzurichten. Sie müssen diese Einrichtung abschließen, bevor Sie das ER Framework zum Entwerfen einer neuen ER-Lösung verwenden können.

## <a name="design-a-domain-specific-data-model"></a>Entwerfen eines domänenspezifischen Datenmodells

Erstellen Sie eine neue ER-Konfiguration, die eine [Datenmodell](er-overview-components.md#data-model-component)-Komponente für den Bereich Lagerortverwaltung enthält. Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie ein ER-Format für die Erstellung von Etiketten für Lagerstandorte entwerfen.

### <a name="import-a-data-model-configuration"></a>Importieren Sie eine Datenmodellkonfiguration

Führen Sie diese Schritte aus, um das erforderliche Datenmodell aus einer von Microsoft bereitgestellten XML-Datei zu importieren. Alternativ können Sie auch Ihr eigenes Datenmodell erstellen, wie im nächsten Abschnitt beschrieben.

1. Laden Sie die Datei [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Exchange** \> **Laden aus XML-Datei**.
5. Wählen Sie **Durchsuchen** und suchen Sie dann die Datei **Warehouse model.version.1.xml** und wählen Sie sie aus.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

![Importierte ER-Datenmodell-Konfiguration auf der Seite Konfigurationen.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Erstellen Sie eine Datenmodellkonfiguration

Anstatt die von Microsoft bereitgestellte Datenmodelldatei zu importieren, können Sie ein Datenmodell von Grund auf erstellen. Ein Beispiel für die Ausführung dieser Aufgabe finden Sie unter [Erstellen einer neuen Datenmodellkonfiguration](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Überprüfen Sie das Datenmodell

Sie können eine bearbeitbare Version des konfigurierten Datenmodells auf der Seite **Datenmodell-Designer** anzeigen.

![Struktur des ER-Datenmodells auf der Seite Datenmodell-Designer.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Entwerfen einer Modellzuordnung für das konfigurierte Datenmodell

Als Benutzer in der Rolle Electronic Reporting Developer müssen Sie eine neue ER-Konfiguration erstellen, die eine [Modellzuordnung](er-overview-components.md#model-mapping-component) Komponente für das Lager-Datenmodell enthält. Diese Komponente implementiert das konfigurierte Datenmodell für Dynamics 365 Finance und ist spezifisch für diese App. Sie müssen es so konfigurieren, dass die Anwendungsobjekte angegeben werden, die verwendet werden, um das konfigurierte Datenmodell zur Laufzeit mit Anwendungsdaten zu füllen. Um diese Aufgabe abzuschließen, müssen Sie verstehen, wie die Datenstruktur der des Geschäftsbereichs Lagerortverwaltung in Finance implementiert ist.

### <a name="import-a-model-mapping-configuration"></a>Importieren Sie eine Konfiguration für die Modellzuordnung

Führen Sie diese Schritte aus, um die erforderliche Modellzuordnung aus einer von Microsoft bereitgestellten XML-Datei zu importieren. Alternativ können Sie auch eine eigene Modellzuordnung erstellen, wie im nächsten Abschnitt beschrieben.

1. Laden Sie die Datei [Warehouse model mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Exchange** \> **Laden aus XML-Datei**.
5. Wählen Sie **Durchsuchen** und suchen und wählen Sie dann die Datei **Lagermodell Zuordnung.Version.1.1.xml**.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

![Importierte ER-Model-Zuordnungskonfiguration auf der Seite Konfigurationen.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Erstellen Sie eine Konfiguration für die Modellzuordnung

Anstatt die von Microsoft zur Verfügung gestellte Modellzuordnungsdatei zu importieren, können Sie eine Modellzuordnung von Grund auf erstellen. Ein Beispiel für die Ausführung dieser Aufgabe finden Sie unter [Erstellen einer neuen Konfiguration für die Modellzuordnung](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Die Modellzuordnung überprüfen

Sie können eine bearbeitbare Version der konfigurierten Modellzuordnung auf der Seite **Modellzuordnungsdesigner** anzeigen.

![Struktur der ER-Model-Zuordnung auf der Seite Modellzuordnung Designer.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Entwerfen eines Formats

Als Benutzer in der Rolle des Electronic Reporting Functional Consultant müssen Sie eine neue EB-Konfiguration erstellen, die eine Komponente [Format](er-overview-components.md#format-component) enthält. Um diese Komponente zu konfigurieren, verwenden Sie ZPL II-Code, um das Layout des Labels für den Standort Ihres Lagers festzulegen.

### <a name="import-a-format-configuration"></a>Importieren Sie eine Formatkonfiguration

Führen Sie diese Schritte aus, um das erforderliche Format aus einer von Microsoft bereitgestellten XML-Datei zu importieren. Alternativ können Sie auch ein eigenes Format erstellen, wie im nächsten Abschnitt beschrieben.

1. Laden Sie die Datei [Warehouse location labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Exchange** \> **Laden aus XML-Datei**.
5. Wählen Sie **Durchsuchen**, und suchen Sie dann die Datei **Warehouse location labels.version.1.1.xml** und wählen Sie sie aus.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

![Importierte ER-Format-Konfiguration auf der Seite Konfigurationen.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Erstellen einer Formatkonfiguration

Anstatt die von Microsoft bereitgestellte Formatdatei zu importieren, können Sie ein Format von Grund auf erstellen. Ein Beispiel für die Ausführung dieser Aufgabe finden Sie unter [Erstellen einer neuen Formatkonfiguration](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Das Format überprüfen

Sie können eine bearbeitbare Version des konfigurierten Formats auf der Seite **Formatdesigner** anzeigen.

![Struktur des ER-Formats auf der Seite Formatdesigner.](./media/er-design-zpl-labels-format.png)

Die Datenquelle `model.Location.Label` dieses Formats ist so konfiguriert, dass sie Labels erzeugt, die die folgenden Informationen enthalten:

- Der Lagertitel als Text
- Der Lagertitel als Strichcode
- Der Titel des Ortes
- Prüfziffern

Auf der Seite **Formeldesigner** für die Datenquelle enthält die ER-Formel, die zur Erzeugung von Labels verwendet wird, eine `CONCATENATE`-Funktion, die die Informationen im gewünschten Layout kombiniert.

![Formel für die Datenquelle auf der Seite Formel-Designer.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Das Layout des Labels ist so gestaltet, dass der Ortstitel und die Prüfziffern in der Mitte des Labels ausgerichtet sind. ZPL II unterstützt jedoch keine zentrierte Ausrichtung für Barcodes. Daher wird die Formel der Datenquelle `model.Location.Warehouse.Alignment` verwendet, um den Strichcode in der Mitte des Etiketts auszurichten. Diese Formel berechnet den Linksversatz des Strichcodes auf der Grundlage der Anzahl der Zeichen im Lagertitel.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Bereiten Sie Ihre Umgebung für die Vorschau der generierten Etiketten vor

Das folgende Beispiel verwendet eine Druckeremulator-Anwendung für ZPL-Etiketten, um eine Vorschau der generierten Etiketten auf dem Bildschirm anzuzeigen. Führen Sie diese Schritte aus, um diese Option zu aktivieren.

1. Fügen Sie das [Drucker](er-destination-type-print.md) ER-Ziel für das **Lagerort-Etikett** ER-Format hinzu und konfigurieren Sie es so, dass es generierte Labels von Finance an den [Document Routing Agent (DRA)](install-document-routing-agent.md) sendet.
2. Installieren und konfigurieren Sie den DRA, um generierte Etiketten aus Finance an einen lokalen Drucker weiterzuleiten, auf den von der aktuellen Arbeitsstation aus zugegriffen werden kann.
3. Fügen Sie einen lokalen Drucker für den aktuellen Arbeitsplatz hinzu und konfigurieren Sie ihn so, dass er die vom DRA erzeugten Etiketten an eine Druckeremulator-Anwendung weiterleitet.
4. Installieren Sie eine Druckeremulator-Anwendung als Erweiterung des Chrome-Webbrowsers und konfigurieren Sie sie so, dass sie die generierten Etiketten von einem lokalen Drucker an einen Webdienst weiterleitet, der die generierten Etiketten rendert und sie zur Vorschau an den Druckeremulator zurückgibt.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER-Bericht</p>
<p>Druckziel</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Dokument-Routing-Agent</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Lokaler Drucker</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Drucker-Emulator</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Rendering des Webdienstes</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Installieren und konfigurieren Sie eine Drucker-Emulator-Anwendung

Fügen Sie eine Druckeremulator-Anwendung für die ZPL-Rendering-Engine zu Ihrem Chrome-Webbrowser hinzu. Dieses Beispiel verwendet den [Zpl Printer](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) Emulator, der auf dem [Labelary ZPL Web Service](http://labelary.com/service.html) basiert. Die Anwendung des Druckeremulators übergibt die von einem lokalen Drucker erzeugten Labels im ZPL-Format an den Webdienst und gibt die Labels dann als PDF- oder PNG-Dateien zur Vorschau zurück.

1. Suchen Sie im Chrome Web Store die Druckeremulator-Anwendung, die Sie verwenden möchten, und wählen Sie sie aus. Wählen Sie dann **Zu Chrome hinzufügen**, um es zu Ihrem Chrome-Webbrowser hinzuzufügen.

    ![Hinzufügen der Druckeremulator-Anwendung zum Chrome Webbrowser aus dem Chrome Web Store.](./media/er-design-zpl-labels-add-app.png)

2. Wählen Sie **App starten**, um die Anwendung Druckeremulator über den Chrome Webbrowser auszuführen.

    ![Ausführen der Druckeremulator-Anwendung über den Chrome-Webbrowser.](./media/er-design-zpl-labels-run-app.png)

3. Konfigurieren Sie die ausgeführte Anwendung:

    1. Schalten Sie die Anwendung aus.
    2. Legen Sie in den Druckereinstellungen den Host auf **127.0.0.1** fest.
    3. Legen Sie den Port auf **9100** fest.

        ![Konfigurieren Sie die Druckeremulator-Anwendung.](./media/er-design-zpl-labels-configure-app.png)

    4. Schalten Sie die Anwendung wieder ein. Sie sollten eine Nachricht erhalten, die besagt, dass der Drucker auf dem angegebenen Host und Port gestartet wurde.

        ![Die Anwendung Drucker-Emulator ist wieder eingeschaltet.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Da die Druckeremulator-Anwendung, die in diesem Beispiel verwendet wird, zur Darstellung der Etiketten auf einen Webdienst angewiesen ist, stellen Sie sicher, dass Ihre Sicherheitseinstellungen die Kommunikation mit dem Dienst zulassen. Andernfalls empfängt die Anwendung die gerenderten Labels nicht, und es ist keine Vorschau dieser Labels verfügbar.

### <a name="add-and-configure-a-local-printer"></a>Fügen Sie einen lokalen Drucker hinzu und konfigurieren Sie ihn

[Hinzufügen eines neuen lokalen Druckers](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b), den das aktuelle Gerät verwenden kann, um generierte Etiketten vom DRA an die Druckeremulator-Anwendung weiterzuleiten.

1. In Windows wählen Sie **Start** \> **Einstellungen** \> **Geräte** \> **Drucker \& Scanner**.
2. Wählen Sie **Drucker \& Scanner-Einstellungen**.
3. Wählen Sie für **Drucker oder Scanner hinzufügen** die Option **Gerät hinzufügen**.
4. Für **Der gewünschte Drucker ist nicht aufgeführt**, wählen Sie **Manuell hinzufügen**.
5. Im Feld **Drucker über andere Optionen suchen** wählen Sie **Lokalen Drucker oder Netzwerkdrucker mit manuellen Einstellungen hinzufügen**.
6. Wählen Sie im Feld **Wählen Sie einen Druckeranschluss** die Option **Erstellen Sie einen neuen Port**, und führen Sie dann die folgenden Schritte aus:

    1. Wählen Sie im Feld **Typ des Ports** **Standard TCP/IP Port**.
    2. Geben Sie in das Feld **Hostname oder IP-Adresse** **127.0.0.1** ein.
    3. Geben Sie in das Feld **Port** **ZPL** ein.
    4. Warten Sie, bis der Vorgang **Erkennung des TCP/IP-Ports** abgeschlossen ist.
    5. Wählen Sie im Feld **Gerätetyp** die Option **Benutzerdefiniert** und anschließend die Option **Einstellungen**.
    6. Stellen Sie sicher, dass die folgenden Einstellungen für den Port festgelegt sind:

        - **Port Name:** ZPL
        - **Druckername oder IP-Adresse:** 127.0.0.1
        - **Protokoll:** Raw
        - **Port-Nummer:** 9100

7. Wählen Sie im Feld **Installation des Druckertreibers** die Option **Generisch / Nur Text**.
8. Geben Sie in das Feld **Druckername** **ZebraPrinter** ein.

![Hinzufügen eines lokalen Druckers für das aktuelle Gerät.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>Installieren und konfigurieren Sie den DRA

Bereiten Sie den DRA vor, um die von Finance generierten Labels an den konfigurierten lokalen Drucker weiterzuleiten.

1. [Installieren Sie den DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Konfigurieren Sie den DRA](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Registrieren Sie den lokalen Drucker](install-document-routing-agent.md#register-network-printers) im DRA.
4. [Aktivieren Sie den lokalen Drucker](install-document-routing-agent.md#administer-network-printers) in Ihrer Finance Umgebung.

![Bereiten Sie den DRA für den Druck der generierten Etiketten vor.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>Das Ziel der elektronischen Berichterstellung konfigurieren

Bereiten Sie das ER-Ziel so vor, dass es die generierten Labels von Finance an den DRA weiterleitet.

1. Wählen Sie **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Ziel der elektronischen Berichterstellung**.
2. Wählen Sie auf der Seite **Elektronisches Berichtsziel** im Aktionsbereich **Neu**.
3. Wählen Sie im Feld **Referenz** die Option **Lagerort Etiketten**.
4. Wählen Sie im Inforegister **Dateiziel** die Option **Neu** aus.
5. Geben Sie in das Feld **Name** **Labels** ein.
6. Im Feld **Name der Dateikomponente** wählen Sie **Bericht**.
7. Wählen Sie **Einstellungen**.
8. Legen Sie im Dialogfeld **Zieleinstellungen** auf der Registerkarte **Drucker** die Option **Aktiviert** auf **Ja** fest.
9. Im Feld **Druckername** wählen Sie **ZebraPrinter**.
10. Wählen Sie im Feld **Dokument-Routing-Typ** die Option **ZPL**.
11. Wählen Sie **OK** aus.

![Konfigurieren des ER-Ziels für das Format der Etiketten für Lagerstandorte auf der Seite Ziel für elektronische Berichte.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Lagerstandorte überprüfen

1. Gehen Sie zu **Lagerortverwaltung** \> **Einrichtung** \> **Lagerort** \> **Standorte**.
2. Filtern Sie auf der Seite **Orte**, um nur die Orte anzuzeigen, die einen Wert im Feld **Kontrollziffern** haben.

![Überprüfen der Lagerstandorte auf der Seite Standorte.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Lagerort-Etiketten drucken

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Lagermodell** und wählen Sie **Lagerort Etiketten**.
3. Wählen Sie im Aktivitätsbereich auf **Ausführen**.
4. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter**.
5. Suchen Sie auf der Registerkarte **Bereich** die Zeile, in der das Feld **Tabelle** auf **Orte** und das Feld **Feld** auf **Ort** festgelegt ist. Geben Sie in das Feld **Kriterium** **LPEaktiviert** ein.
6. Wählen Sie **OK** aus.
7. Wählen Sie **OK** aus. Ein Label wird generiert und auf der Vorschauseite in der Druckeremulator-Anwendung angezeigt.

![Überprüfen eines generierten Labels auf der Vorschauseite der Anwendung Zpl-Druckeremulator.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Ändern Sie das Layout eines Labels

Sie können das aktuelle Layout der Etiketten für Ihre Lagerstandorte ändern. Das folgende Beispiel zeigt, wie Sie das Layout so ändern können, dass die generierten Labels eine Standortprofil-ID enthalten.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Legen Sie das Feld **Ziele für Entwurfsstatus verwenden** [ER Benutzerparameter](electronic-reporting-destinations.md#applicability) auf **Ja** fest.
3. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Lagermodell** und wählen Sie **Lagerort Etiketten**.
4. Wählen Sie **Designer** aus.
5. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Zuordnung** die Datenquelle `model.Location.Label`.
6. Im Dialogfeld **Eigenschaften der Datenquelle** wählen Sie **Bearbeiten** \> **Formel bearbeiten**.
7. Überprüfen Sie auf der Seite **Formeldesigner** im Feld **Formel** die ER-Formel, die für die Erstellung von Labels verwendet wird.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Aktualisieren Sie die Formel, um den generierten Labels eine Standortprofil-ID hinzuzufügen.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Wählen Sie **Speichern** aus.
10. Wählen Sie **OK** aus.
11. Wählen Sie im Aktivitätsbereich auf **Ausführen**.
12. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter**.
13. Suchen Sie auf der Registerkarte **Bereich** die Zeile, in der das Feld **Tabelle** auf **Orte** und das Feld **Feld** auf **Ort** festgelegt ist. Geben Sie in das Feld **Kriterien** **Bucht** ein.
14. Wählen Sie **OK** aus.
15. Wählen Sie **OK** aus. Ein Label wird generiert und auf der Vorschauseite in der Druckeremulator-Anwendung angezeigt.

![Überprüfung eines generierten Labels, das eine Standortprofil-ID enthält, auf der Vorschauseite der Anwendung Zpl-Drucker-Emulator.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Codierung

> [!NOTE]
> Sie müssen die Kodierungseinstellung der **Common\\File** Komponente des bearbeitbaren ER-Formats und die entsprechende Einstellung des gestalteten Labels synchronisieren. Der Wert des Feldes **[Kodierung](er-suppress-bom-characters.md)** der Komponente **Common\\File** darf nicht im Widerspruch zu einem ZPL-Befehl stehen, der zur Steuerung der Kodierung des Labels verwendet wird (zum Beispiel der Befehl `^CI`). ER überprüft nicht, ob diese Einstellungen synchronisiert sind.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Druckziel](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
