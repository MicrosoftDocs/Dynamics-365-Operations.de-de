---
title: Überblick über Produktempfehlungen
description: Dieses Thema enthält allgemeine Informationen zu Produktempfehlungen. Mit Produktempfehlungen können Kunden einfach und schnell gesuchte Produkte finden und sogar Produkte, deren Kauf sie ursprünglich nicht eingeplant hatten.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770046"
---
# <a name="product-recommendations-overview"></a>Überblick über Produktempfehlungen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce kann verwendet werden, um Produktempfehlungen auf der E-Commerce-Website und dem POS-Gerät (Point of Sale) anzuzeigen. Produktempfehlungen sind Artikel, an denen ein Kunde interessiert sein könnte. Die Empfehlungen basieren auf den Kauftrends anderer Kunden in Online- und physischen Filialen.

Mit Produktempfehlungen können Kunden leicht und schnell die gewünschten Produkte finden, während sie eine Erfahrung erhalten, die ihnen gute Dienste leistet. Cross-Selling und Upselling können Kunden sogar dabei unterstützen, zusätzliche Produkte zu finden, deren Kauf sie ursprünglich nicht eingeplant hatten. Wenn Empfehlungen zur Unterstützung der Produktfindung verwendet werden, können sie mehr Conversion-Möglichkeiten schaffen, den Umsatz steigern und sogar die Kundenzufriedenheit und -bindung verbessern.

In Commerce basieren Produktempfehlungen in großem Umfang auf maschinellen Lerntechnologien von Microsoft Recommendations.


## <a name="scenarios"></a>Szenarien

Produktempfehlungen sind für die folgenden Szenarien verfügbar:

- **Auf jeder Filialseite zum Durchsuchen oder jeder Landingpage im E-Commerce:** Wenn Kunden oder Geschäftspartner eine Filialseite besuchen, kann die Empfehlungs-Engine Produkte in den Listen **Neu**, **Bestseller** und **Populär** vorschlagen.
- **Auf jeder Produktdetailseite:** Wenn Kunden oder Filialmitarbeiter die Seite **Produktdetails** aufrufen, schlägt die Empfehlungs-Engine zusätzliche Artikel vor, die wahrscheinlich auch gekauft werden. Diese Artikel werden in der Liste **Personen gefällt auch** angezeigt.
- **Auf der Transaktionsseite oder der Auscheckseite:** Die Empfehlungs-Engine schlägt Artikel basierend auf der gesamten Liste der Artikel im Warenkorb vor. Diese Artikel werden in der Liste **Wird häufig zusammen gekauft** angezeigt.

## <a name="recommendation-service"></a>Empfehlungsdienstleistung

Produktempfehlungen verwenden die Recommendations-Technologien für maschinelles Lernen auf folgende Weise:

- Daten in dem für den Empfehlungsdienst erforderlichen Format werden aus der Commerce-Betriebsdatenbank extrahiert und an den Entitätsspeicher gesendet.
- Der Empfehlungsdienst verwendet die Daten, um die Empfehlungsmodule für die Listen **Personen gefällt auch**, **Wird häufig zusammen gekauft**, **Neu**, **Bestseller** und **Populär** zu schulen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Erstellen von kuratierten Produktempfehlungslisten](create-editorial-recommendation-lists.md)

[Verwalten von KI-ML-basierten Produktempfehlungsergebnissen](modify-product-recommendation-results.md)

[Hinzufügen von Produktempfehlungslisten zu Seiten](add-reco-list-to-page.md)