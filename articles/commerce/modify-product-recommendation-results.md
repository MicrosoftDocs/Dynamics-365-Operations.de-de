---
title: Verwalten von KI-ML-basierten Produktempfehlungsergebnissen
description: In diesem Thema wird erläutert, wie Sie Ergebnisse zu Produktempfehlungen basierend auf maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) an Ihr Unternehmen anpassen.
author: bebeale
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
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770069"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a>Verwalten von KI-ML-basierten Produktempfehlungsergebnissen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Ergebnisse zu Produktempfehlungen basierend auf maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) an Ihr Unternehmen anpassen. 

Nach dem Aktivieren der Produktempfehlungen werden die Standardeinstellungen wirksam. Diese Parameter können für viele Anforderungen verwendet werden. Es empfiehlt sich, einige Zeit zum Bewerten einzuplanen und festzustellen, ob die Ergebnisse zur Verkaufsbewegung von Produkten passen. Wir empfehlen, die Ergebnisse einige Tage lang auszuwerten, bevor Sie die Parameter nach Bedarf ändern und erneut testen. 

## <a name="understanding-recommendation-list-parameters"></a>Verstehen der Empfehlungslistenparameter

Informieren Sie sich vor dem Ändern der Parameter, wie sich diese auf die folgenden Ergebnisse auswirken.

### <a name="trending-product-list"></a>Populäre Produktliste

Die **populäre** Produktliste besitzt zwei Parameter, die geändert werden können: ![Beispiel für populäre Standardlistenparameter](./media/exampletrendingparameters.png)
1. **Neue Produkte aus den letzten X Tagen einbeziehen** – Produkte, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum hinzugefügt wurden, können zur Auswahl von Produktkandidaten verwendet werden. Der Standardwert in der Abbildung weist darauf hin, dass Produkte mit einem Alter von 180 Tagen in der Liste der populären Produktliste verwendet werden können.
1. **Verkäufe aus den letzten X Tagen einbeziehen** – Verkaufsvorgänge, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum getätigt wurden, können zum Bestellen der Produkte verwendet werden. Der obige Standardwert legt nahe, dass alle Einkäufe, die in den letzten 30 Tagen für ein Produkt getätigt wurden, verwendet werden, um die Platzierung des Produkts in der Liste der populären Produkte zu bestimmen. 

### <a name="best-selling-product-list"></a>Bestseller-Produktliste

Abhängig von Ihrem Unternehmen kann Bestseller andere Ergebnisse als Trends liefern, obwohl beide Transaktionsdaten für die Bestellung von Produkten verwenden. Da Bestseller nicht nach Sortimentsdatum ablaufen, können mit Bestseller immer noch sehr beliebte ältere Produkte hervorgehoben werden, die möglicherweise von der Trendliste gestrichen wurden. 

Die **Bestseller**-Produktliste besitzt einen Parameter, der geändert werden kann:

![Beispiel für Bestseller-Standardlistenparameter](./media/examplebestsellingparameters.PNG)
1. **Verkäufe aus den letzten X Tagen einbeziehen** – Verkaufsvorgänge, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum getätigt wurden, können zum Bestellen der Produkte verwendet werden. Der obige Standardwert legt nahe, dass alle Einkäufe, die in den letzten 30 Tagen für ein Produkt getätigt wurden, verwendet werden, um die Platzierung des Produkts in der Bestseller-Produktliste zu bestimmen. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Manuelles Hinzufügen oder Entfernen von Produkten aus Empfehlungslisten

### <a name="for-new-trending-or-best-selling"></a>Für Neu, Beliebt oder Bestseller

1.  Gehen Sie zu **Einzelhandel** > **Produktempfehlungen** > **Empfehlungsparameter**.
1.  In der Liste mit freigegebenen Einzelhandelsparametern, wählen Sie **Empfehlungslisten** aus.
1.  Wählen Sie die Liste aus, über die Sie Produkte hinzufügen oder entfernen.
1.  Um der Tabelle Produkte hinzuzufügen, wählen Sie **Zeile hinzufügen** aus. 
1.  Suchen Sie in der Spalte Produkte anhand von **Name** oder **Produktnummer** nach einem Produkt.
![Beispiel zur Suche nach einem Produkt in der neuen Produktliste](./media/examplenewlistconfiguration1.png)
1.  Wählen Sie unter der Spalte Zeilentyp eine von zwei Optionen aus:
    -   **Einschließen** – rückt ein Produkt an die Spitze der Liste
    -   **Ausschließen** – entfernt ein Produkt aus der Liste ![Beispiele für Einschließen oder Ausschließen eines Produktes aus der neuen Produktliste](./media/examplenewlistconfiguration2.png)
1.  Durch das Ändern der **Anzeigereihenfolge** wird die Reihenfolge der Produkte mit der Markierung **Einschließen** in der Liste ändern.
    - Wenn zwei Produkte denselben Wert für **Anzeigereihenfolge** besitzen, dann kann die endgültige Reihenfolge dieser beiden Ergebnisse vom Backoffice abweichen.
1.  So entfernen Sie Produkte aus der Tabelle: Wählen Sie die zu entfernende Zeile und dann **Entfernen** aus.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Für Listen wie Personen gefällt auch oder Wird häufig zusammen gekauft

Im Kontext von Listen wie **Wird häufig zusammen gekauft** oder **Personen gefällt auch** wird das maschinelle Lernen verwendet, um die Kaufmuster von Verbrauchern zu analysieren und so verwandte Produkte zu empfehlen, die gemeinsam für ein einzigartiges Startprodukt gekauft werden. 
 
Ein **Startprodukt** ist das Produkt, für das Sie Ergebnisse generieren möchten. Im Rahmen der manuellen Anpassung von Empfehlungslisten fügen Sie Ergebnisse für dieses Produkt hinzu oder entfernen sie. 

Befolgen Sie diese Schritte, um manuell Ergebnisse für ein Startprodukt hinzuzufügen oder zu entfernen:
1.  Wählen Sie das **Startprodukt** aus. 
1.  Suchen Sie in der Spalte **Produkt** anhand von **Name** oder **Produktnummer** nach einem Produkt.
![Beispiel für die Suche nach einem Produkt in der Liste Wird häufig zusammen gekauft](./media/exampleFBTlistconfiguration1.png)
1. Wählen Sie in der Spalte **Zeilentyp** eine von zwei Optionen aus:
    - **Einschließen** – rückt ein Produkt an die Spitze der Liste
    - **Ausschließen** – Entfernt ein Produkt aus der Liste     
![Beispiel für das Einbeziehen oder Ausschließen eines Produkts in die Liste Wird häufig zusammen gekauft](./media/exampleFBTlistconfiguration2.png)
1.  So entfernen Sie Produkte aus der Tabelle: Wählen Sie die zu entfernende Zeile und dann Entfernen aus.


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Hinzufügen von Produktempfehlungslisten zu Seiten](add-reco-list-to-page.md)
