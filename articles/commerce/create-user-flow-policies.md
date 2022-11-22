---
title: Benutzerflussrichtlinien erstellen
description: In diesem Artikel wird beschrieben, wie Sie Benutzerflussrichtlinien im Microsoft Azure Portal erstellen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785257"
---
# <a name="create-user-flow-policies"></a>Benutzerflussrichtlinien erstellen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Benutzerflussrichtlinien im Microsoft Azure Portal erstellen.

Benutzerflüsse sind die Richtlinien die Azure Active Directory (Azure AD) Business-to-Consumer (B2C) verwendet, um eine sichere Anmeldung bereitzustellen, sich anzumelden, das Profil zu bearbeiten und für die Benutzererfahrung für vergessene Kennwörter. Dynamics 365 Commerce verwendet diesen Fluss, um die Richtlinienaktionen für die Interaktion mit dem Azure AD B2C-Mandant auszuführen. Wenn ein Benutzer mit diesen Richtlinien interagiert, werden sie an den Azure AD B2C-Mandant weitergeleitet, um die Aktionen auszuführen.

Azure AD B2C bietet drei grundlegende Benutzerflusstypen:
- Registrieren Sie sich und melden Sie sich an
- Profilbearbeitung
- Kennwort zurücksetzen

Sie können die Standardbenutzerflüsse verwenden, die von Azure AD bereitgestellt werden, die eine Seite anzeigen, die von Azure AD B2C gehostete wird. Alternativ können Sie eine HTML-Seite erstellen, um das Erscheinungsbild dieser Benutzerflusserfahrungen zu steuern. 

