---
title: Verlassene Warenkörbe erkennen und Benachrichtigungen an die Kunden senden
description: In diesem Thema wird beschrieben, wie Sie die Microsoft Dynamics 365 Commerce Konnektor-Beispiel-App für verlassene Warenkörbe anpassen, um verlassene Warenkörbe zu erkennen und Erinnerungs-E-Mail-Benachrichtigungen an Kunden zu senden.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 82848f1ff068cea0adfc6ec1b33fc4bb035f78dc
ms.sourcegitcommit: 374bbdde90fc9a68c0799158a50409bfbe8ca64e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/25/2022
ms.locfileid: "8353361"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Verlassene Warenkörbe erkennen und Benachrichtigungen an die Kunden senden

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die Microsoft Dynamics 365 Commerce Konnektor-Beispiel-App für verlassene Warenkörbe anpassen, um verlassene Warenkörbe zu erkennen und Erinnerungs-E-Mail-Benachrichtigungen an Kunden zu senden.

Die Möglichkeit, Umsätze zurückzugewinnen und Kunden durch Benachrichtigungen über abgebrochene Warenkörbe zu binden, ist eine wichtige Funktionalität, die Dynamics 365 Commerce unterstützt. Durch die Anpassung der Beispiel-App für den Commerce Konnektor für aufgegebene Warenkörbe können Einzelhändler auf Warenkörbe auf dem Retail Server zugreifen, die während eines vom Einzelhändler definierten Zeitfensters nicht geändert wurden. Diese Warenkörbe können dann abgerufen, mit Produkt- und Kundendaten angereichert und an einen Drittanbieter für E-Mail-Marketing weitergeleitet werden, der E-Mail-Benachrichtigungen generieren und an die Kunden senden kann.

Die E-Mail-Benachrichtigung über den abgebrochenen Einkaufswagen, die Kunden erhalten, kann die folgenden Informationen enthalten:

- Den Vornamen des Kunden.
- Der Nachname des Kunden.
- Wählen Sie die E-Mail-Adresse des Kunden aus.
- Eine URL, die den Kunden zu seinem Warenkorb zurückführt.
- Die Währung der Transaktion.
- Eine Liste der Produkte im Einkaufswagen des Kunden. Für jedes Produkt sind die folgenden Informationen enthalten:

    - Der Anzeigename des Produkts
    - Die Produkt-ID (wird verwendet, um eine URL zur Produktbeschreibungsseite zusammenzustellen)
    - Ein Produktbild, das automatisch in der Größe verändert werden kann, um sich an verschiedene Ansichtsgrößen anzupassen
    - Alt-Text für das Produktbild
    - Der Preis pro Einheit des Produkts

## <a name="abandoned-cart-connector-sample"></a>Beispiel für den Konnektor Abandoned Cart

