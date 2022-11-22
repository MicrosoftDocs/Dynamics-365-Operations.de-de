---
title: Erstellen oder Verknüpfen eines vorhandenen Azure AD AAD B2C-Mandanten im Azure-Portal
description: In diesem Artikel wird beschrieben, wie Sie einen vorhandenen Azure Active Directory (Azure AD) Business-to-Consumer (B2C)-Mandant im Microsoft Azure Portal erstellen oder mit ihr verknüpfen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785248"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Erstellen oder Verknüpfen eines vorhandenen Azure AD AAD B2C-Mandanten im Azure-Portal

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie einen Azure Active Directory (Azure AD) Business-to-Consumer (B2C)-Mandant im Microsoft Azure Portal erstellen oder mit ihr verknüpfen. Weitere Informationen finden Sie unter [Tutorial: Erstellen eines Azure Active Directory-B2C-Mandanten](/azure/active-directory-b2c/tutorial-create-tenant).

Zum Erstellen oder Verknüpfen mit einem bestehenden Azure AD B2C-Mandant im Azure-Portal befolgen Sie diese Schritte.

1. Melden Sie sich beim [Azure-Portal](https://portal.azure.com/) an.
1. Wählen Sie im Azure-Portalmenü die Option aus **Erstellen Sie eine Ressource**. Stellen Sie sicher, dass Sie das Abonnement und das Verzeichnis verwenden, die mit Ihrer Commerce-Umgebung verbunden werden.

    ![Erstellen Sie eine Ressource in Azure-Portal.](./media/B2CImage_1.png)

1. Gehe zu **Identität \> Azure Active Directory B2C**.
1. Einmal auf der Seite **Erstellen Sie einen neuen B2C-Mandanten oder einen Link zu einem vorhandenen Mandanten** verwenden Sie auf der folgenden Seite eine der folgenden Optionen, die den Anforderungen Ihres Unternehmens am besten entspricht:

    - **Erstellen Sie einen neuen Azure AD B2C Mandanten**: Verwenden Sie diese Option, um einen neuen Azure AD B2C-Mandanten zu erstellen.
        1. Wählen Sie **Neuen Azure AD B2C Mandant erstellen**.
        1. Unter **Name der Organisation** geben Sie den Namen der Organisation ein.
        1. Unter **Anfänglicher Domainname** geben Sie den ursprünglichen Domainnamen ein.
        1. Für **Land oder Region** wählen Sie das Land oder die Region aus.
        1. Wählen Sie **Erstellen**, um den Mieter zu erstellen.

     ![Einen neuen Azure AD-Mandanten erstellen.](./media/B2CImage_2.png)

     - **Um einen vorhandenen Azure AD B2C-Mandant für das Azure-Abonnement** zu verknüpfen: Verwenden Sie diese Option, wenn Sie bereits einen Azure AD B2C-Mandant haben, zu dem Sie einen Link erstellen möchten.
        1. Wählen Sie **Einen vorhandenen Azure AD B2C-Mandant für das Azure-Abonnement** verknüpfen.
        1. Für **Azure AD B2C Mandant** wählen Sie den entsprechenden B2C-Mandanten aus. Wenn im Auswahlfeld die Meldung Keine berechtigten B2C-Mandanten gefunden angezeigt wird, haben Sie keinen vorhandenen berechtigten B2C-Mandanten und müssen einen neuen erstellen.
        1. Für **Ressourcengruppe** wählen Sie **Neu erstellen**. Geben Sie einen **Namen** für die Ressourcengruppe ein, die den Mandanten enthalten soll, und wählen Sie die Option **Standort der Ressourcengruppe** und dann **Erstellen**.

    ![Verbinden Sie einen Azure AD B2C-Mandant für das Azure-Abonnement.](./media/B2CImage_3.png)

1. Sobald das Neue Azure AD B2C-Verzeichnis erstellt wird (dies kann einige Momente dauern), wird im Dashboard ein Link zum neuen Verzeichnis angezeigt. Über diesen Link gelangen Sie zur Seite Willkommen bei Azure Active Directory B2C.

    ![Link zum neuen Azure AD-Verzeichnis.](./media/B2CImage_4.png)

> [!NOTE]
> Wenn Sie mehrere Abonnements in Ihrem Azure-Konto haben oder den B2C-Mandanten ohne Verknüpfung mit einem aktiven Abonnement eingerichtet haben, wird eine Anzeige **Fehlerbehebung** Sie darauf hinweisen, den Mandant mit einem Abonnement zu verknüpfen. Wählen Sie die Meldung zur Fehlerbehebung aus und befolgen Sie die Anweisungen, um das Abonnementproblem zu beheben.

Das folgende Bild zeigt ein Beispiel für eine Anzeige Azure AD B2C **Fehlerbehebung**.

![Warnung: Das angezeigte Verzeichnis hat kein aktives Abonnement.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Nächste Schritte

Um mit dem Einrichten eines B2C-Mandanten in Commerce fortzufahren, fahren Sie fort mit [Die B2C-Anwendung erstellen](create-b2c-app.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md)

[B2C Anwendungen erstellen](create-b2c-app.md)

[Benutzerflussrichtlinien erstellen](create-user-flow-policies.md)

[Anbieter sozialer Identität hinzufügen (optional)](add-social-identity-providers.md)

[Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen](update-hq-aad-b2c-info.md)

[Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Weitere B2C Informationen](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
