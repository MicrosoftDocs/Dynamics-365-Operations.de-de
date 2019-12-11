---
title: Erstellen einer E-Commerce-Webseite
description: In diesem Thema werden die Aufgaben beschrieben, die bei der Erstellung einer neuen E-Commerce-Site in Dynamics 365 Commerce zugeordnet werden.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697128"
---
# <a name="create-an-e-commerce-site"></a>Erstellen einer E-Commerce-Webseite

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema werden die Aufgaben beschrieben, die bei der Erstellung einer neuen E-Commerce-Site in Dynamics 365 Commerce zugeordnet werden.

## <a name="overview"></a>Übersicht

Um mit der Entwicklung der E-Commerce-Site zu beginnen, müssen Sie eine neue Site in der Siteerstellungsumgebung einrichten. Bevor Sie eine neue Site erstellen können, muss mindestens ein Onlineshop in Dynamics 365 Retail erstellt werden. 

## <a name="set-up-your-site"></a>Site einrichten

Um Ihre Site einzurichten, gehen Sie folgendermaßen vor.

1. Im Microsoft Lifecycle Services (LCS) wählen Sie den Link für die Siteerstellungsumgebung aus. 
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

[Onlineshop – Überblick](online-store-overview.md)

[Bereitstellen einer neuen E-Commerce-Webseite](deploy-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Konfigurieren Ihres Domänennamens](configure-your-domain-name.md)

[Unterstützung für ein Content Delivery Network (CDN) hinzufügen](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Übersicht über die Erstellung von Startseiten](authoring-home-overview.md)

[Neue Seite hinzufügen](add-new-page.md)
