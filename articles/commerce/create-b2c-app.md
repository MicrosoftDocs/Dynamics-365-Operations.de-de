---
title: B2C-Anwendung erstellen
description: In diesem Artikel wird beschrieben, wie Sie eine Business-to-Consumer (B2C)-Anwendung im Microsoft Azure Portal erstellen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785247"
---
# <a name="create-a-b2c-application"></a>B2C-Anwendung erstellen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie eine Business-to-Consumer (B2C)-Anwendung im Microsoft Azure Portal erstellen.

Sobald Ihr B2C-Mandant erstellt wurde, erstellen Sie eine B2C-Anwendung innerhalb Ihres neuen Azure Active Directory (Azure AD) BSC-Mandanten, um mit den Commerce-Aktionen zu interagieren.

Führen Sie folgende Schritte aus, um eine B2C-Anwendung zu erstellen.

1. Wählen Sie im Azure-Portal zu **App-Registrierungen** und wählen Sie dann **Neue Registrierung** aus.
1. Geben Sie unter **Name** den Namen für diese Azure AD B2C-Anwendung ein.
1. Wählen Sie unter **Unterstützte Kontotypen** **Konten in einem beliebigen Identitätsanbieter oder Organisationsverzeichnis (zur Authentifizierung von Benutzern mit Benutzerflows)** aus.
1. Geben Sie bei **URI umleiten** Ihre dedizierten Antwort-URLs als Typ **Web** ein. Unter [Antwort-URLs](#reply-urls) unten finden Sie Informationen zu Antwort-URLs und deren Formatierung. Eine Umleitungs-URI/Antwort-URL muss eingegeben werden, um Umleitungen von Azure AD B2C zurück zu Ihrer Site zu aktivieren, wenn sich ein Benutzer authentifiziert. Die Antwort-URL kann während des Registrierungsvorgangs oder später durch Auswahl des Links **Umleitungs-URI hinzufügen** im **Überblick**-Menü in der B2C-Anwendung im Abschnitt **Überblick** hinzugefügt werden.
1. Wählen Sie unter **Berechtigungen** **Administratoreinwilligung zu OpenID- und Offline-Zugriffsberechtigungen erteilen**.
1. Wählen Sie **Registrieren** aus.
1. Wählen Sie die neu erstellte Anwendung und navigieren Sie zum Menü **Authentifizierung**. 
1. Wenn eine Antwort-URL eingegeben wurde, wählen Sie unter **Implizite Berechtigungen und Hybridflows** sowohl die Option **Zugriffstoken** als auch **ID-Token** aus, um sie für die Anwendung zu aktivieren, und wählen Sie dann **Speichern** aus. Wenn bei der Registrierung keine Antwort-URL eingegeben wurde, kann diese auch auf dieser Seite durch Auswahl von **Eine Plattform hinzufügen** hinzugefügt werden, indem Sie **Web** auswählen und dann den Umleitungs-URI der Anwendung eingeben. Der **Implizite Zuschüsse und hybride Ströme**-Abschnitt wird dann verfügbar sein, um die Optionen **Zugriffstoken** und **ID-Token** auszuwählen.
1. Gehen Sie zum Menü **Überblick** des Azure-Portals und kopieren Sie die **Anwendungs-ID (Client-ID)**. Notieren Sie diese ID für spätere Einrichtungsschritte (später als **Client-GUID** bezeichnet).

Weitere Informationen zu App-Registrierungen in Azure AD B2C finden Sie unter [Neue Benutzeroberfläche für App-Registrierungen in Azure Active Directory B2C](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Antwort-URLs

Antwort-URLs sind wichtig, da sie eine Zulassungsliste der zurückgegebenen Domains bereitstellen, wenn Ihre Website Azure AD B2C zur Authentifizierung eines Benutzers aufruft. Dies ermöglicht die Rückkehr des authentifizierten Benutzers zur Domäne, bei der er sich anmeldet (Ihre Website-Domäne). 

Im Feld **Antwort-URL** auf dem Bildschirm **Azure AD B2C – Anwendungen \> Neue Anwendung** müssen Sie separate Zeilen für Ihre Site-Domain und (sobald Ihre Umgebung bereitgestellt ist) die von Commerce generierte URL hinzufügen. Diese URLs müssen immer ein gültiges URL-Format verwenden und dürfen nur Basis-URLs sein (keine nachgestellten Schrägstriche oder Pfade). Die Zeichenfolge ``/_msdyn365/authresp`` muss dann wie in den folgenden Beispielen an die Basis-URLs angehängt werden.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Die Domäne sollte vollständig mit der E-Commerce-Domäne übereinstimmen. Wenn Sie mehrere Domänen haben, müssen Sie diese URL für jede Domäne hinzufügen.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Nächste Schritte

Um mit dem Einrichten eines B2C-Mandanten in Commerce fortzufahren, fahren Sie fort mit [Benutzerflow-Richtlinien erstellen](create-user-flow-policies.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md)

[Erstellen oder Verknüpfen eines vorhandenen Azure AD B2C-Mandanten im Azure-Portal](create-link-aad-b2c-tenant.md)

[Benutzerflussrichtlinien erstellen](create-user-flow-policies.md)

[Anbieter sozialer Identität hinzufügen (optional)](add-social-identity-providers.md)

[Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen](update-hq-aad-b2c-info.md)

[Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Weitere B2C Informationen](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
