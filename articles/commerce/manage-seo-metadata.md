---
title: Verwalten von SEO-Metadaten
description: In diesem Artikel wird das Verwalten von SEO-Metadaten (Search Engine Optimization) in Microsoft Dynamics 365 Commerce beschrieben.
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4b04d675a903279e667e1f5fcee387f05d979e81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276827"
---
# <a name="manage-seo-metadata"></a>Verwalten von SEO-Metadaten

[!include [banner](includes/banner.md)]

In diesem Artikel wird das Verwalten von SEO-Metadaten (Search Engine Optimization) in Microsoft Dynamics 365 Commerce beschrieben.

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
1. Wählen Sie im Seiteneditor oben im Seitengliederungssteuerelement auf der linken Seite **Option für Gliederungsmodus** (Zahnradsymbol) und dann **Ansicht der erweiterten Gliederung** aus.
1. Erweitern Sie in der Gliederungsansicht die Struktursteuerelemente, um den Inhalt des **HTML-Kopf**-Slots anzuzeigen.
1. Im **HTML-Kopf**-Slot wählen Sie das gewünschte SEO-Modul aus (z. B. **Seitenzusammenfassung**, **Produktseitenzusammenfassung**, **Zusammenfassung der Kategorieseite** oder **Metatags**).
1. Bearbeiten Sie im Eigenschaftenbereich auf der rechten Seite die gewünschten SEO-Daten für das ausgewählte SEO-Modul (z. B. **Titel**, **Beschreibung** oder **Freigabebild**).
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Geben Sie im Feld **Kommentare** **Aktualisierte SEO-Daten** ein und wählen Sie dann **OK** aus.
1. Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen. Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.
1. Wählen Sie **Veröffentlichen** aus.

> [!TIP]
> Autoren können die **Option für Gliederungsmodus** (Zahnradsymbol) oben in der linken Gliederungssteuerung im Seiteneditor verwenden, um zwischen der **Ansicht der grundlegenden Gliederung** und der **Ansicht der erweiterten Gliederung** zu wechseln. **Ansicht der grundlegenden Gliederung** ist die Standardeinstellung und filtert die Gliederung so, dass nur Module im **Body**-HTML-Slot für eine Seite angezeigt werden. **Ansicht der erweiterten Gliederung** zeigt das gesamte Seitenmodul, einschließlich der Slots für **HTML-Kopf**, **Textanfang** und **Textende**. Diese Ansicht ist nützlich, wenn Autoren bestimmte SEO- oder Skriptmoduleinstellungen für eine Seite bearbeiten müssen.

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
