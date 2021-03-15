---
title: Verwalten von SEO-Metadaten
description: In diesem Thema wird das Verwalten von SEO-Metadaten (Search Engine Optimization) in Microsoft Dynamics 365 Commerce beschrieben.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c7cf9e76ffb30ee5c8bba318b2644e67c757bff0
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097414"
---
# <a name="manage-seo-metadata"></a>Verwalten von SEO-Metadaten


[!include [banner](includes/banner.md)]

In diesem Thema wird das Verwalten von SEO-Metadaten (Search Engine Optimization) in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

SEO-Metadaten für eine Site können mithilfe von Site-Maps und Seitenmetadaten verwaltet werden.
    
## <a name="site-maps"></a>Sitemaps

Eine Sitemap ist eine maschinenlesbare Liste der Seiten Ihrer Website im XML-Format. Sie soll von Suchmaschinen genutzt werden, damit sie bessere Suchergebnisse auf Ihrer Website bereitstellen können. Sitemaps können manuell von Suchmaschinen erfasst oder in einer robots.txt-Datei veröffentlicht werden.

Dynamics 365 Commerce unterstützt die automatische Generierung von Sitemaps. Siteübersichten werden automatisch aktualisiert, wenn die Seiten veröffentlicht bzw. zurückgenommen werden.

### <a name="turn-on-site-map-generation"></a>Sitemap-Generierung aktivieren

1. Melden Sie sich beim Erstellungstool an.
1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.
1. Stellen Sie sicher, dass die Option **Sitemaps aktiviert** aktiviert ist.

## <a name="page-metadata"></a>Seitenmetadaten

Mit Dynamics 365 Commerce können Sie SEO-Metadaten für einzelne Seiten verwalten. Sie können diese Informationen im Abschnitt **SEO-Eigenschaften** eines Seitencontainers anzeigen und ändern. Die folgenden SEO-Metadaten-Eigenschaften werden unterstützt:

- Titel
- Beschreibung
- SEO-Schlüsselwörter
- Aria-Labels
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Seitenmetadaten ändern

Um Seitenmetadaten zu ändern, führen Sie diese Schritte aus.

1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie im Navigationsbereich links **Seiten** aus.
1. Wählen Sie die Startseite aus, um sie im Seiteneditor zu öffnen.
1. Wählen Sie in der Befehlsleiste **Bearbeiten** aus.
1. Erweitern Sie im Eigenschaftenbereich rechts **Standard-Metatags**.
1. Um ein neues Metatag hinzuzufügen, wählen Sie **Hinzufügen** aus und geben Sie den Tag dann im Feld ein. Um ein vorhandenes Metatag zu entfernen, wählen Sie das Papierkorb-Symbol rechts daneben aus.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Geben Sie im Feld **Kommentare** **Aktualisierte Metatags** ein und wählen Sie dann **OK** aus.
1. Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen. Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.
1. Wählen Sie **Veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bestehende Seite einer Website ändern](modify-existing-page.md)

[Neue Seite hinzufügen](add-new-page.md)

[Auswählen von Seitenlayouts](select-page-layouts.md)

[Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md)

[Erweitern einer Produktseite](enrich-product-page.md)

[Füllen einer Kategorie-Landingpage](enrich-category-page.md)

[Überprüfen der Zugänglichkeit des Seiteninhalts](verify-accessibility.md)

[Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]