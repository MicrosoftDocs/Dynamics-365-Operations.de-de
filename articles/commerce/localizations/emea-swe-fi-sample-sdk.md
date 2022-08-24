---
ms.openlocfilehash: a20971ac9a44c409363bbce6cd8b8343f16d800f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274204"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Richtlinien für die Bereitstellung des Beispiels für die Integration der Steuereinheit für Schweden (veraltet)
---

Titel: Richtlinien für die Bereitstellung des Beispiels für die Integration der Steuereinheit für Schweden (veraltet) [!include [banner](../includes/banner.md)]
Beschreibung: Dieser Artikel enthält Richtlinien zum Bereitstellen des Beispiels für die Integration der Steuereinheit für Schweden aus dem Retail SDK

Autor: EvgenyPopovMBS Dieser Artikel enthält Richtlinien zum Bereitstellen des Beispiels für die Integration der Steuereinheit für Schweden aus dem Software Development Kit (SDK) für Retail auf einem virtuellen Computer (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen zu diesem Beispiel für die steuerliche Integration finden Sie unter [Beispiel für die Integration von Steuereinheiten für Schweden](emea-swe-fi-sample.md). ms.date: 20.12.2021

ms.topic: Artikel Das Beispiel für die fiskalische Integration für Schweden ist Teil des Retail SDK. Informationen zur Installation und Verwendung des SDK finden Sie in der [Retail Software Development Kit (SDK)-Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dieses Beispiel besteht aus Erweiterungen für die Commerce Runtime (CRT), die Hardware-Station und den Point of Sale (POS). Um dieses Beispiel auszuführen, müssen Sie CRT, Hardwarestation und POS-Projekte ändern und erstellen. Es wird empfohlen, dass Sie ein unverändertes Retail SDK verwenden, um die Änderungen vorzunehmen, die in diesem Artikel beschrieben werden. Es wird außerdem empfohlen, dass Sie ein Quellsteuerungssystem verwenden, wie Azure DevOps bei dem noch keine Dateien geändert wurden.
Zielgruppe: Anwendungsbenutzer, Entwickler, IT-Experten

ms.reviewer: v-chgriffin
## <a name="development-environment"></a>Entwicklungsumgebung
ms.search.region: Global

ms.author: josaw Gehen Sie folgendermaßen vor, um eine Entwicklungsumgebung einzurichten, damit Sie das Beispiel testen und erweitern können.
ms.search.validFrom: 01.03.2019

### <a name="enable-crt-extensions"></a>Aktivieren der CRT Erweiterungen
---


Die CRT-Erweiterungskomponenten sind in den CRT-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **CommerceRuntimeSamples.sln** unter **RetailSdk\\SampleExtensions\\CommerceRuntime**.
2. Aktivieren Sie die aktuelle Beispiel-HardwareStation-Erweiterung, indem Sie die folgende Zeile zum Abschnitt **composition** in der Konfigurationsdatei **HardwareStation.Extension.config** hinzufügen.


#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample Komponente
    ``` xml

    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.CleanCashSample** und erstellen Sie es.
    ```
2. In the **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** assembly file.

3. Copy the assembly file to the CRT extensions folder:
3. Make the following changes in the **Customization.settings** package customization configuration file under the **BuildTools** folder:


    - **Commerce Scale Unit:** Copy the file to the **\\bin\\ext** folder under the Internet Information Services (IIS) Commerce Scale Unit site location.
    - Remove the following line to exclude the earlier Hardware station extension from deployable packages.
    - **Local CRT on Modern POS:** Copy the file to the **\\ext** folder under the local CRT client broker location.


        ``` xml
4. Find the extension configuration file for CRT:
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />

        ```
    - **Commerce Scale Unit:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.

    - **Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.
    - Add the following lines to include the current sample Hardware station extension in deployable packages.


5. Register the CRT change in the extension configuration file.
        ``` xml

        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
    ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        ```
    ```


#### <a name="update-modern-pos"></a>Modern POS aktualisieren
#### <a name="extension-configuration-file"></a>Erweiterungskonfigurationsdatei


1. Öffnen Sie die Lösung **CloudPOS.sln** unter **RetailSdk\\POS**.
1. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:
2. Deaktivieren Sie die frühere POS-Erweiterung:


    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - Fügen Sie in der Datei **tsconfig.json** den Ordner **FiscalRegisterSample** zur Ausschlussliste hinzu.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.
    - Entfernen Sie die folgenden Zeilen aus der Datei **extensions.json** im Ordner **RetailSDK\\POS\\Extensions**.


2. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.
        ``` json

        {
    ``` xml
            "baseUrl": "FiscalRegisterSample"
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        }
    ```
        ```


### <a name="enable-hardware-station-extensions"></a>Hardware station-Erweiterungen aktivieren
3. Aktivieren Sie die aktuelle Beispiel-POS-Erweiterung, indem Sie die folgenden Zeilen in der Datei **extensions.json** unter dem Ordner **RetailSDK\\POS\\Extensions** hinzufügen.


Die Hardware station-Erweiterungskomponenten sind in den Hardware station-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **HardwareStationSamples.sln.sln** unter **RetailSdk\\SampleExtensions\\HardwareStation**.
    ``` json

    {
#### <a name="cleancash-component"></a>CleanCash Komponente
        "extensionPackages": [

            {
1. Suchen Sie das Projekt **HardwareStation.Extension.CleanCashSample** und erstellen Sie es.
                „baseUrl“: „Microsoft/AuditEvent.SE“
2. Suchen Sie im Ordner **Extension.CleanCashSample\\bin\\Debug** die Assembly-Dateien **Contoso.Commerce.HardwareStation.CleanCashSample.dll** und **Interop.CleanCash\_1\_1.dll**.
            }
3. Kopieren Sie die Assembly-Dateien in den Hardwarestations-Erweiterungsordner:      ]

    }
    - **Freigegebene Hardware station:** Kopieren Sie die Dateien in den Ordner **Lagerfach** unter dem IIS Hardware stations-Websitespeicherort.
    ```
    - **Dedicated hardware station on Modern POS:** Copy the files to the Modern POS client broker location.


#### Update Cloud POS
4. Find the extension configuration file for the Hardware station's extensions. The file is named **HardwareStation.Extension.config**.


1. Open the **ModernPOS.sln** solution under **RetailSdk\\POS**.
    - **Shared hardware station:** The file is under the IIS Hardware station site location.
2. Disable the earlier POS extension:
    - **Dedicated hardware station on Modern POS:** The file is under the Modern POS client broker location.


    - In the **tsconfig.json** file, add the **FiscalRegisterSample** folder to the exclude list.
5. Add the following line to the **composition** section of the configuration file.
    - Remove the following lines from the **extensions.json** file under the **RetailSDK\\POS\\Extensions** folder.


    ``` xml
        ``` json
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        {
    ```
            "baseUrl": "FiscalRegisterSample"

        }
### <a name="enable-modern-pos-extension-components"></a>Modern POS-Erweiterungskomponenten aktivieren
        ```


1. Öffnen Sie die Lösung **ModernPOS.sln** unter **RetailSdk\\POS** und stellen Sie sicher, dass sie ohne Fehler kompiliert werden kann. Stellen Sie außerdem sicher, dass Sie Modern POS von Visual Studio aus ausführen können, indem Sie den Befehl **Ausführen** verwenden.
3. Aktivieren Sie die aktuelle Beispiel-POS-Erweiterung, indem Sie die folgenden Zeilen in der Datei **extensions.json** unter dem Ordner **RetailSDK\\POS\\Extensions** hinzufügen.


    > [!NOTE]
    ``` json
    > Modern POS must not be customized. You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.
    {

        "extensionPackages": [
2. Enable the extensions that must be loaded by adding the following lines in the **extensions.json** file.
            {

                "baseUrl": "Microsoft/AuditEvent.SE"
    ``` json
            }
    {
        ]
        "extensionPackages": [
    }
            {
    ```
                "baseUrl": "Microsoft/AuditEvent.SE"

            }
#### <a name="create-deployable-packages"></a>Bereitstellbare Pakete erstellen
        ]

    }
Führen Sie **msbuild** für das gesamte Retail SDK aus, um bereitzustellende Pakete zu erstellen. Übernehmen Sie die Pakete über Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Retail SDK-Pakete](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
    ```

    > [!NOTE]
    > For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.

3. Erstellen Sie die Lösung neu.
4. Führen Sie Modern POS im Debugger aus, und testen Sie die Funktionen.

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS-Erweiterungskomponenten aktivieren

1. Öffnen Sie die **CloudPOS.sln** Lösung unter **RetailSdk\\POS** und stellen Sie sicher, dass sie ohne Fehler kompiliert werden kann.
2. Aktivieren Sie die Erweiterungen, die geladen werden müssen, indem Sie die folgenden Zeilen in der Datei **extensions.json** hinzufügen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Weitere Informationen und Beispiele, die zeigen, wie Quellcodeordner einbezogen werden und das Laden von Erweiterungen ermöglicht wird, finden Sie in den Anleitungen in der readme.md-Datei im Projekt **Pos.Extensions**.

3. Erstellen Sie die Lösung neu.
4. Führen Sie Lösung aus, indem Sie den Befehl **Run** verwenden, und folgen Sie den Schritten im Retail SDK-Handbuch.

## <a name="production-environment"></a>Produktionsumgebung

Das vorherige Verfahren aktiviert die Erweiterungen, die Komponenten des Musters für die Integration der Einheit sind. Darüber hinaus müssen Sie diese Schritte ausführen, um bereitstellbare Pakete zu erstellen, die Commerce-Komponenten enthalten, und diese Pakete in einer Produktionsumgebung anzuwenden.

1. Nehmen Sie die folgenden Änderungen in den Paketkonfigurationsdateien unter dem Ordner **RetailSdk\\Assets** vor:

    - In den Konfigurationsdateien **commerceruntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** fügen Sie die folgenden Positionen zum Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - In der Konfigurationsdatei **HardwareStation.Extension.config** fügen Sie die folgende Position dem Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Nehmen Sie die folgenden Änderungen in der Paketanpassungs-Konfigurationsdatei **Anpassungs-Einstellungen** im Ordner **BuildTools** vor:

    - Fügen Sie die folgende Zeile hinzu, um die CRT-Erweiterungen in die bereitzustellenden Pakete aufzunehmen.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Fügen Sie die folgenden Zeilen hinzu, um die Hardware-Stationserweiterung in die bereitzustellenden Pakete aufzunehmen.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Aktivieren Sie die POS-Erweiterung, indem Sie die folgenden Zeilen in der Datei **extensions.json** unter dem Ordner **RetailSDK\\POS\\Extensions** hinzufügen.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Starten Sie die MSBuild-Eingabeaufforderung für Visual Studio-Hilfsprogramm und führen Sie **msbuild** unter dem Ordner Retail SDK aus, um bereitstellbare Pakete zu erstellen.
5. Übernehmen Sie die Pakete über Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Bereitstellbare Pakete erstellen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Schließen Sie alle erforderlichen Einrichtungsaufgaben ab, die unter [Einrichten der Integration mit Steuereinheiten](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units) beschrieben sind.

## <a name="design-of-the-extensions"></a>Gestaltung der Erweiterungen

### <a name="crt-extension-design"></a>CRT Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Fiskalbeleg-Anbieter ist, besteht darin, servicespezifische Belege zu erzeugen und Antworten von der Einheit zu verarbeiten.

Die CRT-Erweiterung ist **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Weitere Informationen über den Aufbau der Fiskalintegrationslösung finden Sie unter [Fiskalischer Registrierungsprozess und Fiskalintegrationsbeispiele für Fiskalgeräte und -dienste](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Anforderungshandler

Es gibt einen einzigen **DocumentProviderCleanCash** Request Handler für den Beleg-Anbieter. Dieser Handler wird verwendet, um fiskalische Belege für die Einheit zu erzeugen.

Dieser Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie liefert einen dienstspezifischen Beleg, der in der Einheit registriert werden sollte.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Derzeit werden Verkaufs- und Audit-Ereignisse unterstützt.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei **DocumentProviderFiscalCleanCashSample** befindet sich im Ordner **Configuration** des Erweiterungsprojekts. Mit dieser Datei können Sie die Einstellungen für den Beleg-Anbieter von der Commerce-Zentrale aus festlegen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- Zuordnung von MwSt.-Codes

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein fiskalischer Konnektor ist, ist die Kommunikation mit der Einheit.

Die Hardware-Stationserweiterung ist **HardwareStation.Extension.CleanCashSample**. Sie verwendet das HTTP-Protokoll, um Belege, die die Erweiterung CRT erzeugt, an die Einheit zu senden. Es behandelt auch die Antworten, die von der Steuereinheit empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der **CleanCashHandler** Request Handler ist der Einstiegspunkt für die Bearbeitung von Anfragen an die Einheit.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** - Diese Anfrage sendet Belege an die Einheit der Steuereinheit und gibt eine Antwort von ihr zurück.
- **IsReadyFiscalDeviceRequest** - Diese Anfrage wird für einen Statuscheck der Steuereinheit verwendet.
- **InitializeFiscalDeviceRequest** - Diese Anfrage wird zur Initialisierung der Steuereinheit verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Der Zweck der Datei besteht darin, die Konfiguration der Einstellungen für den Fiskalkonnektor von der Commerce-Zentrale aus zu ermöglichen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- **Verbindungsstring** - Die Einstellungen für die Verbindung der Einheit.
- **Timeout** - Die Zeitspanne in Millisekunden, die der Treiber auf eine Antwort der Steuereinheit wartet.

## <a name="migrating-from-the-earlier-integration-sample"></a>Migration von dem früheren Integrationsbeispiel

Wenn Sie das frühere [Beispiel für die POS-Integration mit Steuereinheiten für Schweden](retail-sdk-control-unit-sample.md) verwenden, müssen Sie möglicherweise von diesem auf das aktuelle Integrationsbeispiel migrieren. Um die Änderung zu übernehmen und in Zukunft rechtzeitig Updates für die Funktionen für Schweden zu erhalten, müssen Sie möglicherweise ein Upgrade durchführen, kleinere Code- und Konfigurationsanpassungen in den von Ihnen erstellten Erweiterungen vornehmen und Ihre Lösungen neu erstellen. An der von Ihnen erstellten Erweiterungslogik sind keine größeren Änderungen erforderlich. Das frühere Integrationsbeispiel und Ihre Anpassungen funktionieren weiterhin, wenn von Ihrer Seite keine Änderungen vorgenommen werden. Sie können also die Übernahme für Ihre Umgebung planen, vorbereiten und durchführen.

### <a name="migration-process"></a>Migrationsprozess

Die Migration von dem früheren Integrationsmuster auf das aktuelle Muster für die Integration von Steuereinheiten sollte auf dem Konzept einer schrittweisen Aktualisierung basieren. Mit anderen Worten: Alle Komponenten der Commerce-Zentrale und der Commerce Scale Unit sollten bereits aktualisiert sein, bevor Sie mit der Aktualisierung der POS- und Hardware-Station-Komponenten beginnen.

Um zu verhindern, dass ein Ereignis oder eine Transaktion doppelt signiert wird (d.h. sowohl von der früheren als auch von der aktuellen Erweiterung) oder dass ein Ereignis oder eine Transaktion aufgrund der fehlenden Konfiguration nicht signiert werden kann, empfehlen wir Ihnen, alle POS- und Hardware-Stationen, die das frühere Beispiel verwenden, auszuschalten und sie dann gleichzeitig zu aktualisieren. Diese gleichzeitige Aktualisierung kann z.B. für jeden Store einzeln durchgeführt werden, indem das Funktionsprofil des Stores und das Hardwareprofil der Hardwarestation aktualisiert werden.

Der Migrationsprozess sollte aus den folgenden Schritten bestehen.

1. Aktualisieren Sie die Komponenten der Commerce-Zentrale.
1. Aktualisieren Sie die Komponenten der Scale-Unit von Commerce und aktivieren Sie die Erweiterungen des aktuellen Beispiels.
1. Stellen Sie sicher, dass alle Offline-Transaktionen von offline-fähigen MPOS-Geräten synchronisiert werden.
1. Schalten Sie alle Geräte aus, die die Komponenten der früheren Testversion verwenden.
1. Schließen Sie alle erforderlichen Einrichtungsaufgaben ab, die unter [Einrichten der Integration mit Steuereinheiten](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units) beschrieben sind.
1. Aktualisieren Sie die Komponenten POS und Hardware-Station, deaktivieren Sie die Erweiterungen, die Teil des früheren Beispiels sind, und aktivieren Sie die Erweiterungen des aktuellen Beispiels.

    > [!NOTE]
    > Je nach Art der Umgebung finden Sie weitere technische Details über den Migrationsprozess entweder im Abschnitt [Migration in einer Entwicklungsumgebung](#migration-in-a-development-environment) oder im Abschnitt [Migration in einer Produktionsumgebung](#migration-in-a-production-environment) dieses Artikels.

### <a name="migration-in-a-development-environment"></a>Migration in einer Entwicklungsumgebung

#### <a name="update-crt"></a>CRT aktualisieren

1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.CleanCashSample** und erstellen Sie es.
2. Suchen Sie im Ordner **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Commerce Scale Unit:** Kopieren Sie die Datei in den Ordner **\\bin\\ext** unter dem Standort der IIS Commerce Scale Unit.
    - **Lokal CRT auf Modern POS:** Kopieren Sie die Datei in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce Scale Unit:** Die Datei heißt **CommerceRuntime.ext.config** und befindet sich im Ordner **bin\\ext** unter dem Speicherort der IIS Commerce Scale Unit-Site.
    - **Lokal CRT auf Modern POS:** Die Datei heißt **CommerceRuntime.MPOSOffline.Ext.config** und befindet sich im Ordner **bin\\ext** unter dem lokalen CRT Client Broker Speicherort.

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

5. Finden und entfernen Sie die frühere Erweiterung CRT aus der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Schließen Sie diesen Schritt erst ab, wenn Sie alle POS-Geräte aktualisiert haben, die mit dieser CRT-Instanz arbeiten.

6. Registrieren Sie die aktuellen Beispielerweiterungen CRT in der Erweiterungskonfigurationsdatei, indem Sie die folgenden Zeilen hinzufügen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Hardware-Station aktualisieren

1. Suchen Sie das Projekt **HardwareStation.Extension.CleanCashSample** und erstellen Sie es.
2. Suchen Sie im Ordner **Extension.CleanCashSample\\bin\\Debug** die Assembly-Dateien **Contoso.Commerce.HardwareStation.CleanCashSample.dll** und **Interop.CleanCash\_1\_1.dll**.
3. Kopieren Sie die Assembly-Dateien in den Hardware stations-Erweiterungsordner:

    - **Freigegebene Hardware station:** Kopieren Sie die Dateien in den Ordner **Lagerfach** unter dem IIS Hardware stations-Websitespeicherort.
    - **Dedizierte Hardware station auf Modern POS:** Kopieren Sie die Dateien zum Modern POS-Client-Broker-Speicherort.

4. Suchen Sie die Konfigurationsdatei der Erweiterung **HardwareStation.Extension.config**:

    - **Ferngesteuerte Hardwarestation:** Die Datei befindet sich unter dem Standort der IIS-Hardwarestation.
    - **Lokale Hardwarestation auf Modern POS:** Die Datei befindet sich unter dem Speicherort des Modern POS Client Brokers.

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

5. Suchen Sie die frühere Erweiterung Hardware-Station und entfernen Sie sie aus der Erweiterungskonfigurationsdatei.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 und früher](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 und später](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 und höher](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Fügen Sie die folgende Zeile in den Abschnitt **composition** der Konfigurationsdatei der Erweiterungen ein.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Modern POS aktualisieren

1. Öffnen Sie die Lösung **CloudPOS.sln** unter **RetailSdk\\POS**.
2. Deaktivieren Sie die frühere POS-Erweiterung, indem Sie die folgenden Zeilen aus der Datei **extensions.json** entfernen.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Aktivieren Sie die aktuelle Beispiel-POS-Erweiterung, indem Sie die folgenden Zeilen in der Datei **extensions.json** hinzufügen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Cloud POS aktualisieren

1. Öffnen Sie die Lösung **ModernPOS.sln** unter **RetailSdk\\POS**.
2. Deaktivieren Sie die frühere POS-Erweiterung, indem Sie die folgenden Zeilen aus der Datei **extensions.json** entfernen.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Aktivieren Sie die aktuelle Beispiel-POS-Erweiterung, indem Sie die folgenden Zeilen in der Datei **extensions.json** hinzufügen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Migration in einer Produktionsumgebung

#### <a name="update-crt"></a>CRT aktualisieren

1. Entfernen Sie die frühere Erweiterung CRT aus den Konfigurationsdateien **CommerceRuntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** im Ordner **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Schließen Sie diesen Schritt erst ab, wenn Sie alle POS-Geräte aktualisiert haben, die mit dieser CRT-Instanz arbeiten.

2. Aktivieren Sie die aktuellen Beispielerweiterungen CRT, indem Sie die folgenden Änderungen in den Konfigurationsdateien **CommerceRuntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** unter dem Ordner **RetailSdk\\Assets** vornehmen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Fügen Sie in der Konfigurationsdatei **Customization.settings** für die Paketanpassung im Ordner **BuildTools** die folgende Zeile hinzu, um die aktuelle Beispielerweiterung CRT in bereitgestellte Pakete aufzunehmen.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Hardware-Station aktualisieren

1. Entfernen Sie die frühere Erweiterung HardwareStation, indem Sie die Konfigurationsdatei **HardwareStation.Extension.config** ändern.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 und früher](#tab/retail-7-3)

    Entfernen Sie den folgenden Abschnitt aus den Konfigurationsdateien **HardwareStation.Shared.config** und **HardwareStation.Dedicated.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 und später](#tab/retail-7-3-1)

    Entfernen Sie den folgenden Abschnitt aus der Konfigurationsdatei **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 und höher](#tab/retail-10-0)

    Entfernen Sie den folgenden Abschnitt aus der Konfigurationsdatei **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---
