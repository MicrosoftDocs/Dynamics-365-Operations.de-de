---
title: Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site
description: In diesem Artikel werden Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Website von der Entwicklung bis zur Produktion behandelt.
author: josaw1
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 77bbc04e849cf1cdeb7ce19226f43354635ddbe0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275618"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site


[!include [banner](includes/banner.md)]

In diesem Artikel werden Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Website von der Entwicklung bis zur Produktion behandelt.

## <a name="a-site-that-is-under-development"></a>Eine Seite, die sich in der Entwicklung befindet

Um sicherzustellen, dass Suchmaschinen eine in der Entwicklung befindliche Website nicht indizieren, sollten alle Seiten der Website die Meta-Tags **noindex** und **nofollow** haben. Eine gute Vorgehensweise besteht darin, ein Fragment auf der Grundlage des [MetaTags-Moduls](metatags-module.md) zu erstellen, das den folgenden Meta-Tag-Eintrag enthält, und sicherzustellen, dass das Fragment dem HTML-Abschnitt \<head\> aller auf Ihrer Website verwendeten Vorlagen hinzugefügt wird.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Langsame Einführung einer Website

Bei einer „langsamen Einführung“ wird eine Website einem begrenzten Publikum oder Markt zur Verfügung gestellt, bevor die vollständige Einführung erfolgt. Wenn Sie einen Soft-Launch Ihrer Website durchführen, sollten Sie die **noindex**-Meta-Tags an Ort und Stelle lassen. Auf diese Weise können Sie sicherstellen, dass die langsame Einführung auf das begrenzte Publikum beschränkt bleibt, das Sie erreichen möchten.

## <a name="a-site-that-is-in-production"></a>Eine Site, die in Produktion ist

Wenn eine Site in Produktion ist, sollten Sie sicherstellen, dass alle Site-Seiten korrekt mit Tags versehen sind. Microsoft Dynamics 365 Commerce verwendet die für eine Seite eingegebenen Informationen, um alle SEO-Informationen auf dieser Seite zu rendern. Die folgenden Module bieten diese Funktionalität: Kategorieseitenübersicht, Listenseitenübersicht und Produktseitenübersicht.

Um die Indizierung von Suchmaschinen zu optimieren, verwendet das Rendering-Framework beide Informationen aus den SEO-Eigenschaften, die in Dynamics 365 Commerce konfiguriert sind, und modulspezifische Informationen. Für eine Site, die in Produktion ist, sollten Sie sicherstellen, dass die robots.txt-Datei die Indizierung Ihrer gesamten Site ermöglicht und Links zu Ihrem veröffentlichten Site-Map-Dokument enthält. Sie sollten die Funktionalität zum Generieren der Sitemap unter **Website-Einstellungen \> Sitemaps aktiviert** aktivieren.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Seiten-SEO-Einstellungen für die interne Vorschau, begrenzte Zielgruppen und alle Zielgruppen

Da Dynamics 365 Commerce authentifizierte WYSIWYG-Vorschauen (What you see is what you get) in Visual Page Builder unterstützt, können Autoren ihren Seiteninhalt vorbereiten, ohne befürchten zu müssen, dass die Informationen für die Besucher der Website sichtbar werden. Wenn eine Seite veröffentlicht werden muss, aber nur begrenzt sichtbar sein soll, sollte sie mit dem Meta-Tag **noindex** versehen werden, damit sie von Suchmaschinen nicht indiziert wird. Wenn die Seite dann für alle Zielgruppen bereit ist, sollten alle grundlegenden SEO-Metadaten vorhanden sein, um die Effizienz der Suchmaschinenindizierung zu maximieren. Außerdem sollte der **nolimit** Meta-Tag entfernt werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Verwalten von e-Commerce Benutzern und Rollen](manage-ecommerce-users-roles.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)

[Verwalten der Inhaltssicherheitsrichtlinie](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
