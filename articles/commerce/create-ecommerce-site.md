---
title: E-Commerce-Website erstellen
description: In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Website im Dynamics 365 Commerce-Website-Generator erforderlich sind.
author: bicyclingfool
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 01f22772fd8c8984a2f92c516972d6659325a18c
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090768"
---
# <a name="create-an-e-commerce-site"></a>E-Commerce-Website erstellen

[!include [banner](includes/banner.md)]

In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Website im Dynamics 365 Commerce-Website-Generator erforderlich sind.

Wenn Sie die Dynamics 365 Commerce-Funktionen lizenzieren, wird der Website-Generator mit einer Starter Site bereitgestellt, die Sie als Grundlage für Ihre eigene Website verwenden können. Wenn Sie jedoch von Grund auf neu beginnen oder eine zweite Site einrichten möchten, müssen Sie eine neue Site in der Site-Erstellungsumgebung einrichten. 

## <a name="set-up-your-site"></a>Site einrichten

Um Ihre Site einzurichten, gehen Sie folgendermaßen vor.

1. Öffnen Sie die Site Builder-Umgebung. Sie finden einen Link zum Site Builder in Microsoft Lifecycle Services (LCS) auf der Seite mit den Umgebungsfunktionen für Commerce.
1. Auf der Startseite für die Siteerstellungsumgebung wählen Sie **Neue Site** aus.
1. Geben Sie im Dialogfeld **Neue Site** die folgenden Informationen ein.

| Feld                               | Beschreibung |
|-------------------------------------|-------------|
| Sitename                           | Geben Sie den angezeigten Namen ein, der für Ihre Site in der Siteerstellungsumgebung verwendet werden soll. Dieser Name ist nur in der Erstellungsumgebung sichtbar und wird nicht Debitoren angezeigt werden. |
| Site-Administrator-Sicherheitsgruppe | Geben Sie die Microsoft Azure Active Directory (Azure AD) Sicherheitsgruppe ein, die Benutzer verwaltet, die die Siteadministratorrolle für diese Site haben. |
| Standardkanal (Nummer der Organisationseinheit) | Wählen Sie den Onlineshop aus, aus, für den diese Site als Internet-Schaufenster dient. Wenn Sie möchten, dass Ihre E-Commerce-Webseite mehrere Onlineshops unterstützen soll, müssen Sie die Shops Ihrer Website in **Website-Einstellungen** zuordnen, nachdem die Website eingerichtet wurde. |
| Standardsprache                            | Geben Sie die Standardsprache für diesen Onlineshop und Markt an. Ein Onlineshop kann mehrere Sprachen unterstützen. Wenn Sie mehrere Sprachen für diesen Onlineshop oder einen anderen Onlineshop unterstützen möchten, können Sie diesen so konfigurieren unter **Siteeinstellungen**, nachdem die Site eingerichtet wurde.  |
| Domäne                              | Wählen Sie den Domänennamen, der als Domäne für diesen Onlineshop dienen soll. Wenn Sie keine Domänen in LCS konfiguriert haben, können Sie dieses Feld leer lassen. Nachdem die Domäne in LCS konfiguriert ist, müssen Sie sie in Ihrem Onlineshop unter **Siteeinstellungen** hinzufügen.  |
| Pfad                              | Wenn Ihr Site mehr als eine Sprache für einen angegebenen Domänennamen unterstützt, verwenden Sie das Pfadfeld, um eine eindeutige Standort URL für diese Domäne und Sprachenkombination zu erstellen. Sollte die gewünschte Sprache, die Sie im Feld **Standardsprache** angegeben haben, die einzige Sprache sein, die Sie für diese Domäne unterstützen oder die Standardsprache nach der Lokalisierung der Site in weitere Sprachen sein wird, wird empfohlen, dass Sie das Feld leer gelassen. |

Nachdem Ihre Site erstellt wurde, können Sie prüfen, dass sie Ihrem Onlineshop zugeordnet ist, indem Sie die Registerkarte **Produkte** auswählen. Sie sollten das Sortiment von Produkten sehen, das dem Onlineshop zugewiesen wurde. Sie können das Drop-Down-Menü im oberen linken Rand auch verwenden, um auf die zugewiesenen Produkte nach Kategorie zuzugreifen.

## <a name="rename-your-site"></a>Ihre Website umbenennen

Führen Sie diese Schritte aus, um Ihre Website in Site Builder umzubenennen.

1. Um die Standortlistenansicht zu öffnen, wählen Sie **Standortumschalter** in der oberen rechten Ecke und dann **Standorte verwalten** . 
1. Aktivieren Sie das Kontrollkästchen neben der Seite, die Sie umbenennen möchten, und wählen Sie dann **Umbenennen** in der Befehlsleiste.
1. Geben Sie im Dialogfeld **Neuer Standortname** den neuen Standortnamen ein und wählen Sie dann **OK**. Die Site-Liste wird aktualisiert und zeigt den neuen Namen der Site an.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Domänennamen konfigurieren](configure-your-domain-name.md)

[Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
