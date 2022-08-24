---
title: Beispiel zur Integration der Kontrolleinheit für Schweden
description: Dieser Artikel bietet einen Überblick über das Beispiel der Fiskalintegration für Schweden in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 3376e6a901b692371a44b5c74c1e6b4afd0cd573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275065"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Beispiel zur Integration der Kontrolleinheit für Schweden

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet einen Überblick über das Beispiel der Fiskalintegration für Schweden in Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Dieses Beispiel für die fiskalische Integration ersetzt das frühere [Beispiel für die POS-Integration mit Steuereinheiten für Schweden](retail-sdk-control-unit-sample.md). Das frühere Beispiel nutzt nicht die Vorteile des [Fiscal Integration Framework](./fiscal-integration-for-retail-channel.md) und wird in späteren Updates veraltet sein. Informationen darüber, wie Sie von dem früheren Beispiel auf das Beispiel migrieren, das der Dynamics 365 Commerce Version **10.0.22 und früher** entspricht, finden Sie unter [Migration vom früheren Integrationsbeispiel](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Die Commerce-Funktionalität für Schweden enthält ein Beispiel für die Integration des Point of Sale (POS) mit schwedenspezifischen Steuereinheiten, die als *Steuereinheiten* bezeichnet werden. Dieses Beispiel erweitert die [Fiskalintegrationsfunktionalität](fiscal-integration-for-retail-channel.md). Es wird davon ausgegangen, dass eine Steuereinheit physisch mit einer Hardware-Station verbunden ist, mit der die Kasse gekoppelt ist. Dieses Beispiel verwendet als Beispiel die Anwendungsprogrammierschnittstelle (API) der [CleanCash Type A](https://www.retailinnovation.se/produkter) Steuereinheit von Retail Innovation HTT AB. Es wird die Version 1.1.4 der CleanCash API verwendet.

Das Beispiel wird in der Form eines Quellcodes bereitgestellt und ist Teil des Retail Software Development Kit (SDK).

Microsoft gibt keine Hardware, Software oder Belege von Retail Innovation HTT AB frei. Wenn Sie wissen möchten, wie Sie die Steuereinheit erhalten und bedienen können, wenden Sie sich an [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Szenarien

Das Beispiel für die Integration von Steuereinheiten in Schweden umfasst die folgenden Funktionalitäten:

- Verkäufe, Retouren und Quittungskopien werden automatisch in einer Steuereinheit registriert, das mit der Hardware-Station verbunden ist, die mit dem POS gekoppelt ist.
- Der Steuercode und die Herstellungsnummer der Steuereinheit für eine registrierte Transaktion werden von der Steuereinheit erfasst und in der Transaktion gespeichert. Diese Daten werden auch als *Fiskalantwort* bezeichnet. Die fiskalische Antwort kann auf der Seite **Store Transaktionen** eingesehen werden.
- Angepasste Felder für den Steuercode und die Herstellungsnummer der Steuereinheit können zu einem Bonlayout hinzugefügt werden. Auf diese Weise können Sie die fiskalische Antwort für eine Transaktion auf einen Bon drucken.
- Die fiskalische Antwort für eine Transaktion wird auf dem Kanalbericht **Elektronische Erfassung (Schweden)** angezeigt.
- Es stehen mehrere Optionen zur Fehlerbehandlung zur Verfügung. Im Folgenden finden Sie einige Beispiele hierfür:

    - Wiederholen Sie die Fiskalregistrierung, wenn dies möglich ist. Sie können die steuerliche Registrierung wiederholen, wenn z.B. die Steuereinheit nicht verbunden ist, nicht bereit ist oder nicht antwortet.
    - Verschieben Sie die Steuererfassung.
    - Überspringen Sie Steuererfassung, oder markieren Sie die Buchung als erfasst, und schließen Sie Infocodes ein, um den Grund für den Fehler und zusätzliche Informationen zu erfassen.
    - Überprüfen Sie die Verfügbarkeit der Steuereinheit, bevor eine neue Verkaufstransaktion eröffnet oder eine Verkaufstransaktion abgeschlossen wird.

### <a name="limitations-of-the-sample"></a>Einschränkungen des Beispiels

Das Beispiel für die Integration von Steuereinheiten in Schweden unterstützt derzeit keine Kundenauftragsszenarien.

## <a name="setting-up-the-integration-with-control-units"></a>Einrichten der Integration mit Steuereinheiten

Weitere Informationen über die Einrichtung, die für Schweden erforderlich ist, finden Sie unter [Einrichten von Commerce für Schweden](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Konfigurieren der schwedenspezifischen Quittungen

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurieren Sie benutzerdefinierte Felder, damit sie in Belegformate für Verkaufsbelege verwendet werden können

Sie können den Sprachtext und die angepassten Felder, die in den POS-Bonformaten verwendet werden, konfigurieren. Das Standardunternehmen des Benutzers, der die Boneinrichtung erstellt, sollte die gleiche juristische Person sein, in dem die Sprachtexteinstellung erstellt wird. Alternativ sollten dieselben Sprachtexte im Standardunternehmen des Benutzers und in der juristischen Person des Shops verwendet werden, für den das Setup erstellt wird.

Fügen Sie auf der Seite **Sprachentext** die folgenden Datensätze für die Beschriftungen der benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass **Sprachen-ID**, **Text-ID** und **Text**-Werte, die in der Tabelle angezeigt werden, nur Beispiele sind. Sie können sie ändern, damit sie Ihre Anforderungen erfüllen. Die von Ihnen verwendeten **Text-ID**-Werte müssen jedoch eindeutig sein und gleich oder größer als 900001 sein.

Fügen Sie die folgenden POS-Labels in den Abschnitt **POS** der Seite **Sprachentext** ein.

| Sprachkennung | Textkennung | Text                  |
|-------------|---------|-----------------------|
| en-US       | 900001  | Steuereinheit registrieren |
| en-US       | 900002  | Gerät registrieren       |

Fügen Sie auf der Seite **Benutzerdefinierte Felder** die folgenden Datensätze für die benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass die Werte für **Untertitelrext-ID** den Werten **Textkennung** entsprechen müssen, die Sie auf der Seite **Sprachentext** angegeben haben.

| Name                         | Typ    | Textkennung Titel |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Zugang | 900001          |
| SE_FISCALREGISTERID          | Zugang | 900002          |

> [!NOTE]
> Es ist wichtig, dass Sie die richtigen benutzerdefinierten Feldnamen angeben, wie in der vorherigen Tabelle aufgeführt. Ein falscher benutzerdefinierter Feldname führt zu fehlenden Daten in Belegen.

#### <a name="configure-receipt-formats"></a>Bonformate konfigurieren

Ändern Sie für jedes erforderliche Format den Wert des Felds **Druckverhalten** auf **Immer drucken**.

Fügen Sie im Quittungsformat-Designer die folgenden angepassten Felder in den Abschnitt **Fußzeile** ein. Beachten Sie, dass die Feldnamen den Sprachtexten entsprechen, die Sie im vorherigen Abschnitt dieses Artikels definiert haben.

- **Steuereinheit-Code registrieren** - Dieses Feld gibt den Steuercode aus.
- **Gerät registrieren** - In diesem Feld wird die Herstellungsnummer der Steuereinheit ausgedruckt.

Weitere Informationen zum Arbeiten mit Belegformaten finden Sie unter [Belegvorlagen und Drucken](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Steuerliche Integration für Schweden festlegen

Das Beispiel für die Integration der Steuereinheit für Schweden basiert auf der [Fiskalintegrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil des Retail SDK. Das Beispiel befindet sich im Ordner **src\\FiscalIntegration\\CleanCash** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [das Beispiel in release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung der Commerce Runtime (CRT) ist, und einem fiskalischen Konnektor, der eine Erweiterung der Commerce Hardware Station ist. Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die vorherige Version des Retail SDK auf einer virtuellen Maschine (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS) verwenden. Weitere Informationen finden Sie unter [Einsatzrichtlinien für das Beispiel der Integration von Steuereinheiten für Schweden (veraltet)](emea-swe-fi-sample-sdk.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

Schließen Sie die Schritte zur Einrichtung der Fiskalintegration ab, die unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md) festgelegt sind.

1. [Richten Sie einen Steuererfassungsprozesses ein](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Legen Sie außerdem die Einstellungen für die fiskalische Registrierung fest, die [spezifisch für dieses Beispiel der Integration von Einheiten sind](#set-up-the-registration-process).
1. [Legen Sie Einstellungen zur Fehlerbehandlung fest](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurieren Sie die Channel-Komponenten](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Den Erfassungsprozess einrichten

Um den Registrierungsprozess zu aktivieren, folgen Sie diesen Schritten, um die Commerce-Zentrale festzulegen. Weitere Informationen finden Sie unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laden Sie die Konfigurationsdateien für den Fiskalbeleg-Anbieter und den Fiskal-Konnektor herunter:

    1. Öffnen Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository.
    1. Wählen Sie eine korrekte Version des Release Branches entsprechend Ihrer SDK-/Anwendungsversion (zum Beispiel **[Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Öffnen Sie **src \> FiscalIntegration \> CleanCash**.
    1. Laden Sie die Konfigurationsdatei des Anbieters von fiskalischen Belegen herunter unter **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** (zum Beispiel [die Datei für Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. Laden Sie die Konfigurationsdatei des fiskalischen Konnektors unter **HardwareStation \> Connector.CleanCashSample \> Konfiguration \> ConnectorCleanCashSample.xml** herunter (z.B. [die Datei für Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Die Konfigurationsdateien für dieses Beispiel zur Fiskalintegration befinden sich in den folgenden Ordnern des Retail SDK auf einer Entwickler-VM in LCS:
    >
    > - **Konfigurationsdatei für den Anbieter steuerlicher Belege:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **Konfigurationsdatei für den steuerlichen Konnektor:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

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

- **Mehrwertsteuer-Code-Zuordnung** - Diese Zuordnung legt gerätespezifische Mehrwertsteuer-Codes auf entsprechende Umsatzsteuer-Codes fest. Die Zuordnung des MwSt.-Codes sollte das folgende Format haben:

    ```
    1 : code1 ; 2 : code2
    ```

    Hier ist eine Erklärung für dieses Format:

    - *1* und *2* sind gerätespezifische Umsatzsteuercodes.
    - Ein Semikolon (;) wird als Trennzeichen verwendet.
    - *code1* und *code2* sind Mehrwertsteuer-Codes, die in der Commerce-Zentrale konfiguriert werden. Sie müssen die Beispielzuordnung entsprechend den in Ihrer Anwendung konfigurierten Steuerkennzeichen ändern.

    Die Steuereinheiten unterstützen bis zu vier verschiedene MwSt.-Codes. Die Zuordnung des Mehrwertsteuerkennzeichens kann daher wie folgt festgelegt werden:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Mehrere Mehrwertsteuerkennzeichen können demselben gerätespezifischen MwSt.-Code zugeordnet werden.

#### <a name="fiscal-connector-settings"></a>Einstellungen für den Fiscal Konnektor festlegen

Die folgenden Einstellungen sind in der Konfiguration des Fiskalkonnektors enthalten, die als Teil des Beispiels für die Fiskalintegration bereitgestellt wird:

- **Verbindungsstring** - Die Einstellungen für die Verbindung der Einheit.
- **Timeout** - Die Zeitspanne in Millisekunden, die der Treiber auf eine Antwort der Steuereinheit wartet.

### <a name="configure-channel-components"></a>Konfigurieren Sie die Channel-Komponenten

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Weitere Informationen finden Sie unter [Einsatzrichtlinien für das Beispiel der Integration von Steuereinheiten für Schweden (veraltet)](emea-swe-fi-sample-sdk.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

#### <a name="set-up-the-development-environment"></a>Die Umgebung für die Entwicklung festlegen

Um eine Entwicklungsumgebung zum Testen und Erweitern des Beispiels festzulegen, gehen Sie wie folgt vor.

1. Klonen oder laden Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository herunter. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion. Weitere Informationen finden Sie unter [Herunterladen von Retail SDK Beispielen und Referenzpaketen von GitHub und NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Öffnen Sie die Lösung zur Integration der Steuereinheiten unter **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln**, und erstellen Sie sie.
1. Installieren Sie CRT Erweiterungen:

    1. Suchen Sie das Installationsprogramm für die Erweiterung CRT:

        - **Commerce Scale Unit:** Im Ordner **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** finden Sie den **ScaleUnit.CleanCash.Installer** Installer.
        - **Lokal CRT auf Modern POS:** Im **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** Ordner finden Sie den **ModernPOS.CleanCash.Installer** Installer.

    2. Starten Sie das Installationsprogramm für die CRT-Erweiterung über die Befehlszeile:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT auf Modern POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Installieren Sie die Hardware Station Extensions:

    1. Im Ordner **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** finden Sie das **HardwareStation.CleanCash.Installer** Installationsprogramm.
    1. Starten Sie das Installationsprogramm für die Erweiterung über die Befehlszeile:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produktionsumgebung

Legen Sie die Schritte unter [Einrichten einer Build-Pipeline für ein Fiskalintegrationsbeispiel](fiscal-integration-sample-build-pipeline.md) fest, um die Cloud Scale-Unit und die Self-Service bereitstellbaren Pakete für das Fiskalintegrationsbeispiel zu erzeugen und freizugeben. Die **CleanCash build-pipeline.yml** Vorlage YAML-Datei finden Sie im Ordner **Pipeline\\YAML_Files** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository.

## <a name="design-of-the-extensions"></a>Gestaltung der Erweiterungen

Das Beispiel für die Integration der Steuereinheit für Schweden basiert auf der [Fiskalintegrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil des Retail SDK. Das Beispiel befindet sich im Ordner **src\\FiscalIntegration\\CleanCash** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [das Beispiel in release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung von CRT ist, und einem fiskalischen Konnektor, der eine Erweiterung von Commerce Hardware Station ist. Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Weitere Informationen finden Sie unter [Einsatzrichtlinien für das Beispiel der Integration von Steuereinheiten für Schweden (veraltet)](emea-swe-fi-sample-sdk.md). Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

### <a name="crt-extension-design"></a>CRT Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Fiskalbeleg-Anbieter ist, besteht darin, servicespezifische Belege zu erzeugen und Antworten von der Einheit zu verarbeiten.

#### <a name="request-handler"></a>Anforderungshandler

Es gibt einen einzigen **DocumentProviderCleanCash** Request Handler für den Beleg-Anbieter. Dieser Handler wird verwendet, um fiskalische Belege für die Einheit zu erzeugen.

Dieser Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie liefert einen dienstspezifischen Beleg, der in der Einheit registriert werden sollte.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Derzeit werden Verkaufs- und Audit-Ereignisse unterstützt.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Fiskalbeleg-Anbieter befindet sich unter **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** im [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Mit dieser Datei können Sie die Einstellungen für den Beleg-Anbieter von der Commerce-Zentrale aus festlegen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein fiskalischer Konnektor ist, ist die Kommunikation mit der Einheit. Sie verwendet das HTTP-Protokoll, um Belege, die die Erweiterung CRT erzeugt, an die Einheit zu senden. Es behandelt auch die Antworten, die von der Steuereinheit empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der **CleanCashHandler** Request Handler ist der Einstiegspunkt für die Bearbeitung von Anfragen an die Einheit.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** - Diese Anfrage sendet Belege an die Einheit der Steuereinheit und gibt eine Antwort von ihr zurück.
- **IsReadyFiscalDeviceRequest** - Diese Anfrage wird für einen Statuscheck der Steuereinheit verwendet.
- **InitializeFiscalDeviceRequest** - Diese Anfrage wird zur Initialisierung der Steuereinheit verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Fiskalkonnektor befindet sich unter **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** im [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Der Zweck der Datei besteht darin, die Konfiguration der Einstellungen für den Fiskalkonnektor von der Commerce-Zentrale aus zu ermöglichen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
