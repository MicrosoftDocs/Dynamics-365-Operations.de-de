---
ms.openlocfilehash: b17bd56f9f3e4def341658626915adbd7f5aada6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281537"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Bereitstellungsrichtlinien für Registrierkassen für Norwegen (veraltet)
---

Titel: Bereitstellungsrichtlinien für Registrierkassen für Norwegen (veraltet) [!include [banner](../includes/banner.md)]
Beschreibung: Dieser Artikel ist eine Anleitung zum Bereitstellen, die zeigt, wie Sie die Lokalisierung Microsoft Dynamics 365 Commerce für Norwegen aktivieren.

Autor: EvgenyPopovMBS Dieser Artikel ist eine Anleitung zum Bereitstellen, die zeigt, wie Sie die Lokalisierung Microsoft Dynamics 365 Commerce für Norwegen aktivieren. Die Lokalisierung besteht aus mehreren Erweiterungen der Commerce-Komponenten. Mit den Erweiterungen können Sie beispielsweise angepasste Felder auf Quittungen drucken, zusätzliche Audit-Ereignisse, Verkaufstransaktionen und Zahlungstransaktionen am Point of Sale (POS) registrieren, Verkaufstransaktionen digital signieren und X- und Z-Berichte in lokalen Formaten drucken. Weitere Informationen über die Lokalisierung für Norwegen finden Sie unter [Kassenfunktionalität für Norwegen](./emea-nor-cash-registers.md).
ms.date: 20.12.2021

ms.topic: Artikel Dieses Beispiel ist Teil des Software Development Kit (SDK) für Retail. Informationen über das SDK finden Sie in der [Architektur des Software Development Kit (SDK) für Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md).
Zielgruppe: Anwendungsbenutzer, Entwickler, IT-Experten

ms.reviewer: v-chgriffin Dieses Beispiel besteht aus Erweiterungen für die Commerce Runtime (CRT), den Retail Server und den POS. Um dieses Beispiel ausführen zu können, müssen Sie die Projekte CRT, Retail Server und POS modifizieren und erstellen. Es wird empfohlen, dass Sie ein unverändertes Retail SDK verwenden, um die Änderungen vorzunehmen, die in diesem Artikel beschrieben werden. Wir empfehlen Ihnen außerdem, eine Steuereinheit wie Microsoft Visual Studio Online (VSO) zu verwenden, in dem noch keine Dateien geändert wurden.
ms.search.region: Global

ms.author: josaw
> [!NOTE]
ms.search.validFrom: 28.02.2018 In Commerce 10.0.8 und höher wird der Retail Server als Commerce Scale Unit bezeichnet. Da sich Dieser Artikel auf mehrere Vorgängerversionen der App bezieht, wird im gesamten Artikel *Retail Server* verwendet.
>
---
> Einige Schritte in den Verfahren in diesem Artikel unterscheiden sich je nach der Version von Commerce, die Sie verwenden. Weitere Informationen finden Sie unter [Neuheiten und Änderungen in Dynamics 365 Retail](../get-started/whats-new.md).


6. Aktualisieren Sie die Retail Server Konfigurationsdatei. Fügen Sie in der Datei **RetailSDK\\Packages\\RetailServer\\Code\\web.config** die folgenden Zeilen in den Abschnitt **extensionComposition** ein.
### <a name="using-certificate-profiles-in-commerce-channels"></a>Verwendung von Zertifikatsprofilen in Commerce-Kanälen


    ``` xml
In Commerce 10.0.15 und höher können Sie die Funktion [Benutzerdefinierte Zertifikatsprofile für Einzelhandelsgeschäfte](./certificate-profiles-for-retail-stores.md) verwenden, die ein Failover in den Offline-Modus unterstützt, wenn Key Vault oder die Commerce-Zentrale nicht verfügbar sind. Die Funktion erweitert die Funktion [Geheimnisse für Einzelhandelskanäle verwalten](../dev-itpro/manage-secrets.md).
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />

    ```
