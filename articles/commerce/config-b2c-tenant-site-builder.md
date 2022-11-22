---
title: Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder
description: In diesem Artikel wird beschrieben, wie Sie Ihren Business-to-Consumer (B2C) Mandanten in Microsoft Dynamics 365 Commerce Site Builder konfigurieren.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785258"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Ihren Business-to-Consumer (B2C) Mandanten in Microsoft Dynamics 365 Commerce Site Builder konfigurieren.

Einmal eingerichtet für Ihr Azure AD ist Ihr B2C-Mandant abgeschlossen. Sie müssen den B2C-Mandanten im Commerce Site Builder konfigurieren. Zu den Konfigurationsschritten gehören das Sammeln von B2C-Anwendungsinformationen aus dem Azure-Portal, das Eingeben dieser B2C-Anwendungsinformationen in den Site Builder und das Zuordnen der B2C-Anwendung zu Ihrer Site und Ihrem Kanal.

### <a name="collect-the-required-application-information"></a>Sammeln Sie die erforderlichen Anwendungsinformationen

Führen Sie die folgenden Schritte aus, um die erforderlichen Anwendungsinformationen zu erfassen.

1. Gehen Sie im Azure-Portal zu **Home \> Azure AD B2C - App-Registrierungen**.
1. Wählen Sie Ihre Anwendung aus und wählen Sie dann im linken Navigationsbereich **Übersicht**, um die Anwendungsdetails zu erhalten.
1. Über den Verweis **Anwendungs-(Client-)ID** erfassen Sie die Anwendungs-ID der B2C-Anwendung, die in Ihrem B2C-Mandanten erstellt wurde. Dies wird später als **Client-GUID** im Site Builder eingegeben.
1. Wählen Sie **Weiterleitungs-URIs** und sammeln Sie die für Ihre Site angezeigte Antwort-URL (die bei der Einrichtung eingegebene Antwort-URL).
1. Gehen Sie zu **Home \> Azure AD B2C - User Flows**, und sammeln Sie die vollständigen Namen der einzelnen Richtlinien für User Flows.

Die folgende Abbildung zeigt ein Beispiel für die **Azure AD B2C - App Registrierungen** Übersichtsseite.

![Azure AD B2C - Übersichtsseite für App-Registrierungen mit hervorgehobener Anwendungs- (Client-) ID](./media/ClientGUID_Application_AzurePortal.png)

Das folgende Bild zeigt ein Beispiel für Benutzerflussrichtlinien auf der Seite **Azure AD B2C – Benutzerströme (Richtlinien)**.

