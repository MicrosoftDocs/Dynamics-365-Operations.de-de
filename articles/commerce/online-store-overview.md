---
title: E-Commerce-Website-Übersicht
description: Dieses Thema bietet eine Übersicht über die Unterstützung für E-Commerce-Websites in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b7050f954116213f700e4a2b3326547f4d070674
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353011"
---
# <a name="e-commerce-site-overview"></a>E-Commerce-Site – Übersicht

[!include [banner](includes/banner.md)]

Dieses Thema bietet eine Übersicht über die Unterstützung für E-Commerce-Websites in Microsoft Dynamics 365 Commerce. Es enthält Informationen darüber, wie E-Commerce-Online-Shops in Dynamics 365 Commerce initialisiert und verwaltet werden. Es enthält auch Links zu weiteren Informationen zu Onlineshops und Informationen zum Einrichten und Konfigurieren einer E-Commerce-Website. Obwohl dieses Thema viele der Grundlagen abdeckt, behandelt es nicht alles, was zum Einrichten einer E-Commerce-Produktionswebsite erforderlich ist. Weiterführende Themen finden Sie in der Dynamics 365 Commerce-Dokumentation.

## <a name="online-store-channel"></a>Onlineshopkanal

Bevor Sie eine Ihre Website in Dynamics 365 Commerce erstellen können, muss mindestens ein Onlineshopkanal eingerichtet sein. Weitere Informationen finden Sie unter [Online-Kanal einrichten](channel-setup-online.md). 

In Dynamics 365 Commerce können Sie einen Onlineshopkanal verwenden, um die Produkte, Preise, Sprachen, Zahlungsmethoden, Lieferarten, Erfüllungszentren und andere Aspekte der Onlinefunktionalität festzulegen, die Ihren Kunden zur Verfügung stehen soll.

Nur ein Onlineshopkanal muss eingerichten werden, bevor Sie mit Dynamics 365 Commerce loslegen können. Jedoch kann eine einzelne E-Commerce-Website die Online-Umgebung für mehrere Onlineshops bereitstellen. Wenn zum Beispiel mehrere Online-Shops eingerichtet sind, um unterschiedliche geografische Regionen zu unterstützen, kann ein einzelner Satz von E-Commerce-Seiten verwendet werden, um die von jedem Shop definierten einzigartigen Umgebungen und Funktionalitäten bereitzustellen. Weitere Informationen zum Konfigurieren einer Site für die Unterstützung mehrerer Onlineshops finden Sie unter [Verknüpfen Sie eine Online-Site mit einem Kanal](associate-site-online-store.md).

