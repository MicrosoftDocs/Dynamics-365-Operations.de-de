---
title: Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für die Tschechische Republik (Legacy)
description: Dieser Artikel enthält Richtlinien für die Bereitstellung des Beispiels für die steuerliche Integration für die Tschechische Republik aus dem Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: d689e5b48fb8274a58d0c3a18e70b598aca2c310
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287537"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für die Tschechische Republik (Legacy)

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Richtlinien für die Bereitstellung des Integrationsbeispiels für den Steuerregistrierungsdienst für die Tschechische Republik aus dem Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK) auf einer virtuellen Entwicklermaschine (VM) in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen zu den Beispielen für diese steuerliche Integration finden Sie unter [Beispiele für die steuerliche Integration für die Tschechische Republik](emea-cze-fi-sample.md). 

Das Steuererfassungsdienst-Integrationsbeispiel für die Tschechische Republik ist Teil des Retail SDK. Informationen zur Installation und Verwendung des SDK finden Sie in der [Retail Software Development Kit (SDK)-Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dieses Beispiel besteht aus Erweiterungen für die Commerce Runtime (CRT) und Hardwarestation. Um dieses Beispiel auszuführen, müssen Sie die CRT und Hardwarestation-Projekte ändern und erstellen. Es wird empfohlen, dass Sie ein unverändertes Retail SDK verwenden, um die Änderungen vorzunehmen, die in diesem Artikel beschrieben werden. Es wird außerdem empfohlen, dass Sie ein Quellsteuerungssystem verwenden, wie Azure DevOps bei dem noch keine Dateien geändert wurden.

## <a name="development-environment"></a>Entwicklungsumgebung

Gehen Sie folgendermaßen vor, um eine Entwicklungsumgebung einzurichten, damit Sie das Beispiel testen und erweitern können.

### <a name="enable-commerce-runtime-extensions"></a>Commerce-Laufzeiterweiterungen aktivieren

Die CRT-Erweiterungskomponenten sind in den CRT-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **CommerceRuntimeSamples.sln** unter **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample-Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.EFRSample**, und erstellen Sie es.
2. Im Ordner **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** suchen Sie die Assembly-Datei **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Commerce Scale Unit:** Kopieren Sie die Datei in den Ordner **\\bin\\ext** unter dem Microsoft Internet Information Services (IIS) Commerce Scale Unit Standort.
    - **Lokal CRT auf Modern POS:** Kopieren Sie die Datei in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR-Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.DataModelEFR**, und erstellen Sie es.
2. Im Ordner **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** suchen Sie die Assembly-Datei **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Commerce Scale Unit:** Kopieren Sie die Datei in den Ordner **\\bin\\ext** unter dem Standort der IIS Commerce Scale Unit.
    - **Lokal CRT auf Modern POS:** Kopieren Sie die Datei in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Erweiterungskonfigurationsdatei

1. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

2. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Erweiterungen für steuerliche Konnektoren aktivieren

Sie können fiskalische Konnektor-Erweiterungen auf der [Hardware-Station](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) oder dem [POS-Register](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network) aktivieren.

### <a name="enable-hardware-station-extensions"></a>Hardware station-Erweiterungen aktivieren

Die Hardware station-Erweiterungskomponenten sind in den Hardware station-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **HardwareStationSamples.sln.sln** unter **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>EFRSample-Komponente

1. Suchen Sie das Projekt **HardwareStation.Extension.EFRSample**, und erstellen Sie es.
2. Im Ordner **Extension.EFRSample\\bin\\Debug** suchen Sie die folgende Assembly-Dateien:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopieren Sie die Assembly-Dateien in den Hardware stations-Erweiterungsordner:

    - **Freigegebene Hardware station:** Kopieren Sie die Dateien in den Ordner **Lagerfach** unter dem IIS Hardware stations-Websitespeicherort.
    - **Dedizierte Hardware station auf Modern POS:** Kopieren Sie die Dateien zum Modern POS-Client-Broker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für die Erweiterungen der Hardware station. Die Datei hat den Namen **HardwareStation.Extension.config**.

    - **Freigegebene Hardware station:** Die Datei befindet sich unter dem IIS Hardware station-Websitespeicherort.
    - **Dedizierte Hardware station auf Modern POS:** Die Datei befindet sich unter dem Modern POS-Client-Broker-Speicherort.

5. Fügen Sie die folgende Position zum Abschnitt **Anordnung** der Konfigurationsdatei hinzu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>POS-Erweiterungen aktivieren

Das Beispiel für die POS-Erweiterung befindet sich im Ordner **src\\FiscalIntegration\\PosFiscalConnectorSample** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository.

Um das Beispiel der POS-Erweiterung im veralteten SDK zu verwenden, führen Sie diese Schritte aus.

1. Kopieren Sie den Ordner **Pos.Extension** in den Ordner POS **Extensions** des veralteten SDK (zum Beispiel `C:\RetailSDK\src\POS\Extensions`).
1. Benennen Sie die Kopie des Ordners **Pos.Extension** in **PosFiscalConnector** um.
1. Entfernen Sie die folgenden Ordner und Dateien aus dem Ordner **PosFiscalConnector**:

    - bin
    - DataService
    - devDependencies
    - Bibliotheken
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Öffnen Sie die **CloudPos.sln** oder **ModernPos.sln** Lösung.
1. Nehmen Sie in das Projekt **Pos.Extensions** den Ordner **PosFiscalConnector** auf.
1. Öffnen Sie die Datei **extensions.json**, und fügen Sie die Erweiterung **PosFiscalConnector** hinzu.
1. Erstellen Sie das SDK.

### <a name="production-environment"></a>Produktionsumgebung

Die vorherige Prozedur aktiviert die Erweiterungen, die Komponenten des Steuererfassungsdienst-Integrationsbeispiels sind. Darüber hinaus müssen Sie diese Schritte ausführen, um bereitstellbare Pakete zu erstellen, die Commerce-Komponenten enthalten, und diese Pakete in einer Produktionsumgebung anzuwenden.

1. Nehmen Sie die folgenden Änderungen in den Paketkonfigurationsdateien unter dem Ordner **RetailSdk\\Assets** vor:

    - In den Konfigurationsdateien **commerceruntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** fügen Sie die folgenden Positionen zum Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - In der Konfigurationsdatei **HardwareStation.Extension.config** fügen Sie die folgende Position dem Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. Nehmen Sie die folgenden Änderungen in der Paketanpassungs-Konfigurationsdatei **Anpassungs-Einstellungen** im Ordner **BuildTools** vor.

    - Fügen Sie die folgenden Zeilen hinzu, um die CRT-Erweiterungen in die bereitstellbaren Paketen einzuschließen.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Fügen Sie die folgende Zeilen hinzu, um die Hardware station-Erweiterung in die bereitstellbaren Pakete einzuschließen.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Starten Sie die MSBuild-Eingabeaufforderung für Visual Studio-Hilfsprogramm und führen Sie **msbuild** unter dem Ordner Retail SDK aus, um bereitstellbare Pakete zu erstellen.
4. Übernehmen Sie die Pakete über Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Bereitstellbare Pakete erstellen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Schließen Sie alle erforderlichen Setupaufgaben ab, die im Abschnitt [Commerce für die Tschechische Republik einrichten](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic) beschrieben sind.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

Die Beispiele für diese steuerliche Integration für die Tschechische Republik basiert auf der [steuerlichen Integrationsfunktionalität](fiscal-integration-for-retail-channel.md). Weitere Informationen über das Design der Lösung für die steuerliche Integration finden Sie unter [Überblick über die steuerliche Integration für Commerce-Kanäle](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter dienstspezifische Dokumente erzeugt und Antworten aus dem Steuererfassungsdienst handhabt.

Die CRT-Erweiterung ist **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Anforderungshandler

Es gibt einen Anforderungshandler für den Dokumentanbieter: **DocumentProviderEFRFiscalCZE**. Er wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen.

Dieser Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Derzeit werden folgende Ereignisse unterstützt: Verkäufe, Kundenkontoeinlagen und Kundenauftragseinlagen.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Diese Anforderung gibt die Antwort vom Steuererfassungsdienst zurück. Diese Antwort wird serialisiert, um eine Zeichenfolge zu bilden, sodass sie bereit zum Speichern ist.

#### <a name="configuration"></a>Variante

Die **DocumentProviderFiscalEFRSampleCzech** Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Mit dieser Datei können Sie die Einstellungen für den Beleg-Anbieter von der Commerce-Zentrale aus festlegen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- Zuordnung von MwSt.-Sätzen
- MwSt-Standardgruppe
- Mehrwertsteuergruppe einzahlen

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuererfassungsdienst.

Die Hardware-Stationserweiterung hat den Namen **HardwareStation.Extension.EFRSample**. Es verwendet das HTTP- oder HTTPS-Protokoll, um Dokumente, die die Erweiterung CRT erzeugt, an den fiskalischen Registrierungsdienst zu senden. Sie handhabt auch die Antworten, die vom Steuererfassungsdienst empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der Anforderungshandler **EFRHandler** ist der Einstiegspunkt für die Handhabung von Anforderungen an den Steuererfassungsdienst.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** – Diese Anforderung sendet Dokumente an den Steuererfassungsdienst und gibt eine Antwort von ihm zurück.
- **IsReadyFiscalDeviceRequest** – Diese Anforderung wird für eine Integritätsprüfung des Steuererfassungsdiensts verwendet.
- **InitializeFiscalDeviceRequest** – Diese Anforderung wird für Initialisierung des Steuererfassungsdiensts verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Der Zweck der Datei besteht darin, die Konfiguration der Einstellungen für den Fiskalkonnektor von der Commerce-Zentrale aus zu ermöglichen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- **Endpunktadresse** – Die URL des Steuererfassungsdiensts.
- **Timeout** - Die Zeitspanne in Millisekunden, die der Konnektor auf eine Antwort des fiskalischen Registrierungsdienstes warten wird.

### <a name="pos-fiscal-connector-extension-design"></a>Design der POS Fiskalkonnektor-Erweiterung

Der Zweck der POS Fiskalkonnektor-Erweiterung ist die Kommunikation mit dem Fiskalregistrierungsdienst von POS. Sie verwendet das HTTPS-Protokoll für die Kommunikation.

#### <a name="fiscal-connector-factory"></a>Fiscal Konnektor Fabrik

Die Fiskal Connector Fabrik factory ordnet den Namen des Konnektors der Implementierung des Fiskal Connectors zu und befindet sich in der Datei **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. Der Name des Konnektors sollte mit dem Namen des steuerlichen Konnektors übereinstimmen, der in der Commerce-Zentrale angegeben ist.

#### <a name="efr-fiscal-connector"></a>EFR Fiskalischer Konnektor

Der EFR-Fiscal-Konnektor befindet sich in der Datei **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. Es implementiert die Schnittstelle **IFiscalConnector**, die die folgenden Anfragen unterstützt:

- **FiscalRegisterSubmitDocumentClientRequest** - Diese Anfrage sendet Dokumente an den Fiskalregistrierungsdienst und gibt eine Antwort von ihm zurück.
- **FiscalRegisterIsReadyClientRequest** - Diese Anfrage wird für einen Gesundheitscheck des fiskalischen Registrierungsdienstes verwendet.
- **FiscalRegisterInitializeClientRequest** - Diese Anfrage wird zur Initialisierung des fiskalischen Registrierungsdienstes verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Der Zweck der Datei besteht darin, die Konfiguration der Einstellungen für den Fiskalkonnektor von der Commerce-Zentrale aus zu ermöglichen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- **Endpunktadresse** – Die URL des Steuererfassungsdiensts.
- **Timeout** - Die Zeitspanne in Millisekunden, die der Konnektor auf eine Antwort des fiskalischen Registrierungsdienstes warten wird.
