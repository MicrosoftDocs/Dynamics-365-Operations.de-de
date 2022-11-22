---
title: Anbieter sozialer Identität hinzufügen
description: In diesem Artikel wird beschrieben, wie Sie soziale Identitätsanbieter im Microsoft Azure Portal hinzufügen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785239"
---
# <a name="add-social-identity-providers"></a>Anbieter sozialer Identität hinzufügen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie soziale Identitätsanbieter im Microsoft Azure Portal hinzufügen.

Mit Anbietern sozialer Identität können Benutzer ihre sozialen Konten zur Authentifizierung verwenden. Das Hinzufügen der Authentifizierung des Anbieters sozialer Identität ist in Dynamics 365 Commerce optional. 

Wenn die Anbieterauthentifizierung der sozialen Identität nicht hinzugefügt wird, ist die Standardeinstellung Azure Active Directory (Azure AD) B2C-Profile das Hauptprofil für Ihre Benutzerbasis. Benutzer wählen ihren eigenen Benutzernamen (ihre bevorzugte E-Mail-Adresse) und legen ein Passwort fest. Azure AD B2C authentifiziert Benutzer direkt. 

Wenn die Authentifizierung eines Anbieters für soziale Identität hinzugefügt wird und ein Benutzer einen der angebotenen Anbieter für soziale Identität auswählt, wird weiterhin eine Entität in der Liste Azure AD B2C-Mandant erstellt. Azure AD B2C authentifiziert dann die Anmeldeinformationen des Benutzers beim Anbieter der sozialen Identität.

> [!NOTE]
> Durch die Anmeldung des Identitätsanbieters wird ein Datensatz im B2C-Mandanten erstellt, jedoch in einem anderen Format als bei lokalen Konten, da die Referenz des externen Anbieters für soziale Identität zur Authentifizierung aufgerufen wird. Der Benutzer kann bei allen Anbietern sozialer Identitäten dieselbe E-Mail-Adresse verwenden. Dies bedeutet, dass der für die Authentifizierung verwendete E-Mail-Benutzername möglicherweise nicht für den Mandanten eindeutig ist. Azure AD B2C erzwingt nur, dass Benutzer auf lokalen B2C-Konten eine eindeutige E-Mail-Adresse haben.

Bevor Sie einen Anbieter für soziale Identität zur Authentifizierung hinzufügen können, müssen Sie zum Portal des Identitätsanbieters gehen und eine Anwendung für Identitätsanbieter einrichten, wie in der Anleitung Azure AD B2C-Dokumentation beschrieben. Eine Liste der Links zur Dokumentation finden Sie unten.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Einzelmieter)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-Konto](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Fügen Sie einen Anbieter für soziale Identität hinzu und richten Sie ihn ein

> [!NOTE]
> Das Hinzufügen von Anbietern sozialer Identitäten ist ein optionaler Schritt beim Einrichten eines Business-to-Consumer (B2C)-Mandanten in Microsoft Dynamics 365 Commerce.

Führen Sie die folgenden Schritte aus, um einen Anbieter für soziale Identität hinzuzufügen und einzurichten.  

1. Navigieren Sie im Azure-Portal zu **Identitätsanbieter**.
1. Wählen Sie **Hinzufügen** aus. Der Bildschirm **Identitätsanbieter hinzufügen** wird angezeigt.
1. Unter **Name** geben Sie den Namen ein, der den Benutzern auf Ihrem Anmeldebildschirm angezeigt werden soll.
1. Unter **Typ des Identitätsanbieters** wählen Sie einen Identitätsanbieter aus der Liste aus.
1. Wählen Sie **OK**.
1. Wählen Sie **Richten Sie diesen Identitätsanbieter ein**, um auf den Bildschirm **Richten Sie den Anbieter für soziale Identität ein** zuzugreifen.
1. Unter **Kunden ID** geben Sie die Client-ID ein, die Sie im Setup der Identitätsanbieteranwendung erhalten haben.
1. Unter **Geheimer Clientschlüssel** geben Sie den geheimen Clientschlüssel ein, den Sie im Setup der Identitätsanbieteranwendung erhalten haben.
1. Benutzer-Flow für Anmelde-/Registierungsrichtlinien hinzufügen:
1. Gehe zu **Azure AD B2C – Benutzerflüsse (Richtlinien) \> {Ihre Anmeldungsrichtlinie} \> Identitätsanbieter**.
1. Wählen Sie jeden Identitätsanbieter aus, den Sie für Ihr Konto eingerichtet haben, um die Benutzer-Flow-Richtlinie zum Anmelden/Registrieren anzuhängen. Um diese Flows zu testen, wählen Sie **Führen Sie den Benutzerfluss aus** für jeden Identitätsanbieter. Auf einer neuen Registerkarte wird die Anmeldeseite mit dem Auswahlfeld für den neuen Identitätsanbieter angezeigt.

Das folgende Bild zeigt Beispiele für die Bildschirme **Identitätsanbieter hinzufügen** und **Richten Sie den Anbieter für soziale Identität ein** in Azure AD B2C.

![Hinzufügen eines Anbieters für soziale Identität zu Ihrer Anwendung.](./media/B2CImage_14.png)

Das folgende Bild zeigt ein Beispiel für die Auswahl von Identitätsanbietern auf der Seite Azure AD B2C **Identitätsanbieter**.

![Wählen Sie jeden Anbieter für soziale Identität aus, der für Ihre Richtlinie aktiviert werden soll.](./media/B2CImage_16.png)

Das folgende Bild zeigt ein Beispiel für einen Standard-Anmeldebildschirm mit einer Anmeldeschaltfläche für Anbieter sozialer Identität.

> [!NOTE]
> Wenn Sie die in Commerce erstellten benutzerdefinierten Seiten für Ihre Benutzerflows verwenden, müssen die Schaltflächen für soziale Identitätsanbieter mithilfe der Erweiterbarkeitsfeatures der Commerce-Modulbibliothek hinzugefügt werden. Wenn Sie Ihre Anwendungen bei einem bestimmten sozialen Identitätsanbieter einrichten, kann in einigen Fällen bei URL- oder Konfigurationszeichenfolgen zwischen Groß- und Kleinschreibung unterschieden werden. Weitere Informationen finden Sie in den Verbindungsanweisungen Ihres sozialen Identitätsanbieters.
 
![Beispiel für einen Standard-Anmeldebildschirm mit angezeigter Anmeldeschaltfläche des sozialen Netzwerks als Identitätsanbieter.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Nächste Schritte

Um mit dem Einrichten eines B2C-Mandanten in Commerce fortzufahren, fahren Sie mit [Aktualisieren Sie Commerce headquarters mit den neuen Azure AD B2C-Informationen](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md)

[Erstellen oder Verknüpfen eines vorhandenen Azure AD B2C-Mandanten im Azure-Portal](create-link-aad-b2c-tenant.md)

[B2C Anwendungen erstellen](create-b2c-app.md)

[Benutzerflussrichtlinien erstellen](create-user-flow-policies.md)

[Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen](update-hq-aad-b2c-info.md)

[Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Weitere B2C Informationen](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
