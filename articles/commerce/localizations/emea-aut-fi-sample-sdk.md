---
title: Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für Österreich (Legacy)
description: Dieses Thema enthält Richtlinien für die Bereitstellung des Beispiels für die steuerliche Integration für Österreich aus dem Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 6238b67a35a303a03c51bbd261dd24d1b2acf041
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077114"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für Österreich (Legacy)

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Richtlinien für die Bereitstellung des Integrationsbeispiels für den Steuerregistrierungsdienst für Österreich aus dem Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK) auf einer virtuellen Entwicklermaschine (VM) in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen zu den Beispielen für diese steuerliche Integration finden Sie unter [Beispiele für die steuerliche Integration für Österreich](emea-aut-fi-sample.md). 

Das Steuererfassungsdienst-Integrationsbeispiel für Österreich ist Teil des Retail SDK. Informationen zur Installation und Verwendung des SDK finden Sie in der [Retail Software Development Kit (SDK)-Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dieses Beispiel für die steuerliche Integration besteht aus Erweiterungen für die Commerce Runtime (CRT) Hardwarestation und Verkaufsstelle (POS). Um dieses Beispiel auszuführen, müssen Sie CRT, Hardwarestation und POS-Projekte ändern und erstellen. Es wird empfohlen, dass Sie ein unverändertes Retail SDK verwenden, um die Änderungen vorzunehmen, die in diesem Thema beschrieben werden. Es wird außerdem empfohlen, dass Sie ein Quellsteuerungssystem verwenden, wie Azure DevOps bei dem noch keine Dateien geändert wurden.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

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

### <a name="enable-modern-pos-extension-components"></a>Modern POS-Erweiterungskomponenten aktivieren

1. Öffnen Sie die Lösung **ModernPOS.sln** unter **RetailSdk\\POS** und stellen Sie sicher, dass sie ohne Fehler kompiliert werden kann. Stellen Sie außerdem sicher, dass Sie Modern POS von Visual Studio aus ausführen können, indem Sie den Befehl **Ausführen** verwenden.

    > [!NOTE]
    > Modern POS darf nicht angepasst werden. Sie müssen die Benutzerkontensteuerung (UAC) aktivieren, und Sie müssen zuvor installierte Instanzen von Modern POS bei Bedarf deinstallieren.

2. Aktivieren Sie das Laden der Instanzen, indem Sie die folgenden Zeilen in der Datei **extensions.json** hinzufügen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Weitere Informationen und Beispiele, die zeigen, wie Quellcodeordner einbezogen werden und das Laden von Erweiterungen ermöglicht wird, finden Sie in den Anleitungen in der readme.md-Datei im Projekt **Pos.Extensions**.

3. Erstellen Sie die Lösung neu.
4. Führen Sie Modern POS im Debugger aus, und testen Sie die Funktionen.

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS-Erweiterungskomponenten aktivieren

1. Öffnen Sie die **CloudPOS.sln** Lösung unter **RetailSdk\\POS** und stellen Sie sicher, dass sie ohne Fehler kompiliert werden kann.
2. Aktivieren Sie das Laden der Instanzen, indem Sie die folgenden Zeilen in der Datei **extensions.json** hinzufügen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Weitere Informationen und Beispiele, die zeigen, wie Quellcodeordner einbezogen werden und das Laden von Erweiterungen ermöglicht wird, finden Sie in den Anleitungen in der readme.md-Datei im Projekt **Pos.Extensions**.

3. Erstellen Sie die Lösung neu.
4. Führen Sie Lösung aus, indem Sie den Befehl **Run** verwenden, und folgen Sie den Schritten im Retail SDK-Handbuch.

## <a name="production-environment"></a>Produktionsumgebung

Die vorherige Prozedur aktiviert die Erweiterungen, die Komponenten des Steuererfassungsdienst-Integrationsbeispiels sind. Darüber hinaus müssen Sie diese Schritte ausführen, um bereitstellbare Pakete zu erstellen, die Commerce-Komponenten enthalten, und diese Pakete in einer Produktionsumgebung anzuwenden.

1. Nehmen Sie die folgenden Änderungen in den Paketkonfigurationsdateien unter dem Ordner **RetailSdk\\Assets** vor:

    - In den Konfigurationsdateien **commerceruntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** fügen Sie die folgenden Positionen zum Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - In der Konfigurationsdatei **HardwareStation.Extension.config** fügen Sie die folgende Position dem Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Nehmen Sie die folgenden Änderungen in der Paketanpassungs-Konfigurationsdatei **Anpassungs-Einstellungen** im Ordner **BuildTools** vor:

    - Fügen Sie die folgenden Zeilen hinzu, um die CRT-Erweiterungen in die bereitstellbaren Paketen einzuschließen.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Fügen Sie die folgende Zeilen hinzu, um die Hardware station-Erweiterung in die bereitstellbaren Pakete einzuschließen.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Starten Sie die MSBuild-Eingabeaufforderung für Visual Studio-Hilfsprogramm und führen Sie **msbuild** unter dem Ordner Retail SDK aus, um bereitstellbare Pakete zu erstellen.
4. Übernehmen Sie die Pakete über Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Bereitstellbare Pakete erstellen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Schließen Sie alle erforderlichen Einrichtungsaufgaben ab, die im Abschnitt [Commerce für Österreich einrichten](emea-aut-fi-sample.md#set-up-commerce-for-austria) beschrieben sind.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

Die Beispiele für diese steuerliche Integration für Österreich basiert auf der [steuerlichen Integrationsfunktionalität](fiscal-integration-for-retail-channel.md). Weitere Informationen über das Design der Lösung für die steuerliche Integration finden Sie unter [Überblick über die steuerliche Integration für Commerce-Kanäle](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter dienstspezifische Dokumente erzeugt und Antworten aus dem Steuererfassungsdienst handhabt.

Die CRT-Erweiterung ist **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Anforderungshandler

Es gibt zwei Anforderungshandler für Dokumentanbieter:

- **DocumentProviderEFRFiscalAUT** – Dieser Handler wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen.
- **DocumentProviderEFRNonFiscalAUT** – Dieser Handler wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen.

Diese Handler werden von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetNonFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches nicht-steuerliche Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Aktuell werden die folgenden Ereignisse unterstützt: Vertrieb, Drucken von X-Bericht, Drucken von Z-Bericht, Debitorenkonto-Einzahlungen, Debitorenauftragseinzahlungen, Überwachungsereignisse und Nicht-Vertriebsbuchungen.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Diese Anforderung gibt die Antwort vom Steuererfassungsdienst zurück. Diese Antwort wird serialisiert, um eine Zeichenfolge zu bilden, sodass sie bereit zum Speichern ist.

#### <a name="configuration"></a>Variante

Die Konfigurationsdateien befinden sich im Ordner **Konfiguration** des Erweiterungsprojekts:

- **DocumentProviderFiscalEFRSampleAustria** – Für Steuerdokumente.
- **DocumentProviderNonFiscalEFRSampleAustria** – Für nicht-steuerliche Dokumente.

Der Zweck dieser Dateien ist es, Einstellungen zu aktivieren, damit der Dokumentanbieter von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgende Einstellung wird hinzugefügt:

- Zuordnung von MwSt.-Sätzen

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuererfassungsdienst.

Die Hardware station-Erweiterung ist **HardwareStation.Extension.EFRSample**. Sie verwendet das HTTP-Protokoll, um Dokumente, die die CRT-Erweiterung generiert, zum Steuererfassungsdienst zu übermitteln. Sie handhabt auch die Antworten, die vom Steuererfassungsdienst empfangen werden.

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
- **Zeitlimit** – Die Zeitdauer in Millisekunden, die der Treiber auf eine Antwort vom Steuererfassungsdienst wartet.