Nachdem ein Online-Shop eingerichtet wurde, kann er der Dynamics 365 Commerce-Site zugeordnet werden, die als Ihre Online-Storefront dient. Weitere Informationen zu Onlineshops und deren Einrichtung finden Sie unter [Richten Sie Online-Shops ein](/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Neuen E-Commerce-Mandanten bereitstellen

Während der Initialisierung einer E-Commerce-Website werden Sie zur Eingabe eines Domänennamens aufgefordert. Weitere Informationen zu Domänen in Commerce finden Sie unter [Ihren Domänennamen konfigurieren](configure-your-domain-name.md) und [Domänen in Dynamics 365 Commerce](domains-commerce.md). Um einen neuen E-Commerce-Mandanten mithilfe von [Microsoft Dynamics Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) bereitzustellen, folgen Sie den Schritten in [Einen neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md). Nachdem Ihr E-Commerce-Mandant in LCS eingerichtet wurde, wird ein Link zum Commerce-Website-Generator bereitgestellt. Sie können dann den Commerce-Website-Generator verwenden, um Ihre E-Commerce-Websites zu initialisieren und zu konfigurieren.

## <a name="initialize-your-e-commerce-site"></a>Ihre E-Commerce-Website initialisieren

Wenn Sie den Commerce-Website-Generator von LCS aus starten, wird die Seite **Websites** angezeigt. Diese Seite enthält zwei vorkonfigurierte Websites **Standard** und **fabrikam**, wie im Beispiel in der folgenden Abbildung gezeigt.

![Seite „Websites“ im Commerce-Website-Generator.](media/e-commerce-site-01.png)

Wenn Sie eine dieser Websites auswählen, werden Sie aufgefordert, einen Domänennamen, einen standardmäßigen Online-Shop-Kanal, eine unterstützte Sprache für den ausgewählten Kanal und einen Pfad auszuwählen. Wenn nur ein Kanal verwendet wird, können Sie den Pfad leer lassen. Weitere Online-Shop-Kanäle oder -Sprachen können später im Commerce-Website-Generator konfiguriert werden. Jeder zusätzliche Kanal oder jede zusätzliche Sprache erfordert einen eindeutigen Pfad. Sie haben beispielsweise zwei Online-Kanäle, die einer einzigen Website zugeordnet sind, und der Domänenname für die Website lautet `www.fabrikam.com`. In diesem Fall kann der Pfad für einen Kanal der Standardwert sein, der keinen Pfad hat (`https://www.fabrikam.com`), und der zweite Kanal kann auf einen neuen Pfad festgelegt werden, wie z. B. **site2**, der dann die folgende URL `https://www.fabrikam.com/site2` hat. Die folgende Abbildung zeigt ein Beispiel für ein Dialogfeld zur Website-Initialisierung im Commerce-Website-Generator.

![Dialogfeld „Website-Initialisierung“ im Commerce-Website-Generator.](media/e-commerce-site-02.png)

Die Seite **Websites** enthält auch eine Schaltfläche **Neue Website**. Das Dialogfeld, das angezeigt wird, wenn Sie diese Schaltfläche auswählen, ähnelt dem Dialogfeld für die Website-Initialisierung, wird jedoch zum Erstellen einer neuen Website verwendet. Neue Websites sind leer. Sie enthalten nicht dieselben Standardvorlagen, Fragmente, Seiten und Bilder, die mit den Websites **Standard** und **fabrikam** bereitgestellt werden. Bei Bedarf können Sie jedoch ein Supportticket öffnen, um das Hinzufügen einer Kopie des Standardinhalts zu einer neuen leeren Website anzufordern. Weitere Informationen finden Sie unter [Eine E-Commerce-Website erstellen](create-ecommerce-site.md).

Nachdem eine neue Website initialisiert wurde, wird die **Start**-Seite des Commerce-Website-Generators angezeigt. Diese Seite enthält Links zu allgemeinen Aktionen und Anleitungsinhalten, wie im Beispiel in der folgenden Abbildung gezeigt.

![Links auf der Startseite im Commerce-Website-Generator.](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Online-Shop-Kanäle ändern oder Online-Shop-Kanäle zu einer E-Commerce-Website hinzufügen

Nachdem eine E-Commerce-Website erstellt wurde, können Sie den Kanal ändern, dem sie zugeordnet ist, indem Sie den Schritten in [Eine E-Commerce-Website einem Online-Kanal zuordnen](associate-site-online-store.md) folgen. Das Beispiel in der folgenden Abbildung zeigt, wie eine Kanalvorgangseinheitsnummer (OUN) auf der Seite **Kanäle** geändert werden kann (**Website-Einstellungen \> Kanäle**). Nachdem Sie eine Änderung vorgenommen haben, vergessen Sie nicht, **Speicher und veröffentlichen** auszuwählen. Auf diese Weise stellen Sie sicher, dass die Änderung veröffentlicht wird.

![Seite „Kanäle“ im Commerce-Website-Generator.](media/e-commerce-site-04.png)

Sie können neue Kanäle hinzufügen, indem Sie auswählen **Kanal hinzufügen** auswählen. Um einem Kanal neue Sprachen hinzuzufügen, wählen Sie den Kanal aus und wählen Sie dann **Gebietsschema hinzufügen** im angezeigten Kanaldialogfeld aus. Bevor Gebietsschemas im Dialogfeld angezeigt werden können, müssen sie für den Online-Shop-Kanal in der Commerce-Zentralverwaltung vorkonfiguriert sein.

![Dialogfeld „Kanal“ im Commerce-Website-Generator.](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Azure B2C-Mandant einrichten

Dynamics 365 Commerce verwendet Azure Active Directory (Azure AD) business-to-consumer (Unternehmen-zu-Verbraucher; B2C), um Benutzeranmeldeinformationen und Authentifizierungs-Flows zu unterstützen. Informationen zum Einrichten Ihres Azure B2C-Mandanten finden Sie unter [B2C-Mandant in Commerce einrichten](set-up-b2c-tenant.md), [Benutzerdefinierte Seiten für Benutzeranmeldungen einrichten](custom-pages-user-logins.md) und [Mehrere B2C-Mandanten in einer Commerce-Umgebung einrichten](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Übersicht über die standardmäßigen Website-Seiten

Die Websites **Standard** und **fabrikam** enthalten vorkonfigurierte Vorlagen, Fragmente und Seiten, die Ihnen den Einstieg erleichtern. Weitere Informationen finden Sie in folgenden Themen:

- [Übersicht zur Startseite](quick-tour-home-page.md)
- [Übersicht zur Produktdetailseite](quick-tour-pdp.md)
- [Übersicht zu Einkaufswagen und Seiten für den Bezahlvorgang](quick-tour-cart-checkout.md)
- [Übersicht zu Kontoverwaltungsseiten](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Website-Einstellungen verwalten

Informationen zum Verwalten Ihrer Website-Einstellungen finden Sie in den folgenden Themen:

- [E-Commerce Benutzer und Rollen verwalten](manage-ecommerce-users-roles.md)
- [Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site](/search-engine-optimization-considerations.md)
- [Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) verwalten](manage-csp.md)
- [Sitedesign auswählen](select-site-theme.md)

## <a name="manage-site-content"></a>Website-Inhalte verwalten

Informationen zum Verwalten von Website-Inhalten finden Sie in den folgenden Themen:

- [Seitenmodellglossar](page-elements-overview.md)
- [Dokumentstatus und -lebenszyklus](document-states-overview.md)
- [Vorlagen und Layout](templates-layouts-overview.md)
- [Arbeiten mit Fragmenten](work-with-fragments.md)
- [Arbeiten mit Modulen](work-with-modules.md)
- [Überblick über die Verwaltung digitaler Anlagen](dam-overview.md)
- [Informationen zur Modulbibliothek](starter-kit-overview.md)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[E-Commerce-Website erstellen](create-ecommerce-site.md)

[Eine neue E-Commerce-Website bereitstellen](deploy-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Domänennamen konfigurieren](configure-your-domain-name.md)

[Unterstützung für ein Content Delivery Network (CDN) hinzufügen](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]