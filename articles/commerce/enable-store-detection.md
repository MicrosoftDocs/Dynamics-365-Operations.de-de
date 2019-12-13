---
title: Standortbasierte Shop-Erkennung aktivieren
description: In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697611"
---
# <a name="enable-location-based-store-detection"></a>Standortbasierte Shop-Erkennung aktivieren

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.

## <a name="overview"></a>Übersicht

Mit ortsbasierter Shoperkennung im Handel können Sie Standortsinhalt für Debitoren auf Grundlage des Lagerplatzes angeben. Wenn ortsbasierte Shoperkennung aktiviert ist, wird der Handelsrendering-Service die Länder/-Regionsinformationen von die IP-Adresse des Webbrowsers des Debitors verwenden, um den Debitor an die beste geografische Standortskonfiguration zu verweisen, die verfügbar ist.

## <a name="privacy-notice"></a>Datenschutzhinweis

Wenn Sie die ortsbasierte Shoperkennungsfunktion aktivieren, werden Informationen im Browser des Debitors für ein Microsoft-Lagerplatz-Service gesendet. Diese Angabe wird dann verwendet, um den Debitoreninhalt bereitzustellen, der für die elektronische Adresse relevant ist. Beide Informationen, die vom im Browser des Debitors und von den standortbasierten Informationen übermittelt wird, die an den Debitor zurückgegeben wird, sind abhängig von Informationen zum Datenschutz und Cookiekompatibilitätspolitischen Richtlinien.

## <a name="turn-on-location-based-store-detection"></a>Standortbasierte Shop-Erkennung aktivieren

Um ortsbasierte Shoperkennung im Handel zu aktivieren, gehen Sie folgendermaßen vor.

1. Im Erstellungstool gehen Sie zu Ihrer Site.
1. Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.
1. Wählen Sie **Site-Einstellungen**.
1. Hier können Sie die Option **Aktivieren basierend auf Shoperkennung** auf **Aktiviert** festlegen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Onlineshop – Überblick](online-store-overview.md)

[Erstellen einer E-Commerce-Webseite](create-ecommerce-site.md)

[Bereitstellen einer neuen E-Commerce-Webseite](deploy-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Konfigurieren Ihres Domänennamens](configure-your-domain-name.md)

[Unterstützung für ein Content Delivery Network (CDN) hinzufügen](add-cdn-support.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)
