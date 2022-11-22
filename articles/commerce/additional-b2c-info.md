---
title: Weitere B2C Informationen
description: Dieser Artikel enthält zusätzliche Informationen dazu, wie Sie Ihren Business-to-Consumer (B2C)-Mandanten in Microsoft Dynamics 365 Commerce einrichten.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785238"
---
# <a name="additional-b2c-information"></a>Weitere B2C Informationen

[!include [banner](includes/banner.md)]

Dieser Artikel enthält zusätzliche Informationen dazu, wie Sie Ihren Business-to-Consumer (B2C)-Mandanten in Microsoft Dynamics 365 Commerce einrichten.

### <a name="customer-migration"></a>Kundenmigration

Wenn Sie in Betracht ziehen, Kundendatensätze von einer früheren Plattform für Identitätsanbieter zu migrieren, arbeiten Sie bitte mit dem Dynamics 365 Commerce Team, um Ihre Kundenmigrationsanforderungen zu überprüfen.

Für weitere Azure AD B2C-Dokumentation zur Kundenmigration siehe [Migrieren Sie Benutzer zu Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Benutzerdefinierte Richtlinien

Weitere Informationen zum Anpassen finden Sie unter Azure AD B2C-Interaktionen und Richtlinienflüsse, die über das hinausgehen, was B2C-Standardrichtlinien bieten, siehe [Benutzerdefinierte Richtlinien in Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundäradministrator

Ein optionales sekundäres Administratorkonto kann im Abschnitt **Benutzer** Ihres B2C-Mandanten hinzugefügt werden. Dies kann ein direktes Konto oder ein allgemeines Konto sein. Wenn Sie ein Konto für mehrere Teamressourcen freigeben müssen, kann auch ein gemeinsames Konto erstellt werden. Aufgrund der Empfindlichkeit der gespeicherten Daten in Azure AD B2C, sollte ein gemeinsames Konto gemäß den Sicherheitspraktiken Ihres Unternehmens genau überwacht werden.

### <a name="set-up-a-custom-sign-in-domain"></a>Benutzerdefinierte Anmeldedomäne einrichten

Mit Azure AD B2C können Sie eine benutzerdefinierte Anmeldedomäne für den Azure AD B2C-Mandanten einrichten. Anweisungen finden Sie unter [Benutzerdefinierte Domänen für Azure Active Directory B2C aktivieren](/azure/active-directory-b2c/custom-domain). 

Wenn Sie eine benutzerdefinierte Anmeldedomäne verwenden, muss die Domäne in den Commerce-Website-Generator eingegeben werden.

Um eine benutzerdefinierte Anmeldedomäne im Website-Generator einzugeben, folgen Sie diesen Schritten.

1. Wählen Sie oben rechts im Website-Generator die Site-Umschaltfunktion und dann **Sites verwalten** aus.
1. Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen \> Einrichtung der Site-Authentifizierung** aus, um den Bereich zu erweitern.
1. Wählen Sie im Abschnitt **Site-Authentifizierungsprofile** die Option **Verwalten** aus.
1. Wählen Sie im Flyout-Menü auf der rechten Seite die Schaltfläche **Bearbeiten** (Stiftsymbol) neben dem Site-Authentifizierungsprofil aus, für das Sie eine benutzerdefinierte Domäne eingeben möchten.
1. Geben Sie im Dialogfeld **Site-Authentifizierungsprofil bearbeiten** unter **Benutzerdefinierte Domäne für Anmeldung** Ihre benutzerdefinierte Anmeldedomäne ein (z. B. „login.fabrikam.com“).

> [!WARNING]
> Wenn Sie auf eine benutzerdefinierte Domäne für den Azure AD B2C-Mandanten aktualisieren, wirkt sich die Änderung auf die Ausstellerdetails des Mandanten für das generierte Token aus. Die Ausstellerdetails enthalten dann die benutzerdefinierte Domäne anstelle der von Azure AD B2C bereitgestellten Standarddomäne. Eine andere **Aussteller**-Konfiguration in Commerce headquarters (**Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Freigegebene Handelsparameter \> Identitätsanbieter**) ändert die Interaktion des Systems mit Site-Benutzern und erstellt möglicherweise einen neuen Kundendatensatz, wenn sich ein Benutzer beim neuen Aussteller authentifiziert. Alle Änderungen an benutzerdefinierten Domänen sollten gründlich getestet werden, bevor Sie in einer Azure AD B2C-Live-Umgebung zu der benutzerdefinierten Domäne wechseln.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md)

[Erstellen oder Verknüpfen eines vorhandenen Azure AD B2C-Mandanten im Azure-Portal](create-link-aad-b2c-tenant.md)

[B2C Anwendungen erstellen](create-b2c-app.md)

[Benutzerflussrichtlinien erstellen](create-user-flow-policies.md)

[Anbieter sozialer Identität hinzufügen (optional)](add-social-identity-providers.md)

[Aktualisieren Sie die Commerce headquarters mit den neuen Azure AD B2C-Informationen](update-hq-aad-b2c-info.md)

[Konfigurieren Sie Ihren B2C-Mandanten im Commerce Site Builder](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
