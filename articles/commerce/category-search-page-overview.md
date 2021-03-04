---
title: Übersicht über die Standard-Kategorie-Landingpage und die Suchergebnisseite
description: Dieses Thema gibt eine Übersicht über die Standard-Kategorie-Startseite und Suchergebnisseite in Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e85449c10fa4a768a144ce423a77bd1fc2c94352
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412531"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Übersicht über die Standard-Kategorie-Landingpage und die Suchergebnisseite

[!include [banner](includes/banner.md)]

Dieses Thema gibt eine Übersicht über die Standard-Kategorie-Startseite und Suchergebnisseite in Microsoft Dynamics 365 Commerce E-Commerce.

## <a name="default-category-landing-page"></a>Standard-Kategorie Startseite

Die Standardkategoriestartseite ist die Seite, zu der die Websitebenutzer in der Regel gelangen, wenn sie eine Kategorie in der Navigationshierarchie auswählen. Mit der Kategorieseite können Sie durchsuchen, und Sie können die kategorisierten Produkte auch sortieren und verfeinern.

![Standard-Kategorie Startseite](./media/SimpleCategoryLandingDressCategory.png)

Oben auf der Seite befindet sich eine Kopfzeile mit allen Produktkategorien und anderen Seiten, die Verkaufsmanager kategorisiert haben. Konfiguration wird als Teil der Konfiguration der Kanalnavigationshierarchie ausgeführt. Unten auf der Startseite befindet sich eine Fußzeile mit Direktlinks zu verschiedenen Themen, die Kunden interessieren könnten.

Die folgenden Komponenten sind für eine Kategorie zentral:

- **Produktplatzierungskacheln** zeign die Produkte, die der Verkaufmanager in einer Kategorie als Teil der Variante der Navigationshierarchie definiert.
- **Verfeinerungs- und Auswahlzusammenfassung** sind Filter, die Zählungen beeinhalten und zur Feinsuche von Artikeln verwendet werden. Der Verkaufmanager konfiguriert sie als Teil der Konfiguration der Metadaten, die den Kanalkategorien und Produktattributen zugeordnet werden.
- **Sortieroptionen** werden von den Websitebesuchern verwendet, um die Produkte zu sortieren. Standardmäßig sind die folgenden Sortieroptionen verfügbar:

    - Preis - niedrig bis hoch.
    - Preis - hoch bis niedrig
    - Produktname - \[A-Z\] 
    - Produktname - \[Z-A\] 
    - Bewertung - tief bis hoch
    - Bewertung - hoch bis tief

- Die **Paginierung** ermöglicht es Websitebesuchern, von einer Seite mit kategorisierten Produktergebnissen zu einer anderen Seite zu wechseln.
- **Gesamtzahl** gibt die Gesamtzahl von Produkten an, die in einer Kategorie definiert werden.

## <a name="enrich-a-category-landing-page"></a>Füllen einer Kategorie-Landingpage

Wenn Sie für eine Kategorieangebotsseite eine angepasste Erfahrung für eine bestimmte Kategorie möchten, können Sie die Kategoriestartseite für diese Kategorie „anreichern“. So können Sie ein Marketings-Video und Geschichten zu den Kategorien hinzufügen, um die Aufmerksamkeit des Käufers abzurufen. Weitere Informationen finden Sie unter [Reichern Sie eine Kategorieangebotsseite an](enrich-category-page.md).

![Angereicherte Kategorie-Startseite](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Ergebnisseite automatisch vorschlagen und suchen

Websitebenutzer können eine Website durchsuchen, entweder, indem sie zu einer Kategorie in der Navigationshierarchie gehen oder indem Sie einen Suchbegriff in der Auswahlliste eingeben.

Sobald der Benutzer mit der Eingabe im Suchfeld beginnt, schlägt die automatische Funktionalität Suchbegriffe vor.

Nachfolgend sind einige Vorschlagstypen, die angezeigt werden können:

- **Schlüsselwörter** werden verwendet, um Artikel zu allen Produkten zu suchen, die in dem Kanal sortiert werden.
- **Produkte** beinhalten direkte Links zu Produktdetailseiten bereit.
- **Bewertete Kategoriesuchvorschläge** führt verschiedene Kategorien auf und lässt Benutzer nach Schlüsselwörtern in einer bestimmten Kategorie suchen.

![Umfassende automatische Vorschläge](./media/ImmersiveAutoSuggestUX.png)

Wenn Benutzer eines der Schlüsselwörter oder eine bewertete der Kategorie aus den Suchvorschlägen auswählt oder wenn es keine Vorschläge für den Suchbegriff gibt, den sie eingeben, werden sie zu einer Suchergebnisseite umgeleitet. Die Benutzer kann dann die Suchergebnisse durchsuchen, sortieren und verfeinern, um den gewünschten Artikel zu finden.

![Suchenangebote](./media/SearchLanding.png)

Die folgenden Komponenten sind für eine Suchergebnisseite zentral:

- **Produktplatzierungskacheln** zeigen die Produkte für die Suche des Benutzers. Standardmäßig werden diese Kacheln durch die Cloud-betriebene Suchenbedeutungspunktzahl für die Benutzersuche sortiert.
- **Verfeinerungs- und Auswahlzusammenfassung** sind Filter, die Zählungen beeinhalten und zur Feinsuche von Artikeln verwendet werden. Der Verkaufmanager konfiguriert sie als Teil der Konfiguration der Metadaten, die dann den Kanalkategorien und Produktattributen zugeordnet werden.
- **Sortieroptionen** werden von den Websitebesuchern verwendet, um die Produkte zu sortieren. Standardmäßig sind die folgenden Sortieroptionen verfügbar:

    - Preis - niedrig bis hoch.
    - Preis - hoch bis niedrig
    - Produktname - \[A-Z\] 
    - Produktname - \[Z-A\] 
    - Bewertung - tief bis hoch
    - Bewertung - hoch bis tief
    - Standard

- Die **Paginierung** ermöglicht es Websitebesuchern, von einer Seite mit kategorisierten Produktergebnissen zu einer anderen Seite zu wechseln.
- **Gesamtzahl** gibt die Gesamtzahl von Produkten an, die in einer Kategorie definiert werden und den Suchkriterien entsprechen.

>[!NOTE]
>Diese Cloud-betriebenen Suchfunktionen sind ab Version 10.0.8 verfügbar. Stellen Sie sicher, dass unter **Handelsparameter > Konfigurationsparameter** ein Eintrag für „ProductSearch.UseAzureSearch set to 'true'“ vorhanden ist. 
![Konfigurationsparameter für die Cloud-betriebene Suche](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Cloud-basierte Suche](cloud-powered-search-overview.md)

[Übersicht der Startseite](quick-tour-home-page.md)

[Übersicht der Produktdetailseiten](quick-tour-pdp.md)

[Übersicht der Einkaufswagen- und Auschecken-Seiten](quick-tour-cart-checkout.md)

[Übersicht der Kontenverwaltungsseiten](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]