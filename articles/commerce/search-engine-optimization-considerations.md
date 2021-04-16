---
title: Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site
description: In diesem Thema werden Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Website von der Entwicklung bis zur Produktion behandelt.
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 52a10c754315bfef2a01c593f5fa5366e9054982
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791798"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site


[!include [banner](includes/banner.md)]

In diesem Thema werden Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Website von der Entwicklung bis zur Produktion behandelt.

## <a name="a-site-that-is-under-development"></a>Eine Seite, die sich in der Entwicklung befindet

Während eine Website entwickelt wird, sollten alle Websiteseiten die folgende Bezeichnung haben: Die Metatags **NOINDEX** und **NOFOLLOW**, damit Suchmaschinen die Seiten nicht indizieren und Entwicklungsversionen Ihrer Website in ihrem Cache speichern. Um diese Konfiguration durchzuführen, müssen Sie das Standard-Metatags-Modul zur Site-Seitenvorlage hinzufügen. Die Standardeigenschaften für Metatags sind dann im Abschnitt SEO-Eigenschaften im Seiteneditor verfügbar. Mit diesen Eigenschaften können Sie die Metatags verwalten.

## <a name="soft-launch-of-a-site"></a>Langsame Einführung einer Website

Bei einer „langsamen Einführung“ wird eine Website einem begrenzten Publikum oder Markt zur Verfügung gestellt, bevor die vollständige Einführung erfolgt. Bei einer langsamen Einführung Ihrer Website sollten Sie die Metatags **NOINDEX** beibehalten. Auf diese Weise können Sie sicherstellen, dass die langsame Einführung auf das begrenzte Publikum beschränkt bleibt, das Sie erreichen möchten.

## <a name="a-site-that-is-in-production"></a>Eine Site, die in Produktion ist

Wenn eine Site in Produktion ist, sollten Sie sicherstellen, dass alle Site-Seiten korrekt mit Tags versehen sind. Microsoft Dynamics 365 Commerce verwendet die für eine Seite eingegebenen Informationen, um alle SEO-Informationen auf dieser Seite zu rendern. Die folgenden Module bieten diese Funktionalität: Kategorieseitenübersicht, Listenseitenübersicht und Produktseitenübersicht.

Um die Indizierung von Suchmaschinen zu optimieren, verwendet das Rendering-Framework beide Informationen aus den SEO-Eigenschaften, die in Dynamics 365 Commerce konfiguriert sind, und modulspezifische Informationen. Für eine Site, die in Produktion ist, sollten Sie sicherstellen, dass die robots.txt-Datei die Indizierung Ihrer gesamten Site ermöglicht und Links zu Ihrem veröffentlichten Site-Map-Dokument enthält. Sie sollten die Funktionalität zum Generieren der Sitemap unter **Website-Einstellungen \> Sitemaps aktiviert** aktivieren.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Seiten-SEO-Einstellungen für die interne Vorschau, begrenzte Zielgruppen und alle Zielgruppen

Da Dynamics 365 Commerce authentifizierte WYSIWYG-Vorschauen (What you see is what you get) in Visual Page Builder unterstützt, können Autoren ihren Seiteninhalt vorbereiten, ohne befürchten zu müssen, dass die Informationen für die Besucher der Website sichtbar werden. Wenn eine Seite veröffentlicht werden soll, ihre Verfügbarkeit jedoch begrenzt sein muss, sollte sie das Meta-Tag **NOINDEX** aufweisen, damit sie nicht von Suchmaschinen indiziert wird. Wenn die Seite dann für alle Zielgruppen bereit ist, sollten alle grundlegenden SEO-Metadaten vorhanden sein, um die Effizienz der Suchmaschinenindizierung zu maximieren. Darüber hinaus sollte das Metatag **NOLIMIT** entfernt werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Verwalten von e-Commerce Benutzern und Rollen](manage-ecommerce-users-roles.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)

[Verwalten der Inhaltssicherheitsrichtlinie](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]