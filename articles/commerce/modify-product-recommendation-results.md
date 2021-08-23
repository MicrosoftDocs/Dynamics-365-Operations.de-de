---
title: Anpassen von KI-ML-basierten Produktempfehlungsergebnissen
description: In diesem Thema wird erläutert, wie Sie Ergebnisse zu Produktempfehlungen basierend auf maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) an Ihr Unternehmen anpassen.
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
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5374b2ce559134bd26036b06ac6d96a9f5510ab847544707fc9885506aaab547
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748521"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>Anpassen von KI-ML-basierten Produktempfehlungsergebnissen


[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Ergebnisse zu Produktempfehlungen basierend auf maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) an Ihr Unternehmen anpassen. 

Nach dem Aktivieren der Produktempfehlungen werden die Standardeinstellungen wirksam. Diese Parameter können für viele Anforderungen verwendet werden. Es empfiehlt sich, einige Zeit zum Bewerten einzuplanen und festzustellen, ob die Ergebnisse zur Verkaufsbewegung von Produkten passen. Wir empfehlen, die Ergebnisse einige Tage lang auszuwerten, bevor Sie die Parameter nach Bedarf ändern und erneut testen. 

## <a name="understanding-recommendation-list-parameters"></a>Verstehen der Empfehlungslistenparameter

Informieren Sie sich vor dem Ändern der Parameter, wie sich diese auf die folgenden Ergebnisse auswirken.

### <a name="trending-product-list"></a>Populäre Produktliste

Die Bestseller-Produktliste besitzt zwei Parameter, der geändert werden können:

![Beispiel für Bestseller-Standardlistenparameter](./media/exampletrendingparameters.png)

1. **Neue Produkte aus den letzten X Tagen einbeziehen** – Produkte, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum hinzugefügt wurden, können zur Auswahl von Produktkandidaten verwendet werden. Der Standardwert in der Abbildung weist darauf hin, dass Produkte mit einem Alter von 180 Tagen in der Liste der populären Produktliste verwendet werden können.
1. **Verkäufe aus den letzten X Tagen einbeziehen** – Verkaufsvorgänge, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum getätigt wurden, können zum Bestellen der Produkte verwendet werden. Der obige Standardwert legt nahe, dass alle Einkäufe, die in den letzten 30 Tagen für ein Produkt getätigt wurden, verwendet werden, um die Platzierung des Produkts in der Liste der populären Produkte zu bestimmen. 

### <a name="best-selling-product-list"></a>Bestseller-Produktliste

Abhängig von Ihrem Unternehmen kann die Bestseller-Liste andere Ergebnisse als Trends liefern, obwohl beide Transaktionsdaten für die Bestellung von Produkten verwenden. Da Bestseller nicht nach Sortimentsdatum ablaufen, können mit Bestseller immer noch sehr beliebte ältere Produkte hervorgehoben werden, die möglicherweise von der Trendliste gestrichen wurden. 

Die Bestseller-Produktliste besitzt einen Parameter, der geändert werden kann:

![Beispiel für Bestseller-Standardlistenparameter.](./media/examplebestsellingparameters.PNG)

1. **Verkäufe aus den letzten X Tagen einbeziehen** – Verkaufsvorgänge, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum getätigt wurden, können zum Bestellen der Produkte verwendet werden. Der obige Standardwert legt nahe, dass alle Einkäufe, die in den letzten 30 Tagen für ein Produkt getätigt wurden, verwendet werden, um die Platzierung des Produkts in der Bestseller-Produktliste zu bestimmen. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Manuelles Hinzufügen oder Entfernen von Produkten aus Empfehlungslisten

### <a name="for-new-trending-or-best-selling-lists"></a>Für Neu-, Beliebt- oder Bestseller-Listen

1.  Gehen Sie zu **Einzelhandel und Handel** > **Produktempfehlungen** > **Empfehlungsparameter**.
1.  In der Liste der freigegebenen Parameter wählen Sie **Empfehlungs-Listen**.
1.  Wählen Sie die Liste aus, über die Sie Produkte hinzufügen oder entfernen.
1.  Um der Tabelle Produkte hinzuzufügen, wählen Sie **Zeile hinzufügen** aus. 
1.  Suchen Sie in der Spalte Produkt nach einem Produkt **Name** oder **Produktnummer.**

    ![Beispiel für die Suche nach einem Produkt in der Liste Neues Produkt.](./media/examplenewlistconfiguration1.png)

1.  Wählen Sie unter der Spalte Zeilentyp eine von zwei Optionen aus:
    -   **Einschließen** – rückt ein Produkt an die Spitze der Liste
    -   **Ausschließen** – Entfernt ein Produkt aus der Liste
    
    ![Beispiel für das Einschließen oder Ausschließen eines Produkts aus der Liste der neuen Produkte.](./media/examplenewlistconfiguration2.png)

1.  Durch das Ändern der **Anzeigereihenfolge** wird die Reihenfolge der Produkte mit der Markierung **Einschließen** in der Liste ändern.
    - Wenn zwei Produkte denselben Wert für **Anzeigereihenfolge** besitzen, dann kann die endgültige Reihenfolge dieser beiden Ergebnisse vom Backoffice abweichen.
1.  So entfernen Sie Produkte aus der Tabelle: Wählen Sie die zu entfernende Zeile und dann **Entfernen** aus.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Für Listen wie Personen gefällt auch oder Wird häufig zusammen gekauft

Im Kontext von Listen wie Wird häufig zusammen gekauft oder Personen gefällt auch, wird das maschinelle Lernen verwendet, um die Kaufmuster von Verbrauchern zu analysieren und so verwandte Produkte zu empfehlen, die gemeinsam für ein einzigartiges Startprodukt gekauft werden. 
 
Ein *Startprodukt* ist das Produkt, für das Sie Ergebnisse generieren möchten. Im Rahmen der manuellen Anpassung von Empfehlungslisten fügen Sie Ergebnisse für dieses Produkt hinzu oder entfernen sie. 

Befolgen Sie diese Schritte, um manuell Ergebnisse für ein Startprodukt hinzuzufügen oder zu entfernen:
1.  Wählen Sie das **Startprodukt** aus. 
1.  Suchen Sie in der Spalte **Produkt** anhand von **Name** oder **Produktnummer** nach einem Produkt.
![Beispiel für die Suche nach einem Produkt in der Liste Wird häufig zusammen gekauft.](./media/exampleFBTlistconfiguration1.png)
1. Wählen Sie in der Spalte **Zeilentyp** eine von zwei Optionen aus:
    - **Einschließen** – rückt ein Produkt an die Spitze der Liste
    - **Ausschließen** – Entfernt ein Produkt aus der Liste     
![Beispiel für das Einbeziehen oder Ausschließen eines Produkts in die Liste Wird häufig zusammen gekauft.](./media/exampleFBTlistconfiguration2.png)
1.  So entfernen Sie Produkte aus der Tabelle: Wählen Sie die zu entfernende Zeile und dann Entfernen aus.


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Produktempfehlungen in POS hinzufügen](product.md)

[Empfehlungen dem Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]