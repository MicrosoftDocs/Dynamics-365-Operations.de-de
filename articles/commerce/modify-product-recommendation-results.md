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
ms.openlocfilehash: dfe04881e71558ed326025d8f2545c3c611df3aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796969"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="34be9-103">Anpassen von KI-ML-basierten Produktempfehlungsergebnissen</span><span class="sxs-lookup"><span data-stu-id="34be9-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="34be9-104">In diesem Thema wird erläutert, wie Sie Ergebnisse zu Produktempfehlungen basierend auf maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) an Ihr Unternehmen anpassen.</span><span class="sxs-lookup"><span data-stu-id="34be9-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="34be9-105">Nach dem Aktivieren der Produktempfehlungen werden die Standardeinstellungen wirksam. Diese Parameter können für viele Anforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34be9-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="34be9-106">Es empfiehlt sich, einige Zeit zum Bewerten einzuplanen und festzustellen, ob die Ergebnisse zur Verkaufsbewegung von Produkten passen.</span><span class="sxs-lookup"><span data-stu-id="34be9-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="34be9-107">Wir empfehlen, die Ergebnisse einige Tage lang auszuwerten, bevor Sie die Parameter nach Bedarf ändern und erneut testen.</span><span class="sxs-lookup"><span data-stu-id="34be9-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="34be9-108">Verstehen der Empfehlungslistenparameter</span><span class="sxs-lookup"><span data-stu-id="34be9-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="34be9-109">Informieren Sie sich vor dem Ändern der Parameter, wie sich diese auf die folgenden Ergebnisse auswirken.</span><span class="sxs-lookup"><span data-stu-id="34be9-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="34be9-110">Populäre Produktliste</span><span class="sxs-lookup"><span data-stu-id="34be9-110">"Trending" product list</span></span>

<span data-ttu-id="34be9-111">Die Bestseller-Produktliste besitzt zwei Parameter, der geändert werden können:</span><span class="sxs-lookup"><span data-stu-id="34be9-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Beispiel für Bestseller-Standardlistenparameter](./media/exampletrendingparameters.png)

1. <span data-ttu-id="34be9-113">**Neue Produkte aus den letzten X Tagen einbeziehen** – Produkte, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum hinzugefügt wurden, können zur Auswahl von Produktkandidaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34be9-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="34be9-114">Der Standardwert in der Abbildung weist darauf hin, dass Produkte mit einem Alter von 180 Tagen in der Liste der populären Produktliste verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="34be9-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="34be9-115">**Verkäufe aus den letzten X Tagen einbeziehen** – Verkaufsvorgänge, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum getätigt wurden, können zum Bestellen der Produkte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34be9-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="34be9-116">Der obige Standardwert legt nahe, dass alle Einkäufe, die in den letzten 30 Tagen für ein Produkt getätigt wurden, verwendet werden, um die Platzierung des Produkts in der Liste der populären Produkte zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="34be9-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="34be9-117">Bestseller-Produktliste</span><span class="sxs-lookup"><span data-stu-id="34be9-117">"Best selling" product list</span></span>