Um diese Funktionalität in der CRT-Erweiterung anzuwenden, gehen Sie folgendermaßen vor.


7. Führen Sie **msbuild** für das gesamte Retail SDK aus, um bereitzustellende Pakete zu erstellen.
1. Erstellen Sie ein neues CRT Erweiterungsprojekt (Projekttyp C#-Klassenbibliothek). Verwenden Sie die Beispielvorlagen aus dem Software Development Kit (SDK) für Retail (RetailSDK\SampleExtensions\CommerceRuntime).
8. Übernehmen Sie die Pakete über Microsoft Dynamics Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Bereitstellbare Pakete erstellen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).


2. Fügen Sie einen angepassten Handler für CertificateSignatureServiceRequest in das Projekt SequentialSignatureRegister ein.
### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Aktivieren Sie die digitale Signatur im Offline-Modus für Modern POS


3. Um einen geheimen Aufruf zu lesen, benutzt `GetUserDefinedSecretCertificateServiceRequest` einen Konstruktor mit dem Parameter profileId. Dadurch wird die Funktionalität mit den Einstellungen aus den Zertifikats-Profilen in Betrieb genommen. Je nach den Einstellungen wird das Zertifikat entweder aus Azure Key Vault oder aus dem lokalen Computerspeicher abgerufen.
Um die digitale Signatur im Offline-Modus für Modern POS zu aktivieren, müssen Sie diese Schritte ausführen, nachdem Sie Modern POS auf einem neuen Gerät aktiviert haben.


    ```csharp
1. Sign in to POS.
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
2. On the **Database connection status** page, make sure that the offline database is fully synchronized. When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);
3. Sign out of POS.

4. Wait a while for the offline database to be fully synchronized.
    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
5. Sign in to POS.
    ```
6. Vergewissern Sie sich auf der Seite **Datenbankverbindungsstatus**, dass die Offline-Datenbank vollständig synchronisiert ist. Wenn der Wert des Feldes **Ausstehende Transaktionen in der Offline-Datenbank** **0** (Null) ist, ist die Datenbank vollständig synchronisiert.

7. Starten Sie Modern POS neu.
4. Wenn das Zertifikat abgerufen wird, fahren Sie mit dem Signieren der Daten fort.



5. Erstellen Sie das Erweiterungsprojekt CRT.
[!INCLUDE[footer-include](../../includes/footer-banner.md)]

6. Kopieren Sie die Ausgabeklassenbibliothek und fügen Sie sie in ...\RetailServer\webroot\bin\Ext für manuelle Tests ein.

7. Aktualisieren Sie in der Datei CommerceRuntime.Ext.config den Abschnitt Erweiterungsanordnung mit den angepassten Bibliotheksinformationen.

## <a name="development-environment"></a>Entwicklungsumgebung

Führen Sie diese Schritte aus, um eine Entwicklungsumgebung festzulegen, in der Sie das Beispiel testen und erweitern können.

### <a name="the-crt-extension-components"></a>Die Komponenten der CRT-Erweiterung

Die CRT-Erweiterungskomponenten sind in den CRT-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die CRT-Lösung, **CommerceRuntimeSamples.sln**, unter **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>Komponente ReceiptsNorway

1. Suchen Sie das Projekt **Runtime.Extensions.ReceiptsNorway** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.ReceiptsNorway\\bin\\Debug** die Assemblierungsdatei **Contoso.Commerce.Runtime.ReceiptsNorway.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem Microsoft Internet Information Services (IIS) Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="salespaymenttransext-component"></a>Komponente SalesPaymentTransExt

1. Suchen Sie das Projekt **Runtime.Extensions.SalesPaymentTransExt** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.SalesPaymentTransExt\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="xzreportsnorway-component"></a>XZReportsNorway Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.XZReportsNorway** und erstellen Sie es.
2. Im Ordner **Extensions.XZReportsNorway\\bin\\Debug** finden Sie die Assembly-Datei **Contoso.Commerce.Runtime.XZReportsNorway.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

# <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent Beispielkomponente