Um die Benutzerrichtlinienseiten mit in Dynamics 365 Commerce erstellten Seiten anzupassen, gehen Sie zu [Richten Sie benutzerdefinierte Seiten für Benutzeranmeldungen ein](custom-pages-user-logins.md). Weitere Informationen finden Sie unter [Passen Sie die Benutzeroberfläche für Benutzererfahrungen an in Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Erstellen Sie eine Registrierungs- und Anmeldebenutzer-Flow-Richtlinie

Um eine Registrierungs- und Anmeldebenutzer-Flow-Richtlinie zu erstellen, führen Sie die folgenden Schritte aus.

1. Wählen Sie im Azure-Portal die Option **Benutzerflüsse (Richtlinien)** im linken Navigationsbereich.
1. Auf der Seite **Azure AD B2C – Benutzerfluss (Richtlinien)** wählen Sie **Neuer Benutzerfluss**.
1. Wählen Sie die **Registrieren und Anmelden**-Richtlinie und dann die Version **Empfohlen** aus.
1. Geben Sie unter **Name** einen Richtliniennamen ein. Dieser Name wird anschließend mit einem vom Portal zugewiesenen Präfix angezeigt (z. B. B2C_1_).
1. Unter **Identitätsanbieter** wählen Sie im **Lokale Konten**-Abschnitt **E-Mail anmelden** aus. Die E-Mail-Authentifizierung wird in den gängigsten Szenarien für Commerce verwendet. Wenn Sie auch die Authentifizierung des Anbieters sozialer Identität verwenden, können Sie diese zu diesem Zeitpunkt ebenfalls auswählen.
1. Unter **Multifaktor-Authentifizierung** wählen Sie die für Ihr Unternehmen geeignete Auswahl. 
1. Unter **Benutzerattribute und Ansprüche** wählen Sie Optionen aus, um Attribute zu sammeln oder Ansprüche zurückzugeben. Wählen Sie **Mehr anzeigen...** aus, um die vollständige Liste der Attribute und Anspruchsoptionen zu erhalten. Für den Handel sind die folgenden Standardoptionen erforderlich:

    | **Attribute sammeln** | **Rückgabeanspruch** |
    | ---------------------- | ----------------- |
    | E-Mail-Adresse          | E-Mail-Adressen   |
    | Vorname             | Vorname        |
    |                        | Identitätsanbieter |
    | Nachname                | Nachname           |
    |                        | Objekt-ID des Benutzers  |

1. Wählen Sie **Erstellen** aus.

Das folgende Bild ist ein Beispiel für den Azure AD B2C-Registrierungs- und Anmeldebenutzer-Flow.

![Konfigurieren der Richtlinieneinstellungen für Registrieren und Anmelden.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Erstellen Sie eine Benutzerflussrichtlinie zur Profilbearbeitung

Um eine Profilbearbeitungs-Benutzerflussrichtlinie zu erstellen, führen Sie die folgenden Schritte aus.

1. Wählen Sie im Azure-Portal die Option **Benutzerflüsse (Richtlinien)** im linken Navigationsbereich.
1. Auf der Seite **Azure AD B2C – Benutzerfluss (Richtlinien)** wählen Sie **Neuer Benutzerfluss**.
1. Wählen Sie **Profilbearbeitung** und dann die Version **Empfohlen** aus.
1. Unter **Name** geben Sie den Benutzerfluss für die Profilbearbeitung ein. Dieser Name wird anschließend mit einem vom Portal zugewiesenen Präfix angezeigt (z. B. B2C_1_).
1. Unter **Identitätsanbieter** wählen Sie im **Lokale Konten**-Abschnitt **E-Mail-Anmeldung** aus.
1. Wählen Sie unter **Benutzerattribute** eines der folgenden Kontrollkästchen aus:
    
    | **Attribute sammeln** | **Rückgabeanspruch** |
    | ---------------------- | ----------------- |
    |                        | E-Mail-Adressen   |
    | Vorname             | Vorname        |
    |                        | Identitätsanbieter |
    | Nachname                | Nachname           |
    |                        | Objekt-ID des Benutzers  |
    
1. Wählen Sie **Erstellen** aus.

Das folgende Bild zeigt ein Beispiel für den Azure AD B2C Profilbearbeitungs-Benutzerfluss.

![Beispiel des Benutzerflows zu Azure AD B2C-Profilbearbeitung](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Erstellen Sie eine Benutzerflussrichtlinie zur Kennwortzurücksetzung

Um eine Kennwortzurücksetzungs-Benutzerflussrichtlinie zu erstellen, führen Sie die folgenden Schritte aus.

1. Wählen Sie im Azure-Portal die Option **Benutzerflüsse (Richtlinien)** im linken Navigationsbereich.
1. Auf der Seite **Azure AD B2C – Benutzerfluss (Richtlinien)** wählen Sie **Neuer Benutzerfluss**.
1. Wählen Sie **Kennwortzurücksetzung** und dann die Version **Empfohlen** aus.
1. Unter **Name** geben Sie einen Namen für den Benutzerfluss zum Zurücksetzen des Kennworts ein.
1. Im Abschnitt **Identitätsanbieter** wählen Sie **Kennwort zurücksetzen mithilfe der E-Mail-Adresse** aus.
1. Wählen Sie **Erstellen** aus.
1. Wählen Sie unter **Anwendungsanspruch** eines der folgenden Kontrollkästchen aus:
    - **E-Mail-Adressen**
    - **Vorname**
    - **Nachname**
    - **Objekt-ID des Benutzers**
1. Wählen Sie **Erstellen** aus.

Das folgende Bild zeigt, wo **Kennwort mit E-Mail-Adresse zurücksetzen** im Azure AD Benutzerfluss zum Zurücksetzen des B2C-Passworts eingestellt werden muss.

![Legen Sie in der Richtlinie zum Zurücksetzen des Kennworts Kennwort mit E-Mail-Adresse zurücksetzen fest](./media/B2CImage_13.png)

## <a name="next-steps"></a>Nächste Schritte

Um mit dem Einrichten eines B2C-Mandanten in Commerce fortzufahren, fahren Sie fort mit [Anbieter sozialer Identität hinzufügen](add-social-identity-providers.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md)

[Erstellen oder Verknüpfen eines vorhandenen Azure AD B2C-Mandanten im Azure-Portal](create-link-aad-b2c-tenant.md)

[B2C Anwendungen erstellen](create-b2c-app.md)

[Anbieter sozialer Identität hinzufügen (optional)](add-social-identity-providers.md)

[Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen](update-hq-aad-b2c-info.md)

[Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Weitere B2C Informationen](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
