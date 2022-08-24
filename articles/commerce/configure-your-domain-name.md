---
title: Domänennamen konfigurieren
description: In diesem Artikel wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.
author: josaw1
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 298ce84008e60cc82a494320b6a41f35338508c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278623"
---
# <a name="configure-your-domain-name"></a>Domänennamen konfigurieren


[!include [banner](includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren. 

## <a name="add-domains-during-e-commerce-initialization"></a>Domänen während der E-Commerce-Initialisierung hinzufügen

Um Ihrer Dynamics 365 Commerce-E-Commerce-Umgebung Domänen zuzuordnen, initialisieren Sie E-Commerce wie beschrieben in [Einen neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md). Während der Initialisierung werden Sie gebeten, Informationen bereitzustellen, die zur Bereitstellung Ihrer E-Commerce-Umgebung verwendet werden. Im Feld **Unterstützte Hostnamen** wählen Sie alle Domänen hinzufügen, die Sie mit dieser Umgebung verwenden möchten. Mehrere Domänen sollten mit Trennzeichen getrennt werden. Auf diese Weise werden die Domänen in allen erforderlichen E-Commerce-Komponenten konfiguriert, und sie sind für die Verwendung bereit, wenn Sie von Ihrem Content Delivery Network (CDN) oder Webserver Datenverkehr umschalten und mit ihm auf die E-Commerce-Front-Ends zeigen.

## <a name="add-domains-after-e-commerce-initialization"></a>Domänen nach der E-Commerce-Initialisierung hinzufügen

Um nach der E-Commerce-Initialisierung neue Domänen zu Ihrer E-Commerce-Umgebung zuzuordnen, müssen Sie eine Dienstanforderung übermitteln.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

[E-Commerce-Website erstellen](create-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