1. Suchen Sie das Projekt **Runtime.Extensions.RegisterAuditEventSample** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.RegisterAuditEventSample\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature Beispielkomponente

1. Suchen Sie das Projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Ändern Sie die Datei **App.config**, indem Sie den Thumbprint, den Store und den Store-Namen für das Zertifikat angeben, das zum Signieren von Verkaufstransaktionen verwendet werden soll.
3. Erstellen Sie das Projekt.
4. Im Ordner **Extensions.SalesTransactionSignatureSample\\bin\\Debug** finden Sie die folgenden Dateien:

    - Die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Die Konfigurationsdatei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopieren Sie die Dateien in den Ordner CRT-Erweiterungen:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

6. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

7. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

# <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent Beispielkomponente

1. Suchen Sie das Projekt **Runtime.Extensions.RegisterAuditEventSample** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.RegisterAuditEventSample\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature Beispielkomponente

1. Suchen Sie das Projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Ändern Sie die Datei **App.config**, indem Sie den Thumbprint, den Store und den Store-Namen für das Zertifikat angeben, das zum Signieren von Verkaufstransaktionen verwendet werden soll.
3. Erstellen Sie das Projekt.
4. Im Ordner **Extensions.SalesTransactionSignatureSample\\bin\\Debug** finden Sie die folgenden Dateien:

    - Die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Die Konfigurationsdatei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopieren Sie die Dateien in den Ordner CRT-Erweiterungen:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

6. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

7. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignatureSample.Messages Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.SalesTransactionSignatureSample.Messages**.
2. Suchen Sie im Ordner **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent Beispielkomponente

1. Suchen Sie das Projekt **Runtime.Extensions.RegisterAuditEventSample** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.RegisterAuditEventSample\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature Beispielkomponente

1. Suchen Sie das Projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Ändern Sie die Datei **App.config**, indem Sie den Thumbprint, den Store und den Store-Namen für das Zertifikat angeben, das zum Signieren von Verkaufstransaktionen verwendet werden soll.
3. Erstellen Sie das Projekt.
4. Im Ordner **Extensions.SalesTransactionSignatureSample\\bin\\Debug** finden Sie die folgenden Dateien:

    - Die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Die Konfigurationsdatei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopieren Sie die Dateien in den Ordner CRT-Erweiterungen:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

6. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

7. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponente SequentialSignatureRegister.Contracts

1. Suchen Sie das Projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Im Ordner **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** finden Sie die Assembly-Datei **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent Beispielkomponente

1. Suchen Sie das Projekt **Runtime.Extensions.RegisterAuditEventSample** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.RegisterAuditEventSample\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="sequentialsignatureregister-component"></a>Komponente SequentialSignatureRegister

1. Suchen Sie das Projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Ändern Sie die Datei **App.config**, indem Sie den Thumbprint, den Store und den Store-Namen für das Zertifikat angeben, das zum Signieren von Verkaufstransaktionen verwendet werden soll.
3. Erstellen Sie das Projekt.
4. Im Ordner **Extensions.SequentialSignatureRegister\\bin\\Debug** finden Sie die folgenden Dateien:

    - Die Assembly-Datei **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Die Konfigurationsdatei **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopieren Sie die Dateien in den Ordner CRT-Erweiterungen:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

6. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

7. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Suchen Sie im Ordner **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponente SequentialSignatureRegister.Contracts

1. Suchen Sie das Projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Im Ordner **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** finden Sie die Assembly-Datei **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

#### <a name="salespaymenttransextnorway-component"></a>Komponente SalesPaymentTransExtNorway

1. Suchen Sie das Projekt **Runtime.Extensions.SalesPaymentTransExtNorway** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway Komponente

1. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

2. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="sequentialsignatureregister-component"></a>Komponente SequentialSignatureRegister

