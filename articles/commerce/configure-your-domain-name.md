---
title: Konfigurieren Ihres Domänennamens
description: In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.
author: psimolin
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ac1b0c8baaddd6ca62cc49657fff364df21c14f2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517120"
---
# <a name="configure-your-domain-name"></a>Konfigurieren Ihres Domänennamens


[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren. 

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
