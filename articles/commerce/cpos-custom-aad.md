---
title: CPOS für die Verwendung einer benutzerdefinierten Azure AD App konfigurieren
description: In diesem Artikel wird erläutert, wie Sie Cloud POS (CPOS) für die Verwendung einer benutzerdefinierten Azure Active Directory (Azure AD) App konfigurieren.
author: boycez
ms.date: 08/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: baa0c3da25308345037b5dd1b4c5907d6213e7f7
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/03/2022
ms.locfileid: "9222968"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>CPOS für die Verwendung einer benutzerdefinierten Azure AD App konfigurieren

[!include [banner](includes/banner.md)]

Standardmäßig verweist Cloud POS (CPOS) in Microsoft Dynamics 365 Commerce auf eine registrierte Erstanbieter-Microsoft-App im Azure Active Directory (Azure AD). Daher können Sie CPOS verwenden, ohne Änderungen an Azure AD vornehmen zu müssen. Möglicherweise möchten Sie jedoch, dass Ihre Instanz von CPOS auf eine benutzerdefinierte Azure AD App verweist, die Sie steuern. In diesem Artikel wird erläutert, wie Sie CPOS für die Verwendung einer benutzerdefinierten Azure AD App konfigurieren.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Eine benutzerdefinierte Retail Server-App in Azure AD einrichten

Mit den folgenden Schritten erstellen und konfigurieren Sie eine benutzerdefinierte Retail-Server-App in Azure AD.