1. Suchen Sie das Projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Ändern Sie die Datei **App.config**, indem Sie den Thumbprint, den Store und den Store-Namen für das Zertifikat angeben, das zum Signieren von Verkaufstransaktionen verwendet werden soll.
3. Erstellen Sie das Projekt.
4. Im Ordner **Extensions.SequentialSignatureRegister\\bin\\Debug** finden Sie die folgenden Dateien:

    - Die Assembly-Datei **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Die Konfigurationsdatei **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopieren Sie die Dateien in den Ordner CRT-Erweiterungen:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

6. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

7. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Suchen Sie im Ordner **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponente SequentialSignatureRegister.Contracts

1. Suchen Sie das Projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Im Ordner **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** finden Sie die Assembly-Datei **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

#### <a name="salespaymenttransextnorway-component"></a>Komponente SalesPaymentTransExtNorway

1. Suchen Sie das Projekt **Runtime.Extensions.SalesPaymentTransExtNorway** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway Komponente

1. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

2. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="sequentialsignatureregister-component"></a>Komponente SequentialSignatureRegister

1. Suchen Sie das Projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Ändern Sie die Datei **App.config**, indem Sie den Thumbprint, den Store und den Store-Namen für das Zertifikat angeben, das zum Signieren von Verkaufstransaktionen verwendet werden soll.
3. Erstellen Sie das Projekt.
4. Im Ordner **Extensions.SequentialSignatureRegister\\bin\\Debug** finden Sie die folgenden Dateien:

    - Die Assembly-Datei **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Die Konfigurationsdatei **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopieren Sie die Dateien in den Ordner CRT-Erweiterungen:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

6. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

7. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Suchen Sie im Ordner **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponente SequentialSignatureRegister.Contracts

1. Suchen Sie das Projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Im Ordner **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** finden Sie die Assembly-Datei **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

#### <a name="salespaymenttransextnorway-component"></a>Komponente SalesPaymentTransExtNorway

1. Suchen Sie das Projekt **Runtime.Extensions.SalesPaymentTransExtNorway** und erstellen Sie es.
2. Suchen Sie im Ordner **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Retail Server:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Retail Server:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Retail Server-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Bearbeiten Sie **nicht** die Dateien CommerceRuntime.config und CommerceRuntime.MPOSOffline.config. Diese Dateien sind nicht für irgendwelche Anpassungen gedacht.

---

### <a name="the-retail-server-extension-components"></a>Die Komponenten der Retail Server-Erweiterung

#### <a name="salestransactionsignature-retail-server-sample-component"></a>Beispielkomponente SalesTransactionSignature Retail Server

1. Suchen Sie im Ordner **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** das Projekt **RetailServer.Extensions.SalesTransactionSignatureSample** und erstellen Sie es.
2. Suchen Sie im Ordner **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** die Assembly-Datei **Contoso.RetailServer.SalesTransactionSignatureSample.dll**.
3. Kopieren Sie die Assembly-Datei in den Erweiterungsordner von Retail Server.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    Der Ordner ist der Ordner **\\bin** unter dem Standort des IIS Retail Servers.

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    Der Ordner ist der Ordner **\\bin** unter dem Standort des IIS Retail Servers.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Der Ordner ist der Ordner **\\bin\\ext** unter dem Speicherort des IIS Retail Server.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    Der Ordner ist der Ordner **\\bin\\ext** unter dem Speicherort des IIS Retail Server.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    Der Ordner ist der Ordner **\\bin\\ext** unter dem Speicherort des IIS Retail Server.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    Der Ordner ist der Ordner **\\bin\\ext** unter dem Speicherort des IIS Retail Server.

    ---

