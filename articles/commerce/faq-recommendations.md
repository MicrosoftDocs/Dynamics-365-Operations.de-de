---
title: Produktempfehlungs-FAQs
description: Dieses Thema enthält Informationen über die Prozesse und Tools, die Sie verwenden können, um Probleme zu beheben, die den Produktempfehlungen oder deren Ergebnisse zugeordnet werden.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e27e4c4d8bdf614d6f55f44daeac3bc152219004
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404301"
---
# <a name="product-recommendations-faq"></a>Produktempfehlungs-FAQs


[!include [banner](includes/banner.md)]

Dieses Thema enthält Informationen über die Prozesse und Tools, die Sie verwenden können, um Probleme zu beheben, die den [Produktempfehlungen](product-recommendations.md) oder deren Ergebnisse zugeordnet werden.

## <a name="best-practices"></a>Bewährte Methoden
Es ist außerordentlich wichtig, das Konzept von Produktmastern und von Varianten zu verwenden. Die vernünftige Gruppierung von Varianten zu einem übergeordneten Produktmaster hilft dem Listenalgorithmus und erstellt bessere Modelle. Darüber hinaus kann der Service nur eine Instanz eines Produkts bedienen statt alle eng zugehörigen Varianten in einer Liste zu nutzen. Wenn alle zugehörigen können Varianten in einer Liste verwendet werden, können fehlerhafte oder doppelte Ergebnisse auftreten.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Warum fehlen Produkte aus meinen Empfehlungslisten?

Normalerweise wenn ein Artikel fehlt in einer Produktempfehlungsliste, ist es ein  Produktkonfigurationsproblem. Beispielsweise gibt es ein falsches Produktstartdatum oder Enddatum, eine Abmessung ist falsch konfiguriert oder das Produkt ist nicht im richtigen Kanalsortiment, etc.

Wenn ein Artikel in einer Empfehlungsliste fehlt, die auf der maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) basiert, passt der Artikel möglicherweise nicht die Empfehlungsliste oder es sind möglicherweise nicht genügend Einkaufsbuchungen für die Empfehlungsliste vorhanden.

Es wird empfohlen, diese Schritte zu prüfen:
1. **Überprüfen Sie, ob in der Produktempfehlungen die Hauptniederlassung aktiviert wurden.** Weitere Informationen dazu, wie diese Funktion aktiviert wird, finden Sie unter [Aktivieren von Produktempfehlungen](enable-product-recommendations.md).
1. **Überprüfen Sie, dass entscheidende Produktattribute festgelegt werden.** Es müssen z.B Sortimente auf **Einschließen** festgelegt werden.
1. **Für neu asssortierte Produkte kann es möglicherweise bis zu 3 Stunden dauern, bevor das Produkt auf der neuen Liste angezeigt wird.**
1. **Wenn ein Produkt noch immer nicht in Trends, Bestseller, Personen gefällt auch oder werden häufig auch zusammen eingekauft, erscheint, dann hat dieses Produkt nicht genügend Transaktionen.** In diesem Fall können Sie entweder auf mehr Transaktionen warten, die Standardempfehlungslistenparameter aktualisieren, oder manuellen Aktivitäten verwenden, um die Empfehlungsproduktlisteergebnisse zu ändern. Weitere Informationen zu Empfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).
1. **Überprüfen Sie, ob das Produkt den Empfehlungskriterien der Liste entspricht.** Weitere Informationen zu Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Wie kann ich schlechte Empfehlungsergebnisse verhindern?

Empfehlungslisten erfordern eine große Anzahl von Transaktionen, um Ergebnisse zu liefern. Daher muss klar sein, ob Benutzer vollständige Verlaufs-Buchungsdaten bereitstellen.

Darüber hinaus werden Produkte, die keine Transaktionen oder wenige Transaktionen enthalten haben in der Regel keine **Person gefällt auch** oder **Häufig zusammen gekauft** Ergebnisse und  erscheinen nicht in **Trends** oder **Bestseller-** Empfehlungslisten. Diese Situation kann bei sehr neuen Produkte oder für alte Produkten auftreten, die eine geringe Anzahl von Einkäufe haben. Gängige neue Artikel überwinden dieses Problem leicht.

Es wird empfohlen, diesen Schritten zu folgen:
1. **Überprüfen Sie, ob das Produkt den Empfehlungskriterien dieser Liste entspricht.** Weitere Informationen zu Produktempfehlungsparameter finden Sie unter AI-ML-basierte Produktempfehlungsergebnisse bearbeiten.
1. **Wenn das Produkt neu ist, sollten Sie eine Empfehlungsliste ändern, bis das Produkt mehr Transaktionen aufweist.** Weitere Informationen zum Bearbeiten von Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).


- **Überprüfen Sie, ob das Produkt den Empfehlungskriterien dieser Liste entspricht.** Weitere Informationen zu Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).
- **Wenn das Produkt neu ist, sollten Sie eine Empfehlungsliste ändern, bis das Produkt mehr Transaktionen aufweist.** Weitere Informationen zum Bearbeiten von Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Kann ich ein Produkt entfernen aber es immer noch im Shop anzeigen?

Sie können Listen anpassen die algorithmisch generiert werden, wenn eine Geschäftsanforderung entsteht. Wenn ein Produkt aus einer Empfehlungsliste entfernt wird, bleibt das Produkt im Shop auffindbar. Weitere Informationen zum Bearbeiten von Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).

Wenn Sie möchten, dass ein Artikel von Shop nicht angezeigt wird, müssen Die den Wert **Artikelsortiments** auf **ausschließen** ändern.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Wie wird eine Liste einer E-Commerce-Seite hinzugefügt?

Für Informationen dazu, wie Produktempfehlungsseiten Ihrer E-Commerce-Website hinzugefügt werden, finden Sie unter [Produktempfehlungslisten der Seite hinzufügen](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Wie aktiviere ich Empfehlungen für POS?

Nachdem Sie Produktempfehlungen aktiviert haben, müssen Sie den Empfehlungsbereich dem Bildschirm der POS-Steuerung hinzufügen. Weitere Informationen finden Sie unter [Hinzufügen einer Empfehlungssteuerung zum Transaktionsbild auf POS-Geräten](add-recommendations-control-pos-screen.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Produktempfehlungen am POS hinzufügen](product.md)

[Empfehlungen zum Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)