Ein Konnektor-Modell, das Microsoft über das Software Development Kit (SDK) für den Einzelhandel bereitstellt, ermöglicht es, Informationen über abgebrochene Einkäufe abzurufen und an einen E-Mail-Marketing-Anbieter einer anderen Partei zu senden. Dieser Konnektor verwaltet die Kommunikation mit Retail Server, verwendet Azure Key Vault für die Sicherheit, plant den Abruf von Warenkörben für ein bestimmtes Zeitfenster und ruft Bestell- und Produktdaten ab. Es bietet auch eine Beispielimplementierung für die Integration mit einem E-Mail-Marketing-Anbieter einer anderen Partei. Der Konnektor ist so aufgebaut, dass er mit [Emarsys](https://emarsys.com) standardmäßig kommuniziert. Es kann jedoch leicht angepasst werden, um mit anderen Lösungen wie Constant Contact, Mailchimp und SendGrid integriert zu werden.

Die folgende Abbildung zeigt die Komponenten der Beispiel-App für den Konnektor für verlassene Warenkörbe.

![Komponenten der Beispiel-App für den Konnektor für abgebrochene Einkäufe](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> In einigen Regionen müssen Kunden die Möglichkeit haben, die Weitergabe ihrer Warenkorbdaten an einen E-Mail-Marketing-Anbieter abzulehnen oder die Löschung ihrer Daten zu verlangen. Microsoft stellt diese Optionen für Kunden jedoch nicht zur Verfügung. Wenn Sie also planen, in Regionen tätig zu werden, in denen dies vorgeschrieben ist, müssen Sie die erforderliche Infrastruktur und Anpassungen bereitstellen, um die Präferenzen der Kunden zu verfolgen und auf der Grundlage dieser Präferenzen zu verhindern, dass Kundendaten an Ihre E-Mail-Plattform weitergegeben werden. Außerdem müssen Sie einen Prozess definieren, um die Kundendaten auf Wunsch des Kunden von Ihrem E-Mail-Marketing-Anbieter zu löschen.

## <a name="obtain-the-code-sample"></a>Holen Sie sich das Codebeispiel

Die Beispiel-App für den Konnektor für aufgegebene Warenkörbe ist im Retail SDK ab Version 10.0.16 enthalten. Den Code finden Sie unter **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample**. Weitere Informationen über das Retail SDK und wo Sie es erhalten können, finden Sie unter [Retail Software Development Kit (SDK)](retail-sdk/retail-sdk-overview.md).

> [!NOTE]
> Obwohl der Beispielcode erstmals in den Builds der Version 10.0.16 zur Verfügung gestellt wurde, ist er mit der Version 10.0.13 und späteren Builds von Retail Server kompatibel.

## <a name="prerequisites-and-dependencies"></a>Voraussetzungen und Abhängigkeiten

Bevor Sie den Beispielcode des Konnektors für verlassene Warenkörbe bereitstellen und konfigurieren können, müssen die folgenden Voraussetzungen erfüllt sein.

### <a name="access-to-commerce-resources"></a>Zugriff auf Commerce-Ressourcen

Um die App für den Konnektor für verlassene Warenkörbe zu konfigurieren und bereitzustellen, müssen Sie Zugriff auf die folgenden Ressourcen von Commerce haben:

- Administrator-Zugriff auf die Commerce-Zentrale für Ihre Umgebung
- Zugriff auf das Lifecycle Services (LCS)-Projekt Microsoft Dynamics für Ihre Umgebung

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Die App für den Konnektor für aufgegebene Warenkörbe verwendet Azure Cosmos DB, um die IDs und Zeitstempel von Warenkörben zu verfolgen, die zuvor abgerufen wurden. Sie können Azure Cosmos DB verwenden, um diese Daten aufzubewahren, oder Sie können das Codebeispiel anpassen, um es in eine andere Datenspeicheroption zu integrieren. Weitere Informationen über Azure Cosmos DB finden Sie unter [Willkommen in Azure Cosmos DB](/azure/cosmos-db/introduction).

Wenn Sie Azure Cosmos DB verwenden, müssen die folgenden Voraussetzungen erfüllt sein, bevor Sie das Beispiel ausführen können:

- Sie müssen ein aktives Azure Cosmos DB Konto haben. Wenn Sie kein Konto haben, lesen Sie [Erstellen Sie ein Datenbankkonto](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Sie müssen die Werte **URI** und **PRIMARY KEY** (oder **SECONDARY KEY**) aus dem **Keys**-Blade Ihres Azure Cosmos DB Kontos im Azure-Portal abrufen. Weitere Informationen zum Abrufen von Endpunkt- und Schlüsselinformationen für Ihr Azure Cosmos DB-Konto finden Sie unter [Zugriffsschlüssel und Kennwörter anzeigen, kopieren und neu generieren](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

Die App für den Konnektor für aufgegebene Warenkörbe verwendet Key Vault, um die Namen und Geheimnisse der verschiedenen Komponenten zu speichern, die einen sicheren Zugriff erfordern.

Um einen Key Vault festzulegen, führen Sie diese Schritte aus.

1. Befolgen Sie die Anweisungen in [Verwalten Sie Key Vault in Azure Stack Hub über das Portal](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. Erstellen Sie Geheimnisse für die folgenden Informationen:

    - Emarsys-Benutzername und API-Geheimnis (Application Programming Interface)
    - Abandoned Cart Application ID und Geheimnis

Der Beispielcode des Konnektors für abgebrochene Warenkörbe verwendet Azure-Standard-Anmeldeinformationen für den Zugriff auf Key Vault. Sie müssen der Identität, die Sie für den Zugriff auf Key Vault verwenden möchten, die Berechtigungen **Liste** und **Lesen** erteilen.

Weitere Informationen über Azure Anmeldeinformationen finden Sie unter [DefaultAzureCredential Klasse](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Erstellen Sie einen Konnektor für die Beispiel-App Abandoned Cart Application ID für den Azure AD Mandant

Sie müssen einen Konnektor für die Beispiel-App „abandoned cart“ erstellen, der die Anwendungs-ID für den Mandant Azure Active Directory (AD) enthält. Informationen darüber, wie Sie eine Anwendungs-ID erstellen, finden Sie unter [Verwenden Sie das Portal, um ein Azure AD-Anwendungs- und Service-Prinzipal zu erstellen, das auf Ressourcen zugreifen kann](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Fügen Sie die Anwendungs-ID des Konnektors für die App „abandoned cart“ zur Liste der zugelassenen Anwendungen für die Retail Server API hinzu.

Als Nächstes müssen Sie die Anwendungs-ID des Konnektors für die Beispiel-App „Abgebrochener Warenkorb“ zur Liste der zugelassenen Anwendungen für die Retail Server API hinzufügen. Informationen darüber, wie Sie eine Anwendungs-ID zur Liste der zugelassenen Anwendungen in Azure hinzufügen, finden Sie unter [Unterstützung für die Service-to-Service-Authentifizierung in Retail Server](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Konfigurieren Sie die Beispiel-App für den Konnektor für abgebrochene Einkäufe

Um die Beispiel-App für den Konnektor für verlassene Warenkörbe zu konfigurieren, ändern Sie die Konfigurationsdatei **appSettings.json**, die sich im Stammverzeichnis des Verzeichnisses **AbandonedCartDetectionSample** befindet. Die folgenden Tabellen beschreiben die Eigenschaften der Konfigurationsdatei.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Eigenschaft    | Description |
| ----------- | ----------- |
| KeyVaultURI | Der DNS-Name (Domain Name System) des Key Vault, den Sie im Azure-Portal verwenden. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Eigenschaft                                      | Description |
| --------------------------------------------- | ----------- |
| TenantId                                      | Die Azure AD Mandant-ID Ihres Azure-Mandanten. |
| RetailServerAudienceId                        | Die Retail Server Zielgruppe ID. Sie können den Standardwert beibehalten. |
| AppIdKeyVaultSecretName                       | Der Name des Geheimnisses, das Sie für die Anwendungs-ID des Konnektors für verlassene Einkaufswagen erstellt haben. |
| AppSecretKeyVaultSecretName                   | Der Name des Geheimnisses, in dem das App-Geheimnis für die Beispielanwendung ID des Konnektors für verlassene Warenkörbe gespeichert ist. |
| RetailServerUrl                               | Die URL Ihrer Retail Server-Instanz. Sie finden diesen Wert in LCS. |
| OperatingUnitNumber                           | Die Nummer der operativen Einheit (OUN). Diesen Wert finden Sie in der Commerce-Zentrale. |
| IncludeAbandonedCartsModifiedSinceLastMinutes | Der Beginn des Zeitfensters für die aufgegebenen Warenkörbe, die Sie zurückholen möchten. Der Wert wird als Anzahl der Minuten vor der aktuellen Zeit angegeben. Legen Sie diese Eigenschaft z.B. auf **120** fest, um alle Kartons abzurufen, die zwischen vor 120 Minuten und dem Ende des Zeitfensters, das durch die Eigenschaft **ExcludeAbandonedCartsModifiedSinceLastMinutes** definiert ist, zuletzt geändert wurden. |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | Das Ende des Zeitfensters für die abgebrochenen Warenkörbe, die Sie abrufen möchten. Der Wert wird als Anzahl der Minuten vor der aktuellen Zeit angegeben. Wenn zum Beispiel die Eigenschaft **IncludeAbandonedCartsModifiedSinceLastMinutes** auf **120** festgelegt ist, legen Sie diese Eigenschaft auf **30** fest, um alle Warenkörbe abzurufen, die zwischen vor 120 Minuten und vor 30 Minuten geändert wurden. In der Praxis definiert diese Eigenschaft die Zeitspanne, die Sie warten möchten, bevor ein Einkaufswagen als aufgegeben erklärt wird. |
| ReturnToCartUrl                               | Die URL des Warenkorbs auf Ihrer E-Commerce Website, in dem Format, das in der Datei **app.config** verwendet wird. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

Der Status des Abrufs des abgebrochenen Warenkorbs, die IDs der Warenkörbe und die Zeitstempel der Änderungen werden in Azure Cosmos DB gespeichert. Standardmäßig verweisen die Einstellungen in der Konfigurationsdatei auf die lokale Emulatorinstanz von Azure Cosmos DB. Wenn Sie den Konnektor für die Produktion bereitstellen, müssen Sie diese Einstellungen aktualisieren, damit sie auf die Azure-Instanz Cosmos DB in Ihrem Azure Abonnement verweisen. Für lokale oder Sandbox-Tests können Sie den [Azure Cosmos Emulator](/azure/cosmos-db/local-emulator) verwenden.

| Eigenschaft    | Description |
| ----------- | ----------- |
| EndPointUri | Die Endpunkt-URI, die von Azure oder dem Emulator bereitgestellt wird. |
| PrimaryKey  | Der Primärschlüssel, der von Azure oder dem Emulator bereitgestellt wird. |
| DatabaseId  | Die Datenbank-ID. Sie können den Standardwert beibehalten oder einen eigenen Wert angeben. |
| ContainerId | Die Container ID. Sie können den Standardwert beibehalten oder einen eigenen Wert angeben. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Wenn Sie eine Integration mit einem anderen E-Mail-Marketing-Anbieter als Emarsys vornehmen, müssen Sie die **IEmailProvider**-Schnittstelle entsprechend erweitern, um mit diesem Anbieter zu kommunizieren.

| Eigenschaft                      | Description |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | Die ID des externen Datensatzes für ein Ereignis, der in Emarsys erstellt wird. Sie finden den Wert unter **Trigger-Einstellungen** in der Kampagne, die Sie erstellt haben, um E-Mail-Benachrichtigungen über verlassene Warenkörbe zu versenden. |
| ApiUserNameKeyVaultSecretName | Der Name des Schlüssels, unter dem der Emarsys API-Benutzername gespeichert ist. |
| ApiSecretKeyVaultSecretName   | Der Name des Schlüssels, in dem das Emarsys API-Geheimnis gespeichert ist. |
| EmarsysContactKeyId           | Die ID der E-Mail-Spalte in der Emarsys-Kontaktdatenbank. Der Standardwert ist **3** und sollte nicht geändert werden müssen. |

### <a name="mediaoptions"></a>MediaOptions

Wenn Sie die E-Commerce Funktionalitäten in Commerce nutzen, können Sie das Digital Asset-Management von Commerce verwenden, um Produktbilder abzurufen. Weitere Informationen über die Funktionalitäten zur Bildvergrößerung in der digitalen Asset-Verwaltung finden Sie unter [ImageSettings Viewport Konfiguration](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Eigenschaft                             | Description |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Die Stamm-URL des Digital Asset Managers Ihrer Website. Sie finden den Wert im Eigenschaftsschlüssel **Media Server Base URL** unter **Retail und Commerce \> Einrichtung \> Channel-Profile** in der Commerce Zentrale. |
| ImageViewPorts                       | Der Container-Knoten für die einzelnen Viewport-Konfigurationen. |
| ImageViewPorts/viewport              | Die Definition des Ansichtsfensters. Verwenden Sie diese Eigenschaft, um die Breitenbereiche für das Ansichtsfenster in Pixeln anzugeben. Ein Beispiel dafür, wie diese Eigenschaft verwendet wird, finden Sie in der Konfigurationsdatei **appSettings.json**. |
| ImageViewPorts/imageWidth            | Die Bildbreite des Ansichtsfensters, in Pixeln. |
| imageViewPorts/imageHeight           | Die Bildhöhe des Ansichtsfensters, in Pixeln. |
| imageViewPorts/useForDefaultImageTag | Ein **wahrer**/**falscher** Wert, der angibt, ob die durch das Ansichtsfenster definierten Dimensionen des Bildes verwendet werden sollen, wenn das `<picture>` HTML-Tag von einem Webbrowser oder E-Mail Client nicht unterstützt wird. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
