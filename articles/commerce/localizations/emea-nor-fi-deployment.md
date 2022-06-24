---
title: Richtlinien für die Bereitstellung von Registrierkassen für Norwegen
description: Dieser Artikel enthält eine Anleitung zur Aktivierung der Kassenfunktionalität für die Lokalisierung Microsoft Dynamics 365 Commerce für Norwegen.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 1f2226432237662e28b9e26017020ab81bb6026b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899066"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Richtlinien für die Bereitstellung von Registrierkassen für Norwegen

[!include[banner](../includes/banner.md)]

Dieser Artikel enthält eine Anleitung zur Aktivierung der Kassenfunktionalität für die Lokalisierung Microsoft Dynamics 365 Commerce für Norwegen. Die Lokalisierung besteht aus mehreren Erweiterungen von Komponenten. Mit diesen Erweiterungen können Sie Aktionen wie das Drucken angepasster Felder auf Quittungen, das Registrieren zusätzlicher Audit-Ereignisse, Verkaufstransaktionen und Zahlungstransaktionen am Point of Sale (POS), das digitale Signieren von Verkaufstransaktionen und das Drucken von Berichten in lokalen Formaten durchführen. Weitere Informationen über die Lokalisierung für Norwegen finden Sie unter [Kassenfunktionalität für Norwegen](./emea-nor-cash-registers.md). Weitere Informationen darüber, wie Sie Commerce für Norwegen konfigurieren, finden Sie unter [Commerce für Norwegen einrichten](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Paketierungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für diese Lokalisierungsfunktionalität verwendet werden. Sie müssen die Version des digitalen Signierbeispiels für Norwegen in der vorherigen Version des Software Development Kit (SDK) für Retail auf einer virtuellen Maschine (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS) verwenden. Weitere Informationen finden Sie unter [Einsatzrichtlinien für Registrierkassen für Norwegen (veraltet)](./emea-nor-loc-deployment-guidelines.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

## <a name="set-up-fiscal-registration-for-norway"></a>Steuerliche Registrierung für Norwegen festlegen

Das Beispiel der Fiskalregistrierung für Norwegen basiert auf der [Fiskalintegrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil des Retail SDK. Das Beispiel befindet sich im Ordner **src\\FiscalIntegration\\SequentialSignatureNorway** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [das Beispiel in Release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) aus einem fiskalischen Beleg-Anbieter und einem fiskalischen Konnektor, die Erweiterungen der Commerce Runtime sind (CRT). Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

Schließen Sie die Schritte zur Einrichtung der Fiskalregistrierung ab, die unter [Einrichten der Fiskalintegration für Commerce-Kanäle](./setting-up-fiscal-integration-for-retail-channel.md) festgelegt sind:

1. [Richten Sie einen Steuererfassungsprozesses ein](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Notieren Sie sich unbedingt die Einstellungen des fiskalischen Registrierungsprozesses, die [Spezifisch für Norwegen](#configure-the-fiscal-registration-process) sind.
1. [Legen Sie Einstellungen zur Fehlerbehandlung fest](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurieren Sie die Channel-Komponenten](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Konfigurieren Sie den Prozess der steuerlichen Registrierung

Führen Sie diese Schritte aus, um den Prozess der steuerlichen Registrierung für Norwegen in der Commerce-Zentrale zu aktivieren.

1. Laden Sie die Konfigurationsdateien für den Fiskalbeleg-Anbieter und den Fiskal-Konnektor aus dem Commerce SDK herunter:

    1. Öffnen Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository.
    1. Öffnen Sie den letzten verfügbaren Branch der Version (z.B. **[Release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Öffnen Sie **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Laden Sie die Konfigurationsdatei des fiskalischen Belegs herunter unter **DocumentProvider.SequentialSignNorway \> Konfiguration \> DocumentProviderSequentialSignatureNorwaySample.xml** (zum Beispiel [die Datei für Release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)).
    1. Laden Sie die Konfigurationsdatei des Fiskalkonnektors unter **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml** herunter (zum Beispiel [die Datei für Release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)).

1. Gehen Sie zu **Retail und Commerce \> Einrichtung der Zentrale \> Parameter \> Gemeinsame Parameter**. Auf der Registerkarte **Allgemein** legen Sie die Option **Steuerintegration aktivieren** auf **Ja** fest.
1. Gehen Sie zu **Retail und Commerce \> Channel Einrichtung \> Fiskalische Integration \> Fiskalische Konnektoren**, und laden Sie die Konfigurationsdatei für den Fiskalischen Konnektor, die Sie zuvor heruntergeladen haben.
1. Gehen Sie zu **Handel und Commerce \> Channel-Einrichtung \> Fiskalische Integration \> Fiskalische Belege**, und laden Sie die Konfigurationsdatei des Fiskalischen Belegs, die Sie zuvor heruntergeladen haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Konnektorfunktionsprofile**. Erstellen Sie ein neues funktionales Konnektorprofil, und wählen Sie den Dokumentanbieter und den Konnektor aus, den Sie vorher geladen haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Technische Profile des Connectors**. Erstellen Sie ein neues technisches Konnektorprofil, und wählen Sie den Konnektor aus, den Sie vorher geladen haben. Legen Sie den Typ des Konnektors auf **Intern** fest.
1. Gehen Sie zu **Retail und Commerce \> Einrichtung der Kanäle \> Fiskalische Integration \> Fiskalische Konnektoren**, und erstellen Sie eine neue fiskalische Konnektorengruppe für das Konnektoren-Funktionsprofil, das Sie zuvor erstellt haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuererfassungsprozesse**. Erstellen Sie einen neuen Fiskalregistrierungsprozess und einen Fiskalregistrierungsprozessschritt und wählen Sie die Fiskalkonnektorgruppe, die Sie zuvor erstellt haben.
1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**. Wählen Sie ein Funktionsprofil aus, das mit dem Einzelhandelsgeschäft verbunden ist, wo der Erfassungsprozess aktiviert werden soll. Im Inforegister **Steuererfassungsprozess** aktivieren Sie den Steuererfassungsprozess, den Sie vorher erstellt haben. Wählen Sie auf der Seite **Steuerdienste** Inforegister das technische Profil des Konnektors, das Sie zuvor erstellt haben. 
1. Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**. Öffnen Sie den Verteilungsplan und wählen Sie die Aufträge **1070** und **1090** aus, um Daten an die Channel-Datenbank zu übertragen.

### <a name="configure-the-digital-signature-parameters"></a>Konfigurieren Sie die Parameter für die digitale Signatur

Sie müssen die Zertifikate konfigurieren, die für die digitale Unterzeichnung von Transaktionen in einem Store verwendet werden sollen. Ein digitales Zertifikat, das in Azure Key Vault gespeichert ist, wird für die Signierung verwendet. Für den Offline-Modus von Modern POS kann die Signierung auch mit einem digitalen Zertifikat erfolgen, das im lokalen Speicher des Rechners gespeichert ist, auf dem Modern POS installiert ist.

Bevor Sie ein digitales Zertifikat verwenden können, das im Key Vault gespeichert ist, müssen die folgenden Schritte ausgeführt werden.

1. Der Key Vault Speicher muss erstellt werden. Wir empfehlen Ihnen, den Speicher in der gleichen geografischen Region wie die Commerce Scale Unit bereitzustellen.
1. Das Zertifikat muss als base64-String-Geheimnis in den Key Vault-Speicher hochgeladen werden.
1. Die Anwendung Application Object Server (AOS) muss autorisiert sein, Geheimnisse aus dem Key Vault-Speicher zu lesen.

Weitere Informationen über die Arbeit mit Key Vault finden Sie unter [Einführung in Azure Key Vault](/azure/key-vault/key-vault-get-started).

Als nächstes müssen Sie auf der Seite **Key Vault Parameter** die Parameter für den Zugriff auf den Key Vault Speicher angeben:

- **Name** und **Beschreibung** - Der Name und die Beschreibung des Key Vault Speichers.
- **Key Vault URL** - Die URL des Key Vault Speichers.
- **Key Vault Client** - Eine interaktive Client ID der Anwendung Azure Active Directory (Azure AD), die zu Authentifizierungszwecken mit dem Key Vault Speicher verbunden ist. Dieser Client sollte Zugriff auf die Lesegeheimnisse des Speichers haben.
- **Key Vault geheimer Schlüssel** - Ein geheimer Schlüssel, der mit der Anwendung Azure AD verbunden ist, die für die Authentifizierung im Key Vault-Speicher verwendet wird.
- **Name**, **Beschreibung** und **Geheime Referenz** - Der Name, die Beschreibung und die geheimen Referenz des Zertifikats.

Als nächstes müssen Sie einen Konnektor für Ihre Zertifikate konfigurieren, die in Key Vault oder im lokalen Zertifikatspeicher gespeichert sind. Dieser Konnektor wird zum Signieren auf der Kanalseite verwendet.

1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Technische Profile des Connectors**.
1. Legen Sie auf der Registerkarte **Einstellungen** Inforegister die folgenden Parameter für digitale Signaturen fest:

    - **Geheimname** - Wählen Sie den Geheimnamen aus, den Sie zuvor auf der Seite **Key Vault Parameter** konfiguriert haben.
    - **Lokaler Zertifikats-Thumbprint** - Geben Sie einen Thumbprint für ein Zertifikat an, das lokal gespeichert ist.
    - **Hash-Algorithmus** - Geben Sie einen der kryptographischen Hash-Algorithmen an, die von Microsoft .NET unterstützt werden, z.B. **SHA1**.
    - **Name des Zertifikatsspeichers** - Dieses Feld ist optional. Verwenden Sie dieses Feld, um einen Standardspeichernamen festzulegen, der zum Durchsuchen lokaler Zertifikate verwendet werden soll.
    - **Speicherort des Zertifikats** - Dieses Feld ist optional. Verwenden Sie dieses Feld, um einen Standardspeicherort festzulegen, der zum Durchsuchen lokaler Zertifikate verwendet werden soll.
    - **Lokales Zertifikat zuerst ausprobieren** - Wählen Sie diese Option, um standardmäßig das Zertifikat aus dem lokalen Store zum Signieren von Daten zu verwenden, anstatt das Zertifikat aus Key Vault.
    - **Statusprüfung aktivieren** - Weitere Informationen über die Funktion der Statusprüfung finden Sie unter [Statusprüfung der steuerlichen Registrierung](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Für Norwegen ist derzeit nur der kryptografische Hash-Algorithmus **SHA1** zulässig.
> - Der Standardname des Stores und der Standort des Stores wurden hinzugefügt, um die Suche nach lokalen Zertifikaten in CRT zu vereinfachen. X509StoreProvider verfügt über eine Liste von Ordnern, in denen Zertifikate gespeichert sind. Wenn der Standard-Store-Name und der Standard-Speicherort nicht angegeben sind, versucht X509StoreProvider, ein Zertifikat in allen Ordnern auf seiner Liste zu finden.

### <a name="configure-channel-components"></a>Konfigurieren Sie die Channel-Komponenten

### <a name="development-environment"></a>Entwicklungsumgebung

Gehen Sie folgendermaßen vor, um eine Entwicklungsumgebung einzurichten, damit Sie das Beispiel testen und erweitern können.

1. Klonen oder laden Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository herunter. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion. Weitere Informationen finden Sie unter [Herunterladen von Retail SDK Beispielen und Referenzpaketen von GitHub und NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Öffnen Sie die Lösung **SequentialSignatureNorway.sln** unter **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway**, und erstellen Sie sie.
1. Installieren Sie CRT Erweiterungen:

    1. Suchen Sie das Installationsprogramm für die Erweiterung CRT:

        - **Commerce Scale Unit:** Im Ordner **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** finden Sie das Installationsprogramm **ScaleUnit.SequentialSignNorway.Installer**.
        - **Lokal CRT auf Modern POS:** Im Ordner **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461** finden Sie den **ModernPos.SequentialSignNorway.Installer** Installer.

    1. Starten Sie das Installationsprogramm für die CRT-Erweiterung über die Befehlszeile:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT auf Modern POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Produktionsumgebung

Legen Sie die Schritte unter [Einrichten einer Build-Pipeline für ein Fiskalintegrationsbeispiel](fiscal-integration-sample-build-pipeline.md) fest, um die Cloud Scale-Unit und die Self-Service bereitstellbaren Pakete für das Fiskalintegrationsbeispiel zu erzeugen und freizugeben. Die **SequentialSignatureNorway build-pipeline.yaml** Vorlage YAML-Datei finden Sie im Ordner **Pipeline\\YAML_Files** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Aktivieren Sie die digitale Signatur im Offline-Modus für Modern POS

Um die digitale Signatur im Offline-Modus für Modern POS zu aktivieren, müssen Sie diese Schritte ausführen, nachdem Sie Modern POS auf einem neuen Gerät aktiviert haben.

1. Melden Sie sich bei POS an.
1. Stellen Sie auf der Seite **Status der Datenbankverbindung** sicher, dass die Offline-Datenbank vollständig synchronisiert ist. Wenn der Wert des Feldes **Ausstehende Downloads** **0** (Null) ist, ist die Datenbank vollständig synchronisiert.
1. Melden Sie sich von POS ab.
1. Warten Sie, bis die Offline-Datenbank vollständig synchronisiert ist.
1. Melden Sie sich bei POS an.
1. Stellen Sie auf der Seite **Status der Datenbankverbindung** sicher, dass die Offline-Datenbank vollständig synchronisiert ist. Wenn der Wert des Feldes **Ausstehende Transaktionen in der Offline-Datenbank** **0** (Null) ist, ist die Datenbank vollständig synchronisiert.
1. Öffnen Sie Modern POS erneut.