<span data-ttu-id="34be9-118">Abhängig von Ihrem Unternehmen kann die Bestseller-Liste andere Ergebnisse als Trends liefern, obwohl beide Transaktionsdaten für die Bestellung von Produkten verwenden.</span><span class="sxs-lookup"><span data-stu-id="34be9-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="34be9-119">Da Bestseller nicht nach Sortimentsdatum ablaufen, können mit Bestseller immer noch sehr beliebte ältere Produkte hervorgehoben werden, die möglicherweise von der Trendliste gestrichen wurden.</span><span class="sxs-lookup"><span data-stu-id="34be9-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="34be9-120">Die Bestseller-Produktliste besitzt einen Parameter, der geändert werden kann:</span><span class="sxs-lookup"><span data-stu-id="34be9-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Beispiel für Bestseller-Standardlistenparameter](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="34be9-122">**Verkäufe aus den letzten X Tagen einbeziehen** – Verkaufsvorgänge, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum getätigt wurden, können zum Bestellen der Produkte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34be9-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="34be9-123">Der obige Standardwert legt nahe, dass alle Einkäufe, die in den letzten 30 Tagen für ein Produkt getätigt wurden, verwendet werden, um die Platzierung des Produkts in der Bestseller-Produktliste zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="34be9-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="34be9-124">Manuelles Hinzufügen oder Entfernen von Produkten aus Empfehlungslisten</span><span class="sxs-lookup"><span data-stu-id="34be9-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="34be9-125">Für Neu-, Beliebt- oder Bestseller-Listen</span><span class="sxs-lookup"><span data-stu-id="34be9-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="34be9-126">Gehen Sie zu **Einzelhandel und Handel** > **Produktempfehlungen** > **Empfehlungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="34be9-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="34be9-127">In der Liste der freigegebenen Parameter wählen Sie **Empfehlungs-Listen**.</span><span class="sxs-lookup"><span data-stu-id="34be9-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="34be9-128">Wählen Sie die Liste aus, über die Sie Produkte hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="34be9-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="34be9-129">Um der Tabelle Produkte hinzuzufügen, wählen Sie **Zeile hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="34be9-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="34be9-130">Suchen Sie in der Spalte Produkt nach einem Produkt **Name** oder **Produktnummer.**</span><span class="sxs-lookup"><span data-stu-id="34be9-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Beispiel für die Suche nach einem Produkt in der Liste Neues Produkt](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="34be9-132">Wählen Sie unter der Spalte Zeilentyp eine von zwei Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="34be9-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="34be9-133">**Einschließen** – rückt ein Produkt an die Spitze der Liste</span><span class="sxs-lookup"><span data-stu-id="34be9-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="34be9-134">**Ausschließen** – Entfernt ein Produkt aus der Liste</span><span class="sxs-lookup"><span data-stu-id="34be9-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Beispiel für das Einschließen oder Ausschließen eines Produkts aus der Liste der neuen Produkte](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="34be9-136">Durch das Ändern der **Anzeigereihenfolge** wird die Reihenfolge der Produkte mit der Markierung **Einschließen** in der Liste ändern.</span><span class="sxs-lookup"><span data-stu-id="34be9-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="34be9-137">Wenn zwei Produkte denselben Wert für **Anzeigereihenfolge** besitzen, dann kann die endgültige Reihenfolge dieser beiden Ergebnisse vom Backoffice abweichen.</span><span class="sxs-lookup"><span data-stu-id="34be9-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="34be9-138">So entfernen Sie Produkte aus der Tabelle: Wählen Sie die zu entfernende Zeile und dann **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="34be9-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="34be9-139">Für Listen wie Personen gefällt auch oder Wird häufig zusammen gekauft</span><span class="sxs-lookup"><span data-stu-id="34be9-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="34be9-140">Im Kontext von Listen wie Wird häufig zusammen gekauft oder Personen gefällt auch, wird das maschinelle Lernen verwendet, um die Kaufmuster von Verbrauchern zu analysieren und so verwandte Produkte zu empfehlen, die gemeinsam für ein einzigartiges Startprodukt gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="34be9-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="34be9-141">Ein *Startprodukt* ist das Produkt, für das Sie Ergebnisse generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="34be9-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="34be9-142">Im Rahmen der manuellen Anpassung von Empfehlungslisten fügen Sie Ergebnisse für dieses Produkt hinzu oder entfernen sie.</span><span class="sxs-lookup"><span data-stu-id="34be9-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="34be9-143">Befolgen Sie diese Schritte, um manuell Ergebnisse für ein Startprodukt hinzuzufügen oder zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="34be9-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="34be9-144">Wählen Sie das **Startprodukt** aus.</span><span class="sxs-lookup"><span data-stu-id="34be9-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="34be9-145">Suchen Sie in der Spalte **Produkt** anhand von **Name** oder **Produktnummer** nach einem Produkt.
![Beispiel für die Suche nach einem Produkt in der Liste Wird häufig zusammen gekauft](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="34be9-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="34be9-146">Wählen Sie in der Spalte **Zeilentyp** eine von zwei Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="34be9-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="34be9-147">**Einschließen** – rückt ein Produkt an die Spitze der Liste</span><span class="sxs-lookup"><span data-stu-id="34be9-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="34be9-148">**Ausschließen** – Entfernt ein Produkt aus der Liste</span><span class="sxs-lookup"><span data-stu-id="34be9-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="34be9-149">![Beispiel für das Einbeziehen oder Ausschließen eines Produkts in die Liste Wird häufig zusammen gekauft](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="34be9-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="34be9-150">So entfernen Sie Produkte aus der Tabelle: Wählen Sie die zu entfernende Zeile und dann Entfernen aus.</span><span class="sxs-lookup"><span data-stu-id="34be9-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="34be9-151">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34be9-151">Additional resources</span></span>

[<span data-ttu-id="34be9-152">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="34be9-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="34be9-153">Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung</span><span class="sxs-lookup"><span data-stu-id="34be9-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="34be9-154">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="34be9-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="34be9-155">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="34be9-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="34be9-156">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="34be9-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="34be9-157">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="34be9-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="34be9-158">Produktempfehlungen in POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="34be9-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="34be9-159">Empfehlungen dem Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="34be9-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="34be9-160">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="34be9-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="34be9-161">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="34be9-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="34be9-162">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="34be9-162">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]