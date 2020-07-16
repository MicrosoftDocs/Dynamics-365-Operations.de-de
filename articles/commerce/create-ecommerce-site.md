---
title: Erstellen einer E-Commerce-Webseite
description: In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Site in Dynamics 365 Commerce Site Builder erforderlich sind.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ea3517a4f2b84db8a87a97d2f644bb4436f8693f
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533435"
---
# <a name="create-an-e-commerce-site"></a>Erstellen einer E-Commerce-Webseite

[!include [banner](includes/banner.md)]

In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Site in Dynamics 365 Commerce Site Builder erforderlich sind.

Wenn Sie die E-Commerce-Funktionen lizenzieren, wird Site Builder eine Starter-Site bereitgestellt, die Sie als Grundlage für Ihre eigene Site verwenden können. Wenn Sie jedoch von Grund auf neu beginnen oder eine zweite Site einrichten möchten, müssen Sie eine neue Site in der Site-Erstellungsumgebung einrichten. 

## <a name="set-up-your-site"></a>Site einrichten

Um Ihre Site einzurichten, gehen Sie folgendermaßen vor.

1. Öffnen Sie die Site Builder-Umgebung. Sie finden einen Link zum Site Builder in Microsoft Lifecycle Services (LCS) auf der Seite mit den Umgebungsfunktionen für Commerce.
1. Auf der Startseite für die Siteerstellungsumgebung wählen Sie **Neue Site** aus.
1. Geben Sie im Dialogfeld **Neue Site** die folgenden Informationen ein.

| Feld                               | Beschreibung |
|-------------------------------------|-------------|
| Sitename                           | Geben Sie den angezeigten Namen ein, der für Ihre Site in der Siteerstellungsumgebung verwendet werden soll. Dieser Name ist nur in der Erstellungsumgebung sichtbar und wird nicht Debitoren angezeigt werden. |
| Site-Administrator-Sicherheitsgruppe | Geben Sie die Microsoft Azure Active Directory (Azure AD) Sicherheitsgruppe ein, die Benutzer verwaltet, die die Siteadministratorrolle für diese Site haben. |
| Standardkanal (Nummer der Organisationseinheit) | Wählen Sie den Onlineshop aus, aus, für den diese Site als Internet-Schaufenster dient. Wenn Sie möchten, dass Ihre E-Commerce-Webseite mehrere Onlineshops unterstützen soll, müssen Sie die Shops Ihren Webseiten zuordnen unter **Site-Einstellungen**, nachdem die Site eingerichtet wurde. |
| Standardsprache                            | Geben Sie die Standardsprache für diesen Onlineshop und Markt an. Ein Onlineshop kann mehrere Sprachen unterstützen. Wenn Sie mehrere Sprachen für diesen Onlineshop oder einen anderen Onlineshop unterstützen möchten, können Sie diesen so konfigurieren unter **Siteeinstellungen**, nachdem die Site eingerichtet wurde.  |
| Domäne                              | Wählen Sie den Domänennamen, der als Domäne für diesen Onlineshop dienen soll. Wenn Sie keine Domänen in LCS konfiguriert haben, können Sie dieses Feld leer lassen. Nachdem die Domäne in LCS konfiguriert ist, müssen Sie sie in Ihrem Onlineshop unter **Siteeinstellungen** hinzufügen.  |
| Pfad                              | Wenn Ihr Site mehr als eine Sprache für einen angegebenen Domänennamen unterstützt, verwenden Sie das Pfadfeld, um eine eindeutige Standort URL für diese Domäne und Sprachenkombination zu erstellen. Sollte die gewünschte Sprache, die Sie im Feld **Standardsprache** angegeben haben, die einzige Sprache sein, die Sie für diese Domäne unterstützen oder die Standardsprache nach der Lokalisierung der Site in weitere Sprachen sein wird, wird empfohlen, dass Sie das Feld leer gelassen. |


Nachdem Ihre Site erstellt wurde, können Sie prüfen, dass sie Ihrem Onlineshop zugeordnet ist, indem Sie die Registerkarte **Produkte** auswählen. Sie sollten das Sortiment von Produkten sehen, das dem Onlineshop zugewiesen wurde. Sie können das Drop-Down-Menü im oberen linken Rand auch verwenden, um auf die zugewiesenen Produkte nach Kategorie zuzugreifen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Konfigurieren Ihres Domänennamens](configure-your-domain-name.md)

[Bereitstellen einer neuen E-Commerce-Webseite](deploy-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Weiterleitungen in großen Mengen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)
