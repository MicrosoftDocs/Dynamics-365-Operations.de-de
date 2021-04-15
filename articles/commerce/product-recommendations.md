---
title: Überblick über Produktempfehlungen
description: Dieses Thema enthält allgemeine Informationen zu Produktempfehlungen. Mit Produktempfehlungen können Kunden einfach und schnell gesuchte Produkte finden und sogar Produkte, deren Kauf sie ursprünglich nicht eingeplant hatten.
author: Moonma
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 044a5c21e4ebf1bf83edc74335e655b9388bc1d4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795596"
---
# <a name="product-recommendations-overview"></a>Überblick über Produktempfehlungen

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce kann verwendet werden, um Produktempfehlungen auf der E-Commerce-Website und dem POS-Gerät (Point of Sale) anzuzeigen. Produktempfehlungen sind Artikel, an denen ein Kunde interessiert sein könnte. Die Empfehlungen basieren auf den Kauftrends anderer Kunden in Online- und physischen Filialen.

Mit Produktempfehlungen können Kunden einfach und schnell die gewünschten Produkte finden, während sie eine Erfahrung erhalten, die ihnen gute Dienste leistet. Cross-Selling und Upselling können Kunden sogar dabei unterstützen, zusätzliche Produkte zu finden, deren Kauf sie ursprünglich nicht eingeplant hatten. Wenn Empfehlungen zur Unterstützung der Produktfindung verwendet werden, können sie mehr Conversion-Möglichkeiten schaffen, den Umsatz steigern und sogar die Kundenzufriedenheit und Kundenbindung verbessern.

In E-Commerce basieren Produktempfehlungen in großem Umfang auf maschinellen Lerntechnologien von Microsoft Recommendations.

## <a name="recommendation-service"></a>Empfehlungsdienstleistung

Der Produktempfehlungsdienst verwendet Technologien für künstliche Intelligenz und maschinelles Lernen (AI-ML) auf folgende Weise:

- Daten in dem für den Empfehlungsdienst erforderlichen Format werden aus der Commerce-Betriebsdatenbank extrahiert und an den Azure Data Lake Storage Entitätsspeicher gesendet.
- Der Empfehlungsdienst verwendet die gespeicherten Daten, um die Empfehlungsmodule für die Listen **Personen gefällt auch**, **Wird häufig zusammen gekauft**, **Neu**, **Bestseller** und **Populär** zu schulen.

## <a name="scenarios"></a>Szenarien

Produktempfehlungen sind für die folgenden Szenarien verfügbar:

- **Auf jeder Filialseite zum Durchsuchen oder jeder Landingpage im E-Commerce:** Wenn Kunden oder Geschäftspartner eine Filialseite besuchen, kann die Empfehlungs-Engine Produkte in den Listen **Neu**, **Bestseller** und **Populär** vorschlagen.
- **Auf jeder Produktdetailseite:** Wenn Kunden oder Filialmitarbeiter die Seite **Produktdetails** aufrufen, schlägt die Empfehlungs-Engine zusätzliche Artikel vor, die wahrscheinlich auch gekauft werden. Diese Artikel werden in der Liste **Personen gefällt auch** angezeigt.
- **Auf der Transaktionsseite oder der Auscheckseite:** Die Empfehlungs-Engine schlägt Artikel basierend auf der gesamten Liste der Artikel im Warenkorb vor. Diese Artikel werden in der Liste **Wird häufig zusammen gekauft** angezeigt.
- **Personalisierte Empfehlungen:** Verkaufsberater können angemeldeten Kunden neben neuen Funktionen die personalisierte Liste **Entnahmen für Sie** bieten, mit der vorhandene Listenszenarien basierend auf dem Kunden personalisiert werden können. Um mehr zu erfahren, gehen Sie zu [Personalisierte Empfehlungen aktivieren](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Arten von Produktempfehlungen

In der folgenden Tabelle werden verschiedene Arten von automatisierten Produktempfehlungen beschrieben, die Einzelhändlern zur Implementierung in Ihrer Dynamics 365 Commerce Lösung über das [Produktkollektionsmodul](product-collection-module-overview.md) zur Verfügung stehen. Einzelhänder können auch personalisierte Ergebnisse für einen angemeldeten Benutzer anzeigen, wenn der Site-Autor diese Option auswählt.

| Produktsammelmodul  | Typ | Beschreibung |
|----------------------------|------|-------------|
| Neue                        | Algorithmisch | Dieses Modul zeigt eine Liste der neuesten Produkte, die kürzlich nach Kanälen und Katalogen sortiert wurden. |
| Bestseller               | Algorithmisch | Dieses Modul zeigt eine Liste der Produkte, die nach der höchsten Anzahl an Verkäufen sortiert sind. |
| Populär                   | Algorithmisch | Dieses Modul zeigt eine Liste der leistungsstärksten Produkte für einen bestimmten Zeitraum an, und zwar geordnet nach der höchsten Anzahl an Verkäufen.  |
| Wird häufig zusammen gekauft | AI-ML | Dieses Modul empfiehlt eine Liste der Produkte, die üblicherweise zusammen mit dem Inhalt des aktuellen Warenkorbs des Verbrauchers gekauft werden. |
| Personen gefällt auch           | AI-ML | Dieses Modul empfiehlt Produkte für ein bestimmtes Saatgutprodukt basierend auf den Kaufmustern der Verbraucher. |
| Entnahmen für Sie              | AI-ML | Dieses Modul empfiehlt eine personalisierte Liste von Produkten basierend auf den Kaufmustern des angemeldeten Benutzers. Für einen Gastbenutzer wird diese Liste reduziert. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Produktempfehlungen in POS hinzufügen](product.md)

[Empfehlungen dem Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]