---
title: Beispiel für Belegdruckerintegration für Polen
description: Dieser Artikel bietet einen Überblick über das Beispiel der Fiskalintegration für Polen in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-01.
ms.openlocfilehash: 52710252d78d34c444de2d40e16423868b12b5c1
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336685"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Beispiel für Belegdruckerintegration für Polen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dieser Artikel bietet einen Überblick über das Beispiel der Fiskalintegration für Polen in Microsoft Dynamics 365 Commerce.

Die Dynamics 365 Commerce-Funktionalität für Polen beinhaltet ein Beispiel für die Integration des Point of Sale (POS) mit einem Fiskaldrucker. Das Beispiel erweitert die [Fiskal-Integrationsfunktionalität](fiscal-integration-for-retail-channel.md) und unterstützt das POSNET THERMAL HD 2.02 Protokoll für Fiskaldrucker von [Posnet Polska S.A.](https://www.posnet.com.pl) Das Beispiel ermöglicht die Kommunikation mit einem Fiskaldrucker, der über einen COM Hafen angeschlossen ist, indem ein nativer Software Fahrer verwendet wird. Sie wurde mit Hilfe eines Softwareemulators implementiert und getestet, den Posnet für den Fiskaldrucker Posnet Thermal HD FV EJ zur Verfügung gestellt hat. Das Beispiel wird in der Form eines Quellcodes bereitgestellt und ist Teil des Commerce Software Development Kit (SDK).

Microsoft gibt keine Hardware, Software oder Belege von Posnet frei. Wenn Sie wissen möchten, wie Sie den Fiskaldrucker erhalten und bedienen können, wenden Sie sich an [Posnet Polska S.A.](https://www.posnet.com.pl).

## <a name="scenarios"></a>Szenarien

Die folgenden Szenarien werden durch das Beispiel der Fiskaldrucker-Integration für Polen abgedeckt:

- Verkaufsszenarien:

    - Druck eines Kassenbons für Cash-and-Carry-Verkäufe und Retouren.
    - Erfassen Sie eine Antwort vom Fiskaldrucker und speichern Sie sie in der Channel-Datenbank.
    - Steuern:

        - Zuordnung zu den Steuercodes (Abteilungen) des Fiskaldruckers.
        - Übertragen Sie zugeordnete Steuerdaten an den Fiskaldrucker.

    - Zahlungen:

        - Zuordnung zu den Zahlungsarten des Fiskaldruckers.
        - Drucken Sie Zahlungen auf einem Fiskalbeleg.
        - Änderungsinformationen drucken.

    - Positionsrabattbetrag drucken.
    - Geschenkkarten:

        - Schließen Sie eine ausgegebene/aufgeladene Zeile einer Geschenkkarte aus einem Steuerbeleg für einen Verkauf aus.
        - Drucken Sie eine Zahlung, die eine Geschenkkarte als reguläre Zahlungsmethode verwendet.

    - Drucken Sie Fiskalquittungen für Vorgänge bei Kundenbestellungen:

        - Für die Einzahlung einer Kundenbestellung wird kein Steuerbeleg gedruckt.
        - Drucken Sie eine Quittung für Carry-Out-Zeilen eines hybriden Kundenauftrags.
        - Drucken Sie einen Kassenbon für den Vorgang der Abholung eines Kundenauftrags.
        - Drucken Sie eine Quittung für eine Rücklieferung.

    - Drucken Sie die [Kundeninformationen](emea-pol-customer-information.md), die für eine Verkaufstransaktion angegeben wurden, auf einem Fiskalbeleg. Ein Beispiel für diese Informationen ist die Umsatzsteuernummer des Kunden.

- Tagesendabschlüsse (Fiskalische X- und Fiskalische Z-Berichte).
- Fehlerbehebung, wie beispielsweise die folgenden Optionen:

    - Wiederholen Sie die Fiskalregistrierung, wenn ein erneuter Versuch möglich ist, z.B. wenn der Fiskaldrucker nicht angeschlossen ist, nicht bereit ist oder nicht reagiert, der Drucker kein Papier mehr hat oder ein Papierstau vorliegt.
    - Verschieben Sie die Steuererfassung.
    - Überspringen Sie Steuererfassung, oder markieren Sie die Buchung als erfasst, und schließen Sie Infocodes ein, um den Grund für den Fehler und zusätzliche Informationen zu erfassen.
    - Prüfen Sie die Verfügbarkeit des Fiskaldruckers, bevor eine neue Verkaufstransaktion eröffnet oder eine Verkaufstransaktion abgeschlossen wird.

### <a name="gift-cards"></a>Geschenkkarten

Das Fiskaldrucker-Integrationsbeispiel implementiert die folgenden Regeln, die sich auf Geschenkkarten beziehen:

- Schließen Sie Verkaufszeilen, die mit den Vorgängen *Geschenkkarte ausgeben* und *Zu Geschenkkarte hinzufügen* verbunden sind, vom Fiskalbon aus.
- Drucken Sie keine Fiskalquittung, wenn sie nur aus Zeilen für Geschenkkarten besteht.
- Ziehen Sie den Gesamtbetrag der Geschenkkarten, die in einer Transaktion ausgegeben oder wieder aufgeladen werden, von den Zahlungszeilen des Fiskalbons ab.
- Speichern Sie berechnete Zahlungsregulierungspositionen in der Kanaldatenbank mit einem Verweis auf eine entsprechende Steuerbuchung.
- Zahlung per Geschenkkarte wird als eine normale Zahlung betrachtet.

### <a name="customer-deposits-and-customer-order-deposits"></a>Debitoreneinzahlungen und Debitorenauftragseinzahlungen

Das Beispiel der Fiskaldrucker-Integration implementiert die folgenden Regeln, die sich auf Kundeneinlagen und Kundenauftragseinlagen beziehen:

- Drucken Sie keine Quittung, wenn es sich bei einer Transaktion um eine Kundeneinzahlung handelt.
- Drucken Sie keinen Kassenbon, wenn eine Transaktion nur eine Einzahlung auf eine Kundenbestellung oder eine Rückerstattung einer Kundenbestellung enthält.
- Drucken Sie den Betrag der zuvor geleisteten Anzahlung auf einem Fiskalbeleg für einen Vorgang zur Abholung eines Kundenauftrags.
- Ziehen Sie den Debitorenauftragseinzahlungsbetrag von den Zahlungspositionen ab, wenn ein hybrider Kundenauftrag erstellt wird.
- Speichern Sie berechnete Zahlungsregulierungspositionen in der Kanaldatenbank mit einem Verweis auf eine Steuerbuchung für einen hybriden Debitorenauftrag.

### <a name="limitations-of-the-sample"></a>Einschränkungen des Beispiels

- Der Fiskaldrucker unterstützt nur Szenarien, bei denen die Mehrwertsteuer im Preis enthalten ist. Daher muss die Option **Preis in Mehrwertsteuer enthalten** auf **Ja** sowohl für Geschäfte als auch Debitoren festgelegt werden.
- Tagesberichte (Fiskal X und Fiskal Z) werden unter Verwendung des eingebetteten Formats *Schichtbericht* gedruckt.
- Das Drucken eines Strichcodes auf Fiskalquittungen wird als potenzielle Anpassung betrachtet, da diese Funktion in den eingebetteten Formaten nicht unterstützt wird und nur mit dem anpassbaren Bericht **Superformat** implementiert werden kann.
- Der Fiskaldrucker unterstützt keine gemischten Transaktionen. Die Option **Verkäufe und Retouren auf einem Bon nicht mischen** sollte in den Profilen der POS-Funktionalität auf **Ja** festgelegt werden.

## <a name="set-up-fiscal-integration-for-poland"></a>Steuerliche Integration für Polen festlegen

Das Beispiel für die Integration des Belegdruckers für Polen basiert auf der [Steuerintegrationsfunktion](fiscal-integration-for-retail-channel.md) und ist Teil des Commerce SDK. Das Beispiel befindet sich im Ordner **src\\FiscalIntegration\\Posnet** des Respository [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Das [Beispiel](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) besteht aus einem Anbieter von Steuerbelegen, der eine Erweiterung der Commerce Runtime (CRT) ist, und einem Steuerconnector, der eine Erweiterung der Commerce Hardwarestation ist. Weitere Informationen zur Verwendung des Commerce SDK finden Sie unter [Laden Sie Beispiele und Referenzpakete für das Retail SDK von GitHub und NuGet herunter](../dev-itpro/retail-sdk/sdk-github.md) und [Buildpipeline für das unabhängige Verpackungs-SDK einrichten](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Das Beispiel für die Integration des Belegdruckers für Polen ist im Commerce SDK ab Commerce-Version 10.0.29 verfügbar. In der Commerce Version 10.0.28 oder früher müssen Sie die frühere Version des Retail SDK auf einem virtuellen Computer (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS) verwenden. Weitere Informationen finden Sie unter [Richtlinien für die Bereitstellung des Beispiels für die Integration von Fiskaldruckern für Polen (veraltet)](emea-pol-fpi-sample-sdk.md).

Schließen Sie die Schritte zur Einrichtung der Fiskalintegration ab, die unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md) festgelegt sind.

1. [Richten Sie einen Steuererfassungsprozesses ein](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Notieren Sie sich auch die Einstellungen für den Prozess der steuerlichen Registrierung, die [spezifisch für dieses Beispiel der Steuerdrucker-Integration sind](#set-up-the-registration-process).
1. [Legen Sie Einstellungen zur Fehlerbehandlung fest](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Fiskalische X/Z-Berichte vom POS festlegen](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurieren Sie die Channel-Komponenten](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Den Erfassungsprozess einrichten

Um den Registrierungsprozess zu aktivieren, folgen Sie diesen Schritten, um die Commerce-Zentrale festzulegen. Weitere Informationen finden Sie unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laden Sie die Konfigurationsdateien für den Fiskalbeleg-Anbieter und den Fiskal-Konnektor herunter:

    1. Öffnen Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository.
    1. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion.
    1. Öffnen Sie **src \> FiscalIntegration \> Posnet**.
    1. Laden Sie die Konfigurationsdatei des Anbieters von Steuerbelegen unter **CommerceRuntime \> DocumentProvider.PosnetSample \> Konfiguration \> DocumentProviderPosnetSample.xml** herunter.
    1. Laden Sie die Konfigurationsdatei des Steuerconnectors herunter unter **HardwareStation \> ThermalDeviceSample \> Konfiguration \> ConnectorPosnetThermalFVEJ.xml**.

    > [!NOTE]
    > In der Commerce Version 10.0.28 oder früher müssen Sie die frühere Version des Retail SDK auf VM für Entwickler in LCS verwenden. Die Konfigurationsdateien für dieses Beispiel zur Fiskalintegration befinden sich in den folgenden Ordnern des Retail SDK auf einer Entwickler-VM in LCS:
    >
    > - **Konfigurationsdatei für Anbieter steuerlicher Belege:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **Konfigurationsdatei für den steuerlichen Konnektor:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter**. Auf der Registerkarte **Allgemein** legen Sie die Option **Steuerintegration aktivieren** auf **Ja** fest.
1. Gehen Sie zu **Handel und Commerce \> Channel-Einrichtung \> Fiskalische Integration \> Fiskalische Belege**, und laden Sie die Konfigurationsdatei des Fiskalischen Belegs, die Sie zuvor heruntergeladen haben.
1. Gehen Sie zu **Retail und Commerce \> Channel Einrichtung \> Fiskalische Integration \> Fiskalische Konnektoren**, und laden Sie die Konfigurationsdatei für den Fiskalischen Konnektor, die Sie zuvor heruntergeladen haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Konnektorfunktionsprofile**. Erstellen Sie ein neues funktionales Profil für den Konnektor. Wählen Sie den Beleg-Anbieter und den Konnektor, den Sie zuvor geladen haben. Aktualisieren Sie die [Einstellungen für die Datenzuordnung](#default-data-mapping) nach Bedarf.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Technische Profile des Connectors**. Erstellen Sie ein neues technisches Profil für den Konnektor und wählen Sie den Fiskalkonnektor, den Sie zuvor erstellt haben. Aktualisieren Sie die [Konnektor-Einstellungen](#fiscal-connector-settings) nach Bedarf.
6. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**. Erstellen Sie eine neue Steuerkonnektorgruppen für das funktionale Konnektorfunktionsprofil, das Sie vorher erstellt haben.
7. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuererfassungsprozesse**. Erstellen Sie einen neuen Fiskalregistrierungsprozess und einen Fiskalregistrierungsprozessschritt und wählen Sie die Fiskalkonnektorgruppe, die Sie zuvor erstellt haben.
8. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**. Wählen Sie ein Funktionsprofil aus, das mit dem Einzelhandelsgeschäft verbunden ist, wo der Erfassungsprozess aktiviert werden soll. Im Inforegister **Steuererfassungsprozess** aktivieren Sie den Steuererfassungsprozess, den Sie vorher erstellt haben.
9. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardwareprofile**. Wählen Sie ein Hardwareprofil aus, das mit der Hardware station verknüpft ist, mit der der Belegdrucker verbunden wird. Im Inforegister **Peripheriegeräte für die Steuerverwaltung** aktivieren Sie das technische Konnektorprofil, das Sie vorher erstellt haben.
10. Öffnen Sie den Vertriebsplan (**Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**), und wählen Sie Jobs **1070** und **1090** aus, um Daten zur Kanaldatenbank zu übertragen.

#### <a name="default-data-mapping"></a>Standarddatenzuordnung

Die folgende Standarddatenzuordnung ist in der Steuerbeleganbieter-Konfiguration enthalten, die als Teil des Steuerintegrationsbeispiels bereitgestellt wird:

- **Zuordnung der Mehrwertsteuersätze** - Die Zuordnung der Steuerprozentwerte, die für die Mehrwertsteuer-Codes festgelegt sind, zu den druckerspezifischen Mehrwertsteuersätzen. Hier ist die Standardzuordnung:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Die erste Komponente in jedem Paar steht für eine Umsatzsteuer-Satznummer, die im Fiskaldrucker konfiguriert ist. Die zweite Komponente stellt den entsprechenden Mehrwertsteuersatz dar. Weitere Informationen über die Konfiguration des Mehrwertsteuersatzes des Fiskaldruckers finden Sie in der Dokumentation des POSNET Treibers.

- **Ausschreibungsart-Zuordnung** - Die Zuordnung von Zahlungsformen, die für den Store konfiguriert sind, zu Zahlungsformularen, die vom Fiskaldrucker unterstützt werden. Hier ist die Standardzuordnung:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Die erste Komponente in jedem Paar steht für eine Zahlungsmethode, die für den Store festgelegt ist. Die zweite Komponente steht für das entsprechende Formular, das von der Steuerdruckerei unterstützt wird. Weitere Informationen zu den Formularen, die der Fiskaldrucker unterstützt, finden Sie in der Dokumentation zum POSNET Fahrer. Sie müssen die Beispielzuordnung entsprechend den in Ihrer Anwendung konfigurierten Zahlungsformen ändern.

#### <a name="fiscal-connector-settings"></a>Einstellungen für den Fiscal Konnektor festlegen

Die folgenden Einstellungen sind in der Konfiguration des Fiskalkonnektors enthalten, die als Teil des Beispiels für die Fiskalintegration bereitgestellt wird:

- **Verbindungsstring** - Ein String, der die Details der Verbindung zum Gerät in einem Format beschreibt, das vom Treiber unterstützt wird. Weitere Informationen finden Sie in der Dokumentation des POSNET Treibers.
- **Datum- und Uhrzeitsynchronisation** – Ein Wert, der angibt, ob Datum und Uhrzeit des Druckers mit der angeschlossenen Hardwarestation synchronisiert werden müssen.
- **Geräte-Timeout** - Die Zeitspanne in Millisekunden, die der Fahrer auf eine Antwort vom Gerät wartet. Weitere Informationen finden Sie in der Dokumentation des POSNET Treibers.

### <a name="configure-channel-components"></a>Konfigurieren Sie die Channel-Komponenten

> [!NOTE]
> - Das Beispiel für die Integration des Belegdruckers für Polen ist im Commerce SDK ab Commerce-Version 10.0.29 verfügbar. In der Commerce Version 10.0.28 oder früher müssen Sie die frühere Version des Retail SDK auf VM für Entwickler in LCS verwenden. Weitere Informationen finden Sie unter [Richtlinien für die Bereitstellung des Beispiels für die Integration von Fiskaldruckern für Polen (veraltet)](emea-pol-fpi-sample-sdk.md).
> - Commerce-Beispiele, die in Ihrer Umgebung bereitgestellt werden, werden nicht automatisch aktualisiert, wenn Sie Dienst- oder Qualitätsupdates auf Commerce-Komponenten durchführen. Sie müssen die erforderlichen Beispiele manuell aktualisieren.

#### <a name="set-up-the-development-environment"></a>Die Umgebung für die Entwicklung festlegen

Um eine Entwicklungsumgebung zum Testen und Erweitern des Beispiels festzulegen, gehen Sie wie folgt vor.

1. Klonen oder laden Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository herunter. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion. Weitere Informationen finden Sie unter [Herunterladen von Commerce SDK Beispielen und Referenzpaketen von GitHub und NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Öffnen Sie die Fiskaldrucker-Integrationslösung unter **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln** und erstellen Sie sie.
1. Installieren Sie CRT Erweiterungen:

    1. Suchen Sie das Installationsprogramm für die Erweiterung CRT:

        - **Commerce Scale Unit:** Im Ordner **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** finden Sie das Installationsprogramm **ScaleUnit.Posnet.Installer**.
        - **Lokal CRT auf Modern POS:** Im Ordner **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** finden Sie den **ModernPOS.Posnet.Installer** Installer.

    1. Starten Sie das Installationsprogramm für die CRT-Erweiterung über die Befehlszeile:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT auf Modern POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Installieren Sie die Hardware Station Extensions:

    1. Im Ordner **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** finden Sie das Installationsprogramm **HardwareStation.PosnetThermalFVFiscalPrinter.Installer**.
    1. Starten Sie das Installationsprogramm für die Erweiterung über die Befehlszeile:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produktionsumgebung

Legen Sie die Schritte unter [Einrichten einer Build-Pipeline für ein Fiskalintegrationsbeispiel](fiscal-integration-sample-build-pipeline.md) fest, um die Cloud Scale-Unit und die Self-Service bereitstellbaren Pakete für das Fiskalintegrationsbeispiel zu erzeugen und freizugeben. Die **Posnet build-pipeline.yml** Vorlage YAML-Datei finden Sie im Ordner **Pipeline\\YAML_Files** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

Das Beispiel für die Integration des Belegdruckers für Polen basiert auf der [Steuerintegrationsfunktion](fiscal-integration-for-retail-channel.md) und ist Teil des Commerce SDK. Das Beispiel befindet sich im Ordner **src\\FiscalIntegration\\Posnet** des Respository [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Das [Beispiel](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) besteht aus einem Anbieter von Steuerbelegen, der eine Erweiterung von CRT ist, und einem Steuerconnector, der eine Erweiterung von Commerce Hardwarestation ist. Weitere Informationen zur Verwendung des Commerce SDK finden Sie unter [Laden Sie Beispiele und Referenzpakete für das Retail SDK von GitHub und NuGet herunter](../dev-itpro/retail-sdk/sdk-github.md) und [Buildpipeline für das unabhängige Verpackungs-SDK einrichten](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Das Beispiel für die Integration des Belegdruckers für Polen ist im Commerce SDK ab Commerce-Version 10.0.29 verfügbar. In der Commerce Version 10.0.28 oder früher müssen Sie die frühere Version des Retail SDK auf VM für Entwickler in LCS verwenden. Weitere Informationen finden Sie unter [Richtlinien für die Bereitstellung des Beispiels für die Integration von Fiskaldruckern für Polen (veraltet)](emea-pol-fpi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter druckerspezifische Dokumente erzeugt und Antworten aus dem Steuerdrucker handhabt. Diese Erweiterung generiert eine Reihe von druckerspezifischen Befehlen im Format JavaScript Object Notation (JSON), die in der POSNET-Spezifikation 19-3678 festgelegt sind.

#### <a name="request-handler"></a>Anforderungshandler

Der **DocumentProviderPosnetProtocol** Handler ist der Einstiegspunkt für die Anforderung, Belege vom Fiskaldrucker zu erzeugen.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein druckerspezifisches Dokument zurück, dass im Steuerdrucker erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Derzeit werden die folgenden Ereignisse unterstützt: Verkauf, X-Bericht drucken und Z-Bericht drucken.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Anbieter von Fiskalbelegen befindet sich unter **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** im Repository [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Mit dieser Datei können Sie die Einstellungen des Anbieters von Fiskalbelegen von der Commerce-Zentrale aus festlegen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuerdrucker. Diese Erweiterung ruft die Funktionen des POSNET-Treibers auf, um Befehle, die die CRT-Erweiterung erzeugt, an den Fiskaldrucker zu senden. Es behandelt auch Gerätefehler.

#### <a name="request-handler"></a>Anforderungshandler

Der **FiscalPrinterHandler** request handler ist der Einstiegspunkt für die Bearbeitung der Anfrage an das Fiskalperipheriegerät.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** – Diese Anforderung sendet Dokumente an den Drucker und gibt eine Antwort vom Steuerdrucker zurück.
- **IsReadyFiscalDeviceRequest** – Diese Anforderung wird für eine Integritätsprüfung des Steuererfassungsgeräts verwendet.
- **InitializeFiscalDeviceRequest** – Diese Anforderung wird für Initialisierung des Druckers verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den fiskalischen Konnektor befindet sich unter **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** im Repository [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Der Zweck der Datei besteht darin, die Konfiguration der Einstellungen des Fiskalkonnektors von der Commerce-Zentrale aus zu ermöglichen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
