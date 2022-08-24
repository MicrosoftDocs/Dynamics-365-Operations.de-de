---
title: Bereitstellungsrichtlinien für das Steuerdrucker-Integrationsbeispiel für Italien (Legacy)
description: Dieser Artikel enthält Richtlinien für die Bereitstellung des Beispiels für die steuerliche Druckerintegration für Italien aus dem Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 9e951c1a1ee5c967d2bd67941ff3d19c62b59ba6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279538"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Bereitstellungsrichtlinien für das Steuerdrucker-Integrationsbeispiel für Italien (Legacy)

[!include[banner](../includes/banner.md)]

Dieser Artikel enthält Richtlinien für die Bereitstellung des Steuerdrucker-Integrationsbeispiels für Italien aus dem Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK) auf einer virtuellen Entwicklermaschine (VM) in Microsoft Dynamics Lifecycle Service (LCS). Weitere Informationen zu den Beispielen für diese steuerliche Integration finden Sie unter [Beispiele für die steuerliche Druckerintegration für Italien](emea-ita-fpi-sample.md). 

Das Steuererfassungsdienst-Integrationsbeispiel für Italien ist Teil des Retail SDK. Informationen zur Installation und Verwendung des SDK finden Sie in der [Retail Software Development Kit (SDK)-Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dieses Beispiel besteht aus Erweiterungen für die Commerce Runtime (CRT) und Hardwarestation. Um dieses Beispiel auszuführen, müssen Sie die CRT und Hardwarestation-Projekte ändern und erstellen. Es wird empfohlen, dass Sie ein unverändertes Retail SDK verwenden, um die Änderungen vorzunehmen, die in diesem Artikel beschrieben werden. Es wird außerdem empfohlen, dass Sie ein Quellsteuerungssystem verwenden, wie Azure DevOps bei dem noch keine Dateien geändert wurden.

## <a name="development-environment"></a>Entwicklungsumgebung

Gehen Sie folgendermaßen vor, um eine Entwicklungsumgebung einzurichten, damit Sie das Beispiel testen und erweitern können.

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime Erweiterungskomponenten

Die CRT Erweiterungskomponenten sind in den Retail SDK enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **CommerceRuntimeSamples.sln** unter **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** und erstellen Sie es.
2. Im Ordner **Extensions.DocumentProvider.EpsonFP90IIISample\\Behälter\\Debuggen** suchen Sie die Assembly-Datei **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Commerce Scale Unit:** Kopieren Sie die Datei in den Ordner **\\bin\\ext** unter dem Microsoft Internet Information Services (IIS) Commerce Scale Unit Standort.
    - **Lokal CRT auf Modern POS:** Kopieren Sie die Datei in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Commerce Scale Unit neu starten:

    - **-Commerce Scale Unit:** Starten Sie die Commerce Scale Unit-Site über den IIS-Manager neu.
    - **Kundenmakler:** Beendet den **dllhost.exe** Prozess im Task-Manager und startt den Modern POS neu.

### <a name="hardware-station-extension-components"></a>Hardware Station-Erweiterungskomponenten

Die Hardwaresations-Erweiterungskomponenten sind in der Retail SDK enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **HardwareStationSamples.sln.sln** unter **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Suchen Sie das Projekt **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample**, und erstellen Sie es.
2. Im Ordner **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** suchen Sie die Assembly-Datei **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll**.
3. Kopieren Sie die Assemblydatei auf eine bereitgestellte Hardwarestationsmaschine:

    - **Remote-Hardware-Station** Kopieren Sie die Dateien in den Ordner **Intervall** unter dem IIS Hardware Stations-Sitespeicherort.
    - **Lokale Hardwarestation:** Kopieren Sie die Dateien zum Modern POS-Client-Broker-Speicherort.

4. Suchen Sie die Konfigurationsdatei für die Erweiterungen der Hardwarestationserweiterung. Die Datei hat den Namen **HardwareStation.Extension.config**:

    - **Remote-Hardwarestation:** Die Datei befindet sich unter dem IIS Hardwarestation-Websitespeicherort.
    - **Lokale Hardwarestation:** Die Datei befindet sich unter dem Modern POS-Client-Broker-Speicherort.

5. Fügen Sie den folgenden Abschnitt dem Abschnitt **Anordnung** der Konfigurationsdatei hinzu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Starten Sie den Hardwarestationsdienst neu:

    - **Remote-Hardware-Station:** Starten Sie die Hardwarestationssite über den IIS-Manager neu.
    - **Lokale Hardwarestation:** Beendet den **dllhost.exe** Prozess im Task-Manager und startet den Modern POS neu.

## <a name="production-environment"></a>Produktionsumgebung

Um bereitstellbare Pakete zu erstellen, die Commerce-Komponenten enthalten, und diese Pakete in einer Produktionsumgebung anzuwenden, müssen Sie folgenden Schritten folgen.

1. Führen Sie die Schritte aus, die im Abschnitt [Entwicklungsumgebung](#development-environment) weiter oben in diesem Artikel beschrieben sind.
2. Nehmen Sie die folgenden Änderungen in den Paketkonfigurationsdateien unter dem Ordner **RetailSdk\\Assets** vor:

    1. In den Konfigurationsdateien **commerceruntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** fügen Sie die folgenden Positionen zum Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. In der Konfigurationsdatei **HardwareStation.Extension.config** fügen Sie die folgende Position dem Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Nehmen Sie die folgenden Änderungen in der Paketanpassungs-Konfigurationsdatei **Anpassungs-Einstellungen** im Ordner **BuildTools** vor:

    1. Fügen Sie die folgende Position hinzu, um die CRT Erweiterungen in die bereitstellbaren Paketen einzuschließen.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Fügen Sie die folgende Zeilen hinzu, um die Hardware station-Erweiterung in die bereitstellbaren Pakete einzuschließen.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Nehmen Sie die folgenden Änderungen in der Datei **Sdk.ModernPos.Shared.csproj** unter dem Ordner **Packages\_SharedPackagingProjectComponents** vor, um die Ressourcendateien für Italien in bereitzustellende Pakete aufzunehmen:

    1. Fügen Sie einen **ItemGroup** Abschnitt hinzu, der Knoten enthält, die auf die Ressourcendateien für die gewünschten Übersetzungen verweisen. Vergewissern Sie sich, dass Sie die richtigen Namensräume und Musternamen angeben. Das folgende Beispiel fügt Ressourcenknoten für die Gebietskörperschaften **it** und **it-CH** hinzu.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Fügen Sie im Abschnitt **Target Name="CopyPackageFiles"** eine Zeile für jedes Gebietsschema hinzu, wie im folgenden Beispiel gezeigt.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Nehmen Sie die folgenden Änderungen in der Datei **Sdk.RetailServerSetup.proj** im Ordner **Packages\_SharedPackagingProjectComponents** vor, um die Ressourcendateien für Italien in bereitzustellende Pakete aufzunehmen:

    1. Fügen Sie einen **ItemGroup** Abschnitt hinzu, der Knoten enthält, die auf die Ressourcendateien für die gewünschten Übersetzungen verweisen. Vergewissern Sie sich, dass Sie die richtigen Namensräume und Musternamen angeben. Das folgende Beispiel fügt Ressourcenknoten für die Gebietskörperschaften **it** und **it-CH** hinzu.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Fügen Sie im Abschnitt **Target Name="CopyPackageFiles"** eine Zeile für jedes Gebietsschema hinzu, wie im folgenden Beispiel gezeigt.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Starten Sie die MSBuild-Eingabeaufforderung für Visual Studio-Hilfsprogramm und führen Sie dann **msbuild** unter dem Ordner Retail SDK aus, um bereitstellbare Pakete zu erstellen.
7. Übernehmen Sie die Pakete über Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Bereitstellbare Pakete erstellen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter druckerspezifische Dokumente erzeugt und Antworten aus dem Steuerdrucker handhabt.

Die CRT-Erweiterung ist **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Weitere Informationen über den Aufbau der Fiskalintegrationslösung finden Sie unter [Fiskalischer Registrierungsprozess und Fiskalintegrationsbeispiele für Fiskalgeräte und -dienste](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Anforderungshandler

Der **DocumentProviderEpsonFP90III** Anforderungshandler ist der Einstiegspunkt für die Anforderung zum Generieren von Dokumenten vom Steuerdrucker.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein druckerspezifisches Dokument zurück, dass im Steuerdrucker erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Derzeit werden die folgenden Ereignisse unterstützt: Verkauf, X-Bericht drucken und Z-Bericht drucken.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Der Zweck der Datei ist es, Einstellungen zu aktivieren, damit der Dokumentanbieter von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- Zuordnung von MwSt.-Codes
- Zuordnung von MwSt.-Sätzen
- Zahlungsmitteltyp-Zuordnung
- Strichcodetyp für Zugangsnummer
- Zahlungsart für Einzahlungen

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuerdrucker.

Die Hardwarestation-Erweiterung ist **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Diese Erweiterung verwendet das HTTP-Protokoll, um Dokumente, die die CRT-Erweiterung generiert, zum Steuerdrucker zu übermitteln. Sie handhabt auch die Antworten, die vom Steuerdrucker empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der Anforderungshandler **EpsonFP90IIISample** ist der Einstiegspunkt für die Handhabung von Anforderungen an das Steuererfassungsgerät.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** – Diese Anforderung sendet Dokumente an den Drucker und gibt eine Antwort vom Steuerdrucker zurück.
- **IsReadyFiscalDeviceRequest** – Diese Anforderung wird für eine Integritätsprüfung des Steuererfassungsgeräts verwendet.
- **InitializeFiscalDeviceRequest** – Diese Anforderung wird für Initialisierung des Druckers verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Der Zweck dieser Datei ist es, Einstellungen zu aktivieren, damit der Konnektor von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- **Endpunktadresse** – Die URL des Druckers.
- **Datum- und Uhrzeitsynchronisation** – Ein Wert, der angibt, ob Datum und Uhrzeit des Druckers mit der angeschlossenen Hardwarestation synchronisiert werden müssen.