1. Melden Sie sich im [Azure Active Directory Admin Center](https://aad.portal.azure.com) über ein Azure AD Benutzerkonto an. Das Benutzerkonto muss nicht zwingend Administratorrechte haben.
1. Wählen Sie **Azure Active Directory**.
1. Wählen Sie **App-Registrierungen** und dann **Neue Registrierung** aus, um das Dialogfeld **Eine Anwendung registrieren**.
1. Stellen Sie die folgenden Felder ein:

    - **Name**: Geben Sie einen benutzerdefinierten Namen für die App ein. Geben Sie beispielsweise **Benutzerdefinierter Retail Server** ein.
    - **Unterstützte Kontotypen**: Wählen Sie die Standardoption **Konten nur in diesem Organisationsverzeichnis (nur Microsoft – einzelner Mandant)** aus.
    - **URI umleiten**: Dieses Feld ist optional. Lassen Sie es frei.
    - **Dienststruktur-ID**: Dieses Feld ist optional. Lassen Sie es frei.
    
1. Wählen Sie **Registrieren** aus. Die Konfigurationsseite für die neu registrierte App wird angezeigt.
1. Wählen Sie im Abschnitt **Überblick \> Grundlagen** **Eine Anwendungs-ID-URI hinzufügen**. Wählen Sie dann **Festlegen** neben **Anwendungs-ID-URI**. Notieren Sie sich den vorgeschlagenen Wert und wählen Sie dann **Speichern** aus, um diesen Wert zu akzeptieren. 
1. Wählen Sie **Einen Geltungsbereich hinzufügen** und legen Sie dann die folgenden Felder fest:

    - **Geltungsbereichsname**: Geben Sie einen benutzerdefinierten Namen für den Geltungsbereich ein. Geben Sie beispielsweise **Legacy.Access.Full** ein.
    - **Wer kann zustimmen**: Geben Sie basierend auf den Sicherheitsrichtlinien Ihrer Organisation an, ob sowohl Administratoren als auch Benutzer oder nur Administratoren ihre Zustimmung erteilen können.
    - **Anzeigename der Administratoreinwilligung**: Geben Sie einen Anzeigenamen ein. Geben Sie beispielsweise **Zugriff auf Retail Server** ein.
    - **Beschreibung Administratoreinwilligung**: Geben Sie eine Beschreibung ein. Geben Sie beispielsweise **Erteilt Zugriff auf Retail-Server-APIs** ein.

1. Wählen Sie **Geltungsbereich hinzufügen**, um den Prozess zur Erstellung des Geltungsbereichs abzuschließen.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Eine benutzerdefinierte COPS-App in Azure AD einrichten

Mit den folgenden Schritten erstellen und konfigurieren Sie eine benutzerdefinierte COPS-App in Azure AD.

1. Melden Sie sich im [Azure Active Directory Admin Center](https://aad.portal.azure.com) über ein Azure AD Benutzerkonto an. Das Benutzerkonto muss nicht zwingend Administratorrechte haben.
1. Wählen Sie **Azure Active Directory**.
1. Wählen Sie **App-Registrierungen** und dann **Neue Registrierung** aus, um das Dialogfeld **Eine Anwendung registrieren**.
1. Stellen Sie die folgenden Felder ein:

    - **Name** – Geben Sie einen Namen für die App ein. Geben Sie beispielsweise **Benutzerdefinierte Cloud-POS** ein.
    - **Unterstützte Kontotypen**: Wählen Sie die Standardoption **Konten nur in diesem Organisationsverzeichnis (nur Microsoft – einzelner Mandant)** aus.
    - **Umleitungs-URI**: Wählen Sie **Single-Page-Anwendung (SPA)** aus der Dropdownliste aus und geben Sie dann Ihre CPOS-URI ein.
    - **Dienststruktur-ID**: Dieses Feld ist optional. Lassen Sie es frei.

1. Wählen Sie **Registrieren** aus. Die Konfigurationsseite für die neu registrierte App wird angezeigt.
1. Legen Sie im Bereich **Manifest** die Parameter **oauth2AllowIdTokenImplicitFlow** und **oauth2AllowImplicitFlow** auf **wahr** fest und wählen Sie dann **Speichern** aus.
1. Fügen Sie im Bereich **Token-Konfiguration** folgendermaßen zwei Ansprüche hinzu:

    - Wählen Sie **Zusätzlichen Anspruch hinzufügen** aus. Legen Sie das Feld **Token-Typ** auf **ID** fest und wählen Sie dann den Anspruch **sid** aus. Wählen Sie **Hinzufügen** aus.
    - Wählen Sie **Zusätzlichen Anspruch hinzufügen** aus. Legen Sie das Feld **Token-Typ** auf **Zugriff** fest und wählen Sie dann den Anspruch **sid** aus. Wählen Sie **Hinzufügen** aus.

1. Wählen Sie im Bereich **API-Berechtigungen** **Eine Berechtigung hinzufügen**.
1. Suchen Sie auf der Registerkarte **Von meiner Organisation verwendete APIs** nach der Retail-Server-App, die Sie im Bereich [Eine benutzerdefinierte Retail-Server-App in Azure AD einrichten](#set-up-a-custom-retail-server-app-in-azure-ad). Wählen Sie dann **Berechtigungen hinzufügen**.
1. Notieren Sie aus dem Bereich **Überblick** den Wert des Felds **Anwendungs-(Client-)ID**.

## <a name="update-the-cpos-configuration-file"></a>Die CPOS-Konfigurationsdatei aktualisieren

Öffnen Sie die CPOS-config.json-Datei und nehmen Sie die folgenden Aktualisierungen darin vor.

1. Ersetzen Sie den **AADClientId**-Schlüsselwert mit dem Wert **Anwendungs-(Client-)ID** der benutzerdefinierten CPOS-App, die Sie im Bereich [Eine benutzerdefinierte CPOS-App in Azure AD einrichten](#set-up-a-custom-cpos-app-in-azure-ad) erstellt haben.
1. Ersetzen Sie den **AADRetailServerResourceId**-Schlüsselwert mit dem **Anwendungs-ID-URI**-Wert der benutzerdefinierten Retail-Server-App, die Sie im Bereich [Eine benutzerdefinierte Retail-Server-App in Azure AD einrichten](#set-up-a-custom-retail-server-app-in-azure-ad) erstellt haben.

CPOS verwendet beide Parameter, wenn es Anfragen an Azure AD sendet, um ein Sicherheitstoken abzurufen.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Die Einstellungen des Identitätsanbieters in den Commerce headquarters aktualisieren

Als Nächstes müssen Sie die Einstellungen des Identitätsanbieters in den Commerce headquarters aktualisieren.

1. Öffnen Sie im Commerce headquarters die Seite **Freigegebene Commerce-Parameter**.
1. Wählen Sie auf der Registerkarte **Identitätsanbieter** im Abschnitt **Identitätsanbieter** die Zeile aus, in der das Feld **Typ** auf **Azure Active Directory** und das Feld **Aussteller** auf Ihren Azure AD-Mandanten festgelegt sind. Diese Einstellung gibt an, dass Sie mit untergeordneten Rastern arbeiten, die die Daten enthalten, die sich auf den Identitätsanbieter beziehen, der Ihrem Azure AD-Mandanten entspricht.
1. Wählen Sie im Bereich **Vertrauende Seiten** **Hinzufügen** aus, um eine Zeile hinzuzufügen.
1. Stellen Sie die folgenden Felder ein:

    - **ClientId**: Geben Sie den Wert der **Anwendungs-(Client-)ID** der benutzerdefinierten CPOS-App ein, die Sie im Bereich [Eine benutzerdefinierte CPOS-App in Azure AD einrichten](#set-up-a-custom-cpos-app-in-azure-ad) erstellt haben.
    - **Typ**: Wählen Sie **Öffentlich** aus.
    - **UserType**: Wählen Sie **Arbeitskraft** aus.

1. Wählen Sie die Reihe, die Sie hinzugefügt haben. Der Abschnitt **Serverressourcen-IDs** unter dem Abschnitt **Vertrauende Seiten** zeigt die Retail-Server-App-IDs an, auf die von der App zugegriffen werden kann, die Sie im Raster **Vertrauende Seiten** ausgewählt haben.
1. Wählen Sie im Bereich **Serverressourcen-IDs** **Hinzufügen** aus, um eine Zeile hinzuzufügen.
1. Geben Sie im Feld **Server-Ressourcen-ID** den **Anwendungs-ID-URI**-Wert der benutzerdefinierten Retail-Server-App ein, die Sie im Bereich [Eine benutzerdefinierte Retail-Server-App in Azure AD einrichten](#set-up-a-custom-retail-server-app-in-azure-ad) erstellt haben.

    > [!IMPORTANT]
    > Bei allen Feldern, die in den vorherigen Schritten erwähnt wurden, muss die Groß-/Kleinschreibung beachtet werden. Die eingegebenen Werte müssen exakt mit den im Azure AD Admin Center konfigurierten Werten übereinstimmen.

1. Gehen Sie zu **IT für Einzelhandel und Handel \> Vertriebsplan** und führen Sie den Einzelvorgang **1110** (**globale Konfiguration**) aus.

Sie können jetzt CPOS-Geräte aktivieren, indem Sie Ihre eigene Azure AD-App verwenden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Aktivierung von Point-of-Sale-(POS-)Geräten](dev-itpro/retail-device-activation.md)

[Aktivierungskonten verwalten und Geräte überprüfen](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
