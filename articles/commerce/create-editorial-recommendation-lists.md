---
title: Manuelle Erstellung kuratierter Empfehlungen
description: Dieser Artikel erklärt, wie Händler manuell Produktlisten für Microsoft Dynamics 365 Commerce-Kunden erstellen und verwalten können.
author: bebeale
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
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e1a1b402165c5cb35696cf1cf6630770ad07508a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892677"
---
# <a name="manually-create-curated-recommendations"></a>Manuelle Erstellung kuratierter Empfehlungen

[!include [banner](includes/banner.md)]

Dieser Artikel erklärt, wie Händler manuell Produktempfehlungslisten für Microsoft Dynamics 365 Commerce-Kunden erstellen und verwalten können.

Kuratierte Listen sind Sammlungen von individuellen Inhalten, die von Personen erstellt und kuratiert wurden.  

## <a name="create-a-new-list"></a>Neue Liste erstellen

Um eine kuratierte Produktempfehlungsliste zu erstellen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Einzelhandel und Handel &gt; Produktempfehlungen &gt; Empfehlungslisten**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Listen-ID** einen Wert ein.
1. Geben Sie im Feld **Listennamen** einen Wert ein.
    - Der **Listenname** Ist der Titel der Liste, der in der kuratierten Listenauswahl des Moduls **Produktsammlung** angezeigt wird.
1. Um Produkte der Liste hinzuzufügen, wählen Sie **Produkte hinzufügen**.
1. Um die Reihenfolge der Produkte in der Liste zu ändern, geben Sie einen Wert in der Spalte **Anzeigereihenfolge** ein.
    - Wenn zwei Produkte den gleichen Wert aufweisen, dann kann der abschließende Auftrag dieser zwei Ergebnisse sich vom Back Office unterscheiden.
1. Wählen Sie **Speichern**, um die Liste zu speichern.

## <a name="example-list"></a>Beispielliste

![Beispiel kuratierte Liste im Backoffice.](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Produktempfehlungen in POS hinzufügen](product.md)

[Empfehlungen dem Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]