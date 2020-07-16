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
ms.openlocfilehash: afc8c7fffbded82be32357bdeb30546afc8b0957
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533297"
---
# <a name="configure-your-domain-name"></a>Konfigurieren Ihres Domänennamens


[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren. 

## <a name="add-domains-during-e-commerce-initialization"></a>Domänen während der E-Commerce-Initialisierung hinzufügen.

Wenn Sie Domänen Ihrer E-Commerce-Umgebung hinzufügen, initialisieren Sie E-Commerce wie beschrieben in [Eine neue E-Commerce-Webseite bereitstellen](deploy-ecommerce-site.md). Während der Initialisierung werden Sie gebeten, Informationen bereitzustellen, die zur Bereitstellung der E-Commerce-Umgebung verwendet werden. Im Feld **Unterstützte Hostnamen** wählen Sie alle Domänen hinzufügen, die Sie mit dieser Umgebung verwenden möchten. Mehrere Domänen sollten mit Trennzeichen getrennt werden. Auf diese Weise werden die Domänen in alle erforderlichen E-Commerce-Komponenten konfiguriert, und sie sind für die Verwendung bereit, wenn Sie vom Datenverkehr aus Ihrem Content-Vertriebsnetz (CDN) oder vom Webserver wechseln und ihn in den E-Commerce-Front-End anzeigen.

## <a name="add-domains-after-e-commerce-initialization"></a>Domänen hinzufügen,nach der E-Commerce-Initialisierung

Wenn Sie neue Domänen mit der E-Commerce-Umgebung nach der E-Commerce-Initialisierung zuordnen möchten, müssen Sie eine Serviceanforderung senden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bereitstellen einer neuen E-Commerce-Webseite](deploy-ecommerce-site.md)

[Erstellen einer E-Commerce-Webseite](create-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Verwalten von robots.txt-Dateien](manage-robots-txt-files.md)

[URL-Weiterleitungen in großen Mengen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)