4. Suchen Sie die Konfigurationsdatei für Retail Server. Die Datei trägt den Namen **web.config** und befindet sich im Stammordner unter dem Standort des IIS Retail Servers.
5. Registrieren Sie die Retail Server Erweiterungen im Abschnitt **extensionComposition** der Konfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Registrieren Sie die Abhängigkeiten der Retail Server Erweiterungen.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4/)

    1. Im Ordner **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** finden Sie die folgenden Dateien:

        - Die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
        - Die Konfigurationsdatei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

    2. Kopieren Sie die Dateien in den Ordner **\\bin** unter dem Standort des IIS Retail Servers.
    3. Registrieren Sie die Änderung CRT in der Erweiterungskonfigurationsdatei für CRT. Diese Datei heißt **commerceruntime.ext.config** und befindet sich im Ordner **bin** unter dem IIS Retail Server Standort.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later/)

    1. Suchen Sie im Ordner **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
    2. Kopieren Sie die Datei in den Ordner **\\bin** unter dem Standort des IIS Retail Servers.
    3. Registrieren Sie die Änderung CRT in der Erweiterungskonfigurationsdatei für CRT. Diese Datei heißt **commerceruntime.ext.config** und befindet sich im Ordner **bin** unter dem IIS Retail Server Standort.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Es sind keine Aktionen erforderlich.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    > [!NOTE]
    > Es sind keine Aktionen erforderlich.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    > [!NOTE]
    > Es sind keine Aktionen erforderlich.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    > [!NOTE]
    > Es sind keine Aktionen erforderlich.

    ---

### <a name="the-modern-pos-extension-components"></a>Die Modern POS Erweiterungskomponenten

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Implementieren Sie den Proxy-Code für den Offline-Modus

Dieser Teil entspricht der Steuereinheit für den Retail Server, erweitert aber das lokale CRT, das verwendet wird, wenn der Client nicht verbunden ist.

1. Ändern Sie in der Datei **Customization.settings** den Abschnitt **@(RetailServerLibraryPathForProxyGeneration)** so, dass er die neue Retail Server-Assembly für die Proxy-Generierung verwendet.
2. Implementieren Sie die folgenden Schnittstellenmethoden in der Klasse **StoreOperationsManager**. Für die erste Iteration fügen Sie den folgenden Code hinzu:

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    ---

3. Um den Proxy-Code neu zu generieren, erstellen Sie den Ordner **Proxies** über die Befehlszeile mit dem Befehl **msbuild /t:Rebuild**.
4. Lösen Sie die **Proxies.RetailProxy** Projektabhängigkeiten auf:

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    Öffnen Sie **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, fügen Sie die **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** in die Lösung ein und fügen Sie dem Projekt **RetailProxy** einen Projektverweis auf **SalesTransactionSignatureSample** hinzu.

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    Öffnen Sie **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, fügen Sie die **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime. Extensions.SalesTransactionSignatureSample.Messages** in die Lösung ein und fügen Sie dem Projekt **RetailProxy** einen Projektverweis hinzu, um auf **SalesTransactionSignatureSample.Messages** zu verweisen.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    ---

5. Passen Sie die Schnittstellenmethoden in der Klasse **StoreOperationsManager** an:

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    > [!NOTE]
    > Dieser Schritt gilt nicht für diese Version.

    ---

6. Aktualisieren Sie die Datei **dllhost.exe.config**, damit der Client Broker die neue RetailProxy-Assembly lädt.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Retail-Proxy-Erweiterungskomponente (Retail 7.3.1 und höher)

Führen Sie das folgende Verfahren nur durch, wenn Sie Retail 7.3.1 und höher verwenden.

1. Suchen Sie im Ordner **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** das Projekt **RetailServer.Extensions.SalesTransactionSignatureSample**, und erstellen Sie es.
2. Suchen Sie im Ordner **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** die Assembly-Datei **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample**.
3. Kopieren Sie die Assembly-Dateien in den Ordner **\\ext** unter dem lokalen CRT Client Broker Speicherort.
4. Registrieren Sie die Retail Proxy-Änderung in der Erweiterungskonfigurationsdatei. Die Datei heißt **RetailProxy.MPOSOffline.ext.config** und befindet sich unter dem lokalen Speicherort des Client Brokers CRT.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Modern POS Erweiterungskomponenten

