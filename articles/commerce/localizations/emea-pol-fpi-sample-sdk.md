---
title: Leitfaden für die Bereitstellung des Beispiels für die Integration des Fiskaldruckers für Polen (veraltet)
description: Dieser Artikel enthält Richtlinien zum Bereitstellen des Beispiels für die Integration von Fiskaldruckern in Polen aus dem Software Development Kit (SDK) für Microsoft Dynamics 365 Commerce Retail.
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 178301e6d8e5f87376ed893e4bf5f966260cad62
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336717"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Leitfaden für die Bereitstellung des Beispiels für die Integration des Fiskaldruckers für Polen (veraltet)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Sie sollten die Richtlinien in diesem Artikel nur befolgen, wenn Sie Microsoft Dynamics 365 Commerce der Version 10.0.28 oder früher verwenden. Ab Commerce Version 10.0.29 ist das Beispiel für die Integration des Belegdruckers für Polen im Commerce Software Development Kit (SDK) verfügbar. Weitere Informationen finden Sie unter [Kanalkomponenten konfigurieren](./emea-pol-fpi-sample.md#configure-channel-components).

Dieser Artikel enthält Richtlinien für die Bereitstellung des Belegdrucker-Integrationsbeispiels für Polen aus dem Dynamics 365 Commerce Retail SDK auf einem virtuellen Computer (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen zu diesem Beispiel für die fiskalische Integration finden Sie unter [Beispiel für die Integration des Fiskaldruckers für Polen](emea-pol-fpi-sample.md). 

Das Beispiel für die steuerliche Integration in Polen ist Teil des Retail SDK. Informationen zur Installation und Verwendung des SDK finden Sie in der [Retail Software Development Kit (SDK)-Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dieses Beispiel besteht aus Erweiterungen für die Commerce Runtime (CRT) und Hardwarestation. Um dieses Beispiel auszuführen, müssen Sie die CRT und Hardwarestation-Projekte ändern und erstellen. Es wird empfohlen, dass Sie ein unverändertes Retail SDK verwenden, um die Änderungen vorzunehmen, die in diesem Artikel beschrieben werden. Es wird außerdem empfohlen, dass Sie ein Quellsteuerungssystem verwenden, wie Azure DevOps bei dem noch keine Dateien geändert wurden.

## <a name="development-environment"></a>Entwicklungsumgebung

Gehen Sie folgendermaßen vor, um eine Entwicklungsumgebung einzurichten, damit Sie das Beispiel testen und erweitern können.

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime Erweiterungskomponenten

Die CRT Erweiterungskomponenten sind in den Retail SDK enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **CommerceRuntimeSamples.sln** unter **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.PosnetSample** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.DocumentProvider.PosnetSample\\Lagerplatz\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll**.
3. Kopieren Sie die Assembly-Datei in den Erweiterungsordner CRT:

    - **Commerce Scale Unit:** Kopieren Sie die Datei in den Ordner **\\bin\\ext** unter dem Microsoft Internet Information Services (IIS) Commerce Scale Unit Standort.
    - **Lokal CRT auf Modern POS:** Kopieren Sie die Datei in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Starten Sie den Commerce-Dienst neu:

    - **Commerce Scale Unit:** Starten Sie die Commerce-Service-Site über den IIS Manager neu.
    - **Kundenmakler:** Beendet den **dllhost.exe** Prozess im Task-Manager und startt den Modern POS neu.

### <a name="hardware-station-extension-components"></a>Hardware Station-Erweiterungskomponenten

Die Hardwaresations-Erweiterungskomponenten sind in der Retail SDK enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **HardwareStationSamples.sln.sln** unter **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Suchen Sie das Projekt **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**, und erstellen Sie es.
2. Suchen Sie im Ordner **Extension.Posnet.ThermalFVFiscalPrinterSample\\Lagerplatz\\Debug** die Assembly-Datei **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll**.
3. Kopieren Sie die Assemblydatei auf eine bereitgestellte Hardwarestationsmaschine:

    - **Remote-Hardware-Station** Kopieren Sie die Dateien in den Ordner **Intervall** unter dem IIS Hardware Stations-Sitespeicherort. Kopieren Sie die Bibliotheken der Druckertreiber (**libposcmbth.dll**, **libcmbth\_serial.dll** und **cmbth\_pl.lng**).

4. Suchen Sie die Konfigurationsdatei für die Erweiterungen der Hardwarestationserweiterung. Die Datei hat den Namen **HardwareStation.Extension.config**:

    - **Remote-Hardwarestation:** Die Datei befindet sich unter dem IIS Hardwarestation-Websitespeicherort.

5. Fügen Sie die folgende Position zum Abschnitt **Anordnung** der Konfigurationsdatei hinzu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Starten Sie den Hardwarestationsdienst neu:

    - **Remote-Hardware-Station:** Starten Sie die Hardwarestationssite über den IIS-Manager neu.

## <a name="production-environment"></a>Produktionsumgebung

In der vorherigen Prozedur aktivieren Sie die Erweiterungen, die Komponenten des Steuererfassungsdienst-Integrationsbeispiels sind. Darüber hinaus müssen Sie diese Schritte ausführen, um bereitstellbare Pakete zu erstellen, die Commerce-Komponenten enthalten, und diese Pakete in einer Produktionsumgebung anzuwenden.

1. Nehmen Sie die folgenden Änderungen in den Paketkonfigurationsdateien unter dem Ordner **RetailSdk\\Assets** vor:

    - In den Konfigurationsdateien **commerceruntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** fügen Sie die folgenden Positionen zum Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - In der Konfigurationsdatei **HardwareStation.Extension.config** fügen Sie die folgende Position dem Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Nehmen Sie die folgenden Änderungen in der Paketanpassungs-Konfigurationsdatei **Anpassungs-Einstellungen** im Ordner **BuildTools** vor:

    - Fügen Sie die folgende Position hinzu, um die CRT Erweiterungen in die bereitstellbaren Paketen einzuschließen.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Fügen Sie die folgende Zeilen hinzu, um die Hardware station-Erweiterung in die bereitstellbaren Pakete einzuschließen.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Starten Sie die MSBuild-Eingabeaufforderung für Visual Studio-Hilfsprogramm und führen Sie **msbuild** unter dem Ordner Retail SDK aus, um bereitstellbare Pakete zu erstellen.
1. Übernehmen Sie die Pakete über Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Bereitstellbare Pakete erstellen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

Das Beispiel für die Integration des Fiskaldruckers für Polen basiert auf der [Fiskalintegrationsfunktionalität](fiscal-integration-for-retail-channel.md). Weitere Informationen über das Design der Lösung für die steuerliche Integration finden Sie unter [Überblick über die steuerliche Integration für Commerce-Kanäle](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter druckerspezifische Dokumente erzeugt und Antworten aus dem Steuerdrucker handhabt.

Die CRT-Erweiterung ist **Runtime.Extensions.DocumentProvider.PosnetSample**. Diese Erweiterung generiert eine Reihe von druckerspezifischen Befehlen im Format JavaScript Object Notation (JSON), die in der POSNET-Spezifikation 19-3678 festgelegt sind.

Weitere Informationen über den Aufbau der Fiskalintegrationslösung finden Sie unter [Fiskalischer Registrierungsprozess und Fiskalintegrationsbeispiele für Fiskalgeräte und -dienste](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Anforderungshandler

Der **DocumentProviderPosnetProtocol** Handler ist der Einstiegspunkt für die Anforderung, Belege vom Fiskaldrucker zu erzeugen.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein druckerspezifisches Dokument zurück, dass im Steuerdrucker erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Derzeit werden die folgenden Ereignisse unterstützt: Verkauf, X-Bericht drucken und Z-Bericht drucken.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **Configuration** des Erweiterungsprojekts. Der Zweck der Datei ist es, Einstellungen zu aktivieren, damit der Dokumentanbieter von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- Zuordnung von MwSt.-Sätzen
- Zahlungsmitteltyp-Zuordnung
- Zahlungsart für Einzahlungen

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuerdrucker.

Die Hardware-Stationserweiterung ist **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Diese Erweiterung ruft die Funktionen des POSNET-Treibers auf, um Befehle, die die CRT-Erweiterung erzeugt, an den Fiskaldrucker zu senden. Es behandelt auch Gerätefehler.

#### <a name="request-handler"></a>Anforderungshandler

Der **FiscalPrinterHandler** request handler ist der Einstiegspunkt für die Bearbeitung der Anfrage an das Fiskalperipheriegerät.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** – Diese Anforderung sendet Dokumente an den Drucker und gibt eine Antwort vom Steuerdrucker zurück.
- **IsReadyFiscalDeviceRequest** – Diese Anforderung wird für eine Integritätsprüfung des Steuererfassungsgeräts verwendet.
- **InitializeFiscalDeviceRequest** – Diese Anforderung wird für Initialisierung des Druckers verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Der Zweck dieser Datei ist es, Einstellungen zu aktivieren, damit der Konnektor von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- **Verbindungsstring** - Ein String, der die Details der Verbindung zum Gerät in einem Format beschreibt, das vom Treiber unterstützt wird. Weitere Informationen finden Sie in der Dokumentation des POSNET Treibers.
- **Datum- und Uhrzeitsynchronisation** – Ein Wert, der angibt, ob Datum und Uhrzeit des Druckers mit der angeschlossenen Hardwarestation synchronisiert werden müssen.
- **Geräte-Timeout** - Die Zeitspanne in Millisekunden, die der Fahrer auf eine Antwort vom Gerät wartet. Weitere Informationen finden Sie in der Dokumentation des POSNET Treibers.
