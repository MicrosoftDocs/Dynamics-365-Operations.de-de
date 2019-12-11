---
title: Konfigurieren Ihres Domänennamens
description: In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770457"
---
# <a name="configure-your-domain-name"></a>Konfigurieren Ihres Domänennamens

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren. 

## <a name="add-domains-during-e-commerce-initialization"></a>Domänen während der E-Commerce-Initialisierung hinzufügen.

Wenn Sie Domänen Ihrer E-Commerce-Umgebung hinzufügen, initialisieren Sie E-Commerce wie beschrieben in [Eine neue E-Commerce-Webseite bereitstellen](deploy-ecommerce-site.md). Während der Initialisierung werden Sie gebeten, Informationen bereitzustellen, die zur Bereitstellung der E-Commerce-Umgebung verwendet werden. Im Feld **Unterstützte Hostnamen** wählen Sie alle Domänen hinzufügen, die Sie mit dieser Umgebung verwenden möchten. Mehrere Domänen sollten mit Trennzeichen getrennt werden. Auf diese Weise werden die Domänen in alle erforderlichen E-Commerce-Komponenten konfiguriert, und sie sind für die Verwendung bereit, wenn Sie vom Datenverkehr aus Ihrem Content-Vertriebsnetz (CDN) oder vom Webserver wechseln und ihn in den E-Commerce-Front-End anzeigen.

## <a name="add-domains-after-e-commerce-initialization"></a>Domänen hinzufügen,nach der E-Commerce-Initialisierung

Wenn Sie neue Domänen mit der E-Commerce-Umgebung nach der E-Commerce-Initialisierung zuordnen möchten, müssen Sie eine Serviceanforderung senden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Onlineshop – Überblick](online-store-overview.md)

[Erstellen einer E-Commerce-Webseite](create-ecommerce-site.md)

[Bereitstellen einer neuen E-Commerce-Webseite](deploy-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Unterstützung für ein Content Delivery Network (CDN) hinzufügen](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)