1. Öffnen Sie die Lösung unter **RetailSdk\\POS\\ModernPOS.sln**, und stellen Sie sicher, dass sie fehlerfrei kompiliert werden kann. Außerdem stellen Sie sicher, dass Sie Modern POS von Microsoft Visual Studio aus ausführen können, indem Sie den Befehl **Run** verwenden.

    > [!NOTE]
    > Modern POS darf nicht angepasst werden. Sie müssen die Benutzerkontensteuerung (UAC) aktivieren, und Sie müssen zuvor installierte Instanzen von Modern POS bei Bedarf deinstallieren.

2. Nehmen Sie die folgenden bestehenden Quellcode-Ordner in das Projekt **Pos.Extensions** auf.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Aktivieren Sie die Kompilierung der Erweiterungen in **tsconfig.json**, indem Sie die folgenden Ordner aus der Exclude-Liste entfernen.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Aktivieren Sie die Ladung der Erweiterungen in **extensions.json**, indem Sie die folgenden Zeilen an der entsprechenden Stelle hinzufügen.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Weitere Informationen und Beispiele, die zeigen, wie Quellcodeordner einbezogen werden und das Laden von Erweiterungen ermöglicht wird, finden Sie in den Anleitungen in der readme.md-Datei im Projekt **Pos.Extensions**.

5. Erstellen Sie die Lösung neu.
6. Führen Sie Modern POS im Debugger aus, und testen Sie die Funktionen.

### <a name="cloud-pos-extension-components"></a>Cloud POS Erweiterungskomponenten

1. Öffnen Sie die Lösung unter **RetailSdk\\POS\\CloudPOS.sln**, und stellen Sie sicher, dass sie fehlerfrei kompiliert werden kann.
2. Nehmen Sie die folgenden bestehenden Quellcode-Ordner in das Projekt **Pos.Extensions** auf.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Aktivieren Sie die zu kompilierenden Erweiterungen in der Datei **tsconfig.json**, indem Sie die folgenden Ordner aus der Ausschlussliste entfernen.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Aktivieren Sie die Ladung der Erweiterungen in **extensions.json**, indem Sie die folgenden Zeilen an der entsprechenden Stelle hinzufügen.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Weitere Informationen und Beispiele, die zeigen, wie Quellcodeordner einbezogen werden und das Laden von Erweiterungen ermöglicht wird, finden Sie in den Anleitungen in der readme.md-Datei im Projekt **Pos.Extensions**.

5. Erstellen Sie die Lösung neu.
6. Führen Sie Lösung aus, indem Sie den Befehl **Run** verwenden, und folgen Sie den Schritten im Retail SDK-Handbuch.
7. Testen Sie die Funktionalität.

### <a name="set-up-required-parameters-in-headquarters"></a>Erforderliche Parameter in Headquarters festlegen

