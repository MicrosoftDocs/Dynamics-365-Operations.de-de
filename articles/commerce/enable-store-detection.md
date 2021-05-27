---
title: Standortbasierte Shop-Erkennung aktivieren
description: In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e26c3130914ebef5a63b79c477d7d5846fd5b71
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027599"
---
# <a name="enable-location-based-store-detection"></a>Standortbasierte Shop-Erkennung aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.

Mit ortsbasierter Shoperkennung im Handel können Sie Standortsinhalt für Debitoren auf Grundlage des Lagerplatzes angeben. Wenn ortsbasierte Shoperkennung aktiviert ist, wird der Handelsrendering-Service die Länder/-Regionsinformationen von die IP-Adresse des Webbrowsers des Debitors verwenden, um den Debitor an die beste geografische Standortskonfiguration zu verweisen, die verfügbar ist.

## <a name="privacy-notice"></a>Datenschutzhinweis

Wenn Sie die ortsbasierte Shoperkennungsfunktion aktivieren, werden Informationen im Browser des Debitors für ein Microsoft-Lagerplatz-Service gesendet. Diese Angabe wird dann verwendet, um den Debitoreninhalt bereitzustellen, der für die Adresse des Debitors relevant ist. Beide Informationen, die vom im Browser des Debitors und von den standortbasierten Informationen übermittelt wird, die an den Debitor zurückgegeben wird, sind abhängig von Informationen zum Datenschutz und Cookiekompatibilitätspolitischen Richtlinien.

## <a name="turn-on-location-based-store-detection"></a>Standortbasierte Shop-Erkennung aktivieren

Um ortsbasierte Shoperkennung im Handel zu aktivieren, gehen Sie folgendermaßen vor.

1. Im Erstellungstool gehen Sie zu Ihrer Site.
1. Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.
1. Wählen Sie **Site-Einstellungen**.
1. Hier können Sie die Option **Aktivieren basierend auf Shoperkennung** auf **Aktiviert** festlegen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Domänennamen konfigurieren](configure-your-domain-name.md)

[Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

[E-Commerce-Website erstellen](create-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