![Sammeln Sie die Namen jedes B2C-Richtlinienflusses.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Geben Sie Ihre Azure AD B2C-Mandantenanwendungsinformationen in Commerce ein

Sie müssen Details der eingeben Azure AD B2C-Mandant in Commerce Site Builder einbinden, bevor der B2C-Mandant Ihren Sites zugeordnet wird.

Führen Sie die folgenden Schritte aus, um Commerce Ihre Azure AD B2C-Mandantenanwendungsinformationen hinzuzufügen.

1. Melden Sie sich als Administrator bei Commerce Site Builder für Ihre Umgebung an.
1. Wählen Sie im linken Navigationsbereich **Mandant-Einstellungen** aus, um den Bereich zu erweitern.
1. Wählen Sie unter **Mandanteneinstellungen** die Option **Einrichtung der Site-Authentifizierung** aus. 
1. Wählen Sie im Hauptfenster neben **Site-Authentifizierungsprofile** die Option **Verwalten** aus. (Wenn Ihr Mandant in der Liste der Site-Authentifizierungsprofile angezeigt wird, wurde er bereits von einem Administrator hinzugefügt. Stellen Sie sicher, dass die Elemente in Schritt 6 unten mit Ihrer gewünschten B2C-Einrichtung übereinstimmen. Ein neues Profil kann auch mit ähnlichen Azure AD B2C-Mandanten oder -Anwendungen erstellt werden, um geringfügige Unterschiede zu berücksichtigen, z. B. unterschiedliche Benutzerrichtlinien-IDs).
1. Wählen Sie **Site-Authentifizierungsprofil** aus.
1. Geben Sie die folgenden erforderlichen Elemente in das angezeigte Formular ein und verwenden Sie dabei die Werte Ihres B2C-Mandanten und Ihrer Anwendung. Nicht erforderliche Felder (solche ohne Sternchen) können leer gelassen werden.

    - **Anwendungsname**: Der Name für Ihre B2C-Anwendung, z. B. Fabrikam B2C.
    - **Name des Mandanten**: Der Name Ihres B2C-Mandanten (verwenden Sie beispielsweise „fabrikam“, wenn die Domain für den B2C-Mandanten als „fabrikam.onmicrosoft.com“ angezeigt wird). 
    - **Kennwor vergessen Richtlinien-ID**: Die ID der Benutzerflussrichtlinie für vergessenes Kennwort, z.B. B2C_1_PasswordReset.
    - **Anmeld-/Registierungsrichtlinien-ID**: Die ID der Registrierungs- und Anmeldebenutzer-Flow-Richtlinie, z. B. „B2C_1_signup_signin“.
    - **Client-GUID**: Die B2C-Anwendungs-ID, zum Beispiel „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6“.
    - **Profilrichtlinien-ID bearbeiten** : Die Benutzerflussrichtlinien-ID für die Profilbearbeitung, z. B. B2C_1A_ProfileEdit.

1. Wählen Sie **OK**. Sie sollten nun den Namen Ihrer B2C-Anwendung in der Liste sehen.
1. Wählen Sie **Speichern** aus, um die Änderungen zu speichern.

Das optionale Feld **Benutzerdefinierte Domäne für Anmeldung** sollte nur verwendet werden, wenn Sie eine benutzerdefinierte Domäne für den Azure AD B2C-Mandanten einrichten. Weitere Details und Überlegungen zur Verwendung des Felds **Benutzerdefinierte Domäne für Anmeldung** finden Sie unter [Zusätzliche B2C-Informationen](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Verknüpfen Sie die B2C-Anwendung mit Ihrer Site und Ihrem Kanal

> [!WARNING]
> - Wenn Ihre Site bereits einer B2C-Anwendung zugeordnet ist, werden durch den Wechsel zu einer anderen B2C-Anwendung die aktuellen Referenzen entfernt, die für Benutzer eingerichtet wurden, die bereits in dieser Umgebung angemeldet sind. Bei einer Änderung stehen den Benutzern keine Anmeldeinformationen zur Verfügung, die der aktuell zugewiesenen B2C-Anwendung zugeordnet sind. 
> - Aktualisieren Sie die B2C-Anwendung nur, wenn Sie die B2C-Anwendung des Kanals zum ersten Mal einrichten oder wenn Sie beabsichtigen, Benutzer mit der neuen B2C-Anwendung erneut mit neuen Anmeldeinformationen für diesen Kanal anzumelden. Seien Sie vorsichtig, wenn Sie Kanäle der B2C-Anwendungen zuordnen, und benennen Sie Anwendungen eindeutig. Wenn in den folgenden Schritten kein Kanal einer B2C-Anwendung zugeordnet ist, werden Benutzer, die sich bei diesem Kanal für Ihre Site anmelden, in die B2C-Anwendung eingegeben, die als **Standard** in **Mandanteneinstellungen \> B2C-Einstellungen** der Liste B2C-Anwendungen angezeigt wird.

Um die B2C-Anwendung Ihrer Site und Ihrem Kanal zuzuweisen, folgen Sie diesen Schritten.

1. Navigieren Sie im Commerce Site Builder zu Ihrer Site.
1. Wählen Sie im linken Navigationsbereich **Site-Einstellungen** aus, um den Bereich zu erweitern.
1. Unten **Seiteneinstellungen**, wählen Sie **Kanäle**.
1. Im Hauptfenster unter **Kanäle** wählen Sie Ihren Kanal.
1. Wählen Sie im Bereich Channel-Eigenschaften auf der rechten Seite den Namen Ihrer B2C-Anwendung aus dem Dropdown-Menü **B2C-Anwendung auswählen**.
1. Wählen Sie **Schließen** und dann **Speichern und veröffentlichen**.

## <a name="next-steps"></a>Nächste Schritte

Um mit dem Einrichten eines B2C-Mandanten in Commerce fortzufahren, fahren Sie fort mit [Zusätzliche B2C-Informationen](additional-b2c-info.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md)

[Erstellen oder Verknüpfen eines vorhandenen Azure AD B2C-Mandanten im Azure-Portal](create-link-aad-b2c-tenant.md)

[B2C Anwendungen erstellen](create-b2c-app.md)

[Benutzerflussrichtlinien erstellen](create-user-flow-policies.md)

[Anbieter sozialer Identität hinzufügen (optional)](add-social-identity-providers.md)

[Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen](update-hq-aad-b2c-info.md)

[Weitere B2C Informationen](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