Weitere Informationen finden Sie unter [Kassenfunktionalität für Norwegen](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Produktionsumgebung

Folgen Sie diesen Schritten, um bereitstellbare Pakete zu erstellen, die Commerce-Komponenten enthalten, und um diese Pakete in einer Produktionsumgebung anzuwenden.

1. Führen Sie die Schritte im Abschnitt [Erweiterungskomponenten für Cloud POS](#cloud-pos-extension-components) oder [Erweiterungskomponenten für Modern POS](#modern-pos-extension-components) weiter oben in diesem Artikel aus.
2. Nehmen Sie die folgenden Änderungen in den Paketkonfigurationsdateien unter dem Ordner **RetailSdk\\Assets** vor:

    1. Fügen Sie in den Konfigurationsdateien **commerceruntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** die folgenden Zeilen in den Abschnitt **composition** ein:

        # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Commerce Proxy-Anpassung aktivieren:

        # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

        Fügen Sie in der Konfigurationsdatei **dllhost.exe.config** im Unterabschnitt **appSettings** des Abschnitts **configuration** die folgenden Zeilen hinzu.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

        Fügen Sie in der Konfigurationsdatei **dllhost.exe.config** im Unterabschnitt **appSettings** des Abschnitts **configuration** die folgenden Zeilen hinzu.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Fügen Sie in der Konfigurationsdatei **RetailProxy.MPOSOffline.ext.config** im Abschnitt **Composition** die folgenden Zeilen hinzu:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

        Fügen Sie in der Konfigurationsdatei **RetailProxy.MPOSOffline.ext.config** im Abschnitt **Composition** die folgenden Zeilen hinzu:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

        Fügen Sie in der Konfigurationsdatei **RetailProxy.MPOSOffline.ext.config** im Abschnitt **Composition** die folgenden Zeilen hinzu:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

        Fügen Sie in der Konfigurationsdatei **RetailProxy.MPOSOffline.ext.config** im Abschnitt **Composition** die folgenden Zeilen hinzu:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Nehmen Sie die folgenden Änderungen in der Konfigurationsdatei **Customization.settings** für die Anpassung des Pakets vor:

    1. Aktivieren Sie die Anpassung des Retail Proxy.

        # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

        Fügen Sie die folgenden Zeilen in den Abschnitt **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** ein.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

        Fügen Sie die folgenden Zeilen in den Abschnitt **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** ein.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Fügen Sie die folgenden Zeilen in den Abschnitt **ItemGroup** ein, um die Erweiterung Retail proxy in die bereitzustellenden Pakete aufzunehmen:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

        Fügen Sie die folgenden Zeilen in den Abschnitt **ItemGroup** ein, um die Erweiterung Retail proxy in die bereitzustellenden Pakete aufzunehmen:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

        Fügen Sie die folgenden Zeilen in den Abschnitt **ItemGroup** ein, um die Erweiterung Retail proxy in die bereitzustellenden Pakete aufzunehmen:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

        Fügen Sie die folgenden Zeilen in den Abschnitt **ItemGroup** ein, um die Erweiterung Retail proxy in die bereitzustellenden Pakete aufzunehmen:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Fügen Sie die folgenden Zeilen in den Abschnitt **ItemGroup** ein, um die CRT-Erweiterungen in die bereitzustellenden Pakete aufzunehmen:

        # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Fügen Sie dem Abschnitt **ItemGroup** folgende Zeilen hinzu, um die Retail Server-Erweiterung in die bereitgestellten Pakete aufzunehmen:

        # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Ändern Sie die folgenden Dateien, um die Ressourcendateien für Norwegen in bereitzustellende Pakete aufzunehmen:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - Für die Datei **Sdk.ModernPos.Shared.csproj** 
    - Fügen Sie eine Zeile zum Abschnitt **ItemGroup** hinzu
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Geben Sie anstelle von <Dateiname> einen Namen für die Ressourcendatei an. Das Gleiche gilt für die anderen unten aufgeführten Beispiele.
 
    - Fügen Sie eine Zeile zum Abschnitt **Target Name="CopyPackageFiles"** hinzu
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - Für die Datei **Sdk.RetailServerSetup.proj** 
    - Fügen Sie eine Zeile zum Abschnitt **ItemGroup** hinzu
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Fügen Sie eine Zeile zum Abschnitt **Target Name="CopyPackageFiles"** hinzu
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Ändern Sie die Konfigurationsdatei des Zertifikats, indem Sie den Fingerabdruck, den Speicherort und den Namen des Stores für das Zertifikat angeben, das zum Signieren von Transaktionen verwendet werden soll. Kopieren Sie dann die Konfigurationsdatei in den Ordner **Referenzen**.

    # <a name="application-update-4"></a>[Anwendungsupdate 4](#tab/app-update-4)

    Die Datei heißt **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** und befindet sich unter **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="application-update-5-and-later"></a>[Anwendungsupdate 5 und höher](#tab/app-update-5-and-later)

    Die Datei heißt **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** und befindet sich unter **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Die Datei heißt **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** und befindet sich unter **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 und später](#tab/retail-7-3-2)

    Die Datei heißt **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** und befindet sich unter **Erweiterungen.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 und später](#tab/retail-7-3-5)

    Die Datei heißt **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** und befindet sich unter **Erweiterungen.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 und später](#tab/retail-8-1-1)

    Die Datei heißt **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** und befindet sich unter **Erweiterungen.SequentialSignatureRegister\\bin\\Debug**.

    ---
