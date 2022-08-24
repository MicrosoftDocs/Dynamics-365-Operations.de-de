---
title: Übersicht über die cloudbasierte Suche
description: Dieser Artikel enthält eine Übersicht der Cloud-betriebenen Suche in Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273665"
---
# <a name="cloud-powered-search-overview"></a>Übersicht über die cloudbasierte Suche

[!include [banner](includes/banner.md)]

Dieser Artikel enthält eine Übersicht der Cloud-betriebenen Suche in Microsoft Dynamics 365 Commerce.

Produkt-Auffindbarkeit hilft sicherzustellen, dass Debitoren Produkte über das Durchsuchen von Kategorien schnell und einfach finden. Für Einzelhändler ist die Produkterkennung ein wichtiges Tool für die Interaktion mit Kunden über alle von der Cloud Scale-Unit (CSU) unterstützten Kanäle, wie E-Commerce und Point of Sale (POS).

Debitoren sind sich an die blitzschnellen Antwortzeiten von Internet-Suchmodulen, tollen E-Commerce-Websites, Sozialen Apps und automatischen Vorschlägen gewöhnt, die angezeigt werden, solange sie Suchbegriffen, facettierte Navigation und Hervorhebungen eingeben. Wenn Kunden in einem E-Commerce Store nicht schnell das Produkt finden, das sie suchen, werden sie nicht zögern, einen anderen E-Commerce Store aufzusuchen.

Die Cloud-gestützte Produktauffindbarkeit in Commerce hilft Einzelhändlern, die Kundenbindung und die Konversionsraten über alle Kanäle hinweg weiter zu erhöhen - powered by CSU.

Die Commerce-Suche verfügt über verbesserte Funktionalitäten, um Einzelhändlern eine bessere Auffindbarkeit von Produkten zu ermöglichen. Gleichzeitig bieten diese Funktionalitäten die Skalierbarkeit und Leistung, die für den E-Commerce-Verkehr erforderlich sind.

## <a name="browse-and-search"></a>Durchsuchen und suchen

Suchrelevanz und Leistung sind entscheidende Faktoren in der Omnikanal-Erfahrung, da Produktauffindbarkeit vorrangig ist für die Suchfunktion zur Informationsabrufung und Inhaltsnavigation. Ein effektives und effizientes Durchsuchen und Sucherlebnis hiflt, die Konversion zu erhöhen.

Die folgende Abbildung zeigt ein Beispiel für typisches Durchsuchen und für Suchfunktionen.

![Suchenangebotsseite.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Facettierte Navigations- und Auswahlzusammenfassung 

Facettierte Navigation hilft Kunden, Inhalt einfacher zu suchen, indem Filter zum Verfeinern der Suche gesetzt werden können, die mit Bedingungen oder einem Satz von Bedingungen verknüpft sind. Nachdem ein Kunde Verfeinerungskriterien ausgewählt und angewendet hat, wird eine Zusammenfassung der Auswahl angezeigt. 

Wenn Sie facettierte Navigation verwenden, können Sie verschiedene Kriterien für verschiedene Bedingungen in einem Bedingungssatz konfigurieren, und müssen keine zusätzlichen Seiten erstellen. 

Die folgende Abbildung zeigt ein Beispiel an, wo facettierte Navigation bei einer Suche verwendet wird.

![Auswahl-Zusammenfassung.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Interaktive automatische Vorschläge

Die aktuelle Autosuggest-Funktionalität zeigt Schlüsselwörter an, die eine Suche nach dem passenden Schlüsselwort auslösen. Aufgrund der neuen Verbesserungen in Commerce können Kunden häufig Links zu Produkten entdecken, bevor sie die Eingabe beendet haben.

Commerce unterstützt auch Funktionen für Schlüsselwortabgleiche in verschiedenen Kategorien. Mit dieser Funktionalität können Kunden die Anzahl von entsprechenden Schlüsselwörtern in Kategorien sehen und eine Suche nach Schlüsselwort in anderen Kategorien starten.

Die folgende Abbildung zeigt ein Beispiel an, wo interaktives automatisches Vorschlagen verwendet wird.

![Umfassende automatische Vorschläge.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sortieren

Die Sortierungsfunktionalität ermöglicht Kunden, Kategorieergebnisse zu sortieren, zu suchen und zu durchsuchen und diese durch Kriterien wie Preis, Produktname und Produktnummer zu verfeinern. Wenn Sie [Produktempfehlungen](product-recommendations.md) in Ihrer Umgebung aktivieren, können Kunden die Ergebnisse auch anhand erweiterter Sortierkriterien sortieren, z. B. „neu“, „Bestseller“ und „beliebt“.


> [!NOTE]
> Diese Cloud-betriebenen Suchfunktionen sind ab Version 10.0.8 verfügbar. Stellen Sie sicher, dass ein Eintrag für „ProductSearch.UseAzureSearch“ auf 'true' festgelegt ist in **Commerce Parameter > Konfigurationsparameter**. 
![Konfigurationsparameter für die cloud-betriebene Suche.](./media/CloudPoweredSearchConfigurationParameters.png)
>Erweiterte Sortieroptionen wie „neu“, „Bestseller“ und „beliebt“ sind mit der Commerce-SSK-Version 9.35+ und der Dynamics 365 Commerce Version 10.0.20 verfügbar.  


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite](category-search-page-overview.md)

[Verwalten von SEO-Metadaten](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
