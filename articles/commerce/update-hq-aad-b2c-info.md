---
title: Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen
description: In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 Commerce headquarters mit neuen Azure Active Directory (Azure AD) Business-to-Consumer (B2C)-Informationen aktualisieren.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785330"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 Commerce headquarters mit neuen Azure Active Directory (Azure AD) Business-to-Consumer (B2C)-Informationen aktualisieren.

Sobald die Azure AD B2C-Bereitstellungsschritte oben abgeschlossen ist, muss die Azure AD B2C-Anwendung muss in Ihrer Dynamics 365 Commerce Umgebung registriert werden.

Um den Hauptsitz mit den neuen Azure AD B2C Informationen zu aktualisieren, befolgen Sie diese Schritte.

1. Gehen Sie im Handel zu **Gemeinsame Commerce-Parameter** und wählen Sie **Identitätsanbieter** im linken Menü.
1. Unter **Identitätsanbieter** gehe Sie wie folgt vor:
    1. Im Kästchen **Aussteller** geben Sie im Feld die Zeichenfolge des Identitätsanbieters ein. Informationen, wie Sie Ihre Ausstellerzeichenfolge finden, finden Sie unten unter [Ausstellerzeichenfolge für die Einrichtung der Zentralverwaltung abrufen](#obtain-issuer-string-for-headquarters-setup).
    1. Geben Sie im Feld **Name** einen Namen für den Herausgeberdatensatz ein.
    1. Im Feld **Art** geben Sie **Azure AD B2C (id_Token)** ein.
1. Unter **Ausgewählte Parteien** gehen Sie bei ausgewähltem oben genannten Element des B2C-Identitätsanbieters wie folgt vor:
    1. Geben Sie im Feld **ClientID** Ihre B2C-Anwendungs-ID ein, die Sie in der **Anwendungs-ID** Feld der Eigenschaftenseite Ihrer B2C-Anwendung finden.
    1. In dem Kästchen **Art** geben Sie **öffentlich** ein.
    1. In dem Kästchen **Benutzertyp** geben Sie **benutzerdefiniert** ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Suchen Sie im Commerce-Suchfeld nach **Verteilungsplan**
1. Im linken Navigationsmenü auf der Seite **Verteilungspläne** wählen Sie **1110 globale Konfiguration**.
1. Wählen Sie im Aktivitätsbereich **Jetzt ausführen**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Ausstellerzeichenfolge für die Einrichtung der Zentralverwaltung abrufen

Führen Sie die folgenden Schritte aus, um die Ausstellerzeichenfolge Ihres Identitätsanbieters zu erhalten.

1. Gehen Sie auf der Seite Azure AD B2C des Azure-Portals zu Ihrem Benutzerflow **Registrieren und Anmelden**.
1. Wählen Sie **Seitenlayouts** im linken Navigationsmenü, dann unter **Layoutname** **Einheitliche Registrierungs- oder Anmeldeseite** und schließlich **Benutzerflow ausführen**.
1. Stellen Sie sicher, dass Ihre Anwendung auf Ihre oben erstellte Azure AD B2C-Anwendung eingestellt ist, und wählen Sie dann den Benutzerflow aus, der unter der Kopfzeile **Benutzerflow ausführen** erscheint, der ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>`` enthält. (Wählen Sie nicht **Benutzerflow ausführen**.) Eine neue Registerkarte wird geöffnet, die Metadaten für die Richtlinie zum Erfassen der Ausstellerzeichenfolge anzeigt.
1. Kopieren Sie auf der Metadatenseite, die in Ihrer Browserregisterkarte angezeigt wird, die Ausstellerzeichenfolge des Identitätsanbieters (den Wert für **Aussteller**, der mit „https://“ beginnt und mit „/v2.0/“ endet), die dem folgenden Beispiel ähnlich sieht.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**ODER**: Führen Sie die folgenden Schritte aus, um dieselbe Metadaten-URL manuell zu erstellen.

1. Erstellen Sie mit Ihrem B2C-Mandanten und Ihrer Richtlinie eine URL für Metadatenadressen im folgenden Format: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Beispiel: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Geben Sie die URL der Metadatenadresse in eine Adressleiste des Browsers ein.
1. Kopieren Sie in den Metadaten die Aussteller-URL des Identitätsanbieters (den Wert für **Aussteller**).
    - Beispiel: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Nächste Schritte

Um mit dem Einrichten eines B2C-Mandanten in Commerce fortzufahren, fahren Sie fort mit [Konfigurieren Sie Ihren B2C-Mandanten im Commerce-Site-Builder](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md)

[Erstellen oder Verknüpfen eines vorhandenen Azure AD B2C-Mandanten im Azure-Portal](create-link-aad-b2c-tenant.md)

[B2C Anwendungen erstellen](create-b2c-app.md)

[Benutzerflussrichtlinien erstellen](create-user-flow-policies.md)

[Anbieter sozialer Identität hinzufügen (optional)](add-social-identity-providers.md)

[Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Weitere B2C Informationen](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
